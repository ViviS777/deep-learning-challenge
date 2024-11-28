# deep-learning-challenge

# ### Neural Network Model Report

---

#### **1. Overview of the analysis: Explain the purpose of this analysis**

The goal of this analysis is to use deep learning models to help **Alphabet Soup** predict which applicant organizations are more likely to receive funding. By analyzing the provided data, we aim to build an accurate classification model to improve decision-making efficiency in funding allocation.

---

#### **2.**

- What variable(s) are the target(s) for your model*:  
  - The target variable for the model is **`IS_SUCCESSFUL`**, which indicates whether the applicant organization successfully received funding.

- **What variable(s) are the features for your model?**:  
  - The remaining columns (after removing irrelevant ones) are used as input features, including both numerical and categorical data. For categorical variables, we use **One-Hot Encoding** to convert them into numerical form.

- **What variable(s) should be removed from the input data because they are neither targets nor features**:  
  - **`EIN` and `NAME`** were removed. These columns have no practical significance for model classification as they only represent unique identifiers.

---

##### How many neurons, layers, and activation functions did you select for your neural network model, and why
- **Model Design**:  
  - Model 1: Two hidden layers, with 20 and 10 neurons respectively, and the activation function is **ReLU**.  
  - Model 2: Three hidden layers, with 100, 50, and 25 neurons respectively, and the activation function is **ReLU**.  
  - Model 3: Three hidden layers, with 128, 64, and 32 neurons respectively, and the activation function is **Tanh**.  
  - Model 4: Three hidden layers, with 100, 50, and 25 neurons respectively, the activation function is **ReLU**, and the batch size and number of epochs were adjusted (150 epochs).

- **Model Performance**:
  - The accuracy of the models is as follows:
    - Model 1 Accuracy: 0.72201
    - Model 2 Accuracy: 0.72915
    - Model 3 Accuracy: 0.72872
    - Model 4 Accuracy: 0.72813

- **What steps did you take in your attempts to increase model performance**:
  - Adjusted the number of hidden layers: Increased the complexity of the model to capture more feature information.  
  - Adjusted the number of neurons: Added more neurons in the hidden layers to increase the model's capacity.  
  - Tried different activation functions: Tested the model's performance using **ReLU** and **Tanh**.  
  - Increased the number of epochs: Model 4 increased the training epochs to 150 and adjusted the batch size to stabilize the training process.

---

#### **3. Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.**

- **Overall Results**:  
  The four models achieved around 72% prediction accuracy, which did not meet the target performance (>75%).

- **Recommendation**:  
  - Although deep neural networks performed well, other classification models could be attempted to improve performance. For example:  
    - **Support Vector Machines (SVM)**: Often perform better on smaller datasets.  
    - **Random Forest or Gradient Boosting Trees (e.g., XGBoost)**: Can automatically select important features, reduce the need for feature engineering, and improve model performance.


    