# Skincancer_detection
This project is part of the ISIC 2024 Skin Cancer Detection Challenge, aiming to develop AI models that detect malignant skin lesions from real-world smartphone-like images. The focus is on building reliable diagnostic systems for early screening in primary care settings.
ISIC 2024 – Skin Cancer Detection with 3D-TBP

This repository presents our complete solution for the ISIC 2024 Skin Cancer Detection Challenge, an international competition focused on building reliable AI systems for the early detection of malignant skin lesions. The primary objective of this challenge is to develop models that can accurately classify skin cancer from lesion images captured under real-world conditions, similar to those taken using smartphones in primary healthcare or non-clinical environments.

Unlike traditional dermoscopy-based datasets, which are collected in controlled clinical settings, the ISIC 2024 dataset introduces significant variability in lighting, background noise, and image quality. It contains lesion images along with extensive patient metadata from thousands of patients across three continents, enabling the development of more robust and generalizable diagnostic models.

# Our Methodology

To achieve strong performance, we adopted a multimodal learning approach by integrating both image data and tabular patient information:

Deep Learning for Image Classification:
We experimented with several state-of-the-art CNN backbones such as EfficientNet and ResNet to extract meaningful lesion representations from images.

Tabular Machine Learning Models:
Patient metadata was leveraged using Gradient Boosted Decision Tree algorithms including XGBoost, LightGBM, and CatBoost, which proved effective for structured clinical features.

Imbalance Handling Strategies:
Since malignant samples are significantly fewer than benign ones, we applied focal loss, stratified sampling, and Faiss-based undersampling techniques to improve model stability and reduce bias.

Feature Fusion and Ensemble Learning:
We combined CNN feature embeddings with metadata-based predictions, and further boosted accuracy through ensemble methods integrating outputs from multiple models.

# Repository Highlights

This repository includes dedicated notebooks for:

Faiss-based balanced data creation

Tabular-only training with GBDT models

Multimodal image + metadata training pipelines

Exploratory Data Analysis (EDA) for dataset insights

Overall, this project aims to contribute toward accessible, scalable, and accurate automated skin cancer screening systems that can support early diagnosis beyond specialized clinical environments.
