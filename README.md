# Parkinson’s Personalized Ensemble  
**Adaptive Deep Learning Models for Parkinson’s Diagnosis using Smartwatch Sensor Data**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)  
[![PhysioNet Dataset](https://img.shields.io/badge/Dataset-PADS-blue)](https://physionet.org/content/parkinsons-sensor/1.0.0/)  
[![Built With](https://img.shields.io/badge/Built%20with-TensorFlow%20%7C%20XGBoost%20%7C%20Sklearn-green)](https://github.com/sonnymarmon/parkinsons-personalized-ensemble)

---

## Overview

This project builds and evaluates **adaptive deep learning models** (CNN, LSTM) and ensemble classifiers to detect movement disorders—specifically Parkinson’s Disease (PD)—using smartwatch sensor data.  

It leverages the [`PADS` dataset (PhysioNet)](https://physionet.org/content/parkinsons-sensor/1.0.0/) and focuses on real-time task classification, condition prediction, and future personalization pipelines.

---

## Objectives

- Use smartwatch accelerometer + gyroscope data from 469 patients
- Build baseline XGBoost + deep learning (CNN, LSTM) models
- Integrate patient-specific personalization via fine-tuning
- Benchmark classification performance across models
- Prepare for publication and AI competitions (e.g. Microsoft Imagine Cup)

---

## Repository Structure
parkinsons-personalized-ensemble/
│
├── data/
│ ├── raw/ # Raw .bin and JSON files (3 patients only)
│ └── processed/ # Pre-extracted window data (.npy files)
│
├── notebooks/
│ ├── data_preprocessing.ipynb # Windowing and feature extraction
│ ├── train_base_models.ipynb # XGBoost classifier
│ └── train_deep_models.ipynb # CNN & LSTM models
│
├── paper/
│ ├── paper_draft.tex # Research draft (WIP)
│ └── figures/ # Plots and visualizations
│
├── requirements.txt
├── README.md
└── LICENSE


---

## Dataset: PADS (Parkinson’s Disease Smartwatch)

- **Source**: University Hospital Münster (Germany), via PhysioNet  
- **Subjects**: 469 individuals  
- **Sensors**: Apple Watch Series 4 (accelerometer + gyroscope)  
- **Tasks**: 11 guided neurological movements  
- **Classes**: Parkinson’s Disease, Other Disorders, Healthy Controls  

> For full access: [https://physionet.org/content/parkinsons-sensor/1.0.0/](https://physionet.org/content/parkinsons-sensor/1.0.0/)

---

## Setup

1. Clone repo:
   ```bash
   git clone https://github.com/sonnymarmon/parkinsons-personalized-ensemble.git
   cd parkinsons-personalized-ensemble
