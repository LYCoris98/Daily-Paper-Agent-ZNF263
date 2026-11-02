## Review setup
- **Input scope** Full manuscript text provided (Abstract, Introduction, Results, Discussion, Methods, Author Contributions, Data Availability, Acknowledgments). Figures, figure legends, and supplementary tables are referenced but not supplied.
- **Assessment boundary** Assessment is limited to the written text and the claims as stated. No figure panels, supplementary tables (Table S1–S8), raw data, or statistical detail beyond what is described in prose were available for verification.
- **Shared manuscript claim summary** The authors propose that nuclear (not total intracellular) lactate availability sets H3K18 lactylation in breast cancer; that a CTCF–LDHB axis, together with ERα status, determines whether LDHB is expressed (TNBC) or repressed (non-TNBC); that LDHB consumes lactate to favor H3K18 acetylation while CTCF-dependent MCT1 delivers lactate to the nucleus to sustain H3K18la where LDHB is low; and that at a CTCF site downstream of TACC3 exon 3, H3K18la versus H3K18ac recruits distinct reader/splicing-factor complexes (SMARCA4–hnRNPA1 vs TRIM33–SRSF10) to drive exon skipping (EMT) versus inclusion (stemness), with LDHB inhibition suppressing tumor growth in vivo.
- **Visible evidence base** Narrative descriptions of: scRNA-seq reanalysis (GSE165929, GSE161529), ATAC-seq and CTCF ChIP-seq in MCF7, RNA-seq after CTCF depletion, Seahorse ECAR/OCR, dCas9-DNMT3A/HDAC3/AARS1 epigenome editing, luciferase reporter and site-directed mutagenesis, ChIP-qPCR/MeDIP-qPCR, histone mark immunoblotting, nuclear/intracellular/extracellular lactate and pyruvate assays, LDHB overexpression and AXKO-0046 inhibition, PAR-CLIP, proximity ligation assay, confocal imaging, TACC3 isoform functional assays, and a 4T1 syngeneic mouse tumor experiment. All quantitative support resides in figures/tables not provided.
- **Missing materials affecting confidence** All main figures (1–15) and supplementary figures (S1–S5); Tables S1–S8; figure legends; raw sequencing data (stated as deposited but "available upon publication"); patient clinicopathological detail (Table S6); antibody and primer tables; any statistical reporting (n, tests, correction) beyond brief mentions.

## Reviewer
- **Overall assessment** The manuscript describes a mechanistically ambitious, multi-layered model linking CTCF, subtype-specific lactate handling, intragenic histone H3K18 acylation, and co-transcriptional alternative splicing of TACC3, with an in vivo LDHB-inhibition arm. The conceptual framing (nuclear lactate as the proximal determinant; kinetic-plus-adaptor coupling) is coherent and potentially interesting. However, from the supplied text alone, the central causal chain is not established. Several key steps rest on correlative or single-system observations, some internal statements are inconsistent, and critical controls and quantitative detail are not visible. The work is not assessable at the level required to support its headline claims without the figures, tables, and statistics.
- **Who would be interested in the results, and why** Cancer metabolism and epigenetics researchers (lactate, lactylation, LDHB, MCT1/MCT4), chromatin and transcription biologists (CTCF, Pol II pausing, histone acylation readers), RNA-processing/splicing groups (co-transcriptional splicing, hnRNPA1, SRSF10, TRIM33, SMARCA4), and breast-cancer translational researchers interested in TNBC subtype-specific vulnerabilities and LDHB as a target.
- **Major strengths**
  - A clear, testable central hypothesis that distinguishes nuclear from total lactate as the determinant of H3K18la, which is a meaningful refinement over bulk-lactate framing.
  - Use of orthogonal perturbations (genetic depletion, dCas9-DNMT3A/HDAC3/AARS1 targeted editing, pharmacological LDHB inhibition, overexpression) across two subtype-representative lines.
  - A locus-resolved mechanistic proposal at TACC3 exon 3 that attempts to unify kinetic (Pol II pause) and adaptor (reader plus splicing factor) models.
  - Inclusion of an in vivo tumor-growth arm and patient-sample correlation, which, if supported, would extend the findings beyond cell lines.
- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** Causal inference / central claim
- **Claim pointer** Nuclear lactate availability, rather than total intracellular lactate, determines H3K18 lactylation, and LDHB sets this balance.
- **Evidence pointer** Results sections on LDHB and H3K18la (Figure 5, Figure 6); location not provided for underlying data.
- **Concern** The nuclear-versus-total distinction is supported by comparing two cell lines that differ in many respects beyond LDHB (ER status, glycolytic rate, transporter repertoire). The causal test relies on LDHB overexpression in MCF7 and AXKO-0046 in MDA-MB-231, but the text does not report whether nuclear lactate and H3K18la changes were dissociated from total lactate changes, nor whether the inhibitor's effects are on-target and LDHB-specific. The claim that nuclear lactate is "the more proximal determinant" is asserted rather than demonstrated by an experiment that holds total lactate constant while varying nuclear lactate.
- **Why it matters** The central novelty of the paper depends on nuclear lactate being the operative pool. If the observations are equally explained by total lactate, subtype background, or off-target inhibitor effects, the framing collapses to a less distinctive claim.
- **Resolution test** Show that manipulating nuclear lactate import/export (e.g., MCT1/MCT4 or nuclear-targeted perturbations) changes H3K18la while total intracellular lactate is unchanged, and that LDHB rescue/inhibition effects on H3K18la track nuclear rather than total lactate across multiple lines.

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** Mechanistic sufficiency / causality at the TACC3 locus
- **Claim pointer** At CBSDS downstream of TACC3 exon 3, H3K18la recruits SMARCA4–hnRNPA1 to drive exon skipping, whereas H3K18ac recruits TRIM33–SRSF10 to drive inclusion.
- **Evidence pointer** Results sections on TACC3 splicing and reader complexes (Figures 9–12); location not provided.
- **Concern** The reader/splicing-factor assignments rest largely on depletion-plus-occupancy and PLA interaction data. The text does not establish direct binding of SMARCA4 to H3K18la or TRIM33 to H3K18ac at this locus, nor that reader recruitment is the causal determinant of the splicing outcome rather than a correlate of the mark. The claim that hnRNPA1 binds a "consensus splicing silencer motif near exon 3" and that SRSF10 "stabilizes 3'/5' splice site recognition" is stated without supporting data in the text.
- **Why it matters** The adaptor model is the mechanistic core of the paper. Without direct binding and epistasis evidence, the reader-to-splicing-factor linkage remains a proposed model rather than an established mechanism.
- **Resolution test** Provide direct binding assays (e.g., recombinant reader domain with modified vs unmodified H3K18 peptides), reader-domain mutants that abolish mark recognition, and epistasis showing that reader/splicing-factor depletion occludes the mark-dependent splicing switch.

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** Yes
- **Axis** Internal consistency / data integrity
- **Claim pointer** CTCF drives LDHB in TNBC and a CTCF–ERα complex represses LDHB in non-TNBC; CTCF is a positive driver of LDHB in both contexts.
- **Evidence pointer** Results section on CTCF/ERα/LDHB (Figures 3–4); location not provided.
- **Concern** The text contains statements that are difficult to reconcile. It states that CTCF depletion or ESR1-promoter methylation "supported LDHB expression" in MCF7 while also concluding CTCF is a positive driver of LDHB and that ERα converts this into repression. The direction of effect of CTCF loss on LDHB in MCF7 is described inconsistently across the section. Additionally, the model requires CTCF occupancy at the LDHB promoter in both lines yet opposite transcriptional outcomes, which is asserted but not mechanistically resolved beyond the ERα/EZH2/H3K27me2 correlation.
- **Why it matters** The subtype-specific LDHB regulation is a load-bearing element of the axis. Contradictory directional statements undermine confidence in the interpretation and in the figure-to-text correspondence.
- **Resolution test** Clarify and reconcile the direction of LDHB change upon CTCF loss in MCF7 versus MDA-MB-231 with matched quantification, and demonstrate the repressive complex (ERα–EZH2–H3K27me2) is necessary and sufficient for LDHB repression at the same CTCF-occupied promoter.

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** Yes
- **Axis** In vivo claim support
- **Claim pointer** Inhibiting LDHB restores exon skipping and suppresses tumor growth in vivo, identifying LDHB as a tractable target in TNBC.
- **Evidence pointer** Results section on in vivo LDHB inhibition (Figure 14); Methods "Animal Experiments"; location not provided.
- **Concern** The in vivo experiment uses 4T1 (murine TNBC) cells and AXKO-0046, but the text does not report whether tumor reduction is accompanied by the proposed molecular mechanism in vivo (TACC3 isoform switching, H3K18la/ac status, target engagement). The link between tumor growth suppression and the CTCF–LDHB–TACC3 axis is asserted rather than demonstrated. Group sizes, randomization detail, and statistical power are not provided in the text.
- **Why it matters** The therapeutic conclusion depends on the in vivo effect being mechanistically attributable to the proposed axis, not to general LDHB inhibition or off-target toxicity.
- **Resolution test** Show target engagement and pathway readouts (TACC3 splicing, H3K18la/ac, stemness markers) in treated tumors, with adequate n, randomization, and blinded quantification, and demonstrate that the axis mediates the growth effect.

- **Concern ID** R1-M5
- **Severity** Major
- **Blocking** No
- **Axis** Specificity of pharmacological and epigenetic tools
- **Claim pointer** AXKO-0046 specifically inhibits LDHB; dCas9-HDAC3 removes H3K18la; dCas9-AARS1 writes H3K18la.
- **Evidence pointer** Results sections on LDHB inhibition and targeted editing (Figures 6, 10); Methods "dcas9-mediated epigenome editing"; location not provided.
- **Concern** The text does not report selectivity controls for AXKO-0046 (e.g., LDHB vs LDHA), nor global versus locus-specific effects of dCas9-HDAC3 and dCas9-AARS1. HDAC3 has broad deacetylase activity and AARS1 has reported roles beyond H3K18la; the claim of mark-specific, locus-restricted action is not substantiated in the supplied text.
- **Why it matters** If the tools are not mark- or target-specific, the causal inferences about H3K18la/ac at CBSDS are weakened.
- **Resolution test** Provide selectivity data (dose-response, LDHA/LDHB isoform-specific readouts, catalytically dead dCas9-fusion controls, global histone mark immunoblotting) demonstrating locus-restricted and mark-specific effects.

- **Concern ID** R1-M6
- **Severity** Major
- **Blocking** No
- **Axis** Reproducibility / statistical reporting
- **Claim pointer** Genome-wide and locus-specific conclusions across RNA-seq, ChIP-seq, ATAC-seq, and functional assays.
- **Evidence pointer** Throughout Results; Methods "RNA-seq data analysis", "ChIP-seq data analyses"; location not provided.
- **Concern** The text reports few replicate numbers, effect sizes, or statistical tests for the sequencing and functional comparisons. Several key claims (e.g., "595 downregulated genes had reduced promoter H3K18ac", differential CTCF occupancy, isoform usage) are stated without visible thresholds, replicate structure, or multiple-testing context in the prose. Data availability states sequencing data will be released only upon publication, limiting independent verification.
- **Why it matters** Without replicate and statistical transparency, the robustness of the genome-wide and splicing claims cannot be judged.
- **Resolution test** Report n, statistical tests, effect sizes, and thresholds for each key comparison, and make sequencing data available for review.

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** Nomenclature / clarity
- **Affected element** Figure callout "Figure J" in the MCT1 section.
- **Evidence pointer** Results section on CTCF/MCT1 (Figure 7); location not provided.
- **Issue** The text refers to "Figure J" without a number, which is ambiguous.
- **Required correction** Correct the figure callout to the intended panel.

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** Consistency of cell-line/dataset description
- **Affected element** scRNA-seq dataset identifiers.
- **Evidence pointer** Results (GSE165929) versus Methods (GSE161529); location not provided.
- **Issue** The Results cite GSE165929 while the Methods describe GSE161529, which may be a discrepancy or two different datasets used without clear linkage.
- **Required correction** Clarify which dataset underlies each analysis and reconcile the identifiers.

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** Terminology precision
- **Affected element** Use of "acylation" in the title versus "acetylation/lactylation" in the text.
- **Evidence pointer** Title; throughout.
- **Issue** "Acylation switch" is used broadly; the manuscript specifically addresses H3K18la and H3K18ac. The broader term may overstate generality.
- **Required correction** Define acylation scope explicitly or use the specific marks consistently.

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** Reporting completeness
- **Affected element** Patient sample analysis.
- **Evidence pointer** Methods "Breast Cancer Patient Samples"; Figure 5D–F; Table S6; location not provided.
- **Issue** Sample number, subtype composition, and staging are deferred to a supplementary table not provided; the correlation claim cannot be evaluated.
- **Required correction** Report n per subtype and the statistical basis for the LDHB–H3K18la correlation in the main text.

- **Concern ID** R1-m5
- **Severity** Minor
- **Axis** Figure-to-text traceability
- **Affected element** Numerous multi-panel figure references.
- **Evidence pointer** Throughout Results; location not provided.
- **Issue** Many claims are attributed to figure panels that are not supplied, preventing verification of whether the text matches the data.
- **Required correction** Ensure each claim maps to a specific, legible panel with quantified replicates.

- **Technical failings that need to be addressed before the case is established** R1-M1, R1-M2, R1-M3, R1-M4 (blocking); R1-M5, R1-M6 (supporting). The nuclear-lactate causal claim, the reader/splicing-factor mechanism, the internal consistency of the LDHB regulation model, and the in vivo mechanistic linkage are the primary unresolved items.

- **Assessment against Nature-style criteria**
  - **Originality** The nuclear-lactate framing and the kinetic-plus-adaptor coupling at a single splicing locus are conceptually distinctive. However, individual components (CTCF and Pol II pausing, histone lactylation, reader-recruited splicing factors) build on prior work, and the incremental novelty depends on the nuclear-versus-total distinction being causally demonstrated, which is not yet established from the text.
  - **Scientific importance** Potentially significant for TNBC biology and for lactate–chromatin coupling if the mechanism holds. The therapeutic implication (LDHB inhibition) is attractive but currently supported only by an in vivo growth effect without demonstrated mechanistic linkage.
  - **Interdisciplinary readership** The topic spans metabolism, epigenetics, and RNA processing, which suits a broad audience. The current presentation, with dense locus-level detail and unresolved inconsistencies, would need tightening for non-specialist accessibility.
  - **Technical soundness** Not established from the supplied material. Key causal steps rely on correlative or single-system evidence, tool specificity is not demonstrated, and statistical/replicate reporting is sparse.
  - **Readability for nonspecialists** The narrative is generally well organized, but the density of gene/mark/reader nomenclature and the internal inconsistencies reduce clarity for a general readership.

- **Recommendation posture** Currently not established from the provided evidence. The manuscript is potentially supportive if the blocking technical concerns (nuclear-lactate causality, reader/splicing-factor mechanism, internal consistency, in vivo mechanistic linkage) are resolved with direct evidence and full data/statistics.

## Risk / unsupported claims
- **Unsupported as written** Nuclear lactate, rather than total intracellular lactate, is the proximal determinant of H3K18la (no experiment holding total lactate constant while varying nuclear lactate is described).
- **Unsupported as written** SMARCA4 is a specific reader of H3K18la and TRIM33 a direct binder of H3K18ac at CBSDS (no direct binding data described; reader identity rests on depletion/occupancy and PLA).
- **Unsupported as written** hnRNPA1 binds a consensus silencer motif near exon 3 and SRSF10 stabilizes 3'/5' splice site recognition (asserted without supporting data in the text).
- **Unsupported as written** LDHB inhibition suppresses tumor growth through the CTCF–LDHB–TACC3 axis in vivo (no in-tumor pathway readouts or target engagement reported).
- **Weakly supported** CTCF is a positive driver of LDHB in both subtypes while ERα converts this to repression (directional statements are internally inconsistent in the text).
- **Weakly supported** AXKO-0046 acts specifically on LDHB (no selectivity data described).
- **Weakly supported** dCas9-HDAC3 and dCas9-AARS1 act mark-specifically and locus-restrictedly (no catalytically dead or global-mark controls described).
- **Not assessable** All genome-wide claims (differential CTCF occupancy, H3K18la/ac enrichment, 595-gene intersection, isoform usage) and all patient-sample correlations, because figures, tables, and statistics were not provided.
- **Not assessable** Reproducibility of any result, given absent replicate/statistical reporting and sequencing data withheld until publication.