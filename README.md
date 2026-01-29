# SpikeGate-YOLO
Official PyTorch implementation of SpikeGate-YOLO. An energy-efficient SNN for object detection.
# SpikeGate-YOLO

**SpikeGate-YOLO: An Energy-Efficient Spiking Neural Network for Object Detection with Dynamic Pruning**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Framework](https://img.shields.io/badge/Framework-PyTorch-orange.svg)]()
[![Status](https://img.shields.io/badge/Status-Under%20Review-red)]()

> **📢 Note:** This repository hosts the official PyTorch implementation of the paper **"SpikeGate-YOLO"**. 
>
> **The full source code, pretrained models, and configuration files will be publicly released immediately upon the acceptance of the paper.** We are currently finalizing the documentation and code cleanup to ensuring reproducibility.

## 📖 Introduction

SpikeGate-YOLO is a novel Spiking Neural Network (SNN) framework designed for high-performance and energy-efficient object detection on edge devices. By introducing the **Reparam-Spike Gating (RSG)** mechanism and **Spike Multi-scale Difference Feature Hallucination (SpikeMDFH)**, our method effectively suppresses background noise and aligns multi-scale temporal features.

### Key Features:
- **State-of-the-Art Accuracy:** Achieves **69.3% mAP** on the Gen1 automotive dataset, outperforming existing SNN detectors.
- **Extreme Sparsity:** The RSG module reduces the average firing rate in deep layers to **0.11**, significantly minimizing redundancy.
- **Energy Efficiency:** Reduces dynamic power consumption by **~24%** compared to SpikeYOLO, achieving a superior Power-to-Parameter ratio.
- **Generalizability:** Plug-and-play support for various backbones, including Anchor-free YOLO and ResNet architectures.

## 🚀 Installation & Requirements (Coming Soon)

The code is built on PyTorch and SpikingJelly. Detailed installation instructions will be provided.

**Prerequisites (Expected):**
- Python >= 3.8
- PyTorch >= 1.12
- SpikingJelly
- CUDA Toolkit

## 📊 Model Zoo & Results

We will provide pretrained weights for both **COCO 2017** and **Gen1** datasets.

| Model | Backbone | Dataset | mAP@50 | Power (mJ) | Download |
| :---: | :---: | :---: | :---: | :---: | :---: |
| SpikeGate-YOLO | YOLO-S | Gen1 | 69.3% | 14.1 | *Coming Soon* |
| SpikeGate-YOLO | ResNet-18 | Gen1 | 54.3% | -- | *Coming Soon* |

## 🛠️ Usage

### Training
```bash
# Example command (Placeholder)
python train.py --cfg configs/spikegate_yolo_gen1.yaml --batch-size 32
