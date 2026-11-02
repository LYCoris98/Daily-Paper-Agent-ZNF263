## Review setup
- **Input scope** Abstract only (full text not provided)
- **Assessment boundary** Evaluation is restricted to the supplied abstract. No methods, figures, tables, supplementary material, or line-level content were available, so mechanistic, statistical, and reproducibility claims cannot be independently verified.
- **Shared manuscript claim summary** The authors report that cfChIP-seq in prostate cancer plasma defines 35,120 modification-associated positions (MAPs) where nucleosomes carrying H3K4me2 (active) and H3K9me3 (repressive) marks occupy reproducibly offset positions; that these offsets recur across marks, an independent cohort, and nuclease-digested cell-line chromatin; that MAPs are enriched in transcribed genes and depleted near TSS and CTCF sites; that nucleosome protection at MAPs correlates with tumor fraction (TF) across 2,535 cfDNA datasets; that a 50-MAP targeted panel distinguishes TF ≥3% from 0% (AUC 0.91-0.96) and outperforms a fragmentomics-based TF predictor; and that MAP protection at ASCL1 sites detects neuroendocrine transformation.
- **Visible evidence base** Abstract-level statements only. No primary data, no figure or table references, no statistical detail, no cohort descriptions beyond cancer type mentions.
- **Missing materials affecting confidence** Full text, Methods, figures, tables, supplementary data, cohort characteristics, cfChIP-seq quality metrics, antibody validation, statistical models, cross-validation scheme, and independent validation details.

## Reviewer
- **Overall assessment** The abstract describes a conceptually interesting extension of cfDNA fragmentomics, namely that histone-modification state may impose reproducible nucleosome positional offsets detectable in plasma. The reported effect sizes (AUC 0.91-0.96, r = 0.89-0.91) and the breadth of the dataset (2,535 cfDNA datasets) are notable if substantiated. However, from the supplied material alone the central claims are not independently assessable. Key concerns include whether the observed offsets are attributable to histone modification per se rather than to underlying sequence, GC content, or chromatin accessibility; whether the cfChIP-seq signal is specific given the low input and antibody-dependent nature of the assay; and whether the reported performance is established on held-out data. The work is potentially of interest but currently rests on unverifiable abstract-level assertions.
- **Who would be interested in the results, and why** Researchers in liquid biopsy and cfDNA fragmentomics, epigenetics and chromatin biology, prostate and genitourinary oncology, and computational genomics. If validated, a mutation-independent, histone-modification-informed readout of tumor fraction and cancer state would be relevant to minimal residual disease monitoring, treatment response tracking, and lineage plasticity such as neuroendocrine transformation.
- **Major strengths**
  - Addresses a clear biological question, whether cfDNA nucleosome positioning encodes chromatin state and histone modification identity.
  - Reports replication across histone marks, an independent cfChIP-seq cohort, and nuclease-digested cell-line chromatin, which if properly executed strengthens generalizability.
  - Uses a large external corpus (2,535 cfDNA sequencing datasets) for the TF correlation analysis.
  - Demonstrates a potential translational application with a compact 50-MAP panel and comparison against an existing fragmentomics-based predictor.
  - Includes a disease-state application (ASCL1-linked neuroendocrine transformation) that, if robust, would be clinically meaningful.
- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** Causal attribution / confounding
- **Claim pointer** Nucleosomes bearing H3K4me2 and H3K9me3 occupy reproducibly offset positions, and these offsets define distinct nucleosome positions attributable to histone modification state.
- **Evidence pointer** Abstract only; location not provided
- **Concern** The abstract does not establish that the positional offsets are caused by or specific to histone modification status rather than to underlying DNA sequence, GC content, nucleosome occupancy, or chromatin accessibility differences that co-vary with these marks. H3K4me2 and H3K9me3 occupy largely distinct genomic compartments, so offset differences could reflect compartment-level sequence or accessibility properties rather than a direct modification-position relationship.
- **Why it matters** The central mechanistic claim of the paper depends on this attribution. If offsets are confounded by sequence or accessibility, the interpretation that histone modifications "define" nucleosome positions is not supported.
- **Resolution test** Show that offsets persist after controlling for sequence composition, GC content, and accessibility, for example by sequence-matched or accessibility-matched comparisons, or by demonstrating mark-specific offset signatures at the same loci.

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** Assay specificity / technical validity
- **Claim pointer** cfChIP-seq identifies 35,120 modification-associated positions in plasma.
- **Evidence pointer** Abstract only; location not provided
- **Concern** cfChIP-seq from plasma operates on very low input and depends on antibody specificity and immunoprecipitation efficiency. The abstract provides no information on antibody validation, input amounts, background or input controls, or how nonspecific pull-down was excluded. Without this, the 35,120 MAPs cannot be accepted as modification-associated.
- **Why it matters** If the immunoprecipitation is not specific, the MAP set and all downstream analyses, including TF correlation and panel performance, are compromised at the foundation.
- **Resolution test** Report antibody validation (for example peptide competition, knockout or spike-in controls), input and IgG controls, replicate concordance, and fraction-of-reads-in-peaks metrics, with a demonstration that MAPs are recovered above background.

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** Yes
- **Axis** Statistical validity / overfitting
- **Claim pointer** A 50-MAP model distinguished samples with tumor fractions ≥3% vs 0% with AUCs of 0.91-0.96 across prostate, breast, and lung cancers and outperformed a state-of-the-art fragmentomics-based tumor fraction predictor.
- **Evidence pointer** Abstract only; location not provided
- **Concern** The abstract does not state whether the 50-MAP panel and model were derived and evaluated on independent data, how samples were split, whether cross-validation was used, or how the comparator predictor was trained and tuned. With only 50 features selected from 35,120 candidates, selection bias and overfitting are substantial risks, and the cross-cancer generalization claim requires independent cohorts per cancer type.
- **Why it matters** The reported AUCs and the superiority claim over an existing method are only meaningful under a properly held-out evaluation. Without this, the performance figures are not established.
- **Resolution test** Provide a pre-specified train/test split or nested cross-validation, report confidence intervals and sample sizes per cancer type, and demonstrate that the comparator was evaluated under equivalent conditions.

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** Correlation interpretation / confounding by tumor fraction
- **Claim pointer** Nucleosome protection at a subset of MAPs correlated with tumor fraction across 2,535 cfDNA datasets, reflecting differences in histone modification status between cancer-derived and non-malignant chromatin.
- **Evidence pointer** Abstract only; location not provided
- **Concern** Correlation between MAP protection and TF may be driven by global cfDNA fragmentation differences, tumor-derived fragment length distributions, or copy-number effects rather than by histone modification status. The abstract does not describe how TF was estimated, whether the correlation survives adjustment for fragment length and GC, or whether the relationship is monotonic across the TF range.
- **Why it matters** The claim that MAP protection reflects modification-status differences between malignant and non-malignant chromatin requires exclusion of generic fragmentomic confounders.
- **Resolution test** Report partial correlations or regression adjusting for fragment length, GC content, and copy number, and show that MAP protection adds information beyond these covariates.

- **Concern ID** R1-M5
- **Severity** Major
- **Blocking** No
- **Axis** Clinical claim support
- **Claim pointer** MAP protection at ASCL1 binding sites identified neuroendocrine transformation of prostate cancer from cfDNA.
- **Evidence pointer** Abstract only; location not provided
- **Concern** The number of neuroendocrine transformation cases, the reference standard used to define transformation, and whether the finding was validated are not stated. A single or few cases would not support a general detection claim.
- **Why it matters** This is the most clinically consequential claim in the abstract and is presented without any indication of cohort size or validation.
- **Resolution test** Report the number of transformation events, the reference standard (for example histopathology or clinical criteria), and independent validation, ideally with sensitivity and specificity.

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** Terminology precision
- **Affected element** Use of "define" in the title and abstract
- **Evidence pointer** Title; Abstract; location not provided
- **Issue** "Define" implies a causal or deterministic relationship that correlational cfChIP-seq data cannot establish.
- **Required correction** Soften to "are associated with" or "distinguish" unless causal evidence is provided.

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** Cohort reporting
- **Affected element** Patient and sample description
- **Evidence pointer** Abstract; location not provided
- **Issue** No sample sizes, cancer stages, treatment status, or cohort composition are given for the prostate cancer plasma cohort or the independent cfChIP-seq cohort.
- **Required correction** Add cohort sizes and key clinical characteristics in the abstract or main text.

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** Comparator description
- **Affected element** "state-of-the-art fragmentomics-based tumor fraction predictor"
- **Evidence pointer** Abstract; location not provided
- **Issue** The comparator is not named or cited, and the basis for the superiority claim is not specified.
- **Required correction** Name and cite the comparator and state the metric and conditions of comparison.

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** Numerical consistency
- **Affected element** Genome fraction of the 50-MAP panel
- **Evidence pointer** Abstract; location not provided
- **Issue** The claim that the panel uses fragments from "< 0.001% of the genome" is not accompanied by the genomic span or calculation.
- **Required correction** Provide the panel footprint and how the percentage was computed.

- **Concern ID** R1-m5
- **Severity** Minor
- **Axis** Reproducibility
- **Affected element** Data and code availability
- **Evidence pointer** Abstract; location not provided
- **Issue** No accession numbers or code repository are mentioned.
- **Required correction** Provide data accessions and analysis code.

- **Technical failings that need to be addressed before the case is established** R1-M1, R1-M2, R1-M3 (blocking); R1-M4 and R1-M5 additionally required for the correlative and clinical claims respectively.

- **Assessment against Nature-style criteria**
  - **Originality** Moderate to high if substantiated. Using histone-modification-associated nucleosome offsets in cfDNA as a readout is a distinct angle relative to standard fragmentomics, though it builds on established cfChIP-seq and nucleosome-positioning literature.
  - **Scientific importance** Potentially high for liquid biopsy if the modification-specificity and TF-independence claims hold. Currently asserted rather than demonstrated in the supplied material.
  - **Interdisciplinary readership** Reasonable. The work spans epigenetics, computational genomics, and oncology, which suits a broad audience if the technical basis is made accessible.
  - **Technical soundness** Not assessable from the abstract. Specificity of cfChIP-seq, control for sequence and accessibility confounders, and held-out evaluation of the 50-MAP model are unresolved.
  - **Readability for nonspecialists** The abstract is generally clear, but terms such as MAPs, cfChIP-seq, and tumor fraction are used without brief definition, and the distinction between correlation and causation is blurred by "define."

- **Recommendation posture** Currently not established from the provided evidence. Supportive of further consideration only if the blocking technical concerns (R1-M1, R1-M2, R1-M3) are resolved with full methods, controls, and held-out validation.

## Risk / unsupported claims
- That histone modifications "define" nucleosome positions, which asserts causality not demonstrated by the supplied material (unsupported as stated).
- That the 35,120 MAPs are modification-associated, absent antibody validation and background controls (not assessable).
- That MAP protection reflects histone modification status differences between cancer and non-malignant chromatin, absent adjustment for fragmentomic confounders (weak as presented).
- That the 50-MAP model achieves AUC 0.91-0.96 and outperforms a state-of-the-art predictor, absent a described held-out evaluation and named comparator (not assessable).
- That MAP protection at ASCL1 sites identifies neuroendocrine transformation, absent cohort size, reference standard, and validation (not assessable).
- That the approach is a "mutation-independent readout of tumor fraction and cancer state from routine cfDNA sequencing," which generalizes beyond the evidence presented (overreach relative to supplied material).