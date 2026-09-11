# Review

## Review setup
- **Input scope** Full manuscript (including Abstract, Introduction, Results, Discussion, Methods, and Supplementary information)
- **Assessment boundary** Scientific content, experimental design, data analysis, and interpretation as presented in the manuscript
- **Shared manuscript claim summary** The authors report that allele-specific chromatin architecture is a common feature of imprinted domains in mouse brain, driven by methylation-sensitive CTCF binding at imprinting control regions. They identify a distal enhancer (E105) at the Mest-Copg2 domain that engages different promoters on maternal and paternal alleles, and show that Copg2 imprinted expression in neurons is regulated by both enhancer-mediated activation and antisense transcription (MestXL).
- **Visible evidence base** Capture Hi-C, CUT&Tag, ATAC-seq, RNA-seq, CRISPRi screening, ASO knockdown, RT-ddPCR, FISH, DNMTi treatment, ChromHMM analysis
- **Missing materials affecting confidence** No major missing materials identified; all key datasets appear to be presented

## Reviewer
- **Overall assessment** This manuscript presents a comprehensive and technically rigorous analysis of allele-specific chromatin architecture at imprinted domains in the mouse brain. The study combines high-resolution Capture Hi-C with functional perturbations (CRISPRi, ASO, DNMTi) to establish causal relationships between chromatin organization and imprinted gene expression. The identification of a distal enhancer (E105) that engages different promoters on maternal and paternal alleles, together with the demonstration that both enhancer activity and antisense transcription contribute to Copg2 imprinting, represents a significant advance in understanding how 3D genome organization coordinates imprinted regulation. The work is well-executed, the data are generally convincing, and the conclusions are largely supported by the evidence presented.

- **Who would be interested in the results, and why** Researchers in genomic imprinting, 3D genome organization, gene regulation, and neuroepigenetics will find this study of high interest. The systematic analysis of allele-specific chromatin architecture across multiple imprinted domains provides a valuable resource, while the mechanistic dissection of the Mest-Copg2 domain offers a paradigm for how enhancer activity and antisense transcription cooperate to establish allele-specific expression. The work also has broader implications for understanding how chromatin architecture shapes regulatory outcomes in development and disease.

- **Major strengths** 1) High-resolution, allele-specific Capture Hi-C across multiple imprinted domains in primary neural tissue, providing a systematic view of parent-of-origin chromatin organization. 2) Integration of multiple complementary approaches (Capture Hi-C, CUT&Tag, ATAC-seq, CRISPRi, ASO, DNMTi) to establish causal relationships. 3) Identification and functional validation of a distal enhancer (E105) that exhibits allele-specific promoter engagement. 4) Demonstration that both enhancer-mediated activation and antisense transcription contribute to Copg2 imprinting, providing a dual regulatory mechanism. 5) Rigorous use of reciprocal crosses to control for strain-specific effects.

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** No
- **Axis** Causal inference / experimental design
- **Claim pointer** "E105 acts as a long-range enhancer that promotes maternal Copg2 expression through allele-specific chromatin interactions, while on the paternal allele it engages the Mest/MestXL promoter to drive transcription."
- **Evidence pointer** Figures 5, 6; Results sections "CRISPRi screening reveals a distal enhancer for the Mest-Copg2 domain" and "Copg2 is regulated by both a distal enhancer and MestXL transcription"
- **Concern** The claim that E105 engages different promoters on the two parental alleles is based on virtual 4C profiles (Fig. 6b) showing preferential contacts to Mest on paternal and Copg2 on maternal alleles. However, the resolution of Capture Hi-C (5 kb bins) is insufficient to definitively assign these contacts to specific promoters, particularly given that the Mest and Copg2 TSSs are separated by only ~150 kb and the E105 region may contact multiple genomic loci. The virtual 4C profiles show relative enrichment, not absolute specificity, and the authors acknowledge that "E105 was not the highest frequency contact for either promoter." The functional data (CRISPRi, ASO) demonstrate that E105 regulates both genes, but do not directly prove that the mechanism involves differential physical contact rather than, for example, indirect effects through chromatin state changes or other regulatory elements.
- **Why it matters** The central mechanistic model of the paper—that allele-specific chromatin architecture directs enhancer engagement with different target genes on maternal versus paternal alleles—depends on this claim. If the enhancer contacts both promoters on both alleles but exerts different effects due to other factors (e.g., promoter competence, local chromatin state, or the presence of MestXL transcription), the model would need substantial revision.
- **Resolution test** Higher-resolution approaches (e.g., Micro-C, HiChIP for H3K27ac, or 4C-seq at sub-kb resolution) could more definitively establish allele-specific enhancer-promoter contacts. Alternatively, allele-specific enhancer deletion or activation (e.g., using dCas9-p300) combined with allele-specific expression analysis could test whether the enhancer is required for maternal Copg2 activation and paternal Mest activation independently. The authors should also consider whether the observed contact patterns could be explained by other mechanisms, such as allele-specific chromatin state differences at the enhancer itself.

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** No
- **Axis** Mechanistic interpretation / specificity of perturbation
- **Claim pointer** "Mest/MestXL then contributes to repression of paternal Copg2, likely through transcriptional interference, although a direct repressive role of the RNA cannot be excluded."
- **Evidence pointer** Figures 6d-f; Results section "Copg2 is regulated by both a distal enhancer and MestXL transcription"
- **Concern** The ASO targeting the MestXL extended 3' UTR reduced MestXL by >93% but also partially reduced total Mest RNA (~50%). The authors acknowledge this but refer to the perturbation as "Mest/MestXL knockdown." This confound makes it difficult to distinguish whether the observed increase in paternal Copg2 expression is due to loss of MestXL specifically, loss of Mest (which is the canonical protein-coding transcript), or both. Furthermore, the ASO mechanism (inducing premature transcription termination) could have indirect effects on local chromatin state or transcription factor binding that are independent of the RNA product. The claim that MestXL is "nuclear-enriched" (Fig. 6d) is based on fractionation, but the enrichment is modest (~2-fold) compared to known nuclear lncRNAs (Neat1, Malat1), and the FISH data (Supplementary Fig. 14d) show co-localization with the Copg2 transcription site but do not quantify the proportion of MestXL molecules that are nuclear versus cytoplasmic.
- **Why it matters** The model proposes that MestXL acts as a repressive transcript on the paternal allele, but the evidence for this specific mechanism is incomplete. If the effect is mediated by Mest rather than MestXL, or if the ASO has off-target effects, the model would need to be revised. Understanding the precise mechanism is important for the broader claim that antisense transcription and enhancer activity cooperate to establish imprinting.
- **Resolution test** 1) Perform rescue experiments by expressing MestXL (or Mest) from a heterologous locus in the ASO-treated cells to determine which transcript is responsible for the repression. 2) Use CRISPRi to specifically target the MestXL promoter without affecting Mest transcription, if such a distinction is possible. 3) Quantify the nuclear-to-cytoplasmic ratio of MestXL more rigorously using spike-in controls and multiple reference genes. 4) Test whether MestXL RNA itself can repress Copg2 when expressed in trans (e.g., by plasmid transfection).

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** No
- **Axis** Generalizability / scope of claims
- **Claim pointer** "allele-specific chromatin architecture is a common feature of imprinted domains in the mouse brain"
- **Evidence pointer** Figures 1, 2; Results section "Imprinted domains exhibit allele-specific chromatin architectures"
- **Concern** The study examines eight imprinted domains, and the authors state that "most domains exhibited clear allele-specific chromatin architectures, although the magnitude of these differences varied between loci." However, the analysis is limited to these eight domains, which were selected based on prior knowledge of imprinting. The claim of "common feature" would be strengthened by a more systematic, unbiased assessment. Additionally, the Capture Hi-C approach targets only ~23 Mb across these eight domains, so the study cannot address whether allele-specific architecture is a general property of imprinted regions genome-wide. The authors also note that "the magnitude of these differences varied," but do not provide a quantitative framework for assessing what constitutes a meaningful architectural difference versus noise.
- **Why it matters** The title and abstract emphasize the systematic nature of the analysis, but the scope is limited to eight pre-selected domains. Overstating the generalizability could mislead readers about the prevalence of allele-specific chromatin architecture at imprinted loci.
- **Resolution test** 1) Provide a quantitative metric (e.g., insulation score difference, contact frequency difference) for each of the eight domains and define a threshold for "clear" allele-specific architecture. 2) Discuss the limitations of the targeted approach more explicitly in the Discussion. 3) If possible, perform a genome-wide analysis (e.g., using existing Hi-C data) to assess whether the eight domains are representative of imprinted regions more broadly.

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** Statistical rigor / reproducibility
- **Claim pointer** "CRISPRi-mediated repression of E105 resulted in a significant, though incomplete, reduction of H3K27ac at the enhancer site in NPC-derived neurons (padj = 1.7 × 10−13)"
- **Evidence pointer** Figure 5e; Results section "CRISPRi screening reveals a distal enhancer for the Mest-Copg2 domain"
- **Concern** The statistical analysis of H3K27ac changes at E105 following CRISPRi is based on CUT&Tag data from n=2 biological replicates per condition. While the p-value is highly significant, the small sample size raises concerns about the reliability of the effect size estimate and the potential for false positives. The authors also report that H3K27ac at the Mest and Copg2 promoters was not significantly changed (padj > 0.95), but with n=2, the power to detect moderate changes is very low. The incomplete reduction of H3K27ac at E105 (the authors describe it as "significant, though incomplete") is consistent with partial CRISPRi efficiency, but the quantitative extent of the reduction is not reported.
- **Why it matters** The conclusion that E105 functions as an enhancer depends on the specificity of the CRISPRi effect. If the H3K27ac reduction is not robustly quantified, or if the sample size is insufficient to detect off-target effects at promoters, the interpretation could be compromised.
- **Resolution test** 1) Increase the number of biological replicates for CUT&Tag to at least n=3. 2) Report the fold-change in H3K27ac at E105, not just the p-value. 3) Perform additional validation of CRISPRi specificity, such as measuring H3K27ac at other enhancers in the domain or using a different gRNA targeting E105. 4) Consider using an orthogonal method (e.g., ChIP-qPCR) to confirm the H3K27ac changes.

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** Data presentation / clarity
- **Affected element** Figure 1
- **Evidence pointer** Figure 1a-p
- **Issue** The allele-specific contact matrices in Figure 1a-h are presented at 5 kb resolution, but the authors do not provide a clear visual guide for interpreting the highlighted features (TAD-like structures, loops, stripes). The allelic subtraction maps (Fig. 1i-p) are useful but the color scale is not explicitly defined in the main figure legend.
- **Required correction** Add a schematic or annotation to the figure explaining how to interpret the highlighted features. Include the color scale for the subtraction maps in the main figure legend, not just in the methods.

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** Data interpretation / overstatement
- **Affected element** Abstract
- **Evidence pointer** Abstract, line "These architectures largely originate from imprinting control regions"
- **Issue** The abstract states that allele-specific architectures "largely originate from imprinting control regions," but the evidence for this is correlative (pile-up analysis showing insulation at gDMRs) and the DNMTi experiment is in mESCs, not neurons. The causal relationship is not fully established for all eight domains.
- **Required correction** Soften the language to reflect the correlative nature of the evidence, e.g., "are associated with" or "correlate with" imprinting control regions.

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** Data presentation / completeness
- **Affected element** Figure 5c
- **Evidence pointer** Figure 5c
- **Issue** The CRISPRi screen results show relative Mest and Copg2 expression for 25 gRNA pools, but only E105 is highlighted as significant. The authors should provide the full list of gRNA targets and their effects, either in a supplementary table or as a data source, to allow readers to assess the specificity of the screen.
- **Required correction** Include a supplementary table with all gRNA target coordinates, the number of gRNAs per target, and the expression changes for Mest and Copg2 for each target.

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** Technical detail / reproducibility
- **Affected element** Methods
- **Evidence pointer** Methods, "Capture Hi-C analysis"
- **Issue** The description of the pile-up analysis using Coolpuppy is brief. The authors should specify the parameters used (e.g., window size, normalization method, whether the analysis was performed on merged or individual replicates).
- **Required correction** Provide more detailed parameters for the Coolpuppy analysis, including the specific command or script used.

- **Concern ID** R1-m5
- **Severity** Minor
- **Axis** Data interpretation / clarity
- **Affected element** Figure 6f
- **Evidence pointer** Figure 6f
- **Issue** The statistical comparisons in Figure 6f are complex, with multiple pairwise tests. The authors use Tukey's HSD test, which is appropriate for multiple comparisons, but the figure legend lists many p-values without a clear summary of the main findings. The key result—that E105 inhibition reduces maternal Copg2 and MestXL knockdown increases paternal Copg2—is somewhat obscured by the dense statistical reporting.
- **Required correction** Simplify the figure legend to highlight the main comparisons and their biological interpretation. Consider adding a schematic summary of the results.

- **Concern ID** R1-m6
- **Severity** Minor
- **Axis** Data presentation / completeness
- **Affected element** Supplementary Figure 13
- **Evidence pointer** Supplementary Figure 13a
- **Issue** The ATAC-seq analysis identified ~100 allele-specific peaks, but the authors state that "most of which overlapped known imprinted promoters or DMRs." The number of peaks that do not overlap known imprinted regions is not reported, and these could represent novel regulatory elements.
- **Required correction** Report the number of allele-specific ATAC-seq peaks that do not overlap known imprinted promoters or DMRs, and discuss whether any of these were tested in the CRISPRi screen.

- **Concern ID** R1-m7
- **Severity** Minor
- **Axis** Data interpretation / overstatement
- **Affected element** Discussion
- **Evidence pointer** Discussion, paragraph 4
- **Issue** The authors state that "the Mest–Copg2 domain exhibits a more complex regulatory architecture" than the H19-Igf2 locus, but the comparison is based on a single example. The H19-Igf2 locus is also known to have complex regulation beyond simple insulation (e.g., CTCF-independent mechanisms, multiple enhancers).
- **Required correction** Acknowledge that the H19-Igf2 locus also has complex regulation and that the comparison is illustrative rather than definitive.

- **Technical failings that need to be addressed before the case is established** R1-M1 (allele-specific enhancer-promoter contact specificity), R1-M2 (MestXL mechanism), R1-M4 (statistical rigor of CUT&Tag)

- **Assessment against Nature-style criteria** 
  - **Originality**: High. The systematic analysis of allele-specific chromatin architecture across multiple imprinted domains, combined with functional validation of a distal enhancer and its integration with antisense transcription, represents a novel contribution. The dual regulatory mechanism (enhancer activation + antisense repression) at the Mest-Copg2 domain is a new paradigm.
  - **Scientific importance**: High. The study addresses a fundamental question in genomic imprinting—how 3D genome organization contributes to allele-specific gene regulation—and provides mechanistic insights that are likely to be broadly relevant to understanding long-range gene regulation.
  - **Interdisciplinary readership**: Moderate to high. The work will be of primary interest to researchers in epigenetics, gene regulation, and neurobiology. The technical approaches (Capture Hi-C, CRISPRi, CUT&Tag) are well-established, and the findings are presented in a way that is accessible to specialists. Nonspecialists may find the level of detail challenging.
  - **Technical soundness**: Generally high, with some concerns. The experimental design is rigorous (reciprocal crosses, multiple biological replicates, orthogonal validation). However, the resolution of Capture Hi-C (5 kb) limits the specificity of enhancer-promoter contact assignment, and the ASO experiment has a confound (partial Mest knockdown). The statistical power for some experiments (CUT&Tag with n=2) is limited.
  - **Readability for nonspecialists**: Adequate. The introduction provides sufficient background, and the results are clearly structured. However, the figures are dense and may be difficult for nonspecialists to interpret without careful study. The abstract and discussion effectively summarize the key findings.

- **Recommendation posture** Supportive if technical concerns are resolved. The manuscript presents a valuable and largely convincing study, but the central mechanistic model (allele-specific enhancer-promoter contacts) and the role of MestXL require stronger evidence. The authors should address the concerns about contact specificity (R1-M1) and the ASO confound (R1-M2) with additional experiments or more cautious interpretation. The statistical rigor of the CUT&Tag data (R1-M4) should be improved. If these concerns are satisfactorily addressed, the manuscript would be suitable for publication in a high-impact journal.

## Risk / unsupported claims
- The claim that E105 engages different promoters on maternal and paternal alleles through allele-specific chromatin interactions (R1-M1) is supported by correlative evidence (virtual 4C) but not by direct causal demonstration. The resolution of Capture Hi-C is insufficient to definitively assign contacts to specific promoters.
- The claim that MestXL represses paternal Copg2 through transcriptional interference (R1-M2) is supported by the ASO experiment, but the confound with partial Mest knockdown and the lack of a direct test of the RNA's role make this claim provisional.
- The claim that allele-specific chromatin architecture is a "common feature" of imprinted domains (R1-M3) is based on eight pre-selected domains and may not be generalizable to all imprinted loci.
- The claim that the Meg3 locus exhibits "transcription-associated chromatin features" as an alternative mechanism for allele-specific organization (Fig. 3) is based on correlative evidence (H3K36me3 enrichment) and lacks functional validation. This should be presented as a hypothesis rather than a conclusion.