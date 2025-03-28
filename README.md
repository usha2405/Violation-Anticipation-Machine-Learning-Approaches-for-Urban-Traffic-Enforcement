# Violation Anticipation: Machine Learning Approaches for Urban Traffic Enforcement

## Introduction

This project presents a machine learning-based approach to predict parking ticket violations in New York City. It aims to support law enforcement by anticipating potential violations, thereby improving the efficiency of traffic management and public safety.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Examples](#examples)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)

## Installation

Clone the GitHub repository:

```bash
git clone https://github.iu.edu/Luddy-B565-SP24/rkapgate-ushajain-psorte/tree/main/finalproject
```

Install required packages:

```bash
pip install -r requirements.txt
```

## Usage

The application includes a Tkinter-based interface where users can input features such as registration state, plate type, vehicle make, violation county, street name, and time of day to predict potential parking violations.

## Features

- Predicts parking ticket violations using historical NYC data
- Decision Tree and Artificial Neural Network (ANN) models
- Data pre-processing including feature thresholding and binning
- GUI using Tkinter for demonstration
- Accuracy:
  - Decision Tree: 98%
  - ANN: 97.73% on test data

## Dependencies

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow/Keras
- Matplotlib
- Tkinter

## Configuration

The models use 29 features, including:
- Registration State
- Plate Type
- Vehicle Body Type
- Vehicle Make
- Violation County
- Street Name
- Time of Day
- And others...

Feature selection and preprocessing reduce class imbalance and noise.

## Documentation

Refer to the project PDF `FinalProject_PredictingTicketViolations.pdf` for detailed methodology, model architecture, evaluation, and charts.

## Examples

Run the Tkinter app:

```bash
python app.py
```

Provide input features to get a prediction of likely violation codes.

## Results

### Decision Tree Model
- Accuracy: 98%
- Strengths: Easy to interpret, high performance on training data.
- Weaknesses: Risk of overfitting, particularly on underrepresented classes.

### Artificial Neural Network (ANN)
- Training Accuracy: 97.16%
- Validation Accuracy: 97.56%
- Test Accuracy: 97.73%
- Strengths: Better generalization, robust to class imbalance, captures nonlinear relationships.
- Performance: Confusion matrix and classification reports show more uniform predictions across all classes compared to decision tree.

## Challenges Faced

- **Class Imbalance**: The dataset originally had 100 violation classes, with many underrepresented. Filtering and feature thresholding were required to improve model generalization.
- **Noisy Data**: Approximately 5% of the data was identified as noise contributing to 40 uncommon classes, and was removed.
- **High Dimensionality**: 33 original features required careful selection and transformation (e.g., binning, encoding).
- **Overfitting**: Especially in the decision tree model, which required pruning (using `ccp_alpha=0.01`) to enhance generalization.
- **Sparse Features**: Some columns had high cardinality with low correlation, requiring informed decisions on retention or removal.

## Troubleshooting

- Ensure all dependencies are installed
- Check for missing input fields in the GUI
- Review logs for model loading errors

## Contributors
- Rajat Kapgate
- Usha Jain
- Pranav Sorte
