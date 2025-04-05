# 🧬 Automated Flagellar Motor Detection in Cryo-ET

This project provides an automated image processing pipeline using **YOLOv8 medium size model** for detecting **flagellar motors** in **cryo-electron tomography (cryo-ET)** data. The algorithm is designed to reduce manual annotation and improve scalability in the analysis of microbial motility machinery.

## 📚 Overview

The **flagellar motor** is a complex molecular machine responsible for microbial movement and is key in processes such as **chemotaxis** and **pathogenesis**. Understanding its structure and function requires high-resolution imaging, often achieved through **cryo-electron tomography (cryo-ET)**.

While cryo-ET provides detailed 3D images of cells in near-native states, automated analysis remains challenging due to:

- Low signal-to-noise ratios
- Variable orientations of the motor
- Dense, crowded cellular environments

This project addresses these limitations by offering a tool to **automatically identify the presence and location of flagellar motors** in tomograms.

## 📏 Metrics

| Metric    | Value   |
| --------- | ------- |
| Precision | ~84.5%  |
| Recall    | ~84.0%  |
| F1 Score  | ~84.3%  |
| mAP50     | ~86.6%  |
| mAP50-95  | ~42.03% |

> The `best` model weight can be downloaded from `models` directory.

## ✨ Features

- ✅ Automatic detection of flagellar motors in cryo-ET tomograms
- 📦 Modular pipeline for easy integration and customization
- ⚙️ Handles noisy data and orientation variability
- 📉 Reduces manual annotation time and effort
- 🧪 Ideal for high-throughput structural biology workflows

## 🛠 Installation

1. Clone the repository:

```bash
git clone https://https://github.com/yashkc2025/automated_flagellar_motor_detection.git
cd flagellar-motor-detection
```

2. Create a virtual environment and install dependencies:

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## 🧪 Data

The data for this notebook can be found at

- https://www.kaggle.com/competitions/byu-locating-bacterial-flagellar-motors-2025/data

## 📦 Folder Structure

The project is divided into two parts:

- `prepare_dataset.ipynb` - extracts useful 2d slices from scans and applies 8 bit image normalisation.
- `model.ipynb` - Finetunes model on our dataset and validates result
