# EV Power Forecasting: Research and Analysis

This repository contains the code, data, and research paper for forecasting electric vehicle (EV) power demand using machine learning models. The project uses historical EV charging data from Palo Alto (2011-2021) to compare various time-series forecasting methods.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Models](#models)
- [Repository Structure](#repository-structure)
- [How to Use](#how-to-use)
- [Results](#results)
- [Research Paper](#research-paper)
- [Acknowledgments](#acknowledgments)

## Introduction

The growing adoption of electric vehicles (EVs) emphasizes the need for accurate power demand forecasting to optimize grid operations. This project evaluates and compares three machine learning models for EV load forecasting:

- **Long Short-Term Memory (LSTM)**
- **Bidirectional LSTM (BiLSTM)**
- **Sequence-to-Sequence (Seq2Seq)**

Our goal is to identify the most effective model for predicting EV power consumption using real-world data.

## Dataset

The dataset consists of EV charging data collected in Palo Alto from **2011 to 2021**. It includes information on charging sessions, power consumption, and timestamps. The data is preprocessed to remove anomalies and standardize formats.

## Models

### 1. LSTM
A recurrent neural network (RNN) variant designed to handle long-term dependencies, making it suitable for time-series forecasting.

### 2. BiLSTM
An extension of LSTM that processes input sequences in both forward and backward directions for improved context awareness.

### 3. Seq2Seq
A model architecture often used in sequence prediction tasks, such as translation and time-series forecasting, leveraging an encoder-decoder framework.

## Repository Structure

```
├── main.ipynb         # Main code for training and evaluating models
├── wrapper.ipynb      # Data preprocessing and preparation
├── EV_Power_Forecasting2.pdf  # Research paper detailing the methodology and results
├── data/              # Folder for storing the dataset
└── results/           # Folder for storing model outputs and performance metrics
```

## How to Use

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ogjash/ev-power-forecasting.git
   cd ev-power-forecasting
   ```

2. **Install Dependencies**:
   Make sure you have Python and Jupyter Notebook installed. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. **Train and Evaluate Models**:
   Use `main.ipynb` to train the models and evaluate their performance.

## Results

### Model Comparison
| Model      | RMSE   | MAE    |
|------------|--------|--------|
| LSTM       | 0.143  | 0.109  |
| BiLSTM     | 0.118  | 0.080  |
| Seq2Seq    | 0.111  | 0.073  |

The Seq2Seq model demonstrated the best overall performance, particularly in capturing complex temporal patterns.

## Research Paper

For detailed methodology, analysis, and insights, refer to the research paper [EV Power Forecasting2.pdf](https://github.com/user-attachments/files/18275539/EV.Power.Forecasting2.pdf).

## Acknowledgments

- Data sourced from the City of Palo Alto.
- Gratitude to the mentors and collaborators who guided this research.
- Data is already preprocessed by code in wrapper.ipynb
