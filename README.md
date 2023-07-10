# deep-learning-challenge
Created a binary classifier that can predict whether applicants will be successful if funded by the company.

## This repository contains code for a deep learning model to predict the success of charitable donations. The model uses a dataset of charitable organizations and their application information to train and make predictions.

### Libraries

    * scikit-learn
    * pandas
    * tensorflow
    

## The provided code implements a deep learning model to predict the success of charitable donations. Here is a summary of the code and an explanation of the results:

1. The code starts by importing the necessary libraries, including scikit-learn, pandas, and tensorflow.

2. It then loads the dataset from the provided URL using pandas.

3. The dataset is preprocessed by dropping non-beneficial ID columns ('EIN' and 'NAME') and performing binning for categorical variables ('APPLICATION_TYPE' and 'CLASSIFICATION').

4. Categorical data is converted to numeric using one-hot encoding.

5. The preprocessed data is split into training and testing datasets.

6. A StandardScaler instance is created to scale the data.

7. The deep learning model is defined using tf.keras.models.Sequential. It consists of two hidden layers with 9 and 18 nodes, respectively, and an output layer with a single node and sigmoid activation.

8. The model is compiled with binary cross-entropy loss and the Adam optimizer. It is then trained using the training dataset for 50 epochs.

9. The model's performance is evaluated on the testing dataset, and the loss and accuracy metrics are printed.

10. Finally, the trained model is saved to an HDF5 file named 'AlphabetSoupCharity.h5'.

The results of the model training and evaluation are as follows:

After training for 50 epochs, the model achieved an accuracy of approximately 73.4% on the testing dataset.
The loss value obtained on the testing dataset was approximately 0.553.
These results indicate that the model has learned patterns in the data and can predict the success of charitable donations with moderate accuracy. It's important to note that the actual performance may vary depending on the dataset and specific problem domain. Further experimentation and fine-tuning of the model may be necessary to improve its accuracy and generalization capabilities.
