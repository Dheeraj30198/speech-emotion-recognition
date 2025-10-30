# Speech Emotion Recognition Using RNN and MFCC Features

This project implements Speech Emotion Recognition using Recurrent Neural Networks (RNN) and Mel Frequency Cepstral Coefficient (MFCC) features, trained on the RAVDESS dataset.

## Overview

Speech Emotion Recognition (SER) aims to detect human emotions from speech signals. This repository demonstrates a deep learning approach using MFCC features extracted from audio and an LSTM-based RNN for classification.

## Features

- **MFCC Feature Extraction**: Converts raw audio into features suitable for emotion recognition.
- **RNN Model (LSTM)**: Leverages temporal relationships in speech for improved emotion classification.
- **RAVDESS Dataset**: Uses a publicly available, labeled emotional speech corpus.
- **Jupyter Notebooks / Google Colab**: Provides step-by-step guidance for data preparation, feature extraction, model training, and inference.

## Project Structure

```
speech-emotion-recognition/
│
├── notebooks/
│   ├── 01_data_setup.ipynb        # Downloading and organizing the dataset
│   ├── 02_feature_extraction.ipynb # Extract MFCC features from audio
│   ├── 03_model_training.ipynb    # Train RNN (LSTM) on features
│   └── 04_inference.ipynb         # Perform emotion recognition on new samples
├── data/                          # Preprocessed features (MFCCs)
├── requirements.txt               # Python dependencies
└── README.md
```

## Google Colab

You can run all notebooks directly on [Google Colab](https://colab.research.google.com/):

- **No local setup required**: Simply open each notebook in Colab and follow the steps.
- **GPU acceleration**: Use Colab’s free GPU for faster training.
- **Data Handling**: Upload the RAVDESS dataset to Colab or use Google Drive integration for persistent storage.
- **Environment**: Install dependencies using `!pip install -r requirements.txt` or add individual packages as needed in a notebook cell.

**How to use on Colab:**
1. Open [Google Colab](https://colab.research.google.com/).
2. Upload the notebook (`.ipynb`) file or use the GitHub import feature (`File > Open notebook > GitHub`).
3. Run the setup and follow instructions in each notebook cell.
4. For larger datasets, consider mounting your Google Drive:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

## Installation (Local, Optional)

1. **Clone the repository**
   ```bash
   git clone https://github.com/Dheeraj30198/speech-emotion-recognition.git
   cd speech-emotion-recognition
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download the RAVDESS dataset**
   - The instructions for downloading are provided in `01_data_setup.ipynb`.

## Usage

Run the Jupyter notebooks (locally or on Colab) in order:

1. **Data Setup**: Download and organize the raw RAVDESS audio files.
2. **Feature Extraction**: Extract MFCC features and save them to the `data/` directory.
3. **Model Training**: Train an LSTM-based RNN using the extracted features.
4. **Inference**: Test the trained model on new or unseen samples.

## Dataset

- **RAVDESS**: [Ryerson Audio-Visual Database of Emotional Speech and Song](https://zenodo.org/record/1188976)
  - Contains 24 professional actors vocalizing two statements with various emotional intonations.
  - Emotions include: calm, happy, sad, angry, fearful, disgust, surprised, neutral.

## Model Details

- **Feature Extraction**: MFCCs (typically 13 coefficients per frame)
- **Model Architecture**: LSTM-based RNN for sequential modeling of speech features
- **Classification Output**: Predicts one of several emotion classes per input sample

## Results

Sample results and accuracy metrics can be found in the `03_model_training.ipynb` notebook. You can visualize predictions and evaluate performance on test samples.

## Contributing

Pull requests and suggestions for improvements are welcome! Please open an issue for bug reports or feature requests.

## References

- [RAVDESS Dataset](https://zenodo.org/record/1188976)
- [MFCC Overview](https://en.wikipedia.org/wiki/Mel-frequency_cepstrum)
- [LSTM Networks](https://en.wikipedia.org/wiki/Long_short-term_memory)
