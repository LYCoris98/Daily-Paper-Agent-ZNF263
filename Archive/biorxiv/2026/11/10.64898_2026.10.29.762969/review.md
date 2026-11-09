## Review setup

- **Input scope** 预印本全文（含摘要、引言、结果、讨论、材料与方法），无图/表/补充材料
- **Assessment boundary** 仅基于提供的文本内容评估科学逻辑、证据充分性和结论支撑度；无法验证图表数据、统计细节或补充文件
- **Shared manuscript claim summary** 该研究通过条件性敲除小鼠模型，在视网膜发育中比较了ChAHP复合物亚基Adnp和Chd4的功能，发现两者在视网膜生长中具有共同作用，但在细胞命运决定上存在显著差异，提示Chd4可能通过NuRD复合物发挥ChAHP非依赖性功能
- **Visible evidence base** 免疫共沉淀/质谱、免疫组化、Western blot、scRNA-seq（多组学整合）、cut&run-seq、已发表的ATAC-seq数据
- **Missing materials affecting confidence** 所有图表、补充图/表、统计细节、cut&run-seq峰调用参数、scRNA-seq聚类注释细节、差异表达基因列表

## Reviewer

- **Overall assessment** 该研究针对一个具有重要神经发育疾病相关性的染色质重塑复合物，在视网膜发育模型中进行了系统的功能解剖。研究设计合理，采用了多种互补技术（遗传学、转录组学、基因组学、蛋白质组学），并利用了作者此前建立的皮层模型进行比较。核心发现——Adnp和Chd4在视网膜中功能分化——具有新颖性和潜在的重要临床意义。然而，当前版本存在几个关键问题：scRNA-seq整合分析的批次效应控制方法需要更严格的验证；Adnp cKO中Chd4蛋白水平下降的机制未阐明；cut&run-seq数据的定量比较缺乏统计框架。这些问题的解决对于支撑"Chd4具有ChAHP非依赖性功能"的核心结论至关重要。

- **Who would be interested in the results, and why** 神经发育生物学和表观遗传学领域的研究者会对该研究感兴趣，特别是关注染色质重塑复合物在脑区特异性功能的研究组。此外，由于ADNP和CHD4与自闭症谱系障碍和智力障碍的强遗传关联，研究神经发育疾病机制的转化医学研究者也会关注。视网膜作为中枢神经系统的可及模型，该研究为理解脑区特异性染色质调控机制提供了比较框架。

- **Major strengths** 1) 研究设计具有明确的比较逻辑，通过同一驱动系（Chx10-Cre）在相同发育时间点敲除两个亚基，使表型差异可直接归因于基因功能差异；2) 多组学整合策略（scRNA-seq + cut&run-seq + 已发表ATAC-seq）提供了从基因组定位到转录输出的完整证据链；3) 作者注意到Adnp基因注释的潜在问题（readthrough转录本导致的multimapping），体现了方法学上的严谨性；4) 与作者此前在皮层中的发现形成对比，提示脑区特异性依赖，这一比较视角增加了研究的深度。

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** 数据整合与批次效应控制
- **Claim pointer** "We performed demultiplexing, filtered low quality and contaminant cells, and performed batch correction, leaving 9,580 cells from the prior Chd4 dataset, along with 4,521 cells from the new Adnp experiment" 以及后续基于整合数据的聚类和差异表达分析
- **Evidence pointer** Results: "Coordinate and divergent effects of Adnp and Chd4 on gene regulation"; Materials and Methods: "Multi-seq"
- **Concern** 两个scRNA-seq数据集（Adnp实验和Chd4实验）是独立处理的，整合时仅以"sequencing batch"作为协变量。然而，两个实验可能在不同时间、不同试剂批次、甚至不同测序深度下完成。scVI的批次校正依赖于模型假设，如果两个数据集的技术差异过大（如细胞捕获效率、测序饱和度不同），校正可能不充分或过度。此外，Adnp实验仅4,521个细胞，远少于Chd4实验的9,580个细胞，这种不平衡可能影响聚类和差异表达分析的统计功效。作者未提供整合前后的质量控制指标（如批次熵、混合度评分）来验证校正效果。
- **Why it matters** 该研究的一个核心结论是"Adnp和Chd4 cKO在转录组水平上具有相似性但Chd4影响更广泛"。如果批次效应未充分校正，观察到的差异可能部分反映技术变异而非生物学差异，这将直接影响对Chd4非依赖性功能的判断。
- **Resolution test** 提供整合前后的UMAP图对比、各批次细胞在聚类中的分布比例、以及基于批次混合度的定量评估（如kBET或LISI评分）。此外，应展示仅用Adnp实验内部对照比较的结果，以排除批次效应。

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** 蛋白稳定性与复合物完整性
- **Claim pointer** "immunohistochemistry on P1 retinas confirmed the ablation of Adnp protein, but also revealed ∼50% reduction in Chd4 protein levels. Examining Chd4 cKOs, we observed a corresponding reduction in Adnp protein levels."
- **Evidence pointer** Results: "Conditional ablation of ChAHP subunits in the developing retina"; Figure 3B-C; Figure S2
- **Concern** 作者观察到Adnp缺失导致Chd4蛋白水平下降50%，反之亦然。这一发现有两种可能解释：(1) 复合物亚基相互稳定，缺失一个导致另一个降解；(2) 存在交叉调控的转录或翻译机制。作者未提供任何实验来区分这些可能性。更重要的是，如果Adnp cKO中Chd4蛋白水平显著下降，那么Adnp cKO的表型可能部分或全部归因于Chd4功能的部分丧失，而非Adnp本身的独立功能。这直接挑战了"Adnp通过ChAHP非依赖性机制调节视网膜生长"的结论。
- **Why it matters** 该研究的核心逻辑是比较Adnp和Chd4缺失的表型差异来推断功能分工。如果两个亚基的缺失都导致对方蛋白水平下降，那么观察到的表型差异可能反映的是残余蛋白水平的差异，而非功能通路的本质差异。这需要更严格的遗传上位性分析或蛋白水平挽救实验。
- **Resolution test** 提供Adnp cKO中Chd4蛋白下降的机制分析（如mRNA水平检测区分转录vs.翻译后调控）；在Adnp cKO背景下过表达Chd4（或反之）观察表型是否恢复；或使用Chd4催化失活突变体（非缺失）来区分支架功能与酶活功能。

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** No
- **Axis** cut&run-seq定量比较
- **Claim pointer** "we performed cut&run-seq, which suggested that Adnp and Chd4 are recruited to the same genomic loci – many of which are also occupied by the Ctcf transcription factor" 以及 "we observed increased Ctcf occupancy relative to wild-type, which was reflected in an increase in called peaks from ∼45,000 up to ∼64,000"
- **Evidence pointer** Results: "Coordinate and divergent effects of Adnp and Chd4 on gene regulation"; Figure 7C-D
- **Concern** cut&run-seq数据的分析仅描述了峰的重叠和数量的变化，但缺乏定量比较的统计框架。峰数量的增加（45,000到64,000）可能反映的是峰调用阈值的敏感性变化、染色质可及性的整体改变，而非Ctcf结合位点的特异性增加。作者未提供差异结合分析（如DiffBind或MAnorm），也未说明峰数量变化的生物学意义。此外，cut&run-seq在P0进行，而scRNA-seq在P1进行，时间点的不一致可能影响数据整合的解读。
- **Why it matters** 该研究试图建立"Chd4缺失导致Ctcf占据增加"的机制模型。如果这一观察缺乏统计支撑，机制推断的基础将不牢固。峰数量的简单比较在cut&run-seq中尤其容易受技术噪声影响。
- **Resolution test** 提供基于重复样本的差异结合分析（需至少2-3个生物学重复），展示Ctcf峰变化的效应量和显著性；讨论P0与P1时间点差异对结论的影响；或将Ctcf占据变化与差异表达基因进行关联分析。

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** 表型分析的定量与统计
- **Claim pointer** "the cKO retinas were considerably smaller. Cell counts revealed clear reductions in the ONL and INL" 以及 "significant reductions in many cell types, while offsetting increases in specific cell types were not observed"
- **Evidence pointer** Results: "Adnp is required for retinal growth"; Figures 3G-H, 4A-M
- **Concern** 细胞计数和视网膜大小的定量分析缺乏详细的统计描述。作者未报告每个基因型/时间点的生物学重复数、计数方法（如是否使用立体学方法）、以及统计检验的具体类型。此外，作者提到"small numbers of mismigrated cells"和"a few ectopic ganglion cells"，但这些定性描述缺乏定量支撑。对于Adnp cKO中"no change in proportionality"的结论，需要提供效应量和统计功效分析。
- **Why it matters** 该研究的一个关键结论是Adnp缺失导致视网膜发育不良但不改变细胞命运比例。这一阴性结论需要足够的统计功效来支撑，否则可能因检测灵敏度不足而得出错误的"无差异"结论。
- **Resolution test** 提供完整的统计方法描述（重复数、检验类型、多重比较校正）、细胞计数的详细方法（如是否盲法计数）、以及基于效应量和变异度的功效分析。

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** 方法学描述完整性
- **Affected element** cut&run-seq实验流程
- **Evidence pointer** Materials and Methods: "Cut&run-seq"
- **Issue** cut&run-seq方法描述过于简略，未提及细胞数量、抗体浓度、测序深度、峰调用软件及参数、以及重复数。
- **Required correction** 补充完整的实验参数和分析流程，或引用已发表的详细方法论文。

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** 数据可及性
- **Affected element** 数据存储
- **Evidence pointer** Data availability
- **Issue** 作者声明scRNA-seq和cut&run-seq数据"will be uploaded to GEO"，但未提供访问编号或预计时间。对于预印本读者，数据的即时可及性对验证结论很重要。
- **Required correction** 提供GEO访问编号（即使是临时编号），或至少在预印本中提供审阅者链接。

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** 文献引用完整性
- **Affected element** 引言和讨论中的背景引用
- **Evidence pointer** Introduction; Discussion
- **Issue** 引言中关于ChAHP复合物的描述主要引用了Ostapcuk等人2018年的工作，但该领域近年有较多进展（如Adnp在增强子调控中的功能、Chd4在神经干细胞中的非酶活功能等），部分相关文献未引用。
- **Required correction** 补充近3-5年的相关文献，特别是关于ChAHP在神经发育中的最新研究。

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** 图表引用一致性
- **Affected element** 结果部分图表引用
- **Evidence pointer** Results sections
- **Issue** 文中引用了Figure S1-S7和Table S1-S3，但未提供补充材料的图例或简要说明，读者无法在预印本中获取这些信息。
- **Required correction** 在预印本中附上补充材料的图例列表，或提供补充文件的直接链接。

- **Technical failings that need to be addressed before the case is established** R1-M1（批次效应控制）、R1-M2（蛋白交叉调控的机制区分）、R1-M3（cut&run-seq定量比较的统计框架）

- **Assessment against Nature-style criteria** 
  - **Originality** 该研究首次在视网膜发育模型中系统比较了ChAHP复合物两个核心亚基的功能，发现脑区特异性的功能分化，这一发现具有原创性。特别是"Adnp缺失导致增殖缺陷而Chd4缺失导致命运决定异常"的分离，为理解染色质重塑复合物的亚基特异性功能提供了新视角。
  - **Scientific importance** 如果核心结论得到充分支撑，该研究对理解ADNP和CHD4突变导致的不同神经发育表型具有重要价值。然而，目前证据的强度不足以完全确立"Chd4通过NuRD而非ChAHP调控视网膜命运决定"这一关键论断。
  - **Interdisciplinary readership** 该研究跨越发育神经生物学、表观遗传学和神经遗传学三个领域，对这三个领域的研究者都有吸引力。视网膜作为模型系统的可及性也增加了其方法学上的参考价值。
  - **Technical soundness** 研究采用了多种先进技术（scRNA-seq、cut&run-seq、条件性敲除），技术路线合理。但存在上述提到的批次效应控制、蛋白交叉调控机制、cut&run-seq定量比较等关键技术问题，需要在发表前解决。
  - **Readability for nonspecialists** 文章结构清晰，逻辑连贯，对背景知识的介绍充分。但部分技术细节（如scVI模型配置、cut&run-seq分析流程）对非专业读者可能较难理解，建议在结果部分增加更直观的解释。

- **Recommendation posture** 目前证据尚不足以完全确立核心结论。该研究具有重要的科学价值和原创性，但需要解决批次效应控制、蛋白交叉调控机制区分、cut&run-seq定量比较等关键技术问题。建议作者在补充实验和重新分析后重新提交。如果这些问题得到充分解决，该研究有潜力发表在高影响力期刊。

## Risk / unsupported claims

1. "Chd4 has additional ChAHP-independent functions in regulating progenitor fate decisions" — 该结论依赖于Adnp和Chd4 cKO表型的差异，但Adnp cKO中Chd4蛋白下降50%的事实使这一推断复杂化，目前证据不足以排除"部分表型差异源于Chd4水平下降"的可能性
2. "Adnp regulates retinal growth in a ChAHP-independent manner" — 作者提出这一可能性，但未提供直接证据（如ChAHP非依赖性Adnp靶基因的鉴定）
3. "extensive co-recruitment of Adnp and Chd4 to Ctcf-occupied loci" — 基于cut&run-seq峰重叠，但缺乏定量比较和统计检验
4. "increased Ctcf occupancy in Chd4 cKOs" — 基于峰数量从45,000到64,000的变化，但未提供差异结合分析
5. "Adnp cKOs did not alter cell type specification" — 阴性结论，但未提供统计功效分析
6. "the two proteins formed a complex in vivo" — 基于免疫共沉淀，但未提供定量比较或对照实验的详细描述
7. "Adnp exons are doubly annotated... creating a multi-mapping problem" — 该解释合理但未通过实验验证（如RT-PCR或RNA-FISH）直接证实