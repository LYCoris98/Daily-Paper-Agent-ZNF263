# Bromodomain and extra-terminal motif (BET) inhibition induces coordinated repression of the stem cell-related HOX signature in glioblastoma uncovering an epigenetic vulnerability


## Background
  Glioblastoma (GB) is the most aggressive primary brain tumor, characterized by therapy resistance, attributed to a multitude of epigenetic changes resulting in phenotypic plasticity with altered cell states. To uncover druggable epigenetic vulnerabilities, we disturbed GB-derived spheres with an inhibitor of Bromodomain and extra-terminal motif proteins (BETi) and observed coordinated repression of the aberrantly activated hemopoietic stem-like cell signature, dominated by HOXA genes. This signature has been associated with poor prognosis and resistance to therapy in GB. Here we investigate the deregulated epigenetic landscape and potential vulnerabilities in high-HOX GB.


## Methods
  GB-derived spheres (GS) were treated with the BETi (JQ1) or transduced with inducible constructs to genetically modulate HOXA10 expression short-hairpin (sh)RNA for knockdown, ectopic HOXA10). Functional effects were evaluated through proliferation, neurosphere formation, and senescence assays. Epigenomic profiling incorporated RNA-seq, Chromatin Immuno Precipitation sequencing (ChIP-seq), Assay for Transposase-Accessible Chromatin sequencing (ATAC-seq), promoter capture MicroC, and DNA methylation.


## Results
  BETi-mediated rapid, coordinated downregulation of the HOX-signature suggested direct transcriptional regulation. Knockdown of HOXA10 alone yielded similar effects, decreasing expression of HOXA genes, reducing proliferation, self-renewal capacity, and triggering senescence. Conversely, ectopic HOXA10 expression failed to reactivate the HOXA cluster or reverse BETi-mediated biological effects. Integrative epigenomic analysis of high-HOX-GS revealed concerted activation of the HOXA region, with broad domains of H3K27ac/H3K4me3 associated with super-enhancer activity, open chromatin (ATAC), and focal DNA hypomethylation. Architectural changes included altered CCCTC-binding factor (CTCF) interactions and increased promoter-anchored looping.


## Conclusion
  These results position the HOX-signature as a potential therapeutic target and offer a mechanistic rationale for disrupting BET-dependent transcriptional regulation in high-HOX GB.


## Methods

### Cell Culture
  Patient-derived glioblastoma sphere (GS) lines LN-2540GS (RRID: CVCL_WS28), LN-2669GS (CVCL_WS29), and LN-2683GS (CVCL_WS30) were established, molecularly characterized, and authenticated in our laboratory following institutional ethics guidelines (Brain Tumor Biobank BB 031_BBLBGT, CER-VD protocol F25/99); and cultured under stem cell conditions.19,24,25 The GS lines were re-authenticated in 2025. HEK293T cells were maintained in DMEM with Glutamax and 5% FBS. All lines were regularly tested for mycoplasma. The BETi JQ1 (APExBIO, No. A1910) was used at the indicated concentrations. Additional details are available in the Supplementary Methods.


### Plasmid Preparation and Molecular Cloning
  Tet-ON inducible HOXA10-tGFP expression constructs were made and transduced into the GS lines. In brief, the HOXA10-tGFP insert was PCR-amplified from pCMV6-AC-HOXA10-tGFP and cloned into a modified pCW22-Cas9-Blast vector through In-Fusion Snap Assembly (Takara Bio Inc., 638948). Constructs were verified by sequencing. Primer sequences are listed in Table S1, and additional details can be found in the Supplementary Methods.


### Lentiviral Particle Production and Transduction
  Inducible short-hairpin (sh)RNA constructs targeting HOXA10 (shHOXA10#2 and shHOXA10#5) and a non-targeting control (shNTC) were obtained from Horizon Discovery. Lentiviral particles were produced in HEK293T cells, concentrated, and used to transduce GS lines as described in the Supplementary Methods. Transduced cells were selected with puromycin (shRNA) or blasticidin (ectopic HOXA10-tGFP). Additional information on shRNA constructs is provided in Table S2.


### Proliferation Assay
  Cell proliferation was assessed using the CyQUANT Direct Red Cell Proliferation Assay (Invitrogen, C35013). Cells were seeded in a black, clear-bottom 96-well plate (Costar, 3603) and treated the following day with DMSO, 0.5 µM JQ1, 0.5 µg/mL doxycycline (DOX), or combinations thereof. Fluorescence was measured on a SpectraMax iD3 plate reader after a 1-hour incubation at 37 °C and 5% CO2. Readings were taken on days 0, 4, 8, 12, and 16, with the medium and treatment replenished on day 8. GS spheroids were centrifuged at 200 × g for 2 minutes before each reading.


### β-Galactosidase Activity Assay
  Total β-galactosidase activity was measured as a senescence marker using the luminescent Beta-Glo Assay System (Promega, E4720). Cell seeding and treatment conditions were identical to those in the proliferation assay and were performed in white 96-well plates (Costar, 3917). Luminescence was measured on a SpectraMax iD3 plate reader after a 30-min incubation at RT. Signal was normalized to relative cell number by dividing the β-galactosidase signal by the corresponding relative fluorescence value from the final time point of the proliferation assay.


### Neurosphere Formation Assay
  The neurosphere formation assay was adapted from Gusyatiner et al.10 For each biological replicate, technical triplicates of shNTC, shHOXA10#2, and shHOXA10#5 transduced spheres were seeded into wells of a 24-well plate. The following day, cells were treated with DMSO, 0.5 µM JQ1, 0.5 µg/mL DOX, or a combination. Media and treatments were refreshed every 7 days. On day 21, spheres 50 µm in diameter were counted. The experiments were performed in biological triplicate.


### RNA Isolation and Real-Time Quantitative PCR (RT-qPCR) Analysis
  Total RNA isolation and qRT-PCR were performed as previously described26 using primers listed in Table S1. Expression levels were normalized to GAPDH.


### Western Blotting
  GS lines were collected by centrifugation. Westerns were performed as previously described26 and probed with primary antibodies and corresponding secondary antibodies, as detailed in Table S3.


### RNA-Seq Sample and Library Preparation, Sequencing, Preprocessing, and Pathway Analysis
  RNA-seq data from LN-2683GS spheres treated with 1 µM JQ1 or DMSO over a time course of 48 h were obtained from Gusyatiner et al10 (GEO accession number, GSE329546). For the transduced LN-2683GS (shNTC, shHOXA10#2, and shHOXA10#5) spheroids, RNA-seq was performed following DOX and JQ1 treatment. Libraries were prepared and sequenced at the Genomic Technology Facilities (GTF, University of Lausanne). Data were processed using the nf-core/rnaseq pipeline, aligned to Genome Reference Consortium Human Build 38 (GRCh38), and normalized with trimmed mean of M-values (TMM). Filtered genes (Table S4) were subjected to differential expression analysis using a generalized linear mixed model with a negative binomial distribution where construct type and replicate (batch) information are included as random intercepts. Genes with q-value ≤ 0.05 and |log2 fold-change| ≥ 0.58 were considered significant. Pathway over-representation analysis (ORA) was performed using gene sets from the nolecular signature database (MSigDB), Bonferroni-adjusted P-value ≤.05.27,28 Additional details on library preparation, sequencing, bioinformatic processing, statistical modeling, and pathway analysis are provided in the Supplementary Methods (Acc# GSE329531).


### Chromatin Immunoprecipitation
  Chromatin immunoprecipitation (ChIP)-seq data and corresponding RNA-seq data for LN-2683GS spheres treated for 2 h with JQ1 or DMSO were obtained from a previous study10 (GEO: GSE329543, GSE329544). For ChIP-seq analysis of LN-2540GS and LN-2669GS spheroids performed in this study, chromatin was prepared using the ChIP-IT Express Magnetic Chromatin Immunoprecipitation Kit (Active Motif, 53008) according to the manufacturer’s suspension cell protocol.

  For ChIP-qPCR, 7 µg of chromatin per reaction was immunoprecipitated using antibodies listed in Table S3. Enrichment at target regions (primer sequences in Table S1) was calculated as a percentage over input and fold enrichment over IgG.

  For ChIP-seq, 10 µg of chromatin was immunoprecipitated with antibodies detailed in Table S3. Libraries were prepared by the GTF (University of Lausanne) and sequenced on an AVITI Sequencer. ChIP-seq data were processed using the nf-core/chipseq pipeline (v2.0.0),29 aligned to GRCh38 with Bowtie2, and peaks were called using MACS2. CTCF data were analyzed with the sevenC R package to compute correlation-based chromatin contacts.30 Detailed protocols for ChIP-qPCR, ChIP-seq library preparation, and bioinformatic analysis are available in the Supplementary Methods (Acc #GSE329530).


### Assay for Transposase-Accessible Chromatin (ATAC)-Seq Sample and Library Preparation
  LN‑2540GS and LN‑2669GS spheroids (1 × 106 cells each) were collected and treated with DNase I (StemCell Technologies, 07900) to remove potential apoptotic artifacts. Libraries were prepared using the ATAC‑seq Kit (Active Motif, 53150) according to the manufacturer’s instructions. After tagmentation and PCR amplification, libraries were cleaned with AMPure XP beads (Beckman Coulter, A63880) using a 1.8X ratio. Tagmentation and library preparation efficiencies were then tested on a Fragment Analyzer. Sequencing was performed on an AVITI Sequencer (150‑nt paired‑end, 100 million reads/sample). Data were processed using the nf‑core/atacseq pipeline (v2.1.2), aligned to GRCh38 with Bowtie2 (v2.4.4), and peaks were called with MACS2 (v2.2.7.1). (Acc# GSE329528)


### Promoter Capture Micro-C (micrococcal nuclease-based chromatin conformation capture)
  LN-2540GS and LN-2669GS spheroids were processed by Cantata Bio (Scotts Valley, CA, USA) using the Dovetail Micro‑C (Dovetail, 20101E) and Human Pan Promoter Panel v1.0 (Dovetail, part no. CP3-PP-001) Kits, with sequencing to ∼150 million paired‑end reads. Reads were aligned to GRCh38. Contact matrices were processed using the cooler Python package and R packages HiCExperiment, HiContacts, and HiCcompare. A/B compartments were predicted using constrained K‑means in HiCDOC. Topologically Associating Domains (TADs) were identified with SpectralTAD. Differential analysis between the 2 sphere lines was performed using multiHiCcompare, with interactions tested by exact binomial tests. Detailed protocols and analysis parameters are provided in the Supplementary Methods (Acc# GSE329532).


### Illumina Methylation Data
  The DNA methylation datasets were previously published (Illumina human 450 k, GEO: GSE60274).19 The datasets corresponding to LN-2540GS and LN-2669GS were re-annotated for GRCh38 using the Illumina EPICv1 manifest. Probes with a detection P-value >.01 in >1% of samples were removed. Normalized beta-values were used for visualization.31,32


### Statistical Analysis
  All statistical analyses were performed using R (version 4.5.2) or GraphPad Prism 10. The data were analyzed with the statistical test described in the corresponding figure legends. Statistical significance was determined based on P-values, as indicated by asterisks in the figures: P ≤ .05 (*), P ≤ .01 (**), P ≤ .001 (***), and P ≤ .0001 (****). Data are presented as mean values, and error bars represent the standard deviation (SD).


## Results

### Concerted Downregulation of HOXA Dominated Stem-Cell Signature By the BETi JQ1 in High-HOX Stem-Like GB-Derived Spheres
  To identify epigenetic deregulation in GB, we analyzed RNA sequencing (RNA-seq) data from the patient-derived LN-2683GS sphere line treated with the BETi JQ1 over a 48-hour time course, as previously reported by Gusyatiner et al.10 This analysis revealed dynamic transcriptional response patterns, of which 2 showed rapid and sustained downregulation of expression.11 Among these significantly repressed gene sets, we identified the stem cell-related HOX signature that was coordinately downregulated over the time course of 4 to 48 h, illustrated in a heat map (Figure S1A). This signature is enriched for HOXA genes, comprising, but not limited to, HOXA3, HOXA5, HOXA7, HOXA9, and HOXA10, together with HOXC6, HOXD3, HOXD8, HOXD10, and the stem cell marker Prominin 1 (PROM1, CD133).16 Gene Set Enrichment Analysis (GSEA) against the GB-derived molecular signatures from Murat et al16 revealed a significant negative enrichment score for the core HOX signature (G28, P-adjusted ≤.001) following JQ1 treatment (Figure S1B).

  To place these transcriptional effects into their epigenetic context, we investigated the epigenetic landscape with focus on the HOXA region on CHR 7. The DNA methylation profile of LN-2683GS spheres closely matched that of the corresponding patient’s GB (GB 2683), emphasizing the clinical relevance of this in vitro model (Figure 1A). In untreated spheres, the HOXA cluster exhibited a permissive epigenetic configuration, characterized by focal DNA hypomethylation and broad enrichment of active histone marks (H3K27ac, H3K4me3), consistent with robust, concerted transcriptional activation (Figure 1B). BETi with JQ1 for 2 h reduced BRD4 binding and decreased binding of RNA Polymerase II (Pol2), associated with downregulation of gene expression across the entire HOXA cluster. These coordinated changes suggested that JQ1 treatment-induced rapid downregulation of HOXA cluster gene expression, indicating that the actively transcribed HOXA cluster genes are highly sensitive to BETi in this high-HOX GS line (Figure 1). In this GS line the transcriptional activation and sensitivity to BETi was also observed for the other HOX clusters, HOXB on CHR 17, HOXC on CHR 12, and HOXD on CHR 2 (Figure S2A-C).

  The JQ1 sensitivity of high-HOX GS lines to coordinated downregulation of expression was confirmed for HOXA genes in LN-2683GS and LN-2669GS. Accordingly, depletion of HOXA10 protein was observed over a 120 h time course (Figure S3).


### HOXA10 Knockdown Is Associated With the Repression of Other HOXA Genes
  Intrigued by the coordinated repression of HOXA gene cluster expression by BETi in high-HOX GS lines, we investigated whether targeting an individual gene within the locus would affect cluster-wide expression. We focused on HOXA10, whose promoter DNA methylation pattern in two GB cohorts showed one of the strongest correlations with the global HOX signature expression (our data-set and TCGA-GBM; RV coefficient of correlation matrices, 0.84; P<.001), as we reported previously.19 DOX-inducible shRNA-mediated knockdown of HOXA10 in the high-HOX GS lines LN-2683GS and LN-2669GS efficiently reduced HOXA10 mRNA and protein levels within 72 h and 120 h, respectively (Figure 2). Moreover, HOXA10 knockdown led to coordinated downregulation of other HOXA cluster genes, including HOXA5, HOXA6, HOXA7, and HOXA9, which was reproduced in LN-2669GS. The effect of coordinated downregulation by shRNA targeting HOXA10 was comparable to that of JQ1 treatment. Notably, combining HOXA10 knockdown with JQ1 treatment did not further reduce HOXA gene expression relative to either perturbation alone, as reflected also in similar depletion of the HOXA10 protein levels within 120 h.


### HOXA10 Knockdown Reduces Proliferation, Self-Renewal Capacity, and Induces a Senescence-Like Phenotype
  Next, we determined the functional consequences of HOXA10 downregulation in the high-HOX GS lines. DOX-induced HOXA10 knockdown significantly reduced cellular proliferation over 16 days in both LN-2683GS and LN-2669GS (Figure 3A). Likewise, the neurosphere formation assays revealed reduction in secondary sphere formation in the range of 50% after 21 days of HOXA10 knockdown, indicating a substantial loss of self-renewal capacity (Figure 3B). The reduction of these biological features associated with malignancy was accompanied by induction of a senescence-like phenotype, evidenced by a 4- and 2-fold increase in β-galactosidase activity after 16 days in LN-2683GS and LN-2669GS, respectively (Figure 3C). In accordance, decrease of the senescence-associated biomarker Lamin B1 (LMNB1) was observed at both the mRNA and protein levels within 3 and 5 days of HOXA10 knockdown, respectively (Figure 3D and E). These phenotypic changes mirrored those induced by BETi (JQ1), while no additive reduction was observed in combination, suggesting that HOXA10 operates within the BET-dependent transcriptional network rather than independently.


### Ectopic HOXA10 Expression Is Insufficient to Activate the HOX Transcriptional Program or Counteract BETi
  To assess whether HOXA10 is sufficient to drive expression of the HOX gene signature, we introduced DOX-inducible ectopic HOXA10-tGFP expression into low- and high-HOX GS lines. Ectopic expression of HOXA10 had no effect on transcription of other HOXA genes in the low-HOX GS line LN-2540GS (Figure S3) nor in the high-HOX GS lines LN-2669GS and LN-2683GS that are “wired” to express HOX genes (Figure S5). Moreover, the ectopic expression of HOXA10 in the two high-HOX GS lines was neither able to rescue cell growth, nor to prevent induction of the senescence-like phenotype upon JQ1 treatment. These findings indicate that ectopic HOXA10 expression alone is insufficient to reestablish the HOX signature transcriptional program or to counteract BETi-induced effects.


### Transcriptomic Profiling After HOXA10 Depletion Reveals Repression of Stemness and Induction of Neural-Like Transcriptional Signatures
  To characterize the transcriptional consequences of HOXA10 depletion, we performed RNA sequencing on LN-2683GS spheres 5 days after induction of shHOXA10, or after 5 days of JQ1 treatment, when depletion of the HOXA10 protein is observed (Figure 2).

  Analysis of the JQ1 response revealed that prolonged BETI induced widespread transcriptional reprogramming, confirming consistent transcriptional changes in key pathways after 5 days, extending beyond the previously described observation interval.10,11 Expression changes following the knockdown by shHOXA10 at the time of HOXA10 depletion were more limited. Differential expression analysis identified 233 significantly altered genes (differentially expressed genes, DEGs; 194 upregulated and 39 downregulated using a generalized linear mixed model (Bonferroni, P ≤ .05; |logFC| > 0.58) (Table S4). Overrepresentation analysis (ORA) of cancer-related signatures (MSigDB H and C2) revealed enrichment of 8 pathways associated with stemness, differentiation, and extracellulat matrix (ECM) organization—all of which overlapped with the 229 JQ1-affected pathways (Figure 4A), which in addition were already present after 48 h of treatment. Interestingly, top pathways identified by ORA using Gene Ontology signatures (C5: GO_BP and C5: GO_CC) showed significant enrichment for 6 pathways, of which 4 were unique to HOXA10 depletion, and associated with neuronal differentiation, axonogenesis, and synaptic signaling programs (Figure 4B; Table S5). We compiled a prioritized shortlist of candidate genes from the RNA-seq data for validation. Selection was based on fold-change (logFC) in significant DEGs, their consistent contribution to enriching stemness and neuronal differentiation signatures, and their baseline expression levels in the GS lines. This yielded a panel of genes with established roles in neural development or GB biology, including downregulation of the stemness-associated gene Distal-Less Homeobox 1 (DLX1),33 alongside induction of genes with established neurogenic functions, including the transcription factor Neuronal Differentiation 1 (NEUROD1),34,35 the tumor suppressor KLF Transcription Factor 9 (KLF9),36,37 the neuronal markers L1 Cell Adhesion Molecule (L1CAM)38,39 and the Synaptosome Associated Protein 25 (SNAP25)40 (Figure 4C). These genes were absent from those differentially expressed after short-course JQ1 exposure, indicating that they likely correspond to secondary effects of HOXA10 loss that are not captured as early transcriptional responses to BETi.


### Local Organization of Chromatin Architecture, Histone Modifications at Regulatory Regions of the HOXA Locus in High-HOX Spheres
  To explore whether the transcriptional activation of the HOXA cluster in high-HOX GB is linked to differences in chromatin structure, we characterized and compared the epigenetic landscape in the low-HOX LN-2540GS and high-HOX LN-2669GS GS lines at several hierarchical levels of chromatin organization.

  We investigated 3-dimensional chromatin structure using promoter capture Micro-C. Compartmentalization of CHR 7 into A/B assigned the HOXA locus to the B compartment (at 516 kb resolution) in both LN-2540GS and LN-2669GS, like most of the distal part of CHR 7p, including the locus of the gene encoding the epidermal growth factor receptor (EGFR) (Figure S6A). Of note, both GS lines display classic GB hallmarks of gain of CHR 7 and loss of CHR 10, based on 450 k data. No major differences were apparent in higher-order chromatin organization. Differential analysis of significant local interactions on CHR 7 revealed a peak at the HOXA locus and at the EGFR locus, with opposite signs in the 2 GS lines. This is in accordance with the known amplified EGFR locus of the low-HOX GS line LN2540GS (Figure S6B).

  At the level of TADs, at 64 kb and 32 kb resolution, the HOXA locus was located at the intersection of 2 TADs (Figure 5A). Local interactions within the HOXA region were increased in the high-HOX LN-2669GS (Figure 5A). Furthermore, these areas, spanning the HOXA1-HOXA3 and HOXA9-HOXA10 regions, were associated with enhanced chromatin accessibility in the high-HOX GS line, based on ATAC-seq coverage (Figure 5B). The coverage of CTCF ChIP-seq identified some differences in detected CTCF peaks at the 5’ end of the HOXA region (#8) or outside (#9) in the high-HOX LN-2669GS that were absent in the low-HOX GS line or vice versa, suggestive of distinct, unique loops linking these CTCF peaks (#8, #9) to upstream HOXA regions (3’). LN-2669GS showed unique ATAC-seq enrichment across multiple regions of the HOXA cluster, concordant with the regions corresponding to sites of increased chromatin interactions identified by Micro-C. The significant differences (fold changes) of these interactions between the GS lines are illustrated for the extended HOXA region in Figure 5C (locations summarized in Table S6). Differences also appeared for contacts linking HOXA promoters to the gene encoding the Src kinase-associated phosphoprotein 2 (SKAP2) (250-350 kb) at the 3′ TAD boundary of the HOXA region that is part of the GB-associated HOX signature. In concordance, these regions with increased interactions exhibited open chromatin (ATAC) and enrichment of H3K27ac and H3K4me3 coverage, suggesting activated regulatory elements across the HOXA cluster in the high-HOX spheres. Moreover, enhancer classification suggested that a large part of the HOXA cluster, from HOXA1 to HOXA9, was associated with super-enhancer activity, along with sharp promoter-proximal peaks for H3K27ac and H3K4me3. The corresponding DNA CpG methylation patterns of the 2 GS lines aligned with the respective activated or silenced state of the HOXA regions (Figure 5B).


### Epigenetic Landscape of Other HOX Clusters Contributing to the High-HOX Signature
  To set the dominating contribution of the HOXA cluster into context of the overall HOX signature, the local epigenetic landscapes were visualized for the other HOX clusters (HOXC, CHR 12q; HOXD, CHR 2q; HOXB, CHR 17q). They contribute to varied degrees to the hematopoietic stem-like expression signature of high-HOX GB. Differential analyses of the high-HOX LN-2669GS versus the low-HOX LN-2540GS revealed the highest activity in the HOXC cluster, with concordant open chromatin (ATAC), active marks (H3K27ac) classifying as super-enhancers, and focal Cytosine-phosphate-Guanine (CpG) hypomethylation. We observed limited activity in the HOXD cluster, without super-enhancer formation. Basically, no activity was observed in the HOXB cluster, which does not contribute to the core HOX signature. These observations are in line with their distinct contributions to the expression of the core HOX signature (Figure S7A [HOXC]; B [HOXD]; C [HOXB]). However, in the high-HOX GS line LN-2683GS, the other HOX clusters showed higher activity (Figure 1, Figure S2A-C), reflecting intertumoral heterogeneity.


### Activation of the Canonical and Alternative HOXA10 Promoter in the High-HOX GS Line
  Based on our previous findings that attributed a special role of HOXA10 in the activation of the overall HOX signature in GB, we investigated the canonical and alternative HOXA10 promoters in LN-2540GS and LN-2669GS by ChIP-qPCR (Figure S8). Enrichment of active histone marks (H3K27ac, H3K4me3, and H3K9ac) was significantly higher at both promoter regions in the high-HOX LN-2669GS than in LN-2540GS, with more pronounced differences (fold change, FC) at the canonical promoter. In accordance, enrichment of the repressive mark H3K27me3 was significantly lower in LN-2669GS across most promoter regions examined. These data confirm, at single-promoter resolution, that both the canonical and alternative HOXA10 promoters are epigenetically active in the high-HOX GS line.


## Discussion
  Aberrant activation of a hemopoietic stem cell-like transcriptional program, dominated by HOXA genes, is a characteristic feature of a subset of GB. The association of a gene dosage effect on CHR 7 and escape from compensatory hypermethylation was hypothesized as an underlying driver of dysregulation of HOXA genes.19 In this research, we reveal the epigenetic landscape in the HOXA region associated with this coordinated, activated transcriptional program in the high-HOX GB-derived sphere models. Functional perturbation experiments using pharmacologic interference with the epigenetically regulated transcriptional machinery via BETi revealed coordinated repression of the entire HOX signature. This was associated with reduced BRD4 occupancy and reduced Pol II binding. We observed profound effects in high-HOX GS lines, reducing proliferation and self-renewal capacity and inducing a senescence-like phenotype. Most interestingly, we observed similar biological changes when we genetically perturbed the transcriptional program by targeting HOXA10 alone. However, reduced cell proliferation and induction of a senescence-like phenotype are common stress responses.

  Investigating the HOXA cluster with multi-layered epigenomic profiling of high- and low-HOX GS lines revealed a permissive chromatin landscape in high-HOX lines with distinct CTCF loops and increased chromatin interactions within the extended HOXA region. Alterations in CTCF binding have been linked to cancer-related enhancer rewiring.14,41,42 However, at a higher level of 3D chromatin organization, we observed no major differences.

  The HOXA cluster is a gene- and CpG island-rich region and forms a super-enhancer in the high-HOX GS line (spanning HOXA1 to HOXA9) (Figure S5). Interestingly, the active HOXA10 is at the 5’ end of this super-enhancer. A special role has been attributed to HOXA10, as hypomethylation at its promoter showed the highest correlation with expression of the high-HOX signature in GB.19 Interference with HOXA10 expression by shRNAs was sufficient to repress cluster-wide activity of other HOXA genes, and phenocopied JQ1-mediated biological effects, reducing proliferation, self-renewal capacity and induction of a senescence-like phenotype. However, ectopic expression neither activated other HOXA genes in low-HOX GS nor rescued high-HOX GS cells from JQ1-mediated biological effects. This suggests that the regulatory context of endogenous HOXA10 expression is mechanistically important for the activity of the HOX signature. The regulatory context governing the coordinated dysregulation of HOX genes across the 4 distinct HOX clusters (A, C, D, B) located on different CHRs remains unclear. However, their variable contribution to the core HOX signature derived from a GB cohort, dominated by HOXA genes, was well aligned with their local epigenetic landscapes, explaining the distinct activation levels and respective transcripts of the signature in the GS line LN-2669GS. These observations further emphasize the dominant role of the HOXA locus, which is associated with a super-enhancer that encompasses the entire region of the expressed HOXA genes. A recent review on HOX gene dysregulation in GB highlighted the importance of the HOXA cluster, reporting higher expression levels and a stronger correlation with progression and prognosis.43

  Interindividual heterogeneity among GB, exemplified by LN-2683GS, may also present higher transcriptional activity in other HOX clusters, including HOXB, which does not contribute to the core GB-derived HOX signature. The high correlation of HOX gene expression in high-HOX GB precludes determination of their individual functional contribution to worse prognosis and response to therapy.12,16,17,20,44 This association can be reproduced in GB using nuclear HOXA10 expression (immunohistochemistry) as a surrogate biomarker.16

  Cluster-wide regulation is a defining feature of HOX loci during development outside the forebrain, where shared regulatory elements, chromatin looping, and coordinated epigenetic remodeling enable synchronized gene expression.45 Although HOX genes are not expressed in the development of the forebrain or the adult brain, the adoption of this aberrant concerted activation of the hemopoietic stem cell-related HOX signature in GB highlights the stem-like tumor state,13,15,16,19 in line with the reported loss of the repressive mark H3K27me3 across the 4 HOX clusters.20

  BETi rapidly suppressed cluster-wide expression, a change associated with decreased RNA Polymerase II occupancy, without concurrent alterations in histone modifications associated with active chromatin marks. This aligns with Crump et al,46 who reported that BETi disrupts transcription while enhancer-promoter contacts remain intact, concluding that these are separable events and that high-level BRD4 binding is not required to maintain these interactions. This dissociation indicates that BET proteins are not necessary to establish the potential for transcription—unlike the open chromatin and enhancer landscape—but are essential for maintaining transcription at active loci.5,6,47 Furthermore, BRD4 binding is essential for active super-enhancer function, which can activate transcription of associated proto-oncogenes and maintain oncogenic identity.48 Super-enhancers have been associated with the formation of loops, interchromosomal interactions, and higher-order hubs.49 The dependence on this continuous activation presents a potentially druggable vulnerability.

  Genetic interference with shRNAs targeting HOXA10 expression, a key component of the HOXA cluster, recapitulated the effects of BETi with similar functional outcomes and shared transcriptional programs. In particular, HOXA10 knockdown affected pathways regulating stemness, differentiation, and ECM organization, as well as neuronal differentiation markers such as NEUROD1, KLF9, and L1CAM.

  A key insight from this work is that the permissive landscape in high-HOX cells is defined by “local” coordinated epigenetic organization, comprising focal DNA hypomethylation, broad H3K27ac and H3K4me3 domains, and increased chromatin accessibility, associated with increased promoter-centered looping, especially in the HOXA1-HOXA3 and HOXA9-HOXA10 regions. In contrast, at a higher structural level, most of the distal part of CHR 7p, encompassing the HOXA cluster and the EGFR gene, was assigned to the B compartment that is associated with condensed chromatin (heterochromatin) and considered transcriptionally inactive.50 No difference in the compartmentalization of this genomic region was observed between the high- and low-HOX GS line. Current efforts aim to identify higher-order structural epigenetic alterations (3D), including compartment switching, that may give rise to new interactions and uncover druggable vulnerabilities in GB.51,52 Yet, local rewiring without compartment switching has been recognized as a mechanism for inactivating repression of proto-oncogenes in cancer.53,54

  These findings identify potentially targetable vulnerabilities with important therapeutic implications. They support using BETi to disrupt the HOX-driven stem-like state while also complementing their known roles in repressing other programs relevant to GB,7,55 including interferon signaling, MGMT expression, and deregulation of “Histone Deacetylase (HDAC) targets”—associated pathways. The latter 2 show additive or synergistic effects when combined with TMZ or an HDAC inhibitor, respectively.10,11 However, the similarities observed in phenotypes induced by HOXA10 knockdown and BETi, without an additive effect when combined, suggest that aberrant activation of the HOX signature acts within a broader BET-dependent regulatory context in high-HOX GB. HOX signature expression may be a useful biomarker for patient stratification in future epigenetic therapy trials or HOX-targeted therapies.18,43 Our data provide a mechanistic rationale for strategies such as BETi or other epigenetic drugs that induce vulnerabilities by destabilizing the epigenetic framework, thereby abrogating the stem-like state and possibly rendering cells more susceptible to differentiation or synergistic combination therapies.


## Supplementary Material

## Supplementary Material
  Supplementary material is available online at Neuro-Oncology Advances (https://academic.oup.com/noa).


## Author Contributions
  Conception and design: Monika E. Hegi, Davide Chiesi, and Pierre Bady; Acquisition of data (experimental data) (Davide Chiesi, Mihalis V. Xirouchakis, Carla Mendes Ferreira, and Kedir S. Mohammed); Analysis and interpretation of data Davide Chiesi, Pierre Bady, Monika E. Hegi, Mihalis V. Xirouchakis, Carla Mendes Ferreira, and Kedir S. Mohammed; Computational biology and biostatistics, and Pierre Bady; Manuscript writing: Davide Chiesi, Monika E. Hegi, and Pierre Bady; Review, and/or revision of the manuscript: all coauthors. Study supervision: Monika E. Hegi.


## Conflict of Interest Statement
  All authors report no competing conflict of interest.


## Funding
  This study was funded by the Swiss National Science Foundation (320030_215718 to M.E.H.). C.M.F. was supported by the Lundin Family Brain Tumor Center.


## Ethics Approval Statement
  Patient-derived glioblastoma sphere (GS) lines LN-2540GS (RRID: CVCL_WS28), LN-2669GS (RRID: CVCL_WS29), and LN-2683GS (RRID: CVCL_WS30) were established, molecularly characterized and authenticated in our laboratory following institutional ethics guidelines (Brain Tumor Biobank BB 031_BBLBGT, approved by the ethics committee of the canton de Vaud, Switzerland, CER-VD, protocol F25/99).


## Data Availability
  The datasets are available at the Gene Expression Omnibus (ncbi.nlm.nih.gov/geo/).


### Datasets (This Study)
  RNA-seq (LN-2683GS, transduced) GSE329531; ChIP-seq (LN-2669GS, LN-2540GS) GSE329530; ATAC-seq (LN-2669GS, LN-2540GS) GSE329528; microC (LN-2669GS, LN-2540GS) GSE329532.


### Previously Described Datasets
  Hu 450 k methylation data, GEO6027419; RNA-seq (LN-2683GS, BETi time course) GSE32954610,11; RNA-seq (LN-2683GS; associated with ChIP-seq) GSE32954410; ChIP-seq LN-2683GS; GSE329543.10


## Acknowledgments
  We thank the collaborators at the Genomic Technology Facility (GTF) of the University of Lausanne for their excellent technical support. The graphical abstract was partly Created in BioRender. Chiesi, D. (2026) https://BioRender.com/eknk0ez