## Review setup
- **Input scope** Abstract only
- **Assessment boundary** Claims and evidence as presented in the abstract; no figures, methods, or supplementary material were available for evaluation
- **Shared manuscript claim summary** The authors report a new platform, Micro Capture-C variant-to-function (MCCv), that uses single-allele chromatin structure analysis to map regulatory variants in cis-regulatory elements to target genes. They apply this to 405 immune-mediated inflammatory disease-associated cis-regulatory elements in CD4+ T cells, identify a gain-of-function mechanism involving a neo-CTCF motif that blocks super-enhancer contacts with the SESN3 promoter, and demonstrate that SESN3 regulates mTOR via tryptophan sensing with relevance to autoimmunity in mouse models.
- **Visible evidence base** Abstract text only; no figures, tables, methods, or supplementary data provided
- **Missing materials affecting confidence** All primary data, methodological details, statistical analyses, validation experiments, and mouse model results are absent. The abstract alone cannot support assessment of technical soundness or reproducibility.

## Reviewer
- **Overall assessment** The abstract describes a potentially valuable technical advance in variant-to-function mapping, with a compelling biological finding. However, the evidence base available for review is limited to the abstract, which precludes verification of the central claims. The platform concept is innovative and the reported discovery of a neo-CTCF gain-of-function mechanism is of high interest, but the technical and statistical foundations cannot be assessed from the supplied material.

- **Who would be interested in the results, and why** Geneticists and functional genomics researchers studying noncoding variant interpretation, particularly those working on autoimmune disease genetics. The MCCv platform addresses a well-recognized bottleneck in linking GWAS variants to causal mechanisms, and the SESN3-mTOR-tryptophan axis may interest immunologists and researchers studying metabolic regulation of immune responses.

- **Major strengths** The abstract presents a clear technical innovation with a plausible solution to a known problem in variant-to-function mapping. The application to 405 elements in a disease-relevant cell type is substantial in scale. The reported discovery of a neo-CTCF gain-of-function mechanism is mechanistically interesting and provides a concrete example of the platform's utility. The connection from chromatin architecture to gene regulation to metabolic sensing to mouse model validation represents a complete biological narrative.

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** Technical soundness
- **Claim pointer** "MCCv can phase other heterozygous variants within a locus to link regulatory variants to allelically imbalanced gene expression and directly read out variant effects on chromatin interactions after genome editing"
- **Evidence pointer** location not provided
- **Concern** The abstract claims that MCCv can phase heterozygous variants and read out variant effects after genome editing, but no methodological detail, validation data, or performance metrics are provided. It is unclear how single-allele chromatin structure data are generated, what throughput and resolution are achieved, and how phasing is performed.
- **Why it matters** The entire platform claim rests on the technical capability of MCCv. Without evidence of sensitivity, specificity, reproducibility, and comparison to existing methods, the central technical advance cannot be evaluated.
- **Resolution test** Provide methods and validation data demonstrating MCCv performance, including comparison to existing approaches, error rates, and reproducibility metrics.

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** Evidence sufficiency
- **Claim pointer** "We uncovered a previously undescribed gain-of-function mechanism, which increases risk of autoimmunity through creation of a neo-CTCF motif that blocks super-enhancer contacts with the SESN3 promoter"
- **Evidence pointer** location not provided
- **Concern** The abstract asserts a causal chain from a neo-CTCF motif to blocked super-enhancer contacts to increased autoimmunity risk. No data are shown demonstrating that the motif is functional, that the chromatin interaction change is causal rather than correlative, or that the variant is statistically associated with disease in a manner consistent with the proposed mechanism.
- **Why it matters** This is the central biological discovery of the paper. If the causal chain is not rigorously established, the significance of the work is substantially diminished.
- **Resolution test** Provide functional validation of the neo-CTCF motif, allele-specific chromatin interaction data, and genetic evidence linking the variant to disease risk.

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** Yes
- **Axis** Evidence sufficiency
- **Claim pointer** "We showed that SESN3 regulates mammalian target of rapamycin by sensing tryptophan and demonstrated its role in autoimmunity using mouse models"
- **Evidence pointer** location not provided
- **Concern** The abstract makes two substantial biological claims: SESN3 senses tryptophan to regulate mTOR, and SESN3 plays a role in autoimmunity in mouse models. Neither claim is accompanied by any experimental detail, effect sizes, or statistical support.
- **Why it matters** These claims extend beyond the technical platform into new biology. If the tryptophan-sensing mechanism and the mouse model results are not robustly supported, the broader significance of the work is weakened.
- **Resolution test** Provide experimental data for tryptophan sensing, mTOR regulation, and mouse model phenotypes with appropriate statistical analysis.

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** Clarity
- **Affected element** Platform name and description
- **Evidence pointer** Abstract, first sentence
- **Issue** The name "Micro Capture-C variant-to-function platform (MCCv)" is introduced without explaining what distinguishes it from prior Micro Capture-C methods or what "variant-to-function" specifically entails in the platform context.
- **Required correction** Briefly clarify the key innovation over existing Micro Capture-C approaches and define the variant-to-function workflow in one or two sentences.

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** Scope clarity
- **Affected element** Study scale
- **Evidence pointer** Abstract, "we investigated 405 cis-regulatory elements"
- **Issue** It is unclear whether all 405 elements were fully analyzed through the entire MCCv pipeline or whether this number represents the initial screen with a smaller subset taken forward for detailed analysis.
- **Required correction** Clarify how many elements were carried through each stage of the analysis.

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** Generalizability
- **Affected element** Cell type specificity
- **Evidence pointer** Abstract, "in CD4(+) T cells"
- **Issue** The abstract does not address whether MCCv is applicable to other cell types or whether the SESN3 mechanism is CD4+ T cell-specific.
- **Required correction** Add a brief statement on generalizability or acknowledge the cell type limitation.

- **Technical failings that need to be addressed before the case is established** R1-M1, R1-M2, R1-M3. The technical validation of MCCv, the causal evidence for the neo-CTCF mechanism, and the SESN3 biology all require full experimental data before the central claims can be accepted.

- **Assessment against Nature-style criteria** 
  - Originality: High. The single-allele chromatin architecture approach to variant-to-function mapping appears novel and addresses a recognized bottleneck in the field.
  - Scientific importance: Potentially high. Linking noncoding variants to mechanisms in autoimmune disease is of broad interest, and the SESN3-tryptophan-mTOR axis could open new research directions.
  - Interdisciplinary readership: Moderate to high. The work bridges genomics, immunology, and metabolism, which could attract readers across these communities.
  - Technical soundness: Not assessable from the abstract alone. The central platform claims require detailed methods and validation data.
  - Readability for nonspecialists: The abstract is reasonably accessible, though the platform description assumes familiarity with chromatin conformation capture techniques.

- **Recommendation posture** Currently not established from the provided evidence. The abstract presents an interesting concept and a compelling biological narrative, but the absence of all primary data prevents verification of the central technical and biological claims. A full manuscript with methods, figures, and statistical analyses would be required for proper evaluation.

## Risk / unsupported claims
- The claim that MCCv can "directly read out variant effects on chromatin interactions after genome editing" is unsupported without genome editing validation data.
- The claim of a "previously undescribed gain-of-function mechanism" is unsupported without demonstration of novelty relative to existing literature.
- The claim that SESN3 "senses tryptophan" is unsupported without mechanistic data showing direct sensing versus indirect regulation.
- The claim that the mechanism "increases risk of autoimmunity" is unsupported without genetic association data linking the specific variant to disease risk.
- The mouse model demonstration of SESN3's role in autoimmunity is unverifiable without experimental details.