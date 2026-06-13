# ECG Signal-to-Image Mapping with CNN Classification

A biomedical signal processing project that converts 1D ECG signals into 2D frequency images (Spectrograms) using Short-Time Fourier Transform (STFT), then classifies them using a Convolutional Neural Network (CNN).

## Project Overview

| Item | Details |
|------|---------|
| Dataset | MIT-BIH Arrhythmia (87,554 heartbeats) |
| Method | STFT Spectrogram + CNN |
| Accuracy | ~77% (10 epochs, 1000 samples) |
| Framework | TensorFlow / Keras |

## Methodology

1. **Load ECG Data** — MIT-BIH Arrhythmia dataset (normal vs arrhythmia)
2. **Signal-to-Image** — Convert each heartbeat to a 2D spectrogram via STFT
3. **CNN Classification** — Train a CNN on spectrogram images to detect arrhythmia

## Results

- Training Accuracy: ~77%
- The model successfully distinguishes normal ECG patterns from arrhythmic ones
- Spectrogram visualization reveals clear frequency-domain differences between classes

## Course

Introduction to Biomedical Signal Processing  
Islamic Azad University, East Tehran Branch — 2025
