# 2x2-Panel-Project


Overview

This project explores the problem of identifying and locating a target number within a 2x2 panel of randomly placed handwritten digits. Inspired by CAPTCHA systems, we use a machine learning model to recognize numbers even after random rotations and position changes. The dataset used is derived from the UCI ML handwritten digit dataset.

Problem Statement

Have you ever been asked to prove you're not a robot by selecting certain numbers from an image? This project attempts to automate such a task by developing a classifier that:

Detects whether a given number exists in a 2x2 panel.

Identifies which quadrant of the panel contains the target number.

Dataset

We initially considered using the MNIST dataset but opted for a smaller, more manageable version of the UCI ML handwritten dataset to reduce training time. The dataset consists of labeled images of individual digits, which were later combined into 2x2 panels.

Methodology

Data Preparation: The dataset was preprocessed by concatenating individual digit images into 2x2 panels.

Model Selection: We experimented with both Multi-Layer Perceptron (MLP) and Convolutional Neural Networks (CNN). CNNs provided better accuracy.

Training Steps:

The model first learned to identify individual numbers.

It was then trained on non-rotated 2x2 panels.

Finally, it was trained on rotated versions to simulate real-world CAPTCHA conditions.

Testing & Evaluation: The model's performance was evaluated across different degrees of rotation (0, 10, 20 degrees).

Results

Increasing the number of training images improved accuracy significantly.

Rotating the digits made classification harder but was mitigated with additional training.

The model struggled more with some digits (e.g., '5') due to their variability in handwriting styles.

Files in This Repository

2x2 Panel.ipynb: Jupyter Notebook containing the model training and evaluation code.

2x2 Panel.pdf: Detailed report explaining the project methodology and results.

How to Use

Clone the repository:

git clone https://github.com/yaminipravallika03/2x2-Panel-Project.git

Open 2x2 Panel.ipynb in Jupyter Notebook or Google Colab.

Run all cells to train and test the model.

Future Improvements

Extend the model to larger datasets like MNIST.

Improve accuracy for rotated digits by incorporating data augmentation techniques.

Experiment with attention mechanisms to enhance localization accuracy.
