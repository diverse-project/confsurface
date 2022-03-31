# Learning methods

Fundamentally, we are addressing a regression problem: the goal is to predict a continuous variable out of predictive variables (features) corresponding to compile-time options.
Many statistical learning techniques can be used to address this problem.
We have chosen several techniques considered in the software product line literature. 
Our goal here is also to understand how difficult the learning is. 
For example, can a simple linear regression fit the distribution of binary size? 
Hence we make vary learning techniques from simple to more powerful. 
Another criterion is that we want to gather interpretable information out of learning models -- see RQ3 for more details.
Hence, neural networks and techniques like *DeepPerf* have not been considered. 

## Linear regression (OLS)

It predicts the target as a weighted sum of the features. 
The learned feature coefficients are easy to interpret and provide a strength of a compile-time option. 
We rely on the well-known ordinary least squares (OLS). 
OLS finds the weights that minimize the squared differences between the actual and the estimated outcomes.
The linearity of the learned relationship makes the interpretation easy. 

## Linear regression with interaction terms

One of the limitation of basic linear regression is that interactions among features are not captured. 
Prior works suggest that for many configurable systems and non-functional properties, it is necessary to consider interactions as part of the learning. 
Is it also the case for binary size and gadget? 
To investigate this hypothesis, we build linear models with polynomial combinations of the features (i.e. degree two and three). 
Hence we can investigate the effects of handling 2-wise (resp. 3-wise) interactions as part of the learning process (called polynomial regression hereafter) 

## Variants of linear regression. 

In addition to the inclusion of interaction terms, it is possible to use variants of OLS. 
We have considered Ridge, Lasso, Huber loss. 
Such techniques perform embedded feature selection and/or regularization in order to enhance the prediction accuracy. 
For instance, Lasso shrinks some coefficients throughout the training. 
We have considered such variants with and without interaction terms. 


## Decision trees (DT).

 It is the most used technique for regression problems. 
The tree structure is capable of dealing with interactions between options. 
Furthermore, it is possible to review the rules of tree for reaching a specific non-functional objective. 
We use CART-based implementations that have shown to reach competing accuracy. 


## Random forests (RF).

It is an ensemble learning method: the principle is to construct a multitude of decision trees at training time. 
As an ensemble method, the accuracy of random forests can be better than decision trees. 


