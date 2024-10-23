# Titanic-Survival-Prediction-Using-Bayesian-Networks-and-Exact-Inference
## Overview
This paper explores how Bayesian Networks could be used to predict the survival probability upon sinking of the Titanic. The exact inference machinery provides a basis for probabilistic predictions. This article investigates passenger survival chances in relation to passenger class, age, gender, and fare using a graphical model that brings into focus the relationships existing between variables.
The Titanic dataset records important information about passengers such as class (1st, 2nd, 3rd), gender, age, fare, and survival status. We can focus on such variables for constructing the Bayesian Network, which is a probabilistic model that captures the dependencies between them.
In our network, Survived is the variable of interest and thus denotes if a passenger survived while Pclass, Sex, Age, and Fare are its influencing factors. They are connected so we can predict survival based on their values.
## Data Preparation and Preprocessing
We preprocess the Titanic data set by discretizing continuous variables like Age and Fare into categories. This is important, as Bayesian Networks operate on discrete states. We deal with missing data by dropping or imputation to make the data set ready for analysis.
## Bayesian Network Structure and Inference
The structure of the network corresponds to how survival is conditioned on other factors. We estimate CPDs using the training data. Once we have specified the network, we will apply Variable Elimination for exact inference-the algorithm to compute the probability of survival given specific attributes of passengers. We do that by iteratively eliminating variables to compute posterior probabilities such that we can now predict the outcome conditioning on the evidence.
## Implementation of Exact Inference in Code
The code for the implementation at the top employs the pgmpy library to describe the structure of the network by specifying the inter-variable relationships. It then feeds in discretized data to estimate the CPDs using Maximum Likelihood Estimation, MLE. For exact inference, we create an inference object and then call the query() function by passing in the evidence, such as passenger class, gender, age, or fare. This method gives the survival probability distribution for the evidence provided, thus enabling us to predict the outcomes.
## Model Evaluation
We have assessed the performance of the model by comparing the actual results with the results obtained after making predictions through some metrics, such as accuracy, precision, recall, and F1-score. These assessments give an idea about how well the survival pattern is captured from the model.

## Conclusion
This present project demonstrates the power of Bayesian Networks in modeling complex relationships and making predictions. How different factors played their innings for survival/demise really tells a story, especially in the Titanic tragedy. The methods developed here may easily be adapted to other data sets, thereby revealing the versatility of probabilistic reasoning over a variety of fields.
