---
---
# Reading 1 — Comments by Theme

Your comments on Stokes et al. and Jiang et al., grouped into the fifteen themes we discussed in
class. Names have been removed. Comments are otherwise unedited, including original spelling.
The numbering matches the [discussion slides](slides/paper-discussion-1/paper-discussion-1.html).

Within each theme, individual comments are separated by a horizontal rule.

## 1. Excitement about Stokes and the power of ML for drug discovery

I find this paper particularly interesting because it goes beyond simply reporting a deep learning model – the authors also performed a full in vitro and even in vivo validation of their hits. Not many machine learning papers do so. I also appreciate that they designed and screened their own training dataset rather than using an existing antibiotic database (which could be easier). This choice shows that the authors really wanted to find a novel antibiotic with a new mechanism of action, rather than one biased towards rediscovering variations of already known one. Additionally, the authors didn’t just report a single successful prediction but also did a detailed mechanistic investigation into how halicin works, combining different assays to build a coherent picture of its mode of action.

---

In [1], it was very interesting how the DNN was able to generalize so well and identify antibacterial drugs with low structural similarity to the training molecules with so little data (2k training samples seems so small to me). The model was able to easily identify new structures that scientists have not been able to identify even after decades of research.

---

What I found most interesting about the first paper was seeing how broad the applications of machine learning can be. Most of my exposure to ML has been in prediction and finance, so seeing similar methods used for antibiotic discovery made the potential of ML feel much wider. I also found it interesting that the model could learn useful structural relationships from molecular data without researchers having to manually specify every pattern that might matter. Domain expertise was still essential for designing experiments and validating results, but the model could search for patterns across a space that would be extremely difficult to examine manually. This suggests that improvements in machine learning can have benefits across many different scientific fields.

---
Reading about the usefulness of neural networks and machine learning in biology was inspiring to me. Most of my research experience has been in finance, where ML can certainly be useful, but seeing these methods applied to antibiotic discovery made me ponder how extremely important these models can become when used in the right domain. A relatively general ML framework can help narrow enormous search spaces and potentially contribute to discoveries with direct effects on human health. It made me appreciate that improvements in machine learning are not only technical achievements; depending on where they are applied, they can have consequences that are much broader and more meaningful.

---

I think the most exciting point on this paper was that they have showed this deep learning approach could avoid a lot of time comsuming labor work in the laboratory when it gets harder for novel antibiotic screening. The predictions made by machine learning could save a lot efforts.

---

What do you find exciting? For the first paper, it seems exciting to me (as a natural science layman), that this is novel approach to identify/predict compounds that exhibit antibacterial activity, and crucially does so in a way that explores the vast space of possible chemicals that would be beyond unreasonable to explore in laboratory settings. Crucially, while the approach does perform a ranking, it does so in order to narrow down the space instead of finding the best compound, instead of finding the “best” one (a situation for which I would be skeptical of the model’s capabilities). I feel that the idea to narrow down the possibilities seems broadly applicable to many problems in science.

---

I found that this paper goes beyond reporting model performance. It completes the full pipeline from computational prediction to in vitro validation, mechanism-of-action studies, and validation in mouse infection models. Compared with simply reporting a higher ROC-AUC, this prospective validation provides stronger evidence that the model has practical scientific value.


## 2. What does Jiang et al. actually say about whether descriptors are better than GNNs?

On the first pass I read Jiang as simply showing that graph models do not work as well on molecules, and I also assumed the benchmark data itself must have been biased in favor of graph models somehow. Neither of those is what the paper says, and it took a second read to sort out. The argument is actually three separate things stacked on top of each other. First, the descriptor baselines in earlier work were weak, usually one fingerprint set plus a classical method, with XGBoost left out entirely. Second, averaging three runs is too noisy to separate the two families at all, which is why the single-split tables look inconclusive and the 50-split tables do not. Third, the ToxCast and MUV splits leaked in a way that only helped multi-task neural models. Only that last one is anything like bias, and it lives in the split rather than in the data. The data quality section muddied this for me, because they do wash the datasets, removing salts, counterions, and duplicates with conflicting labels, and in several datasets that is over 4% of the molecules, but then they report that it barely changes any result.

---

The juxtaposition of the two papers highlights the dynamic between deep learning exploration and rigorous empirical verification. Stokes et al. shows the power of graph-based deep learning to traverse a massive, non-intuitive search space (> 108 molecules) and identify halicin—a compound whose antibacterial properties eluded decades of conventional drug discovery. In contrast, Jiang et al. provides a vital, grounded reality check by demonstrating that off-the-shelf gradient-boosted trees and SVMs trained on classical physicochemical descriptors can match or outperform complex graph representations without requiring intensive GPU compute. Together, they demonstrate that practical computational chemistry requires both ambitious exploratory models and well-calibrated baseline models.

---

The two papers disagree, but they never really meet, and that was the most useful thing about reading them together. Jiang measures a mean test score over 50 splits. Stokes measures how many of its predicted compounds killed bacteria. Stokes never reports a matched top-k hit rate for any baseline model and Jiang never tests anything in the real world, so neither result can be used against the other.

---

The most exciting part for me was that the first paper followed the computer predictions with real experiments, including tests in mice. The model helped the researchers decide which molecules to test, and it saved researchers a lot of time. Reading the papers together also helped me separate two questions: “Can this model help make a useful discovery?” and “Is this model better than other methods?” I do not think the papers necessarily disagree. A graph model can help find an antibiotic without being the best model for every drug-discovery task.

---

What I found interesting. Stokes evaluates the model by whether ranked compounds work in real experiments, not only by a held-out prediction score. The sharp difference between the top-ranked set (51/99 active) and bottom-ranked set (2/63 active) makes the value of ranking intuitive. Jiang provides what can be seen as the complementary warning: a learned graph representation is not inherently better than strong descriptors and conventional models. I like real experiments for validation the best.

---

Jiang focuses on how representation predicts benchmark labels best; Stokes is more about whether model-guided ranking can produce experimentally useful candidates. Drug-discovery models definitely need both forms of evidence.

---

I found the papers particularly interesting together: Stokes demonstrates that model-guided screening can lead to experimentally validated discoveries, while Jiang questions whether sophisticated models consistently outperform strong conventional baselines. Stokes’s combination of graph representations and molecular descriptors also suggests that learned representations and existing chemical knowledge can complement each other.

---

I liked that the Stokes paper includes both prediction and a real experiment. Many ML papers stop after reporting a benchmark score. Here, the authors ordered compounds, tested them, and then evaluated one candidate in mice. At the same time, the Jiang paper makes the Stokes result easier to interpret carefully. Molecules are naturally graphs, but that fact alone does not prove that a graph model will outperform a strong fingerprint or descriptor baseline. The two papers together show why a successful experimental result is more helpful than a small change in benchmark accuracy.

---

What stands out to me the most about the GNN trained by Stokes et al. is that the training dataset only contained 2,335 compounds. In comparison, in Jiang et al., they found that datasets with a similar size had traditional descriptor-based methods outperform the graph-based methods, and the graph-based methods Attentive FP and GCN only had better performance on the larger datasets. That being said, the tasks that the two papers study are very different: Stokes et al. aimed to find a candidate list of molecules that exhibit a particular property, while Jiang et al. was mainly concerned with average prediction performance. I would be curious to know if the performance of the model in Stokes et al. could be significantly improved with a larger training dataset.

---

I don’t think there is a direct conflict between the claim of the second paper to the first paper. Stokes’s group hasn’t tried out the descriptors based representation to train a deep neural network to find antibiotics against E.Coli’s growth.


---

What I find interesting: Jiang et al., 2021 questions the common belief that GNN can work better than descriptor based models and finds in some regimes, descriptor only models are more enjoyable for its higher prediction accuracy and the shorter runtime. Stokes et al., 2020 showed a specific regime that GNN can actually be better: identifying molecules with antibacterial activity. In their paper, they hypothesized that GNN augmented with descriptor can improve the performance under limited samples.

---

The limitations I noticed was that they only picked four descriptor-based models and four graph-based models in their evaluation. They did prove that tranditonal descriptors-based models could result in comparable predictions as GNN, while there are other GNNs might be able to give better predictions than descriptors- based models. It will be more persuasive if they could try more GNNs in their studies.

---

For [2], I think that benchmarking all of the different machine learning methods is helpful, but from the tables, I think it is hard to come to any hard conclusions about whether one model is “better” than the other. I think a nuanced take of “be open to descriptor-based models, especially if computational cost is a concern” would probably be more insightful.


## 3. What representation and model should we use? Interaction of model + features

Both papers made me think more carefully about when representation-learning models should be used and when domain-designed features may be more valuable. With large amounts of high-quality data, graph neural networks may be able to learn useful representations directly from molecular structure. With smaller datasets, however, expert-created features can add significant value. The second paper supports this idea because graph models became more competitive on larger or multi-task datasets, while descriptor-based methods remained strong on many smaller datasets.

This relates closely to how I think about my own ML research. I often focus on finding the best model for a dataset, but these papers reinforce that model choice and feature design should be considered together. Understanding the domain well enough to construct meaningful features can be just as important as using a more advanced algorithm. Neither paper suggests that domain knowledge is becoming unnecessary; if anything, they show that human-designed features and ML can complement each other.

---

What future directions they open: I think their papers opened new directions to find out what are the favorable regimes of descriptor based methods and what are the favorable regimes of GNN methods. This would help model selection when given a specific task and training samples. Further, it is interesting to find out a way to augment GNN methods with descriptors so that this can always improve over the performance of both methods. Intuitively, since descriptors contained useful information, a smart way to augment that should help improve the GNN performance under limited samples.

---

I think these two papers open discussion on the sample size needed to learn a good representation directly from molecular graph end-to-end. Jiang et al., 2021’s result suggests that graph neural network may require a large training data size to learn. Stokes et al., 2020 tries to solve this issue by naively appending human crafted descriptors but it did not outperform using GNN alone. I think it might be more useful to reverse enginnering how each node should interact with neighbours to get the value of each descriptors and encode directly this mapping to the neural network. In this way, the network may be able to more directly adjust the weights to warm start from a known informative weights and try to find a better representation that has even more information.

---

A: The paper demonstrates a critical-thinking approach — rather than accepting the commonly reported claim that GNNs are inherently better for molecular property prediction, the authors ran extensive experiments to test this assumption against the alternative. It makes you consider testing different models rather than defaulting to whatever is currently considered the "gold standard" in the field, thus finding the best fit for your specific experimental data (with consideration of computational cost as well).

---

As mentioned above, I wish the paper had gone further than relying solely on statistical performance measurements to judge how accurate the models' predictions were — actually carrying out some wet-lab validation of the top predicted hits would have strengthened their claim that descriptor-based models are the better choice. Another point is that the paper doesn't consider hybrid models. As I understand it, the halicin paper used a graph neural network (D-MPNN) combined with RDKit descriptors specifically to overcome a known limitation of GNNs — their difficulty capturing global molecular features, especially in larger molecules — and this hybrid approach gave them their best results. This comparison paper doesn't test that scenario, so it isn't clear whether their "pure" GNN architectures (GCN, GAT, MPNN, Attentive FP) are representative of what a well-designed graph-based approach can achieve.

One clear direction would be to test a hybrid model, like D-MPNN combined with RDKit features (same as the halicin paper), against these eight benchmark ML models to see how it performs relative to both the pure graph-based and pure descriptor-based approaches. Another interesting observation was that GNNs specifically benefit from larger, multi-task datasets. This suggests it could be worth training multi-task GNNs on this kind of data — for example, in antibiotic discovery, training a model simultaneously on activity data across multiple pathogens, rather than a single-task model trained only on one species.

---

The paper's overall conclusion states that "descriptor-based models are able to achieve better or comparable predictions to graph-based models" — but their own results show this depends heavily on dataset size and task structure, with GNNs actually winning on the larger, multi-task datasets. This distinction matters, since larger multi-task datasets arguably reflect more realistic structure-activity relationship problems — in practice, we're rarely working with a single small dataset, and modeling multiple related biological activities together is often closer to how real drug discovery campaigns operate. Also, I didn’t fully understand how SHAP method works, but working with Claude to understand it.

---

The conclusion is also narrower than the abstract made me think. Graph models still come first on several datasets, and the real claim is that on small single-task data a good descriptor model is the safer default, not that graph models fail.

---

o I think what makes this paper interesting was that this paper challenged the common assumption that GNN would present better predictions than tranditonal descriptors-based models with their comparison between the two models. They showed that a lot of factors (for example, dataset quality and ML algorithm design) could affect the performance.

---

What I found most interesting was that the results were different from what I initially expected. Since molecules naturally have a graph structure, it seems reasonable to expect a model specifically designed for graphs to perform better. However, the paper shows that using a more natural or complicated representation does not necessarily lead to better predictions. In many cases, simpler models using good molecular descriptors were just as good or even better. I also found the comparison of computational cost useful. Accuracy is usually the first thing I look at when comparing machine learning models, but the amount of computation required also matters in practice. If two models give similar predictions, I would generally prefer the model that is faster and easier to understand.

---

One question this paper made me think about is when exactly a graph-based model starts to become more useful than a descriptor-based model. The results suggest that GNNs can become more competitive for larger and multi-task datasets, but this does not happen consistently across all of the datasets. It would be interesting to study this more systematically by changing the amount and diversity of training data and observing when the advantage shifts from descriptor-based models to graph-based models. Another direction would be to test whether the same conclusions hold when the models are asked to predict molecules that are structurally very different from those in the training data. This would help determine whether GNNs are better at learning representations that can generalize to new areas of chemical space.

---

One broader point I took from this paper is that the choice of a machine learning model should depend on the problem and the available data rather than simply choosing the newest method. The graph-based models become more competitive on some of the larger and multi-task datasets, while descriptor-based methods remain very strong on many of the smaller datasets. This also made me think that an interesting question for future work would be to understand when learning a molecular representation with a GNN actually becomes more useful than using existing molecular descriptors. For example, this may depend on the amount of training data, the diversity of the molecules, and the type of property being predicted.

---

For the paper Jiang et al., I found their conclusion that descriptor-based models outperform the GNN models in terms of prediction accuracy, especially the classification prediction which I thought GNN models might be advantageous.

---

For the paper Jiang et al., I think they should provide more detailed categorization of different task types by relating the datasets to their biological background. For example, as the Table 9 shows, descriptor-based models completely outperform GNN models (all top 3 are descriptor-based models) in the classification tasks in the datasets BBBP. However, taking a closer look at this dataset, we can see that it is about brain-blood barrier penetration which could be explained by molecules’ solubility or other physical properties that can be measured by numeric values and encoded with descriptors. In contrast, the datasets HIV and BACE are about the biochemical properties of a molecule which might require the information more than descriptors can provide. For example, molecular structure with stereochemistry is critical for being the substrate of an enzyme, which GNN is a better choice than descriptor-based methods. Therefore, I believe more clarification on the datasets and the tasks will help evaluate the performance of these models more accurately (also more useful for biologists).

---

Usually we think graph-based ML model is more attractive in molecular properties predictions due the inherent similarity of molecules and graph. However, this paper shows that descriptor-based model still perform better in molecular properties predictions and are more efficient.

---

What ideas for future research did the paper(s) inspire? I think in future research, especially on molecular properties predictions tasks, we should consider and compare both descriptor-based and graph-based models. Traditional descriptor-based models seem to give more efficient predictions and can give better accuracies in general, while graph-based models perform better on some large and multitasks dataset.

---

For future research, I would investigate whether improvements come from architecture, training objectives, richer inputs, or additional data. A modern comparison should distinguish these contributions and examine when each approach succeeds, e.g. with limited labels, unfamiliar scaffolds, and consequential local modifications. A meaningful question might be whether better computational performance leads to better experimental decisions.

---

A model’s limitations may come from missing inputs, restricted information propagation, insufficient training examples, or coarse experimental labels.These problems require different solutions. If the same architecture improves substantially after changing its training objective, its previous limitations cannot be attributed entirely to the architecture.

---

If two molecules become identical under the chosen representation, the model cannot reliably distinguish them using that representation alone. Conversely, adding 3D coordinates does not guarantee that the model has the biologically relevant conformation or experimental context. More information is useful only if it captures the distinctions relevant to the task.

---

The takeaway is that model choice should be treated as an empirical question. Stokes et al. show that deep learning can be genuinely useful in a discovery pipeline. Jiang et al. show that this does not make conventional baselines incompetent. The most convincing method is the one that survives fair comparisons and produces useful compounds, and might not always be the one with the more sophistcated architecture.

---

It draws our attention to what representation of biological molecules can best represent them to be used in a machine learning context. I think it depends on the predicted property. I don’t know much about biology but coming from a viewpoint of condensed matter theorist working on quantum materials, there would be certain insights regarding different properties of materials of interest. Then the correct representation should be based off those insights. For example, the properties of interest in Jiang’s group involves aqueous solubility, and from physical chemistry hydrophobicity is known to be main cause. So descriptor method will indeed perform well here. For bacterial growth inhibition, it depends on whether a molecule can go through a bacterial membrane and cause disruption, so in that case, the atomic structure is important, which is captured by graphical neural network.

---

I found interesting that they are comparing models that use different training data to perform the same task prediction. Also, I found interesting the computational cost comparison, which implies that given a good subset of features, it is much faster to train a simpler model and get better efficiency.  A possible continuation of the ideas is to device a method to compare the learned features with the MOE descriptors to see if there is some correlation between them.

---

There are some aspects of the design that I do not fully understand. The first is the relative importance of the descriptors obtained from RDKit for extending the GNN representation. It is unclear how crucial good representations are. Some models with only trained representations seem to have ranked halicin better, but the authors mention that these representations are useful for representing the global features of molecules. Another design choice that I do not fully understand is how to select the GNN architecture. If it is only used to represent the local molecular structure, does that mean that we expect all molecules in the training dataset to have a similar local structure?

---

What did you find confusing about Paper 1? They said they “augmented the learned representation with molecular features to prevent overfitting. I thought that adding more features makes overfitting more likely. Also why did they prioritize molecules with low similarity to ones in the training set? Are bacteria less likely to be immune to them or are they just demonstrating what their model can do?

---

The second paper was interesting because it showed that a more complicated model is not automatically better. Descriptor-based models still performed extremely well, especially when data were limited.


## 4. Descriptors have lots of chemistry knowledge baked in

What I find confusing: For Jiang et al,m 2021’ s comparison, expert-crafted descriptors already encode selected chemical and structural information, potentially simplifying the prediction problem.  It will be interesting to see how sensitive descriptors-based methods are with different quality of descriptors. Also the authors did not provide a clear explanation on why sometimes GNN are better and sometimes worse. Stokes et al., 2020 provides an example where GNN is better but it seems GNN only is better than GNN with descriptors, I am confused why the authors did not use GNN alone for their task.

---

I’m thinking why in this case descriptor-based model perform better than graph-based model. There are two reasons I can think of right now: (i) the descriptor-based models are more developed and extensively studied and optimized, while graph-based models are still developing fast. It’s possible that in the near future graph-based model perform better and become cheaper. (ii) the descriptors are selected based on chemical features, which already contains lot of hidden information (such as hydrogen bonding, polarities, functional groups, etc.) that has been studied by chemists for centuries. So the descriptor-based model already ‘learned’ lots of chemistry knowledge before training (It’s more a like semi-empirical methods). The graph-based model, although also contains some chemistry knowledge, it has way less effective chemistry in the model before training. The energy and electronic structure is closely related to the geometry of the molecules (Hammond-Leffler Hypothesis). The electronic structure of the molecule, which is a more fundamental quantity, determines the reactivity. Therefore, the molecular properties should be best descried and predicted based on graph-based method (or something similar). I believe graph-based method is intrinsically closer to the real molecule and should be more accurate upon careful optimization by close collaboration of computational scientists and chemists.


## 5. Downsides of descriptors

I noticed that the researchers care about the efficiency and the cost in their studies. However, they also mentioned, especially in paper 2, one single approach and limited datasets are not good enough for making a reliable prediction. Therefore, I am curious how would people evaluate their efficiecncy and cost when training models.

---

I felt the Jiang et al. paper may not be completely fair when they claimed that the descriptor-based models are less resource-demanding. A lot of those descriptors (like van der Waals surface area) are derived from experimental data or calculated by some other software, and those use resources too.

---

Jiang et al. were useful in making the comparisons, though the descriptor pipeline is not feature-free. It uses a large battery of expert-designed descriptors and fingerprints, and features generated with MOE. The reported training times do not cover the cost and effort of the software to prepare those inputs. It may be that more evaluations with scaffold or chronological splits would be useful. Repeating a random split many times may decrease variance, but it does not assess generalization to different families of chemicals. This is a crucial situation in the field of drug discovery.


## 6. SHAP and t-SNE are cool

In [2], I found the SHAP values analysis very interesting, and I do appreciate that the authors
took interpretability into account. Interpretability of machine learning models is a major concern
for scientists using automated. I also found the observation of descriptor-based methods to be
more conservative than graph-based methods for virtual screening to be really surprising. I
would not have expected a systematic divide like that. It would be interesting to dive into why
that is.

For [2], I found the SHAP values analysis very interesting. Why did they only conduct it for
XGBoost? I wish they would have done this for all of the models, or at least all of the
descriptor-based models. Is the SHAP analysis easier for XGBoost? I believe that SHAP can be
computed for neural networks, but perhaps it is computationally very expensive? This could
have been another reason to favor descriptor-based models. I think that was the point that they
were trying to make, but it was not clear.

---

What did you find interesting or exciting about Paper 2? I wasn’t aware of methods for interpreting results from ML models. It makes sense that when you’re using AI for science you want to be able to understand what the model is doing because that can further scientific understanding.

---

A thought I had while reading these papers- it is very difficult to visualize machine learning/AI models. The t-SNE from ﬁgure 5 in Stokes et al. was helpful, but I would like to learn more about how to visually represent the modeling process.

---

I also found the discussion of SHAP in Jiang et al. to be very interesting and I am curious how it might be extended to graph neural networks. 1) How much do practitioners care about model interpretability? This seems to be one clear advantage of some traditional descriptor-based models. Is there current work being done to make graph neural network models less of a black box?


## 7. Stokes: Missing Baselines

[1] did not conduct a thorough comparison between their GNN model and other possible model
architectures (DNN with fingerprinting, random forest classifiers, and SVM model). There was
some anecdotal evidence that their GNN model outperformed the other models. They noted that
their prediction for halicin was stronger than the other models.

In Stokes et al., although the authors tracked the ranking of baseline models (Random Forest and SVM on Morgan fingerprints) during in silico scoring, they did not carry those simpler baselines through the wet-lab validation pipeline. It remains an open question whether a standard gradient- boosted tree trained on their 2,335-molecule screen would have prioritized halicin or equally potent leads. 

---

What do you think the paper(s) could have improved? Maybe I missed some information but I’m thinking that this paper should provide some evidence that discovery of halicin using DNN is not coincident. A good model should give good accuracies on the ‘best molecules’ should also give good accuracies on ‘bad molecules. This means that the molecules that predicted good should perform good in wet experiments, and the molecules that predicted bad should perform bad in wet experiments. Therefore the author should also test randomly selected molecules that have low scores and see if perform ‘bad’ on inhibition of E. Coli growth.

---

The missing baseline in Stokes bothered me most. They did train other models, including the same network without RDKit features and a few Morgan fingerprint models, but the only thing reported is where each one ranked halicin, and it is all in the supplement. There is no ROC-AUC for those baselines on the same folds and no top-k hit rate measured the same way as the 51 of 99 they report for their own model. After reading Jiang, the question I want answered is whether a tuned XGBoost on good descriptors also puts halicin in the top 99. Training and scoring a model like that would be cheap compared to the wet-lab validation the paper already ran.

---

The obvious experiment is the one neither paper ran. Take Jiang’s eight tuned models, apply Stokes’s curation rule to one library, and test the top compounds from each in the same assay. That gives one number per model family, measured the way Stokes measures instead of the way Jiang does. Both halves already exist, since Jiang shows that models with equal AUC pick different candidates and Stokes shows how to score a candidate list.

---

For Stokes et al., I would like to see lab testing of the same number of top choices from each model. The authors compared predictions from several methods, but this additional experiment would help show which method finds more useful compounds with the same testing budget.

---

Both papers made me question what counts as a “better” model. Successful discovery does not establish superiority over alternative screening methods, and higher average benchmark performance may hide failures on subtle but important structural changes. I would have liked more targeted evaluations of activity cliffs and stereoisomers, alongside equal-budget experimental comparisons of model-selected candidates.

---

For Stokes et al., I would have liked a cleaner comparison with the baseline models. In the main model, halicin was placed very high in the ranking, but halicin was still one of many. Human judgement related to the degree of novelty, development status, availability, and predicted toxicity was critical after the ranking step. Making the same relative budget of experiments and testing available for each model should make the value of the graph model more clear.

---

A useful next step would be a benchmark in which graph models and descriptor models receive the same training data and the same experimental budget. Each method could nominate a fixed number of compounds from a new chemical library. The main outcome would be the number of experimentally confirmed, structurally novel hits rather than only ROC-AUC. I would also test hybrid models more systematically. A graph model may learn task-specific patterns, while chemical descriptors supply useful prior knowledge. Uncertainty estimates could then decide which compounds should be tested next.

---

In Stokes I liked that the checking goes both ways. Showing that top predictions work is normal. Testing the bottom 63 and finding almost nothing, and then scoring the WuXi anti-tuberculosis library where the best of 9,997 molecules only reached 0.37 and assaying the top 200 and bottom 100 with no actives at all, is not. For a screening campaign the second thing may matter more, since a model that gives high scores to a dead library will burn the entire budget.

---

[1] also did not touch on hyperparameter tuning. Was there a significant amount of hyperparameter tuning? Were the results sensitive to hyperparameter tuning?


## 8. The importance of data splits, clarifying the data pipeline

In Jiang et al., it is initially confusing how a standard stratified train/validation/test split could cause data leakage until looking at the outer-join operation across tasks. Because each sparse bioassay column in ToxCast was split independently into 80/10/10 sets to guarantee active labels in every fold, the same physical molecule ended up in the training split for Assay A while being assigned to the test split for Assay B. When merged into a multi-task matrix, the deep models had effectively seen the test molecules’ graph structures during training, which explained the inflated performance that vanished under true random splits.


For Jiang et al., while their protocol of 50 repeated random splits exposed split variance and data leakage, they did not systematically benchmark scaffold-based splits (e.g., Murcko scaffold clustering) across all datasets. Scaffold splits represent a critical challenge in hit-to-lead campaigns, and evaluating them would have provided deeper insight into how each representation generalizes across structurally novel chemical domains.

A key takeaway from both works is the paramount importance of data splitting hygiene in AI for science. As Jiang et al. demonstrated on the ToxCast dataset, seemingly subtle procedural choices such as merging independently stratified task splits, can inadvertently introduce representation leakage across tasks. Ensuring robust cross-validation across multiple random seeds, checking for target-correlated descriptor bias, and strictly verifying that test molecules remain unseen across all targets are crucial prerequisites before committing resources to wet-lab validation.

---

In Jiang the ToxCast result is the part I will remember. The leak is not sloppiness and it is not bias in the data. It comes from a sensible fix to a different problem, and it happens to help only one family of models. Finding a 0.13 AUC artifact inside a benchmark that several papers had already reused is a good reason to read splitting code instead of trusting a table.

---

In addition, on ESOL, SVM has a training RMSE of 0.149 against a test RMSE of 0.569, while the graph models fit training much worse and land between 0.587 and 0.708 on test. So SVM still wins on test error, but its much larger train-test gap points to overfitting on a small narrow dataset, which is not the same as showing that graph models generalize better. Tracking how that gap changes with dataset size and chemical diversity would give a simple rule for when the descriptor side stops being the safe first choice, and it would also say something about why the hybrid that Stokes used is a reasonable default.

---


One thing I would have liked to see is a stronger test of how the models perform on molecules that are substantially different from the molecules used for training. The authors repeat their experiments with many random train/test splits, which helps reduce the chance that the conclusions depend on one lucky split. However, in an actual drug discovery problem, we may want to make predictions for new chemical structures that are quite different from the compounds already present in the training data. It would therefore have been useful to include an additional evaluation where the training and test molecules are separated according to their chemical structures. This could provide a better idea of which methods are able to generalize to new regions of chemical space, rather than only predicting randomly held-out molecules from the same dataset.

---

For Jiang et al., I would like to see more tests where the test molecules have different core structures from the training molecules. I think separating molecules by their core structures would better test whether a model can handle unfamiliar compounds.

---

Interesting that the accuracy of models depends to data selection and splitting. Here particularly, the authors observed that the NN-based models yield much better predictions than the descriptor- based models to the ToxCast dataset. Since they were hoping to see results other way around, they looked at the splitting method and observed that the choice of data splitting was leading to overfitting. One could have easily confused about the performance of these models had they not checked into the training methods.

---

Although the authors did mention that the traditional methods work better than the GNNs, their claims are based on marginal differences in the test and validation errors. However, the final predictions from these models were significantly different for the HIV VS they performed later. I was confused about the reliability of these predictions. Particularly the test and validation errors were similar across different methods but the training errors in descriptor based models were significantly lower, is there some sort of overfitting here?

---

The paper mainly uses random data splits. Scaffold or temporal splits would provide a more realistic evaluation of generalization to structurally novel molecules.

---

I also found the description of the ‘four experimental phases’ difficult to follow on first read and worked through it with Claude to break it down. My understanding now is that phases 1a and 1b serve two different purposes despite looking similar: phase 1a (80% training / 10% validation / 10% test split, repeated 20 times) exists purely to measure how good the model is, this is what produced the reported ROC-AUC of 0.896. Phase 1b then removes test set (90% training / 10% validation only) because, once they'd confirmed the model works well in phase 1a, they no longer needed to measure performance — they wanted to use as much of the small 2,335-molecule dataset as possible to train the strongest possible model. The 20 different random splits in phase 1b don't get averaged into a metric like they were in 1a; instead, each of the 20 resulting models becomes one member of the final 20-model ensemble that's used to make predictions. Phases 2 through 4 then apply that ensemble to new chemical libraries (prediction), add the empirically tested results back into the training set and repeat the process (retraining), and finally generate predictions on the next library using the updated model.


## 9. Inappropriate binarization

In [1], they note, “we observed that 8 of the 23 molecules displayed detectable growth inhibitory
activity”. “Detectable” seems to imply that even a small amount of growth inhibition activity
would be considered a “success”, but in the paper, they use 80% or more growth inhibition as
the cut-off for positively classified molecules. If the growth inhibition was a small but detectable
amount for a test molecule, then the “correct” label is actually the negative label. Perhaps I just
do not understand the field well enough, because perhaps discovering a molecule with any
amount of antibacterial behavior is a success. It just seems to me that if the growth inhibition is
small, then the molecule is not actually a viable antibiotic. I think that only molecules that
demonstrate real promise as antibiotics should be noted in the success metrics (“among the
most highly predicted molecules, our model performed well (51.5% accuracy)”)

---

What was unclear? Before reading the second paper, I was questioning whether a classification or regression problem made more sense for this task, since if I understand correctly, there were OD600 measurements (in [0, 1]) that could have been used, but this data is coarsened to {0, 1}.

---

For Jiang, the screening section leans on an arbitrary threshold. They call 0.5 arbitrary themselves, and part of the 7 to 329 spread is just calibration rather than real disagreement about which molecules look good. Comparing overlap at the same top-k, or calibrating the scores first, would separate those two things. The bigger issue is that none of it was tested. The only ground truth is that all eight models found zidovudine. Testing even ten compounds from the two most different models would have turned this into a statement about which model finds real drugs.


## 10. Model agreement and disagreement, power of ensembles

I was also surprised that models with similar AUC values could rank very different molecules near the top. This raises the question of whether disagreement between strong models could itself be useful. Instead of choosing one model and ignoring the others, researchers might be able to use multiple models to find candidates that any single model would miss.  A useful future direction could also be studying model disagreement directly. If several strong models independently rank the same candidate highly, that could increase confidence. If one model strongly favors a candidate that others ignore, it may point to a more unusual area worth investigating.

---

Another interesting observation: when the eight models were compared on their predicted HIV inhibitor candidates, their top-ranked compounds were highly diverse. Of the top 160 compounds, 116 were unique, and only 10 compounds were ranked in the top 20 by three or more models. Notably, all eight models converged on one known drug, zidovudine, an established HIV/AIDS treatment. Beyond that, though, there was little structural overlap, and no single structural feature was common across all eight models. This shows that different ML algorithms, even with comparable overall accuracy, can identify quite different sets of candidate compounds. I wish the authors had gone further and experimentally benchmarked which of these predicted candidates performs better in vitro, rather than relying solely on statistical agreement/disagreement between models.

---

Jiang’s overlap analysis also suggests something more useful than picking a winner. Eight models with similar accuracy barely agree on which molecules to flag, which suggests their candidate sets are complementary and worth testing together rather than choosing one. The thing to optimize is not mean AUC but how many real actives you get in k tests, and a consensus or diversity-aware ranking targets that directly.

---

I found it interesting that relatively simple descriptor-based models often outperformed more complicated GNNs. The paper also shows that similar benchmark performance does not imply similar behavior in virtual screening: different models selected very different candidates.

---

I think Stokes et al. did a good job testing generalization across chemical libraries and by validating halicin in actual mouse infection models. Jiang et al. provided a well-rounded comparison of model performances by assigning classification, regression, and mixed tasks. It is also interesting that in HIV screeing, different ML algorithms with similar accuracy pick diverse potential inhibitors, which supports that the design of the algorithm can determine its focus or evaluation of different features in prediction and that accuracy alone is not a sufficient representation of the final prediction results.


## 11. Shortlist design / was stokes just lucky?

Stokes et al. paper. I found it very interesting that halicin just barely made their shortlist threshold cutoff; they only considered the top 99 molecules from a library of 6,111 according to their scoring function and threshold, and halicin had rank 89. If halicin was ranked slightly worse they would never have discovered its effectiveness from their study. This demonstrates the importance of having a strong method for creating a shortlist of drugs to further consider.  I found it a little strange how they portray the pipeline; they first do a full physical screen of 2,335 molecules which they describe as an “inexpensive” step, implying that the next step will be much more complex. But the next step considers a library of 6,111 molecules from the Drug Repurposing Hub. This is only 2.6x as large as the number of molecules in the initial phase. If it is that easy/inexpensive to do the screen of 2,335 molecules, why not screen the other 6,111 as well? I understand that ultimately they are creating a neural network that will be applicable for the significantly larger dataset of > 107 million molecules. But this does not explain why the initial 2,335 are inexpensive while the additional 6,111 are considered expensive.

---

I found it interesting that this model could identify a molecule that inhibits growth from such a small amount of data. There were only a few compounds similar to halicin in the training dataset, so I don’t think the model is just doing pattern recognition. I wonder if it learned something about the chemical mechanisms that made the molecules in the training dataset effective. What do we know about the mechanism of action of the molecules most similar to halicin in the training data set? Is it a similar mechanism?

---

There are some non-transparent choices in their workflow that I would like to see explained in more detail. The first is the criteria used to select the set of molecules from the set of highest scores given by the model that warrant further study. They said they used a deep learning model to evaluate toxicity, but they do not talk about the level of uncertainty they expect from it, given that this model could perform badly in the chosen database. They also mention phase investigation, but I don’t know if this is a reliable criterion, as they could be testing the efficiency for something else. Finally, they discuss structural similarity, but I believe this is a poor criterion for determining the usefulness of molecules, as two similar molecular structures can have very different effects in the body. The fact that they found something that seems to work alleviates this issue to some extent, but raises the question of whether this was just luck.

---

The cutoffs are also unexplained. The ZINC15 filter used a score above 0.8 and Tanimoto below 0.4 with no check on how sensitive the result is to either number. The 23 compounds were not the top 23 either, because whether they could be obtained at all was a third filter. The paper admits in the discussion that synthesis cost and instability limit what you can get, so 8 out of 23 is not a clean precision estimate. And at the 107 million scale there is no version of the low-score test that made the earlier result convincing, so we do not know the false negative rate where the search space is largest.

---

Their approach ended up identifying a molecule that “could function through an uncommon mechanism of action”, which is promising from the perspective of antibacterial resistance. It came across as a welcome surprise. Was it just luck that the top 99 list had any molecules that had “low structural similarity to training set molecules”? Or maybe this just follows from the train and test databases being quite different? Otherwise, could something about the prediction task be changed to ensure it ranks molecules more likely to be resistant higher?

---

For the paper Stokes et al., one factor that leads to the discovery of halicin is that despite the small size of the initial training dataset, it contains structurally diverse compounds beyond the antibiotic’s library, which enables the discovery of antibiotics with novel chemistry scaffolds. This emphasizes the importance of training dataset diversity for virtual screening.

---

This work used antibiotic library as well as some natural products as training set and applied machine learning method to obtain a model (on 104 data set) that can give predictions on large chemistry libraries (108 order). This significantly accelerates the discovery of new antibiotics. The prediction results were carefully selected for experimental test. The selection is based on test scores, toxicity and structures. The author intentionally select molecules with unique structure that is different from many common antibiotics is smart, this avoids predictions with similar outcomes as already known antibiotics and can inspire chemists for design next generation antibiotics or other drug molecules.

---

The other striking thing to me about the results in Stokes et al. was that they were able to identify antibiotics that are structurally dissimilar from any known antibiotics. I expect machine learning models to be very good at identifying known patterns in new data, but the identification of completely new structures (with perhaps some small pieces of known patterns) is profound. I am curious to know if this is particular to graph-based models or if more traditional descriptor-based models can also be capable of this (in a way that is not a one-off or fluke).

---

One part I found confusing was how the model performed on the WuXi anti-tuberculosis library and the ZINC15 database, after applying the model to the WuXi library, none of the 300 tested compounds (the top 200 and bottom 100 predictions) showed any antibacterial activity, which suggested the model couldn’t perform well to that chemical space. However, they moved on a subset of the ZINC15 database and selected specific compounds, they describe as contain molecules with ‘antibiotic-like physicochemical properties.’ I am not sure exactly what these properties are, how the selected compounds were defined, or why this pre-selection steps were expected to work better than the WuXi library did, especially since the initial WuXi results suggested the model struggles outside the original training distribution.


## 12. What experiments should we use as a judge when discovering antibiotics? A lot more work is needed to create a validated drug.

One thing I am confused about Stokes et al.’s experimental design is using antibiotic acitivities against E.coli as the primary training data. Though the paper mentions that the assay was cheap and chemically diverse, I wonder if E.coli is an ideal candidate to represent bacterial activities broadly.

Future ideas on extending Stokes et al.’s discussion include setting effective desired outcome for model training. Currently the paper relies on growth inhibition, but I wonder if there are other quantifiable options such as bacterial density or change in mutation rate.  Training and testing the model effectiveness on datasets with varied sizes are also worth exploring, as the authors mentioned that the training data is still limited. This observation is connected to what Jiang et al. found--training a better graph-based model might need more samples.

---

Another direction is extending model to multi-objective classification task, predicting other features like activity and solubility.

---

The paper's Discussion section covers a few of these directions, as the authors state that their model is, at the moment, more of a proof-of-concept. Firstly, they propose moving beyond simple growth inhibition as the training phenotype, toward more targeted phenotypic screens enriched for molecules acting through specific mechanisms. This suggests a pipeline that predicts not just "does this molecule stop bacterial growth" but "does this molecule act through a specific, desirable mechanism" — which could make discovered hits more mechanistically predictable from the outset, rather than requiring the extensive downstream mechanistic wet-lab work they had to do after the fact for halicin. They also acknowledge that synthesis was a major practical bottleneck.

---

On the mouse side, the C. difficile group is n = 4 after three of seven mice failed to get infected, and that group carries the claim about beating standard treatment. The wound model is also topical treatment of a surface infection, which is a fine first step but says nothing about systemic dosing, and there is no PK or tolerability data.

---

One thing I noticed in Stokes is that it trains on E. coli growth inhibition at a single concentration, which they picked because it is cheap and reproducible rather than because it is the right target, and they say so in the discussion. Halicin does not work on P. aeruginosa, and they guess this is a membrane permeability problem but never test it. A growth assay in one organism does pick up permeability effects indirectly, but it cannot tell whether the failure comes from permeability or from something else specific to that species. A cleaner design would hold a second organism out entirely and use it to test whether the model transfers, rather than folding it into training.

---

The paper from Stokes et al. seems very exciting, I was looking up this drug though and apparently it doesn’t have the right pharmacokinetic proﬁle to stay in the body. That makes me wonder whether the ability to evade metabolism/elimination should have been another key property to train the model on. A lot of promising drugs fail at the clinical stage because of how they interact with human metabolism, so I feel that could be a more useful future direction.

---

The mouse results are interesting but limited. The treatment groups had only four to six animals depending on the experiment. Calling halicin a discovered antibiotic is reasonable at the screening stage, but I don’t think it’s enough to define halicin as a validated medicine. Possibly there are many other factors to be considered such as side effects and so on.

---

It also lacks laboratory validation, so it is unclear which model’s virtual-screening candidates are actually better.

---

What could be improved. Stokes uses small mouse groups and establishes neither human safety nor clinical efficacy. Its final candidate choice also combines model ranking with manual criteria, so the model alone is not the complete discovery system. Jiang relies heavily on random data splits; scaffold or time splits would test generalization to genuinely different chemistry more directly. Its speed comparison also uses different hardware and implementations.


## 13. More data, active learning

Although, I am not a computational expert, I think the training dataset is on the smaller end – and only 120 of the 2335 screened compounds were positive hits (which is around 5%). I would speculate that the model could improved with a larger and more balanced training set. Alternatively, they could use some methods to address the imbalanced data (examples: reweighting the loss function, oversampling hits), which might have helped the model learn the minority class better. I am also not sure whether this is correct, but in their retraining strategy, the compounds selected for empirical testing at each round were always the top ranked (99, then 200) and bottom ranked (63, then 100) predictions – essentially the compounds the model was most confident about, whether it is positive or negative. While this makes sense experimentally, I think it might have been more informative to also test some compounds the model was uncertain about, since those are the ones that would teach the model the most and potentially improve its ability to generalise, rather than reinforcing what is already predicting well.

---

Future research inspired by the papers. Use active learning: predict candidates, test the most informative molecules, retrain, and repeat. Evaluate each round on new scaffolds while jointly measuring activity, toxicity, resistance, and pharmacokinetics.


---

For further improvements, I am not sure if around 2500 compounds in their dataset are good enough for training. Maybe they are good with E. coli, but there are many other types of bacteria. Probably, more resources need to be included in their model to generalize this prediction.


## 14. Generative models for generating molecules

Another point, the prediction presented in this work is based on known molecules from a known library. It’s not generative. I’m thinking if the model can be further improved to be generative, so scientist can really benefit from the new molecules that might never be made before. However this is hard – a generative model is harder to construct, the new molecules should be stable, reasonable, and chemically accessible. This might include new representation method, some prediction related to molecules electron density, and automatic retro-synthesis analysis.

---

Instead of predicting using data in existing library (which may not cover much antibiotic molecule), we could use generative models (like variational flow matching) to generate eligible data. Then apply this model on the larger chemical space.


## 15. Argument for self-driving labs

A broader lesson from these papers is that the relevant unit of scaling in science may not be model size or compute, but the number of reliable experimental learning cycles. Progress in coding and mathematics has accelerated because candidate solutions can be generated, verified, and used as feedback at very low cost. Scientific discovery is more difficult because experiments are slow, noisy, expensive, and sometimes difficult to reproduce.

The first paper shows that a predictive model becomes scientifically meaningful only when its predictions survive prospective experimental validation. The second shows that, under limited-data conditions, a more sophisticated representation learner does not necessarily outperform simpler descriptor-based methods. These results suggest that model architecture is not currently the only, or even the primary, bottleneck.

The most scalable near-term opportunities may therefore be scientific domains with programmable inputs, automated experiments, and clear quantitative outputs, such as protein desgin, synthetic chemistry, and materials design. An AI-native laboratory could repeatedly propose candidates, execute experiments, validate the measurements, and update its beliefs. If this loop becomes fast and reliable, experiments themselves can become a renewable source of training data. In this view, the central challenge is not merely building a larger scientific model, but building an environment in which scientific models can learn from reality at scale.
