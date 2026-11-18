# ECG Signal-to-Image Mapping with CNN (Prototype)

Course prototype: converts single ECG heartbeats into spectrogram images (STFT) and classifies them with a small CNN.

> **Status: early prototype.** This was built for the course *Introduction to Biomedical Signal Processing* (Islamic Azad University, East Tehran Branch, 2026). A rigorous, patient-independent version is being developed as a BSc thesis project.

## What this notebook does

- Data: Kaggle "Heartbeat" version of MIT-BIH (`mitbih_train.csv`, 87,554 beats, 5 classes, 125 Hz)
- Subset used: 500 normal beats (class 0) vs 500 supraventricular beats (class 1)
- Features: spectrogram per beat (`scipy.signal.spectrogram`, nperseg=32), resized to 32x32
- Model: small 2-layer CNN (Keras), 10 epochs

## Results

- Training accuracy reached about 77%. No held-out test set was used.

## Known limitations

- Only 1,000 beats used, two classes only (not general arrhythmia detection)
- Validation split was not shuffled and contained only class-1 beats, so validation metrics are not meaningful
- No patient information in this dataset version, so patient-independent evaluation is not possible
- Normalization applied before splitting; no fixed random seed

## Next

A corrected, patient-independent evaluation on the raw MIT-BIH database (inter-patient split, per-class metrics, baseline comparison) is planned as a separate repository.

## Course

Introduction to Biomedical Signal Processing  
Islamic Azad University, East Tehran Branch, 2026
