## Does a map-level insulation constraint improve sequence-based prediction of 3D genome folding? A Stage 1 Registered Report with a reverse-complement-equivariant state-space model (HiFold-Mamba)


## Abstract

Background. Sequence-to-contact-map models are trained with pixel-wise losses, although the features of interest (insulation, domain boundaries, loops) are summaries of the map. Insulationbased losses help Hi-C resolution enhancement. No pre-specified test has asked whether they improve sequence-based prediction, judged against annotations independent of the training data. Proposed study. HiFold-Mamba predicts 448 × 448 maps at 2,048 bp from 1,048,576 bp of DNA on the DNALongBench contact-map task. Every component is reverse-complement-equivariant: convolutional tower, bidirectional Mamba blocks, multi-scale mixer and symmetric pairwise head. We pre-register three hypotheses: » H1: it exceeds each of three trained baselines (reproduced Akita, a parameter-matched Transformer and a parameter-matched CNN) by ≥0.01 stratum-adjusted correlation (SCC). » H2: an insulation and boundary loss, computed from the predicted map with the operator used on the observed map, improves boundary AUROC and loop AP against independent 4DN boundary calls and ENCODE CTCF ChIA-PET loops, at equal training steps and without loss of SCC. » H3: pretraining plus few-shot adaptation beats training from scratch on four held-out cell lines.Tests use a paired bootstrap over 237 one-megabase test blocks (one-sided α = 0.025). Pilot data. » Verification. The benchmark target, the window coordinates and the networks equivariance were verified. » Locus-shared reference. Copying other cell lines measured maps at the same locus matches published Akita on the benchmarks SCC (0.227 vs. 0.230). » SCC weightings. Two weightings in common use weight distance strata in opposite directions and agree only moderately (ρ = 0.54). » Comparison rule. In simulations calibrated on the pilot data, a per-block-best comparison against several baselines has no power. We therefore test against each baseline, which gives ≥ 90 % power at a true gain of 0.02 when between-model correlation is ≥ 0.95. » H2 positive control. On validation windows, observed maps recover the independent boundaries (AUROC 0.61 − 0.91) and loops (0.86 − 0.90). This fixed the insulation window and showed that these annotations are largely shared across cell types.


## Competing Interest Statement

The authors have declared no competing interest.


## Footnotes

https://github.com/malekpouri/HiFold-Mamba

Thank you for your interest in spreading the word about bioRxiv.

NOTE: Your email address is requested solely to identify you as the sender of this article.


## Citation Manager Formats


## Subject Area