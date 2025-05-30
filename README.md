# 🤖 AI Interviewer

**AI Interviewer** is an interactive, Streamlit-based web application that simulates various types of interview scenarios using speech recognition and large language models (via Groq API). It's designed to help job candidates prepare more effectively by providing personalized questions, evaluating spoken and typed answers, and offering constructive feedback.

---

## 🚀 Features

### 🏆 Complete Interview Suite
- Full-length interview simulation with **HR**, **Domain-based**, and **Resume-based** rounds.
- Tracks performance across rounds and visualizes scores.
- Provides structured feedback and model-generated ideal answers.

### 💼 HR-Based Interview
- Loads customizable HR questions from a CSV file.
- Converts questions to speech.
- Accepts voice responses and provides immediate feedback.

### 🧑‍💻 Domain-Based Interview
- Domain-specific questions based on selected expertise.
- CSV-based question loading with user-chosen domains.
- Score visualization via charts for self-assessment.

### 📄 Resume-Based Interview
- Analyzes uploaded resumes (PDF or DOCX).
- Extracts key information using NLP and regex.
- Generates 10+ tailored questions.
- Evaluates candidate responses with LLM assistance.

---

## 🛠️ Technologies Used

- **Streamlit** – Frontend UI and interaction
- **Groq (LLM API)** – Question evaluation and answer suggestions (LLaMA-3)
- **spaCy** – Resume and text analysis
- **speech_recognition** / **streamlit-mic-recorder** – Voice input
- **pyttsx3 / gTTS** – Text-to-speech for audio questions
- **matplotlib** – Score visualization
- **pdfminer / python-docx** – Resume text extraction

---

## 📁 Project Structure

```
.
├── main_app.py                 # Entry point with interview type selector
├── complete_interview.py       # Full interview suite (HR + Domain + Resume)
├── hr_interview.py             # HR-specific interview app
├── Interview.py                # Domain-specific interview app
├── resume_interviewer.py       # Resume-based interview app
├── hr_questions.csv            # (Expected) HR questions source file
├── interview_questions.csv     # (Expected) Domain questions source file
```

---

## ⚙️ Setup Instructions

1. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

2. **Add API Key**:  
   Replace `api_key="..."` in the Python files with your actual **Groq API key**.

3. **Run the App**:
   ```bash
   streamlit run main_app.py
   ```

4. **Add Question Files** (optional):
   - `hr_questions.csv` – List of HR questions (column: "Question")
   - `interview_questions.csv` – Columns: `Domain`, `Questions`

---

## 📌 Notes

- Requires a valid internet connection and microphone access for voice features.
- Text-to-speech uses `pyttsx3` or `gTTS`, depending on the module.
- Evaluation scoring depends on the reliability and output format of the LLM via Groq.

---

## 📄 License

MIT License. See `LICENSE` file for details.

---

## 👨‍💻 Author

Built with ❤️ by [Your Name or GitHub Username].
