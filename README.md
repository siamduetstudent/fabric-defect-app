# Project 06: Fabric Defect Detection for Quality Control

## Overview
This project automates the manual inspection of fabric rolls in the textile industry. It builds a binary Convolutional Neural Network (CNN) classifier to detect defective vs. non-defective fabric patches. A Grad-CAM visualization layer is integrated to highlight the specific region triggering the defect classification, making the AI's decision interpretable for quality inspectors.

This project is part of the **Applied Machine Learning — EDGE Series**, DUET Gazipur.

## Features
- **Binary Image Classification:** Detects whether a fabric patch is defective or clean.
- **Explainable AI (Grad-CAM):** Generates a heatmap overlaid on the original image, localizing the defect.
- **Interactive GUI:** Built with Gradio, allowing users to upload images, view confidence scores, and analyze Grad-CAM heatmaps side-by-side.
- **Synthetic Data Augmentation:** Balances the dataset by generating synthetic non-defective patches from blurred defect crops.

## Dataset
- **Primary Source:** NEU Surface Defect Database / Kaggle Fabric Defect Dataset.
- **Classes:** Defective (1), Non-Defective (0).
- **Preprocessing:** Resized to 224x224, normalized to [0, 1].

## Repository Structure
```text
├── README.md
├── notebook.ipynb         # Complete Kaggle notebook with EDA, Training, and GUI
├── data/                  # Directory for raw dataset (not included in repo)
├── output/                # Saved models and plots (best_model.keras, eda.png, etc.)
└── examples/              # Sample images for the GUI demo