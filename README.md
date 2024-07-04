# Egyptian ASR Transformer
## Table of contents
1. [Project Overview](#Project-Overview)

2. Features

3. Dataset

4. Preprocessing
    - Audio Cleaning
    - Spectrogram Extraction

5. Model Architecture

## Project Overview
This repository contains the code and resources for a Transformer-based Automatic Speech Recognition (ASR) system tailored for the Egyptian dialect of Arabic. The system is designed to handle a dataset of 100 hours of audio recordings, employing advanced preprocessing techniques and a state-of-the-art Transformer architecture to achieve high accuracy in transcription.

*Automatic Speech Recognition (ASR)* systems are revolutionizing the possibilities in this area. Recent developments in speech signal processing, such as speech recognition, speaker diarization, etc., have inspired numerous applications of speech technologies. The development of Arabic Speech Recognition has been lagging compared to the advances of first-tier languages due to many reasons such as the availability of open-source data, the limited number of involved research groups, and the wide variability existing between the formal standard Arabic and the locally spoken Arabic dialects.

## Features
- **Audio Preprocessing**: Cleans and prepares raw audio data.
- **Spectrogram Extraction**: Converts audio signals into spectrograms for model input.
- **Transformer Architecture**: Utilizes a Transformer model for ASR tasks.
- **Customizable Hyperparameters**: Allows tuning of model parameters for optimized performance.

## Dataset
A data resource consisting of 100 hrs. of Egyptian dialect speech data is used for the competition.
Many usage scenarios for ASR systems are in an outdoor context where the audio signal embeds the effects of compound noise sources. In this challenge, we target the performance of ASR in noisy environments.

The dataset comprises 100 hours of audio recordings in the Egyptian dialect of Arabic. Each audio file is accompanied by its corresponding transcription.

## Preprocessing
### Audio Cleaning

The audio cleaning process involves:
1. **Noise Reduction**: Removing background noise using techniques such as spectral gating.
2. **Silence Removal**: Detecting and removing silence segments.
3. **Normalization**: Normalizing audio volume levels for consistency.

### Spectrogram Extraction

Spectrograms are extracted from the cleaned audio using the following steps:

1. **Framing**: Splitting the audio signal into overlapping frames.
2. **Windowing**: Applying a window function (e.g., Hamming window) to each frame.
3. **Fourier Transform**: Converting each frame to the frequency domain using Short-Time Fourier Transform (STFT).
4. **Log Scaling**: Converting the magnitude spectrum to a logarithmic scale to emphasize perceptually relevant frequencies.

## Model Architecture
### Transformer Model
The Transformer model architecture includes:

1. **Encoder**: Consists of multiple layers, each with self-attention and feed-forward neural networks.
2. **Decoder**: Mirrors the encoder structure and incorporates attention mechanisms to focus on relevant parts of the input during transcription.
3. **Positional Encoding**: Adds positional information to the input embeddings to preserve the order of sequences.

## Training
Training the model involves:

1. **Data Preparation**: Splitting the dataset into training, validation, and test sets.
2. **Hyperparameter Tuning**: Adjusting learning rate, batch size, number of layers, etc.
3. **Training Loop**: Iteratively updating model weights using backpropagation and optimization techniques (e.g., Adam optimizer).
4. **Checkpointing**: Saving model checkpoints for recovery and evaluation.

## Evaluation
The model's performance is evaluated using:

- **Word Error Rate (WER)**: Measures the accuracy of transcriptions by comparing them to the ground truth.
