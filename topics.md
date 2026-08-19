---
title: Topics
---

# Topics and resources

This list is **tentative**. The topics are reasonably firm but we may reorder or drop some. The papers listed under each topic are likely to change and are just shown to give a sense for the topic.

[Back to the course page](index.html)

---

## 1. Supervised learning in science: property prediction

Classical supervised learning methods applied to important problems in science. While these methods are becoming more classical, they are still important.

- *Neural Message Passing for Quantum Chemistry* (ICML 2017) — [arXiv:1704.01212](https://arxiv.org/abs/1704.01212)
- Heid et al., *Chemprop: A Machine Learning Package for Chemical Property Prediction*, J. Chem. Inf. Model. — [doi:10.1021/acs.jcim.3c01250](https://doi.org/10.1021/acs.jcim.3c01250)
- Dunn et al., *Benchmarking materials property prediction methods: the Matbench test set*, npj Comput. Mater. 2020 — [doi:10.1038/s41524-020-00406-3](https://doi.org/10.1038/s41524-020-00406-3)

## 2. Computer vision and inverse problems in characterization

Recovering structure from measurements. Cryo-EM reconstruction and diffusion-prior methods for inverse problems are the same problem viewed two ways.

- Zhong et al., *CryoDRGN: reconstruction of heterogeneous cryo-EM structures using neural networks*, Nature Methods 2021 — [doi:10.1038/s41592-020-01049-4](https://doi.org/10.1038/s41592-020-01049-4)
- *InverseBench: Benchmarking Plug-and-Play Diffusion Priors for Inverse Problems in Physical Sciences* (ICLR 2025) — [arXiv:2503.11043](https://arxiv.org/abs/2503.11043)

## 3. Machine-learned interatomic potentials

- *E(3)-equivariant graph neural networks for data-efficient and accurate interatomic potentials* (NequIP), Nature Communications 2022 — [doi:10.1038/s41467-022-29939-5](https://doi.org/10.1038/s41467-022-29939-5)
- *MACE: Higher Order Equivariant Message Passing Neural Networks for Fast and Accurate Force Fields* (NeurIPS 2022) — [arXiv:2206.07697](https://arxiv.org/abs/2206.07697)
- *A foundation model for atomistic materials chemistry* (MACE-MP-0) — [arXiv:2401.00096](https://arxiv.org/abs/2401.00096)
- Dataset: *Open Materials 2024 (OMat24)* — [arXiv:2410.12771](https://arxiv.org/abs/2410.12771)

## 4. Protein language models and structure prediction

- Jumper et al., *Highly accurate protein structure prediction with AlphaFold*, Nature 2021 — [doi:10.1038/s41586-021-03819-2](https://doi.org/10.1038/s41586-021-03819-2)
- *Evolutionary-scale prediction of atomic-level protein structure with a language model* (ESMFold), Science 2023 — [doi:10.1126/science.ade2574](https://doi.org/10.1126/science.ade2574)
- Abramson et al., *Accurate structure prediction of biomolecular interactions with AlphaFold 3*, Nature 2024 — [doi:10.1038/s41586-024-07487-w](https://doi.org/10.1038/s41586-024-07487-w)
- Hayes et al., *Simulating 500 million years of evolution with a language model* (ESM3), Science 2025 — [doi:10.1126/science.ads0018](https://doi.org/10.1126/science.ads0018)

## 5. Generative models for chemical and materials design

- Watson et al., *De novo design of protein structure and function with RFdiffusion*, Nature 2023 — [doi:10.1038/s41586-023-06415-8](https://doi.org/10.1038/s41586-023-06415-8)
- Zeni et al., *A generative model for inorganic materials design* (MatterGen), Nature 2025 — [doi:10.1038/s41586-025-08628-5](https://doi.org/10.1038/s41586-025-08628-5)
- *Simple and Effective Masked Diffusion Language Models* (NeurIPS 2024) — [arXiv:2406.07524](https://arxiv.org/abs/2406.07524) — Kuleshov group, Cornell Tech
- *Discrete Diffusion Modeling by Estimating the Ratios of the Data Distribution* (SEDD, ICML 2024) — [arXiv:2310.16834](https://arxiv.org/abs/2310.16834)

ESM3 (above) also belongs here — it trains and samples with masked diffusion.

## 6. Uncertainty quantification, active learning, and Bayesian optimization

- Frazier, *A Tutorial on Bayesian Optimization* — [arXiv:1807.02811](https://arxiv.org/abs/1807.02811)
- Hirschfeld et al., *Uncertainty Quantification Using Neural Networks for Molecular Property Prediction*, J. Chem. Inf. Model. 2020 — [doi:10.1021/acs.jcim.0c00502](https://doi.org/10.1021/acs.jcim.0c00502)

## 7. LLMs for black-box optimization

- *AlphaEvolve: A coding agent for scientific and algorithmic discovery* — [arXiv:2506.13131](https://arxiv.org/abs/2506.13131)
- *Generalists vs. Specialists: Evaluating LLMs on Highly-Constrained Biophysical Sequence Optimization Problems* (LLOME) — [arXiv:2410.22296](https://arxiv.org/abs/2410.22296)

## 8. Self-driving labs

- Gongora et al., *A Bayesian experimental autonomous researcher for mechanical design* (BEAR), Science Advances 2020 — [doi:10.1126/sciadv.aaz1708](https://doi.org/10.1126/sciadv.aaz1708) — Keith Brown's group
- Burger et al., *A mobile robotic chemist*, Nature 2020 — [doi:10.1038/s41586-020-2442-2](https://doi.org/10.1038/s41586-020-2442-2)
- Szymanski et al., *An autonomous laboratory for the accelerated synthesis of inorganic materials* (A-Lab), Nature 2023 — [doi:10.1038/s41586-023-06734-w](https://doi.org/10.1038/s41586-023-06734-w)
- Leeman et al., *Challenges in High-Throughput Inorganic Materials Prediction and Autonomous Synthesis*, PRX Energy 2024 — [doi:10.1103/PRXEnergy.3.011002](https://doi.org/10.1103/PRXEnergy.3.011002) — the critique of A-Lab; read the two together

## 9. Agents for science

- Boiko et al., *Autonomous chemical research with large language models* (Coscientist), Nature 2023 — [doi:10.1038/s41586-023-06792-0](https://doi.org/10.1038/s41586-023-06792-0)
- *Language agents achieve superhuman synthesis of scientific knowledge* (PaperQA2) — [arXiv:2409.13740](https://arxiv.org/abs/2409.13740)

## 10. Neural surrogates for simulation: PINNs, neural operators, and weather

Three ways to put a neural network where a solver used to be, and they are not interchangeable. A
PINN puts the physics in the loss and solves one problem instance. A neural operator learns the
solution map across instances from data. A weather model replaces an entire operational pipeline.
Weather is the clearest case of AI displacing mature physics-based software in production, which
makes it the right place to ask what made that domain tractable when others have not been.

**Physics-informed neural networks**

- Raissi et al., *Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear PDEs*, J. Comput. Phys. 2019 — [doi:10.1016/j.jcp.2018.10.045](https://doi.org/10.1016/j.jcp.2018.10.045)
- Karniadakis et al., *Physics-informed machine learning*, Nature Reviews Physics 2021 — [doi:10.1038/s42254-021-00314-5](https://doi.org/10.1038/s42254-021-00314-5)
- *Characterizing possible failure modes in physics-informed neural networks* (NeurIPS 2021) — [arXiv:2109.01050](https://arxiv.org/abs/2109.01050)
- McGreivy & Hakim, *Weak baselines and reporting biases lead to overoptimism in machine learning for fluid-related partial differential equations*, Nature Machine Intelligence 2024 — [doi:10.1038/s42256-024-00897-5](https://doi.org/10.1038/s42256-024-00897-5)

**Neural operators**

- *Fourier Neural Operator for Parametric Partial Differential Equations* — [arXiv:2010.08895](https://arxiv.org/abs/2010.08895)

**Weather**

- Lam et al., *Learning skillful medium-range global weather forecasting* (GraphCast), Science 2023 — [doi:10.1126/science.adi2336](https://doi.org/10.1126/science.adi2336)
- Price et al., *Probabilistic weather forecasting with machine learning* (GenCast), Nature 2024 — [doi:10.1038/s41586-024-08252-9](https://doi.org/10.1038/s41586-024-08252-9)

## 11. Extracting information from the literature

- Dagdelen et al., *Structured information extraction from scientific text with large language models*, Nature Communications 2024 — [doi:10.1038/s41467-024-45563-x](https://doi.org/10.1038/s41467-024-45563-x)
