# SpikeGate-YOLO

**SpikeGate-YOLO: An Energy-Efficient Spiking Neural Network for Object Detection with Dynamic Pruning**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Framework](https://img.shields.io/badge/Framework-PyTorch-orange.svg)]()
[![Status](https://img.shields.io/badge/Status-Under%20Review-red)]()

> **📢 Note:** This repository hosts the official PyTorch implementation of the paper **"SpikeGate-YOLO"**. 
>
> **The full source code, pretrained models, and configuration files will be publicly released immediately upon the acceptance of the paper.** We are currently finalizing the documentation and code cleanup to ensure reproducibility.

## 📖 Introduction

**SpikeGate-YOLO** is a spiking object detection architecture optimized for spike-driven processing, designed to overcome the limitations of feature expression and inefficient fusion in existing SNNs. 

To address the structural redundancy and temporal information loss in traditional modules, we introduce a dual-path enhancement strategy featuring two novel components:

1.  **Reparam-Spike Gating (RSG) Block:** Synergizes structural reparameterization with dynamic feature recalibration. This block decouples training dynamics from inference efficiency and adaptively modulates information flow, significantly enhancing the capture of fine-grained textures while maintaining sparsity.
2.  **Spike Multi-Granularity Difference-aware Feature Harmonizer (SpikeMDFH):** A novel fusion module that utilizes difference-aware dynamic attention and biologically inspired gating to facilitate robust multi-scale feature fusion without compromising spike sparsity.

### Key Features:
- **State-of-the-Art Accuracy:** - **Gen1 (Neuromorphic):** Achieves **69.3% mAP@50** and **42.9% mAP50:95**, setting a new benchmark for event-based detection.
    - **COCO (Static):** Achieves **63.4% mAP@50** and **46.3% mAP50:95**, outperforming existing SNN-based detectors.
- **Extreme Sparsity:** The RSG module effectively filters redundant background noise, reducing the average firing rate in deep layers to **0.11**.
- **Energy Efficiency:** Reduces dynamic power consumption by **~24%** compared to SpikeYOLO, establishing a superior Pareto frontier between accuracy and energy cost.
- **Strong Generalizability:** The proposed RSG and SpikeMDFH components are plug-and-play, demonstrating consistent improvements across different architectures (e.g., Spike-YOLOv5, Spike-ResNet).

## 🚀 Installation & Requirements (Coming Soon)

The code is built on PyTorch and SpikingJelly. Detailed installation instructions will be provided.

**Prerequisites (Expected):**
- Python >= 3.8
- PyTorch >= 2.2.2
- SpikingJelly

## 📊 Model Zoo & Results

We provide baseline results for both **Neuromorphic (Gen1)** and **Static (COCO 2017)** datasets based on the paper's experiments.

### 1. Gen1 Automotive Dataset
Performance comparison with varying model sizes and time steps ($T$).

| Model | Params (M) | T | Power (mJ) | mAP@50 | mAP50:95 | Download |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| SpikeGate-YOLO-S | 18.2 | 4 | **9.8** | 67.2% | 41.7% | *Coming Soon* |
| SpikeGate-YOLO-L | 31.6 | 1 | 4.7 | 64.4% | 39.9% | *Coming Soon* |
| SpikeGate-YOLO-L | 31.6 | 2 | 8.8 | 66.3% | 41.5% | *Coming Soon* |
| **SpikeGate-YOLO-L** | **31.6** | **4** | 14.1 | **69.3%** | **42.9%** | *Coming Soon* |

### 2. COCO 2017 Dataset

| Model | Params (M) | T | mAP@50 | mAP50:95 | Download |
| :---: | :---: | :---: | :---: | :---: | :---: |
| SpikeGate-YOLO-S | 18.2 | 1 | 60.8% | 44.2% | *Coming Soon* |
| **SpikeGate-YOLO-L** | **31.7** | **1** | **63.4%** | **46.3%** | *Coming Soon* |

## 🛠️ Usage

### Training
```bash
# Example command
python train.py

Inference
# Example command 
python test.py 
