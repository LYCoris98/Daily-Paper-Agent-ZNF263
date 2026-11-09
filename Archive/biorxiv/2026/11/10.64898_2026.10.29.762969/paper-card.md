## 01 基本信息

- **标题**：Molecular dissection of the ChAHP complex subunits Adnp and Chd4 reveals common and divergent functions in retinal development
- **作者**：Medisetti S; Kalinina A; Shah S; Fayaz MA; Clémot-Dupont S; Picketts DJ; Mattar P
- **单位**：未提供（根据基金信息推测为加拿大渥太华大学/渥太华医院研究所系统）
- **期刊/平台**：bioRxiv（预印本）
- **年份**：2026
- **论文类型**：预印本（原创研究）
- **领域**：发育神经生物学、表观遗传学、视网膜发育、染色质重塑
- **关键词**：ChAHP复合物、Adnp、Chd4、视网膜发育、神经祖细胞、NuRD复合物、Ctcf、条件性基因敲除、单细胞RNA测序、CUT&RUN
- **DOI/ID**：10.64898/2026.10.29.762969
- **代码**：未提供
- **数据**：scRNA-seq和CUT&RUN-seq数据将上传至GEO；蛋白质组学数据将提交至PRIDE（截至阅读时未提供登录号）
- **阅读日期**：2026年11月（根据预印本日期推断）
- **在「cpdch基因家族」方向中的位置**：本文直接研究Chd4（即cpdch基因家族核心成员）及其在ChAHP复合物中的功能，是cpdch基因家族在视网膜发育中功能解析的关键文献。该文通过条件性敲除策略，区分了Chd4依赖ChAHP复合物与非ChAHP依赖（即NuRD复合物）的功能，为理解cpdch基因家族成员在不同组织中的功能分工提供了重要范式。

## 02 一句话总结

本文通过视网膜特异性条件性敲除Adnp和Chd4，结合组织学、scRNA-seq和CUT&RUN-seq，发现Adnp主要通过ChAHP复合物调控视网膜生长（祖细胞增殖与存活），而Chd4还通过NuRD复合物独立调控细胞命运决定，表明视网膜发育中Chd4的功能大部分不依赖ChAHP。

## 03 研究问题

- **具体问题**：ChAHP染色质重塑复合物的两个亚基Adnp和Chd4在视网膜发育中分别发挥什么功能？它们的功能是共同的（通过ChAHP复合物）还是分化的（各自独立）？
- **为什么重要**：ADNP和CHD4均与神经发育障碍（HVDAS和SIHIWES综合征）密切相关，且两者共享相似的表观遗传特征。理解它们在神经发育中的共同与分化功能，对阐明这些疾病的发病机制至关重要。此外，视网膜是研究神经祖细胞命运决定的理想模型系统。
- **现有方法不足**：Adnp和Chd4的种系敲除均导致早期胚胎致死（Adnp约E9，Chd4在植入前），无法研究其在神经发育后期的功能。脑-wide条件性敲除（Nestin-Cre）也因围产期致死而无法进行后期分析。此前在端脑（Emx1-Cre）的研究显示Adnp和Chd4表型高度相似，但其他脑区是否如此尚不清楚。
- **精确研究问题**：Can conditional ablation of Adnp versus Chd4 in the developing retina reveal common (ChAHP-dependent) versus divergent (ChAHP-independent) functions in retinal growth and cell fate specification?

## 04 背景与发展脉络

> 注：此脉络基于本文框架及引文，标记为「经外部核验」的部分以引文为准。

1. **ChAHP复合物的发现与初步表征**（Ostapcuk et al., 2018）：首次描述ChAHP复合物由CHD4、ADNP和HP1（Cbx1/3/5）组成，在胚胎干细胞中调控基因表达。局限：主要在体外多能干细胞中研究，体内神经发育功能未知。
2. **ADNP与神经发育障碍的关联**（Helsmoortel et al., 2014; De Rubeis et al., 2013; Satterstrom et al., 2020）：ADNP是自闭症谱系障碍中最常见的de novo突变基因之一，HVDAS综合征以智力障碍和自闭症为特征。局限：机制不清。
3. **CHD4与SIHIWES综合征的关联**（Sifrim et al., 2016; Weiss et al., 2016, 2020）：CHD4突变导致SIHIWES综合征，与HVDAS共享相似的表观遗传特征（Karimi et al., 2025）。局限：神经发育机制不明。
4. **Chd4在端脑发育中的功能**（Nitarska et al., 2016）：Chd4通过NuRD复合物调控端脑神经发生。局限：脑-wide敲除致死，无法研究后期功能。
5. **Adnp和Chd4在端脑中的条件性敲除**（Clémot-Dupont et al., 2024; Larrigan et al., 2023, 2026）：Emx1-Cre驱动的Adnp和Chd4条件性敲除显示高度相似的皮层表型，提示ChAHP在端脑中的主导作用。局限：仅研究了端脑。
6. **本研究的定位**：将Adnp和Chd4的条件性敲除扩展到视网膜，发现与端脑不同的结果——视网膜中Chd4的功能大部分不依赖ChAHP，提示不同脑区对ChAHP的依赖性存在差异。

## 05 核心痛点

| 痛点 | 表现 | 成因或作者解释 | 文中证据 |
|------|------|----------------|----------|
| Adnp转录本检测困难 | 多个RNA-seq数据集中Adnp表达缺失或极低 | Adnp外显子在鼠基因组中被双重注释，存在一个由Adnp外显子剪接到上游Dpm1基因的readthrough转录本（NR_132310），造成多比对问题，导致模糊比对的reads被丢弃 | Results "ChAHP complex expression during retinal development" 节，Fig. S1 |
| 种系敲除致死 | Adnp和Chd4种系敲除均早期胚胎致死，无法研究神经发育后期功能 | Adnp敲除约E9死亡，Chd4敲除在植入前阶段致死 | Introduction 节，引用 Pinhasov et al., 2003; O'Shaughnessy-Kirwan et al., 2015 |
| 脑-wide条件性敲除限制 | Nestin-Cre驱动的Chd4敲除在围产期死亡，无法进行后期分析 | Chd4在广泛神经前体细胞中敲除导致严重发育缺陷 | Introduction 节，引用 Nitarska et al., 2016 |
| 端脑与视网膜表型不一致 | Adnp和Chd4在端脑中表型高度相似，但在视网膜中显著分化 | 不同脑区对ChAHP复合物的依赖性不同；Chd4在视网膜中主要通过NuRD复合物发挥功能 | Discussion 节 |
| Chd4敲除后Adnp蛋白水平下降 | Chd4 cKO中Adnp蛋白减少约50% | 作者推测ChAHP复合物完整性对亚基稳定性重要 | Results "Conditional ablation of ChAHP subunits" 节，Fig. S2 |

## 06 核心思想

**1) 表面方法**：
构建Adnp条件性敲除等位基因（CRISPR/Cas9引入loxP位点），利用Chx10-Cre驱动视网膜特异性敲除，与已有的Chd4条件性敲除小鼠进行比较。通过组织学分析（细胞计数、增殖/凋亡标记）、scRNA-seq（转录组分析）和CUT&RUN-seq（基因组结合分析）系统比较Adnp和Chd4敲除后的表型与分子变化。

**2) 核心洞察**：
- Adnp和Chd4虽然形成ChAHP复合物并在视网膜中广泛共表达，但它们的敲除表型显著不同：Adnp主要影响视网膜生长（祖细胞增殖减少、凋亡增加），而Chd4主要影响细胞命运决定（细胞类型比例失衡）。
- 蛋白质组学显示Chd4的互作组包含大量NuRD复合物亚基，而Adnp的互作组中NuRD亚基不富集，提示Chd4在视网膜中主要通过NuRD复合物发挥功能。
- 基因组结合分析显示Adnp和Chd4在Ctcf占据的位点共定位，但Chd4敲除后Ctcf占据增加，提示Chd4的染色质重塑活性可能对抗Ctcf的结合。
- 端脑与视网膜表型的差异提示：不同脑区对ChAHP复合物的依赖性不同，这可能解释了为什么ADNP和CHD4突变虽然共享表观遗传特征，但临床表型存在差异。

**3) 可能的普适教训** [Analysis]：
- 同一蛋白复合物的不同亚基在不同组织/发育阶段可能具有截然不同的功能权重——复合物整体功能不能简单从单一组织的研究外推。
- 条件性敲除策略结合多组学比较（表型+转录组+基因组结合）是解析复合物亚基功能分化的有效范式。
- 基因注释问题（如readthrough转录本）可能导致表达数据的系统性偏差，需要多方法验证。

## 07 方法总览

- **输入**：Adnp条件性敲除小鼠（新构建）、Chd4条件性敲除小鼠（已有）、Chx10-Cre转基因小鼠；P0-P21视网膜组织
- **输出**：视网膜表型描述（大小、细胞组成）、转录组变化（scRNA-seq）、基因组结合图谱（CUT&RUN-seq）、蛋白互作组（coIP-MS）
- **主要模块**：
  1. 遗传学：Adnp flox等位基因构建（CRISPR/Cas9）、视网膜特异性敲除（Chx10-Cre）
  2. 组织学：免疫荧光染色（细胞类型标记物）、细胞计数、增殖（Ki67）和凋亡（activated caspase-3）检测
  3. 蛋白质互作：coIP + 质谱（LC-MS/MS）
  4. 转录组：scRNA-seq（10X Genomics）+ Multi-seq多重样本标记 + scVI整合分析
  5. 基因组结合：CUT&RUN-seq（Adnp、Chd4、Ctcf抗体）
- **训练/分析流程**：scRNA-seq数据经CellRanger处理→deMULTIplex去多重化→Scanpy质量控制→scVI批次校正→Leiden聚类→差异表达分析
- **反馈回路**：表型发现（Adnp vs Chd4差异）→ 转录组验证 → 基因组结合解释 → 蛋白互作补充机制
- **假设**：Chx10-Cre在视网膜祖细胞中高效且特异；Adnp flox等位基因敲除后无功能蛋白残留；scRNA-seq和CUT&RUN-seq数据的批次效应可通过计算方法校正

## 08 核心模块拆解

| 模块 | 功能 | 为何需要 | 输入输出 | 支撑证据 | 移除后的已知或预期影响 |
|------|------|----------|----------|----------|------------------------|
| Adnp条件性敲除小鼠构建 | 实现视网膜特异性Adnp敲除 | 种系敲除致死，需要时空可控的敲除策略 | 输入：CRISPR靶向载体；输出：Adnp flox小鼠 | Results "Conditional ablation" 节，Fig. 3A-C | 无法研究Adnp在视网膜中的功能（预期影响） |
| 组织学表型分析 | 定量比较Adnp和Chd4敲除后的视网膜形态与细胞组成 | 确定表型相似性与差异性 | 输入：P21视网膜切片；输出：各层细胞计数、细胞类型比例 | Results "Adnp is required for retinal growth" 节，Fig. 3-4 | 无法区分Adnp和Chd4的功能异同（预期影响） |
| 增殖/凋亡检测 | 确定视网膜生长缺陷的细胞机制 | 区分细胞增殖减少与细胞死亡增加 | 输入：P1视网膜切片；输出：Ki67+和activated caspase-3+细胞数 | Results 节，Fig. 5 | 无法确定Adnp敲除导致视网膜发育不良的机制（预期影响） |
| coIP-MS蛋白质组学 | 鉴定Adnp和Chd4的体内互作蛋白 | 确认ChAHP复合物存在并发现差异互作 | 输入：P0视网膜蛋白提取物；输出：互作蛋白列表 | Results 节，Fig. 2A-B | 无法确认ChAHP复合物在视网膜中的存在及Chd4-NuRD关联（预期影响） |
| scRNA-seq + Multi-seq | 比较Adnp和Chd4敲除后的转录组变化 | 鉴定共同与分化的基因表达程序 | 输入：P1视网膜单细胞；输出：聚类、差异表达基因 | Results 节，Fig. 6-7 | 无法评估Adnp和Chd4对基因调控的贡献（预期影响） |
| CUT&RUN-seq | 绘制Adnp、Chd4、Ctcf的基因组结合图谱 | 确定ChAHP复合物的靶基因及与Ctcf的关系 | 输入：P0视网膜细胞；输出：结合峰、共占据分析 | Results 节，Fig. 7C-D | 无法确定ChAHP的基因组靶点（预期影响） |
| 基因模块评分 | 评估Chd4差异可及性基因在Adnp cKO中的表达变化 | 检验Chd4靶基因是否受Adnp调控 | 输入：scRNA-seq表达矩阵+ATAC-seq基因列表；输出：模块评分 | Results 节，Fig. 7E | 无法区分ChAHP依赖与非依赖的Chd4靶基因（预期影响） |

## 09 关键公式符号

本文为描述性分子遗传学研究，未使用数学模型或形式化公式。核心分析为差异表达统计（Wilcoxon秩和检验）和聚类算法（Leiden算法），均为标准生信工具，无需要单独列出的公式。

## 10 实验设计与证据链

**数据集/群体**：
- 小鼠品系：C57BL/6J背景；Adnp flox（新构建）、Chd4 flox（Williams et al., 2004）、Chx10-Cre-GFP（Rowan and Cepko, 2004）
- 样本量：组织学分析n值未在摘要中明确；scRNA-seq为3个野生型 vs 3个Adnp cKO视网膜（P1），与3个对照 vs 3个Chd4 cKO视网膜（P1）整合
- 最终分析细胞数：9,580（Chd4数据集）+ 4,521（Adnp数据集）
- 指标：细胞计数、细胞类型比例、Ki67+细胞数、activated caspase-3+细胞数、差异表达基因数
- 仪器：Zeiss LSM900共聚焦显微镜、10X Genomics Chromium平台、Orbitrap Fusion Lumos质谱仪
- 评测协议：免疫荧光染色+人工计数；scRNA-seq经deMULTIplex去多重化、Scanpy质量控制、scVI批次校正、Leiden聚类

**实验表格**：

| 实验 | 检验的claim | 对比与条件 | 结果 | 支持的结论 | 不支持更强的结论 | 来源 |
|------|-------------|------------|------|-------------|-------------------|------|
| Adnp/Chd4免疫共定位 | ChAHP亚基在视网膜中共表达 | E11-P5各阶段免疫荧光 | 两蛋白在所有细胞类型中广泛共表达 | ChAHP复合物可能在视网膜中广泛存在 | 共表达不等于功能耦合 | Results 节，Fig. 1 |
| coIP-MS | Adnp和Chd4在体内形成复合物 | P0视网膜提取物，Adnp和Chd4抗体分别IP | Chd4是Adnp最丰富的互作蛋白；CBX3富集；Chd4互作组含NuRD亚基 | ChAHP复合物在视网膜中确实存在；Chd4同时与NuRD关联 | coIP不能区分直接/间接互作 | Results 节，Fig. 2 |
| Adnp cKO表型分析 | Adnp调控视网膜生长 | Adnp cKO vs WT，P21 | 视网膜明显减小，ONL和INL细胞数减少 | Adnp是视网膜生长所必需 | 不能确定是增殖还是存活缺陷 | Results 节，Fig. 3 |
| 增殖/凋亡检测 | Adnp调控祖细胞增殖或存活 | P1 Ki67和caspase-3染色 | Adnp cKO中Ki67+细胞减少、caspase-3+细胞增加 | Adnp同时影响祖细胞增殖和存活 | 因果关系未建立 | Results 节，Fig. 5 |
| scRNA-seq比较 | Adnp和Chd4敲除的转录组效应 | Adnp cKO vs Chd4 cKO vs 对照 | Adnp cKO仅42个DEGs，Chd4 cKO有540个DEGs；多数Adnp DEGs也在Chd4 cKO中差异 | Adnp和Chd4有共同靶基因，但Chd4有大量独立靶基因 | 差异可能部分来自批次效应 | Results 节，Fig. 7A-B |
| CUT&RUN-seq | Adnp和Chd4的基因组共定位 | P0视网膜，Adnp、Chd4、Ctcf抗体 | Adnp峰与Chd4和Ctcf峰大量重叠；~40% Adnp峰被Chd4和Ctcf共占 | ChAHP复合物在基因组上协同结合 | 共占据不等于功能依赖 | Results 节，Fig. 7C-D |
| 基因模块评分 | Chd4靶基因是否受Adnp调控 | 在Adnp cKO中评估Chd4差异可及性基因的表达 | 该模块在Adnp cKO中无明显变化 | Chd4的靶基因调控大部分不依赖Adnp | 模块评分可能掩盖基因特异性效应 | Results 节，Fig. 7E |

## 11 结论正确解读

- **任务范围**：本研究仅涉及视网膜发育（E11至P21），不涵盖其他脑区或成年期功能。
- **基因范围**：仅研究了Adnp和Chd4两个基因，未涉及ChAHP复合物中HP1亚基（Cbx1/3/5）的功能。
- **条件性敲除的时空限制**：Chx10-Cre从E11开始在视网膜祖细胞中表达，因此无法评估Adnp/Chd4在E11之前的视网膜发育（如视泡形成）中的功能。
- **Adnp cKO的残留表达**：Adnp蛋白在cKO中"strongly reduced"而非完全消失，不能排除残留蛋白的部分功能。
- **Chd4 cKO的复杂性**：Chd4同时是ChAHP和NuRD复合物的亚基，其敲除表型不能简单归因于任一复合物的功能丧失。
- **端脑与视网膜的比较**：本文结果与端脑研究（Clémot-Dupont et al., 2024）的差异提示ChAHP功能具有区域特异性，但直接跨脑区比较需谨慎，因为使用的Cre驱动子不同（Emx1-Cre vs Chx10-Cre）。
- **临床相关性**：虽然ADNP和CHD4突变与神经发育障碍相关，但本文的完全敲除模型不能直接模拟人类中的单倍剂量不足或显性负效突变。
- **有边界的复述**：在视网膜发育中，Adnp通过ChAHP复合物促进祖细胞增殖和存活以支持视网膜生长，而Chd4还通过NuRD复合物独立调控细胞命运决定；ChAHP复合物在视网膜中的功能主要限于生长调控，而非细胞类型规格决定。

## 12 作者自认局限

| 局限 | 具体表现 | 作者提出的未来方向 | 来源 |
|------|----------|---------------------|------|
| Adnp cKO中残留蛋白表达 | Adnp蛋白"strongly reduced"而非完全敲除 | 未明确提及 | Results "Conditional ablation" 节 |
| Chd4敲除的补偿效应 | Chd3/Chd5旁系同源物上调可能部分补偿Chd4功能 | 未明确提及 | Results 节，Fig. 6E |
| scRNA-seq批次效应 | Adnp和Chd4数据集分别处理，可能引入批次差异 | 使用scVI进行批次校正 | Methods "Multi-seq" 节 |
| 端脑与视网膜比较的局限性 | 不同Cre驱动子、不同发育时间窗 | 未明确提及 | Discussion 节 |
| 无法区分ChAHP依赖与非依赖功能 | Chd4敲除同时影响ChAHP和NuRD通路 | 未明确提及 | Discussion 节 |
| 未研究HP1亚基（Cbx1/3/5）功能 | ChAHP复合物包含三个HP1蛋白，本研究未涉及 | 未明确提及 | 全文 |

## 13 批判性分析

| [Analysis] 观察 | 潜在问题或替代解释 | 为何重要 | 如何检验 | 依据 |
|-----------------|---------------------|----------|----------|------|
| Adnp cKO中DEGs数量极少（42个） | 可能反映Adnp在视网膜中确实作用有限，但也可能是敲除效率不足或检测灵敏度限制 | 如果Adnp功能被低估，则"ChAHP主要调控生长"的结论可能不完整 | 验证Adnp敲除效率（蛋白/转录本水平）；增加生物学重复；使用不同的差异表达阈值 | Results 节，Fig. 7A |
| Chd4 cKO中Adnp蛋白下降50% | 可能是Chd4敲除后细胞组成改变（如特定细胞类型减少）的间接效应，而非复合物稳定性直接受影响 | 如果Adnp下降是细胞组成变化的反映，则"复合物完整性影响亚基稳定性"的解释不成立 | 在scRNA-seq数据中按细胞类型分层分析Adnp表达；进行时间序列分析 | Results "Conditional ablation" 节，Fig. S2 |
| CUT&RUN-seq显示Adnp和Chd4共占据Ctcf位点，但功能上Adnp敲除效应远弱于Chd4 | 可能Adnp在Ctcf位点的功能是辅助性的，或Adnp的主要功能在其他未检测的位点 | 这挑战了"ChAHP复合物作为一个整体发挥功能"的简单模型 | 比较Adnp和Chd4敲除后的染色质可及性变化（ATAC-seq）；进行Adnp和Chd4双敲除实验 | Results 节，Fig. 7C-D |
| 端脑与视网膜表型差异 | 可能反映ChAHP功能的区域特异性，但也可能是实验条件差异（Cre驱动子、遗传背景、分析时间点） | 如果差异来自实验条件而非生物学差异，则"区域特异性"结论不成立 | 在相同遗传背景下用相同Cre驱动子比较不同脑区；使用交叉设计 | Discussion 节 |
| 未检测Chd4 cKO中细胞类型比例变化的具体机制 | 作者观察到细胞类型失衡，但未深入探讨是命运转换还是选择性死亡 | 区分这两种机制对理解Chd4在命运决定中的角色至关重要 | 谱系追踪实验；凋亡抑制实验 | Results 节，Fig. 4-5 |

## 14 学到什么

> **Agent 提炼的知识候选**

1. **条件性敲除比较策略**：在同一个发育系统（视网膜）中，用相同的Cre驱动子分别敲除同一复合物的不同亚基，通过表型比较区分复合物整体功能与亚基独立功能。这是解析多亚基复合物功能组织的有效范式，可迁移到cpdch基因家族其他成员（如Chd3、Chd5）的功能研究。
2. **多组学交叉验证**：将表型分析（组织学）、转录组（scRNA-seq）、基因组结合（CUT&RUN-seq）和蛋白质互作（coIP-MS）四种维度结合，从不同层面验证同一结论。对于cpdch基因家族研究，可借鉴此策略系统比较不同家族成员的功能。
3. **基因注释陷阱**：Adnp的readthrough转录本（与Dpm1融合）导致表达数据中Adnp信号缺失，这是一个重要的技术警示。在研究cpdch基因家族时，需检查是否存在类似的基因注释问题（如反义转录本、readthrough转录本、假基因干扰）。
4. **补偿效应的考虑**：Chd4敲除后Chd3/Chd5上调，提示cpdch基因家族成员间可能存在功能补偿。在设计敲除实验时，需同时检测其他家族成员的表达变化。
5. **Ctcf在ChAHP功能中的潜在角色**：Adnp和Chd4在Ctcf位点共占据，且Chd4敲除后Ctcf占据增加，提示ChAHP可能通过调控Ctcf结合来影响染色质结构。这为cpdch基因家族与绝缘子功能的关系提供了新线索。
6. **区域特异性功能**：同一复合物在不同脑区（端脑vs视网膜）的功能权重不同，提示研究cpdch基因家族时需考虑组织特异性，不能简单跨组织外推。
7. **scRNA-seq聚类作为表型读出**：作者通过聚类分析发现cKO细胞进入"新型"聚类，提示转录组状态偏移可作为表型变化的敏感指标，即使传统组织学未显示明显差异。

## 15 与已有知识连接

- **ChAHP复合物的原始发现**：Ostapcuk et al. (2018) 首次描述ChAHP复合物（Chd4-Adnp-HP1）在胚胎干细胞中的功能。本文将其扩展到体内视网膜发育，并发现与体外研究部分不一致的结果（体外认为ChAHP主要调控基因沉默，本文发现其调控生长而非命运）。
- **Chd4/NuRD在神经发育中的已知功能**：Nitarska et al. (2016) 在端脑中的研究；本文与之对比，发现视网膜中Chd4的功能更依赖NuRD而非ChAHP。
- **Adnp在皮层发育中的功能**：Clémot-Dupont et al. (2024) 的端脑研究显示Adnp和Chd4表型相似；本文的视网膜研究显示两者分化，形成互补图景。
- **Ctcf与染色质绝缘子的关系**：Ctcf是已知的染色质绝缘子蛋白，本文发现Adnp/Chd4在Ctcf位点共占据，与Kaaij et al. (2019) 在胚胎干细胞中的发现一致，提示这一机制可能具有普遍性。
- **视网膜发育的时序调控**：与视网膜发育中已知的转录因子网络（如Pax6、Otx2等）连接，本文使用的细胞类型标记物与领域标准一致。
- **cpdch基因家族（Chd3/4/5）的补偿机制**：本文观察到Chd4敲除后Chd3/Chd5上调，与文献中关于CHD家族成员功能冗余的报道一致。
- **[Analysis] 候选方向**：本文结果提示，cpdch基因家族成员在不同组织中的功能分工可能取决于其与不同互作复合物（ChAHP vs NuRD）的组装偏好。这为研究cpdch基因家族的组织特异性功能提供了新框架。

## 16 研究想法

> **Agent 生成的研究候选**

**候选1：cpdch基因家族成员在视网膜发育中的功能冗余与分工**
- **来源局限/观察**：本文仅研究了Chd4，但观察到Chd3/Chd5在Chd4敲除后上调，提示补偿机制。
- **核心假设**：Chd3和Chd5在视网膜发育中部分补偿Chd4的功能，且三者可能通过不同的复合物（ChAHP vs NuRD）发挥差异化功能。
- **初步方法**：构建Chd3/Chd5条件性敲除或敲低模型，与Chd4 cKO进行单/双/三敲除比较；利用scRNA-seq和CUT&RUN-seq分析补偿性转录和染色质变化。
- **验证方式**：比较单敲与多敲的表型严重程度；检测Chd3/5是否也能与Adnp形成复合物。
- **创新状态**：unverified

**候选2：Adnp-Chd4-Ctcf轴在视网膜祖细胞增殖调控中的机制**
- **来源局限/观察**：本文发现Adnp和Chd4在Ctcf位点共占据，且Adnp cKO中增殖减少。
- **核心假设**：Adnp-Chd4通过调控Ctcf介导的染色质环状结构，控制特定增殖相关基因（如细胞周期调节因子）的表达。
- **初步方法**：在Adnp cKO中进行Hi-C或HiChIP分析Ctcf介导的染色质互作变化；结合CUT&RUN-seq数据鉴定Adnp-Chd4-Ctcf共占据的启动子-增强子对。
- **验证方式**：CRISPR干扰特定Ctcf位点，检测是否模拟Adnp cKO的增殖缺陷。
- **创新状态**：unverified

**候选3：ChAHP复合物在不同脑区（端脑vs视网膜）的功能差异机制**
- **来源局限/观察**：本文与Clémot-Dupont et al. (2024) 的端脑研究结果不同——端脑中Adnp和Chd4表型相似，视网膜中分化。
- **核心假设**：不同脑区中ChAHP与NuRD复合物的组装比例不同，导致Chd4功能权重差异。
- **初步方法**：在不同脑区（端脑、视网膜、小脑）进行定量蛋白质组学或免疫沉淀定量比较ChAHP vs NuRD复合物的丰度；比较Adnp和Chd4的结合位点在不同脑区的差异。
- **验证方式**：在视网膜中过表达Adnp，观察是否使Chd4表型向"ChAHP依赖"方向转变。
- **创新状态**：unverified

**候选4：Adnp readthrough转录本（Adnp-Dpm1）的功能意义**
- **来源局限/观察**：本文发现Adnp外显子与Dpm1形成readthrough转录本（NR_132310），导致表达数据中Adnp信号缺失。
- **核心假设**：该readthrough转录本可能具有独立的调控功能（如作为lncRNA调控Adnp表达），或影响Adnp mRNA的稳定性/翻译效率。
- **初步方法**：在不同发育阶段和细胞类型中定量readthrough转录本与正常Adnp转录本的比例；利用CRISPR破坏readthrough转录本特异性外显子，观察Adnp表达和视网膜发育的变化。
- **验证方式**：RNA-FISH或长读长测序确认readthrough转录本的存在和亚细胞定位。
- **创新状态**：unverified

**候选5：ChAHP复合物在视网膜祖细胞时间序列命运决定中的动态作用**
- **来源局限/观察**：本文发现Adnp cKO中细胞类型比例不变但总数减少，而Chd4 cKO中细胞类型比例改变。
- **核心假设**：ChAHP复合物在视网膜发育早期（E11-E15）主要调控祖细胞扩增，而NuRD在晚期调控命运选择；两者在时间上的动态平衡决定最终细胞组成。
- **初步方法**：利用诱导型Cre（如CAGG-CreER）在不同时间点敲除Adnp或Chd4，比较早期vs晚期敲除的表型差异；结合单细胞RNA速度分析推断命运转换轨迹。
- **验证方式**：在Chd4 cKO中同时敲除Adnp，观察是否恢复细胞类型平衡（遗传上位性分析）。
- **创新状态**：unverified