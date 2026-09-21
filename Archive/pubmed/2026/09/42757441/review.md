## Review setup
- **Input scope** 摘要（仅提供摘要文本，无正文、图表或补充材料）
- **Assessment boundary** 仅评估摘要中提出的概念性主张及其论证逻辑；无法评估方法学、数据支撑或实验验证
- **Shared manuscript claim summary** 该文主张转录与3D基因组组织之间的因果关系尚未明确；基于已有证据，转录并非大规模基因组特征（如compartment和TAD）建立的严格必要条件，而主要在较细空间尺度上影响增强子-启动子相互作用、局部染色质环和微区室；RNA分子、聚合酶驱动的超螺旋和R-loop形成可能在基因水平调节染色质组织；基因组架构为基因表达提供相对稳定的框架，而转录及相关因子以背景依赖方式细化染色质组织
- **Visible evidence base** 摘要中提及的文献类别（perturbation, imaging, modeling studies）及概念性论述；无具体数据、图表或方法细节
- **Missing materials affecting confidence** 正文全文、图表、参考文献列表、方法部分、系统检索策略或文献筛选标准均未提供；无法验证文献覆盖的全面性或主张的代表性

## Reviewer
- **Overall assessment** 这是一篇概念性综述的摘要，提出一个及时且重要的问题，即转录与3D基因组组织的因果关系方向。摘要清晰地区分了不同空间尺度上的证据强度，并提出了一个合理的综合框架，即基因组架构提供稳定框架而转录进行局部细化。然而，摘要中若干关键主张缺乏可验证的文献支撑细节，且部分表述存在过度概括的风险。作为综述类文章，其价值将高度依赖于正文中对证据的系统性梳理和批判性评估，而当前摘要无法充分展示这一点。

- **Who would be interested in the results, and why** 该综述将吸引染色质生物学、基因表达调控、表观遗传学和3D基因组学领域的研究人员。具体而言，从事Hi-C、Micro-C、成像和单分子研究的研究者，以及关注转录与核组织之间因果关系的计算生物学家和生物物理学家，都会对该综述感兴趣。此外，该文对"cause versus consequence"框架的讨论可能对设计扰动实验的研究组具有指导意义。

- **Major strengths** 
  1. 问题定位清晰且具有领域重要性，直接针对一个长期存在争议的核心问题
  2. 摘要明确区分了不同空间尺度（大规模特征 vs. 局部相互作用）上的证据强度，避免了过度简化的"转录需要或不需要3D组织"的二元论述
  3. 提出了一个可操作的综合框架（稳定框架加背景依赖的细化），为未来研究提供了概念性指导
  4. 提及了多种机制（RNA分子、超螺旋、R-loop），显示了对分子机制的全面考虑

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** 证据充分性
- **Claim pointer** "Evidence from perturbation, imaging, and modeling studies suggests that transcription is not strictly required for the establishment of large-scale genome features such as compartments and topologically associating domains (TADs)"
- **Evidence pointer** 摘要，第2-3句；具体文献未提供
- **Concern** 摘要声称"perturbation, imaging, and modeling studies"支持转录并非大规模基因组特征建立的严格必要条件，但未提供任何具体研究示例、实验系统或证据强度的评估。该领域存在相互矛盾的文献，部分研究表明转录抑制可影响compartment segregation，而另一些研究则显示TAD在转录抑制后仍保持。摘要未说明作者如何权衡这些矛盾证据，也未提供纳入或排除文献的标准。
- **Why it matters** 这是全文的核心主张之一。如果该主张的证据基础不透明或选择性引用，将直接影响综述的可信度和结论的可靠性。读者需要了解作者如何系统性地评估了该领域的证据，而非仅接受一个概括性结论。
- **Resolution test** 在正文中提供系统性的文献综述方法（如检索策略、纳入排除标准），并明确讨论支持与反对该主张的关键研究及其局限性。摘要中应至少提及1-2个代表性研究或指出综述中对该证据分歧的讨论位置。

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** 主张的精确性
- **Claim pointer** "transcription seems to exert more prominent effects at finer spatial scales, where it influences enhancer-promoter interactions, local chromatin loops, and microcompartments"
- **Evidence pointer** 摘要，第4句；具体文献未提供
- **Concern** 摘要将转录对"finer spatial scales"的影响作为一个统一主张，但enhancer-promoter interactions、local chromatin loops和microcompartments是不同性质的染色质特征，其与转录的因果关系可能各不相同。例如，某些增强子-启动子相互作用的建立可能先于转录激活，而另一些则可能由转录本身驱动。摘要未区分这些不同特征与转录之间的因果方向差异，也未说明"influences"具体指建立、维持还是调节。
- **Why it matters** 该主张是全文的第二个核心论点。如果不同空间尺度上的证据被混为一谈，将削弱综述作为领域参考的价值。精确区分不同染色质特征与转录的因果关系是回答"cause, consequence, or coordination"问题的关键。
- **Resolution test** 在正文中分别讨论enhancer-promoter interactions、local chromatin loops和microcompartments与转录的因果关系证据，并明确区分哪些是建立、哪些是维持、哪些是调节。摘要中应反映这种区分，或至少指出不同特征之间的证据差异。

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** No
- **Axis** 概念框架的完整性
- **Claim pointer** "genome architecture provides a relatively stable framework for regulated gene expression, while transcription and associated factors refine chromatin organization in a context-dependent manner"
- **Evidence pointer** 摘要，倒数第2句
- **Concern** 摘要提出的综合框架（稳定框架加背景依赖的细化）虽然合理，但未考虑时间动态性。3D基因组组织在细胞周期、分化和发育过程中会发生显著重排，而转录活动也呈现动态变化。"relatively stable"的表述可能低估了基因组组织的动态特性，也未讨论在何种时间尺度上该框架成立。
- **Why it matters** 如果该框架被表述为普遍适用，可能误导读者对基因组组织动态性的理解。细胞类型特异性和发育阶段特异性的基因组重排是已知现象，综述应明确其框架的适用范围和边界条件。
- **Resolution test** 在正文中讨论该框架在不同时间尺度（分钟、小时、细胞周期、发育）和不同细胞状态下的适用性，并在摘要中适当限定"relatively stable"的适用范围。

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** 术语精确性
- **Affected element** "microcompartments"
- **Evidence pointer** 摘要，第4句
- **Issue** "microcompartments"在3D基因组学文献中并非标准术语，可能指代不同的结构（如转录工厂、相分离凝聚体、或Hi-C中检测到的小规模结构域）。该术语的使用可能造成歧义。
- **Required correction** 在正文中明确定义"microcompartments"在该综述中的具体含义，或使用更标准的术语（如"sub-TAD structures"、"transcription factories"或"phase-separated condensates"）并说明选择理由。

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** 机制讨论的深度
- **Affected element** "RNA molecules, polymerase-driven supercoiling, and R-loop formation may further modulate chromatin organization at the gene level"
- **Evidence pointer** 摘要，第5句
- **Issue** 摘要将三种机制并列提出，但未说明它们之间的相互关系或相对贡献。例如，R-loop形成与超螺旋之间存在已知的相互影响，而RNA分子可能通过多种途径（如相分离、RNA-DNA相互作用）发挥作用。
- **Required correction** 在正文中分别讨论每种机制的证据强度，并说明它们之间可能的协同或拮抗关系。摘要中可简要指出这些机制可能相互关联。

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** 未来方向的明确性
- **Affected element** "systematic, multi-scale perturbations across different biological and biochemical systems"
- **Evidence pointer** 摘要，最后一句
- **Concern** 该未来方向建议较为笼统，未具体说明哪些类型的扰动（如快速转录抑制、基因座特异性操控、时空调控）或哪些系统（如体外重构、类器官、体内模型）最为关键。
- **Required correction** 在正文中提供更具体的未来研究方向建议，包括推荐的技术路线和预期能解决的关键问题。摘要中可适当增加一两个具体例子。

- **Technical failings that need to be addressed before the case is established** R1-M1和R1-M2所涉及的主张需要正文中系统性的文献证据支撑才能确立。当前摘要中这些主张以概括性陈述呈现，缺乏可验证的文献基础。R1-M3涉及的概念框架需要更明确的边界条件定义。

- **Assessment against Nature-style criteria** 
  - **Originality** 该综述的问题框架（cause, consequence, or coordination）并非全新，但将证据按空间尺度进行区分并综合为一个统一框架具有一定的新颖性。然而，摘要中未展示与已有综述的差异化定位。
  - **Scientific importance** 该问题对3D基因组学和转录调控领域具有高度重要性，是领域内持续争论的核心问题。如果综述能够系统性地整合现有证据并提供清晰的概念框架，将具有较高的科学价值。
  - **Interdisciplinary readership** 该主题涉及分子生物学、生物物理学、计算生物学和基因组学，具有跨学科吸引力。但摘要的表述方式可能对非专业读者不够友好，部分术语（如"microcompartments"）缺乏定义。
  - **Technical soundness** 作为综述，技术可靠性取决于文献综述的系统性和证据评估的客观性。当前摘要无法验证这一点，但概念框架的逻辑一致性较好。
  - **Readability for nonspecialists** 摘要整体可读性尚可，但部分概念（如TAD、compartment、supercoiling）对非专业读者可能需要更多背景说明。摘要的抽象层次较高，缺乏具体例子。

- **Recommendation posture** 目前无法从摘要单独判断该综述是否达到发表标准。概念框架合理且问题重要，但核心主张的证据基础需要正文验证。建议在获得全文后进行完整评估。当前立场为"conditional"，取决于正文中证据综述的系统性和批判性。

## Risk / unsupported claims
- "transcription is not strictly required for the establishment of large-scale genome features" — 摘要中无具体文献支撑，且该领域存在矛盾证据，需正文系统综述验证
- "transcription seems to exert more prominent effects at finer spatial scales" — 缺乏对不同染色质特征（enhancer-promoter interactions、local chromatin loops、microcompartments）证据差异的区分
- "RNA molecules, polymerase-driven supercoiling, and R-loop formation may further modulate chromatin organization" — 三种机制的相对贡献和相互关系未说明
- "genome architecture provides a relatively stable framework" — "relatively stable"缺乏时间尺度和细胞状态的条件限定
- 摘要中所有关于"evidence suggests"的表述均无法从摘要本身验证，需依赖正文的文献综述质量