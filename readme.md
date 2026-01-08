# Spectral-Normalised DCGAN for CIFAR-100 Image Generation

This repository contains the code and report for a generative modelling project using a **Spectral-Normalised Deep Convolutional GAN (SN-DCGAN)** trained on the **CIFAR-100** dataset.

## Overview
- Task: Unconditional image generation
- Dataset: CIFAR-100 (32×32 RGB images)
- Model: DCGAN with **spectral normalisation** applied to the discriminator
- Evaluation metric: Fréchet Inception Distance (FID)

## Method
- Generator: Convolutional architecture with batch normalisation and ReLU activations
- Discriminator: Convolutional architecture with spectral normalisation and LeakyReLU
- Training uses an adversarial minimax objective with Adam optimisation
- Hyperparameters tuned via targeted grid search:
  - Learning rate
  - Momentum parameters
  - Generator/discriminator capacity balance

## Results
- **FID score: 56.63**
- **973,936 parameters**
- Trained for **50,000 optimisation steps**
- Generated images exhibit structural diversity and a continuous latent space

## Repository Contents
- `report.pdf` — Detailed methodology, theory, experimental setup, results, and limitations
- `dcgan.py` — Generator, discriminator, and training loop implementation

## Notes
The project focuses on **training stability, evaluation of generative quality**, and the impact of spectral normalisation on adversarial learning dynamics.
