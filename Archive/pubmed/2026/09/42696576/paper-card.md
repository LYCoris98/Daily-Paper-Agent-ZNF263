## 01 基本信息
- **标题**: CTCF aligns single-cell TAD-like domain boundaries and stabilizes long-range active chromatin clusters
- **作者与单位**: Chen, Ziyin; Li, Xuan; Dai, Yunpeng; Shao, Kaiwen; Sun, Haolun; Wu, Nan; Yan, Jian; Zhang, Yanxiao; Yu, Miao. 单位未在摘要中提供，但根据致谢部分，通讯作者M.Y.实验室为复旦大学。
- **期刊/预印本平台**: Science Advances
- **年份**: 2026-09-04
- **论文类型**: 研究论文
- **领域**: 三维基因组学、单细胞多组学、基因调控
- **关键词**: CTCF, 单细胞Hi-C, TAD-like domain (TLD), 染色质结构, 转录调控, HiRES, SALTAFinder
- **DOI/arXiv 号**: 10.1126/sciadv.aee2863
- **代码**: https://github.com/YuLab-FDU/SALTAFinder; https://doi.org/10.5281/zenodo.19478233
- **数据**: 国家基因组科学数据中心 (NGDC) 登录号 CRA033983 (HiRES) 和 CRA034099 (spike-in RNA-seq)
- **阅读日期**: 2024-05-21
- **该文在「cpdch基因家族」方向中的位置**: 该文研究的是CTCF这一关键结构蛋白，而非cpdch基因家族。然而，其研究范式、核心概念（如单细胞TAD-like domain边界概率、高阶染色质组装体SALTA）以及分析方法（SALTAFinder）对研究cpdch基因家族在三维基因组中的功能具有高度可迁移性。cpdch基因家族可能通过类似机制影响染色质环或结构域边界，该文提供了研究此类问题的单细胞多组学框架。

## 02 一句话总结
该文利用单细胞多组学技术HiRES，在CTCF缺失的小鼠胚胎干细胞中，发现CTCF并非消除单细胞TAD-like domain (TLD)，而是通过约束边界位置来对齐边界，并稳定富含超增强子和高表达基因的长程活性染色质簇（SALTAs），其缺失导致全局转录能力下降。

## 03 研究问题
- **具体问题**: CTCF缺失如何在单细胞水平上重塑染色质三维结构和转录？具体而言，CTCF缺失是消除TAD边界，还是改变边界在单细胞中的形成位置？这种结构紊乱是否会影响细胞的全局转录能力？
- **为什么重要**: CTCF是三维基因组的关键结构蛋白，但其在单细胞水平上的功能尚不明确。理解其作用机制对于揭示基因调控、发育和疾病（如癌症）中染色质结构异常至关重要。
- **现有方法为何不足**: 传统的bulk Hi-C实验掩盖了单细胞间染色质折叠的异质性，无法揭示CTCF缺失对单细胞中TAD-like domain (TLD) 边界定位和稳定性的影响。
- **精确的「Can ... ?」研究问题**: Can CTCF loss eliminate TLD boundaries, or does it alter where boundaries form across single cells? Can such structural disorganization influence a cell’s global transcriptional capacity?

## 04 背景与发展脉络
- **阶段1: 群体水平研究 (Bulk Hi-C)**: 代表性方法为bulk Hi-C。优点：揭示了CTCF在TAD边界和染色质环形成中的核心作用。局限：掩盖了单细胞间的异质性，无法解释细胞间TAD边界的波动。
- **阶段2: 单细胞水平研究 (scHi-C, 成像)**: 代表性方法为单细胞Hi-C和染色质示踪成像。优点：揭示了单细胞中高度可变的TAD-like domain (TLD) 结构。局限：通常缺乏与转录的直接关联，且对CTCF缺失后的单细胞结构变化理解有限。
- **本文主张的位置**: 本文通过联合测量单细胞染色质接触和转录的HiRES技术，填补了CTCF缺失后单细胞结构变化与转录输出之间的空白。它提出CTCF的主要功能是“对齐”单细胞边界，而非创建边界本身，并首次鉴定了CTCF依赖的高阶活性染色质簇（SALTAs）。
- **注**: 此脉络是「经外部核验」的，基于文中引言部分对前人工作的总结。

## 05 核心痛点
| 痛点 | 表现 | 成因或作者解释 | 文中证据 |
| :--- | :--- | :--- | :--- |
| 单细胞边界定位的异质性 | 即使是在bulk TAD边界处，单细胞中作为边界的概率也仅为~13%。 | 单细胞中TLD边界是概率性的，bulk TAD边界是这些概率的最大值，而非普遍使用的边界。 | Results 图1G, 1K; fig. S3B |
| CTCF缺失后边界“消失”的误解 | 在bulk水平上，CTCF缺失导致TAD边界减弱，但单细胞中TLD的数量和大小不变。 | CTCF缺失并非消除边界，而是使边界位置在细胞间更分散，即边界概率从原CTCF位点向邻近区域重新分布。 | Results 图1I, 1J, 1K; fig. S4 |
| 全局转录能力下降的检测困难 | 标准RNA-seq归一化假设总RNA量恒定，会掩盖CTCF缺失导致的全局转录下降。 | 标准方法无法检测到全局性的RNA总量变化，需要细胞数归一化或内参RNA spike-in。 | Results 图2F-2I; Discussion |
| 高阶染色质结构的识别 | 传统方法难以在单细胞中系统性地识别由多个远距离TLD组成的空间簇。 | 缺乏针对单细胞Hi-C数据的高阶结构识别工具。 | Results 图3A; 作者开发了SALTAFinder |

## 06 核心思想
1.  **表面方法**: 应用单细胞多组学技术HiRES，同时从同一细胞核获取染色质接触（Hi-C）和转录组（RNA-seq）数据。开发SALTAFinder算法，从单细胞Hi-C数据中识别由多个远距离TLD组成的空间聚集结构（SALTAs）。
2.  **核心洞察**: CTCF的主要功能不是创建TAD边界，而是在单细胞间“对齐”边界位置，并稳定那些富含活性基因和增强子的高阶染色质簇（SALTAs）。CTCF缺失导致边界位置分散、活性SALTAs解体，进而与全局转录能力下降相关联。
3.  **可能的普适教训 [Analysis]**: 对于研究染色质结构蛋白（如cpdch基因家族成员），不能仅依赖群体水平的分析。单细胞水平的分析可以揭示蛋白在“约束结构变异性”而非“创建结构”中的关键作用。此外，联合测量结构和功能（如转录）是揭示因果关系的强有力手段。

## 07 方法总览
- **输入**: 对照和CTCF缺失的CTCF-AID小鼠胚胎干细胞（mESCs）。
- **输出**: 单细胞TLD边界概率图谱、A/B compartment分数、SALTAs列表及其分类、单细胞转录组数据。
- **模块**:
    1.  **HiRES实验**: 同时从同一细胞核获取Hi-C和RNA-seq数据。
    2.  **数据处理与质控**: 使用HiRES pipeline处理数据，过滤低质量细胞。
    3.  **单细胞TLD鉴定**: 使用Higashi算法在50kb分辨率下鉴定每个单细胞中的TLD。
    4.  **单细胞Compartment分析**: 使用Higashi计算100kb分辨率的compartment分数。
    5.  **SALTAFinder**: 将每个染色体的接触网络建模为加权图，使用改进的模块度最大化算法（fast-greedy）划分模块，每个模块内包含至少3个TLD，定义为SALTA。
    6.  **SALTA分类**: 基于ChromHMM染色质状态，对SALTAs进行K-means聚类，分为活性、混合和非活性三类。
    7.  **正交验证**: 使用原位荧光逆转录结合流式细胞术和Drosophila RNA spike-in的RNA-seq验证全局转录能力下降。
- **训练**: 不适用（无监督学习为主，如SALTAFinder的模块度优化）。
- **工具**: HiRES pipeline, Higashi, SALTAFinder, Seurat, DESeq2, cooltools, ChromHMM, hickit等。
- **反馈回路**: 无显式反馈回路。
- **假设**: 单细胞Hi-C接触图可以近似为加权网络；模块度最大化可以识别空间上聚集的TLD簇；ChromHMM状态可以反映SALTAs的功能状态。
- **文字流程**: 首先，对对照和CTCF缺失的mESCs进行HiRES实验，获得配对单细胞Hi-C和RNA-seq数据。然后，对Hi-C数据进行单细胞TLD和compartment分析，发现CTCF缺失导致边界概率重新分布和A compartment内部相互作用减弱。接着，开发SALTAFinder算法，从单细胞Hi-C数据中识别高阶TLD组装体SALTAs，并发现活性SALTAs在CTCF缺失后减少和扩张。最后，结合RNA-seq数据，发现活性SALTAs的减少与全局转录能力下降和特定基因表达下调相关。

## 08 核心模块拆解
| 模块 | 功能 | 为何需要 | 输入输出 | 支撑证据 | 移除后的已知或预期影响 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **HiRES** | 同时从同一细胞核获取染色质接触和转录组信息。 | 实现单细胞中3D基因组结构与转录的直接关联，避免批次效应。 | 输入：固定细胞；输出：配对单细胞Hi-C和RNA-seq数据。 | 方法部分详细描述；UMAP显示基于DNA和RNA的聚类均能区分两组细胞（图1E, 1F）。 | 无法直接关联单细胞结构与功能，只能进行群体水平的推断。 |
| **Higashi (单细胞TLD鉴定)** | 在单细胞水平上鉴定TAD-like domain (TLD)。 | 揭示bulk TAD在单细胞中的异质性，量化边界概率。 | 输入：单细胞Hi-C接触矩阵；输出：每个单细胞的TLD边界列表。 | 结果图1G-1K；与bulk TAD边界和CTCF/cohesin位点共定位（图1G）。 | 无法获得单细胞域结构信息，只能依赖群体平均的TAD分析，掩盖异质性。 |
| **SALTAFinder** | 从单细胞Hi-C数据中识别由多个远距离TLD组成的空间聚集结构（SALTAs）。 | 系统性地鉴定单细胞中高阶染色质组装体，揭示CTCF对长程活性簇的稳定作用。 | 输入：单细胞TLD列表和接触矩阵；输出：每个单细胞的SALTAs列表。 | 与GAM/SPRITE数据一致（fig. S7F, G）；3D模型显示Rg显著小于随机对照（图3G）。 | 无法识别单细胞中高阶染色质组织，无法发现CTCF对活性簇的稳定作用。 |
| **SALTA分类 (K-means)** | 基于ChromHMM染色质状态对SALTAs进行功能分类。 | 区分不同功能状态的SALTAs，特别是与高转录活性相关的类别。 | 输入：所有SALTAs的ChromHMM状态组成；输出：7个SALTA类别（C1-C7）。 | C1 SALTAs富集超增强子和高表达基因（图4B, 4C）；CTCF缺失后C1/C2减少（图4D）。 | 无法区分SALTAs的功能状态，无法揭示CTCF对特定活性簇的影响。 |

## 09 关键公式符号
- **公式1: 模块度 (Modularity, Q)**
    - **公式**: `Q = Σ_i (e_ii - a_i^2)`
    - **符号含义**: `e_ii` 是组i内部边的比例；`a_i` 是连接到组i的边的比例。
    - **用途**: 衡量网络划分质量，用于SALTAFinder的模块度最大化算法。
    - **直觉**: Q值高表示组内连接紧密、组间连接稀疏，是理想的社区结构。
    - **来源**: Methods节 "SALTA identification"。

- **公式2: 回转半径 (Radius of Gyration, Rg)**
    - **公式**: `Rg = sqrt( (1/n) * Σ_i [(x_i - x̄)^2 + (y_i - ȳ)^2 + (z_i - z̄)^2] )`
    - **符号含义**: `(x_i, y_i, z_i)` 是第i个粒子（50kb bin）的3D坐标；`(x̄, ȳ, z̄)` 是所有粒子的质心；`n` 是粒子数。
    - **用途**: 量化SALTA在3D空间中的紧凑程度。
    - **直觉**: Rg越小，SALTA越紧凑。
    - **来源**: Methods节 "Spatial analysis of SALTAs"。

## 10 实验设计与证据链
- **数据集/群体**: CTCF-AID knock-in mESCs (F123细胞系)，对照和auxin处理（CTCF缺失）组。
- **规模**: 668个高质量单细胞（344 CTCF-depleted, 324 control）。
- **指标**: TLD边界概率 (PTLD-B), 绝缘分数, compartment分数, SALTA大小/跨度/数量, 每个细胞的RNA UMIs/基因数, 荧光强度。
- **基线**: 未处理的CTCF-AID mESCs。
- **骨干/仪器**: HiRES实验流程, DNBSEQ-T7测序仪, Sony Cell Sorter MA900。
- **评测协议**: 使用Wilcoxon秩和检验、Pearson相关、Kolmogorov-Smirnov检验等统计方法比较两组差异。

| 实验 | 检验的claim | 对比与条件 | 结果 | 支持的结论 | 不支持更强的结论 | 来源 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **单细胞TLD分析** | CTCF缺失消除TLD边界。 | 对照 vs. CTCF-depleted mESCs。 | TLD数量和大小不变（图1I, 1J）；边界概率从原CTCF位点向邻近区域重新分布（图1K）。 | CTCF缺失不消除边界，而是改变边界位置。 | 不能证明CTCF对边界形成完全无影响，因为边界概率分布发生了显著变化。 | Results 图1 |
| **A compartment相互作用分析** | CTCF缺失影响A compartment内部相互作用。 | 对照 vs. CTCF-depleted mESCs的pseudobulk O/E矩阵。 | 观察到显著的intra-A compartment接触频率降低（图2E）。 | CTCF缺失导致A compartment内部相互作用减弱。 | 不能证明这是转录下降的直接原因，可能只是相关。 | Results 图2E |
| **全局转录能力测量** | CTCF缺失降低每个细胞的转录输出。 | 对照 vs. CTCF-depleted mESCs，使用原位RT-流式细胞术和spike-in RNA-seq。 | 流式细胞术显示~75%荧光信号（图2G, 2H）；spike-in RNA-seq显示~91%转录输出（图2I）。 | CTCF缺失导致全局转录能力下降。 | 不能证明这是由结构变化直接导致的，可能涉及其他机制。 | Results 图2F-2I |
| **SALTA特征比较** | CTCF缺失破坏活性SALTAs。 | 对照 vs. CTCF-depleted mESCs的SALTAs。 | SALTA大小和跨度增加（fig. S8）；活性SALTAs (C1/C2) 比例下降（图4D）。 | CTCF稳定活性SALTAs，其缺失导致活性簇扩张和解体。 | 不能证明SALTA解体是转录下降的唯一原因。 | Results 图4, fig. S8 |
| **基因表达与SALTA环境关联** | 基因在活性SALTA中的定位与其表达水平相关。 | 比较同一基因在位于C1/C2 SALTA内 vs. 外的单细胞中的表达。 | 位于C1/C2 SALTA内的TSS表达更高（图4G）。 | 活性SALTA环境支持高转录。 | 不能证明因果关系，可能是高转录导致基因进入活性SALTA。 | Results 图4G |

## 11 结论正确解读
- **任务范围**: 该研究仅限于小鼠胚胎干细胞（mESCs）中CTCF的急性缺失（48小时auxin处理）。
- **oracle/真值输入**: 使用CTCF-AID系统实现可诱导的CTCF降解，并通过Western blot验证。HiRES数据经过严格质控。
- **端到端状态**: 研究从实验到计算分析是完整的，但结论是关联性的，而非严格的因果证明。
- **算力成本**: 未提供具体算力成本，但单细胞Hi-C数据处理和3D建模计算量较大。
- **历史数据依赖**: 依赖于已发表的ChIP-seq、Hi-C、GAM、SPRITE等数据集进行验证和比较。
- **模型依赖**: 依赖于Higashi进行单细胞TLD鉴定，依赖于SALTAFinder的模块度算法，依赖于ChromHMM进行染色质状态注释。
- **最难情形**: 单细胞Hi-C数据稀疏性可能导致TLD边界频率被低估（作者在Discussion中承认）。
- **群体/领域边界**: 结论适用于mESCs，是否适用于其他细胞类型或发育阶段尚不清楚。
- **不确定性**: CTCF缺失与转录下降之间的因果关系未明确建立。SALTA的生物学意义和动态性需要进一步验证。
- **有边界的复述**: 在CTCF-AID小鼠胚胎干细胞中，CTCF的急性缺失导致单细胞TAD-like domain边界位置在细胞间更分散，并导致富含活性基因和超增强子的高阶染色质簇（SALTAs）扩张和解体，这些变化与每个细胞总RNA产量的下降相关。

## 12 作者自认局限
| 局限 | 具体表现 | 作者提出的未来方向 | 来源 |
| :--- | :--- | :--- | :--- |
| 单细胞数据稀疏性导致边界频率低估 | 由于单细胞接触数有限，TLD边界在bulk TAD边界处的发生频率可能被低估。 | 未明确提及，但暗示需要更高覆盖度的单细胞数据。 | Discussion |
| 因果关系未明确 | 转录下降与A compartment解体之间的因果关系尚不清楚。 | 需要未来研究阐明。 | Discussion |
| 机制不明确 | CTCF影响高阶染色质组织和转录能力的机制尚不清楚。 | 可能通过直接稳定局部结构，或通过影响转录间接影响结构。 | Discussion |
| 适用范围有限 | 研究仅限于mESCs。 | 需要研究在分化细胞或发育过程中是否发生类似现象。 | Discussion |
| SALTA分析局限于染色体内 | 当前SALTA分析仅限于染色体内TLD。 | 扩展框架以研究染色体间TLD聚类。 | Discussion |

## 13 批判性分析
| [Analysis] 观察 | 潜在问题或替代解释 | 为何重要 | 如何检验 | 依据 |
| :--- | :--- | :--- | :--- | :--- |
| 活性SALTAs (C1/C2) 的减少与全局转录下降相关，但因果方向未定。 | 可能是转录下降导致活性SALTAs解体，而非反之。转录活性本身可能驱动活性染色质簇的形成。 | 区分因果方向对于理解CTCF的功能机制至关重要。 | 使用转录抑制剂（如α-amanitin）处理细胞，观察SALTAs是否解体。如果解体，则支持转录驱动结构；如果不变，则支持结构驱动转录。 | Results 图4 |
| SALTAFinder的模块度算法可能对接触网络中的噪声敏感。 | 单细胞Hi-C数据稀疏且噪声高，模块度最大化可能将随机连接误判为结构。 | 影响SALTA鉴定的可靠性和生物学意义。 | 使用模拟数据（已知真实结构）或更高分辨率的成像数据（如MERFISH）来验证SALTAFinder的准确性和鲁棒性。 | Methods节 "SALTA identification" |
| 研究仅使用了一个细胞系（F123 mESCs），结论的普适性有限。 | 观察到的现象可能具有细胞系特异性，而非CTCF功能的普遍特征。 | 限制结论向其他细胞类型或体内环境的推广。 | 在多种细胞系（如人K562、HCT116）或原代细胞中重复CTCF敲除实验，观察TLD边界和SALTAs的变化。 | 未提供 |
| 作者声称CTCF“对齐”边界，但“对齐”的分子机制未阐明。 | 可能依赖于cohesin的环挤压，但该研究未直接测试。 | 理解CTCF功能的分子基础。 | 同时敲除CTCF和cohesin loader (NIPBL) 或卸载因子 (WAPL)，观察边界对齐和SALTA稳定性的变化。 | Discussion |

## 14 学到什么
**Agent 提炼的知识候选**

1.  **可迁移概念: 单细胞边界概率 (PTLD-B)**
    - **描述**: 将bulk TAD边界理解为单细胞中边界概率的局部最大值，而非普遍使用的固定边界。
    - **如何迁移到cpdch基因家族**: 如果cpdch基因家族成员参与染色质结构域边界形成，可以计算其在单细胞中的边界概率，评估其缺失是“消除”边界还是“分散”边界位置。

2.  **可迁移方法: 联合单细胞多组学 (HiRES)**
    - **描述**: 同时从同一细胞测量染色质结构和转录，实现直接关联。
    - **如何迁移到cpdch基因家族**: 可以设计类似实验（如scHi-C + scRNA-seq），研究cpdch基因家族敲除后，染色质结构变化与特定基因表达变化在单细胞水平上的直接对应关系。

3.  **可迁移方法: 高阶结构识别算法 (SALTAFinder)**
    - **描述**: 基于网络模块度，从单细胞Hi-C数据中识别由多个域组成的空间簇。
    - **如何迁移到cpdch基因家族**: 可以应用SALTAFinder或类似算法，研究cpdch基因家族是否参与形成或稳定特定的高阶染色质组装体，例如活性基因簇或抑制性染色质中心。

4.  **可迁移实验设计: 全局转录能力测量**
    - **描述**: 使用原位RT-流式细胞术和spike-in RNA-seq来检测全局RNA总量的变化，避免标准归一化方法的掩盖。
    - **如何迁移到cpdch基因家族**: 如果怀疑cpdch基因家族影响全局转录输出，可以使用这些方法进行验证，而不仅仅是分析差异表达基因。

## 15 与已有知识连接
- **相似**: 与Nora et al. (2017) 和 Hsieh et al. (2020) 的bulk Hi-C研究一致，均发现CTCF缺失导致TAD边界减弱和A/B compartment变化。本文在单细胞层面提供了更精细的机制解释。
- **组合**: 与GAM (Beagrie et al., 2017) 和 SPRITE (Quinodoz et al., 2018) 的多重相互作用数据一致，验证了SALTAs作为真实空间聚集体的存在。
- **冲突**: 与早期认为CTCF是TAD边界“创建者”的观点不同，本文提出CTCF是边界的“对齐者”和“稳定者”。这并非完全冲突，而是对CTCF功能的更精细描述。
- **可迁移领域**: 该研究框架可直接迁移到其他结构蛋白（如cohesin, condensin, 以及cpdch基因家族）的功能研究，特别是那些在发育和疾病中起作用的蛋白。

## 16 研究想法
**Agent 生成的研究候选**

1.  **名称**: 探究cpdch基因家族对单细胞TAD-like domain边界稳定性的影响
    - **来源局限/观察**: 该文发现CTCF通过“对齐”单细胞边界来稳定结构。cpdch基因家族成员可能具有类似或互补的功能。
    - **核心假设**: cpdch基因家族成员（如cpdch1, cpdch2）的缺失会导致单细胞TLD边界概率在特定基因组区域（如cpdch结合位点）重新分布，增加边界位置的变异性。
    - **相对本文的增量**: 将CTCF的研究范式迁移到一个新的、功能尚不明确的基因家族，可能揭示其在染色质结构中的新角色。
    - **初步方法**: 在mESCs或其它细胞系中敲除cpdch基因，进行单细胞Hi-C（或HiRES）实验。使用Higashi鉴定TLD，计算边界概率，并与对照比较。重点关注cpdch ChIP-seq峰附近的边界变化。
    - **验证方式**: 观察边界概率在cpdch结合位点是否显著降低，并在邻近区域升高。与bulk Hi-C的TAD边界变化进行对比。
    - **可能的失败模式**: cpdch基因家族可能不直接影响TLD边界，而是通过其他机制（如影响环挤压或compartmentalization）发挥作用。单细胞数据深度不足可能无法检测到细微变化。
    - **创新状态**: unverified

2.  **名称**: 鉴定cpdch基因家族依赖的高阶染色质组装体
    - **来源局限/观察**: 该文开发了SALTAFinder来识别CTCF依赖的活性染色质簇。cpdch基因家族可能参与形成或维持其他类型的高阶结构。
    - **核心假设**: cpdch基因家族成员参与形成特定的SALTAs，这些SALTAs可能富集于特定基因（如发育相关基因）或染色质状态（如Polycomb抑制区域）。
    - **相对本文的增量**: 将SALTAFinder应用于新的基因家族，可能发现与CTCF不同的、功能特异性的高阶染色质组织模式。
    - **初步方法**: 在cpdch敲除细胞中进行单细胞Hi-C，运行SALTAFinder。比较对照和敲除组中SALTAs的数量、大小、组成（基于ChromHMM）和3D紧凑度。特别关注与cpdch结合位点共定位的SALTAs。
    - **验证方式**: 观察特定类型的SALTAs（如抑制性SALTAs）在cpdch敲除后是否发生显著变化（如扩张、解体）。结合RNA-seq，分析这些SALTAs内基因的表达变化。
    - **可能的失败模式**: cpdch基因家族可能不参与高阶结构形成，或SALTAFinder的参数不适用于其介导的结构。单细胞数据深度不足。
    - **创新状态**: unverified

3.  **名称**: 探究cpdch基因家族与CTCF在单细胞三维基因组中的协同或拮抗作用
    - **来源局限/观察**: 该文聚焦于CTCF。许多结构蛋白协同工作，cpdch可能与CTCF有功能重叠或竞争。
    - **核心假设**: cpdch基因家族与CTCF共同调控特定基因组位点的边界稳定性和高阶结构形成，其双敲除会产生协同或拮抗效应。
    - **相对本文的增量**: 从单基因研究扩展到基因家族间的相互作用，揭示更复杂的调控网络。
    - **初步方法**: 构建CTCF和cpdch基因的双敲除细胞系。进行单细胞Hi-C，比较单敲除和双敲除在TLD边界概率、SALTA特征和转录输出上的差异。使用统计模型（如线性模型）检测交互效应。
    - **验证方式**: 如果双敲除的效应大于单敲除效应之和，则表明协同作用；如果小于，则表明拮抗或冗余。重点关注两者共同结合的区域。
    - **可能的失败模式**: 双敲除可能导致细胞活力严重下降，难以获得足够的高质量单细胞数据。两者功能可能完全独立，无交互效应。
    - **创新状态**: unverified