### **Overview of the Analysis**

The purpose of this analysis is to evaluate the performance of a deep learning model designed to classify whether an application for charity funding is successful or not. The classification is based on various features of the application. The model's performance is assessed to determine how well it can predict successful applications and to identify potential improvements for achieving better accuracy.

### **Results**

#### Data Preprocessing

* Target Variable:  
  * “IS\_SUCCESSFUL” is the target variable. This indicates whether an application was successful (1) or not (0).  
* Feature Variables:  
  * All variables in the dataset, excluding the target variable, are considered features.  
* Variables to Remove:  
  * Non-beneficial ID columns such as EIN and NAME were removed as they do not contribute to the prediction of success and can lead to overfitting.

#### Compiling, Training, and Evaluating the Model

* Neurons, Layers, and Activation Functions:  
  * Layers and Neurons:  
    * First Hidden Layer: 285 neurons with ReLU activation  
    * Second Hidden Layer: 160 neurons with ReLU activation  
    * Third Hidden Layer: 97 neurons with ReLU activation  
    * Fourth Hidden Layer: 100 neurons with ReLU activation  
    * Output Layer: 1 neuron with Sigmoid activation  
  * Activation Functions:  
    * ReLU (Rectified Linear Unit) was used for hidden layers to introduce non-linearity and help the model learn complex patterns. Sigmoid activation was used in the output layer to generate probabilities for binary classification.  
* Model Performance:  
  * Loss: 0.5553  
  * Accuracy: 73.26%  
  * Target Performance:  
    * A target performance achieving higher than 70% accuracy is generally considered satisfactory. However, the model did not reach an accuracy of 75%.  
* Steps Taken to Increase Performance:  
  * Utilized early stopping with patience set to 5 to prevent overfitting and restore the best weights observed during training.  
  * Applied data scaling using StandardScaler to normalize features, which can help in improving model convergence and performance.

### **Summary**

After adjusting the input data in multiple different ways, I could not get an accuracy score higher than 75%. The model achieved an accuracy score of 73.26% and a loss of 0.5553 on the test dataset. The model, which was built with multiple hidden layers and ReLU activations, demonstrates a reasonable level of performance, though there is room for improvement.

#### One recommendation for improvement would be to use alternative models. Alternative models like Gradient Boosting Machines or Random Forests can sometimes be better than deep neural networks on data that is stored in rows/columns by capturing other types of relationships and interactions between features. By utilizing this recommendation and evaluating alternative approaches, it may be possible to achieve improved performance and better predict the success of the charity applications.

