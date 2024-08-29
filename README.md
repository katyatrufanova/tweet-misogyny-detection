# Tweet Misogyny Detection

## Project Overview

This project focuses on the automatic detection of misogynistic content in tweets using state-of-the-art language models. The study compares the performance of AlBERTo, UmBERTo, and XLM-T models in both binary and ternary classification tasks, with and without data augmentation.

## Dataset

The dataset used in this project is from the Automatic Misogyny Identification (AMI) task, which is part of the EVALITA 2020 campaign. Due to the terms of use, the dataset is not included in this repository. To obtain the dataset, please visit the AMI EVALITA 2020 website and follow their instructions to request access.
Once you have obtained the dataset, place the files in a folder named dataset in your Google Drive, maintaining the following structure:

```
dataset/
├── testset/
│   ├── AMI2020_test_identityterms
│   ├── AMI2020_test_raw_gold_anon.tsv
│   └── AMI2020_test_synt_gold.tsv
└── trainingset/
    ├── AMI2020_training_identityterms
    ├── AMI2020_training_raw_anon.tsv
    └── AMI2020_training_synt.tsv
```

## Project Structure
This project consists of several Jupyter notebooks, each focusing on a specific model and classification task. The notebooks are designed to be run in Google Colab to take advantage of free GPU resources.

### Notebooks:
- `AlBERTo_binary_classification.ipynb`
- `UmBERTo_binary_classification.ipynb`
- `XLM-T-binary.ipynb`
- `AlBERTo_ternary_classification.ipynb`
- `UmBERTo_ternary_classification.ipynb`
- `XLM-T-ternary.ipynb`
- `AlBERTo_binary_augmented.ipynb`
- `UmBERTo_binary_augmented.ipynb`
- `XLM_t_binary_augmented.ipynb`
- `AlBERTo_ternary_augmented.ipynb`
- `UmBERTo_ternary_augmented.ipynb`
- `XLM_T_ternary_augmented.ipynb`

## Setup and Execution
1. Upload the notebooks to your Google Drive.
2. Open the notebooks using Google Colab.
3. Ensure that the dataset is placed in your Google Drive as described in the Dataset section.
4. Run the cells in the notebooks sequentially.

*Note: The notebooks include all necessary package installations and imports.*

## Models
This project evaluates three state-of-the-art models:
- **AlBERTo**: A BERT-based model pre-trained on Italian tweets.
- **UmBERTo**: Another BERT-based model pre-trained on a large Italian corpus.
- **XLM-T**: A multilingual model capable of processing text in multiple languages, including Italian.

## Experiments
The project consists of 12 experiments:
1. Binary classification (misogynous vs. non-misogynous) for each model
2. Ternary classification (non-misogynous, misogynous but not aggressive, aggressive and misogynous) for each model
3. Binary classification with data augmentation for each model
4. Ternary classification with data augmentation for each model

## Results
The results of the experiments are presented in the individual notebooks. A summary of the findings can be found in the project report.

## Additional Files
- `Presentation.pdf`: A presentation summarizing the project, methodology, and results.
- `Report.pdf`: A detailed report of the project, including introduction, methodology, results, and analysis.

## Acknowledgments
- EVALITA 2020 AMI task organizers for providing the dataset
- AlBERTo: Italian BERT Language Understanding Model Polignano et al., 2019 [Paper](https://www.scopus.com/inward/record.uri?eid=2-s2.0-85074851349&partnerID=40&md5=7abed946e06f76b3825ae5e294ffac14) [Github Repository](https://github.com/marcopoli/AlBERTo-it)
- UmBERTo: Italian Language Model trained with Whole Word Masking Parisi et al., 2020 [Github Repository](https://github.com/musixmatchresearch/umberto)
- XLM-T: Multilingual Language Models in Twitter Barbieri et al., 2022 [Paper](https://aclanthology.org/2022.lrec-1.27) [Github Repository](https://github.com/cardiffnlp/xlm-t)
