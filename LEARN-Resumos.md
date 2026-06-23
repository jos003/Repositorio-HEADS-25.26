
Data Mining cycle:
Business Understanding, Data Understanding, Data Preparation, Modeling, Evaluation, and Deployment

Inductive Bias - looks for a hypothesis, in the space of possible hypotheses

chosen representation represents a **representation bias**.
way the algorithm searches represents a **search bias**.

# Learning and Evaluating Classifiers: Validation and Generalization of Models

Error Metrics:
- Proportion of correctly classified cases (accuracy, sensitivity, specificity, precision, F1, ...)
- Distance between predicted and actual values (e.g. mean squared error)

Apparent error - Calculating the classification error on the same data used to train the model

Estimating Generalized Error:
1. Holdout - Pessimista
2. Random Sampling - does not allow to evaluate performance in all existing cases
3. K-folds Cross-validation
	1. The procedure is repeated K times, in order to use all the subsets as a test
	2. complete procedure several times (M)
	3. usual to stratify the groups
4. Leave-one-out Cross-validation
5. Bootstrap

# Learning Tree Models: Decision Trees and Random Forests

#### Appropriate Problems for Decision Tree Learning
- Instances are represented by attribute-value pairs.
- The target function has discrete output values.
- Disjunctive descriptions may be required.
- The training data may contain errors.
- The training data may contain missing attribute values.

ID3 Algorithm

Selecting the Best Attribute
- **Entropy** measures the impurity of a collection of examples for all _n_ classes.
- **Information gain** measures the expected reduction in entropy.

C4.5 - includes split information or intrinsic value term (sensitive to how broadly and uniformly the attribute splits the data)

C4.5 (and later C5.0) improved ID3 by:
- Handling heterogeneous attributes.
- Handling missing values.
- Handling costs.
- Pruning trees after creation.
- Boosting.

CART (Classification and Regression Trees)
- É igual aos outros mas usas Gini impurity (measure of how often a randomly chosen element from the set would be incorrectly labelled if it was randomly labelled according to the distribution of labels in the subset)

Random Forests
- Bagging approach + random selection of features
- Final classification of the random forest is usually done by majority vote of the ensemble.

# Ensemble Machine Learning: Bagging, Boosting and Stacking

Bagging
- (bootstrapped sample of same size as original sample -> Compute the bootstrapped estimator) X M (número de repitições)
- When to use - Unstable Models

Boosting
- **better predictive power** than bagging
- Learn model -> Compute the gradient vector (loss function attributed to each case) -> Repeat
- Overfitting Risk

Stacking
- combining heterogeneous models using another model
- Correct Training (Out-of-Fold)
	1. Split data into K folds
	2. For each fold k:
	    - Train each base model on the remaining K-1 folds
	    - Generate out-of-fold predictions for fold k
	3. Use all OOF predictions as features to train the meta-model
- Meta-model - Linear Meta-model (Good default choice; Lower overfitting risk)

|Method|Reduces|Type|Execution|Risks|
|---|---|---|---|---|
|Bagging|Variance|Homogeneous|Parallel|Low|
|Boosting|Bias (+var.)|Homogeneous|Sequential|Overfitting|
|Stacking|Both|Heterogeneous|Parallel + meta|Leakage|

Low correlation between models - Critical condition for Ensamble Success

Some ~ solutions for ensemble explainability:
• SHAP values: individual feature attribution per prediction
• Feature importance (global): which features contribute most
• Partial dependence plots: marginal effect of each feature

**AUC-ROC:** Overall discriminative ability; threshold-independent
**F1-Score:** Harmonic mean of precision and recall; useful for rare classes
**Calibration:** Predicted probability reflects actual event frequency
**Brier Score:** Mean squared error of probabilities; combines calibration and discrimination

When NOT to Use Ensembles
- Mandatory clinical explainability
- Very small datasets
- Prohibitive computational cost
- Simple model is already sufficient

# Learning Bayesian Networks: Probabilistic Graphical Models and Classifiers


Bayesian Probability - Probability that the hypothesis is true, updating the a priori probability about the hypothesis with the new incoming available data.

Bayesian Networks - -Describe the probability distribution governing a set of variables by specifying a set of conditional independence assumptions along with a set of conditional probabilities. Each variable is a node in the network, and its dependency defined by their ascendants in the network, quantified by a conditional probability table.

Learning Structure from Data
* **Search-and-score methods:** Search algorithm selects a subset of high-quality Bayesian Networks; a quality measure (score) decides which candidate is the best.
* **Constraint-based structure learning:** Identifies the structure that best encodes a set of conditional dependence and independence assumptions.

**Hill-Climbing Strategy (Defined from data):**
1. Start with no dependencies.
2. Compute the likelihood of observing the data given the model.
3. Test all possible single dependencies, computing the respective likelihood.
4. If the likelihood increases above a given threshold, insert that dependency.
5. Repeat until the threshold is not reached by any new dependency.

Naïve Bayes Classifier -  all the attributes are conditionally independent given the value of the outcome.

Tree-Augmented Naïve Bayes (TAN) Classifier - Relaxes the attribute independence assumption by employing a tree structure, in which each attribute only depends on the class and one other attribute. It uses a maximum weighted spanning tree that maximizes the likelihood of the training data.

Preprocessing for Naïve Bayes - Box-Cox transformations, scaling, and centering

# Support Vector Machines: Finding Optimal Separability

Linear Classification
- divide the input space into a collection of regions labelled according to the classification.
- Methods include:
	* Perceptron
	* Optimal Separating Hyperplane
* Any linear monotone transformation of the discriminant function will create linear decision boundaries.
* Methods that use *logit*:
	* Linear discriminant analysis (LDA)
	* Linear logistic regression


**Perceptron Learning Algorithm:** The perceptron learning algorithm tries to find a separating hyperplane by minimizing the distance of misclassified points to the decision boundary.

**Optimal Separating Hyperplanes:** The optimal separating hyperplane separates the two classes and maximizes the distance to the closest point from either class.

Support Vector Classifier
- The tuning parameter of this procedure is the **cost parameter C**.
* Points on the wrong side of the boundary are **support vectors**.
* Points on the correct side of the boundary but close to it (in the margin), are also **support vectors**.
* Larger values of C focus attention more on (correctly classified) points near the decision boundary, while smaller values involve data further away.
* Either way, misclassified points are given weight, no matter how far away.

**Kernel function** computes inner products in the transformed space.

**Three popular kernels:**
* *dth*-Degree polynomial
* Radial basis
* Neural network

# Artificial Neural Networks

The perceptron learning mechanism looks to choose the weight values so that the output value is correct for each given instance.

The algorithm in fact uses stochastic gradient descent to minimize error. That is, instead of computing the sum of the (error-based) gradient contributions of each observation followed by a step in the negative gradient direction, a step is taken after each observation is visited. Hence the misclassified observations are visited in some sequence, and the parameters are updated via a multiplicative learning rate.

Gradient Descent - At each iteration, the weight vector is updated in the direction of the negative gradient, until the minimum is reached. This is done by computing the first derivative according to each component of the weight vector.

Perceptron vs gradient descent
- Perceptron
	- updates only on mistakes
	- uses a non-smooth step function
- Gradient descent
	- uses continuous, differentiable loss
	- updates even when correct (small corrections)

Multi Layered Networks - Each neuron includes a non-linear activation function, although fully differentiable across the entire domain of the function, instead of the one used in the perceptron.

The network includes one or more layers of hidden neurons, highly connected, that are neither input nor output. These will allow the model to learning more complex tasks, expanding the search space and dimensions.

Activation Functions:
* Linear
* Logistic
* Hyperbolic Tangent

Backpropagation
- Changes to the gradient descent are needed.
- Perceptron → error is local and immediate
- Backprop → error is distributed through the network

Momentum - To avoid being stuck in local minima, we add a momentum term which tries to maintain the direction from previous update: Increasing the speed of adaptation in horizontal areas of the error surface, while preventing strict changes in direction.

Deep Learning - artificial neural networks with complex multilayers.

# Deep Learning: From Perceptron to LLMs

Perceptron: The perceptron is the foundation of neural networks. It consists of input nodes that feed into hidden layers, which are fully connected to output nodes.
* Each neuron applies an activation function to a weighted sum of its inputs plus a bias term.
* **Weights and Bias:** Arrows represent learnable weights. The perceptron computes a linear combination before activation.
* **Learning Rate:** Indicates the pace at which the weights get updated (can be fixed or adaptively changed).

#### Activation Functions
Used at the end of a hidden unit to introduce non-linear complexities to the model:
* **Sigmoid:**(0,1).
* **Tanh:** (-1,1). Zero-centred, better than sigmoid for hidden layers.
* **ReLU (Rectified Linear Unit):** Outputs 0 for negative inputs, identity for positive. Computationally cheap and avoids vanishing gradient; **dominant in modern networks**.
* **Leaky ReLU:** Like ReLU but allows a small **negative slope for negative inputs, preventing dead neurons**.

Training and Updating Weights
1. Obtain the prediction.
2. Calculate the loss using a loss function (e.g., cross-entropy) which measures the error between the prediction and the true label.
3. **Backpropagation:** Backpropagate the loss to get the gradients using the chain rule.
4. **Gradient Descent:** Use the gradients to update the weights.

Convolutional Neural Networks:
- excel in image
- **Architecture:**
	* **Convolutional Layers:** Apply learned filters to detect local features.
	* **Pooling Layers:** Downsample feature maps, reducing spatial size and parameters while retaining important features.
	  * Max pooling (maximum value)
	  * Average pooling(mean) 
	  * **Fully Connected Layers:** Flatten the pooled features into a vector and produce class scores.
	* **Stride:** Denotes the number of pixels by which the window moves after each convolution or pooling operation.

Recurrent Neural Networks
- label, classify, or generate sequences (e.g., time series analysis, natural language processing).
* Unlike feedforward networks, RNNs have loops in their connections, enabling information to carry over from one step to the next (memory of past inputs).
* **Advantages:** Can process input of any length, model size doesn't increase with input size, and weights are shared across time.
* **Drawbacks:** Computation is slow, and they suffer from the **vanishing/exploding gradient problem**, making it difficult to access information from a long time ago (short-term memory limitation).

Long Short-Term Memory
- Designed to solve the short-term memory limitations of standard RNNs.
* **Cell State:** Acts as long-term memory, like a conveyor belt running straight down the entire chain with minor linear interactions.
* **Hidden State:** Acts as short-term memory.
* **Gates:** Structures that optionally let information through, using a sigmoid neural net layer and pointwise multiplication.
  * *Forget Gate:* Decides what to erase from the cell state.
  * *Input Gate:* Decides what new information to write.
  * *Output Gate:* Controls what part of the cell state to expose as the hidden state.

Transformers
- Unlike RNNs, Transformers do not rely on sequential processing. They can operate in parallel over all tokens in a sequence.
* **Attention Mechanism:** "Attention Is All You Need". Attention layers tell the model to pay specific attention to certain words in a sentence and ignore others when dealing with the representation of each word.

**Architecture Components:**
* **Encoder:** Receives an input and builds a representation of it. Optimized for acquiring understanding (bi-directional attention).
* **Decoder:** Uses the encoder’s representation and previous outputs to generate a target sequence. Optimized for generating outputs (auto-regressive).

**Types of Models:**
* *Encoder-only:* Good for sentence classification, named entity recognition.
* *Decoder-only:* Good for generative tasks like text generation (modern LLMs).
* *Encoder-decoder (Sequence-to-sequence):* Good for translation or summarization (e.g., T5, BART).

Large Language Models (LLMs)
- Modern LLMs are usually Decoder-only architectures with billions of parameters.
* **Temperature:** Controls the randomness or creativity of the generated text. A low (deterministic); high (diverse outputs).
* **Hallucinations:** Factual inconsistencies or fabrications.

**Training Phases:**
1. **Pretraining:** Learning to predict the next token on vast amounts of text data.
2. **Instruction Tuning / Fine-Tuning:** The model is fine-tuned to follow instructions and generate helpful responses (often using Reinforcement Learning from Human Feedback - RLHF).

**Techniques for Improvement:**
* **Fine-Tuning:** Updating the model's weights to adapt its behavior, writing style, or vocabulary.
* **RAG (Retrieval Augmented Generation):** Connecting the LLM to a vector database to search for relevant external data before generating a response, helping with Q&A and factual accuracy.
* **Reasoning Models:** Using reinforcement learning to incentivize step-by-step reasoning capabilities (e.g., DeepSeek-R1 multi-stage training phases).

Prompt Engineering
* **Summarization:** Ask for specific formats (e.g., "Summarize the clinical case in 2-3 bullet points").
* **Data Extraction:** Ask for structured outputs (e.g., "Extract information into a JSON object").
* **Role-based:** Define a persona (e.g., "You are a professor of biomedical data science...").

Applications and Implications in Healthcare
* **Clinical Workflow:** Supporting clinical decision-making, evaluating imaging procedures, or writing patient letters (e.g., communicating diagnostic results).
* **Medical Education & Consultation:** Taking exams, providing cancer-related information, and addressing misconceptions.
* **Benefits:** Academic/scientific writing, benefits in scientific research, and healthcare practice improvements.
* **Risks & Concerns:** Ethical issues (bias, plagiarism, data privacy), risk of incorrect/inaccurate information, transparency issues, and copyright concerns.

# Inductive Modelling: Non-Supervised Learning

**Unsupervised Learning**
* Objective - learn the properties of the probability distribution P(X).

**Examples of Non-Supervised Learning:**
* **Principal Component Analysis (PCA):** Seeks to find **low-dimensional subspaces** with low probability that define the **boundaries** of regions with high probability.
* **Clustering analysis:** Aims to identify multiple convex regions with similar probability density.
* **Association rules:** Attempt to find succinct descriptions of regions with high density.

Association Rules
- look for regions of the space that have high probability relative to their size and support
- **Subset size:** The number of variables considered in the subset.
* **Support (or prevalence):** The proportion of cases in the dataset that satisfy the subset conditions.

APRIORI Algorithm Rule Generation:
If an itemset is split into two disjoint subsets, A and B (A⇒B), where A is the antecedent and B is the consequent:
* **Support:** Estimates the joint probability P(A and B).
* **Confidence:** The support of the rule divided by the support of the antecedent. Estimates conditional probability P(B|A).
* **Lift:** The confidence divided by the support of the consequent (P(B|A)/P(B)). Estimates the association measure. A lift > 1 suggests positive association, = 1 means independence, and < 1 indicates negative association.

APRIORI Algorithm **Challenges / Limitations:**
- Restrictive data format (binary).
* A support threshold is necessary for computational feasibility.
* Rules with high confidence or lift but low support will **never** be **discovered** under a high support threshold (e.g., **rare** adverse drug reactions).

Automatic Classification (Clustering)
- **Similarity/Distance Measures:**
	* Continuous variables: Euclidean or Mahalanobis distance.
	* Categorical variables: Hamming distance or Jaccard similarity.
	* Mixed-type data: Gower's distance.

**Object Dissimilarity:**
* **Normalization:** There is often a need to weight attributes to prevent clusters from being defined by a single dominant attribute (e.g., dividing by average observed distance).
* However, **normalizing is not always desirable**.
* **Missing Data:** Handling missing data is critical.

Clustering Algorithms types:
1. **Combinatorial (partition-based) methods:** Operate directly on the data, minimizing an error function. (NP-hard problem, usually solved via greedy gradient descent).
2. **Mixture models:** Assume data are generated i.i.d. from a probability distribution.
3. **Mode-seeking methods:** Identify modes (peaks) in the data distribution.

K-means
- An iterative gradient descent clustering algorithm designed for continuous variables using Euclidean distance.
1. Randomly choose *k* centroids.
2. Assign each remaining point to the cluster with the nearest centroid.
3. Recalculate centroids based on current members.
4. Repeat until no points change clusters.

Soft K-means (Expectation-Maximization / EM)
- Similar to estimating a probability density based on a mixture of Gaussians.
* **E-step:** Compute the responsibility (probability) of each cluster for each object.
* **M-step:** Re-estimate the parameters of each component based on current responsibilities.
#### K-medoids
Addresses K-means limitations (only quantitative variables, Euclidean distance dependency). Instead of computing a mean, it selects the existing object that minimizes intra-cluster distance (the medoid). Allows the use of **any distance measure**, but **increases** **computational complexity**.

### Which K? (Choosing the number of clusters)
This phenomenon is similar to overfitting in supervised learning!
* **Elbow Method:** Compute intra-cluster dissimilarity for each value of *k* and look for the "elbow" where increasing clusters brings diminishing returns.
* **Gap Statistic:** Compares the observed intra-cluster dispersion with the curve one would obtain if the data were uniformly distributed. The optimal number is the value that maximizes the gap between these two curves. Can correctly identify if optimal K=1.

### Hierarchical Clustering
* **Agglomerative (Bottom-Up):** Start with individual instances and merge the two clusters with the smallest inter-cluster distance step by step.
* **Divisive (Top-Down):** Start with all instances in a single cluster and recursively split the cluster with the largest intra-cluster distance.

**Distance between clusters (Linkage):**
* **Average Linkage:** Average distance between all pairs of objects, one from each cluster. Good compromise, producing well-separated and compact clusters.
* **Complete Linkage:** Maximum distance between any two objects (most distant pair). Tends to produce compact but small clusters.
* **Single Linkage:** Minimum distance between any two objects (closest pair). Tends to produce larger, less compact clusters.

# Learning from data streams

Algorithms that learn from data streams:
- must process examples at the rate they arrive
- use a **single scan** and fixed memory
- **maintain a decision** model at any time
- **adapt** to the most recent data
- might end-up with **approximate results**

Concept drift - the concept about which data is being collected may shift from time to time, each time after some minimum permanence.

Change detection mechanisms approaches:
- Monitoring the evolution of performance indicators adapting techniques used in Statistical Process Control.
- Monitoring distributions on two different time windows. The method monitors the evolution of a distance function between two distributions: data in a reference window and in a current window of the most recent data points.

Change Detection Research Problems:
- False alarms
- How to incorporate in learning algorithms
- Allow partial, fast and efficient updating in the decision model
- Recognize seasonal and re-occurring patterns is an open issue

**Sequential analysis** refers to the body of statistical theory and methods where the **sample size** may **depend in a random manner on the accumulating data**.

**Prequential (predictive sequential) method** 
- General methodology to evaluate learning algorithms in **streaming scenarios**.
- Error of a model is computed from the sequence of examples.
- For each example in the stream, the actual model makes a prediction based only on the example attribute-values.
- Prequential evaluation provides a learning curve that monitors the evolution of learning as a process.
- Is pessimistic
- Compute the prequential error using a forgetting mechanism

# Anomaly detection


**Definition:** Observation which deviates so much from other observations as to arouse suspicion it was generated by a different mechanism.

**The bottom line is:** Know what is expected and detect what deviates from it.

### Motivation for Unsupervised Anomaly Detection
* Why use unsupervised machine learning algorithms for anomaly detection?
  * Sometimes you don't know the data. i.e., you don't know how an anomaly looks like.
  * There are too many features and a particular combination of values might be anomalous.

Univariate Methods for Anomaly Detection:
- Tukey's Method (mild outlier (1.5 * IQR); Extreme outlier (3 * IQR)
- Z-score Outlier Detection (> 3 or < -3 ; z = (x - mean) / standard deviation)
- Median Absolute Deviation (MAD = median( |Xi - median(Xi)| ) ; Formula for detection: (Xi - median(Xi)) / median( |Xi - median(Xi)| ) > threshold.)
- Time Series (Model the time series->Decompose the data->Analyse the remainder to find anomalies)

Multivariate Methods for Anomaly Detection:
- Mahalanobis Distance (Euclidian distance adjusted for covariance.)
- Cook’s Distance (Summarises how much all the values in the regression model change when each point is removed at a time.)
- Local Outlier Factor
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

# Time Series Datamining

Time series is a sequence of data points indexed in time order

To analyze time series, we often extract subsequences using the **Euclidean distance**, which is the straight-line distance between two points. By calculating the pairwise Euclidean distance between all subsequences, we create a Distance Matrix and a Distance Profile.

Matrix Profile: A vector that stores the z-normalized Euclidean distance between any subsequence within a time series and its nearest neighbor.

Conservation is Key. If a pattern is conserved, there must be some mechanism that conserves it

Desirable Properties of Matrix Profile
*   **Exact Solutions**
*   **Simple & Parameter-Free:**
*   **Space Efficient:**
*   **Anytime Performance:**
*   **Incrementally Maintainable:**
*   **Leverage Hardware:** 
*   **Free of Curse of Dimensionality:**
*   **Deterministic Time:**
*   **Handles Missing Data:**
*   **Simplicity and Intuitiveness:**

How to "Read" a Matrix Profile:
- Low values (Motifs)
- High values (Discords)

Time Series Semantic Segmentation (FLOSS)

By sliding across the index and counting the crossing arcs, a near-zero count signals a system change.

FLOSS Advantages:
*   Fast and incrementally computable online.
*   Domain agnostic (works on ECGs, bird calls, insect behavior, factory machines).
*   Parameter-lite (only needs subsequence length $m$, and is highly robust to variations in $m$).
*   Extremely robust to data distortions (downsampling, reduced bit depth, linear trends, missing data, and heavy noise).