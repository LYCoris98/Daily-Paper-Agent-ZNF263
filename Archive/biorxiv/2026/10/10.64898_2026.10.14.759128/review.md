## Review setup

- **Input scope** Abstract only
- **Assessment boundary** Claims and evidence as presented in the abstract; no figures, methods, or supplementary materials were provided for evaluation
- **Shared manuscript claim summary** The authors report that alcohol exposure displaces elongating RNAPIIs2p from gene bodies to promoters and to guanine-rich intergenic CTCF sites. They further claim that high guanine content at the CTCF motif ZF5 binding position predicts increased CTCF and cohesin (RAD21) occupancy, that these changes persist six days after alcohol withdrawal, that Hi-C reveals no impact on structural CTCF loops but altered enhancer-promoter contacts with lasting gene expression changes, and that the same sequence rule applies in a mouse starvation model and in placentae after paternal alcohol exposure.
- **Visible evidence base** Abstract text only; no figures, tables, methods, or statistical details provided
- **Missing materials affecting confidence** All primary data, experimental methods, statistical analyses, genome-wide datasets, and validation details; the abstract references findings across multiple model systems without any supporting data visible

## Reviewer

- **Overall assessment** The abstract presents a potentially interesting hypothesis-driven study linking sequence-specific guanine content in CTCF motifs to alcohol-induced chromatin redistribution. The central idea, that acetaldehyde's guanine-directed chemistry produces sequence-dependent rather than stochastic chromatin changes, is mechanistically plausible and conceptually appealing. However, the abstract compresses a large amount of work across multiple model systems into a very small space, and the absence of any supporting data makes it impossible to evaluate the robustness of the claims. The persistence claim (six days post-withdrawal) and the cross-model generalizability claims are particularly strong and would require substantial evidence. The disconnect between CTCF/cohesin changes and structural loop stability, with effects instead on enhancer-promoter contacts, is an interesting and somewhat counterintuitive finding that would benefit from clearer mechanistic explanation.

- **Who would be interested in the results, and why** Researchers studying alcohol's molecular effects on chromatin and gene expression; investigators in the CTCF/cohesin and 3D genome organization field; those interested in sequence-dependent mechanisms of environmentally induced epigenetic changes; and potentially researchers studying transgenerational effects of alcohol exposure, given the paternal exposure finding.

- **Major strengths** The hypothesis is mechanistically grounded in acetaldehyde's known guanine-directed chemistry, providing a clear sequence-dependence rationale. The study spans multiple levels of analysis, from transcription factor occupancy to 3D genome organization to gene expression, and extends beyond a single cell-line model to two in vivo contexts. The persistence finding, if well-supported, would have significant implications for understanding lasting effects of alcohol exposure.

- **Major Concerns**

  - **Concern ID** R1-M1
  - **Severity** Major
  - **Blocking** Yes
  - **Axis** Evidence sufficiency
  - **Claim pointer** "CTCF occupancy changes persisting even six days after alcohol withdrawal"
  - **Evidence pointer** Abstract; location not provided
  - **Concern** The abstract claims that CTCF occupancy changes persist for six days after alcohol withdrawal, which is a strong temporal claim. No information is provided about the experimental design supporting this, including the time course sampled, the number of biological replicates, the magnitude of the persistent changes relative to acute changes, or whether this persistence is specific to certain loci.
  - **Why it matters** This persistence claim is central to the paper's significance, as it suggests lasting molecular consequences of alcohol exposure. If the effect decays substantially over the six-day period or is only significant at a subset of loci, the interpretation would change considerably. The claim also implies a mechanism for maintaining altered occupancy after the initial insult is removed, which is not addressed.
  - **Resolution test** Provide the full time-course data showing CTCF occupancy at multiple time points post-withdrawal, with statistical comparisons at each time point, and demonstrate that the persistence is robust across replicates and not driven by a small number of outlier loci.

  - **Concern ID** R1-M2
  - **Severity** Major
  - **Blocking** Yes
  - **Axis** Evidence sufficiency
  - **Claim pointer** "the same sequence rule accounts for altered CTCF occupancy in a mouse starvation (metabolic stress) model and in the placentae after paternal alcohol exposure"
  - **Evidence pointer** Abstract; location not provided
  - **Concern** The abstract extends the central finding to two additional in vivo models, a mouse starvation model and paternal alcohol exposure with placental analysis. These are substantial claims that imply the sequence rule is generalizable across different stressors and across generations. No details are provided about the experimental design, sample sizes, the magnitude of effects, or how "the same sequence rule" was tested in these contexts.
  - **Why it matters** These cross-model claims significantly broaden the paper's scope and implications. If the rule applies across different stressors and in a transgenerational context, this would suggest a general principle of sequence-dependent chromatin vulnerability. However, the abstract provides no evidence that these models were tested with equivalent rigor, and the paternal exposure finding in particular raises complex questions about mechanism that are not addressed.
  - **Resolution test** Provide detailed methods and results for each model system, including sample sizes, statistical power, effect sizes, and explicit demonstration that the guanine-content rule predicts occupancy changes in each context. For the paternal exposure model, provide evidence for the mechanism by which the effect is transmitted.

  - **Concern ID** R1-M3
  - **Severity** Major
  - **Blocking** Yes
  - **Axis** Interpretive clarity
  - **Claim pointer** "using Hi-C, we found that these changes to CTCF and cohesin do not impact the pronounced structural CTCF loops, but are instead primarily associated with altered guanine-rich enhancer-promoter contacts that connect to lasting changes to gene expression"
  - **Evidence pointer** Abstract; location not provided
  - **Concern** The abstract reports a dissociation between CTCF/cohesin occupancy changes and structural loop stability, with effects instead on enhancer-promoter contacts. This is a surprising finding that challenges simple models of CTCF function in loop maintenance. The abstract does not explain how CTCF and cohesin occupancy can change substantially without affecting loops, nor how enhancer-promoter contacts are altered independently.
  - **Why it matters** This is arguably the most mechanistically interesting and potentially controversial finding in the paper. If CTCF occupancy changes do not affect structural loops, the field's understanding of CTCF's role in loop maintenance would need revision, or the authors need to provide an alternative explanation for why loops are stable despite occupancy changes. The mechanism linking altered enhancer-promoter contacts to lasting gene expression changes is also unclear.
  - **Resolution test** Provide Hi-C data showing loop stability despite occupancy changes, with appropriate controls and statistical power to detect loop changes if they existed. Provide a mechanistic model, supported by data, for how enhancer-promoter contacts are altered and how these connect to gene expression changes.

  - **Concern ID** R1-M4
  - **Severity** Major
  - **Blocking** No
  - **Axis** Scope and generalizability
  - **Claim pointer** "the same sequence rule accounts for altered CTCF occupancy in a mouse starvation (metabolic stress) model"
  - **Evidence pointer** Abstract; location not provided
  - **Concern** The abstract extends the findings to a starvation model, which is described as "metabolic stress." The connection between alcohol exposure and starvation as comparable stressors is not explained. It is unclear whether the authors are claiming that any metabolic stress produces the same sequence-directed changes, or whether there is a specific shared mechanism.
  - **Why it matters** The generalizability claim is important for the paper's broader significance. If the rule applies to diverse stressors, it suggests a general principle. However, the abstract does not articulate what the shared mechanism might be, leaving the reader to wonder whether this is a meaningful parallel or an opportunistic comparison.
  - **Resolution test** Clarify the rationale for including the starvation model and provide evidence for a shared mechanism, or alternatively frame the starvation data as supporting the generality of the sequence rule without implying a common pathway.

- **Minor Comments**

  - **Concern ID** R1-m1
  - **Severity** Minor
  - **Axis** Clarity
  - **Affected element** Terminology
  - **Evidence pointer** Abstract, first sentence of results description
  - **Issue** The abstract states that RNAPIIs2p "relocates to promoters" after alcohol exposure, but it is unclear whether this means a net increase in promoter-proximal paused polymerase, a redistribution from gene bodies, or both. The term "relocates" implies movement, but the data may only show changes in steady-state occupancy.
  - **Required correction** Clarify whether the promoter increase represents a true redistribution or a change in occupancy that could reflect altered initiation, pausing, or degradation kinetics.

  - **Concern ID** R1-m2
  - **Severity** Minor
  - **Axis** Completeness
  - **Affected element** Model system description
  - **Evidence pointer** Abstract; location not provided
  - **Issue** The abstract refers to "our cell-line model" without specifying the cell type. Given that the findings are extended to mouse models, the choice of human cell line is relevant for interpreting the cross-species claims.
  - **Required Correction** Specify the cell line used and briefly justify its relevance to alcohol research.

  - **Concern ID** R1-m3
  - **Severity** Minor
  - **Axis** Interpretive clarity
  - **Affected element** Mechanistic framing
  - **Evidence pointer** Abstract, guanine content claim
  - **Issue** The abstract states that "high guanine content at the CTCF motifs zinc finger 5 (ZF5) binding position showed the largest increase in both CTCF and cohesin." It is unclear whether the guanine content at ZF5 is the sole predictor or one of several sequence features examined, and whether the effect is specific to ZF5 or reflects overall motif guanine content.
  - **Required Correction** Clarify whether ZF5 guanine content was identified as the strongest predictor among multiple sequence features tested, and whether the effect is specific to this position or correlated with overall motif composition.

- **Technical failings that need to be addressed before the case is established** R1-M1 (persistence claim requires full time-course data), R1-M2 (cross-model generalizability requires detailed evidence from each system), R1-M3 (dissociation between occupancy and loop stability requires direct demonstration with adequate statistical power)

- **Assessment against Nature-style criteria** 
  - Originality: The sequence-dependent framing based on acetaldehyde's guanine chemistry is a novel angle on alcohol's chromatin effects. The finding that CTCF occupancy changes do not affect structural loops is potentially original and counterintuitive.
  - Scientific importance: If fully supported, the findings would establish a sequence-level rule for alcohol-induced chromatin changes with potential relevance to understanding lasting effects of alcohol exposure. The transgenerational claim, if substantiated, would be of high importance.
  - Interdisciplinary readership: The work bridges alcohol research, chromatin biology, and 3D genome organization, which could attract readers from multiple communities. However, the abstract assumes familiarity with CTCF, cohesin, and Hi-C that may limit accessibility.
  - Technical soundness: Cannot be assessed from the abstract alone. The claims span multiple techniques (ChIP, Hi-C, RNA-seq) and model systems, each requiring rigorous validation.
  - Readability for nonspecialists: The abstract is dense and assumes significant background knowledge. The logic is clear but the terminology is specialized.

- **Recommendation posture** Currently not established from the provided evidence. The abstract presents an interesting hypothesis and a broad set of claims, but the absence of any supporting data makes it impossible to assess whether the conclusions are warranted. The persistence and cross-model generalizability claims are particularly strong and would require substantial evidence. A full manuscript with complete methods, figures, and statistical analyses would be needed to evaluate the work properly.