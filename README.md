# Skimlit: Medical Abstract Classification

## Overview

Skimlit is a project for classifying medical abstracts into predefined categories using various machine learning models. This project utilizes different text processing techniques and model architectures to achieve the best performance in text classification tasks.

## Table of Contents

- [Requirements](#requirements)
- [Data](#data)
- [Data Preprocessing](#data-preprocessing)
- [Models](#models)
- [Evaluation](#evaluation)
- [Results](#results)
- [Usage](#usage)

## Requirements

Ensure you have the following packages installed:

- TensorFlow 2.8.0
- TensorFlow Hub 0.12.0
- scikit-learn
- numpy
- pandas
- matplotlib
- wget

You can install these packages using pip:

```bash
pip install tensorflow==2.8.0 tensorflow-hub==0.12.0 scikit-learn numpy pandas matplotlib wget
```

## Data

The dataset used in this project is the PubMed 20k RCT dataset, which is available [here](https://github.com/Franck-Dernoncourt/pubmed-rct). The data consists of medical abstracts with their corresponding categories.

To use the dataset:

1. Clone the repository:

   ```bash
   git clone https://github.com/Franck-Dernoncourt/pubmed-rct.git
   ```

2. The dataset files will be located in the `pubmed-rct/PubMed_20k_RCT_numbers_replaced_with_at_sign/` directory.

## Data Preprocessing

The preprocessing steps include:

1. **Loading Data**: Read text files containing medical abstracts.
2. **Cleaning and Parsing**: Extract relevant lines and structure them into dictionaries.
3. **Converting to DataFrames**: Transform preprocessed data into pandas DataFrames.
4. **Encoding**: One-hot encode target labels and convert text data into suitable formats for modeling.

## Models

Several models are implemented and evaluated. Below is a summary of the performance metrics for each model:

| **Model**  | **Accuracy** | **Precision** | **Recall** | **F1 Score** |
|------------|--------------|---------------|------------|--------------|
| Model 0    | 72.18%       | 0.719         | 0.722      | 0.699        |
| Model 1    | 78.75%       | 0.784         | 0.788      | 0.785        |
| Model 2    | 71.61%       | 0.716         | 0.716      | 0.713        |
| Model 3    | 68.29%       | 0.675         | 0.683      | 0.672        |
| Model 4    | 72.94%       | 0.731         | 0.729      | 0.726        |
| Model 5    | 82.19%       | 0.820         | 0.822      | 0.821        |

## Evaluation

Models are evaluated based on accuracy, precision, recall, and F1 score. The results of each model are compared to determine the most effective approach.

## Results

The results of the models are visualized using bar plots, showing the performance metrics for each model. Model 5 is identified as the best performer based on the evaluation metrics.

## Usage

To run the entire pipeline, including preprocessing and model training:

1. **Prepare the environment**: Ensure all requirements are installed.
2. **Clone the repository**: 

   ```bash
   git clone https://github.com/Franck-Dernoncourt/pubmed-rct.git
   ```

3. **Execute the notebook**: Open the provided notebook in a Jupyter notebook environment or Google Colab, and run all cells sequentially.

4. **Save and load models**: After training, models are saved for future use. You can load the models using TensorFlow's `load_model` method.
