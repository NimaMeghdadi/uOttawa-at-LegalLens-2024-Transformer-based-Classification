# uOttawa at LegalLens-2024: Transformer-based Classification

## Project Overview

This repository contains the code and models used for the **LegalLens-2024 shared task**, which focuses on detecting legal violations within unstructured textual data and associating these violations with potentially affected individuals. 

The project is divided into two subtasks:
- **Subtask A: Legal Named Entity Recognition (L-NER)** - Identifying legal violations using Named Entity Recognition (NER) techniques.
- **Subtask B: Legal Natural Language Inference (L-NLI)** - Linking legal violations to potentially affected individuals using Natural Language Inference (NLI).

This repository demonstrates the effectiveness of transformer models such as **BERT**, **RoBERTa**, and **DeBERTa** for legal tasks.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architectures](#model-architectures)
- [Usage](#usage)
- [Results](#results)
- [License](#license)

---

## Dataset

The datasets used for this project are provided by the **LegalLens-2024 shared task** organizers. They contain textual data representing legal violations and related entities. Each subtask uses different subsets of this data:

- **Subtask A: L-NER** dataset includes tokenized text and corresponding named entities (`violation`, `violation by`, `violation on`, `law`). [Explore the dataset](https://huggingface.co/datasets/darrow-ai/LegalLensNER).
- **Subtask B: L-NLI** dataset involves sentence pairs (premise and hypothesis) with labels (`Entailment`, `Neutral`, `Contradict`). [Explore the dataset](https://huggingface.co/datasets/darrow-ai/LegalLensNLI).

### Data Split
- **Training Set**: Provided by the organizers.
- **Validation Set**: 20% of the training data.
- **Test Set**: Separate from the validation set, used for final evaluation by the organizers.

---

## Model Architectures

### Subtask A: Legal Named Entity Recognition (L-NER)
- **Model**: Fine-tuned **DeBERTa-v3-base**.
- **Library**: Utilized **spaCy** for tokenization and NER task configuration.
- **Evaluation**: The model achieves an F1-score of **86.37%**.

### Subtask B: Legal Natural Language Inference (L-NLI)
- **Model**: Combined **RoBERTa** (ynie/roberta-large-snli_mnli_fever_anli_R1_R2_R3-nli) with a custom-built **CNN** for keyword detection.
- **Library**: Used the **Hugging Face Transformers** library for tokenization and model training.
- **Evaluation**: Achieved an F1-score of **72.4%** on the hidden test set, placing 5th in the competition.

---

## Usage

You can use the code directly in [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NimaMeghdadi/LEGALLENS-2024-DETECTING-LEGAL-VIOLATIONS/).

### Subtask A: Legal Named Entity Recognition (L-NER)

1. **Data Preprocessing**: Tokenize the text using spaCy's tokenizer and prepare the dataset for NER training.

2. **Model Training**: Fine-tune the DeBERTa model on the L-NER dataset and save the model.

3. **Model Testing**: Load the trained model and evaluate it on the test dataset.

### Subtask B: Legal Natural Language Inference (L-NLI)

1. **Data Preprocessing**: Prepare the NLI dataset by tokenizing premises and hypotheses.

2. **Model Training**: Train the combined RoBERTa-CNN model for NLI and save the model.

3. **Model Testing**: Load the trained model and evaluate it on the test dataset.

---

## Results

### Subtask A: Legal Named Entity Recognition (L-NER)
- Best F1-score: **86.37%**

### Subtask B: Legal Natural Language Inference (L-NLI)
- Best F1-score on validation: **88.6%**
- Final F1-score on hidden test set: **72.4%**

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


