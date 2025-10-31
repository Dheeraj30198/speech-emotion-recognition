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
speech-emotion-recognition.ipynb/           
└── README.md
```

## Google Colab

We can run all notebooks directly on [Google Colab](https://colab.research.google.com/):


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

3. **Download the RAVDESS dataset**

## Usage

Run the colab in order:

1. **Data Setup**: Download and organize the raw RAVDESS audio files.
2. **Feature Extraction**: Extract MFCC features and save them to the `data/` directory.
3. **Model Training**: Train an LSTM-based RNN using the extracted features.
4. **Inference**: Test the trained model on new or unseen samples.

## Dataset

- **RAVDESS**: [Ryerson Audio-Visual Database of Emotional Speech and Song](https://drive.google.com/drive/folders/1yRDew-zQrF6b8uE8Q4WrtMPcwt1ACdz8?usp=drive_link)
  - Contains 24 professional actors vocalizing two statements with various emotional intonations.
  - Emotions include: calm, happy, sad, angry, fearful, disgust, surprised, neutral.

## Model Details

- **Feature Extraction**: MFCCs (typically 13 coefficients per frame)
- **Model Architecture**: LSTM-based RNN for sequential modeling of speech features
- **Classification Output**: Predicts one of several emotion classes per input sample

## Results

Sample results and accuracy metrics can be found in the  notebook. You can visualize predictions and evaluate performance on test samples.

## Contributing

Pull requests and suggestions for improvements are welcome! Please open an issue for bug reports or feature requests.

## References

- [RAVDESS Dataset](https://zenodo.org/record/1188976)
- [MFCC Overview](https://en.wikipedia.org/wiki/Mel-frequency_cepstrum)
- [LSTM Networks](https://en.wikipedia.org/wiki/Long_short-term_memory)

## Future Work

As the next step in this project, we aim to develop a **web-based interface** that enables users to provide **live voice input** for real-time emotion detection. This extension will allow the model to process streaming audio, extract MFCC features on-the-fly, and classify emotional states using the trained RNN.

###  Live Emotion Detection via Web Interface

- Users can speak directly into the browser using a microphone.
- The system will capture audio, extract MFCC features in real time, and classify emotions using the LSTM model.
- Visual feedback will be provided instantly, showing the detected emotion and confidence score.

###  Integration with Voice-Enabled AI Tools

This feature has broader implications for enhancing user experience in voice-based AI systems such as:

- **ChatGPT**, **Copilot**, **Perplexity**, and other conversational agents
- By understanding not just the **content** of speech but also the **emotional tone**, AI can respond more empathetically and contextually
- This opens doors to more **emotion-aware interactions**, improving accessibility, mental health support, and human-computer engagement

### Potential Applications

- Emotion-aware virtual assistants
- Real-time feedback in customer service bots
- Sentiment tracking in voice surveys and interviews
- Adaptive learning platforms that respond to student frustration or enthusiasm
