# Speech Recognition using Recurrent Neural Networks (RNN)

**Samudrala Hareesh** — 621243

## Overview

An LSTM-based RNN model that transcribes spoken digits (0–9) into text, leveraging the temporal dynamics of audio signals.

## Method

- **Dataset:** 1,700 labelled spoken-digit audio files, recorded by multiple speakers
- **Preprocessing:** Audio converted to MFCC (Mel Frequency Spectral Coefficients) features, normalized, and split into train/validation/test sets
- **Architecture:** MFCC input → 2 stacked LSTM layers (capturing sequential dependencies) → fully connected softmax output layer
- **Training:** 10 epochs, Adam optimizer, batch size 425, cross-entropy loss, trained via backpropagation through time (BPTT)

## Results

| Metric | Value |
|---|---|
| Test Accuracy | **94.42%** |
| Word Error Rate (WER) | **17.25%** |

Training and validation accuracy/loss curves showed steady convergence, with the model generalizing well to unseen data.

## Future Work

- Explore deeper architectures and attention mechanisms
- Try transformer-based models, data augmentation, and transfer learning to further reduce WER
