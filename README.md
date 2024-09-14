# Audio to Summarized Transcript Project

## Overview

This project demonstrates a pipeline for converting audio files into text transcripts and then summarizing the text using advanced Hugging Face models. It integrates audio transcription and text summarization, featuring a user-friendly interface built with Gradio.

## Files

- **`pipeline_notebook.ipynb`**: Demonstrates the use of Hugging Face models for audio-to-text transcription and text summarization with code example and explanation.
- **`gradio_notebook.ipynb`**: Illustrates various Gradio components and their functionalities, showcasing how to build interactive web interfaces.
- **`full_implementation_notebook.ipynb`**: Combines audio transcription and text summarization with Gradio, providing a complete interactive application with code that integrates all components.
- **`results.csv`**: Contains output data from the full implementation notebook, including transcripts and summaries.
- **`video_demo.mp4`**: A walkthrough video of the full implementation notebook, demonstrating how to use the interactive features.

## Code Overview

- **`pipeline_notebook.ipynb`**: This notebook shows how to use the Whisper model for converting audio to text and the PEGASUS model for summarizing the text. It includes functions to process audio and summarize text, with example code snippets.

- **`gradio_notebook.ipynb`**: Features a demonstration of Gradio components such as `Textbox`, `Slider`, and `Audio`. The code examples illustrate how to build and customize Gradio interfaces for different types of user inputs and outputs.

- **`full_implementation_notebook.ipynb`**: Integrates the transcription and summarization functionality into a Gradio interface. The notebook contains code that allows users to upload audio files, adjust summary length settings, and view both the transcript and summary. It showcases how to combine multiple models and Gradio components into a cohesive application.

## Models Used

- **Whisper (OpenAI)**: A cutting-edge model for automatic speech recognition (ASR). The `base` variant is used to transcribe audio files into text, providing robust performance across various languages and accents.

- **PEGASUS (Hugging Face)**: A model specialized in text summarization, specifically the `google/pegasus-large` variant. It generates concise and coherent summaries from longer texts, ideal for summarizing transcribed content.

  Learn more about the PEGASUS model [here](https://huggingface.co/docs/transformers/main/model_doc/pegasus#pegasus).

## How the Hugging Face Text-to-Text Pipeline Works

1. **Text-to-Text Pipeline Overview**:
   - The text-to-text pipeline from Hugging Face allows you to perform various text processing tasks such as summarization, translation, and more. It typically involves models that take text as input and produce text as output.

2. **Integration in This Project**:
   - **Audio Transcription**: The Whisper model converts audio files into text. This is the first step where spoken content is transcribed into written form.
   - **Text Summarization**: Once the audio is transcribed into text, the PEGASUS model summarizes the text. The summarization model takes the transcribed text and generates a concise summary while retaining the key information.

3. **Pipeline Execution**:
   - **Transcription**: The `whisper_model.transcribe(audio_file)` function processes the audio file and extracts the text.
   - **Summarization**: The `summarization(text, min_length=min_length, max_length=max_length)` function takes the transcribed text and produces a summary within the specified length range.

By using these models, the project efficiently converts spoken content into a summarized written format, making information more accessible and digestible.


## Instructions

1. Open **`full_implementation_notebook.ipynb`** to run the complete pipeline.
2. Use the Gradio interface within the notebook to upload audio files and receive summarized transcripts.

## Expected Output from the Gradio Interface

When interacting with the Gradio interface:

- **Audio Upload**: You will see an audio upload field where you can select and upload an audio file.
- **Sliders**: There will be two sliders allowing you to adjust the minimum and maximum length for the summary.
- **Transcript**: Once the audio file is processed, a textbox will display the transcribed text from the audio.
- **Summary**: Another textbox will show the summary of the transcribed text, which respects the length constraints set by the sliders.

The interface will provide clear and concise feedback based on the uploaded audio and chosen summary parameters.


## Hugging Face Project

Explore the deployed Hugging Face project [here](https://huggingface.co/spaces/RanAlh443/Audio_Transcription_and_Summarization).

## Video Walkthrough

Watch the video demonstration [here](link-to-your-video).
