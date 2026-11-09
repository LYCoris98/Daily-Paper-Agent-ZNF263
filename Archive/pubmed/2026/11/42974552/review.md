## Review setup
- **Input scope** 完整手稿（含摘要、方法、结果、讨论、图表引用及数据可用性声明）
- **Assessment boundary** 仅基于提供的材料进行评估；未提供补充材料、图表文件及原始数据
- **Shared manuscript claim summary** 该研究声称BET抑制剂JQ1在胶质母细胞瘤（GB）来源的干细胞样球体（GS）中诱导以HOXA为主的造血干细胞样HOX signature的协同抑制；HOXA10敲低可部分模拟BETi效应；高HOX GS系呈现许可性表观遗传状态，包括HOXA区域超增强子、开放染色质及局部DNA低甲基化；HOXA10不足以驱动或拯救该signature。
- **Visible evidence base** 正文中引用的图1-5、图S1-S8、表S1-S6；方法学描述；数据可用性声明（GEO accession numbers）
- **Missing materials affecting confidence** 补充材料全文、图表文件、原始测序数据、统计分析细节（如差异表达分析的完整协变量模型）、ChIP-seq峰调用参数、Micro-C数据处理细节均未提供，限制了对核心结论的独立验证能力

## Reviewer
- **Overall assessment** 该研究针对GB中HOX signature的表观遗传调控机制进行了系统性的多组学分析，提出了BETi作为靶向该signature的潜在治疗策略。研究设计合理，从药物扰动到遗传扰动再到染色质结构分析，逻辑链条完整。然而，核心结论中关于HOXA10作为HOX cluster协同调控关键节点的证据强度不足，且缺乏功能验证实验（如HOXA10过表达是否足以激活signature）来支撑因果性声明。多组学数据整合分析深度有限，部分结论（如超增强子、CTCF loop的功能意义）停留在相关性层面。
- **Who would be interested in the results, and why** 胶质母细胞瘤表观遗传学与治疗抵抗领域的研究者；关注BET抑制剂在实体瘤中应用的转化医学研究者；HOX基因调控机制与肿瘤干细胞生物学方向的研究者。该研究提供了BETi靶向HOX signature的机制性框架，对设计基于表观遗传药物的联合治疗策略具有参考价值。
- **Major strengths** 1）多组学整合策略（RNA-seq、ChIP-seq、ATAC-seq、Micro-C、甲基化）系统描绘了HOXA位点的表观遗传状态；2）药物扰动与遗传扰动（shHOXA10）的平行设计增强了结论的可信度；3）将HOX signature与BET依赖性转录调控联系起来，提出了潜在的治疗靶点；4）数据公开可获取，符合可重复性要求。
- **Major Concerns** 见下方详细条目
- **Minor Comments** 见下方详细条目
- **Technical failings that need to be addressed before the case is established** R1-M1（HOXA10敲低效应的特异性与因果性）、R1-M2（HOXA10过表达实验的结论过度解读）、R1-M3（超增强子与CTCF loop的功能证据不足）
- **Assessment against Nature-style criteria** **Originality**：中等。BETi在GB中的研究已有报道，但聚焦于HOX signature的协同调控及染色质结构层面的机制解析具有一定新颖性。**Scientific importance**：中等。HOX signature与GB预后的关联已有文献支持，但该研究提供的机制性见解（BET依赖性调控、超增强子结构）对理解GB表观遗传异质性有贡献，尚未达到范式转变级别。**Interdisciplinary readership**：有限。主要吸引神经肿瘤学与表观遗传学交叉领域读者，对更广泛的生物医学受众吸引力不足。**Technical soundness**：方法学描述基本规范，但关键实验（HOXA10过表达、ChIP-seq分析）存在设计或解读上的缺陷（见R1-M2、R1-M3）。**Readability for nonspecialists**：摘要和引言清晰，但结果部分涉及大量组学术语，对非专业读者有一定门槛。总体而言，该研究符合专业期刊标准，但距离Nature级影响力尚有差距。
- **Recommendation posture** 目前证据不足以完全支撑核心因果性声明；建议在补充关键实验（HOXA10过表达功能验证、BETi时间梯度下的染色质动态变化）后重新评估。若作者能提供补充材料中更详细的分析结果，可能提升结论的可信度。

### Major Concerns

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** 因果推断有效性
- **Claim pointer** "Knockdown of HOXA10 alone yielded similar effects, decreasing expression of HOXA genes, reducing proliferation, self-renewal capacity, and triggering senescence"（摘要及结果部分）
- **Evidence pointer** Figure 2, Figure 3, Results section "HOXA10 Knockdown Is Associated With the Repression of Other HOXA Genes"
- **Concern** 作者声称HOXA10敲低"协同下调"其他HOXA基因，但未提供证据排除脱靶效应或非特异性应激反应。shRNA介导的敲低可能引发全局性转录扰动，而不仅仅是HOXA cluster特异性效应。此外，HOXA10敲低与JQ1处理在HOXA基因表达上的"相似效应"缺乏定量比较（如效应大小、统计检验），无法判断是否真正"相似"。
- **Why it matters** 该claim是全文核心因果链条的关键环节：如果HOXA10敲低效应并非HOXA cluster特异性，则"HOXA10作为BETi下游关键节点"的结论不成立。此外，缺乏HOXA10过表达的功能验证（见R1-M2），使得"HOXA10足以驱动signature"的相反方向因果性也未得到检验。
- **Resolution test** 提供shHOXA10敲低后的全转录组分析，展示HOXA cluster基因的下调是否显著高于全局基因下调背景；进行RNA-seq数据的GSEA分析，验证HOXA signature的特异性富集；补充HOXA10过表达实验，检验是否足以激活HOXA cluster或逆转BETi效应。

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** 结论与证据匹配度
- **Claim pointer** "Ectopic HOXA10 expression failed to reactivate the HOXA cluster or reverse BETi-mediated biological effects"（结果部分）
- **Evidence pointer** Results section "Ectopic HOXA10 Expression Is Insufficient to Activate the HOX Transcriptional Program or Counteract BETi"
- **Concern** 该实验的解读存在逻辑问题。作者在低HOX GS系（LN-2540GS）中过表达HOXA10，发现未能激活HOXA cluster，据此得出结论"HOXA10不足以驱动signature"。然而，LN-2540GS可能缺乏其他必要的协同因子（如特定的染色质状态、转录因子环境），因此该阴性结果不能排除HOXA10在其他context下的充分性。此外，在高HOX GS系中过表达HOXA10并观察BETi效应，但未检测过表达是否达到生理相关水平，也未验证HOXA10蛋白的核定位和功能活性。
- **Why it matters** 该实验旨在检验HOXA10的充分性，但实验设计未能有效控制细胞context差异，导致阴性结果的解读范围受限。如果HOXA10确实不是充分条件，则该结论需要更严谨的实验支持；如果实验设计存在缺陷，则结论可能被错误否定。
- **Resolution test** 在高HOX GS系中敲低HOXA10后回补外源HOXA10（rescue实验），检验是否能恢复HOXA cluster表达和细胞表型；在低HOX GS系中过表达HOXA10的同时引入其他候选协同因子（如HOXA cluster的增强子激活剂），检验是否协同激活signature；验证过表达HOXA10的蛋白水平、亚细胞定位和转录活性。

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** No
- **Axis** 机制证据深度
- **Claim pointer** "Integrative epigenomic analysis of high-HOX-GS revealed concerted activation of the HOXA region, with broad domains of H3K27ac/H3K4me3 associated with super-enhancer activity, open chromatin (ATAC), and focal DNA hypomethylation. Architectural changes included altered CCCTC-binding factor (CTCF) interactions and increased promoter-anchored looping."
- **Evidence pointer** Figure 5, Results section "Epigenetic Landscape of Other HOX Clusters Contributing to the High-HOX Signature"
- **Concern** 超增强子（SE）的鉴定标准未明确说明（如SE评分阈值、enhancer-gene关联方法）。CTCF loop差异和启动子锚定loop增加的functional consequence未被验证（如CRISPR干扰特定loop或SE区域后HOXA表达是否改变）。此外，Micro-C数据的分辨率和统计功效未报告，无法评估差异loop的可靠性。
- **Why it matters** 该claim是"表观遗传脆弱性"概念的核心支撑，但当前证据仅显示相关性。如果SE或loop结构并非功能必需，则"脆弱性"的机制基础不成立，BETi敏感性的解释也需要修正。
- **Resolution test** 提供SE鉴定和enhancer-promoter关联的详细参数和统计阈值；在至少一个高HOX GS系中进行CRISPR干扰（CRISPRi）靶向HOXA SE区域或关键CTCF位点，检验HOXA表达和细胞表型变化；报告Micro-C数据的测序深度、分辨率及差异loop的统计检验方法。

### Minor Comments

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** 方法透明度
- **Affected element** 差异表达分析统计模型
- **Evidence pointer** Methods section "RNA-Seq Sample and Library Preparation, Sequencing, Preprocessing, and Pathway Analysis"
- **Issue** 差异表达分析使用了"generalized linear mixed model with a negative binomial distribution where construct type and replicate (batch) information are included as random intercepts"，但未说明该模型的具体实现（如使用的R包、公式、多重检验校正方法）。"construct type"作为随机效应而非固定效应的合理性未解释。
- **Required correction** 提供完整的统计模型描述，包括软件包（如DESeq2、edgeR或自定义模型）、固定效应和随机效应的设定、多重检验校正方法（如BH-FDR），并说明模型选择的依据。

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** 数据呈现完整性
- **Affected element** 图例信息
- **Evidence pointer** Figure 1, Figure 2, Figure 3, Figure 5
- **Issue** 图例中未说明生物学重复数（n）、误差棒类型（SD/SEM）、统计检验方法及显著性标注的具体含义。部分图（如图3C）的β-galactosidase活性数据未展示原始值分布。
- **Required correction** 在所有图例中补充n值、误差棒定义、统计检验名称和显著性阈值；对于关键实验（如增殖、神经球形成），考虑展示单个数据点以评估数据分布。

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** 文献支撑充分性
- **Affected element** Discussion部分关于HOX signature与GB预后的关联
- **Evidence pointer** Discussion section, 参考文献16, 19, 20, 43
- **Issue** 讨论中声称HOX signature与GB预后不良相关，但未提供该关联的效应量或具体参考文献的统计结果。此外，关于BETi在GB中的已有临床前研究（如OTX015等）未在讨论中充分对比。
- **Required correction** 补充HOX signature与GB预后关联的具体数据（如HR值、风险比）或引用更详细的综述；在讨论中增加与已有BETi在GB中研究的对比，明确本研究的增量贡献。

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** 术语准确性
- **Affected element** "senescence-like phenotype"
- **Evidence pointer** Results section "HOXA10 Knockdown Reduces Proliferation, Self-Renewal Capacity, and Induces a Senescence-Like Phenotype"
- **Issue** 作者使用"senescence-like phenotype"描述β-galactosidase活性升高，但未提供其他衰老标志物（如p16、p21表达、SAHF形成）的验证。β-galactosidase活性升高也可反映其他细胞状态（如应激诱导的衰老、分化）。
- **Required correction** 补充至少一个额外的衰老标志物检测，或修改术语为"β-galactosidase activity increase"以避免过度解读。

## Risk / unsupported claims
- "HOXA10 knockdown alone yielded similar effects" — 缺乏与JQ1效应的定量比较，且未排除脱靶效应
- "Ectopic HOXA10 expression failed to reactivate the HOXA cluster" — 实验设计未控制细胞context差异，阴性结论过度泛化
- "Architectural changes included altered CTCF interactions and increased promoter-anchored looping" — 未提供功能验证，且Micro-C数据统计细节缺失
- "These findings position the HOX-signature as a potential therapeutic target" — 缺乏体内实验或患者来源数据支持治疗靶点的临床相关性
- "BETi rapidly suppressed cluster-wide expression... without concurrent alterations in histone modifications" — 该claim基于2小时时间点，无法排除更长时间尺度上的表观遗传重塑