## Review setup
- **Input scope** Full manuscript (including Abstract, Introduction, Results, Discussion, Methods, and Supplementary Information)
- **Assessment boundary** Scientific content, experimental design, data analysis, and interpretation as presented in the provided text
- **Shared manuscript claim summary** The authors report that allele-specific chromatin architecture is a common feature of imprinted domains in the mouse brain, shaped by methylation-sensitive CTCF binding at imprinting control regions. They identify a distal enhancer (E105) at the Mest-Copg2 domain that engages different promoters on each parental allele, and show that Copg2 imprinted expression in neurons is regulated by both enhancer-mediated activation on the maternal allele and antisense transcription (MestXL)-mediated repression on the paternal allele.
- **Visible evidence base** Capture Hi-C, CUT&Tag, ATAC-seq, RNA-seq, CRISPRi screen, ASO knockdown, RT-ddPCR, FISH, DNMTi treatment, ChromHMM analysis
- **Missing materials affecting confidence** Supplementary Figures 1–14 and Supplementary Tables 1–2 are referenced but not provided for review. Source data files are not provided. Code repository URL is given but not accessible in this format.

## Reviewer
- **Overall assessment** This manuscript presents a comprehensive and technically rigorous analysis of allele-specific chromatin architecture at imprinted domains in the mouse brain. The study is well-motivated, the experimental design is thoughtful, and the findings are largely supported by the data presented. The identification of a distal enhancer (E105) that exhibits allele-specific promoter engagement and the integration of enhancer activity with antisense transcription at the Mest-Copg2 domain represent significant advances. However, several concerns regarding the specificity of perturbations, the strength of causal claims, and the generalizability of the model require attention.
- **Who would be interested in the results, and why** Researchers in genomic imprinting, 3D genome organization, gene regulation, and neuroepigenetics will find this work of high interest. The systematic analysis of allele-specific chromatin architecture across multiple imprinted domains and the functional dissection of the Mest-Copg2 regulatory logic provide mechanistic insights that extend beyond individual loci.
- **Major strengths** 1. Systematic and high-resolution allele-specific chromatin contact mapping across eight imprinted domains, with reciprocal crosses to control for strain effects. 2. Integration of multiple orthogonal approaches (Capture Hi-C, CUT&Tag, ATAC-seq, CRISPRi, ASO, FISH) to build a coherent mechanistic model. 3. Functional identification of a distal enhancer (E105) through a CRISPRi screen, with validation by Cas9-mediated deletion and in vivo AAV delivery. 4. Clear demonstration that the enhancer engages different promoters on the two parental alleles, providing a structural basis for allele-specific regulation. 5. Elegant dissection of the dual regulatory logic (enhancer activation + antisense repression) at the Mest-Copg2 domain.
- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** No
- **Axis** Causal inference / perturbation specificity
- **Claim pointer** "Mest/MestXL then contributes to repression of paternal Copg2, likely through transcriptional interference, although a direct repressive role of the RNA cannot be excluded."
- **Evidence pointer** Figure 6e, f; Results section "Copg2 is regulated by both a distal enhancer and MestXL transcription"
- **Concern** The ASO targeting the MestXL extended 3' UTR reduces MestXL by >93% but also reduces total Mest RNA by ~50%. The authors acknowledge this and refer to the perturbation as "Mest/MestXL knockdown." However, the claim that MestXL specifically represses paternal Copg2 is weakened by the inability to separate the effects of MestXL from those of canonical Mest. The ASO may also affect other Mest isoforms or have off-target effects. The FISH data showing MestXL localization at the Copg2 transcription site is suggestive but does not establish a causal or mechanistic link.
- **Why it matters** The central model of the paper posits that MestXL is the specific repressive agent on the paternal allele. If the observed effects are due to loss of canonical Mest or other isoforms, the model would need substantial revision. The distinction between transcriptional interference by the act of transcription versus a repressive function of the RNA product itself is also unresolved.
- **Resolution test** 1. Perform a more specific perturbation, such as inserting a polyA signal or transcription terminator within the MestXL-specific exon to truncate the transcript without affecting canonical Mest. 2. Alternatively, use a CRISPRi approach targeting the MestXL-specific promoter or first exon. 3. Provide evidence that the ASO does not affect the stability or transcription of other Mest isoforms by RT-qPCR with isoform-specific primers. 4. If the RNA itself is repressive, tethering MestXL RNA to the Copg2 locus in trans could be tested, though technically challenging.

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** No
- **Axis** Specificity of enhancer function / pleiotropic effects
- **Claim pointer** "E105 acts as a long-range enhancer that promotes maternal Copg2 expression through allele-specific chromatin interactions, while on the paternal allele it engages the Mest/MestXL promoter to drive transcription."
- **Evidence pointer** Figure 5c–g, Figure 6b, f; Results section "CRISPRi screening reveals a distal enhancer for the Mest-Copg2 domain"
- **Concern** The CRISPRi screen targeted 25 accessible chromatin peaks, and only E105 showed a significant effect on Mest expression. However, the authors note that gRNA efficiency was variable (Supplementary Fig. 13m), and E111 did not induce H3K9me3. This raises the possibility that other regulatory elements were missed due to inefficient targeting. Furthermore, the E105 perturbation reduces Mest expression and alters Copg2 allelic bias, but the effect on total Copg2 levels is not significant. The model posits that E105 is a "distal enhancer" for both genes, but the evidence for direct enhancer activity on Copg2 is indirect (allelic bias change without total expression change). The enhancer could be primarily a Mest enhancer, with the Copg2 effect being an indirect consequence of altered Mest/MestXL transcription.
- **Why it matters** The claim that E105 is a shared enhancer with allele-specific target selection is a key conceptual advance. If E105 primarily regulates Mest, and the Copg2 effect is secondary, the model is less novel and more consistent with known mechanisms of antisense-mediated repression.
- **Resolution test** 1. Perform a more comprehensive screen with validated gRNAs for all candidate regions, or use a tiling approach. 2. Test whether E105 can activate a reporter construct in an enhancer assay (e.g., luciferase or STARR-seq) in a cell-type-specific manner. 3. Use a more direct readout of enhancer activity, such as H3K27ac HiChIP or PLAC-seq, to confirm that E105 contacts the Copg2 promoter on the maternal allele with active chromatin marks. 4. Perform an allelic CUT&Tag for H3K27ac at the Copg2 promoter following E105 perturbation to see if maternal H3K27ac is specifically reduced.

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** No
- **Axis** Generalizability / statistical rigor
- **Claim pointer** "Across the eight imprinted domains examined... most domains exhibited clear allele-specific chromatin architectures"
- **Evidence pointer** Figure 1a–p, Supplementary Figures 2–9
- **Concern** The claim that "most" domains exhibit allele-specific architectures is qualitative. The authors state that the magnitude of differences varies between loci, but no quantitative metric (e.g., an allele-specific insulation score, correlation coefficient, or statistical test) is provided to support this claim across all eight domains. The visual inspection of contact matrices is subjective, and some domains may show more subtle differences than others. The pile-up analysis (Figure 2a, b) is only shown for gDMRs and sDMRs collectively, not for individual domains.
- **Why it matters** The systematic nature of the analysis is a stated strength of the paper. Without quantitative metrics, the reader cannot assess the extent or consistency of allele-specific architecture across domains. This weakens the generalizability of the conclusions.
- **Resolution test** 1. Provide a quantitative measure of allele-specific architecture for each domain, such as an allele-specific insulation score, the number of allele-specific loops, or a correlation coefficient between maternal and paternal contact matrices. 2. Perform a statistical test (e.g., a permutation test) to determine whether the observed allelic differences are significant for each domain. 3. Present these metrics in a summary table or figure.

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** Causal inference / DNMTi experiment
- **Claim pointer** "Loss of DNA methylation leads to biallelic CTCF binding, increased insulation at normally methylated alleles, and disruption of allele-specific chromatin organization, accompanied by reduced allelic expression bias."
- **Evidence pointer** Figure 2d–g; Results section "Methylation-sensitive CTCF at ICRs shapes allelic architecture"
- **Concern** The DNMTi experiment is performed in mESCs, which the authors acknowledge show partial loss of imprinting even under control conditions ("many imprinted genes maintained moderate-to-strong allelic bias (≥60% expression from one allele), likely reflecting partial loss of DNA methylation at DMRs in cultured mESCs"). This baseline instability complicates interpretation. Furthermore, DNMTi induces genome-wide demethylation, so the observed effects on chromatin architecture and gene expression could be indirect consequences of global epigenetic disruption rather than direct effects at ICRs. The authors acknowledge this limitation but do not provide a control experiment to address it.
- **Why it matters** The causal link between DNA methylation, CTCF binding, chromatin architecture, and imprinted expression is a central tenet of the paper. The DNMTi experiment is the primary evidence for this causal chain, but its interpretability is compromised by the cell system and the global nature of the perturbation.
- **Resolution test** 1. Perform a more specific perturbation, such as CRISPR-mediated demethylation of individual ICRs using dCas9-TET1, to test causality at specific loci. 2. Alternatively, use a conditional knockout of a maintenance methyltransferase (e.g., UHRF1 or DNMT1) in a more relevant cell type (e.g., neurons) to avoid the baseline instability of mESCs. 3. At minimum, provide a more detailed analysis of the mESC baseline, including the extent of methylation loss at ICRs under control conditions and a comparison of the DNMTi effect on imprinted versus non-imprinted genes.

- **Concern ID** R1-M5
- **Severity** Major
- **Blocking** No
- **Axis** Statistical rigor / multiple testing
- **Claim pointer** "E105 inhibition significantly reduced the maternal-to-paternal expression ratio of Copg2 (Fig. 5d)"
- **Evidence pointer** Figure 5d; Results section "CRISPRi screening reveals a distal enhancer for the Mest-Copg2 domain"
- **Concern** The CRISPRi screen tested 25 gRNA pools targeting 25 different regions. The authors then performed RT-ddPCR for Copg2 allelic ratio only for the E105-targeting condition. It is unclear whether the other 24 conditions were also tested for allelic effects, or if only E105 was followed up. If only E105 was tested, the statistical significance of the allelic effect cannot be properly evaluated in the context of the full screen, as multiple testing correction was not applied across all 25 targets. The p-value reported (p = 0.0022, Dunnett's test) appears to be from a post-hoc comparison within the E105 experiment, not corrected for the initial screen.
- **Why it matters** The identification of E105 as a regulator of Copg2 allelic bias is a key finding. If the statistical analysis does not account for the multiple comparisons inherent in the screen, the finding may be a false positive.
- **Resolution test** 1. Report the results of the allelic analysis for all 25 targets, or clearly state that only E105 was tested. 2. Apply a multiple testing correction (e.g., Bonferroni or FDR) to the initial screen results. 3. If only E105 was tested for allelic effects, acknowledge this limitation and consider the finding as hypothesis-generating rather than confirmatory, pending validation with independent methods (which is partially provided by the Cas9 deletion and AAV experiments).

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** Clarity / presentation
- **Affected element** Figure 2a, b
- **Evidence pointer** Figure 2a, b
- **Issue** The insulation scores reported in the pile-up analysis (0.90 vs 1.87 for gDMRs; 1.21 vs 1.42 for sDMRs) are described in the text as "insulation score," but the interpretation is confusing. A higher insulation score is said to indicate "strong local insulation" (Figure 2a, unmethylated allele), but in the Methods, the authors state that "regions with higher numbers of cross-boundary contacts were considered less insulated (higher insulation score)." This is contradictory.
- **Required correction** Clarify the definition of the insulation score. If a higher score indicates stronger insulation (fewer cross-boundary contacts), correct the Methods description. If a higher score indicates weaker insulation (more cross-boundary contacts), correct the Results text and figure legend. Ensure consistency throughout.

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** Data presentation
- **Affected element** Figure 4b, c
- **Evidence pointer** Figure 4b, c
- **Issue** The fraction of TSS-anchored contacts per allele is shown for non-imprinted and imprinted genes. The statistical test used is not clearly stated in the figure legend or the main text. The p-value in Figure 4e is reported (p = 0.029, Wilcoxon rank-sum test), but the test for Figure 4b is not specified.
- **Required correction** Clearly state the statistical test used for each panel in the figure legend. If no test was performed, state this explicitly and describe the data as descriptive.

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** Completeness
- **Affected element** Results section "Neural-specific chromatin organization at the Meg3 locus"
- **Evidence pointer** Figure 3a–c
- **Concern** The observation at the Meg3 locus is interesting but underdeveloped. The authors attribute the allele-specific organization to "transcription-associated mechanisms" based on H3K36me3 enrichment, but no functional perturbation is performed to test this. The section feels incomplete and does not contribute to the main narrative of the paper.
- **Required correction** Either provide functional data (e.g., transcription inhibition) to support the claim, or reframe this section as a descriptive observation that highlights the diversity of mechanisms, with a clear statement that the mechanism remains to be tested.

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** Clarity
- **Affected element** Results section "CRISPRi screening reveals a distal enhancer for the Mest-Copg2 domain"
- **Evidence pointer** Figure 5c
- **Issue** The RT-qPCR data in Figure 5c shows that E105 inhibition reduces Mest expression but does not change total Copg2 levels. However, the allelic analysis (Figure 5d) shows a change in the maternal-to-paternal ratio. The authors should explicitly state that the total Copg2 level is unchanged, and that the allelic effect is therefore due to a redistribution of expression between alleles (decreased maternal, increased paternal).
- **Required correction** Add a sentence in the Results section clarifying that the total Copg2 level is unchanged, and that the allelic effect reflects a change in the relative contribution of each allele.

- **Concern ID** R1-m5
- **Severity** Minor
- **Axis** Reproducibility
- **Affected element** Methods section "Capture Hi-C analysis"
- **Evidence pointer** Methods
- **Issue** The description of the custom script for filtering read pairs to capture regions and the custom analysis scripts is vague. The code repository URL is provided, but the specific scripts used for key analyses (e.g., pile-up analysis, insulation score calculation, virtual 4C) should be more clearly referenced.
- **Required correction** Provide a more detailed description of the custom scripts, including the specific functions and parameters used. Ensure the code repository is well-documented and contains all scripts necessary to reproduce the key analyses.

- **Technical failings that need to be addressed before the case is established** R1-M1 (specificity of MestXL perturbation), R1-M2 (specificity of E105 function), R1-M3 (quantitative assessment of allele-specific architecture), R1-M4 (causal inference from DNMTi experiment), R1-M5 (multiple testing in CRISPRi screen)

- **Assessment against Nature-style criteria** 
  - **Originality**: High. The systematic analysis of allele-specific chromatin architecture across multiple imprinted domains and the functional dissection of the Mest-Copg2 regulatory logic are novel. The integration of enhancer activity and antisense transcription into a unified model is a conceptual advance.
  - **Scientific importance**: High. The study addresses a fundamental question in gene regulation (how parent-of-origin expression is established and maintained) and provides mechanistic insights that are likely relevant to other imprinted and monoallelically expressed loci.
  - **Interdisciplinary readership**: Moderate to high. The topic is of broad interest to molecular biologists, geneticists, and neuroscientists. The clear writing and well-structured figures make the work accessible to nonspecialists, though some technical details (e.g., Capture Hi-C analysis) may be challenging.
  - **Technical soundness**: Generally high, but several concerns need to be addressed (see Major Concerns). The experimental design is rigorous, with appropriate controls (reciprocal crosses, biological replicates). The data analysis is largely appropriate, but some statistical and interpretational issues remain.
  - **Readability for nonspecialists**: Good. The abstract and introduction provide sufficient background. The results are presented in a logical order, and the figures are well-designed. The discussion effectively summarizes the key findings and places them in context.

- **Recommendation posture** Supportive if technical concerns are resolved. The manuscript presents a significant advance in the field, but the specificity of the perturbations (MestXL, E105), the quantitative rigor of the architectural analysis, and the causal inference from the DNMTi experiment need to be strengthened. The authors should also address the multiple testing issue in the CRISPRi screen.

## Risk / unsupported claims
- The claim that MestXL specifically represses paternal Copg2 through transcriptional interference is not fully supported, as the ASO perturbation also affects canonical Mest. The mechanism of repression (transcriptional interference vs. RNA-mediated repression) is unresolved.
- The claim that E105 is a shared enhancer that directly activates both Mest and Copg2 is not fully supported, as the effect on total Copg2 levels is not significant. The enhancer may primarily regulate Mest, with the Copg2 effect being indirect.
- The claim that the Meg3 locus exhibits allele-specific chromatin organization due to "transcription-associated mechanisms" is not supported by functional data and should be presented as a hypothesis.
- The claim that "most" imprinted domains exhibit allele-specific chromatin architectures is not quantitatively supported.