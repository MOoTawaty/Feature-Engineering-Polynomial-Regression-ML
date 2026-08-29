# Feature-Engineering-Polynomial-Regression-ML

Feature Engineering & Polynomial Regression ML Project
Project Overview

This project demonstrates how Feature Engineering and Polynomial Regression can be used to improve a machine learning model when the relationship between input features and the target value is non-linear.

A standard Linear Regression model works by finding weights and a bias that best fit the training data:

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

This approach works well when the data follows a roughly straight-line pattern. However, many real-world problems contain curved or more complex relationships. For example, housing prices may not increase linearly with the size of a house.

Feature Engineering

Feature Engineering is the process of creating new features from existing data to help a machine learning model learn important patterns.

Suppose the original feature is:

𝑥
=
Living Area

We can create additional features from it:

𝑥
,
𝑥
2
,
𝑥
3

For example:

𝑥
1
=
𝑥

𝑥
2
=
𝑥
2

𝑥
3
=
𝑥
3

These newly created features are called polynomial features.

Feature Engineering allows us to transform the original data into a form that is more useful for the machine learning model.

Polynomial Regression

After creating polynomial features, we can use them with Linear Regression.

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

Although the equation contains 
𝑥
2
 and 
𝑥
3
, it is still considered a linear model with respect to its parameters 
𝑤
0
,
𝑤
1
,
 and 
𝑤
2
.

A simple quadratic relationship can be written as:

𝑦
=
1
+
𝑥
2

By creating 
𝑥
2
 as a new feature, Linear Regression can learn a curved relationship instead of being limited to a straight line.

Selecting Useful Features

Sometimes it is not obvious which features will produce the best model. We can provide several possible features and allow the training process to determine their importance.

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

After training, the model might produce:

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

The weight associated with 
𝑥
2
 is larger than the weights associated with 
𝑥
 and 
𝑥
3
. This means that 
𝑥
2
 has a stronger contribution to the model's fitted predictions for this dataset.

A weight that becomes very small or approaches zero indicates that the corresponding feature has little contribution to the model.

Gradient Descent

The model uses Gradient Descent to learn the appropriate values of the weights and bias.

During training, Gradient Descent repeatedly adjusts:

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

to reduce the difference between the model's predictions and the actual target values.

As training progresses, the model learns which features are more useful for representing the relationship in the data.

Overall Process

The project follows this general workflow:

Original Features

↓

Feature Engineering

↓

𝑥
,
 
𝑥
2
,
 
𝑥
3
,
…

↓

Polynomial Regression

↓

Gradient Descent

↓

Learned Weights

↓

Predictions

Conclusion

The main idea of this project is that Linear Regression alone cannot always model non-linear data effectively. By using Feature Engineering, we can create new features such as 
𝑥
2
 and (x^
