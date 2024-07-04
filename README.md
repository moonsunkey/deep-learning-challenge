# Alphabet Soup Nonprofit Foundation Funding Predictor

The purpose of this analysis is to develop a tool to help the nonprofit foundation Alphabet Soup select the applicants for funding with the best chance of success in their ventures.

## Results

### Data Preprocessing

- **Target Variable(s) for the Model:**
  - `IS_SUCCESSFUL`: This variable indicates whether the application for funding was successful or not.

- **Feature Variable(s) for the Model:**
  - `NAME`
  - `APPLICATION_TYPE`
  - `AFFILIATION`
  - `CLASSIFICATION`
  - `USE_CASE`
  - `ORGANIZATION`
  - `STATUS`
  - `INCOME_AMT`
  - `SPECIAL_CONSIDERATIONS`
  - `ASK_AMT`

- **Variables to be Removed:**
  - `EIN`: This is an ID number and does not contribute to predicting the success of funding applications.

### Neural Network Model Design

- **Input Features:**
  - Number of input features: 74 

- **Neural Network Architecture:**
  - **Layer 1:**
    - Neurons: 80
    - Activation Function: ReLU
  - **Layer 2:**
    - Neurons: 30
    - Activation Function: ReLU
  - **Output Layer:**
    - Neurons: 1
    - Activation Function: Sigmoid (for binary classification)
    - **Reason:** The Sigmoid activation function is used in the output layer to produce a probability score between 0 and 1, indicating the likelihood of the application being successful.

- **Why these choices?**
  - **Neurons and Layers:**
    - **80 neurons in the first layer** were chosen to capture a broad range of interactions between features.
    - **30 neurons in the second layer** were selected to refine the model’s understanding further.
    - This architecture strikes a balance between complexity and computational efficiency, allowing the model to learn effectively without overfitting.
  - **Sigmoid Activation in Output Layer:**
    - Suitable for binary classification problems as it provides a probability that can be mapped to two classes (success or failure).

### Model Performance

- **Achieved Performance:**
  - The model was able to achieve an accuracy of 75%.
  - The model's loss function minimized to 0.5114.

  - ![Model Performance Screenshot](path/to/screenshot.png)
    
### Steps to Improve Model Performance

- **Increase Neurons:**
  - Enhanced the model by adding more neurons to the second layer.
![Model Accuracy Plot](path/to/accuracy_plot.png)
- **Add Layers:**
  - Improved the model architecture by introducing an additional layer.
![Model Accuracy Plot](path/to/accuracy_plot.png)
- **Feature Engineering:**
  - Reintroduced `NAME` as a feature to capture any potential hidden patterns.

### Summary

- **Overall Results:**
  - The deep learning model was able to classify funding applications with a reasonable degree of accuracy. However, there is room for improvement to enhance predictive performance.

- **Recommendations for Alternative Models:**
  - **Random Forest Classifier:**
    - This ensemble method can handle a large number of input features and is less prone to overfitting compared to deep neural networks.
    - Random forests also provide feature importance metrics, which can be valuable for understanding which features contribute the most to prediction accuracy.

  - **Gradient Boosting Machines (GBM):**
    - GBM can provide high predictive power and is effective in handling imbalanced datasets.
    - They iteratively correct errors from previous models, which can result in better performance on complex datasets.

By considering these alternative models, we might achieve better accuracy and more insights into the key factors driving the success of funding applications.

---

### Visual Representations


*Figure 1: Model Accuracy over Epochs*

![Model Loss Plot](path/to/loss_plot.png)
*Figure 2: Model Loss over Epochs*
