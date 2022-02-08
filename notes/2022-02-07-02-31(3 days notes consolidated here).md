# MLSS
# 2022-02-07

Lead Scribe: Surbhi Rathore

## Opening Notes
Handling missing data.

## Paper - Handling Missing Values when Applying Classification Models
 [paper](https://www.jmlr.org/papers/volume8/saar-tsechansky07a/saar-tsechansky07a.pdf) -- Presented by Emmely 
 
### Analysis over different treatments of missing values at prediction time.
 
 - Alternative courses of action when features are missing:
     - Discard instances: Simply discarding instances with missing values.
     - Acquire missing values: In practice, a missing value may be obtainable by incurring a cost, such as the cost of performing a diagnostic test or the cost of acquiring consumer data from a third party.
     - Imputation : The main idea of imputation is that if an important feature is missing for a particular instance, it can be estimated from the data that are present.
         - (Predictive) Value Imputation (PVI): Value imputation estimates a value to be used by the model in place of the missing feature. Value imputation is more common in the statistics community
         - Distribution-based Imputation (DBI): Distribution-based imputation estimates the conditional distribution of the missing value, and predictions will be based on this estimated distribution. distribution-based imputation is the basis for the most popular treatment used by the (non-Bayesian) machine learning community 
         - Unique-value imputation: Rather than estimating an unknown feature value it is possible to replace each missing value with an arbitrary unique value.
     - Reduced-feature Models: Reduced-feature models : We refer to these models as reduced-feature models, as they are induced using only a subset of the features that are available for the training data. Reduced-feature models can be computationally expensive.

- Missing Completely At Random (MCAR) : refers to the scenario where missingness of feature values is independent of the feature values (observed or not). (missing values have nothing to to do with feature values)

#### Comparison of PVI, DBI and Reduced Modeling
- Reduced-feature modeling performs consistently outperforms the other two method. 

#### LOW and HIGH FEATURE IMPUTABILITY Result
- PVI is better for higher feature imputability, and DBI is better for lower feature imputability. Value imputation generally preferable for high feature imputability, and DBI generally better for low feature imputability.

#### REDUCED-FEATURE MODELING SHOULD HAVE ADVANTAGES ALL ALONG THE IMPUTABILITY SPECTRUM
- Reduced modeling is a lower-dimensional learning problem than the modeling to which imputation methods are applied, it will tend to have lower variance and thereby may exhibit lower generalization error.

####  Evaluation with “Naturally Occurring” Missing Values
-  By “naturally occurring,” we mean that these are data sets from real classification problems, where the missingness is due to processes of the domain outside the control.

### Conclusions
```{epigraph}
Reduced-feature models are preferable both to distribution-based imputation and 
to predictive value imputation.Reduced models undertake a lower-variance learning 
task, and do not fall prey to certain pathologies. Predictive value imputation 
and DBI are easy to apply, but one almost always pays—sometimes dearly—with 
suboptimal accuracy.
```
## Paper - Missing data imputation using statistical and machine learning methods in a real breast cancer problem
 [paper](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.701.4234&rep=rep1&type=pdf) -- Presented by Chan 

### The ‘‘El Alamo-I’’ breast cancer dataset
- one of the largest databases on breast cancer in Spain.
- The missing data represent 5:61% of the overall data set.

### Statistical methods
- The statistical imputation methods include mean imputation, hot-deck, and MI methods based on regression and the expectation maximisation (EM) algorithm.
    - Mean Imputation: is a simple application of regression imputation, the mean value of each non-missing variable is used to fill in missing values for all observations.
    -  Hot-deck imputation : nearest neighbour hot-deck imputation is applied, where a nonrespondent is assigned the value of the nearest neighbour record according to a similarity criterion.
    -   Multiple imputation : , MI replaces an unknown value with a set of plausible data and uses an appropriate model that incorporates random variation. MI has several desirable features: 
        -   (1) an appropriate random error is introduced into the imputation process to obtain approximately unbiased estimates of all parameters; 
        -   (2) good estimates of standard errors are obtained from repeated imputation; and 
        -   (3) MI can be used for any kind of data and any kind of analysis without specialised software.

### Machine learning methods

- Imputation methods based on machine learning are sophisticated procedures that generally consist of creating a predictive model to estimate values that will substitute the missing items.
- These approaches model the missing data estimation based on information available in the data set. 
- Three well-known imputation techniques using machine learning approaches: MLP, SOM and KNN.
    - Multi-layer perceptron : 
        - An MLP consists of multiple layers of computational units interconnected in a feed-forward way. 
        - Each unit in one layer is directly connected to the neurons of the subsequent layer. 
        - A fully connected, two-layered MLP architecture was used and sigmoidal activation functions.
        - MLP networks can be used to estimate missing values by training an MLP to learn the incomplete features (used as outputs),using the remaining complete features as inputs.
    - Self-organisation maps : 
        - An SOM is a neural network model made out of a set of nodes (or neurons) that are organised on a 2D grid and fully connected to the input layer.
        - The training of a basic SOM is performed using an iterative process. After the weight vectors are initialised, they are updated using all input training vectors.
        - After the SOM model has been trained, it can be used to estimate missing values. 
    - K-nearest neighbours : 
        -  the KNN imputation algorithm uses only similar cases with the incomplete pattern. 
        -  Given an incomplete pattern x, this method selects the K closest cases that are not missing values in the attributes to be imputed (i.e., features with missing values in x), such that they minimise some distance measure.
        -  The optimal value of K is usually chosen by crossvalidation.
        -  Calculation of replacement value depends on the type of data;
            - example, the mode is selected for discrete data (categorical data),
            - while the mean is used for numerical data (continuous data).
    - The ANN prognosis model : 
        - numerical simulations are performed on the data imputed by the methods described above on neural networks comprising a single hidden layer with the number of neurons between 2 and 50.
        
####  Model evaluation
- The accuracy of the prognosis models is evaluated by testing two main properties: 
    - discrimination and calibration. Discrimination is the ability to separate patients with and without a relapse event.
    - Calibration is the ability to correctly estimate the risk or probability of a future event. 

### Conclusions
```{epigraph}
machine learning techniques may be the best approach to imputing missing values, 
as they led to statistically significant improvements in prediction accuracy. 
Imputation techniques depend on the available data and the prediction model used. 
Also, these results might not generalise to different data sets

```

## closing 

- Volunteers for paper presentation: Chamudi & Lily 

--------------------------------------------------------------------------------------


# MLSS

# 2022-02-02
Lead Scribe: Damon Coffey

Roles for computing in social change
-concerns about fairness, bias and accountability in the field

Introduction:
- high stakes decision making algorithms have potential to predict outcomes more accurately
- cs has generally failed to target the correct point of intervention
- ex: intervention at the selection phase in employment context could prevent a hostile work place

Computing as a Diagnostic
- computing can help us measure social problems and diagnose how they manifest in tech systems
- computing cannot solve issues on its own
- Diagnostics work can be valuable
    - highlight tech dimensions of social problems
- misinformation can negatively affect marginalized populations more ex: search engines displaying low quality health information

- not presented as solutions, rather as tools to document practices
    - not to confuse diagnostics with treatment
    - computing is not unique in helping diagnose social problems
        - sociology, etc..
    - certain tools can be treated as certainity for every situation, which is not the case

Computing as a Formalizer
- computing requires explicit specification of inputs and goals
- these inputs and goals can be affected by transperency, accountability and stake holder participation
    - need to be precise
ex: risk assessment: debate over how to formalize pretrial risk, if and how to use these instruments
- not all data is easy to quantify
- may press people to rely on measures that are incorrect

Computing as Rebuttal
- computing can clarify the limits of technical interventions and of policies promised on them
- limits of computing can drive people to reject computational approaches
- ex: using an algotrithm to determine an immigrants societal worth, not good. Should seek a differnt method rather than forcing a technological one
- need to understand what algorithms are actually capable of, instead of forcing it on everything
    - need to show what an algorthm CANT do (prove limits)
- prediction algorithms for risk assessment
- computational research on fairness is built on discrimination law
- Risks
    - proclomations of what a computational tool is incapable of may focus on improving tool even if it is not possible

Computing as a Synecdoche
- computing can foreground long standing social problems in a new way
- Eubank's core concern: computing is just one mechanism through which longstanding poverty policy is manifested
- Automated systems can divert poor people from the resources they need
- computing can help bring attention to old problems, however

- synecdochal focus on computing must walk a pragmatic line between over emphasis on tech aspects and recognition of the work tech actually does
- need to find a balance between the two and develop better systems with more emphasis on social issues







--------------
# 2022-01-31

Lead Scribe: Derek Jacobs

## admin 

- grading contract will be posted in time for Wednesday
- notes & posting [example](https://github.com/ml4scisoc/ml4scisoc.github.io/pull/4)
- can leave out admin in notes; that material wil mostly be other places

## Opening Notes

- set the stage for how we think about other work and setting up your projects



## Scientific Method in the Science of Machine Learning 
 [paper](https://arxiv.org/abs/1904.10922) 


### Introduction
- ML is having a hard time explaining some results
- Replications are failing 


### Scientific Method

```{epigraph}
Starting from the assumption that there exists accessible ground truth, the scientific method is a systematic framework for experimentation that allows researchers to make objective statements about
phenomena and gain knowledge of the fundamental workings of a system under investigation.

-- Jessica Zosa Forde and Michela Pagnini
```
- process and a social contract
    - ML might not be systematic
        - Control the randomness of our algorithms
    - Procedures/Trust allow comparisons of results
- assumes a ground truth
    - Things can go wrong if there simply isn\'t a ground truth
    - Especially when using ML in social context
- Hypotheses
    - A formed "guess"
    - In CS, the learning process is as follows
        - Here's a problem (that has an answer)
        - Write code to solve it to specifications
    - Hypotheses can be falsified through statistical and other analysis
        - You can prove the opposite is not true, but challenging to prove truth

you can express hypotheses as priors, but that prior wouldnt be the same in the rest of ML lit

```{admonition} Discuss
When might this not apply? 
```


```{epigraph}
At the base of scientific research lies the notion that an experimental outcome is a random variable, and that appropriate statistical machinery must be employed to estimate the properties of its
distribution. 
```
 
- Treat your accuracies as a random variable as part of an experiment and you're experimenting around those
- In stats people chase having p values <= 0.05 and so we have a reproducibility crisis
- [Reproducibility Study](https://osf.io/ezcuj/wiki/home/)
    - < 40% replicated the original results

- there are some problems with NHST but there are alternatives that are still rigorous
    - [for design research](https://schmettow.github.io/New_Stats/index.html#what-new-stats)
    - [in psych](https://www.psychologicalscience.org/members/new-statistics)
    - [bayesian in hci](https://www.mjskay.com/papers/chi_2016_bayes.pdf)
        - Bayesian
            - Priors allowed
            - More broadly defined
            - Everything we do is influenced by our thoughts and so there's some subjectivity
            - Interpreting results in terms of previous results
        - Frequentist
            - No Priors
            - Probabilities strictly refer to events like fair coin flips (100 flips we expect 50 heads 50 tails)
            - Knowledge does not accrue

### Case study

HEP:
- proposed thoery
- null hypothesis
- cafeull accounting
- model building and hypothesis testing phases
- parametric models derived from first prcinicples
- statistical test is constructed

ML Analogy: 
- suspect new activation
- formulate quantitative hypothesis
    - How will it work, what'll it do, how much will it improve
    - And behavior of how it'll change
- run experiments
    - Record outcomes from base models (no intervention)
- This is a statistical model of your experiment, not an actual model
    - Dataset, optimizer, init, hyperparameters, etc are just noise in the question of "does the activation function work"
    - Or make things specific (improve results with a specific dataset)

### Recommendations


**1. formulate hypotheses first
2. statistical testing**
3. operate in controlled,
reproducible, and verifiable settings
4. negative result workshops 
    - [pregistration workshop at neurips 2021](https://preregister.science/neurips2020.html) not an author as speaker
        - If your experimental plan is good, results are published regardless of positive or negative case
    - [new journal](https://www.jmlr.org/tmlr/editorial-policies.html)

## Value Laden Shifts in ML

[paper](https://arxiv.org/abs/1912.01172)
@brownsarahm reminder from lily
**talk on incorporating ethics into teaching data structs - environmental cost of algorithms**

- Looking at how different values influence what is being done in ML
- disciplinary shifts are not objective, but value laden
- Model Types
    - Different categories of models typically used for specific purposes
    - The structure of what our learning algorithm outputs
    - e.g. CNN for image processing, Linear Models, SVMs, etc

### Model types as organizing 

- many researchers self-organize in types; eg for revieing, workshops etc
    - How do we organize them in a package like sklearn, but also "who knows who works on this"
- commitment is fueled by exemplars
- has down stream effects: 
    - guide research agenda and problem selection
        -  How model types influence problem selection
            - Different types are tailored to different problems
            - Most popular model means most funding
            - More funding on specific models drives improvements to that area specifically and other problems get lost
    - constrain search for solutions
    - prerequisites, eg deep learning  and data volume (fig 1) and compute power (fig2)
        - fig1
            - Depending on data amount, we may favor one model over the other, and that in turn is researched more
        - fig2
            - Shows over time how my computer power is used in training AI
            - Recently exponential growth
- model types have parallels but important differences in philosophical scientific organzing principles
    - decreases theory development
    - Kuhn
        - The organizing paradigm defines what questions are valid
        - For example
            - If we only have earth water fire ether, we can't ask what molecules do
- When committed to model types...
    - The whole industry shifts towards it
    - Like NVidia GPUs, computer architectures, etc

### Model type is self-reinforcing 

- comparing them is influenced by the model type points above (problems, prerequisites)

### Comparison between types is value laden 

- Applied to ImageNet
    - Benchmark image classification problem
    - Until 2011, best error rate was 25% (no deep learning)
    - 2012 - AlexNet reached 16% (deep learning)
    - By 2016 ImageNet is basicaclly "done" due to all extremely high accuracies (97% vs 97.1%)
- This doesn't mean the problem of image classification is solved
- prerequisites
    - compute
        - Who has access
    - data
        - Who has access
        - What sets are created/curated
- Evaluation criteria
    - in theories: as a whole, internal consistent, predictive, etc

```{epigraph}
Evaluating theories based on their theoretical
virtues is a value-laden activity when theoretical virtues are carriers
of values.

-- Milli and Dotan
```
- eg consistency requires keeping the bad from the old in new
- eg: metrics and discrimination
    - Something that was sexist previously is still now

### Conclusion

```{epigraph}
A related question inspired by these issues is who should make
decisions in what values are furthered? Who gets to have a voice?
In talking about selection of problems in science, Kitcher (2011)
argues that all sides should have a say, including laypersons [71].
A question for machine learning is: is the same true for machine
learning? Who should have a say about which criteria are important in evaluating model-types? That is itself another value-laden
question.
```

## Overall Paper thoughts

```{admonition} Discuss 
General thoughts?
```
- Think about things that're interesting, confusing, etc (for future reference)
- Take care when conducting ML
    - Feed in data, hope for the best without considering the "why's"

```{admonition} Discuss 
How is this different from how you've thougth about CS before?
```
- There's more to consider before actually coding
- Vast social influences in things as simple as "can i even get this dataset"
- We focus on what works now instead of what hasn't worked

```{admonition} Discuss 
How might the value-laden points about theory development relate the the scientific method points
```
- Two pillars of hypothesis + statistical testing

## Meta points
- (science) scientific mehtod one is a workshop paper (approx length of your project papers)
- this is a position paper (it's not about new experimental results as much as the classic research arguing a position apper)

## closing 

- volunteer: Emmely
- you can use this notes if you like 
- I can provide you "TA" access to prismia to draw there

  - [Roles for computing in social change](https://dl.acm.org/doi/abs/10.1145/3351095.3372871
  - See course site for notes on [expectations during presentations](https://ml4scisoc.github.io/syllabus/learning.html#presentations)

-----------------------------------------
