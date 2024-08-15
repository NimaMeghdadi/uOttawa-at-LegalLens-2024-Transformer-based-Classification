# how to run the code

## Overview

This repository contains code for training and testing Named Entity Recognition (NER) models using [spaCy](https://spacy.io/) and Hugging Face's transformers and database used for fine tuning is [darrow-ai/LegalLensNER](https://huggingface.co/datasets/darrow-ai/LegalLensNER).

## setup

Open the NER_code.ipynb notebook in [Google Colab](https://colab.research.google.com).

## Train

1. Execute the cells sequentially up to the part involving HuggingFace's.

## Test

### Before Running the Test

Set the following variables in the NER_test.ipynb notebook:

- **excel_file_path**: Directory of the test set in .xlsx format.

### Steps to Test the Model

1. Ensure your test set contains two columns: id and tokens.
2. Open the NER_test.ipynb notebook in Google Colab.
3. Execute the cells sequentially to run the test.
run the NER_test.ipynb

The code will generate a predictions_NERLens.csv file containing three columns: id, tokens, and ner_tags.

## Notes

- Models are stored locally and should be accessible from the specified directories.
- Ensure the directory paths are correctly set to avoid errors during training and testing.

By following these steps, you can successfully train and test your NER models using the provided notebooks.
