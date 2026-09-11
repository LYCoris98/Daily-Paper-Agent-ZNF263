## Review setup
- **Input scope** Full manuscript (including main text, figures, methods, and supplementary materials)
- **Assessment boundary** Scientific content only; no assessment of formatting, language, or editorial fit
- **Shared manuscript claim summary** The manuscript reports that CTCF depletion in mouse embryonic stem cells does not eliminate TAD-like domains (TLDs) in single cells but redistributes their boundary positions, weakens A compartment interactions, and reduces per-cell transcriptional capacity. The authors develop SALTAFinder to identify higher-order TLD assemblies (SALTAs) and show that active SALTAs are destabilized upon CTCF loss, correlating with reduced expression of genes within them.
- **Visible evidence base** Full text, figures (1–5), supplementary figures (S1–S9), supplementary tables (S1–S3), and detailed Materials and Methods
- **Missing materials affecting confidence** No missing materials identified; all data and code are deposited and accessible

## Reviewer
- **Overall assessment** This is a technically impressive and conceptually important study that leverages a powerful single-cell multiomic approach (HiRES) to dissect the role of CTCF in genome organization and transcription at unprecedented resolution. The development of SALTAFinder to identify higher-order chromatin assemblies from single-cell Hi-C data is a notable methodological advance. The central finding—that CTCF loss does not eliminate domains but rather redistributes boundary positions and destabilizes active chromatin clusters—provides a refined and mechanistically insightful view of CTCF function. The evidence is generally strong, with multiple orthogonal validations. However, several concerns regarding statistical rigor, causal inference, and the interpretation of the SALTA analysis need to be addressed before the conclusions can be fully established.
- **Who would be interested in the results, and why** Chromatin biologists, epigenomics researchers, and computational biologists interested in 3D genome organization, single-cell technologies, and the role of architectural proteins. The study provides a new framework for analyzing single-cell chromatin conformation data and offers mechanistic insights into how CTCF maintains genome architecture and transcriptional capacity.
- **Major strengths** 1. The use of HiRES to jointly profile chromatin contacts and RNA from the same nucleus is a powerful and well-executed approach that enables direct correlation between structural and transcriptional changes. 2. The development of SALTAFinder is a significant methodological contribution that allows systematic identification of higher-order chromatin assemblies from single-cell Hi-C data. 3. The finding that CTCF loss redistributes TLD boundaries rather than eliminating them is a conceptually important refinement of the current understanding. 4. The study provides multiple orthogonal validations (flow cytometry, spike-in RNA-seq, published datasets) that strengthen the key conclusions.
- **Major Concerns**
    - **Concern ID** R1-M1
    - **Severity** Major
    - **Blocking** Yes
    - **Axis** Statistical rigor / causal inference
    - **Claim pointer** "CTCF depletion reduces per-cell transcriptional capacity" (Abstract, Results, Discussion)
    - **Evidence pointer** Fig. 1B-C, Fig. 2F-I, Fig. 4F-G
    - **Concern** The manuscript claims that CTCF depletion causes a reduction in per-cell transcriptional capacity, but the evidence for causality is correlational. The observed reduction in RNA output could be a consequence of cell stress, cell cycle arrest, or indirect effects of CTCF loss on cellular physiology, rather than a direct result of chromatin reorganization. The authors acknowledge this limitation in the Discussion but do not adequately address it. The flow cytometry and spike-in RNA-seq experiments show a reduction in RNA, but they do not distinguish between reduced transcription and increased RNA degradation. Furthermore, the correlation between SALTA disassembly and gene expression changes (Fig. 4F) is modest (Pearson r not reported, only P = 0.017) and does not establish causality.
    - **Why it matters** The claim that CTCF directly regulates global transcriptional capacity through chromatin organization is a central conclusion of the paper. If the observed reduction in RNA is due to indirect effects, the mechanistic link between CTCF, SALTAs, and transcription is weakened.
    - **Resolution test** 1. Report the Pearson correlation coefficient for Fig. 4F. 2. Perform RNA stability assays (e.g., actinomycin D chase) to rule out increased degradation. 3. Use a more direct measure of transcription, such as nascent RNA sequencing (e.g., Bru-seq or PRO-seq), to confirm that the reduction is at the level of transcription. 4. Consider whether cell cycle analysis could explain the reduced RNA output (e.g., if CTCF depletion causes G1 arrest, cells would have less time to accumulate RNA).

    - **Concern ID** R1-M2
    - **Severity** Major
    - **Blocking** Yes
    - **Axis** Methodological validation / robustness
    - **Claim pointer** "SALTAs represent genuine spatial aggregates of distantly located TLDs" (Results, Fig. 3)
    - **Evidence pointer** Fig. 3G, Fig. S7B-E, Fig. S7F-G
    - **Concern** The validation of SALTAs as genuine spatial structures relies heavily on comparisons with shuffled/shifted controls and comparisons with bulk multiway interaction datasets (GAM, SPRITE). However, the shuffled controls may not adequately account for the inherent biases in single-cell Hi-C data, such as the distance-dependent contact probability and the sparsity of contacts. The comparison with GAM/SPRITE is based on a small subset of domain triplets (11,097) and shows only modest overlap (fraction of alleles where all three domains are in the same SALTA). The authors do not report the absolute overlap fraction, making it difficult to assess the biological significance. Additionally, the downsampling analysis (Fig. S7H-L) shows that SALTA features are stable across a range of contact numbers, but the ARI and WS scores are not reported for the lowest contact numbers (e.g., 10,000), where sparsity is most severe.
    - **Why it matters** If SALTAs are not robustly identified or are artifacts of the computational method, the subsequent analysis of their changes upon CTCF depletion is undermined.
    - **Resolution test** 1. Report the absolute overlap fraction between SALTA-containing alleles and GAM/SPRITE triplets, not just the relative enrichment. 2. Provide ARI and WS scores for all downsampling levels, including the lowest (10,000 contacts). 3. Perform additional validation using independent single-cell Hi-C datasets or imaging-based approaches (e.g., DNA FISH) to confirm the spatial clustering of TLDs within SALTAs. 4. Test the sensitivity of SALTAFinder to the modularity threshold and the requirement for at least three TLDs.

    - **Concern ID** R1-M3
    - **Severity** Major
    - **Blocking** No
    - **Axis** Interpretation / overclaim
    - **Claim pointer** "CTCF stabilizes long-range active chromatin clusters" (Title, Abstract, Discussion)
    - **Evidence pointer** Fig. 4A-G, Fig. S8, Fig. S9
    - **Concern** The manuscript concludes that CTCF "stabilizes" active SALTAs, but the evidence only shows that active SALTAs are less prevalent and more expanded upon CTCF loss. The term "stabilization" implies a direct structural role, but the observed changes could be secondary to reduced transcription or other indirect effects. The authors acknowledge this in the Discussion but the title and abstract present a more definitive claim. Furthermore, the classification of SALTAs into active, mixed, and inactive categories (C1-C7) is based on ChromHMM states from bulk data, which may not accurately reflect the chromatin state in individual cells. The K-means clustering of SALTAs is also sensitive to the number of clusters chosen, and the optimal number is not clearly justified.
    - **Why it matters** Overstating the causal role of CTCF in stabilizing SALTAs could mislead the field. A more nuanced interpretation is warranted.
    - **Resolution test** 1. Rephrase the title and abstract to reflect that CTCF loss is "associated with" destabilization of active SALTAs, rather than claiming direct stabilization. 2. Provide a more rigorous justification for the number of SALTA clusters (e.g., using the elbow method or silhouette analysis). 3. Consider using single-cell chromatin state data (if available) or at least discuss the limitations of using bulk ChromHMM states for single-cell analysis.

    - **Concern ID** R1-M4
    - **Severity** Major
    - **Blocking** No
    - **Axis** Statistical rigor / multiple testing
    - **Claim pointer** "1947 bins showed significantly reduced PTLD-B and 1833 showed increases" (Results)
    - **Evidence pointer** Fig. S4J, table S3
    - **Concern** The identification of bins with significantly changed TLD boundary probability (PTLD-B) is a key result, but the statistical method is not clearly described. The authors state that they used a "Wilcoxon test with FDR < 0.05" for compartment scores (Methods), but it is unclear if the same test was used for PTLD-B. Given the large number of bins tested (genome-wide at 50-kb resolution), multiple testing correction is critical. The authors do not report the number of tests or the FDR threshold used.
    - **Why it matters** Without proper statistical rigor, the list of significantly changed bins may contain false positives, undermining the conclusion that boundaries are redistributed rather than lost.
    - **Resolution test** 1. Clearly describe the statistical test used for PTLD-B analysis, including the number of tests and the FDR threshold. 2. Provide a volcano plot or similar visualization showing the distribution of P-values and effect sizes. 3. Consider using a more stringent threshold (e.g., FDR < 0.01) to ensure robustness.

- **Minor Comments**
    - **Concern ID** R1-m1
    - **Severity** Minor
    - **Axis** Clarity / presentation
    - **Affected element** Fig. 1K
    - **Evidence pointer** Fig. 1K
    - **Issue** The color scale for the heatmap in Fig. 1K is not intuitive. The text describes "gray" for decreased PTLD-B and "yellow" for increased, but the heatmap uses a continuous color scale that makes it difficult to distinguish the magnitude of change.
    - **Required correction** Use a diverging color scale (e.g., blue-white-red) with clear annotations for the direction and magnitude of change.

    - **Concern ID** R1-m2
    - **Severity** Minor
    - **Axis** Completeness
    - **Affected element** Fig. 4F
    - **Evidence pointer** Fig. 4F
    - **Issue** The Pearson correlation coefficient (r) is not reported for the correlation in Fig. 4F. Only the P-value is given.
    - **Required correction** Report the Pearson r value alongside the P-value.

    - **Concern ID** R1-m3
    - **Severity** Minor
    - **Axis** Clarity
    - **Affected element** Methods
    - **Evidence pointer** "SALTA identification" section
    - **Issue** The description of the modified fast-greedy algorithm for modularity optimization is somewhat unclear. The authors state that they "started with a state that there are m groups in the graph, where m is the number of TLDs on the chromosome." This implies that each TLD is initially its own group, but the algorithm then merges groups. It would be helpful to clarify that the algorithm is agglomerative.
    - **Required correction** Rewrite the description to explicitly state that the algorithm is agglomerative and that the initial state has each TLD as a separate group.

    - **Concern ID** R1-m4
    - **Severity** Minor
    - **Axis** Reproducibility
    - **Affected element** Methods
    - **Evidence pointer** "SALTA identification" section
    - **Issue** The authors state that SALTAs with a clustering coefficient of 0 are removed, but the rationale for this threshold is not explained. A clustering coefficient of 0 could occur for a SALTA with only two TLDs (which are already removed by the "at least three TLDs" criterion) or for a SALTA with a star-like topology.
    - **Required correction** Provide a brief justification for removing SALTAs with a clustering coefficient of 0, or consider whether this filter is redundant with the "at least three TLDs" criterion.

    - **Concern ID** R1-m5
    - **Severity** Minor
    - **Axis** Interpretation
    - **Affected element** Discussion
    - **Evidence pointer** Discussion
    - **Issue** The Discussion mentions that "the frequency of TLD boundary occurrence at bulk TAD boundaries is likely underestimated" due to limited contact numbers. This is an important caveat that should be mentioned earlier, perhaps in the Results section where PTLD-B is first introduced.
    - **Required correction** Add a sentence in the Results section (where PTLD-B is first discussed) acknowledging that the absolute boundary frequencies are likely conservative estimates due to the sparsity of single-cell Hi-C data.

- **Technical failings that need to be addressed before the case is established** R1-M1 (causal link between CTCF loss and transcriptional reduction), R1-M2 (robustness of SALTA validation), R1-M4 (statistical rigor of PTLD-B analysis)

- **Assessment against Nature-style criteria** 
  - **Originality:** High. The study provides a novel single-cell perspective on CTCF function and introduces a new computational method (SALTAFinder) for identifying higher-order chromatin assemblies. The finding that CTCF loss redistributes rather than eliminates domain boundaries is a significant conceptual advance.
  - **Scientific importance:** High. CTCF is a central architectural protein, and understanding its role in genome organization and transcription is a fundamental question in chromatin biology. The study has implications for development, disease, and the interpretation of bulk Hi-C data.
  - **Interdisciplinary readership:** Moderate to high. The study will be of interest to chromatin biologists, computational biologists, and cell biologists. The methodological aspects (HiRES, SALTAFinder) may also appeal to a broader audience interested in single-cell technologies.
  - **Technical soundness:** Generally high, but with notable concerns. The HiRES data generation and processing are rigorous. The SALTAFinder method is well-described but requires stronger validation. The statistical analysis of PTLD-B changes needs clarification. The causal inference regarding transcriptional reduction is the weakest link.
  - **Readability for nonspecialists:** Good. The manuscript is well-written and the figures are clear. The abstract and introduction provide sufficient background. However, the Methods section is dense and may be challenging for nonspecialists.

- **Recommendation posture** Supportive if technical concerns are resolved. The study has the potential to be a high-impact contribution, but the concerns regarding causal inference, SALTA validation, and statistical rigor must be addressed before the conclusions can be fully accepted.