# Feature Engineering & Polynomial Regression ML Project

📌 Project Overview

This project demonstrates how Feature Engineering and Polynomial Regression can be used to improve a machine learning model when the relationship between the input features and the target value is non-linear.

A standard Linear Regression model has the form:

𝑓
𝑤
,
𝑏
(
𝑥
)
=
𝑤
0
𝑥
0
+
𝑤
1
𝑥
1
+
⋯
+
𝑤
𝑛
−
1
𝑥
𝑛
−
1
+
𝑏

Linear Regression works well when the relationship between the input and output is approximately linear. However, many real-world datasets contain curved or more complex patterns that cannot be modeled well using a simple straight line.

🔧 Feature Engineering

Feature Engineering is the process of creating new features from existing data to help a machine learning model learn useful patterns.

For example, if the original feature is:

𝑥
=
Living Area

We can create additional features:

𝑥
,
𝑥
2
,
𝑥
3

These new features are called polynomial features.

For example:

Original Feature
       ↓
       x
       ↓
Feature Engineering
       ↓
   x, x², x³


By transforming the original data, we give the model additional information that can help it represent non-linear relationships.

📈 Polynomial Regression

When polynomial features are added to Linear Regression, the model can represent curved relationships.

For example:

𝑓
(
𝑥
)
=
𝑤
0
𝑥
+
𝑤
1
𝑥
2
+
𝑤
2
𝑥
3
+
𝑏

A simple quadratic relationship can be represented as:

# 𝑦 
= 1 + $x^2$

The important idea is that although the model contains $x^2$ and $x^3$, it is still using the Linear Regression machinery because the model is linear with respect to its parameters (weights).

🎯 Selecting Useful Features

Sometimes, we do not know which features will be most useful.

We can provide several possible features:

𝑥
,
𝑥
2
,
𝑥
3

and allow the model to learn their weights:

𝑓
(
𝑥
)
=
𝑤
0
𝑥
+
𝑤
1
𝑥
2
+
𝑤
2
𝑥
3
+
𝑏

For example, after training, the model might produce:

𝑓
(
𝑥
)
=
0.08
𝑥
+
0.54
𝑥
2
+
0.03
𝑥
3
+
0.0106

The learned weights are:

𝑤
0
=
0.08

𝑤
1
=
0.54

𝑤
2
=
0.03

In this example, the weight associated with $x^2$ is larger than the weights associated with $x$ and $x^3$.

This indicates that $x^2$ has a stronger contribution to fitting the training data.

A feature with a weight that becomes very small or approaches zero has a relatively small contribution to the model.

🧠 Gradient Descent

Gradient Descent is used to learn the values of the model's weights and bias.

During training, Gradient Descent adjusts:

𝑤
0
,
𝑤
1
,
𝑤
2
,
𝑏

to reduce the prediction error.

Through this process, the model learns which features are more useful for fitting the data.


🔄 Project Workflow


The overall process can be summarized as:

Original Data
     ↓
Feature Engineering
     ↓
Create Polynomial Features
     ↓
x, x², x³, ...
     ↓
Linear Regression
     ↓
Gradient Descent
     ↓
Learn Feature Weights
     ↓
Make Predictions

📝 Key Concepts

Concept	Description
Linear Regression	Predicts an output using a weighted combination of features.
Feature Engineering	Creates or transforms features to make them more useful for the model.
Polynomial Features	Creates features such as $x^2$, $x^3$, etc.
Polynomial Regression	Uses polynomial features with Linear Regression to model non-linear relationships.
Gradient Descent	Optimizes the model's weights and bias by reducing prediction error.
Feature Weights	Represent how strongly each feature contributes to the model.

🚀 Conclusion

This project shows how a Linear Regression model can be extended to handle non-linear data through Feature Engineering.

By creating polynomial features such as $x^2$ and $x^3$, the model can capture curved patterns that a basic linear model cannot represent.

The model then uses Gradient Descent to learn the appropriate weights for these features and determine how they contribute to the final predictions.

In simple terms:

Feature Engineering creates useful features → Polynomial Regression uses those features → Gradient Descent learns their weights → The model makes better predictions.
