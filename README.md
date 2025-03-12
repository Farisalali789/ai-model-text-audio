# ai-model-text-audio

This repository contains a Google Colab notebook that demonstrates how to use the **Mistral-Nemo-Instruct-2407** language model for text generation and **Microsoft's SpeechT5** for text-to-speech synthesis. The code is designed to run in Google Colab and leverages GPU acceleration for optimal performance.

## Features
- **Text Generation**: Uses the `llama-cpp-python` library with CUDA support to load and run the Mistral-Nemo-Instruct-2407 model.
- **Text-to-Speech**: Converts generated text into speech using Hugging Face's `transformers` library and Microsoft's SpeechT5 model.
- **Interactive Audio Playback**: Displays the generated audio directly in the notebook.

## System Requirements
- **Google Colab**: This notebook is designed to run in Google Colab with GPU support.
- **GPU**: A GPU is required for efficient inference with the Mistral model and SpeechT5.
- **Disk Space**: Approximately **8.5 GB** of disk space is required for the model files and dependencies.
  - The Mistral model (`Mistral-Nemo-Instruct-2407-Q5_K_M.gguf`) alone is **8.13 GB**.

## Installation and Setup
  - Open the notebook in **Google Colab**:
  - Ensure that the runtime type is set to **GPU**:
     - Go to `Runtime` --> `Change runtime type` --> Select `GPU` under Hardware accelerator.

## Code Overview
### Cell 1: Setup and Installation
- Installs CUDA toolkit and GPU-enabled `llama-cpp-python`.
- Downloads the **Mistral-Nemo-Instruct-2407-Q5_K_M.gguf** model (8.13 GB) from Hugging Face.
- Installs Hugging Face `transformers`, `datasets`, and `diffusers` libraries.
- **IMORTANT**: This cell should not be ran more than once per session as to not use too much RAM and cause a crash.

### Cell 2: Text Generation and Speech Synthesis
- Loads the Mistral model and generates text based on a prompt.
- Uses Microsoft's SpeechT5 to convert the generated text into speech.
- Saves the speech as a `.wav` file and plays it interactively in the notebook.
