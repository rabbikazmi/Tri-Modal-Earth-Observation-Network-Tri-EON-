# Multi-Task SegFormer: Classification, Segmentation and Change Detection  
Satellite Image Understanding using Transformers | EuroSAT Dataset

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-Latest-red.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![Model](https://img.shields.io/badge/Model-SegFormer-orange.svg)]()
[![Dataset](https://img.shields.io/badge/Dataset-EuroSAT-lightgrey.svg)]()


## Overview

This repository provides a Multi-Task learning framework built on **SegFormer**, capable of performing:

- Image Classification  
- Semantic Segmentation  
- Optional Change Detection  

The model is trained on a cleaned version of the EuroSAT dataset and supports a fully automated end-to-end training and inference pipeline.

## Project Highlights

### Multi-Task Learning Framework
A single SegFormer model performs multiple tasks using a shared transformer encoder and task-specific heads.  
This leads to:
- Faster inference  
- Reduced GPU memory usage  
- Better generalization  
- Richer scene understanding  

### Novel Contributions

#### 1. Unified Multi-Task SegFormer Architecture
- Shared MiT (Transformer) encoder  
- Separate decoder heads for classification, segmentation, and optional change detection  
- Joint optimization enabling efficient multi-task learning  

#### 2. Domain Adaptation for Remote Sensing
- Pretrained on ADE20K (natural images)  
- Successfully fine-tuned for satellite imagery  
- Demonstrates cross-domain transfer effectiveness for transformers  

#### 3. Extendable Change Detection Head
The architecture includes:
- Dual-image fusion support  
- Differencing feature blocks  
- Pixel-level change masks  

This allows easy extension to datasets such as LEVIR-CD, WHU-CD, and CDD.

#### 4. Lightweight and Reproducible Pipeline
- Cleaned and resized dataset  
- Automatic dataloaders  
- Mixed-precision FP16 training  
- Compatible with T4, L4, and A100 GPUs  

The framework auto-exports:
- Trained weights  
- Classification outputs  
- Segmentation maps  
- Visualizations  

