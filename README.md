# Interpretable ML
<img src="https://github.com/MaartenGr/InterpretableML/blob/master/Images/lime.PNG" width="70%"/>

> Code and instructions for techniques to improve the explainability of machine learning models.

In this repo, you will find the code and instructions for [this article](https://towardsdatascience.com/opening-black-boxes-how-to-leverage-explainable-machine-learning-dd4ab439998e?source=friends_link&sk=55546f17a56c192f4d9f85ab6ccf4005). It is advised to read through the article whilst coding along using the **InterpretableML.ipynb** notebook. 

This repo and the corresponding article describe several methods for applying explainable ML:
* Partial Dependency Plots (PDP)
* Local Interpretable Model-agnostic Explanations (LIME)
* SHapley Additive exPlanations (SHAP)

## Methods
Some methods include: 

### PDP 
Partial Dependency Plots (DPD) show the effect a feature has on the outcome of a predictive based model. It marginalizes the model output over the distribution of features in order to extract the importance of the feature of interest. 

<img src="https://github.com/MaartenGr/InterpretableML/blob/master/Images/occupation.png" width="70%"/>

### LIME
LIME basically tries to step away from deriving the importance of global features and instead approximates the importance of features for local predictions. It does so by taking the row (or set of data points) from which to predict and generate fake data based on that row. It then calculates the similarity between the fake data and the real data and approximates the effect of the changes based on the similarity between the fake and real data.

<img src="https://github.com/MaartenGr/InterpretableML/blob/master/Images/lime.PNG" width="70%"/>

### SHAP
In its essence, SHAP uses game theory to track the marginal contributions of each variable. For each variable, it randomly samples other values from the data set and calculates the change in your model score. These changes are then averaged for each variable to create a summary score, but also gives information on how important certain variables are for a specific data point.

<img src="https://github.com/MaartenGr/InterpretableML/blob/master/Images/shap.PNG" width="70%"/>

### SHAP (Summary)
The Additivity axiom allows the Shapley values for each one-hot encoded generated feature to be summed as a representation of the Shapley value for the entire feature.

<img src="https://github.com/MaartenGr/InterpretableML/blob/master/Images/summary_shap.png" width="70%"/>
