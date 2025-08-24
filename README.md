1.How does regularization prevent overfitting?
Regularization mitigates overfitting by introducing a cost when the algorithm becomes excessively sophisticated. This compels the model to maintain a more straightforward decision boundary and steer clear of capturing random fluctuations in the training dataset. A more streamlined model tends to perform better on novel data. For instance, in Logistic Regression or Support Vector Machines (SVM), a lower value of C implies tougher regularization, resulting in gentler boundaries and reduced overfitting

2.When to choose ensemble methods versus basic algorithms?
Basic algorithms (such as Logistic Regression, Support Vector Machines, K-Nearest Neighbors, or Perceptron) are advantageous when the data collection is modest in size, well-structured, and largely linearly distinguishable. These models are straightforward to configure, quicker to execute, and more transparent in terms of interpretation.
Ensemble techniques (like Random Forests or Gradient Boosting Machines) are preferable when the dataset is extensive, messy, or nonlinear in nature. They aggregate several models, typically yielding enhanced precision and minimizing prediction mistakes, though they tend to be less intuitive to understand.
General guideline: Begin with basic models, and transition to ensemble strategies if the data is intricate or if performance falls short.




MY OBSERVATIONS 
Exercise 1 began with data preprocessing. The Iris dataset was imported and normalized, and a nonlinear moons dataset was synthesized for future comparison. Normalization ensured that all attributes had equal influence, while the moons dataset emphasized why certain challenges require nonlinear classifiers.

Exercise 2 was involved training a Perceptron, one of the most fundamental linear models. On the Iris dataset, it performed adequately, but the learning rate (`eta0`) had a significant impact on outcomes. A low learning rate (0.01) led to slow adaptation, whereas a high rate (1 or 100) caused instability and misclassification. On the nonlinear moons dataset, the Perceptron failed entirely, demonstrating its inability to handle data that isn't linearly separable.

Exercise 3 introduced Logistic Regression. In this case, the `C` parameter regulated regularization. A large `C` value (e.g., 100) weakened the penalty, resulting in intricate decision boundaries that risked overfitting. A small `C` (e.g., 0.01) enforced simpler, smoother boundaries, which occasionally led to underfitting. This highlighted how regularization manages model complexity.

Exercise 4 focused on a linear Support Vector Machine (SVM). This method seeks to maximize the separation between categories. A small `C` (0.1) permitted a broader margin and accepted some classification errors, while a large `C` (100) demanded stricter classification, narrowing the margin and increasing the chance of overfitting.

Exercise 5 expanded SVM to nonlinear scenarios using the kernel method. With the Radial Basis Function (RBF) kernel, the `gamma` parameter controlled the adaptability of the boundary. A low `gamma` (0.01) produced very smooth boundaries, often resulting in underfitting. A high `gamma` (100) created highly flexible boundaries that captured noise and overfit. On nonlinear data like moons, Kernel SVM outperformed its linear counterpart, making it more suitable for curved decision regions.

Exercise 6 explored Decision Trees. These models divide data based on information gain. A tree with limited depth (depth=1) underfit due to its simplicity, while a deep tree (depth=10) overfit by tailoring too closely to the training data. This emphasized the need to regulate tree depth.

Exercise 7 introduced Random Forests, a collection of multiple decision trees. By aggregating several trees, accuracy increased and overfitting was mitigated. Raising the number of trees (e.g., 100) enhanced consistency. Feature importance metrics also indicated which variables were most influential in classification.

IN Exercise 8 involved training a K-Nearest Neighbors (KNN) algorithm. The `k` parameter specified how many nearby points were considered. With `k=1`, the model overfit, reacting too strongly to noise. With `k=10`, it underfit, producing overly generalized boundaries. Altering the distance measure (Euclidean vs. Manhattan) also affected how neighbors were evaluated.

Exercise 9 applied hyperparameter optimization using GridSearchCV to automatically identify optimal settings for models like Logistic Regression, SVM, and KNN. A comparison across all classifiers revealed that Logistic Regression and Linear SVM excelled on linearly structured data like Iris, while Kernel SVM and Random Forest performed better on nonlinear datasets such as moons.





