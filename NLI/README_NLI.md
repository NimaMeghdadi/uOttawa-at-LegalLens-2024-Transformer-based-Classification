# How to run the code

## Overview

This repository contains code for training and testing Natural language inference (NLI) task using [ynie/roberta-large-snli_mnli_fever_anli_R1_R2_R3-nli](https://huggingface.co/ynie/roberta-large-snli_mnli_fever_anli_R1_R2_R3-nli) model on Hugging Face. The dataset has been used from [darrow-ai/LegalLensNLI](https://huggingface.co/datasets/darrow-ai/LegalLensNLI).

## Setup

Open the NLI_code.ipynb notebook in [Google Colab](https://colab.research.google.com).

## Train

### Steps to Train the Model

1. Execute the cells in the NLI_code.ipynb notebook sequentially to train the model.

## Test

### Before Running the Test

Set the following variables in the NLI_test.ipynb notebook:

- **excel_file_path**: Directory of the test set in .xlsx format.

### Steps to Test the Model

1. Ensure your test set contains three columns: id, premise and hypothesis.
2. Open the NLI_test.ipynb notebook in Google Colab.
3. Execute the cells sequentially to run the test.
run the NLI_test.ipynb

The code will generate a predictions_NLILens.csv file containing three columns: Premise, hypothesis, label.

## Notes

- Models are stored locally and should be accessible from the specified directories.
- Ensure the directory paths are correctly set to avoid errors during training and testing.

By following these steps, you can successfully train and test your NLI models using the provided notebooks.
