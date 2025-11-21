Fusion of CNN Image Features + Tumor Boundary Shape Features

This repository contains a novel multimodal deep learning model for brain tumor classification using MRI slices. Unlike typical CNN-only approaches, this project explicitly leverages tumor boundary geometry from the dataset to improve accuracy.

Uses the Brain Tumor Dataset (Jun Cheng et al.)
Includes 3064 T1-weighted contrast-enhanced MRI slices stored in .mat format.

Novel Shape Feature Extraction
Uses cjdata.tumorBorder field (usually ignored in research) to compute:
Area
Perimeter
Roundness
Irregularity
Convex Hull Ratio
Fractal Dimension
These geometric radiomics features describe the tumor's morphological complexity.

Model has two branches:
CNN Branch → learns MRI image features
MLP Shape Branch → learns boundary geometry features

Performance Improvement
Baseline CNN Accuracy: ~80%
Fusion Model Accuracy: ~83%
Improvement: +2.93%
This proves that tumor boundary geometry adds discriminative value.

Repository                Contents
File	Descriptio
fusion_model.h5          	Trained fusion model (CNN + shape features)
baseline_cnn_model.h5    	CNN-only baseline model
shape_scaler.pkl	        StandardScaler for 6 shape features
Welcome_To_Colab.ipynb   	Full training notebook (Google Colab)
README.md	                Project documentation

