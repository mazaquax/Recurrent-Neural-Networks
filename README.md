# Recurrent Neural Networks
Some personal projects on Recurrent Neural Networks
# Avito_text_cat_classification.ipynb
The dataset consists of ~1 million sale announcements from Avito. The problem is to predict if the announcement contains a mobile number of a seller or not. </br>
Data features have 3 types: text, categorical, numerical. I consider two ways of solving the problem and compare them. One feature is called **Category**, to compare these two ways I will use Avarage ROC AUC metric among categories.
### 1. Ensemble method
Here I implement ensemble methods for independent feature subsets and than again use an ensemble to obtain final predictions. Ensemble consists of 4 models: KNN, Naive Bayes, Logistic Regression, XGBoost.
### 2. Recurrent Neural Network method
Here I implement a neural network model which includes Bidirectional Long Short-Term Memory layers for text features. </br></br>
The notebook contains very detailed review of the project. I provide a short summary below.
### Conclusion
As we can see, neural network with LSTM layers allowed us to **increase our metric by ~0.01**. Moreover, implementation of an ensemble model requires more time and precise parameters tuning when **implementation of NN model is quite fast and it does not take much time to tune the model**. </br> But there is **a con about implemented neural network**. **Learning requires too much time if one does not use TPU or CPU**. </br> That is why in different situations we will use different solutions.
