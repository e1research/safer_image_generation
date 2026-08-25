
# Context-Aware Visual Safety Framework for Generative Image Editing

This repository contains the code, datasets, prompts, and reproducibility materials for a proof-of-concept study proposing a two-stage contextual safety framework for generative image editing. The framework combines a **Semantic Sensitivity (SS) Gate** for prompt-level screening with a **Visual Context Safety (VCS) Gate** for image-level contextual assessment.

## Repository Contents

### `safe_llm_for_women_DeepLearning.ipynb`

This notebook contains the implementation and outputs related to the deep learning models used for the VCS Gate, including:

* Model training and evaluation
* Five-fold cross-validation results
* Confusion matrices
* Training convergence curves
* Grad-CAM visualizations and feature consistency analysis

### `safe_llm_for_women_externalVal_and_classicalML.ipynb`

This notebook contains the implementation of the classical machine learning models coupled with pretrained vision architectures, including **CLIP-ViT** and **DINOv2** feature extraction.

It also includes:

* Internal evaluation of the pretrained-feature + ML models
* External validation experiments
* Prompt construction for the validation experiments
* Comparative evaluation of deep learning and pretrained-feature approaches
* Conditional and end-to-end system evaluation

### `safe_llm_for_women_intentGate.ipynb`

This notebook contains the implementation of the **Semantic Sensitivity (SS) Gate**, including:

* Prompt dataset construction
* Prompt crafting and categorization
* Text embedding and feature representation
* Model training and evaluation
* Internal and external validation metrics

## Datasets

The internal dataset constructed for the **Visual Context Safety (VCS) Gate** ($N = 267$) is available here:

[Internal VCS Gate Dataset](https://drive.google.com/drive/folders/1gb9PpRyxhOya1nmQ-6-8R-fxMrJJ0pXU?usp=sharing&utm_source=chatgpt.com)

The external validation dataset is available here:

[External Validation Dataset](https://drive.google.com/drive/folders/14Lc_ig1vydieZ6vQqytlcdi1RqspgFvz?usp=sharing&utm_source=chatgpt.com)

## Prompts

The prompts used to generate the internal and external image samples are available in the following spreadsheet:

[Prompt Dataset and Generation Records](https://docs.google.com/spreadsheets/d/1-IX1GoknwOIF3txoziTlqS3qv_0dANaHiBgP4C-0a-M/edit?usp=sharing&utm_source=chatgpt.com)

The spreadsheet documents the prompts associated with the generated samples and supports inspection of the dataset construction and validation procedures.

Prompts used to train and evaluate the SS Gate are available in `safe_llm_for_women_intentGate.ipynb`, and the prompts for system external validation are available in `safe_llm_for_women_externalVal_and_classicalML.ipynb`. 

## Reproducibility

All experiments were conducted using **Google Colab**. To reproduce the experiments using the provided notebooks:

1. Download the internal and external VCS datasets from the links above.
2. Upload the datasets to your Google Drive.
3. Open the corresponding `.ipynb` notebook in Google Colab.
4. Update the dataset paths, if necessary, to match your Google Drive directory structure.
5. Run the notebook cells sequentially.

The notebooks contain the code used for dataset processing, model training, validation, visualization, and system-level evaluation. Setup should require only minor path adjustments once the datasets are uploaded to Google Drive.
