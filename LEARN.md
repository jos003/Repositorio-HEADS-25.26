[[LEARN-Work]]
[[LEARN-Resumos]]
# 24/02/2026

## 2.01_Machine Learning and Data Mining

**Start your engines!**
Pedro Pereira Rodrigues
PhD Programme in Health Data Science

### Evidence Based Medicine
Conscient, explicit and criterious use of the best available evidence in clinical decision.

The cycle of evidence-based practice shows that practice generates information, which is used in research. Research generates knowledge, which is applied to the patient. The patient generates a decision, which is used in practice.

### Real-World Biomedical Data
The complicated nature of real-world biomedical data has made it necessary to look beyond traditional biostatistics.

### Wealth of Health Data
The routine operation of modern healthcare systems produces a wealth of data in electronic health records, administrative databases, clinical registries, and other clinical systems.

### The 42 V's of Big Data and Data Science
Big Data concepts involve multiple dimensions commonly described as the V's of Big Data.

### Knowledge Discovery
It is widely acknowledged that there is great potential for utilizing these routine data for health research to derive new knowledge about health, disease, and treatments.

### Computational Statistics
Computational statistics is a branch of mathematical sciences concerned with efficient methods for obtaining numerical solutions to statistically formulated problems.

### Data Science
Study on creation, validation and transformation of data to generate meaning.

### Data Science Process & Workflow
The data science process begins with asking an interesting research question that guides the overall workflow of the data science project. Having a well-defined workflow for any data science project is less frustrating for any data professional to work on.

### Data Mining Lifecycle
The Data Mining cycle involves several steps revolving around Data: Business Understanding, Data Understanding, Data Preparation, Modeling, Evaluation, and Deployment. The lifecycle of a data science project is not definitive and can be altered accordingly to improve the efficiency of a specific data science project as per the research requirements.

### Clinical Knowledge Representation
Clinical cases are getting more and more complex, yielding the application of modelling techniques likewise increasingly complex.

### Computational Intelligence
For a computer to be intelligent, it has to be programmed appropriately. Ideally you would like to tell it only as much as it needs to know in a high-level language.

### Artificial Intelligence
* Artificial intelligence (AI) systems are software (and possibly also hardware) systems designed by humans that, given a complex goal, act in the physical or digital dimension.
* AI systems can either use symbolic rules or learn a numeric model, and they can also adapt their behaviour by analysing how the environment is affected by their previous actions.
* As a scientific discipline, AI includes several approaches and techniques, such as machine learning, machine reasoning, and robotics.

### Machine Learning
The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience.

* **Supervised Machine Learning Metaphor:** There is a teacher who teaches the system a concept, with which the student is able to classify new cases, and there is an error function for that classification.
* **Inductive Bias:** A learner that makes no a priori assumptions regarding the identity of the target concept has no rational basis for classifying any unseen instances.
* **Model Performance:** The generalization performance of a learning method relates to its prediction capability on independent test data.
* **Black Boxes:** Some machine learning techniques, although very successful from the accuracy point of view, are very opaque in terms of understanding how they make decisions.

### A Course on Machine Learning and Data Mining
This unit aims to empower students with the necessary knowledge and skills to:
* Interpret and apply machine learning techniques in health databases.
* Identify problems that can be addressed with data mining processes.
* Recognize the most common tasks of knowledge discovery (e.g., clustering, classification, association, regression).
* Apply and interpret the obtained results, according to technical accuracy and impact in the domain.

An introduction to the statistical programming language R will be presented as part of the course and students will be required to complete their assignments in R.

**Syllabus:**
* **Introduction:** includes a ML project in R
* **Classification & Validation:** includes cross-validation
* **Decision Trees:** includes random forests
* **Bayesian Networks:** includes classifiers
* **Neural Networks:** includes deep learning
* **Kernel Methods:** includes SVMs
* **Ensemble Models:** includes bagging and boosting
* **Association Rules:** includes Apriori
* **Cluster Analysis:** includes hierarchical clustering
* **Data Preprocessing:** includes missing data
* **Anomaly Detection:** includes outliers and rare events
* **Big Data - Big Models:** includes streams
* **Text Mining:** includes NLP
* **Visual Data Mining:** includes geospatial analysis

### Software Tools for Machine Learning
The primary software tool highlighted for the first machine learning project is **R**.
## 2.06_Learning and Evaluating Classifiers: Validation and Generalization of Models

### Evidence Based Medicine
Conscient, explicit and criterious use of the best available evidence in clinical decision.

The cycle of evidence-based practice shows that practice generates information, which is used in research. Research generates knowledge, which is applied to the patient. The patient generates a decision, which is used in practice.

### Real-World Biomedical Data
The complicated nature of real-world biomedical data has made it necessary to look beyond traditional biostatistics.

### Wealth of Health Data
The routine operation of modern healthcare systems produces a wealth of data in electronic health records, administrative databases, clinical registries, and other clinical systems.

### Knowledge Discovery
It is widely acknowledged that there is great potential for utilizing these routine data for health research to derive new knowledge about health, disease, and treatments.

### Data Science
Study on creation, validation and transformation of data to generate meaning.

### Clinical Knowledge Representation
Clinical cases are getting more and more complex, yielding the application of modelling techniques likewise increasingly complex.

### Machine Learning
The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience.

### Supervised Machine Learning Metaphor
There is a teacher who teaches the system a concept, with which the student is able to classify new cases, and there is an error function for that classification.

### Inductive Bias
An algorithm that learns automatically from a set of data looks for a hypothesis, in the space of possible hypotheses, that best fits the training data. Each algorithm chooses a representation for this hypothesis.
* The chosen representation represents a **representation bias**.
* The way the algorithm searches for the hypothesis represents a **search bias**.

A learner that makes no a priori assumptions regarding the identity of the target concept has no rational basis for classifying any unseen instances.

### Black Boxes
Some machine learning techniques, although very successful from the accuracy point of view, are very opaque in terms of understanding how they make decisions.

### Hypothesis Induction
Creating a model from a data set is to induce a hypothesis of association between factors (or between factors and a result), as opposed to deducing models from a theory.

We seek hypotheses as correct as possible, i.e. whose model thus formed fits the observed data as well as possible.

### Model Generalization
We can increase the complexity of the model in an attempt to improve:
* the representation of reality
* the adequacy of the model to the data
* the ability to support decisions
...but:

* **Overfitting:** We say that the model is overfitting, that is, that it overfits the seen data, memorizing them, when the performance in the test data is much lower than in the training data.
* **Underfitting:** We say that the model is underfitting, that is, that it did not adjust to the seen data, when the performance is low even in the training data.

*(Visualizing the predictive error: As model complexity increases, training error decreases steadily. However, the test sample error initially decreases but eventually starts to increase again due to overfitting. Low complexity represents high bias and low variance; high complexity represents low bias and high variance).*

### Model Performance
The generalization performance of a learning method relates to its prediction capability on independent test data.

### Evaluating Predictive Models
There is no universal technique for all induction problems! We need to evaluate each technique according to the objective of the studied problem:
* The theoretical evaluation can be exposed, for example, by the inductive characteristics (bias and variance) of the applied models.
* The controlled experimental evaluation must follow clear and transparent assumptions and procedures in order to guarantee the validity of the created models.

#### Error Metrics
The evaluation of a supervised model is usually performed by analyzing the performance in the classification of new cases, e.g:
* Proportion of correctly classified cases (accuracy, sensitivity, specificity, precision, F1, ...)
* Distance between predicted and actual values (e.g. mean squared error)

#### Understanding the Origin of the Error
But is it possible to understand / explain the origin of the error?
* The type of decision and the type of model built may make such an analysis impossible. The decision is usually based on the discrimination of a continuous value, e.g. a probability.
* The ROC curves allow the analysis of the impact of these parameters on the error.

### Estimating Generalized Error
Calculating the classification error on the same data used to train the model produces optimistic estimates, which is why it was agreed to call this the **apparent error** of the model.

We must use strategies for error estimation in alternative, independent samples. Sampling methods for estimating generalized error include:

#### 1. Holdout
A set of data is separated (e.g. 1/3) which are not used in training (derivation) of the model. Estimation of the error is calculated in these held out test set.
**Problems:**
* Estimate is pessimistic (final model trained with all the data will be better than just with the training set).
* It does not allow to evaluate the variability of performance with different combinations of the data (we may have ended up with an “easy” test set).
* How to choose the test set?

#### 2. Random Sampling (Random Subsampling)
The holdout procedure is repeated several times, with equal proportions but random selection of the test set. Estimation of the error is aggregated (e.g. mean and standard deviation) from among the various test sets.
*(Implemented in R's `caret` package as `method="LGOCV"`).*
**Problems:**
* It does not allow to evaluate performance in all existing cases (random selection does not guarantee that all cases have been used in a test set).

#### 3. K-folds Cross-validation
The data is divided into K sub-sets of equal size; K-1 are used for training, and the rest is the test set. The procedure is repeated K times, in order to use all the subsets as a test. Estimation of the error is aggregated (e.g. mean and standard deviation) from the predictions in the K test sets.
*(Implemented in R's `caret` package as `method="repeatedcv"`).*

**Specifications:**
* It is usual to perform the complete procedure several times (M) to allow different definitions of the groups, with the estimate to be aggregated among all M * K executions.
* It is usual to stratify the groups, i.e., to force that both the training set and the test set have similar class proportions.
* There are several studies that discuss the validity of the method, namely with regard to the optimism / pessimism of each estimate.

**Problems:**
* A portion of the training data is shared between the different runs (i.e. not independent).
* Aggregate performance estimate is still dependent on the division made.
* How to divide the data by the K groups?

#### 4. Leave-one-out Cross-validation
Equivalent to an N-folds cross validation, where N is the total number of cases in the set. Estimation of the error is aggregated in the N predictions made. Probably the most accurate estimate of the model's performance.
*(Implemented in R's `caret` package as `method="LOOCV"`).*
**Problems:**
* Computationally more demanding.
* Usually used only in small data sets.

#### 5. Bootstrap
Samples are drawn from the data set, with replacement, of the same size as the initial set, serving as training sets. Unchosen cases (~ 36.8%) serve as a test set. Procedure is repeated several times. The error estimate is aggregated from all iterations (equivalent to leave-one-out, but with less variance).
*(Implemented in R's `caret` package as `method="boot"`).*
**Problems:**
* Computationally very demanding.
* Usually used only in small data sets.
## Notes

LGOCV - Leave group out cross validation

No k-folds o professor costuma usar k = 2.
LOOCV - Leave one out cross validation

# 3/03/2026

## 3.1_Learning Tree Models: Decision Trees and Random Forests

### Evidence Based Medicine
Conscient, explicit and criterious use of the best available evidence in clinical decision.

The cycle of evidence-based practice shows that practice generates information, which is used in research. Research generates knowledge, which is applied to the patient. The patient generates a decision, which is used in practice.

### Real-World Biomedical Data
The complicated nature of real-world biomedical data has made it necessary to look beyond traditional biostatistics.

### Wealth of Health Data
The routine operation of modern healthcare systems produces a wealth of data in electronic health records, administrative databases, clinical registries, and other clinical systems.

### Knowledge Discovery
It is widely acknowledged that there is great potential for utilizing these routine data for health research to derive new knowledge about health, disease, and treatments.

### Data Science
Study on creation, validation and transformation of data to generate meaning.

### Clinical Knowledge Representation
Clinical cases are getting more and more complex, yielding the application of modelling techniques likewise increasingly complex.

### Machine Learning
The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience.

### Supervised Machine Learning Metaphor
There is a teacher who teaches the system a concept, with which the student is able to classify new cases, and there is an error function for that classification.

### Inductive Bias
An algorithm that learns automatically from a set of data looks for a hypothesis, in the space of possible hypotheses, that best fits the training data. Each algorithm chooses a representation for this hypothesis.
* The chosen representation represents a **representation bias**.
* The way the algorithm searches for the hypothesis represents a **search bias**.

A learner that makes no a priori assumptions regarding the identity of the target concept has no rational basis for classifying any unseen instances.

### Black Boxes
Some machine learning techniques, although very successful from the accuracy point of view, are very opaque in terms of understanding how they make decisions.

### The Iris Data Set
*(The presentation uses the Iris Data Set to visually demonstrate how algorithms create boundaries based on features like Sepal Length, Sepal Width, Petal Length, and Petal Width to classify setosa, versicolor, and virginica species).*

### Decision Tree Learning
Method for approximating discrete-valued target functions, in which the learned function is represented by a decision tree.

#### Appropriate Problems for Decision Tree Learning
* Instances are represented by attribute-value pairs.
* The target function has discrete output values.
* Disjunctive descriptions may be required.
* The training data may contain errors.
* The training data may contain missing attribute values.

### ID3 Algorithm
* Top-down approach.
* At each level, answers the question: “Which attribute should be tested to better discriminate the class?”
* Greedy search for an acceptable decision tree.
* Never backtracks to reconsider earlier choices.

#### Inductive bias of ID3
* Because of the subtle interaction between the heuristic attribute selection and particular found examples, it is difficult to characterize precisely the inductive bias exhibited by ID3.
* However, we can approximately define it as a **preference for short decision trees over complex ones**.
* Trees that place high information gain attributes close to the root are preferred over those that do not.

### Selecting the Best Attribute
So, which attribute is the best classifier? Measures are usually based on the posterior distribution of classes after the split.
* **Entropy** measures the impurity of a collection of examples for all *n* classes.
* **Information gain** measures the expected reduction in entropy.

What if we use *Date* as a predictor? There are so many possible values that we are bound to split into many small subsets, yielding high information gains. However, this does not translate into better predictors. Can we do better than information gain?

### C4.5
**Information gain ratio** penalizes attributes by incorporating a term, called split information or intrinsic value, that is sensitive to how broadly and uniformly the attribute splits the data, where *IV* is the entropy of the attribute variable.

#### Improvements from ID3
C4.5 (and later C5.0) improved ID3 by:
* Handling heterogeneous attributes.
* Handling missing values.
* Handling costs.
* Pruning trees after creation.
* Boosting.

### CART (Classification and Regression Trees)
* **Gini impurity** is a measure of how often a randomly chosen element from the set would be incorrectly labelled if it was randomly labelled according to the distribution of labels in the subset.
* **Variance reduction** is a broader estimate, also introduced in CART, for continuous target variables.

### Random Forests
* To avoid the heuristic decisions and reduce inductive bias of decision trees, random forests have been proposed.
* The idea is to combine the bagging approach and random selection of features:
  * Multiple bootstrapped samples are taken from the original data set.
  * A decision tree with randomly selected features is learned from each sample.
  * Final classification of the random forest is usually done by majority vote of the ensemble.

### Software Application: Using 'rpart' and 'caret'
*(Using the Breast Cancer Coimbra data set)*

* **rpart**: Used to build individual decision trees using Information Gain or Gini Impurity metrics, allowing for the visualization and summary of the decision nodes.
* **caret**: Used to train models with cross-validation (e.g., 3 times 10-fold CV), evaluate model accuracy, plot ROC curves, and compare the performance of standard Decision Trees (CART) versus Random Forests (`rf`). It also allows tuning complexity parameters (`cp` for trees, `mtry` for random forests).

### Exercise
Compare a decision tree with a random forest in the Cervical Cancer (Risk Factors) data set (available from UCI repository), trying to accurately classify Dx.Cancer.

## Notes

Offline learning - é usada uma base de dados.
Online learning - está sempre a ser alimentado; é mais difícil de ser alimentado.

greedy search - sempre para a frente.

devemos usar um preditor por cada 10/15/ou 20 casos positivos +/-

# 17/03/2026

## 4.1_Ensemble Machine Learning: Bagging, Boosting and Stacking

### Evidence Based Medicine
Conscient, explicit and criterious use of the best available evidence in clinical decision.

The cycle of evidence-based practice shows that practice generates information, which is used in research. Research generates knowledge, which is applied to the patient. The patient generates a decision, which is used in practice.

### Wealth of Health Data
The routine operation of modern healthcare systems produces a wealth of data in electronic health records, administrative databases, clinical registries, and other clinical systems.

### Knowledge Discovery
It is widely acknowledged that there is great potential for utilizing these routine data for health research to derive new knowledge about health, disease, and treatments.

### Machine Learning
The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience.

### Data Science
Study on creation, validation and transformation of data to generate meaning.

### Real-World Biomedical Data
The complicated nature of real-world biomedical data has made it necessary to look beyond traditional biostatistics.

### Clinical Knowledge Representation
Clinical cases are getting more and more complex, yielding the application of modelling techniques likewise increasingly complex.

### Supervised Machine Learning Metaphor
There is a teacher who teaches the system a concept, with which the student is able to classify new cases, and there is an error function for that classification.

### Ensemble Methods
Ensemble methods aim at improving the predictive performance of a given statistical learning or model fitting technique.

The general principle of ensemble methods is to construct a linear combination of some model fitting method, instead of using a single fit of the method.

### Content
We will cover:
* Bagging
* Boosting
* Stacking

### Bagging
Bootstrap aggregating is an ensemble method for improving unstable estimation or classification schemes.
* Introduced as a **variance reduction mechanism** for methods that do variable selection and fitting in a linear model.
* Popular due to its simplicity and popularity of bootstrap methods.

#### Algorithm
1. Create a bootstrapped sample of same size as original sample.
2. Compute the bootstrapped estimator (e.g., model derivation and error).
3. Repeat steps 1 and 2, M times, usually M = 50 or 100.

The bagged estimator is the average of all estimators (if M = inf then we would have an expected value for the estimator). The finite number M in practice governs the accuracy of the Monte Carlo approximation but otherwise, it shouldn’t be viewed as a tuning parameter for bagging.

#### Classification Options
For classification, two options apply:
* Compute the average of computed probabilities of each model
* Majority voting

Bagging improves the predictive performance of classification and regression trees. It is worth pointing out that bagging a decision tree is almost never worse (in terms of predictive power) than a single tree.

#### Variants
* **Subagging:** Subsample aggregating
* **Bragging:** Bootstrap robust aggregating

#### Disadvantages
* The main disadvantage of bagging, and other ensemble algorithms, is the lack of interpretation.
* A linear combination of decision trees is much harder to interpret than a single tree.
* Likewise bagging a variable selection-fitting algorithm for linear models gives little clues which of the predictor variables are actually important.

#### When to use

**Unstable Models:**
- Decision trees
- Small neural networks
- High-variance models
- Models sensitive to data perturbations

**Not Useful:**
- Linear regression (already stable)
- Any stable model (low variance)
- Low-variance models
- kNN with large k

Bagging + Feature Subsampling = Random Forest


### Boosting
Unlike bagging, which is a parallel ensemble method, boosting methods are sequential ensemble algorithms where the weights given to learned examples depend on the previous fitted functions.

Boosting has been empirically demonstrated to be very accurate in terms of classification (e.g., AdaBoost algorithm). Boosting algorithms often have **better predictive power** than bagging. For instance, across various datasets, boosting trees was found to be better than a single classification tree. The biggest loss for boosting in comparison with bagging was observed in datasets with very low misclassification error.

#### Algorithm
1. Learn the base model with the data.
2. Compute the gradient vector (loss function attributed to each case).
3. Repeat 1 and 2 with weighted data according to its error contribution.

The key idea is to give more weight to instances for which the error is higher, to improve the model in that direction.

Allows to **reduce the Bias** (and also variance).

#### Overfitting Risk

**Causes of Overfitting:**
• Too many iterations (large M)
• Learning rate too high
• Trees too deep
• Small or noisy dataset

**Regularization**
• Shrinkage (small γ, ~0.01–0.1)
• Early stopping via validation set
• Subsampling (stochastic GB)
• Limit tree depth
### Stacking
Stacking works by combining heterogeneous models learned on the same original data set. After learning the desired models, the outputs of the single models are combined using another model which takes them as inputs.

For example:
* Learn a decision tree, a k-nn and an SVM with the data.
* Stack the outputs of the three models using a linear model.

#### Correct Training (Out-of-Fold)

Correct Pipeline:
1. Split data into K folds
2. For each fold k:
	- Train each base model on the remaining K-1 folds
	- Generate out-of-fold predictions for fold k
3. Use all OOF predictions as features to train the meta-model

#### Meta-model

**Linear Meta-model**
- Linear / logistic regression
- Interpretable (weights = importance)
- Lower overfitting risk
- Good default choice

**Non-linear Meta-model**
- Random Forest, NN, etc.
- Captures complex interactions
- Higher overfitting risk
- Requires more data

| Method   | Reduces      | Type          | Execution       | Risks       |
| -------- | ------------ | ------------- | --------------- | ----------- |
| Bagging  | Variance     | Homogeneous   | Parallel        | Low         |
| Boosting | Bias (+var.) | Homogeneous   | Sequential      | Overfitting |
| Stacking | Both         | Heterogeneous | Parallel + meta | Leakage     |
### Critical condition for Ensamble Success

Low correlation between models

#### Interpretability vs Performance

Some ~ solutions for ensemble explainability:
• SHAP values: individual feature attribution per prediction
• Feature importance (global): which features contribute most
• Partial dependence plots: marginal effect of each feature

### Evaluation Metrics in Ensembles (and others)

Accuracy is insufficient, especially in imbalanced datasets (common in healthcare)

**AUC-ROC:** Overall discriminative ability; threshold-independent
**F1-Score:** Harmonic mean of precision and recall; useful for rare classes
**Calibration:** Predicted probability reflects actual event frequency
**Brier Score:** Mean squared error of probabilities; combines calibration and discrimination

### When NOT to Use Ensembles

Mandatory clinical explainability
- Regulation requires justifiable decisions (e.g., GDPR Art. 22, EMA guidelines)
Very small datasets
- Bootstrap or boosting amplify noise; simple models generalize better
Prohibitive computational cost
- Training hundreds of models in real-time may be infeasible in clinical production
Simple model is already sufficient
- If logistic regression achieves 95% AUC, the marginal gain doesn't justify complexity

### Advanced Extensions (Optional)

XGBoost / LightGBM / CatBoost
- Optimized gradient boosting implementations; native missing value handling, L1/L2 regularization, GPU support
Blending vs Stacking
- Blending uses a fixed holdout set; stacking uses K-fold. Blending is simpler but wastes data
Bayesian Model Averaging
- Weights models by their posterior probability; rigorous probabilistic framework for combination
Deep Ensembles
- Multiple neural networks with different initializations; epistemic uncertainty estimation
### Exercise
Build three ensemble classifiers for the Breast Cancer Coimbra data set (available from UCI repository) using the `caret` package, using:
* Bagging (`treebag` and `rf`)
* Boosting (`C5.0` and `gdm`)
* Stacking (at least three models)

**Useful packages:** `bag` and `caretEnsemble`

## Notes


Data leakage é o principal erro no inicio da carreira de Datascience.

Mais de 95% de área debaixo da curva é de desconfiar.

Catboost tem tido boa performance.

# 24/03/2026

## 5.01_Learning Bayesian Networks: Probabilistic Graphical Models and Classifiers

### Evidence Based Medicine
Conscient, explicit and criterious use of the best available evidence in clinical decision.

The cycle of evidence-based practice shows that practice generates information, which is used in research. Research generates knowledge, which is applied to the patient. The patient generates a decision, which is used in practice.

### Wealth of Health Data
The routine operation of modern healthcare systems produces a wealth of data in electronic health records, administrative databases, clinical registries, and other clinical systems.

### Knowledge Discovery
It is widely acknowledged that there is great potential for utilizing these routine data for health research to derive new knowledge about health, disease, and treatments.

### Data Science
Study on creation, validation and transformation of data to generate meaning.

### Real-World Biomedical Data
The complicated nature of real-world biomedical data has made it necessary to look beyond traditional biostatistics.

### Clinical Knowledge Representation
Clinical cases are getting more and more complex, yielding the application of modelling techniques likewise increasingly complex.

### Black Boxes
Some machine learning techniques, although very successful from the accuracy point of view, are very opaque in terms of understanding how they make decisions.

### Bayesian Reasoning
Formal process we use to update our beliefs about the world once we have observed some data.

### Bayesian Probability
Computes the probability that the hypothesis is true, updating the a priori probability about the hypothesis with the new incoming available data.

* **A priori probability:** Probability that the hypothesis is true, before the random experiment (e.g., P(heads) = 0.5).
* **A posteriori probability:** Probability that the hypothesis is true, after the random experiment (e.g., P(heads | 3 heads in 10 tosses) < 0.5).

#### Conditional Probability P(A|B)
Since you know that B has occurred, then B is the new (restricted) sample space for the random experiment where A is a possible event. That is:
P(A|B) = P(A ∩ B) / P(B)

### Bayes' Theorem
Taking advantages of the available set operations:
P(A ∩ B) = P(B)P(A|B) and P(B ∩ A) = P(A)P(B|A)
Then:
P(A|B) = [P(A)P(B|A)] / P(B)

### Competition of Ideas
In frequentist statistics, we often view hypothesis tests as an extension of parameter estimation. Here, we’ll think about hypothesis tests instead as a way to compare ideas with an important mathematical tool called the Bayes factor.

The Bayes factor is a formula that tests the plausibility of one hypothesis by comparing it to another. The result tells us how many times more likely one hypothesis is than the other. We’ll then see how to combine the Bayes factor with our prior beliefs to come up with the posterior odds, which tells us how much stronger one belief is than the other at explaining our data.

### Revisiting Bayes’ Theorem
P(H|D) = [P(H) × P(D|H)] / P(D)
* **P(H|D)** is the posterior probability, which tells us how strongly we should believe in our hypothesis, given our data.
* **P(H)** is the prior belief, or the probability of our hypothesis prior to looking at the data.
* **P(D|H)** is the likelihood of getting the existing data if our hypothesis were true.

But P(D) is often very hard to define. P(D) is also totally unnecessary if all we care about is comparing the relative strength of two different hypotheses. For these reasons, we often use the proportional form of Bayes’ theorem:
P(H|D) ∝ P(H) × P(D|H)

#### Ratio of Posteriors
We can use this to compare two hypotheses by examining the ratio of the prior belief multiplied by the likelihood for each hypothesis:
[P(H1) × P(D|H1)] / [P(H2) × P(D|H2)]
What we have now is a ratio of how well each of our hypotheses explains the data we’ve observed.

### Bayesian Knowledge Modeling
Bayesian statistical methods allow taking into account prior knowledge when analyzing data, turning the data analysis a process of updating that prior knowledge with biomedical and health-care evidence.

### Bayesian Networks
Bayesian networks offer a general and versatile approach to capturing and reasoning with uncertainty in medicine and health care. They describe the probability distribution governing a set of variables by specifying a set of conditional independence assumptions along with a set of conditional probabilities.

Each variable is a node in the network, and its dependency defined by their ascendants in the network, quantified by a conditional probability table.

#### Qualitative Model (Structure)
Consists of variables (nodes) and dependencies between variables (edges).
* **Defined by experts:** Categorical variables are included, considering three groups: Theories (risk or conditioning factors), Hypotheses (study outcomes), and Observations (symptoms or measurements). Dependencies are defined taking causality into account.
* **Interpreting the qualitative model:** When defined automatically from data, the quantitative model CANNOT be interpreted as a causal model! Dependencies are interpreted as association only. Direction (A -> B) indicates that having information on the conditioning (A) gives more information on the conditioned (B) than the reverse. Inexistence of a dependency is a clear assumption of independence. The model can be adjusted manually after being created from the data.

#### Quantitative Model (Parameters)
Consists of conditional probabilities for each variable state.
* **Defined by:** Expert (subjectively), Theories known in literature (high level of evidence), or Data from an original study.
* **Interpreting the quantitative model:** When defined by an original study, it should be evaluated according to the study design (Cohort, Case-control, Clinical trials) to understand if it represents risks or associations.

#### Interpreting Resulting Probabilities
* **When no evidence is included:** Probabilities are the marginal probabilities for each category, considering the dependencies of the multivariate model (a priori risk).
* **When evidence is included:** Probabilities are the marginal probabilities for the subgroups of patients defined by the evidence, considering the entire multivariate model (a posteriori risk).

### Bayesian Networks for Clinical Decision Support
Complex research questions can be addressed by the same model:
* **Etiology and risk:** Can a visit to China be the cause of patient's SARS?
* **Diagnosis:** The patient visited China; does he have SARS?
* **Prognosis:** The patient has fever and has visited China; without treatment, is he going to develop dyspnea?

*Different objectives require different models for the same problem (e.g., Confounding-adjusted risk estimation vs. Classification of new cases).*

### Supervised Machine Learning Metaphor
There is a teacher who teaches the system a concept, with which the student is able to classify new cases, and there is an error function for that classification.

### Machine Learning
The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience.

### Learning Structure from Data
* **Search-and-score methods:** Search algorithm selects a subset of high-quality Bayesian Networks; a quality measure (score) decides which candidate is the best.
* **Constraint-based structure learning:** Identifies the structure that best encodes a set of conditional dependence and independence assumptions.

**Hill-Climbing Strategy (Defined from data):**
1. Start with no dependencies.
2. Compute the likelihood of observing the data given the model.
3. Test all possible single dependencies, computing the respective likelihood.
4. If the likelihood increases above a given threshold, insert that dependency.
5. Repeat until the threshold is not reached by any new dependency.

### The Classifier Approach
While research often focuses on finding accurate estimates of association between factors and outcomes, there is no certainty that a model thereby defined will act as a good classifier. Classification requires the construction of a classifier that assigns a class label to instances described by a set of attributes.
*"I don't care if the OR for wine drinking and myocardial infarction is of risk (>1) or protection (<1)... I care that I can use that info to discriminate between patients who will develop the disease and those who won't!"*

### Naïve Bayes Classifier
One of the most effective classifiers. It makes a strong independence assumption: all the attributes are conditionally independent given the value of the outcome. P(A | B, C) = P(A | C).

### Augmenting the Naïve Bayes Classifier
Interdependencies between attributes can be addressed directly by allowing an attribute to depend on other non-class attributes. However, techniques for learning unrestricted Bayesian networks often fail to deliver lower zero-one loss than naive Bayes.

### Tree-Augmented Naïve Bayes (TAN) Classifier
TAN is a semi-naïve method. It relaxes the attribute independence assumption by employing a tree structure, in which each attribute only depends on the class and one other attribute. It uses a maximum weighted spanning tree that maximizes the likelihood of the training data.

### Preprocessing for Naïve Bayes
Before running models, preprocessing techniques like Box-Cox transformations, scaling, and centering can be applied to continuous variables to adjust data distribution.

### Exercise
Build a Tree-Augmented Naïve Bayes with the Cervical Cancer (Risk Factors) data set (available from UCI repository), trying to accurately classify Dx.Cancer.


# 07/04/2026


## Notes

**Assignment 1**

Consider the the Cervical Cancer (Risk Factors) data set (available from UCI repository) and try to accurately classify Dx.Cancer.

You must compare different approaches and parameters of a) single decision tree and b) random forest.
Evaluation of derived models should follow a correct methodology, comparing different estimates of generalization error (i.e. holdout, cross-validation, bootstrap, ...)
Submit a report (in PDF, generated from R) with the code and the resulting analysis.

**Assignment 2**

Consider the the Cervical Cancer (Risk Factors) data set (available from UCI repository) and try to accurately classify Dx.Cancer.

You must compare different approaches and parameters of support vector machines.
Evaluation of derived models should follow a correct methodology, comparing different estimates of generalization error (i.e. holdout, cross-validation, bootstrap, ...)

Submit a report (in PDF, generated from R) with the code and the resulting analysis.

# 14/04/2026

## 6.1_Support Vector Machines: Finding Optimal Separability

### Evidence Based Medicine
Conscient, explicit and criterious use of the best available evidence in clinical decision.

The cycle of evidence-based practice shows that practice generates information, which is used in research. Research generates knowledge, which is applied to the patient. The patient generates a decision, which is used in practice.

### Real-World Biomedical Data
The complicated nature of real-world biomedical data has made it necessary to look beyond traditional biostatistics.

### Wealth of Health Data
The routine operation of modern healthcare systems produces a wealth of data in electronic health records, administrative databases, clinical registries, and other clinical systems.

### Knowledge Discovery
It is widely acknowledged that there is great potential for utilizing these routine data for health research to derive new knowledge about health, disease, and treatments.

### Data Science
Study on creation, validation and transformation of data to generate meaning.

### Clinical Knowledge Representation
Clinical cases are getting more and more complex, yielding the application of modelling techniques likewise increasingly complex.

### Machine Learning
The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience.

### Supervised Machine Learning Metaphor
There is a teacher who teaches the system a concept, with which the student is able to classify new cases, and there is an error function for that classification.

### Inductive Bias
An algorithm that learns automatically from a set of data looks for a hypothesis, in the space of possible hypotheses, that best fits the training data. Each algorithm chooses a representation for this hypothesis.
* The chosen representation represents a **representation bias**.
* The way the algorithm searches for the hypothesis represents a **search bias**.

A learner that makes no a priori assumptions regarding the identity of the target concept has no rational basis for classifying any unseen instances.

### Black Boxes
Some machine learning techniques, although very successful from the accuracy point of view, are very opaque in terms of understanding how they make decisions.

### Linear Classification
We can always divide the input space into a collection of regions labelled according to the classification.
The boundaries of these regions can be rough or smooth, depending on the prediction function. For an important class of procedures, these decision boundaries are linear; this is what we will mean by linear methods for classification.

A more direct approach is to explicitly model the boundaries between the classes as linear. For a two-class problem in a p-dimensional input space, this amounts to modelling the decision boundary as a hyperplane.

Methods include:
* Perceptron
* Optimal Separating Hyperplane

#### Linear Decision Boundaries
Fit linear regression models to the class indicator variables, and classify to the largest fit. The decision boundary between two classes is that set of points for which prediction done by the two linear models is the same.

Any linear monotone transformation of the discriminant function will create linear decision boundaries. For example, using the *logit* function – log[p/(1-p)] - the decision boundary is the set of points for which the log-odds are zero.
Methods that use *logit*:
* Linear discriminant analysis (LDA)
* Linear logistic regression

Linear discriminant analysis and logistic regression both estimate linear decision boundaries in similar but slightly different ways.

#### Discriminant-based Classification
Model discriminant functions for each class, and then classify points to the class with the largest value for its discriminant function.

#### Generalized Linear Discriminants
Linear functions in the augmented space map down to functions of higher order in the original space: hence linear decision boundaries expand to higher order decision boundaries.

Working over projections: Although the line joining the centroids defines the direction of greatest centroid spread, the projected data overlap because of the covariance. The discriminant direction minimizes this overlap for Gaussian data.

### Separating Hyperplane Classifiers
These procedures construct linear decision boundaries that explicitly try to separate the data into different classes as well as possible.
* Included in an example with multiple separating hyperplanes, the least squares solution to the problem does not always do a perfect job in separating the points, and might make errors. This is the same boundary found by LDA, in light of its equivalence with linear regression in the two-class case.

### Perceptrons
Classifiers that compute a linear combination of the input features and return the sign of the response.

**Perceptron Learning Algorithm:** The perceptron learning algorithm tries to find a separating hyperplane by minimizing the distance of misclassified points to the decision boundary.

### Optimal Separating Hyperplanes
The optimal separating hyperplane separates the two classes and maximizes the distance to the closest point from either class.

* Provides a unique solution to the separating hyperplane problem.
* By maximizing the margin between the two classes on the training data, this leads to better classification performance on test data.
* The set of conditions of the optimization problem ensure that all the points are at least a signed distance M from the decision boundary, and we seek the largest such M and associated parameters.
* The optimal separating hyperplane produces a function for classifying new observations. Although none of the training observations fall in the margin (by construction), this will not necessarily be the case for test observations. The intuition is that a large margin on the training data will lead to good separation on the test data.

The description of the solution in terms of **support points** seems to suggest that the optimal hyperplane focuses more on the points that count, and is more robust to model misspecification. The LDA solution, on the other hand, depends on all of the data, even points far away from the decision boundary. Note, however, that the identification of these support points required the use of all the data.

When a separating hyperplane exists, logistic regression will always find it, since the log-likelihood can be driven to 0 in this case. When the data are not separable, there will be no feasible solution to this problem, and an alternative formulation is needed. Again one can enlarge the space using basis transformations, but this can lead to artificial separation through over-fitting.

### When Classes Overlap...
Suppose now that the classes overlap in feature space. One way to deal with the overlap is to still maximize M, but allow for some points to be on the wrong side of the margin.
We modify the constraint to measure overlap relative to the width of the margin, keeping the problem convex.

### Support Vector Classifier
The tuning parameter of this procedure is the **cost parameter C**.
* Points on the wrong side of the boundary are **support vectors**.
* Points on the correct side of the boundary but close to it (in the margin), are also **support vectors**.
* Larger values of C focus attention more on (correctly classified) points near the decision boundary, while smaller values involve data further away.
* Either way, misclassified points are given weight, no matter how far away.

*(Example with Iris Data set shows that a smaller C creates a larger margin with more points as support vectors, while a very large C creates a narrower margin).*

### Support Vector Machines (SVM)
Produces nonlinear boundaries by constructing a linear boundary in a large, transformed version of the feature space.

As with other linear methods, we can make the procedure more flexible by enlarging the feature space using basis expansions such as polynomials or splines. Generally linear boundaries in the enlarged space achieve better training-class separation, and translate to nonlinear boundaries in the original space.

The support vector machine classifier is an extension of this idea, where the dimension of the enlarged space is allowed to get very large, infinite in some cases.

It might seem that the computations would become prohibitive. In fact, due to the representation of the optimization problem involving only inner products, we need not specify the transformations *h(x)* at all, but require only knowledge of the **kernel function** that computes inner products in the transformed space.

**Three popular kernels:**
* *dth*-Degree polynomial
* Radial basis
* Neural network

In examples, the radial basis kernel usually performs the best (close to Bayes optimal), as might be expected given the data arise from mixtures of Gaussians.

### Software Application: Using R for SVM
*(Using `e1071` and `caret` packages)*
* **`e1071`:** Used to build SVM models using `svm()` by defining different kernels (e.g., `kernel="linear"` or `kernel="radial"`). Also offers the `tune()` function to optimize parameters like `cost` (C) and `gamma` via cross-validation.
* **`caret`:** Used to run algorithms using cross-validation (e.g., 3 times 10-fold CV) with methods like `svmLinear` and `svmRadial`. It evaluates models using ROC, Sensitivity, and Specificity, enabling direct comparison and plotting of the results.

### Exercise
Build a SVM for the Cervical Cancer (Risk Factors) data set (available from UCI repository), trying to accurately classify Dx.Cancer.

# 28/04/2026

## 7.1_OLD_Artificial Neural Networks: From the Perceptron to the Neuron

### Evidence Based Medicine
Conscient, explicit and criterious use of the best available evidence in clinical decision.

The cycle of evidence-based practice shows that practice generates information, which is used in research. Research generates knowledge, which is applied to the patient. The patient generates a decision, which is used in practice.

### Real-World Biomedical Data
The complicated nature of real-world biomedical data has made it necessary to look beyond traditional biostatistics.

### Wealth of Health Data
The routine operation of modern healthcare systems produces a wealth of data in electronic health records, administrative databases, clinical registries, and other clinical systems.

### Knowledge Discovery
It is widely acknowledged that there is great potential for utilizing these routine data for health research to derive new knowledge about health, disease, and treatments.

### Data Science
Study on creation, validation and transformation of data to generate meaning.

### Clinical Knowledge Representation
Clinical cases are getting more and more complex, yielding the application of modelling techniques likewise increasingly complex.

### Machine Learning
The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience.

### Supervised Machine Learning Metaphor
There is a teacher who teaches the system a concept, with which the student is able to classify new cases, and there is an error function for that classification.

### Inductive Bias
An algorithm that learns automatically from a set of data looks for a hypothesis, in the space of possible hypotheses, that best fits the training data. Each algorithm chooses a representation for this hypothesis.
* The chosen representation represents a **representation bias**.
* The way the algorithm searches for the hypothesis represents a **search bias**.

A learner that makes no a priori assumptions regarding the identity of the target concept has no rational basis for classifying any unseen instances.

### Black Boxes
Some machine learning techniques, although very successful from the accuracy point of view, are very opaque in terms of understanding how they make decisions.

### Linear Classification
We can always divide the input space into a collection of regions labelled according to the classification.
The boundaries of these regions can be rough or smooth, depending on the prediction function. For an important class of procedures, these decision boundaries are linear; this is what we will mean by linear methods for classification.

A more direct approach is to explicitly model the boundaries between the classes as linear. For a two-class problem in a p-dimensional input space, this amounts to modelling the decision boundary as a hyperplane.

Methods include:
* Perceptron
* Optimal Separating Hyperplane

Any linear monotone transformation of the discriminant function will create linear decision boundaries. For example, using the *logit* function – log[p/(1-p)] - the decision boundary is the set of points for which the log-odds are zero.
Methods that use *logit*:
* Linear discriminant analysis (LDA)
* Linear logistic regression

#### Linear Decision Boundaries
Fit linear regression models to the class indicator variables, and classify to the largest fit. The decision boundary between two classes is that set of points for which prediction done by the two linear models is the same.

#### Discriminant-Based Classification
Model discriminant functions for each class, and then classify points to the class with the largest value for its discriminant function.

#### Linear Discriminants
Methods that define optimal separating hyperplanes for the case when two classes are linearly separable.

#### Generalized Linear Discriminants
Linear functions in the augmented space map down to functions of higher order in the original space: hence linear decision boundaries expand to higher order decision boundaries.

#### Linear Discriminant Analysis and Logistic Regression
Linear discriminant analysis and logistic regression both estimate linear decision boundaries in similar but slightly different ways.

#### Separating Hyperplane Classifiers
These procedures construct linear decision boundaries that explicitly try to separate the data into different classes as well as possible.

### Perceptrons
Classifiers that compute a linear combination of the input features and return the sign of the response.

The perceptron uses a vector of real input values, computes a linear combination of those, and generates a value of 1 (if above a certain threshold) or -1 (otherwise).

The perceptron can be used to represent any primitive Boolean function AND, OR, ~AND and ~OR. This ability is extremely important given that all Boolean functions can be represented using these primitives. Moreover, every Boolean function can be represented with a network of perceptrons with at most two levels.

### Perceptron Learning
The perceptron learning mechanism looks to choose the weight values so that the output value is correct for each given instance.

The perceptron learning algorithm tries to find a separating hyperplane by minimizing the distance of misclassified points to the decision boundary.

Start with an admissible weight vector (e.g. random) and iteratively apply the perceptron to the examples, modifying the weights every time an example is misclassified. At each iteration the weights are updated using the perceptron training rule. The learning rate is usually a very low value and is many times decreased over the iterations.

It can be proved that this learning process converges in a finite number of iterations, with perfect classification of examples, as long as they are linearly separable.

#### Perceptron Learning Algorithm
If the classes are linearly separable, it can be shown that the algorithm converges to a separating hyperplane in a finite number of steps. However...

**Problems:**
* When the data are separable, there are many solutions, and which one is found depends on the starting values.
* The “finite” number of steps can be very large.
* When the data are not separable, the algorithm will not converge, and cycles develop; the cycles can be long and therefore hard to detect.

The goal is to minimize the error of misclassified data points, which is proportional to the distance of the misclassified points to the decision boundary.

The algorithm in fact uses stochastic gradient descent to minimize error. That is, instead of computing the sum of the (error-based) gradient contributions of each observation followed by a step in the negative gradient direction, a step is taken after each observation is visited. Hence the misclassified observations are visited in some sequence, and the parameters are updated via a multiplicative learning rate.

#### Perceptron Learning (Delta Rule)
What if examples are not linearly separable? Algorithm should converge to the best approximation of the concept described by the examples.

In order to do so, the delta rule uses gradient descent which is the basis of the Backpropagation algorithm used in networks with several units combined.

### Gradient Descent
Start by considering a linear perceptron. Then, we need to specify a way to measure the error of classifying the examples using a given set of weights.

Given the linear perceptron and quadratic error function, the error surface of possible weight hypotheses will always be a paraboloid with a single local minimum.

At each iteration, the weight vector is updated in the direction of the negative gradient, until the minimum is reached. This is done by computing the first derivative according to each component of the weight vector.

### Artificial Neural Networks
Learning methods based on artificial neural networks are suitable for problems where:
* Instances are represented by many attribute-value pairs.
* The target function may be discrete-valued, real-valued, or a vector of real- or discrete-valued attributes.
* The training examples may contain errors.
* Long training times are acceptable.
* Fast evaluation of the learned target function may be required.
* The ability of humans to understand the learned target function is not important.

These include **Feed-Forward Neural Networks** and **Feed-Backward Neural Networks**.

### Multi Layered Networks
Each neuron includes a non-linear activation function, although fully differentiable across the entire domain of the function, instead of the one used in the perceptron.

The use of a logistic function is biology-motivated given that it tries to take into account the refractory phase of real neurons.

The network includes one or more layers of hidden neurons, highly connected, that are neither input nor output. These will allow the model to learning more complex tasks, expanding the search space and dimensions.

However, the presence of distributed non-linearity and high connectivity disable a sound theoretical interpretation of the model. Also, the use of hidden neurons prevents a good visualization of the learning process.

#### Activation Functions
Each neuron receiving input from N neurons in the previous layer will output a transformation. Functions include:
* Linear
* Logistic
* Hyperbolic Tangent

Each weight will be updated easily since the derivative of these functions is expressed as a function of its output.

### Backpropagation
Since we must consider multiple exit values, we must redefine the error function as the sum of all errors in output neurons. The problem is that the compound error surface will now have multiple local minima, not necessarily the global minimum. Changes to the gradient descent are needed.

### Momentum
To avoid being stuck in local minima, we add a momentum term which tries to maintain the direction from previous update: Increasing the speed of adaptation in horizontal areas of the error surface, while preventing strict changes in direction.

### Deep Learning
The term deep learning refers to artificial neural networks with complex multilayers. To express complex models, deep learning has:
* more neurons,
* more complex ways of connecting layers,
* more computing power to train,
* automatic feature extraction.

Deep learning methods have been found to be fitting for big data study with remarkable success in speech recognition, computer vision, pattern recognition, recommendation systems, and natural language processing. Nowadays, the innovation of DL in image identification, object detection, image classification, and face identification tasks have great success.

One of the most common deep neural networks is the convolutional neural network (CNN).

The major concept of deep learning is learning data representations by increasing the quality of handling the ideas rather than events levels. Mostly in all levels, a significant amount of quality ideas or abstraction representation at an advance level are known through definition regarding fewer quality ideas or non-representations at the basic levels.

This type of stages of learning, growth or hierarchical process of learning is superb because it can enable a system to fathom complex or multi-complex presentations accurately from raw data. This superb characteristic is making deep learning applicable to different fields.

### Software Application: Playground
Tinker with a Neural Network right in your browser: https://playground.tensorflow.org/

### Exercise
Build a Neural Network for the Cervical Cancer (Risk Factors) data set (available from UCI repository), trying to accurately classify Dx.Cancer.

## Notes

As redes neuronais funcionam mal em dados tabulares.

As camadas escondidas chamam-se assim porque não têm interpretabilidade.

Explorar playground.tensorflow.org

# 12/05/2026

## 8.2_Deep Learning: From Perceptron to LLMs

**João Almeida | LEARN | HEADS**

### Summary
* How we got to LLMs:
  * Perceptron
  * CNN (Convolutional Neural Networks)
  * RNN (Recurrent Neural Networks)
  * LSTM (Long Short-Term Memory)
  * Transformers
* ChatGPT
* Usage

### Perceptron
The perceptron is the foundation of neural networks. It consists of input nodes that feed into hidden layers, which are fully connected to output nodes.
* Each neuron applies an activation function to a weighted sum of its inputs plus a bias term.
* **Weights and Bias:** Arrows represent learnable weights. The perceptron computes a linear combination before activation.
* **Learning Rate:** Indicates the pace at which the weights get updated (can be fixed or adaptively changed).

#### Activation Functions
Used at the end of a hidden unit to introduce non-linear complexities to the model:
* **Sigmoid:** S-shaped curve squashing outputs to (0,1). Used in binary classification but suffers from vanishing gradients.
* **Tanh:** S-shape but outputs in (-1,1). Zero-centred, better than sigmoid for hidden layers.
* **ReLU (Rectified Linear Unit):** Outputs 0 for negative inputs, identity for positive. Computationally cheap and avoids vanishing gradient; dominant in modern networks.
* **Leaky ReLU:** Like ReLU but allows a small negative slope for negative inputs, preventing dead neurons.

#### Training and Updating Weights
1. Take a batch of training data and perform forward propagation to obtain the prediction.
2. Calculate the loss using a loss function (e.g., cross-entropy) which measures the error between the prediction and the true label. The objective is to minimize this loss.
3. **Backpropagation:** Backpropagate the loss to get the gradients using the chain rule. The gradient measures how much the loss changes if the weight changes slightly.
4. **Gradient Descent:** Use the gradients to update the weights. If the gradient is positive, decreasing the weight reduces loss; if negative, increasing the weight reduces loss.

### Convolutional Neural Networks (CNN)
CNNs significantly reduce the number of parameters in the network and excel in image processing by recognizing edges, shapes, and patterns. They rely on the fact that pixels representing the same concepts are close to each other (local information).

**Architecture:**
* **Convolutional Layers:** Apply learned filters to detect local features. A small matrix (filter) slides over the input image.
* **Pooling Layers:** Downsample feature maps, reducing spatial size and parameters while retaining important features.
  * *Max pooling:* Selects the maximum value in each window (preserves strongest features).
  * *Average pooling:* Computes the mean of values in each window.
* **Fully Connected Layers:** Flatten the pooled features into a vector and produce class scores.
* **Stride:** Denotes the number of pixels by which the window moves after each convolution or pooling operation.

### Recurrent Neural Networks (RNN)
RNNs are used to label, classify, or generate sequences (e.g., time series analysis, natural language processing).
* Unlike feedforward networks, RNNs have loops in their connections, enabling information to carry over from one step to the next (memory of past inputs).
* **Advantages:** Can process input of any length, model size doesn't increase with input size, and weights are shared across time.
* **Drawbacks:** Computation is slow, and they suffer from the **vanishing/exploding gradient problem**, making it difficult to access information from a long time ago (short-term memory limitation).

### Long Short-Term Memory (LSTM)
Designed to solve the short-term memory limitations of standard RNNs.
* **Cell State:** Acts as long-term memory, like a conveyor belt running straight down the entire chain with minor linear interactions.
* **Hidden State:** Acts as short-term memory.
* **Gates:** Structures that optionally let information through, using a sigmoid neural net layer and pointwise multiplication.
  * *Forget Gate:* Decides what to erase from the cell state.
  * *Input Gate:* Decides what new information to write.
  * *Output Gate:* Controls what part of the cell state to expose as the hidden state.

### Transformers
Unlike RNNs, Transformers do not rely on sequential processing. They can operate in parallel over all tokens in a sequence.
* **Attention Mechanism:** "Attention Is All You Need". Attention layers tell the model to pay specific attention to certain words in a sentence and ignore others when dealing with the representation of each word.

**Architecture Components:**
* **Encoder:** Receives an input and builds a representation of it. Optimized for acquiring understanding (bi-directional attention).
* **Decoder:** Uses the encoder’s representation and previous outputs to generate a target sequence. Optimized for generating outputs (auto-regressive).

**Types of Models:**
* *Encoder-only:* Good for sentence classification, named entity recognition.
* *Decoder-only:* Good for generative tasks like text generation (modern LLMs).
* *Encoder-decoder (Sequence-to-sequence):* Good for translation or summarization (e.g., T5, BART).

### Large Language Models (LLMs)
Modern LLMs are usually Decoder-only architectures with billions of parameters. They work by predicting the probability distribution over sequences of tokens (predicting the next word).
* **Temperature:** Controls the randomness or creativity of the generated text. A low temperature (e.g., 0) creates deterministic, highly probable outputs. A high temperature (e.g., 0.8) generates more diverse outputs.
* **Hallucinations:** Models are optimized to predict the next token that fits the context, not to ensure factual accuracy. This can lead to factual inconsistencies or fabrications.

**Training Phases:**
1. **Pretraining:** Learning to predict the next token on vast amounts of text data.
2. **Instruction Tuning / Fine-Tuning:** The model is fine-tuned to follow instructions and generate helpful responses (often using Reinforcement Learning from Human Feedback - RLHF).

**Techniques for Improvement:**
* **Fine-Tuning:** Updating the model's weights to adapt its behavior, writing style, or vocabulary.
* **RAG (Retrieval Augmented Generation):** Connecting the LLM to a vector database to search for relevant external data before generating a response, helping with Q&A and factual accuracy.
* **Reasoning Models:** Using reinforcement learning to incentivize step-by-step reasoning capabilities (e.g., DeepSeek-R1 multi-stage training phases).

### ChatGPT
Generative Pre-trained Transformer (GPT) is a series of language models developed by OpenAI (GPT-1 to GPT-4).
* **Creation Steps:** Pretraining on massive datasets (Common Crawl, Wikipedia, Books) -> Fine-Tuning -> Reward Model (Manual grading) -> Reinforcement Learning from Human Feedback (RLHF).
* **Performance:** ChatGPT has successfully passed numerous professional exams, including the US Medical Licensing Examination (USMLE), US Bar Exam, Wharton MBA exam, and quantum computing exams.

### Prompt Engineering
The effectiveness of generative AI depends on the accuracy of communicating our needs. "Prompt Engineering" is crucial for articulating precise commands.
* **Summarization:** Ask for specific formats (e.g., "Summarize the clinical case in 2-3 bullet points").
* **Data Extraction:** Ask for structured outputs (e.g., "Extract information into a JSON object").
* **Role-based:** Define a persona (e.g., "You are a professor of biomedical data science...").

### Applications and Implications in Healthcare
* **Clinical Workflow:** Supporting clinical decision-making, evaluating imaging procedures, or writing patient letters (e.g., communicating diagnostic results).
* **Medical Education & Consultation:** Taking exams, providing cancer-related information, and addressing misconceptions.
* **Benefits:** Academic/scientific writing, benefits in scientific research, and healthcare practice improvements.
* **Risks & Concerns:** Ethical issues (bias, plagiarism, data privacy), risk of incorrect/inaccurate information, transparency issues, and copyright concerns.

## Notes

Hoje em dia o que se usa mais é o max polling.

# 19/05/2026

## 9.1.0_Inductive Modelling: Non-Supervised Learning

### Objectives
* Supervised vs non-supervised learning
* How to use and apply association rules
* How to create groups and make automatic classification

### Evidence Based Medicine
Conscient, explicit and discerning use of the best available evidence in clinical decision:
* personal clinical experience;
* best external clinical evidence from quality clinical research;
* values, needs, expectations and individual context of each patient.

The cycle of evidence-based practice shows that practice generates information, which is used in research. Research generates knowledge, which is applied to the patient. The patient generates a decision, which is used in practice.

### Data Science
There are a lot of small data problems that occur in big data. They do not disappear because you have got lots of the stuff. They get worse.

### Clinical Knowledge Representation
* Clinical knowledge is not shallow and therefore requires a decent knowledge representation method.
* Clinical cases are getting more and more complex, yielding the application of modelling techniques likewise increasingly complex.

### Knowledge Representation
What you mean to learn is the **concept**, but the result of the system is a **description** of that concept.

### Computational Intelligence
For a computer to be intelligent, it has to be programmed appropriately. Ideally you would like to tell it only as much as it needs to know in a high-level language.

### Machine Learning
The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience.

### Knowledge Modelling
* **Modelling:** The complicated nature of real-world biomedical data has made it necessary to look beyond traditional biostatistics.
* **Model Creation:** A model creates structure and parameters from both knowledge and data & information.

### Non-Supervised Learning
The supervised learning paradigm relies on the metaphor that there exists a teacher who provides the system with knowledge about the concept to be learned, allowing the learner to classify new instances, evaluated by an error function. It predicts the value of outputs given a set of inputs by learning the conditional probability P(Y|X).

However, knowledge extraction is not always aimed at learning a concept intended to classify observed cases.

**Unsupervised Learning**
* Let X be an n-dimensional random variable. The objective is to learn the properties of the probability distribution P(X).
* We want to learn the joint probability of all variables, which is quite the challenge!
* The dimension of X is usually much higher than in supervised learning.
* The goal is to directly infer the properties of this probability density without the help of a supervisor or teacher providing correct answers or degree-of-error for each observation.

**Examples of Non-Supervised Learning:**
* **Principal Component Analysis (PCA):** Seeks to find low-dimensional subspaces with low probability that define the boundaries of regions with high probability.
* **Clustering analysis:** Aims to identify multiple convex regions with similar probability density.
* **Association rules:** Attempt to find succinct descriptions of regions with high density.

### Association Rules
**Objective:** To identify joint values of X that occur frequently in the dataset.
This approach is commonly applied to **binary variables** and is thus referred to as **market basket analysis**. Items that frequently take the value 1 together are typically considered to be associated.

Instead of searching for specific values where joint probability is high (which becomes intractable with many variables), we look for regions of the space that have high probability relative to their size and support.

* **Subset size:** The number of variables considered in the subset.
* **Support (or prevalence):** The proportion of cases in the dataset that satisfy the subset conditions.

#### APRIORI Algorithm
If the support threshold is set high enough, reducing the number of possible sets, their identification becomes computationally feasible.
1. The cardinality of the set of itemsets with support greater than *t* is small.
2. Any subset B that only has a subset of A will always have support greater than or equal to that of A.

To find frequent itemsets of size *m*, we only consider candidates whose (m−1)-sized subsets are all frequent.

**Rule Generation:**
If an itemset is split into two disjoint subsets, A and B (A⇒B), where A is the antecedent and B is the consequent:
* **Support:** Estimates the joint probability P(A and B).
* **Confidence:** The support of the rule divided by the support of the antecedent. Estimates conditional probability P(B|A).
* **Lift:** The confidence divided by the support of the consequent. Estimates the association measure. A lift > 1 suggests positive association, = 1 means independence, and < 1 indicates negative association.

*Note: These rules do not imply causality.*

**Challenges / Limitations:**
* Restrictive data format (requires binary transactional format).
* A support threshold is necessary for computational feasibility.
* Rules with high confidence or lift but low support will never be discovered under a high support threshold (e.g., rare adverse drug reactions).

### Automatic Classification (Clustering)
**Objective:** Grouping or segmenting a collection of objects into subsets ("clusters") such that those within each cluster are more closely related to one another than objects assigned to different clusters.

**Similarity/Distance Measures:**
* Continuous variables: Euclidean or Mahalanobis distance.
* Categorical variables: Hamming distance or Jaccard similarity.
* Mixed-type data: Gower's distance.

Different similarity measures lead to different clustering. Defining the correct distance measure for the specific problem is far more important than the choice of the clustering algorithm itself.

**Object Dissimilarity:**
* **Normalization:** There is often a need to weight attributes to prevent clusters from being defined by a single dominant attribute (e.g., dividing by average observed distance).
* However, normalizing is not always desirable. If the objective is to find natural groupings, it is beneficial to give more weight to attributes that best distinguish those groups.
* **Missing Data:** Handling missing data is critical (whether to remove instances, impute values, or consider missing pairs as similar).

### Clustering Algorithms
Clustering methods can be classified into three types:
1. **Combinatorial (partition-based) methods:** Operate directly on the data, minimizing an error function. (NP-hard problem, usually solved via greedy gradient descent).
2. **Mixture models:** Assume data are generated i.i.d. from a probability distribution.
3. **Mode-seeking methods:** Identify modes (peaks) in the data distribution.

#### K-means
An iterative gradient descent clustering algorithm designed for continuous variables using Euclidean distance.
1. Randomly choose *k* centroids.
2. Assign each remaining point to the cluster with the nearest centroid.
3. Recalculate centroids based on current members.
4. Repeat until no points change clusters.

To prevent convergence to poor local minima, initialize the algorithm with different sets of centroids and select the result that yields the lowest total intra-cluster distance.

#### Soft K-means (Expectation-Maximization / EM)
Similar to estimating a probability density based on a mixture of Gaussians.
* **E-step:** Compute the responsibility (probability) of each cluster for each object.
* **M-step:** Re-estimate the parameters of each component based on current responsibilities.
Results in a probabilistic assignment of objects to clusters rather than hard assignments.

#### K-medoids
Addresses K-means limitations (only quantitative variables, Euclidean distance dependency). Instead of computing a mean, it selects the existing object that minimizes intra-cluster distance (the medoid). Allows the use of any distance measure, but increases computational complexity.

### Which K? (Choosing the number of clusters)
This phenomenon is similar to overfitting in supervised learning!
* **Elbow Method:** Compute intra-cluster dissimilarity for each value of *k* and look for the "elbow" where increasing clusters brings diminishing returns.
* **Gap Statistic:** Compares the observed intra-cluster dispersion with the curve one would obtain if the data were uniformly distributed. The optimal number is the value that maximizes the gap between these two curves. Can correctly identify if optimal K=1.

### Hierarchical Clustering
Instead of searching for a fixed number *K*, we look at how a hierarchy of clusters is defined.
* **Agglomerative (Bottom-Up):** Start with individual instances and merge the two clusters with the smallest inter-cluster distance step by step.
* **Divisive (Top-Down):** Start with all instances in a single cluster and recursively split the cluster with the largest intra-cluster distance.

**Distance between clusters (Linkage):**
* **Average Linkage:** Average distance between all pairs of objects, one from each cluster. Good compromise, producing well-separated and compact clusters.
* **Complete Linkage:** Maximum distance between any two objects (most distant pair). Tends to produce compact but small clusters.
* **Single Linkage:** Minimum distance between any two objects (closest pair). Tends to produce larger, less compact clusters.

# 26/05/2026

## 10.1_Learning from data streams

PhD Programme in Health Data Science

Machine Learning and Data Mining

Pedro Pereira Rodrigues

FMUP / MEDCIDS / CINTESIS

### Evidence Based Medicine

"**Conscientious**, explicit and **judicious** use of the best available evidence in clinical decision"

### Real-World Biomedical Data

"The complicated nature of real-world biomedical data has made it necessary to look beyond traditional biostatistics."

### Wealth of Health Data

"The routine operation of modern healthcare systems produces a wealth of data in electronic health records, administrative databases, clinical registries, and other clinical systems."

### Big Data

The 42 V's of Big Data and Data Science

### Knowledge Discovery

"It is widely acknowledged that there is great potential for utilizing these routine data for health research to derive new knowledge about health, disease, and treatments."

### Computational Statistics

"Computational statistics is a branch of mathematical sciences concerned with efficient methods for obtaining numerical solutions to statistically formulated problems."

### Data Science

"Study on creation, validation and transformation of data to generate meaning."

### Clinical Knowledge Representation

"Clinical cases are getting more and more complex, yielding the application of modelling techniques likewise increasingly complex."

### Computational Intelligence

"For a computer to be intelligent, it has to be programmed appropriately. Ideally you would like to tell it only as much as it needs to know in a high-level language"

### Artificial Intelligence

"Artificial intelligence (AI) systems are software (and possibly also hardware) systems designed by humans that, given a complex goal, act in the physical or digital dimension."

"AI systems can either use symbolic rules or learn a numeric model, and they can also adapt their behaviour by analysing how the environment is affected by their previous actions."

"As a scientific discipline, AI includes several approaches and techniques, such as machine learning, machine reasoning, and robotics."

### Machine Learning

"The field of machine learning is concerned with **the** question of how to construct computer programs that automatically improve with experience"

### Supervised Machine Learning Metaphor

"There is a teacher who teaches the system a concept, with which the student is able to classify new cases, and there is an error function for that classification."

### Inductive Bias

"A learner that makes no a priori assumptions regarding the identity of the target concept has no rational basis for classifying any unseen instances."

### Model Performance

"The generalization performance of a learning method relates to its prediction capability on independent test data."

### Black Boxes

"Some machine learning techniques, although very successful from the accuracy point of view, are very opaque in terms of understanding how they make decisions."

### Data Streams

"Many sources produce data continuously. These continuous flows of data are called data streams."

### Data Streams vs Data Sets

|**Feature**|**Data Set**|**Data Stream**|
|---|---|---|
|Size|finite|infinite|
|Distribution / Ordering|i.i.d. / independent|non i.i.d. / dependent|
|Evolution|static|non-stationary|

### Data Stream Models

Different data stream models exist:

- insert-only or time series model: once an observation x is produced, it cannot be changed
    
- insert-delete or turnstile model: observations x can be deleted or updated
    
- accumulative or cash-register model: each observation x is an increment to a sum $X(t)=X(t-1)+x$
    

### Data Stream Management

"The main issue in data streams are blocking operators, i.e. queries that require the entire input to be available before they can give an exact output."

### Illustrative example

Find the maximum value in a sliding window over a sequence of numbers.

When we can store in memory all the elements of the sliding window, the problem is trivial and we can find the exact solution.

When the size of the window is greater than the available memory, there is no algorithm that provides an exact solution!

### Open Research Questions

- Approximate query processing techniques to evaluate queries that require an unbounded amount of memory.
    
- Sliding window query processing, both as an approximation technique and as an option in the query language.
    
- Sampling to handle situations where the flow rate of the input stream is faster than the query processor.
    
- The meaning and implementation of blocking operators (e.g., aggregation and sorting) in the presence of unending streams.
    

### Processing and Learning from Data Streams

"In these settings, traditional machine learning algorithms are obsolete."

### Learning from Data Streams

- The challenge problem for data mining is the ability to permanently maintain an accurate decision model.
    
- This issue requires learning algorithms that can modify the current model whenever new data is available at the rate of data arrival.
    
- Moreover, they should forget older information when data is outdated.
    
- In this context, the assumption that examples are generated at random according to a stationary probability distribution does not hold, at least in complex systems and for large time periods.
    
- In the presence of a non-stationary distribution, the learning system must incorporate some form of forgetting past and outdated information.
    
- Learning from data streams require incremental learning algorithms that take into account concept drift.
    
- Solutions to these problems require new sampling and randomization techniques, and new approximate, incremental and decremental algorithms.
    

Hulten & Domingos identified desirable properties of learning systems that are able to mine continuous, high-volume, open-ended data streams as they arrive:
1. incrementality
2. online learning
3. constant time to process each example using fixed memory
4. single scan over the training data, and
5. **taking** drift into account.

Algorithms that learn from data streams:
- must process examples at the rate they arrive
- use a single scan and fixed memory
- maintain a decision model at any time
- adapt to the most recent data
- might end-up with approximate results


### Incremental and decremental issues

The ability to update the decision model whenever new information is available is an important property, but it is not enough. Another required operator is the ability to forget past information.

Some data stream models allow delete and update operators. For example, sliding windows models require the forgetting of old information.

Learning algorithms need forgetting operators that reverse learning: decremental unlearning.

### Cost-performance measurement

- Learning from data streams **requires updating** the decision model whenever new information is available.
    
- This ability can improve the flexibility and plasticity of the algorithm in fitting data, but at some cost usually measured in terms of resources (time and memory) needed to update the model.
    
- It is not easy to define where **the trade-off is** between the benefits in flexibility and the cost for model adaptation.
    
- Learning algorithms exhibit different profiles.
    
- Algorithms with strong variance management are quite efficient for small training sets.
    
- Very simple models, using few free-parameters, can be quite efficient in variance management (for example, the Naïve Bayes classifier) and effective in incremental and decremental operations, being a natural choice in the sliding windows framework.
    
- The main problem with simple approaches is the boundary in generalization performance they can achieve; they are limited by high bias.
    
- Complex tasks requiring more complex models increase the search space and the cost for structural updating.
    
- These models require efficient control strategies for the trade-off between the gain in performance and the cost of updating.
    

### Monitoring Learning

Whenever data flows over time, it is highly **improbable** the assumption that the examples are generated at random according to a stationary probability distribution.

At least in complex systems and for large time periods, we should expect changes (smooth or abrupt) in the distribution of the examples.

A natural approach for these incremental tasks is adaptive learning algorithms, incremental learning algorithms that take into account concept drift.

### Change Detection

Concept drift means that the concept about which data is being collected may shift from time to time, each time after some minimum permanence.

The evidence for changes in a concept is reflected in some way in the training examples.

Old observations, that reflect the behaviour of nature in the past, become irrelevant to the current state of the phenomena under observation and the learning agent must forget that information.

The nature of change is diverse. Changes may occur in the context of learning, due to changes in hidden variables, or in the characteristic properties of the observed variables.

Most learning algorithms use blind methods that adapt the decision model at regular intervals without considering whether changes have really occurred.

Much more interesting are explicit change detection mechanisms.

The advantage is that they can provide meaningful description (indicating change-points or small time-windows where the change occurs) and quantification of the changes.

They may follow two different approaches:

- Monitoring the evolution of performance indicators adapting techniques used in Statistical Process Control.
    
- Monitoring distributions on two different time windows. The method monitors the evolution of a distance function between two distributions: data in a reference window and in a current window of the most recent data points.
    

### Change Detection Research Problems

- The main research issue is to develop methods with fast and accurate detection rates with few false alarms.
    
- A related problem is: how to incorporate change detection mechanisms inside learning algorithms.
    
- Also, the level of granularity of decision models is a relevant property, because it can allow partial, fast and efficient updating in the decision model instead of rebuilding a complete new model whenever a change is detected.
    
- Finally, the ability to recognize seasonal and re-occurring patterns is an open issue.
    

### Evaluating stream learning methods

The design of experimental studies is of paramount importance.

It is a necessary condition, although not sufficient, to allow reproducibility, that is the ability of an experiment or study to be accurately replicated by someone else working independently.

Dietterich proposes a straightforward technique to evaluate learning algorithms when data is abundant: "learn a classifier from a large enough training set and apply the classifier to a large enough test set."

Data streams are open-ended; this could facilitate the evaluation methodologies, because we have train and test sets as large as desired.

The problem is: Is this sampling strategy viable in the streaming scenario? No! Two aspects in the emerging applications and learning algorithms that have strong impact in the evaluation methodologies are:

- the continuous evolution of decision models, and
    
- the non-stationary nature of data streams.
    

Sequential analysis refers to the body of statistical theory and methods where the sample size may depend in a random manner on the accumulating data.

The prequential method is a general methodology to evaluate learning algorithms in streaming scenarios.

### Prequential error estimation

In predictive sequential (or prequential) the error of a model is computed from the sequence of examples.

For each example in the stream, the actual model makes a prediction based only on the example attribute-values.

Prequential evaluation provides a learning curve that monitors the evolution of learning as a process.

Using holdout evaluation, we can obtain a similar curve by applying, at regular time intervals, the current model to the holdout set.

It is known that the prequential estimator is pessimistic: under the same conditions it will report somewhat higher errors.

The prequential error estimated over all the stream might be strongly influenced by the first part of the error sequence, when few examples have been used **to** train the classifier.

Incremental decision models evolve overtime, improving their performance.

The decision model used to classify the first example is different from the one used to classify the hundredth instance.

This observation leads to the following hypothesis: compute the prequential error using a forgetting mechanism.

This might be achieved either using a time window of the most recent observed errors or using fading factors.

Considering a sliding window of size infinite or a fading factor equal to 1, these forgetting estimators equal the prequential estimator.

### Exercise

Using the stream package in R, simulate a learning environment where:

a) data is produced in a stream from $N(0,2)$

b) positive class is determined by data being lower than 2

c) classification is performed by the default classifier (always positive)

d) after 1000 data points, stream changes to $N(2,2)$

e) compute and monitor the prequential error using zero-one loss and four different window models

Incorporate a change detection mechanism into the learning environment monitor.

For example, trigger an alarm if the prequential error rises above a statistical boundary such as:

$\text{warning}: err + stdev > \min(error) + 2 \times \min(stdev)$

$\text{drift}: err + stdev > \min(error) + 3 \times \min(stdev)$
# 2/06/2026

## 11.2_Anomaly detection

### Summary
* **Definition:** Observation which deviates so much from other observations as to arouse suspicion it was generated by a different mechanism.

### When it is used
* Data cleaning
* Predictive maintenance
* Network security
* Financial fraud
* Signal software errors

**The bottom line is:** Know what is expected and detect what deviates from it.

### Motivation for Unsupervised Anomaly Detection
* Why use unsupervised machine learning algorithms for anomaly detection?
  * Sometimes you don't know the data. i.e., you don't know how an anomaly looks like.
  * There are too many features and a particular combination of values might be anomalous.

### Univariate Methods for Anomaly Detection

**Context restrictions:**
*(Example: Summary statistics of admission to triage in a paediatrics ED in minutes, showing a minimum of -84 and a maximum of 1750, indicating potential data entry errors or anomalies).*

#### Tukey's Method
* **Mild outlier:**
  * lower inner fence: Q1 - 1.5 * IQR
  * upper inner fence: Q3 + 1.5 * IQR
* **Extreme outlier:**
  * lower outer fence: Q1 - 3 * IQR
  * upper outer fence: Q3 + 3 * IQR

#### Z-score Outlier Detection
* Z-score tells how many standard deviations away a data point is from the mean.
* Any z-score greater than 3 or less than -3 is considered to be an outlier.
* Formula: z = (x - mean) / standard deviation.

#### Median Absolute Deviation (MAD)
* The median absolute deviation (MAD) is a robust measure of how spread out a set of data is (distance to the median).
* MAD = median( |Xi - median(Xi)| )
* Formula for detection: (Xi - median(Xi)) / median( |Xi - median(Xi)| ) > threshold.

#### Time Series (Example of model based)
* Model the time series:
  * Decompose the data.
  * Analyse the remainder to find anomalies.

### Multivariate Methods

#### Mahalanobis Distance
* Euclidian distance adjusted for covariance.

#### Cook’s Distance
* Summarises how much all the values in the regression model change when each point is removed at a time.
* Not exactly an outlier detection method, for it only measures the regression leverage.
  * If the outlier does not affect the regression it goes undetected.

#### Local Outlier Factor (LOF)
* Distance based algorithm (neighbour distance based method).
* Unsupervised ML algorithm.
* Only works with continuous features.
* Calculates an unidimensional anomaly score (LOF) for multidimensional observations.

#### Isolation Forests
* Based on random forest:
  * instead of trying to classify,
  * we are trying to isolate observations.
* Unsupervised ML algorithm.
* The original method only uses "continuous-valued attributes".

### Dive Deeper into Isolation Forest

#### Decision Trees
* Types of Classification and Regression Trees (CART):
  * Regression Tree (continuous outcome)
  * Classification trees (categorical outcome)
* Recursively binary splitting by feature.
* **Pros:**
  * Interpretability.
  * Less data cleaning required.
* **Cons:**
  * High variance (prone to overfitting).
  * Less effective in predicting the outcome of a continuous variable.

#### Random Forest
* Creates several Decision Trees.
* Random bootstrapping on observations.
* Random selection of features.
* Decision is made by polling the results of the ensemble.
* **Pros:**
  * Can parallelize.
  * The randomness reduces overfitting.
* **Cons:**
  * Memory intensive.
  * Less interpretable than a single decision tree.

#### Method (Isolation Forest)
* **In each isolation tree:**
  * In node, randomly select an attribute.
  * Randomly select a splitting point.
  * Repeat the process and split until all data is isolated or we can only find duplicates in leafs.
  * Count the number of splits until the point is isolated.
* **Isolation forest:** Repeat the process, creating *n* trees.

#### Anomaly Score
* How to calculate the anomaly score:
  * Pass observation through all the trees in the forest.
  * "Average out" the results.
  * Some will have a shortest path to be isolated (anomalies), others will take a longer path (normal).

#### Interpretation
* Results interpretation:
  * A score close to 1 -> indicates anomalies.
  * Score much smaller than 0.5 -> quite safely indicates a normal observation.
  * All scores are close to 0.5 -> the entire sample does not seem to have clearly distinct anomalies.

#### Pros and Cons of Isolation Forest
* **Pros:**
  * Simple.
  * Can parallelize.
  * Computationally cheap (when compared to distance-based algorithms).
  * Handles large data size and high-dimensional data.
* **Cons:**
  * Original method does not work with categorical data.

*(R Package for Isolation Forest: `isotree` - https://cran.r-project.org/web/packages/isotree)*

### The End
"Without data, you're just another person with an opinion." — William Edwards Deming

## Notes

É bom usarmos a detecção de outliers depois de aplicar o log quando as distribuições são assimétricas.
Podemos pegar nos outliers e imputar no percentil 95

# 9/06/2026 - HealthCare Use Cases

## 12_LEARN-examples-2026

### Data Science
* **Definition:** Study on the creation, validation, and transformation of data to generate meaning. A data scientist is a professional who uses scientific methods to deliberately generate meaning from raw data. It is a concept to unify statistics, data analysis, informatics, and their related methods in order to understand and analyze actual phenomena with data.

**Health Data Science - Opportunities:**
* Disease prevention
* Precision Medicine
* Value-based healthcare
* Optimizing workflows
* Infection control
* Patient Support

**Health Data Science - Challenges:**
* Data Quality & Quantity
* Multimodal Data
* Data Access
* Infrastructure
* Liability

### Message Prediction
* **Problem to Solve:**
  1. Sometimes Health Information Systems (HIS) get stuck and stop sending messages, requiring human intervention.
  2. Sometimes HIS would reprocess messages and overload third-party systems.
* **Architecture:** The workflow involves Data Collection, Interoperability (HL7v2 based DS), Model Creation, Feature Creation, REST API, and a CI/CD pipeline (using tools like Docker, Python, scikit-learn, R, and Plumber).

### Process Mining
Process mining is about applying algorithms to event logs to create information about how the processes are really carried out inside an institution.
There are 3 main classes:
1. Process Discovery
2. Conformance Checking
3. Process Enhancement

### Synthetic Data
* **Definition:** Synthetic data is comprised of data that isn’t based on any real-world phenomena or events; rather, it’s generated via a computer program. It is generated from real data and maintains the same statistical properties, meaning an analyst should get similar results as they would with real data.
* **Trade-off:** There is a constant balance between **Data Utility** and **Privacy Protection**.
* **Use Cases:** Software testing, Education, Data collection (timeframe & availability), Class imbalance, Clinical and scientific trials, Academic usage, and Privacy Protection.
* **Methods:** GAN, VAE, Bayesian networks, Copula, Dirichlet processes, SMOTE, etc.

### Distributed Learning
Methods to train models without centralizing all data:
* **Local learning:** Disconnected models.
* **Central learning:** Data and parameters are centralized in the cloud.
* **Federated learning:** Data stays at the edge, while parameters are centralized. The learning task is solved by a loose federation of participating devices (clients) coordinated by a central server. (Can be Horizontal or Vertical Federated Learning).
* **Swarm Learning:** Both data and parameters remain at the edge in a decentralized network.

### Benchmarking with Privacy Constraints
How to benchmark health outcome measures with privacy constraints?
* **Method:** Using clustering algorithms across different data silos. Silos calculate their own centroids and share them with other silos. They iteratively add true centroids, calculate new centroids, and evaluate the score until convergence, all without sharing the raw patient data.

### Birth Type Prediction
* **Goals:** Reduce surgeries, Improve Outcomes, Reduce surgery block time, Improve incentives.
* **The Reality of Data Science:** What do data scientists spend the most time doing? **60% is spent cleaning and organizing data** (only 4% refining algorithms and 3% building training sets).
* **"We have a model, now what?":**
  * *Inference Machine:* Feature creation, data prep, data cleaning, and data formatting.
  * *Data Quality:* How to address it in inference and in training?
  * *Drifting & Logging:* Implementation, storage, and choosing variables.
  * *Validation & DevOps:* Clinical validation, online/offline validation, CI/CD, and dataset versioning.

### Real-World Data (RWD) / Real-World Evidence (RWE)
Evaluating real-world impact by comparing outcomes (e.g., survival analysis for Overall Survival (OS) and Progression-Free Survival (PFS) between different drugs like Palbociclib vs. Ribociclib).
* **Questions to Ask:** Is this difference significative? What variables from the cohort are more impactful? How is this different from traditional chemotherapy? What can we do about it?

### Data Quality Evaluation Tool in Obstetrics
* **Context:** Real-world data from 9 hospitals, ranging from 2019 to 2020, with 2364 to 18177 records.
* **Goal:** Create an automatic data evaluation tool to help clinicians.
* **Steps:** 1. Prepare data -> 2. Develop Tool -> 3. Deploy -> 4. Evaluate.
* **Quality Categories evaluated:**
  * *Completeness* (Missing data percentages)
  * *Plausibility* (Atemporal and Uniqueness plausibility using Bayesian models, Z-scores, Local Outlier Factor, Duplicate Checks)
  * *Conformance* (Value conformance via Manual Rule Engine)
* **API Structure:** The HIS sends rows to evaluate to the DQ API, which applies scoring functions with weights (defined by target evaluator, purpose, setting, etc.) and returns the scores/alerts.

### Bayesian Networks: UFNBayes (Etiology)
* **Goal:** Causality assessment of adverse drug reaction (ADR) reports using an expert-defined Bayesian network.
* **Bibliography Support to ADR Report:** When there is a suspicion of an ADR, we need to ask: *Is this related in the literature?*
* **Requirements:** Coded Drug, Coded Reaction, Data retrieval, Token identification. (e.g., identifying terms like "Ropivacaine" and "Generalized urticaria" from literature abstracts to map cross-reactivity and allergic reactions).

## Notes

GAN, VAE etc são tipos de técnicas de gerar dados.


# 16/06/2026 - Timeseries

## Time Series Datamining
**Francisco Bischoff, MD, MSc**
HEADS - 2026 | MEDCIDS - Departamento de Medicina da Comunidade, Informação e Decisão em Saúde

### What is a Time Series?
A time series is a sequence of data points indexed in time order. Its complexity and behavior can change significantly depending on the length of the series ($n=10$, $n=100$, $n=1,000$).

### We Need a Framework!
*   **Foundations:** Visualizations, Basic statistics.
*   **Advanced:** Clustering, Anomaly detection, ARIMA, SAX, DTW.
*   **Strategic:** Forecasting, More data!

### Comparing Subsequences and Euclidean Distance
To analyze time series, we often extract subsequences (e.g., length $m=2, 3, 5$).
To compare subsequences, we use the **Euclidean distance**, which is the straight-line distance between two points. By calculating the pairwise Euclidean distance between all subsequences, we create a Distance Matrix and a Distance Profile.

### Matrix Profile
**Definition:** A vector that stores the z-normalized Euclidean distance between any subsequence within a time series and its nearest neighbor.

**Computational Complexity:**
*   **Brute Force (Naive):** Time Complexity $O(n^2m)$, Space Complexity $O(n)$.
*   **STAMP (FFT):** Time Complexity $O(n^2)$, Space Complexity $O(n)$.
*   **STOMP (Algebra):** Time Complexity $O(n^2)$, Space Complexity $O(n)$.

**Fundamental Assumption:** Conservation is Key. If a pattern is conserved, there must be some mechanism that conserves it (true in linguistics, music, genetics, literature, etc.).

**Key Claim:** Given the Matrix Profile (MP), most time series data mining problems are trivial or easy! The MP profile has many highly desirable properties, and any algorithm built on top of it will inherit those properties.

#### Desirable Properties of Matrix Profile
*   **Exact Solutions:** Provides no false positives or false dismissals for motif discovery, discord discovery, and time series joins.
*   **Simple & Parameter-Free:** Eliminates the need for building and tuning complex spatial access methods or hash functions.
*   **Space Efficient:** Requires inconsequential linear space overhead, allowing massive datasets to be processed in main memory.
*   **Anytime Performance:** Enables ultra-fast approximate solutions and real-time interaction for extremely large datasets.
*   **Incrementally Maintainable:** Can be updated very efficiently, making it ideal for streaming data.
*   **Leverage Hardware:** Embarrassingly parallelizable on multicore processors, GPUs, and distributed systems.
*   **Free of Curse of Dimensionality:** Time complexity is constant in subsequence length.
*   **Deterministic Time:** Predictable computation time based only on series length.
*   **Handles Missing Data:** Guaranteed to provide answers with no false negatives, even when data is incomplete.
*   **Simplicity and Intuitiveness:** Seeing the world through the MP lens often invites simple and elegant solutions.

#### How to "Read" a Matrix Profile
We use a companion sequence called a **Matrix Profile Index** (MPI), which contains integers used as pointers to find the nearest neighbor to any subsequence in constant time.
*   **Low values (Motifs):** The subsequence in the original time series must have at least one relatively similar subsequence elsewhere in the data. These are conserved shapes or reoccurring patterns.
*   **High values (Discords):** The subsequence in the original time series must be unique in its shape. These are anomalies or Time Series Discords.

### Matrix Profile Applications & Examples
*   **NYC Taxi Passengers:**
    *   *Anomalies (Discords):* Thanksgiving, Daylight Saving Time (apparent doubling of load), Columbus Day. 
    *   *Motifs:* Identifies strong 7-day periodicities.
*   **Italy Power Demand:** Matrix profile is very low on average (strong persistence and history). High values (discords) are explained by Italian holidays falling on different weekdays.
*   **Electrocardiograms (ECG):** Easily identifies premature ventricular contractions and ectopic beats as top discords.
*   **Zebra Finch Vocalizations:** Motifs reveal well-conserved repeated phrases, showing evidence of a vocabulary and grammar.
*   **Seismology:** Low values in a seismograph MP mean repeated earthquakes (foreshocks, aftershocks, triggered swarms).
*   **DNA Strings:** Can be converted to real-valued time series. Identifies lengthy, highly similar repeat units (amplicons) in chromosomes.
*   **Music:** Motifs usually point to the chorus, while discords point to bridges or instrumental solos.

### The Top-K Motifs
A sensible way to extract the top-K motifs uses a parameter $R$ (e.g., $R=2$).
1. Find the nearest pair of points (the Top-1 motif pair, distance $D_1$).
2. Draw a circle ($D_1 \times R$) around both points. Any points within are added to the motif.
3. Find the next nearest pair (excluding the first motif) to find the Top-2 motif ($D_2$), and so on.
*Note: $D_1 < D_2 < D_3$. You can stop (define K) using visual inspection or Minimum Description Length (MDL).*

### From Motifs to Time Series Chains
If we label subsequences by arrival time, we might see them drifting or evolving over time (e.g., a "pattern chain").
*   *Example (Arterial Blood Pressure):* As the chain progresses, the depth of the dicrotic notch decreases during a tilt table test.
*   *Example (Retail Search Queries):* Shows the smooth holiday bump transitioning into a sharply focused bump (the rise of "Cyber Monday" over a decade).

### Generalizing to Joins
The MP can be used as a similarity self-join ($T_A \bowtie_{1nn} T_A$). This generalizes to an AB-similarity join ($T_A \bowtie_{1nn} T_B$), finding the nearest neighbor in $B$ for every subsequence in $A$.
*   **The Golden Batch (Join Discord):** Two series *should* be the same. The difference highlights a unique event (e.g., a specific phrase present in the UK edition of Harry Potter but altered in the US edition).
*   **The Suspicious Similarity (Join Motif):** Two series have *no reason* to be the same, but the join motif shows conserved structures between them (e.g., comparing genomes of two different *Legionella* strains).

### Time Series Semantic Segmentation (FLOSS)
How do we detect when a system changes regimes (e.g., from walking to running, or physiological changes)?
*   **Key Observation:** In the Matrix Profile Index, most "walk" subsequences point to other "walk" subsequences. Rarely will an arrow (arc) cross the boundary between "walk" and "run".
*   **Arc-Curve:** By sliding across the index and counting the crossing arcs, a near-zero count signals a system change.
*   **Corrected Arc-Curve (CAC):** Corrects the natural drop in arcs at the beginning and end of the series using a theoretical inverted parabola.

**FLOSS Advantages:**
*   Fast and incrementally computable online.
*   Domain agnostic (works on ECGs, bird calls, insect behavior, factory machines).
*   Parameter-lite (only needs subsequence length $m$, and is highly robust to variations in $m$).
*   Extremely robust to data distortions (downsampling, reduced bit depth, linear trends, missing data, and heavy noise).

## Notes

As séries temporais podem se aplicar para outros tipos de dados como genéticos.

Falamos do estado da arte para séries temporais.

Distance Profile - vector que tem todas as distâncias euclideanas.
Distance Matrix - Matrix com todas as distâncias.
Matrix Profile - Vector que guarda as menores distâncias euclideanas.

O datamining é feito em cima da matrix profile.

Motifs são padrões que se repetem.
Discords são locais únicos que não se respondem.

Há FLUSS e FLOSS. O FLOSS é online.

A exclusion zone geralmente é metade da janela temporal e é para não encontrar pontos parecidos consigo mesmo.