# Audiobook Customer Conversion Prediction

This project focuses on predicting customer conversion behavior for an audiobook company using a deep neural network. The process involves several key steps:

## Data Preprocessing
- The data is balanced to ensure an equal distribution of the dataset, which is crucial for effective machine learning prediction.
- Three datasets are created: training, validation, and test datasets, which are then saved in npz format for ease of use.
- Standardization of the input features is performed to bring them to the same scale.
- Data is shuffled to introduce randomness, which aids the effectiveness of stochastic gradient descent (SGD).

## Data Balancing
1. The number of target labels (1s) is counted.
2. The goal is to keep as many 0s as 1s while deleting the excess.
3. Indices of data points to be removed are determined based on the condition of having more 0s than 1s.
4. The dataset is balanced by removing the excess data points.

## Standardization of Inputs
- Standardization ensures that all input features have a mean of 0 and a standard deviation of 1, making them suitable for machine learning algorithms.

## Data Shuffling
- Shuffling the data introduces randomness into the dataset, preventing homogeneity and aiding the effectiveness of stochastic gradient descent (SGD).

## Dataset Splitting
- The dataset is split into three parts: training, validation, and test sets, with proportions of 80%, 10%, and 10%, respectively.

## Model Creation
- A deep neural network (DNN) model is created using TensorFlow and Keras.
- The model consists of three hidden layers, each with 50 neurons, and an output layer with softmax activation for classification.

## Choosing Optimizer and Loss Function
- The model is compiled with the Adam optimizer and sparse categorical cross-entropy loss function, suitable for classification tasks.

## Training the Model
- The model is trained on the training dataset with a batch size of 200 and a maximum of 200 epochs.
- Early stopping is implemented with a patience of 2 to prevent overfitting.

## Testing the Model
- The model's performance is evaluated on the test dataset, and metrics like test loss and test accuracy are calculated. The model was able to predict 92% of the customer behavior which signifies a better fit. The model can help the organization channel their energy to customers possible to convert.

This project provides a foundation for predicting customer conversion behavior in the audiobook industry, which can be valuable for business decision-making and optimization.
