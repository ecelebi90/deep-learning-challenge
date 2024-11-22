##Overview
  The non-profit organization, Alphabet Soup needs a tool thathat can help it select the applicants for funding with the best chance of success in their ventures.This tool should be able to predict whether the applicants will be successful if funded by Alphabet Soup.

##Results
  The target variable is y, which is represented by the IS_SUCCESSFUL column. This variable indicates whether the outcome is successful or not.
  The features for your model are represented by X this excludes IS_SUCCESSFUL for sure. For optimization model's, also STATUS, SPECIAL_CONSIDERATIONS_N, SPECIAL_CONSIDERATIONS_Y columns were excluded.Everything else included, ASK_AMT, INCOME_AMT, ORGANIZATION, USE_CASE,CLASSIFICATION,AFFILIATION, APPLICATION_TYPE 
  EIN and NAME should be removed since these data points has no impact on the model

  Layers:
  Total of 3 layers in your model:
  Input Layer: This is implicitly defined by the input dimension specified in the first hidden layer.
  First Hidden Layer: This contains 100 neurons.
  Second Hidden Layer: This contains 50 neurons.
  Output Layer: This contains 1 neuron for binary classification (using the sigmoid activation function).
  Neurons:
  100 neurons in the first hidden layer allow the model to capture complex patterns in the data.
  50 neurons in the second hidden layer provide additional capacity to learn from the outputs of the first layer, allowing for further abstraction and pattern recognition.
  Activation Functions:

  The ReLU (Rectified Linear Unit) activation function is used in the hidden layers. It is chosen because it helps to mitigate the vanishing gradient problem and allows the model to learn complex relationships in the data effectively.
  The sigmoid activation function is used in the output layer, which is appropriate for binary classification tasks, as it outputs a probability value between 0 and 1.
  This structure is designed to balance model complexity and performance, allowing the network to learn effectively while avoiding overfitting. 

  I was not able to achieve the results that was required.

  Steps that are taken to increase the model:
  1) Dropped more columns ("SPECIAL_CONSIDERATIONS_N", "SPECIAL_CONSIDERATIONS_Y", "STATUS") and added more hidden layers and more neurons, also incrased epoch to 200
  2) Dropped one column (STATUS) and added more hidden layers and more neurons, kept the epoch the same (100)
  3) Dropped one column (STATUS), kept the hidden layers the same, but dropping 20% of the neurons during training to reduce overfitting

##Summary
  The deep learning model, with its two hidden layers and a total of 151 neurons, was designed to capture complex patterns in the dataset.
  Loss: The model achieved a loss value of approximately 0.5640. Loss measures how well the predictions align with the true labels; lower values indicate better performance.
  Accuracy: The model attained an accuracy of 72.54% on the test dataset. This suggests the model correctly classified about 73% of the data, indicating moderate performance.
  In conclusion, while the deep learning model shows promise, it is advisable to compare its performance with simpler models to ensure the best approach for the specific classification problem at hand.
  For binary classification problems, we can consider simpler models like:
    Logistic Regression: May work better if the dataset is linearly separable.
    Random Forests: Handles non-linear relationships and can often provide high accuracy with less tuning. This model ensembles methods that can handle complex datasets and often require less tuning than deep learning models.
