## Review setup

- **Input scope** 预印本全文（含摘要、引言、结果、讨论、局限性、方法、补充信息说明）
- **Assessment boundary** 仅基于提供的稿件文本进行评估；未提供图、表、补充数据文件或原始数据
- **Shared manuscript claim summary** 作者提出，肌纤维特异性敲除 Ctcf 的小鼠在出生时无明显表型，但成年后自发发展为严重肌病；整合 snRNA-seq、ATAC-seq、pc-HiC 和 CTCF ChIP-seq 数据，作者认为 CTCF 缺失导致染色质可及性下降、启动子-增强子互作改变，进而引起肌纤维身份丢失、内质网应激/UPR 激活和炎症基因异位表达
- **Visible evidence base** 文本中引用了图 S1-S13 和表 1-2，但未提供任何实际数据、图或表
- **Missing materials affecting confidence** 所有图、表、补充数据、统计分析细节、原始数据均缺失；无法验证任何定量结论或统计显著性声明

## Reviewer

- **Overall assessment** 该研究提出一个有趣且具有潜在重要性的问题：CTCF 介导的 3D 基因组结构在终末分化、有丝分裂后肌纤维中的长期维持作用。作者建立了一个肌纤维特异性 Ctcf 敲除小鼠模型，并观察到自发肌病表型，这本身是有价值的资源。然而，从提供的文本来看，核心结论的支撑证据链存在明显缺口。主要问题包括：表型表征的深度不足、多组学数据整合的逻辑不够清晰、因果关系推断缺乏直接功能验证、以及关键实验（如恢复实验或时间序列分析）的缺失。此外，作者声称 CTCF 缺失导致"病理性基因组重编程"，但提供的证据主要显示相关性而非因果性。该研究有潜力，但目前从提供的材料来看，核心结论尚未被充分确立。

- **Who would be interested in the results, and why** 该研究对以下群体具有潜在吸引力：(1) 染色质结构和 3D 基因组领域的研究者，特别是关注 CTCF 在终末分化细胞中作用的人；(2) 肌肉生物学和肌病研究者，尤其是关注肌纤维身份维持和肌病发病机制的人；(3) 表观遗传学与衰老/退行性疾病交叉领域的研究者。如果 CTCF 在肌纤维中的功能得到充分验证，这可能为理解特发性肌病提供一个新框架。

- **Major strengths** 1) 研究问题具有新颖性和重要性，关注有丝分裂后多核细胞中 3D 基因组结构的长期维持，这是一个未被充分探索的领域；2) 使用了多种互补的组学方法（snRNA-seq、ATAC-seq、pc-HiC、ChIP-seq），体现了技术的全面性；3) 构建了组成性和诱导性两种 Ctcf 敲除模型，有助于区分发育和成年期的作用；4) 观察到自发肌病表型，包括肌纤维萎缩、神经肌肉接头破坏和免疫细胞浸润，具有潜在的转化意义。

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** 表型表征与因果推断
- **Claim pointer** 作者声称 Ctcf 缺失"自发导致严重肌病"，且肌纤维萎缩是 CTCF 缺失的直接后果
- **Evidence pointer** 图 1-2；"location not provided"
- **Concern** 从文本描述来看，肌病表型的表征主要基于组织学和功能学指标（肌肉重量、肌纤维横截面积、握力/悬挂时间、强直收缩力），但缺乏对肌病发病机制的深入分析。关键问题是：肌纤维萎缩是 CTCF 缺失的细胞自主效应，还是继发于神经肌肉接头破坏、免疫细胞浸润或其他非细胞自主机制？作者在结果部分提到 NMJ 形态学破坏和免疫细胞浸润，但没有提供证据区分这些事件的时序关系和因果关系。此外，作者没有提供任何遗传或药理学干预实验来证明 CTCF 缺失与肌病表型之间的因果关系。
- **Why it matters** 如果肌病表型主要是非细胞自主效应（如免疫介导或神经源性），那么"CTCF 在肌纤维中维持基因组完整性"这一核心结论将被削弱。区分细胞自主与非细胞自主效应是建立机制模型的基础。
- **Resolution test** 需要提供：(1) 条件性敲除的时间序列分析，明确肌纤维萎缩、NMJ 破坏和免疫浸润的先后顺序；(2) 在免疫缺陷小鼠或骨髓嵌合体中评估肌病表型，排除免疫细胞浸润的贡献；(3) 在体外培养的肌管中验证 CTCF 缺失的细胞自主效应；(4) 通过回补实验（如 AAV 介导的 CTCF 表达）验证表型可逆性。

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** 多组学数据整合与因果推断
- **Claim pointer** 作者声称 CTCF 缺失导致"病理性基因组重编程"，且染色质可及性下降和启动子-增强子互作改变是基因表达变化的直接原因
- **Evidence pointer** 图 3-5、图 S9-S13；"location not provided"
- **Concern** 作者整合了 snRNA-seq、ATAC-seq、pc-HiC 和 CTCF ChIP-seq 数据，但文本中缺乏对这些数据整合的定量描述。关键问题包括：(1) 差异表达基因、差异可及性区域和差异染色质互作之间的重叠程度如何？是否有统计显著性？(2) 作者如何区分 CTCF 缺失的直接效应（CTCF 结合位点附近的变化）和间接效应（下游转录因子变化导致的变化）？(3) 图 5d-g 中展示的"多层染色质破坏"分类是基于什么标准？这些类别是否有功能验证？(4) 作者提到"部分恢复"的染色质可及性，但未解释这一现象的机制。此外，作者在结果部分提到 CTCF 结合位点富集于"下调基因的启动子"，但未提供具体的富集倍数和统计显著性。
- **Why it matters** 该研究的核心创新点在于将 3D 基因组变化与肌病表型联系起来。如果数据整合分析不能清晰地区分直接和间接效应，或者不能证明染色质变化先于基因表达变化，那么"基因组重编程驱动肌病"的结论就缺乏支撑。
- **Resolution test** 需要提供：(1) 差异表达基因与 CTCF 结合位点的重叠分析（包括超几何检验的 p 值）；(2) 利用 ChIP-seq 数据区分 CTCF 直接靶基因和间接靶基因；(3) 时间序列 ATAC-seq 或 RNA-seq 数据，证明染色质变化先于转录变化；(4) 对关键候选基因进行 CRISPR 或转基因验证。

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** Yes
- **Axis** 统计严谨性与实验重复
- **Claim pointer** 作者声称 snRNA-seq 显示"几乎完全丧失 IIB 型肌核"以及"免疫细胞大量浸润"
- **Evidence pointer** 图 4a-b、图 6a-b；"location not provided"
- **Concern** 文本中未提供任何关于生物学重复数量、统计检验方法、效应量或置信区间的信息。snRNA-seq 的细胞类型注释和比例变化是否有统计显著性？免疫细胞浸润的定量分析是基于什么指标？此外，作者提到"约 50% 的肌核"为"其他肌核"，这一比例是如何计算的？是否有技术重复或独立生物学重复的验证？对于单细胞数据，批次效应是如何处理的？
- **Why it matters** 该研究的结论依赖于对细胞类型组成变化的准确量化。如果统计基础不牢固，所有下游分析（包括轨迹推断和差异表达）都可能受到影响。
- **Resolution test** 需要提供：(1) 每个时间点和基因型的生物学重复数量；(2) 细胞类型比例的统计检验结果（如 DESeq2 或类似方法）；(3) 免疫细胞浸润的定量方法（如流式细胞术或免疫组化定量）；(4) 批次效应处理的详细说明。

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** 与人类疾病的关联
- **Claim pointer** 作者在讨论中暗示 CTCF 缺陷可能与人类特发性肌病相关
- **Evidence pointer** 讨论部分；"location not provided"
- **Concern** 作者在讨论中提出 CTCF 缺陷可能与人类肌病相关的假说，但未提供任何人类遗传学或临床数据支持。是否有特发性肌病患者中存在 CTCF 突变或表达降低的证据？如果有，这些变异是体细胞还是种系？此外，作者提到"CTCF 单倍剂量不足"与人类发育障碍相关，但未讨论这些患者是否表现肌病表型。
- **Why it matters** 如果该研究要提出临床相关性，需要至少提供初步的人类数据或文献支持。否则，这一声明应被明确标记为推测性。
- **Resolution test** 需要提供：(1) 人类肌病数据库中 CTCF 变异的分析；(2) 或至少引用已发表的 CTCF 相关疾病中肌病表型的证据；(3) 或将讨论中的相关声明明确标记为假说。

- **Concern ID** R1-M5
- **Severity** Major
- **Blocking** No
- **Axis** 机制深度
- **Claim pointer** 作者声称 CTCF 缺失导致"肌纤维身份丧失"和"病理性重编程"
- **Evidence pointer** 图 4-5、图 S9-S13；"location not provided"
- **Concern** 作者将"身份丧失"定义为肌纤维类型标志物表达下降和"其他肌核"的出现，但未提供这些"其他肌核"的分子特征。它们是否表达其他谱系的标志物（如平滑肌、间充质或神经元标志物）？还是仅仅表现为成熟标志物缺失？此外，作者提到"异位表达炎症基因"，但未讨论这些基因是否直接受 CTCF 调控，还是通过其他转录因子间接激活。轨迹分析显示 IIB 型肌核向"其他肌核"转变，但这一推断的稳健性如何？是否进行了轨迹分析的交叉验证？
- **Why it matters** "身份丧失"和"重编程"是强声明，需要明确的分子证据支持。如果"其他肌核"只是成熟标志物缺失的萎缩肌核，那么"重编程"的说法可能过于强烈。
- **Resolution test** 需要提供：(1) "其他肌核"的差异表达基因列表和功能富集分析；(2) 与已知细胞谱系标志物的交叉比对；(3) 轨迹分析的稳健性检验（如不同算法或参数设置）。

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** 方法透明度
- **Affected element** 图 S1a 中 Ctcf 敲除策略的验证
- **Evidence pointer** 图 S1a-c；"location not provided"
- **Concern** 文本提到"高效重组"和"CTCF 蛋白大幅减少"，但未提供定量数据（如 Western blot 的灰度定量或 qPCR 的敲除效率百分比）。
- **Required correction** 请提供敲除效率的定量数据（如 Western blot 定量或 qPCR 数据），并说明用于验证敲除的抗体和引物信息。

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** 数据呈现
- **Affected element** 图 5d-g 中"多层染色质破坏"的分类
- **Evidence pointer** 图 5d-g；"location not provided"
- **Concern** 文本中描述了多种染色质变化类别，但未提供这些类别的具体定义和判定标准。
- **Required correction** 请在方法部分或图例中明确每个类别的定义和判定阈值。

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** 文献引用
- **Affected element** 引言中关于 CTCF 在骨骼肌中作用的描述
- **Evidence pointer** 引言部分；"location not provided"
- **Concern** 引言提到"CTCF 在肌生成中的调控作用已有报道"，但未具体引用这些研究。此外，关于 CTCF 在成体组织中的维持作用，引用文献较少。
- **Required correction** 请补充相关文献引用，特别是关于 CTCF 在骨骼肌发育和成体维持中的已有研究。

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** 术语使用
- **Affected element** "病理性基因组重编程"和"身份丧失"
- **Evidence pointer** 摘要和讨论；"location not provided"
- **Concern** 这些术语在文中未明确定义，可能引起读者误解。
- **Required correction** 请在引言或结果部分明确定义这些术语的操作性标准。

- **Concern ID** R1-m5
- **Severity** Minor
- **Axis** 数据可用性
- **Affected element** 数据共享声明
- **Evidence pointer** 方法部分；"location not provided"
- **Concern** 未提供数据可用性声明或 GEO 登录号。
- **Required correction** 请提供所有组学数据的 GEO 登录号或说明数据在审稿期间可获取的途径。

- **Concern ID** R1-m6
- **Severity** Minor
- **Axis** 实验细节
- **Affected element** 小鼠模型
- **Evidence pointer** 方法部分；"location not provided"
- **Concern** 未说明 Ctcf 敲除小鼠的性别、年龄匹配情况，以及用于实验的小鼠数量。
- **Required correction** 请在方法部分补充动物实验的详细设计，包括性别、年龄、样本量和随机化/盲法信息。

- **Concern ID** R1-m7
- **Severity** Minor
- **Axis** 结果呈现
- **Affected element** 图 S13 中 Myh4 位点的代表性展示
- **Evidence pointer** 图 S13；"location not provided"
- **Concern** 仅展示了一个基因位点作为代表性例子，缺乏对其他关键位点的验证。
- **Required correction** 请考虑增加至少一个额外的代表性位点，或提供所有关键位点的汇总统计。

- **Concern ID** R1-m8
- **Severity** Minor
- **Axis** 讨论深度
- **Affected element** 讨论中关于 CTCF 独立于 3D 基因组功能的讨论
- **Evidence pointer** 讨论部分；"location not provided"
- **Concern** 作者未讨论 CTCF 可能通过不依赖 3D 基因组结构的方式（如直接调控转录延伸或 RNA 加工）影响基因表达的可能性。
- **Required correction** 请在讨论中增加对 CTCF 非经典功能的考虑，或明确说明为何这些功能在本文背景下不相关。

## Risk / unsupported claims

1. **"CTCF 缺失导致病理性基因组重编程"**：从提供的文本来看，作者展示了染色质可及性和互作的变化，但未提供直接证据证明这些变化是"重编程"而非单纯的染色质塌缩或降解。该声明需要更严格的分子证据支持。

2. **"CTCF 缺失导致肌纤维身份丧失"**：作者将 IIB 型肌核减少和"其他肌核"出现解释为身份丧失，但未提供这些"其他肌核"的分子特征。它们可能只是萎缩或退化的肌核，而非真正"重编程"为其他身份。

3. **"CTCF 缺失与人类肌病相关"**：讨论中暗示的临床相关性缺乏任何人类数据支持，应明确标记为推测。

4. **"CTCF 缺失导致炎症基因异位表达"**：作者提到 IIB 型肌核中炎症基因上调，但未讨论这些基因是否直接受 CTCF 调控，还是通过其他转录因子间接激活。此外，炎症基因表达是否导致免疫细胞浸润的因果关系未被证明。

5. **"CTCF 缺失导致 NMJ 破坏"**：作者观察到 NMJ 形态学变化，但未提供机制解释。NMJ 破坏可能是肌纤维萎缩的继发效应，而非 CTCF 缺失的直接后果。

6. **"CTCF 对肌纤维转录适应至关重要"**：作者在摘要和讨论中声称 CTCF 对肌纤维的转录适应至关重要，但未提供任何功能性实验（如运动刺激、去神经支配或代谢挑战）来测试这一假说。

7. **"CTCF 缺失导致 ER 应激/UPR 持续激活"**：作者展示了 UPR 标志物上调，但未提供证据证明这是 CTCF 缺失的直接后果，而非肌病的一般特征。

8. **"CTCF 在肌纤维中维持 3D 基因组完整性"**：作者展示了 CTCF 缺失后染色质互作的变化，但未提供证据证明这些变化是"完整性丧失"而非适应性重排。