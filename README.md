# Arabic Text Punctuation Restoration AI Model

## Team Members
* **Mohammad Abdulrazzaq Karkoutly**
* **Namat Bilal Asaad**
* **Ahmad Al-Hati**

## Project Overview
This project aims to build and evaluate deep learning models capable of understanding semantic context and automatically restoring punctuation marks to Arabic texts. The project includes building, training, and evaluating two core models:
1. **AraBERT Model:** Based on `aubmindlab/bert-base-arabertv02` for token classification tasks.
2. **Bi-LSTM Model:** Features a word embedding layer and a masking mechanism to ignore padded tokens.

## Code Notebooks
* `AraBERT_Punctuation_Evaluation.ipynb`: Dedicated notebook for loading AraBERT model weights, evaluating final performance, and displaying the confusion matrix.
* `BiLSTM_Data_Processing_and_Training.ipynb`: Includes text cleaning and extraction steps, class weight calculations to handle data imbalance, and Bi-LSTM model training.

## Datasets & Large Files
Due to the size of the datasets and trained model weights exceeding GitHub's upload limits, large files are hosted via the following direct links:
* **Complete Project Directory (Google Drive):** [Full Project Folder](https://drive.google.com/drive/folders/1GtHnuipzHX9RzFNCNXn9a2MhQeMtF1Nx) *(Contains all trained models, evaluation plots, and large files)*.
* **Model Weights (AraBERT):** [Download Model Weights](https://drive.usercontent.google.com/download?id=1hpfXnJ3aSklcMe6wai_YVGfK_Otb24f5&authuser=0).
* **Dataset:** Utilizes the `SSAC-UNPC` dataset, available for download [here](https://data.mendeley.com/public-files/datasets/2pkxckwgs3/files/4f402c76-388e-4bde-b887-f1be522001db/file_downloaded).

## Data Mining & Preprocessing Strategy
To address class imbalance—specifically the heavy dominance of tokens without punctuation (`NO_PUNCT`)—an under-sampling strategy was applied. Sentences containing rare punctuation marks (e.g., exclamation and question marks) were fully preserved to maintain contextual learning, while unpunctuated tokens were randomly downsampled.
