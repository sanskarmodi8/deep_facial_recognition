# Deep Facial Recognition Project

## Overview

This project uses Tensorflow Functional API to implement deep facial recognition system using a Siamese neural network. Each step is mentioned in the siamese_network.ipynb notebook along with the code and explanations.
This projects follows this paper for building the model - https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf

![PositiveVerificationImg](https://github.com/sanskarmodi8/deep_facial_recognition/blob/main/pos_verified.png) ![NegativeVerificationImg](https://github.com/sanskarmodi8/deep_facial_recognition/blob/main/neg_verified.png)

## Table of Contents

- [Dependencies](#dependencies)
- [Data Collection](#data-collection)
- [Data Preprocessing](#data-preprocessing)
- [Training](#training)
- [Evaluation](#evaluation)
- [Real-time Verification](#real-time-verification)
- [Usage](#usage)
- [Contributing](#contributing)

## Dependencies

To run this project, you need to install the required dependencies. You can install them using the following command:

```bash
pip install -r requirements.txt
```

## Data Collection

The project collects negative images from the Labelled Faces in the Wild dataset and positive and anchor images from the webcam in real-time. The negative images are downloaded and processed, while the positive and anchor images are captured through user input during the data collection phase.

## Data Preprocessing

The collected images are loaded and preprocessed using TensorFlow. The data is then split into training and testing partitions. The training data is used to train a Siamese neural network with an embedding layer.

## Training

The Siamese network is trained using a custom loss function based on binary cross-entropy. The training loop iterates through multiple epochs, updating the weights of the network to minimize the loss.

## Evaluation

The model is evaluated on a testing partition, and precision and recall values are calculated for each batch.

## Real-time Verification

The trained model is used for real-time verification in a webcam feed. Positive images are copied to a verification folder, and the model compares the input image with these verification images. The verification process is triggered by user input ('v' key) in the webcam feed.

## Usage

1. Install dependencies: `pip install -r requirements.txt`
2. Run the notebook which performs following steps:
   
=> Collect and preprocess data

=> Build and Train the Siamese model

=> Evaluate the model on test data

=> Save the model

=> Real-time verification using OpenCV


## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, feel free to open an issue or create a pull request.
