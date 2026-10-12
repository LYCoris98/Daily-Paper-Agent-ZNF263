## 01 基本信息

- **标题**：Cerberus: bidirectional state space blocks improve accuracy and efficiency of regulatory sequence models
- **作者**：Kelley DR; Yuan H; Huang X; Linder J
- **单位**：未提供
- **期刊/平台**：bioRxiv（预印本）
- **年份**：2026
- **论文类型**：预印本（方法学 + 基准评测）
- **领域**：调控基因组学、序列-功能预测模型、state space models、深度学习架构
- **关键词**：Cerberus、Hydra、Mamba-2、bidirectional state space、regulatory sequence models、eQTL、variant effect prediction
- **DOI/ID**：10.64898/2026.10.02.756377
- **代码**：作者声明发布训练与评估代码（具体仓库未提供）
- **数据**：作者声明发布训练数据与基准集（具体链接未提供）
- **阅读日期**：未提供
- **在「cpdch基因家族」方向中的位置**：本文不涉及cpdch基因家族，属于调控序列建模的通用方法学论文。其可迁移价值在于：state space block架构、长程调控建模策略、eQTL/variant effect评测协议，以及模型可解释性方法，均可迁移至cpdch基因家族的调控机制研究。

## 02 一句话总结

本文用Mamba-2构建双向state space block（Hydra）替换Borzoi的transformer块，在保持训练数据与其余架构不变的前提下，实现5.7倍加速和更高的eQTL分类/效应量预测精度，并据此构建786 kb输入的Cerberus集成模型，在GTEx v11三个表型基准上超越Borzoi。

## 03 研究问题

- **具体问题**：在参考基因组提供的独特训练序列有限、新实验只增加标签不增加序列的约束下，如何设计序列-功能模型的架构，使其从有限的序列多样性中学到更多、更准确的调控规则？
- **为什么重要**：基因组序列是固定的，训练数据多样性受限于参考基因组本身；架构效率与表达能力直接决定模型能否在有限数据上达到更高精度，并支持更长输入（覆盖更多调控元件）。
- **现有方法为何不足**：Borzoi等领先模型依赖self-attention计算长程相互作用，其计算成本随序列长度二次增长，限制了输入长度与分辨率；U-net decoder等结构增加了参数与复杂度，但未必带来相应的精度收益。
- **精确研究问题**：Can bidirectional state space blocks (Hydra) replace transformer blocks in regulatory sequence models to improve both accuracy and efficiency, and can scaling such an architecture produce a model (Cerberus) that outperforms existing models on eQTL/sQTL/paQTL variant effect benchmarks?

## 04 背景与发展脉络

*注：此脉络为「仅本文框架」——基于本文引言与方法的叙述整理，未经外部文献核验。*

1. **阶段一：卷积网络时代**（如Basenji系列早期版本）
   - 代表性方法：全卷积网络，局部motif检测 + 层级池化
   - 优点：计算高效、适合局部序列特征
   - 局限：感受野有限，长程调控信息捕获能力弱

2. **阶段二：Transformer/self-attention时代**（如Borzoi）
   - 代表性方法：Borzoi，用self-attention计算长程相互作用
   - 优点：能建模远距离调控关系，精度显著提升
   - 局限：attention计算成本随序列长度二次增长，限制输入长度与分辨率；需要U-net decoder等辅助结构

3. **阶段三：State space models时代**（本文主张的位置）
   - 代表性方法：Mamba-2、Hydra（本文）、Cerberus（本文）
   - 优点：线性计算成本支持更长输入与更高分辨率；双向设计保留上下游上下文；精度超越transformer基线
   - 局限：SSM的机制可解释性仍在探索中（本文通过block深度分析部分回应）

## 05 核心痛点

| 痛点 | 表现 | 成因或作者解释 | 文中证据 |
|------|------|----------------|----------|
| 训练序列多样性受限 | 参考基因组提供有限的独特序列，新实验只增加标签不增加序列 | 基因组序列是固定的生物学事实 | 摘要「The reference genome caps unique training sequences, and new assays add labels, not sequences」 |
| Transformer计算成本高 | self-attention在长序列上计算量二次增长，限制输入长度与分辨率 | attention机制固有的O(L²)复杂度 | 摘要「leading models such as Borzoi compute long-range interactions with self-attention」；「Hydra blocks ran 5.7-fold faster on 8,192-token inputs」 |
| 现有模型精度瓶颈 | Borzoi在eQTL分类与效应量估计上仍有提升空间 | 架构效率限制模型规模与输入覆盖范围 | 摘要中Cerberus vs Borzoi的eQTL AUPRC 0.692 vs 0.668、Spearman ρ 0.379 vs 0.321 |
| 基准评测混杂因素 | eQTL基准中阴性对照可能受等位基因频率、基因表达、位置注释等混杂 | 这些属性与调控功能相关，若不匹配会虚高精度 | 摘要「negatives matched on allele frequency, gene expression, and phenotype-specific positional annotations to reduce confounding」 |

## 06 核心思想

1. **表面方法**：用Mamba-2构建双向state space block（Hydra），替换Borzoi的transformer块；利用SSM的线性复杂度在32 bp分辨率下运行blocks，移除U-net decoder；将架构扩展到786 kb输入并集成8个模型，形成Cerberus。

2. **核心洞察**：调控序列建模的核心瓶颈不是模型容量，而是架构在有限序列多样性下的学习效率。SSM的线性计算成本允许模型在更高分辨率（32 bp vs 更低分辨率）和更长输入（786 kb）下运行，从而让模型直接看到更多原始序列信息，而非依赖U-net等结构进行隐式信息压缩。双向设计确保每个位置同时获得上下游上下文，这对调控元件（如enhancer-promoter interaction）的方向性至关重要。

3. **可能的普适教训** [Analysis]：在数据多样性受限的生物学问题中，架构的「信息效率」比「参数容量」更重要——与其增加模型复杂度，不如让模型在更高分辨率、更长上下文下直接处理原始数据。这一原则可能适用于cpdch基因家族研究：如果训练数据有限，优先考虑能高效利用长上下文的架构，而非堆叠更多参数。

## 07 方法总览

- **输入**：DNA序列（Cerberus为786 kb；Hydra对比实验为8,192 tokens）
- **输出**：调控活性预测（coverage tracks，即基因组区间的预测信号）；下游任务为eQTL/sQTL/paQTL variant effect分类与效应量估计
- **核心模块**：
  1. 卷积前端（stem）：提取局部序列特征（motif检测）
  2. Hydra blocks（双向SSM）：建模长程相互作用，替代transformer
  3. 输出头：预测多track的coverage（无U-net decoder）
- **训练**：在增强的track集合上训练（augmented track collection）；集成8个模型
- **工具**：Mamba-2（SSM实现）；未提供其他框架细节
- **反馈回路**：未明确描述（如是否使用迭代训练/自蒸馏，未提供）
- **文字流程**：DNA序列 → 卷积stem提取局部特征 → 多层Hydra blocks（双向SSM）逐层扩大感受野 → 输出头直接预测各track的coverage → 下游任务中，对variant进行in silico突变（参考序列 vs 突变序列的预测差异）→ 分类/排序variant

## 08 核心模块拆解

| 模块 | 功能 | 为何需要 | 输入输出 | 支撑证据 | 移除后的已知或预期影响 |
|------|------|----------|----------|----------|------------------------|
| 卷积stem | 提取局部序列特征（motif） | 为SSM提供局部归纳偏置，降低序列长度 | 输入：raw DNA序列；输出：token序列 | 未提供消融实验 | [预期] 移除后SSM需从头学习局部特征，可能降低小数据下的精度 |
| Hydra blocks（双向SSM） | 建模长程调控相互作用 | 线性计算成本支持更高分辨率与更长输入；双向设计捕获上下游上下文 | 输入：卷积stem输出；输出：上下文增强的表示 | 5.7倍加速（8,192 tokens）；eQTL分类与效应量精度优于transformer | [实测] 替换为transformer后精度下降（对比实验）；[预期] 移除后模型退化为纯卷积，长程建模能力大幅下降 |
| 32 bp分辨率运行 | 在更高分辨率下处理序列 | 保留更多原始序列信息，减少信息丢失 | 输入：32 bp bins；输出：每bin的预测 | 移除U-net后精度仍提升 | [预期] 若降回低分辨率，需重新引入U-net等decoder，增加复杂度且可能降低精度 |
| 无U-net decoder | 直接输出coverage | SSM线性复杂度使高分辨率直接预测成为可能，无需U-net进行上采样 | 输入：Hydra blocks输出；输出：coverage tracks | 模型更小且更精确 | [实测] 移除U-net后模型更小、更精确（作者主张） |
| 集成（8个模型） | 降低单模型方差，提升鲁棒性 | 单模型可能对特定序列区域有偏 | 输入：8个模型预测；输出：集成预测 | Cerberus整体精度报告 | [预期] 移除集成后精度可能下降，但具体幅度未提供 |
| 基准匹配（negatives matching） | 控制混杂因素 | 等位基因频率、基因表达、位置注释等与调控功能相关，不匹配会虚高精度 | 输入：variant集合；输出：匹配后的正负集 | 摘要明确描述匹配策略 | [预期] 不匹配时精度可能虚高，但作者未提供对比数据 |

## 09 关键公式符号

不适用。本文为方法学/基准评测论文，摘要与正文中未提供需要单独列出的数学公式。模型核心为Mamba-2的state space formulation（外部文献），但本文未在提供的材料中复述。

## 10 实验设计与证据链

- **数据集/群体**：GTEx v11 fine-mapped eQTL、sQTL、paQTL基准；训练数据为增强的track集合（augmented track collection，具体内容未提供）
- **规模**：eQTL基准覆盖48个组织；Cerberus输入786 kb；Hydra对比实验输入8,192 tokens
- **指标**：AUPRC（eQTL分类）、Spearman ρ（效应量估计）
- **基线**：Borzoi（transformer架构）；AlphaGenome（对比模型）
- **预算**：未提供
- **骨干/仪器**：未提供（GPU型号、训练时长等未说明）
- **oracle输入**：不适用（无人工标注的oracle输入；模型输入为DNA序列）
- **评测协议**：fine-mapped variant分类（正负集匹配等位基因频率、基因表达、位置注释）；效应量估计用Spearman相关

| 实验 | 检验的claim | 对比与条件 | 结果 | 支持的结论 | 不支持更强的结论 | 来源 |
|------|------------|------------|------|-------------|-------------------|------|
| Hydra vs Borzoi blocks（速度） | SSM比transformer更高效 | 相同输入长度8,192 tokens，其余架构与训练数据固定 | 5.7倍加速 | SSM在长序列上计算效率显著优于transformer | 未提供不同长度下的扩展性曲线 | 摘要 |
| Hydra vs Borzoi blocks（精度） | SSM在有限数据下学习效率更高 | 相同训练数据与其余架构 | eQTL分类与效应量精度更高 | SSM架构在调控序列建模上优于transformer | 未提供具体数值（除最终模型外） | 摘要 |
| Cerberus vs Borzoi（eQTL） | 扩展后的SSM模型超越transformer基线 | GTEx v11 fine-mapped eQTL，48组织 | AUPRC 0.692 vs 0.668；Spearman ρ 0.379 vs 0.321 | Cerberus在eQTL分类与效应量估计上均优于Borzoi | 未提供显著性检验 | 摘要 |
| Cerberus vs AlphaGenome（eQTL） | Cerberus与另一领先模型对比 | 同上 | 互有胜负：3-100 kb区域领先，coding sequence及3 kb内落后 | Cerberus在中距离调控上优势明显，近端/编码区仍有不足 | 未提供具体数值 | 摘要 |
| Cerberus（sQTL/paQTL） | 泛化到其他调控表型 | GTEx v11 fine-mapped sQTL、paQTL | 均优于Borzoi | SSM架构泛化到多种调控表型 | 未提供具体数值 | 摘要 |
| Block深度可解释性 | 深层blocks捕获更长的调控相互作用 | 对训练后blocks进行归因分析 | 相互作用范围从第1个block的0.9 kb中位半衰期增长到第7个的79 kb；最深层的heads锚定在promoter、enhancer、CTCF peaks | 模型层级结构对应调控相互作用的距离层级 | 未提供与生物学机制的因果验证 | 摘要 |

## 11 结论正确解读

- **任务范围**：本文结论限于调控序列建模（coverage prediction）与variant effect预测（eQTL/sQTL/paQTL），不涉及其他序列-功能任务（如 splicing、methylation等）。
- **oracle/真值输入**：eQTL等基准使用GTEx fine-mapped variants，属于实验观测数据，非人工构造的oracle；模型输入仅为DNA序列，无其他细胞类型或环境信息。
- **端到端状态**：Cerberus是端到端训练的序列-功能模型，但下游variant effect预测依赖in silico突变（参考 vs 突变序列预测差异），属于零样本（zero-shot）迁移，未针对eQTL任务微调。
- **算力成本**：未提供训练成本、GPU数量、训练时长等关键信息，无法评估部署门槛。
- **历史数据依赖**：训练数据为增强的track集合，具体来源、版本、是否包含GTEx数据未说明；若训练数据与评测基准存在重叠，可能引入数据泄漏风险（作者未讨论）。
- **模型依赖**：结论基于Mamba-2实现；其他SSM变体（如S4、Hyena）是否同样有效未验证。
- **最难情形**：Cerberus在coding sequence及距TSS 3 kb以内的variant上落后于AlphaGenome，说明近端调控/编码区变异仍是难点。
- **群体/领域边界**：评测限于GTEx（人类组织），未涉及其他物种或细胞系；fine-mapped variants的可靠性依赖GTEx的统计推断质量。
- **不确定性**：未提供置信区间、显著性检验或多次运行的标准差；集成模型的个体差异未报告。
- **有边界的复述**：在GTEx v11 fine-mapped eQTL/sQTL/paQTL基准上，以786 kb输入、32 bp分辨率、8模型集成的SSM架构（Cerberus），在eQTL分类（AUPRC 0.692 vs 0.668）和效应量估计（ρ 0.379 vs 0.321）上优于Borzoi，并在3-100 kb区间优于AlphaGenome，但在近端（<3 kb）和编码区落后。

## 12 作者自认局限

在提供的材料（摘要）中未发现作者明确承认的局限。

**作者提及的相关约束**（非正式局限）：
- 参考基因组本身限制了训练序列多样性（摘要首句），这是问题背景而非作者承认的模型局限。
- Cerberus在coding sequence和距TSS 3 kb内落后于AlphaGenome（摘要），作者将其作为对比结果报告，未展开讨论原因或承认为局限。

## 13 批判性分析

| [Analysis] 观察 | 潜在问题或替代解释 | 为何重要 | 如何检验 | 依据 |
|-----------------|---------------------|----------|----------|------|
| 训练数据与评测基准可能重叠 | 增强的track集合若包含GTEx相关数据，eQTL评测可能受数据泄漏影响 | 数据泄漏会虚高精度，影响结论可信度 | 检查训练track集合是否包含GTEx eQTL输入特征；在完全排除重叠的基准上重测 | 摘要未说明训练数据来源 |
| 未提供显著性检验与置信区间 | 0.692 vs 0.668的AUPRC差异可能不显著 | 无法判断精度提升是否稳健 | 要求作者提供多次运行的标准差、配对检验或bootstrap CI | 摘要仅报告点估计 |
| 与AlphaGenome的对比不完整 | 仅报告「互有胜负」，未给出具体数值和区域划分标准 | 无法评估整体优劣和差异幅度 | 获取完整对比数据，按距离、注释类别分层分析 | 摘要描述模糊 |
| 可解释性分析（block深度）缺乏因果验证 | 归因分析显示深层blocks锚定调控元件，但这是相关性而非因果性 | 过度解读可解释性可能误导对模型机制的理解 | 进行in silico扰动实验（如删除特定block）验证其对特定调控相互作用的必要性 | 摘要仅报告相关性 |
| 未报告模型在非GTEx数据上的泛化 | 仅评测人类组织eQTL/sQTL/paQTL，未涉及其他物种、细胞系或表型 | 泛化能力未知，可能过拟合GTEx特征 | 在ENCODE、FANTOM等独立数据上评测 | 摘要未提及 |
| 计算成本报告不完整 | 5.7倍加速仅针对block替换，未报告整体训练/推理成本 | 无法评估实际部署价值 | 要求提供端到端训练时间、GPU资源、推理延迟 | 摘要仅报告block级加速 |

## 14 Agent 提炼的知识候选

**标题：Agent 提炼的知识候选**

1. **双向SSM架构设计**：Hydra的双向state space block设计（基于Mamba-2）可直接迁移至cpdch基因家族的调控建模。若需预测cpdch基因在不同细胞类型/条件下的表达调控，可构建以cpdch基因座为中心、覆盖上下游调控元件的长序列输入，用双向SSM捕获enhancer-promoter相互作用。

2. **高分辨率输入策略**：利用SSM的线性复杂度在32 bp分辨率下运行，移除U-net decoder。对cpdch基因家族研究，这意味着可以在不牺牲计算效率的前提下，对cpdch基因座及其调控区域进行高分辨率建模，保留更精细的序列特征（如转录因子结合位点的精确位置）。

3. **基准构建与负样本匹配**：Cerberus的评测协议（负样本匹配等位基因频率、基因表达、位置注释）可直接迁移至cpdch基因家族的variant effect研究。若研究cpdch基因相关疾病变异，应采用同样的匹配策略构建阴性对照，避免混杂因素导致的假阳性。

4. **模型可解释性分析**：通过分析不同深度block的相互作用范围（0.9 kb到79 kb）和锚定元件类型，可迁移至cpdch基因家族研究：训练类似模型后，可分析哪些block/层对应cpdch基因的启动子-增强子相互作用，从而定位关键调控元件。

5. **集成策略**：8模型集成提升鲁棒性。对cpdch基因家族研究，若单模型预测不稳定，可采用类似集成策略降低方差。

6. **零样本variant effect预测**：Cerberus通过in silico突变（参考 vs 突变序列预测差异）进行variant effect预测，无需针对特定表型微调。此方法可直接迁移至cpdch基因家族：对cpdch基因座内的SNV/indel进行in silico突变扫描，预测其调控效应。

## 15 与已有知识连接

- **Mamba-2/SSM文献**：本文基于Mamba-2构建Hydra，与state space model在序列建模中的进展直接相关（如Gu & Dao的Mamba系列）。[Analysis] 读者可对比S4、Hyena等其他SSM变体在调控序列建模上的表现。
- **Borzoi/Enformer系列**：本文以Borzoi为基线，属于调控序列模型（regulatory sequence models）的发展脉络。cpdch基因家族研究者若熟悉Basenji/Borzoi/Enformer，可快速理解本文的改进点。
- **GTEx eQTL/sQTL/paQTL资源**：评测基准基于GTEx v11，这是人类调控 genomics 的标准资源。cpdch基因家族研究若涉及人类组织表达调控，可直接使用同一基准或GTEx数据。
- **AlphaGenome**：作为对比模型，代表另一类调控序列建模方法。[Analysis] 读者可查阅AlphaGenome原文了解其架构差异。
- **可解释性方法**：block深度归因分析属于模型可解释性范畴，与feature attribution、attention analysis等方法论相关。
- **与cpdch基因家族的连接** [Analysis]：cpdch基因家族（若涉及调控研究）可借鉴本文的架构选择（SSM vs transformer）、输入分辨率策略、基准构建方法，以及零样本variant effect预测流程。但本文未涉及cpdch基因家族，所有迁移均为方法论层面的借鉴。

## 16 Agent 生成的研究候选

**标题：Agent 生成的研究候选**

1. **候选名称**：cpdch基因座双向SSM调控模型
   - **来源局限/观察**：Cerberus证明双向SSM在长序列调控建模上优于transformer；cpdch基因家族若存在长程调控机制，可借鉴此架构。
   - **核心假设**：cpdch基因座的调控依赖于距TSS数十kb至数百kb的增强子，双向SSM能比transformer更高效地捕获这些相互作用。
   - **相对本文的增量**：将架构迁移至特定基因家族（cpdch），并针对该基因家族优化输入区域选择。
   - **初步方法**：以cpdch基因TSS为中心，取±400 kb序列输入，用Hydra blocks构建模型，预测cpdch基因在GTEx各组织的表达；与Borzoi对比。
   - **验证方式**：GTEx eQTL基准中cpdch基因相关变异的分类精度；独立ChIP-seq验证预测的增强子区域。
   - **可能的失败模式**：cpdch基因家族可能不存在长程调控，或SSM优势在短基因座上不显著。
   - **创新状态**：unverified

2. **候选名称**：cpdch基因家族variant effect零样本预测流程
   - **来源局限/观察**：Cerberus的in silico突变流程无需微调即可预测variant effect；cpdch基因家族相关疾病变异的功能注释可能缺乏实验数据。
   - **核心假设**：Cerberus（或类似SSM模型）对cpdch基因座内变异的零样本预测能有效区分致病/良性变异。
   - **相对本文的增量**：将通用模型应用于特定基因家族，并整合ClinVar/gnomAD中cpdch相关变异进行验证。
   - **初步方法**：下载Cerberus模型，对cpdch基因座内所有常见/罕见变异进行in silico突变扫描，输出效应分数；与ClinVar标注比较。
   - **验证方式**：ClinVar中cpdch相关变异的AUC/PRC；与MPRA（massively parallel reporter assay）数据对比。
   - **可能的失败模式**：零样本预测对特定基因家族可能系统性偏差；ClinVar标注稀疏。
   - **创新状态**：partially checked（方法已存在，但未应用于cpdch）

3. **候选名称**：cpdch基因家族调控层级可解释性分析
   - **来源局限/观察**：Cerberus的block深度分析显示相互作用范围随深度增长（0.9 kb→79 kb），且深层锚定调控元件；cpdch基因家族的调控层级未知。
   - **核心假设**：cpdch基因座的调控层级遵循「近端启动子→远端增强子→CTCF边界」的距离递增模式，且可通过SSM模型的层级归因揭示。
   - **相对本文的增量**：将归因分析从通用基因组扩展到特定基因家族，并关联cpdch基因家族成员间的差异调控。
   - **初步方法**：训练cpdch基因座SSM模型，对每层block计算相互作用半衰期和锚定元件类型；比较cpdch家族不同成员的调控层级差异。
   - **验证方式**：Hi-C数据验证预测的增强子-启动子相互作用；CRISPR干扰（CRISPRi）验证关键增强子。
   - **可能的失败模式**：归因分析可能仅反映模型内部表征，而非真实生物学机制。
   - **创新状态**：unverified

4. **候选名称**：cpdch基因家族跨物种调控保守性分析
   - **来源局限/观察**：Cerberus在人类GTEx数据上评测；cpdch基因家族的调控保守性可能揭示核心调控元件。
   - **核心假设**：cpdch基因家族的核心调控元件在哺乳动物中保守，且SSM模型能跨物种迁移预测。
   - **相对本文的增量**：将模型从人类扩展到多物种，并聚焦特定基因家族。
   - **初步方法**：用人类训练的Cerberus对小鼠、大鼠等物种的cpdch同源基因座进行预测，比较调控图谱；鉴定保守调控元件。
   - **验证方式**：跨物种ChIP-seq/ATAC-seq一致性；转基因报告实验验证保守增强子。
   - **可能的失败模式**：跨物种序列差异可能导致模型预测失效；保守性分析可能受比对质量影响。
   - **创新状态**：unverified