## Review setup
- **Input scope** Abstract only
- **Assessment boundary** Claims and evidence as presented in the abstract; no methods, figures, tables, or supplementary materials were provided
- **Shared manuscript claim summary** The authors claim that CDT-II, an architecture mirroring the central dogma (DNA self-attention, RNA self-attention, DNA-to-RNA cross-attention), trained on genomic embeddings and raw per-cell expression, can predict CRISPRi perturbation effects, recover known regulatory networks, concentrate attention on regulatory elements, and provide clinically relevant gradient attributions without clinical input
- **Visible evidence base** Abstract-level statistics only: per-gene mean r = 0.84 for perturbation prediction; 6.6-fold enrichment, P = 3.5 x 10^-17 for GFI1B network recovery; mean 7.67x cross-attention enrichment on ENCODE elements, P < 0.001; mean r = 0.82 for gradient attribution on therapeutic targets; TFRC case study narrative
- **Missing materials affecting confidence** Full methods, model architecture details, training/validation splits, baseline comparisons, figure panels, statistical test descriptions, data preprocessing steps, and code verification are not available. The abstract alone cannot support rigorous assessment of the core claims

## Reviewer
- **Overall assessment** The abstract presents an ambitious and potentially valuable framework for interpretable modeling of gene regulation. The reported performance metrics are impressive, and the TFRC case study is a compelling demonstration of clinical relevance emerging from a purely mechanistic model. However, the abstract-level evidence is insufficient to verify the statistical rigor, the validity of the held-out gene evaluation, or the biological specificity of the attention and attribution maps. The central claim that CDT-II functions as an "AI microscope" requires substantially more technical and biological validation than can be assessed from this material.

- **Who would be interested in the results, and why** Computational biologists developing interpretable deep learning models for genomics; experimental biologists studying gene regulatory networks and CRISPR screens; clinicians and translational researchers interested in target identification and drug mechanism prediction. The promise of recovering clinically relevant regulatory structure without clinical data input would attract broad interdisciplinary interest if substantiated.

- **Major strengths** The architectural design directly mirrors the central dogma, which is a conceptually elegant and biologically motivated approach to interpretability. The held-out gene evaluation strategy for CRISPRi prediction is a strong methodological choice. The TFRC case study provides a concrete, clinically anchored demonstration that moves beyond abstract performance metrics. The public availability of code, embeddings, and weights is commendable for reproducibility.

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** Statistical validity
- **Claim pointer** "CDT-II predicts perturbation effects (per-gene mean r = 0.84)" and "Gradient attribution predicts consequences of perturbing therapeutic targets (mean r = 0.82)"
- **Evidence pointer** Abstract, Results section; location not provided
- **Concern** The abstract reports correlation coefficients without specifying the number of genes tested, the variance across genes, the baseline comparator, or the statistical significance of these correlations. A mean r of 0.84 across an unspecified number of held-out genes could range from highly robust to fragile depending on the spread and the number of observations.
- **Why it matters** Correlation coefficients are sensitive to outlier influence and sample size. Without confidence intervals, per-gene distributions, or comparison to a null model or simpler baseline, the reader cannot assess whether the predictive performance reflects genuine biological signal or artifacts of the evaluation setup.
- **Resolution test** Provide per-gene correlation distributions, confidence intervals, number of held-out genes, and comparison to at least one non-interpretable baseline model (e.g., a standard transformer without central dogma structure) and a simple linear model.

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** Biological specificity
- **Claim pointer** "recovers the GFI1B regulatory network (6.6-fold enrichment, P = 3.5 x 10^-17)" and "concentrates cross-attention on ENCODE regulatory elements including CTCF sites (mean 7.67x across 28 target genes, P < .001)"
- **Evidence pointer** Abstract, Results section; location not provided
- **Concern** The enrichment statistics are reported without defining the background model, the set of genes or elements tested, or the correction for multiple comparisons. A 6.6-fold enrichment could be trivially achieved if the background set is poorly matched. Similarly, the cross-attention enrichment on ENCODE elements requires a clear null distribution to be interpretable.
- **Why it matters** Regulatory network recovery and attention enrichment are central to the interpretability claim. If the enrichment statistics are not rigorously defined against appropriate null models, the "AI microscope" claim is not established. The biological specificity of attention maps is a known challenge in genomics deep learning, and the abstract does not demonstrate that the enrichment is specific to relevant cell types or conditions.
- **Resolution test** Specify the background model, the full set of tested genes/elements, multiple testing correction method, and demonstrate that enrichment is cell-type-specific and not reproduced by a permuted-label or randomly initialized model.

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** Yes
- **Axis** Clinical claim validity
- **Claim pointer** "For TFRC, target of the anti-TfR1 antibody PPMX-T003, it identifies erythrocyte-structure, iron-dependent DNA-synthesis and oxidative-stress genes, matching anemia and ferroptosis reported clinically and preclinically-without clinical data as input"
- **Evidence pointer** Abstract, Results section; location not provided
- **Concern** The TFRC case study is presented as a narrative without quantitative evidence. No metrics are provided for how the identified genes were selected, how the match to clinical and preclinical reports was scored, or whether this match exceeds what would be expected by chance from a generic erythroid gene set.
- **Why it matters** This case study is the most compelling translational claim in the abstract. Without a formal enrichment analysis against known TFRC biology or a blinded evaluation, the "matching" could reflect investigator interpretation rather than model performance. The claim that this occurs "without clinical data as input" is important but requires demonstration that the model was not indirectly exposed to clinical information through training data.
- **Resolution test** Provide a quantitative enrichment analysis of the TFRC-attributed genes against curated gene sets for erythrocyte biology, iron metabolism, and ferroptosis, with appropriate background control and multiple testing correction. Also confirm that no clinical annotations were present in any training data.

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** Generalizability
- **Claim pointer** "CDT-II predicts perturbation effects" and "acts as an AI microscope, surfacing clinically relevant regulatory structure from perturbation experiments alone"
- **Evidence pointer** Abstract, Results section; location not provided
- **Concern** The abstract reports results on K562 CRISPRi data only. It is unclear whether the model generalizes to other cell types, other perturbation modalities (e.g., CRISPRa, knockdown), or other species. The "microscope" metaphor implies a general tool, but the evidence is from a single cell line.
- **Why it matters** Regulatory mechanisms are highly context-dependent. A model that works only in K562 would have limited utility. The generalizability claim is implicit in the framing but not tested.
- **Resolution test** Add at least one additional cell type or perturbation dataset to demonstrate cross-context validity, or explicitly scope the claims to K562.

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** Reproducibility
- **Affected element** Availability statement
- **Evidence pointer** Abstract, Availability section
- **Issue** The abstract states that code, embeddings, training data, and weights are available, but does not specify the license, the compute environment, or the expected runtime for reproducing the main results.
- **Required correction** Add a brief statement on software dependencies, hardware requirements, and expected runtime, or refer to a reproducibility section in the full manuscript.

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** Clarity
- **Affected element** Terminology
- **Evidence pointer** Abstract, Results section
- **Issue** The term "AI microscope" is used without definition. It is a metaphor that may be unclear to readers outside the deep learning community.
- **Required correction** Define the term operationally in the abstract or first mention, e.g., "a model whose attention and attribution maps can be directly inspected to reveal regulatory structure."

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** Statistical reporting
- **Affected element** P-values
- **Evidence pointer** Abstract, Results section
- **Issue** P-values are reported for enrichment statistics but the test type (e.g., hypergeometric, permutation, bootstrap) is not stated.
- **Required correction** Specify the statistical test used for each reported P-value in the abstract or refer to the methods section.

- **Technical failings that need to be addressed before the case is established** R1-M1 (statistical rigor of correlation metrics), R1-M2 (enrichment background and multiple testing), R1-M3 (quantitative validation of the TFRC case study). These are the primary technical issues that prevent the core claims from being fully assessed.

## Risk / unsupported claims
- The "AI microscope" framing as a general tool is not supported by single-cell-line evidence
- The clinical relevance claim for TFRC is narrative and lacks quantitative validation
- The held-out gene evaluation is described but the number of genes and variance are not reported
- The enrichment statistics lack defined background models and multiple testing corrections
- The claim that the model works "without clinical data as input" cannot be verified without confirmation that no clinical annotations leaked into training data