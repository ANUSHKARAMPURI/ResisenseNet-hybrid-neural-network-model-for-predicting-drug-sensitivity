# Drug Repurposing in Breast Cancer: Overcoming Drug Resistance with ResisenseNet

## Overview

This repository focuses on drug repurposing, a promising approach to identifying new therapeutic applications for existing drugs. Drug repurposing faces several challenges, including:

## Drug resistance: A major obstacle, particularly in breast cancer treatment, where cancer cells develop mechanisms to evade the effects of therapies.

Role of transcription factors (TFs) and mutations: Both significantly influence drug sensitivity and resistance. Mutations can alter drug targets, while TFs regulate pathways critical to cancer progression and drug response.

The ResisenseNet model was developed to address these challenges, integrating multi-omic data to enhance drug sensitivity predictions and support repurposing strategies.

Dataset: DoRothEA

## The DoRothEA dataset serves as the foundational resource for this project. Key features include:

Content: Comprehensive information on transcription factors, proteins, ligand molecules, and their corresponding descriptors.

Relevance: This dataset provides valuable insights into regulatory pathways and molecular interactions, making it ideal for studying drug resistance mechanisms in breast cancer.

# ResisenseNet Model

* Objective

The ResisenseNet model leverages both ligand- and protein-based features to predict drug sensitivity and identify potential repurposing candidates for breast cancer treatment.

Key Features

* Model Architecture:

Utilizes a hybrid approach combining 1D-Convolutional Neural Networks (1D-CNN) and Deep Layer Perceptrons (DLP) to perform binary classification on drug sensitivity.

* Data Integration:

Incorporates transcription factor and protein data from the DoRothEA dataset, alongside ligand molecule descriptors.

* Rationale

Previous experiences in developing ligand-based screening tools highlighted the need to include protein-based features, which play a crucial role in drug-target interactions.

* Transfer Learning

## To enhance the model's performance and leverage existing knowledge:

* Ligand embeddings: Utilized Mol2Vec (a module in RDKit) to embed ligand molecules into vector representations.

* Protein embeddings: Employed Protein BERT modules to encode amino acid sequences into feature vectors.

These embeddings were combined and used to train the ResisenseNet model, enabling it to make more accurate predictions about drug sensitivity and resistance.

Applications

The trained ResisenseNet model is designed to:

* Screen anticancer drugs for drug sensitivity and resistance in a breast cancer context.

* Facilitate drug repurposing by identifying existing drugs with potential efficacy against resistant breast cancer.


# Getting Started

Prerequisites

* Python 3.8+

* Libraries: tensorflow, pytorch, rdkit, transformers, numpy, pandas


Future Work

* Expanding the dataset to include additional omics layers (e.g., epigenomics).

* Enhancing the model's ability to generalize across other cancer types.

* Developing a user-friendly web application for drug screening.

# Citation

If you use this repository, please cite the associated publication:
* Karampuri, A., Jakkula, B.K., & Perugu, S (2024): "ResisenseNet hybrid neural network model for predicting drug sensitivity and repurposing in breast cancer." Scientific Reports 14, 23949. DOI:10.1038/s41598-024-71076-0

Contact

For questions or collaborations, please contact:
Anush KarampuriEmail: anush.karampuri1@gmail.com

