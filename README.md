# Whisper WhatsApp Bot Skeleton

## 🚀 Project Overview

Welcome to the Whisper WhatsApp Bot Skeleton repository! This project is a simplified version of our Whisper WhatsApp Bot, which utilizes AI to transcribe voice messages and provide concise summaries or answer user questions. The purpose of this repository is to evaluate your skills in building and improving upon the existing code structure.

Feel free to expand the code, integrate additional features, or refactor the existing functions. We encourage you to showcase your creativity and technical abilities.

## 📝 Task Description

Your task is to complete the following modules by implementing the placeholder functions provided:

1. **main.py**:
   - Initialize the FastAPI application.
   - Set up the database and webhook configuration.
   - Define the routes and middleware.

2. **prompts.py**:
   - Extend the predefined prompts if necessary.
   - You can modify or add new prompts based on the application's needs.

3. **question.py**:
   - Implement the `get_answer()` function to generate answers based on user questions and context.
   - Integrate with an AI model of your choice (e.g., OpenAI API).

4. **summarize.py**:
   - Complete the `generate_summary()` function to produce concise summaries of input text.
   - Use a text summarization model or integrate with an AI API.

5. **transcribe.py**:
   - Implement the `transcribe_audio()` and `process_audio_segment()` functions.
   - Handle audio file loading, segment splitting, and transcription using an AI model (e.g., Whisper).

## 🛠️ Setup Instructions

To get started with the project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd whisper-whatsapp-bot-skeleton

Install Dependencies:
Make sure you have Python 3.8+ installed. Then, run: pip install -r requirements.txt

Run the Application:
Start the FastAPI server with: uvicorn main:app --reload
