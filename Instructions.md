# Whisper WhatsApp Bot Skeleton

## 🚀 Project Overview

Welcome to the Whisper WhatsApp Bot Skeleton repository! This project is a simplified version of our Whisper WhatsApp Bot, which utilizes AI to transcribe voice messages and provide concise summaries or answer user questions. The purpose of this repository is to evaluate your skills in building and improving upon the existing code structure.

Feel free to extend the code, integrate additional features, or refactor the existing functions. We encourage you to showcase your creativity and technical abilities.

---

## 📋 Task Description

### 1. **Initialize and Set Up the Application (`main.py`)**

**Objective**: Complete the setup of the FastAPI application.

**Tasks**:
- Implement the `lifespan()` function:
  - Initialize the database connection (you can simulate this with a mock function if needed).
  - Set up a webhook URL using a placeholder URL manager.
- Define API routes by implementing `setup_routers(app)`.
- Ensure CORS settings are secure. Replace the wildcard (`*`) with specific origins if necessary.

### 2. **Extend and Refine Prompts (`prompts.py`)**

**Objective**: Customize the prompts used for AI model interactions.

**Tasks**:
- Review the provided `SUMMARY_PROMPT` and `QUESTION_PROMPT`.
- Modify or enhance these prompts to suit a real-world use case.
- Add at least one new prompt (e.g., a prompt for extracting key points or highlights from a text).

### 3. **Implement Question Answering Logic (`question.py`)**

**Objective**: Develop a function to generate answers based on user questions.

**Tasks**:
- Complete the `get_answer(context: str, question: str) -> str` function:
  - Use `QUESTION_PROMPT` to format the input for the AI model.
  - Integrate with an AI model of your choice (e.g., OpenAI API or a local language model).
  - Extract the response text and return it as the answer.
- Implement error handling and logging for robust operation.
- Add an optional feature: Allow users to specify a "confidence threshold" for the answers. If the model’s confidence is below this threshold, return a message indicating uncertainty.

### 4. **Build the Summarization Function (`summarize.py`)**

**Objective**: Implement a text summarization utility.

**Tasks**:
- Complete the `generate_summary(text: str) -> str` function:
  - Use `SUMMARY_PROMPT` to guide the summarization process.
  - Integrate with an AI model (e.g., OpenAI API, Hugging Face summarization models).
- Add a feature to allow users to specify the length of the summary (e.g., "short", "medium", "long").
- Implement basic error handling and logging for debugging purposes.

### 5. **Develop the Transcription Module (`transcribe.py`)**

**Objective**: Create a transcription pipeline for audio files.

**Tasks**:
- Complete the `transcribe_audio(file_path: str | Path, user)` function:
  - Load the audio file using `pydub.AudioSegment`.
  - Split the audio into segments of 25 minutes or less to handle long files.
  - Implement `process_audio_segment(segment)` to transcribe each segment using an AI model (e.g., Whisper).
- Add a feature to track user cancellation requests during the transcription process.
- Implement detailed logging for each segment processed and handle exceptions gracefully.

### 6. **Testing and Validation**

**Objective**: Ensure the correctness and robustness of your implementation.

**Tasks**:
- Write unit tests for the core functions in `question.py`, `summarize.py`, and `transcribe.py` using a testing framework (e.g., `pytest`).
- Create sample test cases for:
  - Question answering with varied context.
  - Summarization of short, medium, and long texts.
  - Transcription of small and large audio files.
- Optionally, set up a CI/CD pipeline using GitHub Actions to automate testing.

### 7. **Optional Bonus Tasks**

These tasks are optional but will be considered a plus if completed:

- **Refactor the Codebase**: Improve the structure and readability of the existing code. Split large functions into smaller, reusable functions.
- **Implement Caching**: Use caching (e.g., `functools.lru_cache`) to store responses for repeated queries or transcriptions.
- **Enhance Error Handling**: Add more comprehensive error handling and user-friendly error messages.
- **Optimize Performance**: Explore techniques to reduce API call latency or process audio files more efficiently.

---

## 🛠️ Setup Instructions

To get started with the project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd whisper-whatsapp-bot-skeleton
