# 🌍 Multi-Task SegFormer: Classification + Segmentation + (Optional) Change Detection
Satellite Image Understanding using Transformers | EuroSAT Dataset

This repository contains a Multi-Task SegFormer-based deep learning framework capable of performing image classification, semantic segmentation, and optionally change detection on satellite imagery.
The model is trained on a cleaned EuroSAT dataset and supports a fully automated end-to-end pipeline.

🚀 Project Highlights
✔ Multi-Task Learning Framework

A single SegFormer model performs:
*Image Classification
*Semantic Segmentation
*(Extendable) Change Detection
*Instead of using separate models, a shared transformer encoder powers multiple prediction heads → enabling:
*Faster inference
*Lower GPU usage
*Better generalization
*Richer scene understanding

✨ Novel Contributions
🔹 1. Unified Multi-Task SegFormer Architecture
*Shared MiT (Transformer) encoder
*Separate decoder heads:
*classification
*segmentation
*optional change detection
*Joint optimization for efficient learning

🔹 2. Domain Adaptation for Remote Sensing
*SegFormer pretrained on ADE20K (natural images) → fine-tuned successfully on satellite imagery.
*The pipeline demonstrates how transformer architectures transfer across domains even with limited samples.

🔹 3. Extendable Change Detection Head
*Although training is on single-date EuroSAT imagery, the architecture includes:
*dual-image feature fusion support
*differencing blocks
*pixel-wise change masks

This allows effortless extension to datasets like LEVIR-CD, WHU-CD, CDD, etc.

🔹 4. Lightweight & Reproducible Pipeline
*Cleaned and resized dataset
*Automatic data loaders
*Mixed-precision FP16 training
*Works on T4/L4/A100 GPUs

Automated export of:
*trained weights
*classification outputs
*segmentation mass
*visualizations

🛠 Future Work
*Full change-detection training
*Integration with temporal satellite datasets
*Deployment using Gradio
*Real-time geospatial inference pipeline
