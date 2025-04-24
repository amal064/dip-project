# Fourier-Inspired Augmentation Strategies for Improved Supervised Learning

This repository contains the implementation and results for the research paper:  
**_Fourier-Inspired Augmentation Strategies for Improved Supervised Learning_**  

## 📄 Overview

Deep learning models benefit greatly from data augmentation, especially in limited-data scenarios. While traditional augmentations like flipping and cropping operate in the image (spatial) domain, this project explores augmentations in the **Fourier (frequency) domain**.

We propose and evaluate four frequency-based augmentations:
- **AmplitudeRescale**
- **RandomFrequency**
- **PhaseShift**
- **GaussianMixture**

These are integrated into standard supervised learning pipelines and evaluated against baseline models on the Animal-10 image classification dataset using **ResNet-18** and **MobileNetV3**.

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- PyTorch
- NumPy
- Matplotlib
- scikit-learn
- Jupyter Notebook

Install dependencies:
```bash
pip install torch torchvision numpy matplotlib scikit-learn notebook
```

### Running the Notebooks

Launch Jupyter:
```bash
jupyter notebook
```
Open the desired notebook (baseline or augmented) and run all cells to train and evaluate models.

## 🧪 Experiments & Results

| Model         | Baseline Accuracy | With Fourier Augmentation |
|---------------|-------------------|----------------------------|
| ResNet-18     | 87.70%            | **95.53%**                 |
| MobileNetV3   | 87.85%            | **94.10%**                 |

Fourier domain augmentations consistently improve classification accuracy and robustness, particularly in low-data and noisy settings.

## 📊 Augmentations Explained

1. **AmplitudeRescale**: Random rescaling of the amplitude spectrum.
2. **RandomFrequency**: Perturb selected frequency bands with noise.
3. **PhaseShift**: Uniform/random shift in the phase spectrum.
4. **GaussianMixture**: Synthesizes new samples using a GMM fitted on frequency components.

Each transformation is applied in the Fourier domain and inverted back to the image domain for training.

## 📎 Paper

For a deep dive into methodology, theory, and results, refer to the [paper (PDF)](./Fourier_Inspired_Augmentation_Strategies_for_Improved_Supervised_Learning.pdf).

## ✍️ Authors

- Amal Bangari — [amal.bangari2022@vitstudent.ac.in](mailto:amal.bangari2022@vitstudent.ac.in)
- Snehil Chatterjee — [snehil.chatterjee2022@vitstudent.ac.in](mailto:snehil.chatterjee2022@vitstudent.ac.in)
- Geetha S — [geetha.s@vitstudent.ac.in](mailto:geetha.s@vitstudent.ac.in)
