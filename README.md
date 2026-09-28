# AI-ML Recruitment 2026

## Candidate Details

- **Name:** Saiprakash S
- **Program:** B.Tech Artificial Intelligence
- **Institution:** SRM Institute of Science and Technology
- **Year:** 2nd Year

---

## Task Completed

### Task 2 – Neural Network

**MNIST Handwritten Digit Classification**

This project implements a simple neural network to classify handwritten digits from 0 to 9 using the MNIST dataset.

---

## Problem Statement

The objective of this task is to build and train a simple neural network capable of classifying handwritten digit images from 0 to 9.

The project covers dataset understanding, preprocessing, neural network construction, model training, evaluation, and experimentation with the model architecture.

---

## Dataset

The project uses the MNIST Handwritten Digit Database.

MNIST consists of grayscale images of handwritten digits from 0 to 9.

- **Image size:** 28 × 28 pixels
- **Number of classes:** 10
- **Training images:** 60,000
- **Testing images:** 10,000
- **Pixel value range:** 0–255 before normalization

Each image is associated with a label representing the digit shown in the image.

---

## Approach

The project follows the following workflow:

1. Load the MNIST dataset using TensorFlow/Keras.
2. Inspect the dataset dimensions and labels.
3. Visualize sample handwritten digit images.
4. Normalize pixel values from the range 0–255 to 0–1.
5. Flatten each 28 × 28 image into a 784-element vector.
6. Build a simple neural network.
7. Train the model using the training dataset.
8. Monitor training and validation accuracy and loss.
9. Evaluate the model using the test dataset.
10. Generate a confusion matrix to analyse classification performance.
11. Modify the number of neurons in the hidden layer as an experiment.
12. Compare the original and modified models.

---

## Neural Network Architecture

### Original Model

The original neural network consists of:

```text
Input Image
28 × 28 pixels
      ↓
Flatten
      ↓
784 features
      ↓
Dense Layer
128 neurons
ReLU activation
      ↓
Dense Output Layer
10 neurons
Softmax activation
```

---

## Activation Functions

### ReLU

ReLU (Rectified Linear Unit) is used in the hidden layer.

It introduces non-linearity into the network and allows the model to learn more complex patterns from the input images.

### Softmax

Softmax is used in the output layer because the problem has 10 possible classes representing the digits 0 through 9.

It converts the output values into probabilities for the different classes.

---

## Data Preprocessing

The MNIST pixel values initially range from 0 to 255.

The values were normalized by dividing them by 255:

```python
x_train = x_train.astype("float32") / 255.0
x_test = x_test.astype("float32") / 255.0
```

This converts the pixel values to a range between 0 and 1.

The images were then flattened inside the neural network using the Flatten layer, converting each 28 × 28 image into a 784-element vector.

---

## Model Training

The model was trained using:

- **Optimizer:** Adam
- **Loss function:** Sparse Categorical Crossentropy
- **Metric:** Accuracy
- **Epochs:** 10
- **Batch size:** 32
- **Validation split:** 10%

Training and validation accuracy and loss were plotted to observe the model's performance during training.

---

## Evaluation

The model was evaluated using:

- Test Accuracy
- Test Loss
- Confusion Matrix

The confusion matrix helps identify which digits are correctly classified and which digits are incorrectly classified as other digits.

---

## Results

### Original Model

The original model used **128 neurons** in the hidden layer.

- **Test Accuracy:** 97.64%
- **Test Loss:** 0.0859

### Modified Model

The number of neurons in the hidden layer was increased from **128 to 256 neurons**.

- **Test Accuracy:** 97.80%
- **Test Loss:** 0.0877

### Experiment

The experiment was performed to observe how increasing the number of neurons affects the model's ability to learn and generalize.

The test accuracy increased slightly from **97.64% to 97.80%** after increasing the hidden layer from 128 to 256 neurons.

The test loss increased slightly from **0.0859 to 0.0877**. This shows that accuracy and loss can change differently because they measure different aspects of model performance.

The original and modified model results are compared in the Jupyter Notebook.

---

## Key Learnings

1. Learned how to load and understand the MNIST handwritten digit dataset.
2. Learned why image pixel values are normalized before training a neural network.
3. Understood how a Flatten layer converts image data into a form suitable for a dense neural network.
4. Learned the purpose of ReLU activation in hidden layers.
5. Learned why Softmax is suitable for multi-class classification.
6. Learned how to evaluate a classification model using accuracy and a confusion matrix.
7. Observed how changing the number of neurons in a hidden layer can affect model performance.

---

## Challenges

One of the challenges was understanding how the 28 × 28 image data is transformed before being passed to the dense neural network.

This was addressed by using a Flatten layer, which converts each 28 × 28 image into a 784-element vector.

Another challenge was understanding how to interpret the confusion matrix and compare the original model with the modified model.

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- VS Code
- GitHub

---

## Conclusion

A simple neural network was successfully developed to classify handwritten digits from the MNIST dataset.

The images were normalized and processed using a Flatten layer before being passed through a hidden Dense layer using ReLU activation and an output layer using Softmax activation.

The model was trained and evaluated using the MNIST test dataset. Training and validation curves were used to observe the learning behaviour, while the confusion matrix was used to analyse classification errors.

An additional experiment was performed by increasing the number of neurons in the hidden layer from 128 to 256 to study how a change in model capacity affects performance.

The original model achieved a test accuracy of **97.64%**, while the modified model achieved **97.80%**.

---

## Notebook

The complete implementation, training results, visualizations, confusion matrix, and experiment are available in:

`Task-2-MNIST/mnist_neural_network.ipynb`