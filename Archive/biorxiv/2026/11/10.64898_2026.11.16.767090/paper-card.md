## 01 基本信息

- **标题**：CTCF-anchored cohesin loops are a vertebrate-specific innovation
- **作者**：Aihara H; Narita T; Maskey E; Nguyen TBN; Higashijima Y; Yamaguchi Y; Krietenstein N; Choudhary C
- **单位**：Novo Nordisk Foundation Center for Protein Research（哥本哈根大学）；岛根大学；宫崎大学等（具体单位对应关系未提供）
- **期刊/平台**：bioRxiv（预印本）
- **年份**：2026-11-17
- **论文类型**：预印本（研究论文）
- **领域**：3D基因组结构、染色质环挤压、进化发育生物学、比较基因组学
- **关键词**：CTCF、cohesin、loop extrusion、chromatin loops、vertebrate evolution、Micro-C、ChIP-seq
- **DOI/ID**：10.64898/2026.11.16.767090
- **代码**：未提供（分析流程基于公开工具：distiller、cooltools、LS-GKM、TF-MoDISco等）
- **数据**：NCBI GEO accession GSE353712（本研究的ChIP-seq和Micro-C数据）；重分析公开数据：小鼠ESC CTCF (GSE178982)、RAD21 (GSE178982)、H3K27ac (GSE146328)、H3K4me3 (GSE186349)、ATAC-seq (GSE146328)
- **阅读日期**：未提供
- **在「cpdch基因家族」方向中的位置**：该文不直接研究cpdch基因家族，但为研究基因家族成员的染色质调控功能提供了关键方法学框架——通过跨物种结构域交换（domain-swap）结合ChIP-seq/Micro-C来鉴定特定蛋白结构域的功能进化，该策略可直接迁移至cpdch家族成员的功能结构域解析。

## 02 一句话总结

通过跨物种CTCF N端结构域交换实验（小鼠、果蝇、文昌鱼、盲鳗）结合Micro-C和ChIP-seq分析，证明CTCF介导的cohesin环锚定功能（依赖N端YxF基序及ZF1-2）是脊椎动物特有的创新，该功能在脊椎动物祖先中进化获得，并在有颌类中进一步增强。

## 03 研究问题

- **具体问题**：CTCF获得cohesin环锚定（loop-halting）功能的进化时间点是什么？该功能是否为脊椎动物特有？
- **为什么重要**：CTCF-anchored cohesin loops是哺乳动物3D基因组组织的核心机制，对增强子-启动子互作和基因表达调控至关重要。理解该功能的进化起源有助于阐明3D基因组组织的进化逻辑，以及为何脊椎动物依赖这种独特的基因组折叠机制。
- **现有方法不足**：此前研究主要基于序列保守性分析（如YxF基序的存在与否），但序列保守并不等于功能保守；且缺乏直接的功能实验证据来区分"基序存在"与"功能获得"。
- **精确研究问题**：Can the N-terminus of invertebrate CTCF (Drosophila, Branchiostoma) functionally replace the mouse CTCF N-terminus in supporting cohesin loop anchoring, and does the hagfish (jawless vertebrate) N-terminus retain this function?

## 04 背景与发展脉络

*注：以下脉络基于本文框架，未经外部系统核验。*

1. **早期阶段（2010s初）**：Hi-C技术揭示哺乳动物基因组存在TADs和染色质环；CTCF和cohesin被鉴定为关键组织因子。
2. **机制阐明阶段（2010s中）**：loop extrusion模型提出——cohesin挤出染色质环，CTCF以方向依赖方式（convergent orientation）阻止cohesin前进；YxF基序（小鼠226-228）和KTYQR基序（小鼠23-27）被鉴定为cohesin互作关键位点。
3. **比较基因组学阶段（2010s末-2020s初）**：发现CTCF广泛存在于两侧对称动物（bilaterians），但功能差异显著——果蝇CTCF主要作为insulator蛋白，而非cohesin环锚；部分无脊椎动物（如软体动物）缺乏YxF基序。
4. **本文位置**：首次通过跨物种功能置换实验（domain-swap）直接检验CTCF N端功能的进化保守性，结合原生组织（盲鳗）的Micro-C数据，将CTCF环锚定功能的起源定位于脊椎动物祖先。

## 05 核心痛点

| 痛点 | 表现 | 成因或作者解释 | 文中证据 |
|------|------|----------------|----------|
| 序列保守≠功能保守 | YxF基序在果蝇、文昌鱼、盲鳗中均存在，但功能差异巨大 | 仅凭基序存在无法判断是否具有cohesin环锚定功能；可能需要额外的N端序列特征或ZF1-2的协同 | Results 图1A；Discussion |
| 无脊椎动物CTCF功能难以在哺乳动物细胞中评估 | 无法直接在果蝇/文昌鱼中检测CTCF的cohesin环锚定功能 | 缺乏合适的实验系统；果蝇CTCF功能与脊椎动物不同 | Results 图2 |
| 基序预测与功能验证脱节 | AlphaFold预测显示文昌鱼和盲鳗N端均可与RAD21-STAG2互作，但功能差异显著 | 结构预测无法捕捉动态互作强度或体内功能的细微差异 | Supplemental 图3A |
| 进化推断缺乏直接功能证据 | 此前研究仅基于序列分析推断CTCF功能进化 | 缺乏跨物种功能置换实验和原生组织的3D基因组数据 | Introduction；Results |

## 05 核心痛点

| 痛点 | 表现 | 成因或作者解释 | 文中证据 |
|------|------|----------------|----------|
| 序列保守≠功能保守 | YxF基序在果蝇、文昌鱼、盲鳗中均存在，但功能差异巨大 | 仅凭基序存在无法判断是否具有cohesin环锚定功能；可能需要额外的N端序列特征或ZF1-2的协同 | Results 图1A；Discussion |
| 无脊椎动物CTCF功能难以在哺乳动物细胞中评估 | 无法直接在果蝇/文昌鱼中检测CTCF的cohesin环锚定功能 | 缺乏合适的实验系统；果蝇CTCF功能与脊椎动物不同 | Results 图2 |
| 基序预测与功能验证脱节 | AlphaFold预测显示文昌鱼和盲鳗N端均可与RAD21-STAG2互作，但功能差异显著 | 结构预测无法捕捉动态互作强度或体内功能的细微差异 | Supplemental 图3A |
| 进化推断缺乏直接功能证据 | 此前研究仅基于序列分析推断CTCF功能进化 | 缺乏跨物种功能置换实验和原生组织的3D基因组数据 | Introduction；Results |

## 06 核心思想

1. **表面方法**：构建等位基因特异性的小鼠胚胎干细胞（mESC）系统，一个等位基因表达dTAG标记的野生型CTCF，另一个等位基因表达bTAG标记的N端缺失或N端跨物种置换的CTCF变体。通过选择性降解野生型CTCF，评估各变体维持cohesin（RAD21）富集的能力。同时，对盲鳗肝脏组织进行CTCF/RAD21 ChIP-seq和Micro-C分析，检验内源功能。

2. **核心洞察**：CTCF的cohesin环锚定功能不是由单一基序（如YxF）决定的，而是需要N端多个区域（包括YxF和ZF1-2）的协同进化。果蝇和文昌鱼N端虽然含有YxF基序，但缺乏足够的序列上下文来支持cohesin互作；盲鳗N端则已获得该功能，但效率低于小鼠，提示该功能在脊椎动物中经历了"获得-强化"的两步进化。

3. **[Analysis] 可能的普适教训**：功能进化研究不能仅依赖序列基序保守性分析，需要结合跨物种功能置换实验来直接检验"基序存在"与"功能获得"之间的因果关系。该方法可推广至其他蛋白家族（如cpdch基因家族）的功能结构域进化研究。

## 07 方法总览

- **输入**：小鼠Ctcf基因座（内源位点编辑）、四种跨物种CTCF N端序列（小鼠、果蝇、文昌鱼、盲鳗）、盲鳗肝脏组织
- **输出**：CTCF变体维持RAD21富集的能力评估、盲鳗3D基因组特征（CTCF/RAD21共定位、convergent loops、stripes）
- **模块**：
  1. CRISPR-Cas9基因编辑（构建等位基因特异性mESC系）
  2. 诱导型蛋白降解系统（dTAG + BromoTag）
  3. ChIP-seq（CTCF、RAD21、组蛋白修饰）
  4. Micro-C（3D基因组构象捕获）
  5. AlphaFold 3结构预测（CTCF N端与RAD21-STAG2复合物）
  6. 系统发育分析（CTCF直系同源物鉴定与基序保守性）
  7. 机器学习序列分析（LS-GKM + TF-MoDISco）
- **训练**：无监督训练（AlphaFold 3预训练模型）；有监督分类器（LS-GKM，5折交叉验证）
- **工具**：distiller（Micro-C处理）、cooltools（pile-up分析）、FIMO（基序扫描）、bedtools、deepTools、metapredict（无序区域预测）
- **反馈回路**：选择性降解野生型CTCF后检测RAD21变化，评估变体功能；ChIP-seq与Micro-C数据交叉验证
- **假设**：CTCF N端是cohesin互作的主要决定区域；mESC系统可反映CTCF变体的保守功能；盲鳗组织数据可代表脊椎动物祖先状态

## 08 核心模块拆解

| 模块 | 功能 | 为何需要 | 输入输出 | 支撑证据 | 移除后的已知或预期影响 |
|------|------|----------|----------|----------|------------------------|
| 等位基因特异性mESC系统 | 在同一细胞中表达野生型和变体CTCF，实现选择性降解 | 直接比较不同N端变体维持cohesin的能力，避免克隆间差异 | 输入：编辑后的mESC；输出：可诱导降解的细胞系 | Results 图1B；Supplemental 图1A | 预期影响：无法在相同遗传背景下比较变体功能，需依赖跨细胞系比较（预期效应） |
| 诱导型蛋白降解（dTAG/BromoTag） | 快速、选择性清除特定CTCF等位基因产物 | 区分野生型和变体CTCF的独立功能贡献 | 输入：dTAG-13/AGB1处理；输出：特定CTCF蛋白降解 | Results 图2；Supplemental 图2 | 预期影响：无法区分等位基因特异性效应，只能观察总CTCF功能（预期效应） |
| ChIP-seq（RAD21/CTCF） | 定量cohesin和CTCF的基因组占据 | 评估CTCF变体招募cohesin的能力 | 输入：交联染色质；输出：全基因组结合谱 | Results 图2A-C；Supplemental 图2 | 实测效应：N端缺失和果蝇N端置换导致RAD21富集显著下降（实测消融效应） |
| Micro-C | 高分辨率3D基因组构象分析 | 检测盲鳗中CTCF-anchored loops和stripes | 输入：交联细胞核；输出：全基因组接触矩阵 | Results 图5A-B | 预期影响：无法直接验证环锚定功能，只能间接推断（预期效应） |
| AlphaFold 3结构预测 | 预测CTCF N端与RAD21-STAG2的互作模式 | 解释物种间功能差异的结构基础 | 输入：蛋白序列；输出：预测复合物结构 | Supplemental 图3A-B | 预期影响：无法区分动态结合亲和力差异（预期效应） |
| 系统发育分析 | 鉴定CTCF直系同源物及基序保守性 | 确定YxF和KTYQR基序的进化分布 | 输入：527个物种蛋白组；输出：基序保守性图谱 | Results 图1A | 预期影响：无法判断基序存在与功能获得的时间关系（预期效应） |

## 09 关键公式符号

不适用。本文为实验生物学研究，核心分析为ChIP-seq峰富集比较、Micro-C pile-up信号聚合和Pearson/Spearman相关性分析，无需要推导的数学公式。关键统计量为：
- Pearson相关系数 r = 0.87（N端缺失 vs 果蝇N端置换的RAD21变化相关性）
- Spearman秩相关系数 ρ = 0.89
- AUROC = 0.80（序列特征区分H3K27ac+与H3K27ac−区域的分类性能）

## 10 实验设计与证据链

**数据集/群体**：
- 小鼠：mESC系（E14TG2a），4种基因型（CTCF^WT/CTCF^N-del、CTCF^WT/CTCF^N-Drosophila、CTCF^WT/CTCF^N-Branchiostoma、CTCF^WT/CTCF^N-Hagfish）
- 盲鳗：野生捕获（日本Kamo Bay），肝脏组织
- 公开数据：小鼠ESC CTCF/RAD21/H3K27ac/H3K4me3（GSE178982, GSE146328, GSE186349）

**指标**：RAD21 ChIP-seq富集变化、CTCF-RAD21峰重叠率、Micro-C pile-up信号（convergent/tandem/divergent stripes）、基序保守性

**预算/资源**：未提供

**骨干/仪器**：Illumina NextSeq 2000、NovaSeq X

**评测协议**：ChIP-seq峰调用（LanceOtron）、峰重叠定义（峰顶距≤200bp）、Micro-C数据处理（distiller默认参数）、MAPQ≥30

| 实验 | 检验的claim | 对比与条件 | 结果 | 支持的结论 | 不支持更强的结论 | 来源 |
|------|------------|------------|------|------------|-------------------|------|
| 跨物种N端置换+选择性降解 | 无脊椎动物CTCF N端不能支持cohesin招募 | 果蝇/文昌鱼N端置换 vs 小鼠N端；野生型降解后检测RAD21 | 果蝇和文昌鱼N端置换后RAD21富集显著下降，与N端缺失效果相当 | 无脊椎动物N端缺乏cohesin招募功能 | 不能排除ZF1-2或C端区域的补偿作用 | Results 图2B-C |
| 盲鳗N端置换 | 盲鳗N端保留cohesin招募功能 | 盲鳗N端置换 vs 小鼠N端；比较RAD21富集下降程度 | 盲鳗N端支持RAD21富集，但效率低于小鼠N端 | 盲鳗N端具有部分功能 | 不能确定盲鳗N端在原生环境中的完整功能 | Results 图2B-C |
| 盲鳗肝脏ChIP-seq | 盲鳗内源CTCF/RAD21共定位 | 盲鳗CTCF峰与RAD21峰重叠率 | 61.2% RAD21峰与CTCF峰重叠；仅28.4% CTCF峰与RAD21峰重叠 | 盲鳗中cohesin-CTCF共定位不如小鼠紧密 | 不能确定这是否反映环锚定效率差异 | Results 图3A |
| 盲鳗Micro-C | 盲鳗存在CTCF-anchored loops | convergent vs tandem vs divergent CTCF位点对的pile-up信号 | 仅convergent位点对显示stripe特征 | 盲鳗CTCF以方向依赖方式阻滞cohesin | 不能排除其他蛋白介导该效应 | Results 图5A |
| AlphaFold 3结构预测 | 文昌鱼和盲鳗N端均可与RAD21-STAG2互作 | 各物种N端与人类RAD21-STAG2复合物预测 | 文昌鱼和盲鳗N端预测可结合，但果蝇N端不结合 | 结构预测支持功能实验 | 预测不能反映体内动态结合差异 | Supplemental 图3A |
| 基序保守性分析 | YxF基序分布与功能的关系 | 527个物种的CTCF基序扫描 | YxF广泛存在于两侧对称动物，但KTYQR仅存在于脊椎动物 | 基序存在不等于功能获得 | 不能排除其他残基的功能贡献 | Results 图1A |

## 11 结论正确解读

- **任务范围**：本研究仅评估CTCF N端（1-265/293/372/423）在mESC中对cohesin招募的贡献，不涉及CTCF的转录调控功能、DNA结合特异性或其他结构域的功能。
- **Oracle/真值输入**：无外源oracle；功能评估依赖内源RAD21 ChIP-seq信号作为cohesin占据的代理指标。
- **端到端状态**：非端到端。研究聚焦于CTCF N端的单一功能维度（cohesin招募），未评估3D基因组组织的下游功能后果（如基因表达变化）。
- **算力成本**：未提供。
- **历史数据依赖**：依赖公开的小鼠ESC ChIP-seq数据集（GSE178982等）作为参考；盲鳗基因组注释质量可能影响峰调用。
- **模型依赖**：AlphaFold 3预测结果依赖预训练模型，未进行湿实验验证预测的互作界面。
- **最难情形**：文昌鱼N端在mESC中显示部分活性（介于果蝇和盲鳗之间），但文昌鱼内源CTCF是否具有环锚定功能无法直接验证。
- **群体/领域边界**：结论仅适用于两侧对称动物中的CTCF；不涉及cohesin非CTCF依赖的环挤出功能；不涉及植物或单细胞真核生物。
- **不确定性**：进化时间点的推断（"脊椎动物祖先"）基于现存物种的比较，无法直接观察祖先状态；盲鳗作为"活化石"的代表性有限。
- **有边界的复述**：在mESC置换实验和盲鳗组织分析的支持下，CTCF介导的cohesin环锚定功能在现存脊椎动物中保守，在果蝇和文昌鱼中缺失或极弱，提示该功能最可能起源于脊椎动物祖先，并在有颌类中进一步增强。

## 12 作者自认局限

| 局限 | 具体表现 | 作者提出的未来方向 | 来源 |
|------|----------|---------------------|------|
| 盲鳗N端功能效率低于小鼠 | 盲鳗N端置换后RAD21富集下降程度大于小鼠N端 | 未明确提及 | Results 图2B-C |
| 文昌鱼N端显示部分活性 | 文昌鱼N端介于果蝇（无功能）和盲鳗（有功能）之间 | 未明确提及 | Results 图2B-C |
| 盲鳗Micro-C中dot信号较弱 | 与小鼠相比，convergent位点对的焦点富集（dot）较弱 | 未明确提及 | Results 图5A |
| 无法直接验证祖先状态 | 进化推断基于现存物种比较 | 未明确提及 | Discussion |
| 未检测CTCF变体的转录调控功能 | 研究仅聚焦cohesin招募 | 未明确提及 | 未提供 |

*注：作者在提供的摘要和正文中未系统列出"Limitations"章节，以上为从Results和Discussion中可明确归因于作者的表述。*

## 13 批判性分析

| [Analysis] 观察 | 潜在问题或替代解释 | 为何重要 | 如何检验 | 依据 |
|-----------------|---------------------|----------|----------|------|
| mESC系统可能无法完全反映内源CTCF功能 | 异源表达环境可能影响蛋白折叠或互作；mESC的cohesin动力学可能与其他细胞类型不同 | 功能结论的普适性取决于实验系统的代表性 | 在多种细胞类型（如成纤维细胞、肝细胞）中重复置换实验 | Results 图2 |
| 盲鳗N端置换效率低于小鼠，但盲鳗内源Micro-C显示功能性loops | 可能盲鳗CTCF的N端在原生环境中与其他因子协同，或盲鳗cohesin动力学不同 | 影响"盲鳗N端功能较弱"的解释 | 在盲鳗细胞中敲低CTCF观察loop变化；或检测盲鳗cohesin加载因子 | Results 图2 vs 图5 |
| 文昌鱼N端显示部分活性，但被归类为"无功能" | 部分活性可能反映进化中间状态，而非完全无功能 | 影响"脊椎动物特有创新"结论的强度 | 增加更多物种（如海鞘、两栖类）的置换实验 | Results 图2B-C |
| 仅检测RAD21占据，未检测loop extrusion动态 | RAD21占据不等同于环锚定功能；可能变体CTCF仍能阻滞cohesin但招募效率低 | 功能结论需要更直接的动力学证据 | 使用live imaging或Hi-C检测变体CTCF的loop形成 | Results 图2 |
| 基序保守性分析中KTYQR仅存在于脊椎动物，但未直接验证其功能必要性 | 可能KTYQR是功能获得的关键，但缺乏突变实验支持 | 确定功能获得的结构基础 | 在小鼠CTCF中突变KTYQR观察功能丧失 | Results 图1A |
| AlphaFold 3预测显示文昌鱼N端可结合RAD21-STAG2，但功能实验显示无活性 | 预测的静态结构可能无法反映结合亲和力或动力学差异 | 结构预测与功能实验的矛盾需要解释 | 进行ITC或SPR等定量结合实验 | Supplemental 图3A |

## 14 学到什么

**Agent 提炼的知识候选**

1. **跨物种结构域置换（domain-swap）策略**：将不同物种的同源结构域置换到同一骨架蛋白中，在相同细胞环境中比较功能，可有效规避物种间表达差异和补偿效应。该方法可直接迁移至cpdch基因家族——若需解析不同物种cpdch同源物的功能差异，可构建嵌合蛋白在统一细胞系统中评估。

2. **等位基因特异性降解系统**：利用dTAG和BromoTag双标记系统，在同一细胞中实现野生型和变体蛋白的独立、可诱导降解，避免了传统敲除/回补实验的克隆间变异问题。该策略适用于cpdch家族成员的功能冗余研究——当家族内多个成员功能重叠时，可构建不同成员的双标记等位基因系统。

3. **功能进化推断的多层证据框架**：本研究整合了序列保守性分析、结构预测、体外功能置换实验和原生组织3D基因组数据，形成"序列-结构-功能-内源验证"的完整证据链。cpdch基因家族研究可借鉴此框架，从单纯的序列/表达分析升级为功能进化研究。

4. **Micro-C pile-up分析策略**：通过将CTCF位点对按相对方向（convergent/tandem/divergent）分类并聚合信号，可灵敏检测方向依赖的cohesin阻滞事件。该方法可迁移至cpdch家族蛋白的基因组结合位点分析——若cpdch家族成员参与染色质结构调控，可检验其结合位点是否显示方向性特征。

5. **"基序存在≠功能获得"的警示**：YxF基序在果蝇和文昌鱼中均存在，但功能实验显示其不足以支持cohesin招募。这提示在cpdch基因家族研究中，不能仅凭保守结构域或基序的存在推断功能，需要功能实验验证。

## 15 与已有知识连接

- **CTCF-cohesin环挤出模型**：与Davidson et al. (2019) 和Kim et al. (2019) 的体外单分子实验一致，本文进一步提供了进化维度的证据，支持CTCF作为cohesin阻滞因子的功能是脊椎动物特有的。
- **果蝇CTCF insulator功能**：与Bushey et al. (2009) 和Phillips-Cremins et al. (2013) 的果蝇研究一致，果蝇CTCF主要作为insulator蛋白而非cohesin环锚，本文通过功能置换实验直接验证了这一差异。
- **YxF基序功能**：与Li et al. (2020) 和Nishana et al. (2020) 的生化研究一致，YxF基序是CTCF与RAD21-STAG2互作的关键位点；本文扩展了该基序的进化分布分析。
- **盲鳗作为脊椎动物祖先模型**：与Smith et al. (2018) 的盲鳗基因组研究衔接，本文提供了盲鳗3D基因组组织的首批数据。
- **cpdch基因家族关联**：[Analysis] 该文未涉及cpdch基因家族，但其核心方法——跨物种功能置换结合染色质构象捕获——可直接应用于cpdch家族成员的功能研究。若cpdch家族成员编码染色质相关蛋白，可检验其是否具有类似CTCF的cohesin互作功能及其进化保守性。

## 16 研究想法

**Agent 生成的研究候选**

1. **候选名称**：cpdch家族成员与cohesin-CTCF环锚定机制的潜在关联
   - **来源局限/观察**：本文证明CTCF N端是脊椎动物特有的cohesin环锚定功能域；cpdch基因家族在脊椎动物中可能经历了类似的功能获得
   - **核心假设**：cpdch家族中至少一个成员在脊椎动物中获得了与cohesin或CTCF互作的功能，参与3D基因组组织
   - **初步方法**：对cpdch家族成员进行跨物种序列比对，鉴定脊椎动物特有的结构域或基序；利用本文的mESC置换系统，将cpdch候选结构域融合到CTCF骨架中检测cohesin招募
   - **验证方式**：ChIP-seq检测cpdch家族成员的基因组结合位点与CTCF/RAD21的共定位；CRISPR敲除后检测3D基因组变化
   - **创新状态**：unverified

2. **候选名称**：cpdch基因家族在盲鳗等无颌类中的表达与功能分析
   - **来源局限/观察**：本文提供了盲鳗肝脏的CTCF/RAD21 ChIP-seq和Micro-C数据，但未涉及cpdch基因家族
   - **核心假设**：cpdch家族成员在无颌类中已有表达，且可能参与与有颌类不同的3D基因组调控机制
   - **初步方法**：利用本文的盲鳗数据（GSE353712）分析cpdch家族成员的表达水平；在盲鳗基因组中鉴定cpdch家族成员及其染色质互作蛋白
   - **验证方式**：比较盲鳗与小鼠cpdch家族成员的表达模式和基因组结合特征
   - **创新状态**：unverified

3. **候选名称**：cpdch家族蛋白结构域的功能进化解析
   - **来源局限/观察**：本文通过domain-swap证明单一基序（YxF）不足以决定功能，需要多个结构域协同进化；cpdch家族可能面临类似情况
   - **核心假设**：cpdch家族成员的功能分化由多个结构域的协同进化驱动，而非单一关键残基
   - **初步方法**：对cpdch家族成员进行系统发育分析，鉴定共进化的残基网络；构建跨物种嵌合蛋白进行功能分析
   - **验证方式**：在细胞系统中表达嵌合蛋白，检测其与已知互作蛋白的结合能力及下游功能
   - **创新状态**：unverified

4. **候选名称**：cpdch家族成员在增强子-启动子互作中的潜在角色
   - **来源局限/观察**：本文强调CTCF-anchored loops对增强子-启动子互作的重要性；cpdch家族成员可能参与类似的调控
   - **核心假设**：cpdch家族成员通过影响染色质环结构调控特定基因的表达
   - **初步方法**：在cpdch敲除细胞中进行Micro-C和RNA-seq，鉴定受影响的染色质环和差异表达基因
   - **验证方式**：CRISPR干扰特定cpdch结合位点，检测染色质环和基因表达变化
   - **创新状态**：unverified