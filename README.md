# WavePurity - Phase 1 (Legacy Project)

> **Note**: This is an old project developed for audio classification using traditional machine learning approaches. It serves as a foundation for understanding audio feature extraction and basic neural network implementations.

## Project Overview

WavePurity is an audio classification system that combines two popular audio datasets (UrbanSound8K and ESC-50) to create a comprehensive sound classification model. The project implements three different neural network architectures to compare their performance on audio classification tasks.

## 🎯 Objectives

- Combine and standardize audio datasets from different sources
- Extract meaningful features from audio signals using MFCC (Mel-Frequency Cepstral Coefficients)
- Implement and compare three neural network architectures:
  - **ANN** (Artificial Neural Network)
  - **CNN1D** (1D Convolutional Neural Network)
  - **CNN2D** (2D Convolutional Neural Network)
- Evaluate model performance and visualize results

## 📊 Datasets Used

### UrbanSound8K
- Contains 8,732 labeled sound excerpts (≤4s) of urban sounds
- 10 classes: air_conditioner, car_horn, children_playing, dog_bark, drilling, engine_idling, gun_shot, jackhammer, siren, street_music

### ESC-50
- Collection of 2,000 environmental audio recordings
- 50 classes organized into 5 major categories
- Each clip is 5 seconds long

## 🔧 Technical Implementation

### Feature Extraction
- **MFCC Features**: 40 coefficients extracted from each audio file
- **Audio Processing**: Using librosa library for audio loading and feature extraction
- **Standardization**: Consistent preprocessing across both datasets

### Model Architectures

#### 1. ANN (Artificial Neural Network)
```
Input Layer (40 features) → Dense(256) → Dense(128) → Output Layer
```

#### 2. CNN1D (1D Convolutional Neural Network)
```
Input Layer → Conv1D(64) → MaxPooling1D → Flatten → Dense(128) → Output Layer
```

#### 3. CNN2D (2D Convolutional Neural Network)
```
Input Layer → Conv2D(32) → MaxPool2D → Flatten → Dense(128) → Output Layer
```

## 📈 Features

- **Data Visualization**: Distribution analysis of audio categories across datasets
- **MFCC Visualization**: Spectral representation of sample audio files
- **Model Comparison**: Side-by-side evaluation of different architectures
- **Performance Metrics**: Precision, Recall, F1-Score for each model
- **Audio Testing**: Real-time prediction on sample audio files with visualization

## 🛠️ Dependencies

```python
- librosa
- tensorflow/keras
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- tqdm
- IPython
```

## 📊 Expected Results

The project provides comparative analysis between three different approaches to audio classification, showing:
- Training/validation loss and accuracy curves
- Performance metrics (Precision, Recall, F1-Score)
- Visual analysis of audio features (waveform, spectrogram, MFCC)

## ⚠️ Legacy Status

This project represents an earlier approach to audio classification using traditional feature extraction methods. Modern implementations might benefit from:
- End-to-end deep learning approaches
- Transformer-based architectures
- More sophisticated data augmentation techniques
- Advanced audio preprocessing methods

## 🔄 Future Improvements

For next phases, consider checking out future vision.md


## 📝 Notes

- Original implementation designed for Google Colab environment
- Paths may need adjustment for local execution
- Models are saved in H5 format for easy loading and deployment

---

*This project serves as a learning foundation for audio machine learning and demonstrates the evolution of audio classification techniques.*
