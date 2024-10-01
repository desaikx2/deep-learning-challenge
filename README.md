# deep-learning-challenge

**Overview**

This analysis aims to create and refine a deep learning model that predicts the success of charity organizations funded by Alphabet Soup. By examining historical data from previous charity projects, we seek to develop a neural network capable of accurately classifying the likelihood of success for upcoming initiatives. Ultimately, our goal is to enhance decision-making for funding allocation through reliable predictions.

### Results

#### Data Preprocessing

**Target Variable:**
The target variable for the model is **IS_SUCCESSFUL**, a binary indicator showing whether a charity project was successful (1) or not (0).

**Feature Variables:**
All columns except for **EIN**, **NAME**, and **IS_SUCCESSFUL** are used as feature variables. These include various attributes related to the charity projects and the organizations involved.

**Removed Variables:**
**EIN** and **NAME** were excluded from the dataset as they are identifiers that do not provide meaningful insights for predicting project success.

#### Model Development: Compilation, Training, and Evaluation

**Neurons, Layers, and Activation Functions:**

- **Neurons and Layers:**  
  The final neural network comprises three hidden layers with 128, 64, and 32 neurons, respectively. The initial model had fewer neurons and layers, but this was adjusted to better capture complex data patterns, resulting in improved performance.

- **Activation Functions:**  
  The hidden layers utilize the ReLU (Rectified Linear Unit) activation function to introduce non-linearity and handle intricate patterns, while the output layer employs the sigmoid activation function suitable for binary classification tasks.

**Model Performance:**

- **Target Performance:**  
  The goal was to achieve an accuracy of at least 75%. However, after multiple optimization efforts, the final model reached an accuracy of 72% on the test dataset.

**Strategies for Enhancing Performance:**

- **Increased Neurons and Layers:**  
  The model started with a simpler architecture but was enhanced by adding more neurons and layers, which allowed it to learn more detailed patterns from the data.

- **Adjusted Activation Functions:**  
  ReLU was chosen for its effectiveness in deep learning models, while the tanh function was also tested for its suitability with certain data types.

- **Increased Epochs:**  
  The number of training epochs was raised to 150, providing the model with additional learning opportunities, which contributed to the improved accuracy.


  ### Overall Results

The final deep learning model achieved an accuracy of 72%, falling short of the target performance of 75%. While it demonstrates some ability to predict the success of charity projects funded by Alphabet Soup, its current accuracy is insufficient to serve as a reliable basis for funding decisions. Therefore, it may not be the most effective tool for informed funding choices.

### Recommendations for Model Improvement

To enhance the model's performance and potentially reach or exceed the target accuracy of 75%, the following strategies are suggested:

**Increase Model Complexity:**

- **Add More Layers:** Incorporating additional hidden layers could enable the model to learn more complex patterns in the data.
- **Increase Neurons per Layer:** Adding more neurons to each layer may improve the model's capacity to capture intricate relationships within the dataset.

**Experiment with Activation Functions:**

- **Test Different Activation Functions:** Exploring alternatives like Leaky ReLU or ELU may yield better results than ReLU in certain contexts.

**Extend Training Epochs with Early Stopping:**

- **Train for More Epochs:** Increasing the training duration may enhance learning, but implement an early stopping callback to mitigate the risk of overfitting.

By adopting these strategies, the model's accuracy could improve, making it a more reliable tool for predicting the success of charity projects and supporting funding decisions for Alphabet Soup.
