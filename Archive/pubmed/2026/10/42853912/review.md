## Review setup
- **Input scope** 完整手稿正文，包括摘要、引言、结果、讨论、材料与方法、补充材料说明
- **Assessment boundary** 仅基于提供的文本材料进行评审；未提供图表、补充数据文件或原始数据
- **Shared manuscript claim summary** 该研究使用micro-C技术绘制了斑马鱼和非洲鳉鱼鳍再生的染色质相互作用图谱，发现再生过程中染色质环（chromatin loops）的改变是主要的结构变化，而非TAD或区室；鉴定出与再生相关的增强子-启动子相互作用，并通过CRISPR-Cas9删除il11a位点的环相互作用抑制其表达并损害鳍再生效率；发现CTCF/CTCFL和Atf7基序在再生改变的环锚点中富集。
- **Visible evidence base** 文本中引用了多个图（Fig. 1-5）和补充图（fig. S1-S6）及补充表（table S1-S4），但未提供实际图表内容；方法学描述涵盖micro-C、RNA-seq、ATAC-seq、ChIP-seq、scRNA-seq、scATAC-seq、3C、CRISPR-Cas9和转基因报告实验
- **Missing materials affecting confidence** 所有图表数据、统计分析细节、测序质量指标、补充表格内容均未提供；无法验证任何定量结果或统计显著性声明

## Reviewer
- **Overall assessment** 该手稿提出了一个有趣且及时的问题：再生过程中染色质架构如何重组。研究设计合理，将斑马鱼和非洲鳉鱼两种硬骨鱼进行比较，并整合了多种基因组学方法。然而，从提供的文本材料来看，核心结论的支撑证据强度不均衡。染色质环改变为主的结论有一定数据支持，但il11a功能实验的描述过于简略，无法评估其因果关系强度。跨物种比较的进化结论也缺乏足够的定量支撑。该工作有潜力引起再生生物学和3D基因组学领域的广泛兴趣，但当前版本中若干关键证据链需要加强。

- **Who would be interested in the results, and why** 再生生物学研究者会对染色质架构在再生启动中的作用感兴趣；3D基因组学领域的研究者会关注micro-C在非模式生物中的应用以及再生过程中染色质环的动态变化；进化发育生物学研究者会对两种硬骨鱼之间保守和物种特异的染色质重组感兴趣；组织再生医学领域可能关注il11a作为潜在靶点的意义。

- **Major strengths** 1) 首次系统描绘了硬骨鱼鳍再生过程中从稳态到胚基形成的染色质架构变化，填补了该领域的空白；2) 使用micro-C技术提供了比传统Hi-C更高的分辨率，适合检测增强子-启动子相互作用；3) 跨物种比较（斑马鱼和非洲鳉鱼）增加了结论的普适性；4) 结合功能实验（CRISPR-Cas9删除和转基因报告）验证了染色质相互作用的生物学意义；5) 将染色质环动态与特定细胞类型（胚基细胞和基底上皮细胞）联系起来。

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** 结论支撑度
- **Claim pointer** "Notably, perturbing injury-altered loop interactions at the il11a locus suppressed its expression and impaired fin regeneration efficiency."
- **Evidence pointer** Figure 5D-G; 材料与方法中CRISPR-Cas9部分
- **Concern** il11a功能实验是全文最核心的功能验证，但文本中仅用一句话描述结果。缺乏关键细节：删除的是哪个具体区域（增强子？环锚点？）、删除的片段大小、删除后染色质环是否确实被破坏（是否有对照micro-C或3C验证）、再生效率受损的程度和统计显著性、以及il11a表达下降的幅度。此外，材料与方法中未描述如何评估再生效率（是测量再生长度、面积还是组织学评分）。
- **Why it matters** 该实验是建立"染色质环改变→基因表达变化→再生功能影响"因果链的关键环节。如果这一因果链不成立，全文的核心结论将退化为描述性观察。当前描述无法让读者判断该功能验证的严谨性和可靠性。
- **Resolution test** 提供删除区域的详细坐标和大小；展示删除后环相互作用的直接证据（如3C或micro-C验证）；提供再生效率的定量数据和统计方法；明确il11a表达下降的倍数和显著性。

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** No
- **Axis** 数据支撑强度
- **Claim pointer** "Our analyses unveiled that the alteration of chromatin looping upon amputation was dominant compared with that of TADs and compartments."
- **Evidence pointer** Figure 1C-H; fig. S1B-F
- **Concern** 这是全文的核心结论之一，但文本中仅提供了区室强度变化的P值（P < 0.01），未提供TAD绝缘分数变化和环强度变化的统计检验方法和效应量。声称"环的改变占主导"需要三种结构变化的直接比较，但文本中未描述这种比较是如何进行的（是标准化后的百分比变化？还是效应量比较？）。此外，1518个增强和1261个减少的环仅占总环数的约21%，如何从这些数据中得出"dominant"的结论需要更清晰的论证。
- **Why it matters** 该结论是全文的框架性发现，直接影响读者对再生过程中染色质架构重组性质的理解。如果比较方法不明确或统计支撑不足，该结论的可信度将受到质疑。
- **Resolution test** 提供三种结构变化（环、TAD、区室）的标准化比较方法和统计检验；明确"dominant"的操作性定义；展示效应量和置信区间。

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** No
- **Axis** 跨物种比较的严谨性
- **Claim pointer** "Side-by-side comparison between zebrafish and African killifish uncovered conserved and species-specific chromatin reorganization following injury."
- **Evidence pointer** Figure 4A-H; fig. S6A-I
- **Concern** 跨物种比较是本文的重要卖点，但文本中仅提到约60%的直系同源基因位于相同类型的区室中。缺乏关键信息：两种物种的micro-C数据质量是否可比（测序深度、文库复杂度）？比较是在何种分辨率下进行的？"conserved"和"species-specific"的判定标准是什么？非洲鳉鱼的数据仅有一个时间点（2 dpa），而斑马鱼也是2 dpa，但两种物种的再生动力学可能不同，如何确保比较的是生物学上等价的阶段？
- **Why it matters** 进化保守性的结论依赖于跨物种比较的方法学严谨性。如果比较的基准不明确或数据质量不匹配，保守性和物种特异性的结论都可能受到质疑。
- **Resolution test** 提供两种物种数据质量的并列比较；明确保守性和物种特异性的操作性定义；讨论再生阶段可比性的问题。

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** 因果推断
- **Claim pointer** "CTCF/CTCFL and Atf7 binding motifs were the top shared motifs enriched in regeneration-altered loop anchors, implying that these transcription factors are the potential regulators controlling the dynamic chromatin looping during the early onset of regeneration."
- **Evidence pointer** Figure 5H; 材料与方法中motif enrichment分析部分
- **Concern** 从基序富集到"潜在调控因子"的推断存在跳跃。基序富集仅表明这些TF可能结合这些位点，但缺乏以下证据：这些TF在再生过程中是否差异表达？是否确实结合在改变的环锚点（如ChIP-seq验证）？敲低或抑制这些TF是否能改变环的动态？文本中未提供任何功能实验来支持这一推断。
- **Why it matters** 该声明为未来研究提供了方向，但作为结论提出时需要有适当的不确定性表达。当前表述可能过度解读了基序富集结果。
- **Resolution test** 弱化因果语言，改为"这些基序的富集提示CTCF/CTCFL和Atf7可能在再生相关的环重塑中发挥作用，但需要进一步功能验证"；或提供额外的表达或结合证据。

- **Concern ID** R1-M5
- **Severity** Major
- **Blocking** No
- **Axis** 数据可及性
- **Claim pointer** 全文所有定量结果
- **Evidence pointer** 所有图和表
- **Concern** 手稿中引用了大量图表（Fig. 1-5, fig. S1-S6, table S1-S4），但评审材料中未包含任何图表内容。无法验证任何定量声明的准确性，包括差异环的数量、GO富集的显著性、单细胞数据的分析质量等。
- **Why it matters** 作为数据密集型研究，图表的缺失使得核心结论无法被独立评估。特别是补充表S1-S4（差异环列表、GO富集结果等）是验证分析质量的关键材料。
- **Resolution test** 提供所有图表和补充材料以供评审。

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** 方法透明度
- **Affected element** 环鉴定和差异分析
- **Evidence pointer** 材料与方法中Loop calling部分
- **Issue** 环鉴定使用Mustache软件，P值阈值设为0.1（默认值），但未说明该阈值的合理性或是否进行了多重检验校正。差异环的判定标准（fold change阈值、统计检验方法）也未描述。
- **Required correction** 补充差异环的统计检验方法和多重检验校正策略；说明P值阈值选择的依据。

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** 数据呈现
- **Affected element** 区室转换分析
- **Evidence pointer** Figure 1D-E; fig. S1C
- **Issue** 文本提到"relatively enhanced frequency of B-to-A and A-to-B compartment transitions on chromosome 9, 12, and 4"，但未提供这些染色体上转换的绝对数量或与基因组平均水平的比较方法。
- **Required correction** 提供染色体特异性转换的定量数据和统计检验。

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** 方法一致性
- **Affected element** 非洲鳉鱼RNA-seq分析
- **Evidence pointer** 材料与方法中Bulk RNA-seq部分
- **Issue** 非洲鳉鱼的RNA-seq数据来自已发表研究（PRJNA559885），但未说明该数据集的样本量、时间点和处理方法是否与本研究的设计一致。
- **Required correction** 补充对已发表数据集的描述和引用，说明其与本研究micro-C数据的可比性。

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** 结果呈现
- **Affected element** 条纹分析
- **Evidence pointer** Figure 2E-G; fig. S2E-H
- **Issue** 条纹（stripes）分析使用了StripeCaller，但文本中未提供条纹数量变化的统计显著性检验，也未说明条纹形成/破坏与基因表达变化的关联分析。
- **Required correction** 补充条纹动态的统计检验和与基因表达关联的分析。

- **Concern ID** R1-m5
- **Severity** Minor
- **Axis** 讨论深度
- **Affected element** 讨论部分
- **Issue** 讨论中提到了"evolution seems to tolerate substantial changes in such organization"，但未深入讨论本研究发现的保守和物种特异特征如何与已知的再生能力差异联系起来。
- **Required correction** 扩展讨论，将染色质架构的保守/差异特征与再生能力的进化差异更紧密地联系起来。

- **Technical failings that need to be addressed before the case is established** R1-M1（il11a功能实验描述不足，因果链不完整）；R1-M2（"环改变占主导"的比较方法不明确）；R1-M5（图表缺失，无法验证定量结果）

- **Assessment against Nature-style criteria** 
  - **Originality**：该研究首次系统描绘了硬骨鱼鳍再生过程中的染色质架构动态，特别是使用micro-C技术，具有一定的新颖性。然而，染色质环在基因调控中的作用已被广泛研究，将这一框架应用于再生模型是渐进式创新而非概念突破。
  - **Scientific importance**：再生过程中染色质架构如何重组是一个重要问题，该研究提供了有价值的资源。但核心发现（环改变为主、il11a功能验证）的广泛影响取决于因果证据的强度，当前版本中这一证据链尚不完整。
  - **Interdisciplinary readership**：该工作跨越了3D基因组学、再生生物学和进化发育生物学，具有吸引多学科读者的潜力。但技术门槛较高，需要作者在可读性方面做出更多努力。
  - **Technical soundness**：方法学设计总体合理，micro-C的应用是合适的。但关键功能实验的描述过于简略，跨物种比较的方法学细节不足，motif富集到功能推断的链条存在跳跃。
  - **Readability for nonspecialists**：摘要和引言写得清晰，但结果部分对非3D基因组学背景的读者可能较难理解。建议增加对micro-C原理和染色质环生物学意义的简要解释。

- **Recommendation posture** 目前证据基础尚不足以完全支持核心结论。该研究有潜力，但需要补充关键实验细节和数据分析方法。建议大修后重新评审。特别是il11a功能实验的完整描述、环/TAD/区室变化的定量比较方法、以及跨物种比较的严谨性需要加强。