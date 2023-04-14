# X-Ray Covid - ML Classification

This project uses a convolutional neural network to classify chest X-ray images into one of three categories: covid, viral pneumonia, or normal. The dataset used is the [Kaggle COVID-19 Radiography database](https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database?resource=download).

## Project Overview

The Jupyter Notebook included in this repository contains the code and analysis for the project. It is organized into the following sections:

- Data Preparation
- Model Architecture
- Model Training
- Model Evaluation
- Conclusion

## Data Preparation

In the data preparation step, we read in the images from the directory that contains the data, convert them to grayscale if they are not already in grayscale, and store them in a numpy array called `data`. The corresponding labels for each image are stored in a numpy array called `labels`. We use the `LabelEncoder` class from scikit-learn to encode the labels as integers, and then normalize the pixel values in `data` to be between 0 and 1. We also split the data into training and testing sets using `train_test_split`.

## Model Architecture

The model architecture consists of three convolutional layers with increasing numbers of filters, each followed by a max pooling layer. The output of the last pooling layer is flattened and passed through two dense layers. The final layer has 3 units because there are three classes to classify. The choice of this architecture was based on previous research that has shown that CNNs are effective for image classification tasks.

## Model Training

The model was trained using the Adam optimizer and Sparse Categorical Crossentropy loss function. The accuracy metric was used to evaluate the performance of the model. The model was trained for 5 epochs, and the training and validation accuracy were recorded for each epoch.

## Model Evaluation

The trained model achieved an accuracy of approximately 95% on the test set. You can find more details in the Jupyter Notebook.

## Conclusion

In conclusion, this project demonstrates the use of a convolutional neural network for classifying chest X-ray images into three categories: covid, viral pneumonia, and normal. The Jupyter Notebook included in this repository provides a detailed overview of the data preparation, model architecture, model training, and model evaluation steps. Feel free to reach out to me on [GitHub](https://github.com/macfadem) if you have any questions or feedback!
