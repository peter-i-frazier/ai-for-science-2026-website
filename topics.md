---
---

<!-- ===================================================================
     STATUS 2026-08-23 -- READ BEFORE PUBLISHING

     Much of what follows is a PROPOSAL and has NOT been vetted by Peter.

     Provenance is marked per entry. Three kinds:

       [ON PAGE]  Was already on this page before 2026-08-23. Kept as-is.
       [DECK]     Lifted from a built deck in ai-for-science-2026-content
                  (slides/agents-for-science, /language-models,
                  /reasoning-and-tools, /diffusion). Peter chose these when
                  he wrote the deck, so they carry his judgement, but the
                  citation strings have not been re-resolved against DOI or
                  arXiv to confirm title, authors, venue and year.
       [PROPOSED] Claude's suggestion. NOT vetted. Verify before teaching.

     None of the DOIs or arXiv IDs on this page have been resolved and
     checked in this pass. Per CLAUDE.md, a paper's presentation category
     should be checked against the venue's own listing, not the authors'
     page. That check has not been done.

     Structure follows the schedule sheet (the source of truth):
     https://docs.google.com/spreadsheets/d/158I6-Nc0zjxo6BdEY-lMmk8-NmfgePybDzavtb3v0TE/edit

     TOPIC NUMBERS ARE LOAD-BEARING -- DO NOT RENUMBER.
     slides/agents-for-science cross-references "topic 9" and "topic 11" by
     number, and slide 10 of slides/day-1/day-1.md lists topics 1-12.
     Renumbering here silently breaks both.
     =================================================================== -->

# Topics

Papers here show what each topic covers. **The list is provisional and still being built out ---
the reading for each session is announced beforehand.** Topics are reasonably firm; we may still
reorder or drop some.

---

## 1. Supervised learning in science

**Taught:** molecular representations, Fri Sep 4 · graph neural networks, Wed Sep 9 -- Fri Sep 11.

Classical supervised learning applied to problems in science. Becoming classical, still important.

<!-- [ON PAGE] all four below. Two papers previously filed here have moved:
     Ahlmann-Eltze to topic 5, and FLIP2 + Tang et al. to topic 4 -- they are
     protein/genomic benchmark papers and belong with the PLM unit. -->
- *Neural Message Passing for Quantum Chemistry* (ICML 2017) — [arXiv:1704.01212](https://arxiv.org/abs/1704.01212)
- Heid et al., *Chemprop: A Machine Learning Package for Chemical Property Prediction*, J. Chem. Inf. Model. — [doi:10.1021/acs.jcim.3c01250](https://doi.org/10.1021/acs.jcim.3c01250)
- Dunn et al., *Benchmarking materials property prediction methods: the Matbench test set*, npj Comput. Mater. 2020 — [doi:10.1038/s41524-020-00406-3](https://doi.org/10.1038/s41524-020-00406-3)

<!-- [PROPOSED] NOT VETTED. The unit teaches scaffold-vs-random splits and weak
     baselines as its central critique (units/06.md), and HW1 asks students to
     reproduce that gap, but no paper on this page makes that argument for
     molecular property prediction. Errica et al. is the standard citation for
     "GNN comparisons are unfair"; Peter has referred to it as "Errica" in
     schedule-draft.md but never with a full citation. Confirm this is the
     intended paper and check the venue listing before use. -->
- Errica, Podda, Bacciu, Micheli, *A Fair Comparison of Graph Neural Networks for Graph Classification*, ICLR 2020 — [arXiv:1912.09893](https://arxiv.org/abs/1912.09893)

## 2. Agents for science

**Taught:** Wed Oct 14 -- Fri Oct 23, five sessions.

<!-- [DECK] The whole of this topic comes from the "Reading for this unit" slide
     of slides/agents-for-science/agents-for-science.md, which assigns papers
     session by session. Previously this page listed only Coscientist and
     PaperQA2 for what is the largest unit in the course. -->

Session by session:

1. **ChemCrow** — Bran, Cox, Schilter, Baldassari, White, Schwaller, *Augmenting large language models with chemistry tools*, Nature Machine Intelligence 6, 2024 — [doi:10.1038/s42256-024-00832-8](https://doi.org/10.1038/s42256-024-00832-8) — where tools carry the chemistry
2. **Coscientist** — Boiko, MacKnight, Kline, Gomes, *Autonomous chemical research with large language models*, Nature 624, 2023 — [doi:10.1038/s41586-023-06792-0](https://doi.org/10.1038/s41586-023-06792-0) — where the loop touches hardware
3. **Co-Scientist** — Gottweis, Weng, Daryin et al., *Accelerating scientific discovery with Co-Scientist*, Nature 2026 — [doi:10.1038/s41586-026-10644-y](https://doi.org/10.1038/s41586-026-10644-y), preprint [arXiv:2502.18864](https://arxiv.org/abs/2502.18864) · and **Robin** — Ghareeb et al. (FutureHouse), *A multi-agent system for automating scientific discovery*, Nature 2026 — [doi:10.1038/s41586-026-10652-y](https://doi.org/10.1038/s41586-026-10652-y)
4. **Kosmos** — Edison Scientific, *Kosmos: An AI Scientist for Autonomous Discovery*, Nov 2025 — [arXiv:2511.02824](https://arxiv.org/abs/2511.02824) — end to end on data
5. **Kirgis et al.**, *Can AI agents conduct open-ended AI research? Early evidence from two case studies*, July 2026 — [arXiv:2607.27191](https://arxiv.org/abs/2607.27191) · and the **ideation-execution gap** — Si, Hashimoto, Yang, 2025 — [arXiv:2506.20803](https://arxiv.org/abs/2506.20803)

Session 5 is this topic's celebrated-result-versus-critique pairing.

**Background, optional**

- *Language agents achieve superhuman synthesis of scientific knowledge* (PaperQA2) — [arXiv:2409.13740](https://arxiv.org/abs/2409.13740) <!-- [ON PAGE] -->
- **Sakana AI Scientist** — Lu, Lu, Lange, Foerster, Clune, Ha, Nature, March 2026 — [doi:10.1038/s41586-026-10265-5](https://doi.org/10.1038/s41586-026-10265-5), v2 [arXiv:2504.08066](https://arxiv.org/abs/2504.08066) <!-- [DECK] -->
- Kapoor, Stroebl, Narayanan et al., *AI Agents That Matter* — [arXiv:2407.01502](https://arxiv.org/abs/2407.01502) — skim before session 5 <!-- [DECK] -->
- Si, Yang, Hashimoto, ICLR 2025 — [arXiv:2409.04109](https://arxiv.org/abs/2409.04109) — the ideation study that everyone cited <!-- [DECK] -->
- Wei et al., *From AI for Science to Agentic Science* — [arXiv:2508.14111](https://arxiv.org/abs/2508.14111) — survey <!-- [DECK] -->

## 3. Machine-learned interatomic potentials

**Taught:** Mon Sep 14 -- Wed Sep 16.

<!-- [ON PAGE] all four. No changes; this topic already mapped cleanly onto its unit. -->
- *E(3)-equivariant graph neural networks for data-efficient and accurate interatomic potentials* (NequIP), Nature Communications 2022 — [doi:10.1038/s41467-022-29939-5](https://doi.org/10.1038/s41467-022-29939-5)
- *MACE: Higher Order Equivariant Message Passing Neural Networks for Fast and Accurate Force Fields* (NeurIPS 2022) — [arXiv:2206.07697](https://arxiv.org/abs/2206.07697)
- *A foundation model for atomistic materials chemistry* (MACE-MP-0) — [arXiv:2401.00096](https://arxiv.org/abs/2401.00096)
- Dataset: *Open Materials 2024 (OMat24)* — [arXiv:2410.12771](https://arxiv.org/abs/2410.12771)

## 4. Protein language models and structure prediction

<!-- This topic covers TWO units taught five weeks apart. Grouped accordingly
     rather than split, because renumbering would break cross-references. -->

**Protein language models** --- taught Wed Sep 30 -- Fri Oct 2.

- *Evolutionary-scale prediction of atomic-level protein structure with a language model* (ESMFold), Science 2023 — [doi:10.1126/science.ade2574](https://doi.org/10.1126/science.ade2574) <!-- [ON PAGE] -->
- Hayes et al., *Simulating 500 million years of evolution with a language model* (ESM3), Science 2025 — [doi:10.1126/science.ads0018](https://doi.org/10.1126/science.ads0018) <!-- [ON PAGE] -->
- Didi et al., *FLIP2: Expanding Protein Fitness Landscape Benchmarks for Real-World Machine Learning Applications*, ICML 2026 — [flip.protein.properties](https://flip.protein.properties/) <!-- [ON PAGE], moved here from topic 1. Peter confirmed 2026-08-23 that he intends to read this. Venue (ICML 2026) still unverified against the ICML listing. -->
- Tang, Somia, Yu & Koo, *Evaluating the representational power of pre-trained DNA language models for regulatory genomics*, Genome Biology 26:203, 2025 — [doi:10.1186/s13059-025-03674-8](https://doi.org/10.1186/s13059-025-03674-8) <!-- [ON PAGE], moved here from topic 1 -->

**Structure prediction** --- taught Mon Nov 2 -- Wed Nov 4 *(Zoom)*.

<!-- units/16.md asks: teach all three AlphaFold papers, or only the latest?
     Undecided. Both listed until Peter picks. -->
- Jumper et al., *Highly accurate protein structure prediction with AlphaFold*, Nature 2021 — [doi:10.1038/s41586-021-03819-2](https://doi.org/10.1038/s41586-021-03819-2) <!-- [ON PAGE] -->
- Abramson et al., *Accurate structure prediction of biomolecular interactions with AlphaFold 3*, Nature 2024 — [doi:10.1038/s41586-024-07487-w](https://doi.org/10.1038/s41586-024-07487-w) <!-- [ON PAGE] -->

## 5. Virtual cell models

**Taught:** Fri Nov 13 -- Mon Nov 16.

Foundation models trained on single-cell transcriptomics, aiming at a model that predicts how a
cell responds to a perturbation it has never seen. Same recipe as protein language models — mask,
pretrain at scale, fine-tune — applied to a much noisier measurement.

<!-- [ON PAGE] first four. -->
- Cui et al., *scGPT: toward building a foundation model for single-cell multi-omics using generative AI*, Nature Methods 2024 — [doi:10.1038/s41592-024-02201-0](https://doi.org/10.1038/s41592-024-02201-0)
- Theodoris et al., *Transfer learning enables predictions in network biology* (Geneformer), Nature 2023 — [doi:10.1038/s41586-023-06139-9](https://doi.org/10.1038/s41586-023-06139-9)
- Hao et al., *Large-scale foundation model on single-cell transcriptomics* (scFoundation), Nature Methods 2024 — [doi:10.1038/s41592-024-02305-7](https://doi.org/10.1038/s41592-024-02305-7)
- Kedzierska et al., *Zero-shot evaluation reveals limitations of single-cell foundation models*, Genome Biology 2025 — [doi:10.1186/s13059-025-03574-x](https://doi.org/10.1186/s13059-025-03574-x) — read against scGPT and Geneformer
- Ahlmann-Eltze, Huber & Anders, *Deep-learning-based gene perturbation effect prediction does not yet outperform simple linear baselines*, Nature Methods 2025 — [doi:10.1038/s41592-025-02772-6](https://doi.org/10.1038/s41592-025-02772-6) — the linear-baseline critique <!-- [ON PAGE], moved here from topic 1, where it read as a generic supervised-learning paper. It is the same read-against role this topic already gives Kedzierska. Also cited in slides/supervised-learning. -->

## 6. Generative models for chemical and materials design

**Taught:** Mon Oct 26 -- Wed Oct 28, two sessions.

<!-- OVERBOOKED: four-plus papers against two sessions, one of which has to teach
     diffusion fundamentals. units/15.md mentions only RFdiffusion. Either cut
     the materials and discrete-diffusion strands, or give the unit a third
     session from reserve. Flagged on the Units tab of the schedule sheet. -->
- Watson et al., *De novo design of protein structure and function with RFdiffusion*, Nature 620, 1089–1100, 2023 — [doi:10.1038/s41586-023-06415-8](https://doi.org/10.1038/s41586-023-06415-8) <!-- [ON PAGE] -->
- Zeni et al., *A generative model for inorganic materials design* (MatterGen), Nature 639, 624–632, 2025 — [doi:10.1038/s41586-025-08628-5](https://doi.org/10.1038/s41586-025-08628-5) <!-- [ON PAGE] -->
- *Simple and Effective Masked Diffusion Language Models* (NeurIPS 2024) — [arXiv:2406.07524](https://arxiv.org/abs/2406.07524) — Sahoo, Arriola, Schiff, Gokaslan, Marroquin, Chiu, Rush, Kuleshov; Cornell Tech <!-- [ON PAGE], author list added from slides/diffusion -->
- *Discrete Diffusion Modeling by Estimating the Ratios of the Data Distribution* (SEDD, ICML 2024) — Lou, Meng, Ermon — [arXiv:2310.16834](https://arxiv.org/abs/2310.16834) <!-- [ON PAGE] -->
- Zheng, Chen, Mao, Liu, Zhu, Zhang, ICLR 2025 — [arXiv:2409.02908](https://arxiv.org/abs/2409.02908) — masked diffusion is an any-order masked model; part of the reported perplexity advantage was a 32-bit sampling artifact <!-- [DECK] slides/diffusion cites this alongside the other two discrete-diffusion papers; this page had only two of the three. -->

## 7. Uncertainty quantification, active learning, and Bayesian optimization

**Taught:** inside the black-box optimization unit, Fri Nov 6 -- Wed Nov 11.

<!-- Topics 7, 8 and 9 are ONE unit of three sessions in the schedule
     (units/17.md merges them). Kept as three numbered entries because
     slides/agents-for-science references "topic 9" by number. -->
- Frazier, *A Tutorial on Bayesian Optimization* — [arXiv:1807.02811](https://arxiv.org/abs/1807.02811) <!-- [ON PAGE] -->
- Hirschfeld et al., *Uncertainty Quantification Using Neural Networks for Molecular Property Prediction*, J. Chem. Inf. Model. 2020 — [doi:10.1021/acs.jcim.0c00502](https://doi.org/10.1021/acs.jcim.0c00502) <!-- [ON PAGE] -->

## 8. LLMs for black-box optimization

**Taught:** with topic 7, Fri Nov 6 -- Wed Nov 11.

<!-- [ON PAGE] both. -->
- *AlphaEvolve: A coding agent for scientific and algorithmic discovery* — [arXiv:2506.13131](https://arxiv.org/abs/2506.13131)
- *Generalists vs. Specialists: Evaluating LLMs on Highly-Constrained Biophysical Sequence Optimization Problems* (LLOME) — [arXiv:2410.22296](https://arxiv.org/abs/2410.22296)

## 9. Self-driving labs

**Taught:** with topics 7 and 8, Fri Nov 6 -- Wed Nov 11.

<!-- Roughly one session's share of a three-session unit, for four papers.
     The A-Lab/Leeman pairing is the one that matters; the first two are context. -->
- Gongora et al., *A Bayesian experimental autonomous researcher for mechanical design* (BEAR), Science Advances 2020 — [doi:10.1126/sciadv.aaz1708](https://doi.org/10.1126/sciadv.aaz1708) — Keith Brown's group <!-- [ON PAGE] -->
- Burger et al., *A mobile robotic chemist*, Nature 2020 — [doi:10.1038/s41586-020-2442-2](https://doi.org/10.1038/s41586-020-2442-2) <!-- [ON PAGE] -->
- Szymanski et al., *An autonomous laboratory for the accelerated synthesis of inorganic materials* (A-Lab), Nature 2023 — [doi:10.1038/s41586-023-06734-w](https://doi.org/10.1038/s41586-023-06734-w) <!-- [ON PAGE] -->
- Leeman et al., *Challenges in High-Throughput Inorganic Materials Prediction and Autonomous Synthesis*, PRX Energy 2024 — [doi:10.1103/PRXEnergy.3.011002](https://doi.org/10.1103/PRXEnergy.3.011002) — the critique of A-Lab; read the two together <!-- [ON PAGE] -->

## 10. Computer vision and inverse problems in characterization

**Taught:** Mon Sep 21 -- Wed Sep 23.

<!-- units/09.md leaves open whether this is taught on CNNs or vision
     transformers. The papers are unaffected either way, but if it moves to
     ViTs the unit shifts to after Transformers (Mon Sep 28) in the schedule. -->
- Zhong et al., *CryoDRGN: reconstruction of heterogeneous cryo-EM structures using neural networks*, Nature Methods 2021 — [doi:10.1038/s41592-020-01049-4](https://doi.org/10.1038/s41592-020-01049-4) <!-- [ON PAGE] -->
- *InverseBench: Benchmarking Plug-and-Play Diffusion Priors for Inverse Problems in Physical Sciences* (ICLR 2025) — [arXiv:2503.11043](https://arxiv.org/abs/2503.11043) <!-- [ON PAGE] -->

## 11. Neural surrogates for simulation: PINNs, neural operators, and weather

<!-- ================== DECISION NEEDED ==================
     THIS TOPIC HAS NO UNIT IN THE SCHEDULE. Seven papers, the longest list
     on the page, and nothing teaches it. It is currently only a candidate
     for the reserve sessions Wed Nov 18 and Fri Nov 20.

     Weighing against cutting it: slides/agents-for-science explicitly builds
     an argument on it -- "Same shape as Leeman vs A-Lab (topic 9) and
     McGreivy & Hakim vs PINNs (topic 11) ... Three times in one course is a
     property of the field." Cutting this topic costs that deck one of its
     three pillars, and the day-1 deck's celebrated/critique slide already
     lost the PINNs pairing for the same reason.
     ==================================================== -->

**Not currently scheduled** --- candidate for the reserve sessions, Wed Nov 18 -- Fri Nov 20.

<!-- [ON PAGE] all seven. -->
- Raissi et al., *Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear PDEs*, J. Comput. Phys. 2019 — [doi:10.1016/j.jcp.2018.10.045](https://doi.org/10.1016/j.jcp.2018.10.045)
- Karniadakis et al., *Physics-informed machine learning*, Nature Reviews Physics 2021 — [doi:10.1038/s42254-021-00314-5](https://doi.org/10.1038/s42254-021-00314-5)
- *Characterizing possible failure modes in physics-informed neural networks* (NeurIPS 2021) — [arXiv:2109.01050](https://arxiv.org/abs/2109.01050)
- McGreivy & Hakim, *Weak baselines and reporting biases lead to overoptimism in machine learning for fluid-related partial differential equations*, Nature Machine Intelligence 2024 — [doi:10.1038/s42256-024-00897-5](https://doi.org/10.1038/s42256-024-00897-5)
- *Fourier Neural Operator for Parametric Partial Differential Equations* — [arXiv:2010.08895](https://arxiv.org/abs/2010.08895)
- Lam et al., *Learning skillful medium-range global weather forecasting* (GraphCast), Science 2023 — [doi:10.1126/science.adi2336](https://doi.org/10.1126/science.adi2336)
- Price et al., *Probabilistic weather forecasting with machine learning* (GenCast), Nature 2024 — [doi:10.1038/s41586-024-08252-9](https://doi.org/10.1038/s41586-024-08252-9)

## 12. Extracting information from the literature

**Taught:** folded into the agents unit, Wed Oct 14 -- Fri Oct 23.

- Dagdelen et al., *Structured information extraction from scientific text with large language models*, Nature Communications 2024 — [doi:10.1038/s41467-024-45563-x](https://doi.org/10.1038/s41467-024-45563-x) <!-- [ON PAGE] -->

---

## Foundations

<!-- [DECK] This whole section is new to the page. Every paper is lifted from a
     built deck: slides/language-models, slides/reasoning-and-tools,
     slides/diffusion. Previously the page said nothing about the foundations
     units, so it read as though five units were missing.
     Optional-background framing is Claude's; confirm that is right. -->

Background for the foundations units. **Optional** --- these units are taught from slides, not
from papers, and nothing here is assigned reading.

**Language models** --- Mon Oct 5 -- Wed Oct 7

- **Chinchilla** — Hoffmann, Borgeaud, Mensch et al., *Training Compute-Optimal Large Language Models*, 2022 — [arXiv:2203.15556](https://arxiv.org/abs/2203.15556) — how to spend a compute budget
- **The Pile** — Gao, Biderman, Black et al., *An 800GB Dataset of Diverse Text for Language Modeling*, 2020 — [arXiv:2101.00027](https://arxiv.org/abs/2101.00027) — read Table 1, not the prose
- **InstructGPT** — Ouyang, Wu, Jiang et al., *Training language models to follow instructions with human feedback*, 2022 — [arXiv:2203.02155](https://arxiv.org/abs/2203.02155) — SFT and RLHF, the original
- **DeepSeek-R1** — *DeepSeek-R1 incentivizes reasoning in LLMs through reinforcement learning*, Nature 645, 633–638, 2025 — [doi:10.1038/s41586-025-09422-z](https://doi.org/10.1038/s41586-025-09422-z), preprint [arXiv:2501.12948](https://arxiv.org/abs/2501.12948) — where reasoning comes from
- **LLaMA** — Touvron, Lavril, Izacard et al., 2023 — [arXiv:2302.13971](https://arxiv.org/abs/2302.13971) — Table 1
- Schaeffer, Miranda, Koyejo, *Are Emergent Abilities of Large Language Models a Mirage?*, NeurIPS 2023 — [arXiv:2304.15004](https://arxiv.org/abs/2304.15004) — emergence as metric artifact
- Kalai, Nachum, Vempala, Zhang, *Why Language Models Hallucinate*, 2025 — [arXiv:2509.04664](https://arxiv.org/abs/2509.04664) — hallucination as an incentive problem

**Tools and reasoning** --- Fri Oct 9

- **ReAct** — Yao, Zhao, Yu, Du, Shafran, Narasimhan, Cao, *Synergizing Reasoning and Acting in Language Models*, ICLR 2023 — [arXiv:2210.03629](https://arxiv.org/abs/2210.03629)
- **Toolformer** — Schick et al. — [arXiv:2302.04761](https://arxiv.org/abs/2302.04761)
- Snell, Lee, Xu, Kumar, *Scaling LLM Test-Time Compute Optimally can be More Effective than Scaling Model Parameters* — [arXiv:2408.03314](https://arxiv.org/abs/2408.03314)
- Gema et al., *Inverse Scaling in Test-Time Compute* — [arXiv:2507.14417](https://arxiv.org/abs/2507.14417) — the counterweight

**Diffusion** --- Mon Oct 26 -- Wed Oct 28

- Dhariwal, Nichol, *Diffusion Models Beat GANs on Image Synthesis*, 2021 — [arXiv:2105.05233](https://arxiv.org/abs/2105.05233) — classifier guidance
- Ho, Salimans, *Classifier-Free Diffusion Guidance*, 2022 — [arXiv:2207.12598](https://arxiv.org/abs/2207.12598)
- Austin, Johnson, Ho, Tarlow, van den Berg, *Structured Denoising Diffusion in Discrete State-Spaces* — [arXiv:2107.03006](https://arxiv.org/abs/2107.03006)

<!-- GAPS -- no reading proposed, and none needed unless Peter wants some:
     supervised learning (Wed Aug 26), deep learning (Fri Aug 28 - Mon Aug 31),
     vibe coding (Wed Sep 2), CNNs and ResNets (Fri Sep 18),
     transformers (Fri Sep 25 - Mon Sep 28). All taught from slides.
     Deliberately not filled -- proposing canonical papers here would be
     guessing at what Peter wants students to read, which is the thing he
     asked me not to do. -->
