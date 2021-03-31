# Schedule

We will meet synchronously via Zoom: Tu 5:30-8:15

This course will proceed in three main parts: overview, deep dives, and wrap up.

## Structure

### Overview

In the first part of the course we will review ML basics, set norms for interaction and complete a survey of the topics that we will cover for the rest of the semester.  

In this part of the class, Professor Brown will lead synchronous sessions.  Students will be responsible for reading overviews, refreshing background material, and choosing an area for their course project. Students will start with an introductory demo or replication as a mini project.

### Deep Dives

During the middle of the course we will spend one week on each topic. There will be 1-3 papers to read each week.

Students will be responsible for presenting papers in class on a rotating basis.

During this time students will have milestones where they need to complete interim steps for their course project. The first milestone will be a proposal that includes the specific products for the remainder of the milestones based on a template.  


### Conclusion

In the end of the course, we will focus on integrating ideas across multiple topics.

We will also workshop students' projects, giving substantive feedback prior to the final submissions.

Final projects will be evaluated through a presentation and paper


## Weekly topics


``````{list-table} Schedule
:header-rows: 1
:widths: 10 10 20 20
:name: schedule

* - Class
  - Topic
  - Reading
  - Activities
* - 2021-01-29
  - Introduction
  - None
  - introductions, expectation setting
* - 2021-02-01
  - Probability Review
  - Model Based ML, chapter 1
  - reading discussion, setting
* - 2021-02-03
  - ML Process & Mutual information preview
  - Scikit learn getting started,
  - live coding
* - 2021-02-08
  - Missing Data: Intro strategies
  - [Handling Missing Values when Applying Classification Models](https://www.jmlr.org/papers/volume8/saar-tsechansky07a/saar-tsechansky07a.pdf) &
  [Missing data imputation using statistical and machine learning methods in a real
  breast cancer problem](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.701.4234&rep=rep1&type=pdf)
  - Paper discussion led by Daniel
* - 2021-02-10
  - Missing data with graphical models and causal reasoning
  - [Graphical Models for Inference with Missing Data](https://proceedings.neurips.cc/paper/2013/file/0ff8033cf9437c213ee13937b1c4c455-Paper.pdf) &
 [Missing Data as a Causal and Probabilistic Problem](https://auai.org/uai2015/proceedings/papers/204.pdf)
  - Paper discussion led by Julian
* - 2021-02-15
  - Current Challenges in Missing data
  - [Handling Missing Data in Decision Trees: A Probabilistic Approach](https://openreview.net/forum?id=0IXcmQIAJPt) & [How to miss data? Reinforcement learning for environments with high observation cost](https://openreview.net/forum?id=jEN6sD09HWe)
  - Paper discussions by Xavier and Zhen
* - 2021-02-17
  - Current Challenges in Missing data
  - [How to deal with missing data in supervised deep learning](https://openreview.net/forum?id=jEXxzPUMYVZ)
  - Paper discussion by Madhukara, Replication & testing discussion,
* - 2021-02-22
  - Fairness
  - fairml classification chapter and friedler empricial comparison paper
  - Empirical setup
* - 2021-02-24
  - Fairness
  - Reading
  -  preview of lasso and admm constraint to multiobjecitve reformulation
* - 2021-03-01
  - Multi-objective & constrained opt
  - [Elastic Net](https://rss.onlinelibrary.wiley.com/doi/10.1111/j.1467-9868.2005.00503.x)
  - Paper presentation by Daniel, try out elastic net & LASSO in scikit learn
* - 2021-03-03
  - Multi-objective & constrained opt
  - [A critical review of multi-objective optimization in data mining: a position paper](https://dl.acm.org/doi/abs/10.1145/1046456.1046467?casa_token=EolodHNPqJcAAAAA:WP8AqKpTtu74hQbMH6MabfM3HjFbQZ2C5Vp4CV--FTleunL6O_cKD98tfi7KVSWbD89vGdVaReg)
  - Paper presentation and discussion by Zhen
* - 2021-03-08
  - Latent Variable Models
  - [Gaussian Mixture Models](https://jakevdp.github.io/PythonDataScienceHandbook/05.12-gaussian-mixtures.html) and [Topic Models](https://jmlr.org/papers/volume3/blei03a/blei03a.pdf)
  - Paper presentaiton by Xavier
* - 2021-03-10
  - Latent Variable Models
  - [Indian Buffet Process](https://jmlr.org/papers/volume12/griffiths11a/griffiths11a.pdf) and [Auto-Encoding Variational Bayes](https://arxiv.org/pdf/1312.6114.pdf)
  - Paper presentation by Madhukara
* - 2021-03-15
  - Missing or Noisy labels
  - [Learning with Noisy Labels](https://proceedings.neurips.cc/paper/2013/file/3871bd64012152bfb53fdf04b401193f-Paper.pdf) and [Semi Supervised Learning](https://link.springer.com/article/10.1007/s10994-019-05855-6)
  - Julian and Daniel
* - 2021-03-17
  - Noisy Labels as a model for Bias
  - [Recovering from biased data: Can fairness constraints improve accuracy](https://arxiv.org/pdf/1912.01094.pdf) and  [Fair classification with group dependent label noise](https://dl.acm.org/doi/10.1145/3442188.3445915)
  - Zhen
* - 2021-03-22
  - Interpretable & Explanation Intro
  - [A Survey of Methods for Explaining Black Box Models](https://dl.acm.org/doi/pdf/10.1145/3236009)
  - Xavier
* - 2021-03-24
  - A Case for Interpretability over Explanation
  - [Why are we explaining black box models](https://hdsr.mitpress.mit.edu/pub/f9kuryi8/release/6) and [Learning Certifiably optimal rule lists for categorical data](http://jmlr.org/papers/volume18/17-716/17-716.pdf)
  - Madhukara
* - 2021-03-29
  - Models for Explanation
  - [Interpretability Beyond Feature Attribution: Quantitative Testing with Concept Activation Vectors (TCAV)](https://arxiv.org/abs/1711.11279) and [A unified approach to interpreting model predictions](https://dl.acm.org/doi/10.5555/3295222.3295230)
  - Zhen
* - 2021-03-31
  - Choosing Explanations and using explantions
  - [How can I choose an explainer? An Application-grounded
Evaluation of Post-hoc Explanations](https://dl.acm.org/doi/pdf/10.1145/3442188.3445941) [Actionable Recourse in Linear Classification](https://dl.acm.org/doi/10.1145/3287560.3287566)
  - Daniel
* - 2021-04-05
  - What are the risks of explanations
  - [Model Reconstruction from Model Explanations](https://arxiv.org/abs/1807.05185)
  - Activities
* - 2021-04-07
  - What does Interpretable mean
  - [Towards A Rigorous Science of Interpretable Machine Learning](https://arxiv.org/abs/1702.08608) and [Towards falsifiable interpretability research](https://ml-retrospectives.github.io/neurips2020/camera_ready/4.pdf)
  - Activities
* - 2021-04-12
  - Meta issues
  - [The Scientific Method in the Science of Machine Learning](https://arxiv.org/abs/1904.10922) and [Value-laden Disciplinary Shifts in Machine Learning](https://arxiv.org/abs/1912.01172)
  - Activities
* - 2021-04-13
  - Meta issues
  - [Roles for computing in social change](https://dl.acm.org/doi/abs/10.1145/3351095.3372871)
  - Activities
* - 2021-04-19
  - Project Presentations
  - projects
  - presentations with peer feedback
* - 2021-04-21
  - Project Presentations
  - projects
  - peer feedback
* - 2021-04-26
  - Review and Project Reflections
  - Paper feedback
  - presentations with revision plans
``````



<!-- You can also cite references that are stored in a `bibtex` file. For example,
the following syntax: `` {cite}`holdgraf_evidence_2014` `` will render like
this: {cite}`holdgraf_evidence_2014`.





```{bibliography} references.bib
``` -->
