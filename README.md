# Deep_Learning_Model_with_CNN
Drive link of dataset:
https://drive.google.com/file/d/1SHxXCL3Khe0gCggPHqCkefqXMOGhabVL/view?usp=sharing

## Code Explanation

The provided code is an example of a CNN deep learning model for image classification using TensorFlow and Keras. Here is a breakdown of the code:

### Importing Libraries

The necessary libraries are imported at the beginning of the code, including TensorFlow, NumPy, Matplotlib, Seaborn, and various modules from TensorFlow and Keras.

### Data Preprocessing

The code uses the `ImageDataGenerator` class from Keras to perform data augmentation and generate batches of image data for training and validation. The training and validation data directories are specified, along with other parameters such as image size, color mode, batch size, and seed.

### Model Architecture

The code uses the MobileNetV2 architecture as the base model for transfer learning. The base model is loaded with pre-trained weights from the ImageNet dataset. Additional layers are added on top of the base model, including a global average pooling layer, batch normalization layer, dense layer, dropout layer, and a final dense layer with softmax activation for multi-class classification.

### Model Compilation

The model is compiled with the Adam optimizer, a learning rate of 0.0001, categorical cross-entropy loss, and accuracy as the evaluation metric.

### Learning Rate Scheduler

A learning rate scheduler is defined to adjust the learning rate during training. The learning rate is decreased exponentially after the first 5 epochs.

### Model Training

The model is trained using the `fit` method, with the training data, validation data, batch size, and the learning rate scheduler as arguments. The training history is stored in the `history` variable.

### Model Evaluation

The trained model is used to make predictions on the validation data. The predicted classes are compared to the true classes to generate a confusion matrix. The confusion matrix is then visualized using a heatmap.

### Model Performance Visualization

The code plots the training and validation loss and accuracy curves using Matplotlib. Two subplots are created, one for the loss curves and one for the accuracy curves.

### Model Saving

The trained model is saved as a `Classification_model.h5` file.
