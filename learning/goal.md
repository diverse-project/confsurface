# Goal

We aim to understand how accurate learning techniques are and how costly the learning process is. 

For each of the subject systems, we have compiled and measured the binary size and gadgets of some valid compile-time configurations. 
We use the random sampling facility of FeatureIDE over the feature model obtained as part of the engineering effort.

Then, we build prediction models on a *training sample*, a subset of configurations together with the measurements. 

The model can be used to predict non-functional properties of compile-time configurations without building and measuring them. 

For assessing the quality of the prediction model, we compare the predictions with values available in a *testing sample* denoted $C_te$. 

In machine learning, the sample of available observations is usually split with 70% in the training and 30% in the testing sample. 
In our case, we are also interested in investigating how accurate is the prediction model with regards to the size of training set. 
The number of configurations used for training gives an indicator on the cost (e.g. computational investments) of the method. 
We can also compare different statistical methods w.r.t. cost. 
