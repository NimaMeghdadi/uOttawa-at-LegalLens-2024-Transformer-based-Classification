# LEGALLENS-2024-DETECTING-LEGAL-VIOLATIONS

## About The Project
This project is my submission to LEGALLENS-2024-DETECTING-LEGAL-VIOLATIONS [competition](https://www.codabench.org/competitions/3052/) that is based on this [paper](https://aclanthology.org/2024.eacl-long.130/). 
This competition focus on two main tasks:
1. **NER**: Legal Named Entity Recognition (L-NER): Given possible online media text (review), determine or extract legal entities such as "violation," "violation by," "violation on," and "law."
2. **NLI**: Legal Natural Language Inference (L-NLI): Given a premise summarizing a class action complaint and a hypothesis from an online media text, determine if the relationship is entailed, contradicted, or neutral, indicating any association between the review and the complaint.

## How to run the code NER

### Overview

This repository contains code for training and testing Named Entity Recognition (NER) models using [spaCy](https://spacy.io/) and Hugging Face's transformers and database used for fine tuning is [darrow-ai/LegalLensNER](https://huggingface.co/datasets/darrow-ai/LegalLensNER).

## setup

Open the NER_code.ipynb notebook in Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NimaMeghdadi/LEGALLENS-2024-DETECTING-LEGAL-VIOLATIONS/blob/main/NER/NER_code.ipynb).

## Train

1. Execute the cells sequentially up to the part involving HuggingFace.

## Test
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NimaMeghdadi/LEGALLENS-2024-DETECTING-LEGAL-VIOLATIONS/blob/main/NER/NER_test.ipynb)
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

# How to run the code NLI

## Overview

This repository contains code for training and testing Natural language inference (NLI) task using [ynie/roberta-large-snli_mnli_fever_anli_R1_R2_R3-nli](https://huggingface.co/ynie/roberta-large-snli_mnli_fever_anli_R1_R2_R3-nli) model on Hugging Face. The dataset has been used from [darrow-ai/LegalLensNLI](https://huggingface.co/datasets/darrow-ai/LegalLensNLI).

## Setup

Open the NLI_code.ipynb notebook in [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NimaMeghdadi/LEGALLENS-2024-DETECTING-LEGAL-VIOLATIONS/blob/main/NLI/NLI_code.ipynb).

## Train

### Steps to Train the Model

1. Execute the cells in the NLI_code.ipynb notebook sequentially to train the model.

## Test
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NimaMeghdadi/LEGALLENS-2024-DETECTING-LEGAL-VIOLATIONS/blob/main/NLI/NLI_test.ipynb)
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
