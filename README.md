# Emotion_detection_LLM
 Speech-to-Emotion Logger using BERT & Google Speech Recognition

This project captures spoken audio, transcribes it into text, detects the underlying emotion using a BERT-based model (`go-emotions`), and logs everything—along with a timestamp—into a Microsoft Word document.

---

## 🚀 Features

- 🎤 Real-time speech-to-text using Google Speech Recognition
- 🤖 Emotion detection using `bhadresh-savani/bert-base-go-emotion` (fine-tuned BERT)
- 📄 Logs each transcript and emotion into a `.docx` file
- 🕒 Automatically timestamps each entry
- 🛑 Allows easy termination after each recording

---

## 📦 Requirements

Install the following Python packages:

```bash
pip install speechrecognition python-docx transformers torch
Also ensure you have:

PyAudio installed for microphone access (pip install pyaudio or via unofficial wheels)

A working microphone

🧠 Model Used
Model: bhadresh-savani/bert-base-go-emotion

Task: Multi-class emotion classification (joy, anger, sadness, love, etc.)

🧪 How It Works
The script starts listening for a paragraph when the user is ready.

Once the user finishes speaking, they press ENTER.

Google’s speech recognition transcribes the spoken audio into text.

BERT analyzes the paragraph and detects the dominant emotion.

Everything is logged with a timestamp into a .docx file.

📄 Output Sample
Each entry in the Word document looks like this:

yaml
Copy
Edit
Timestamp: 2025-07-10 12:34:56  
🗣 Full Paragraph: I feel excited today because I started a new project!  
Detected Emotion: joy
🖥️ Running the Script
python
Copy
Edit
python speech_emotion_logger.py
You’ll see:

css
Copy
Edit
🎙 Please speak a full paragraph now. Recording until you press ENTER...
🎧 Listening now... speak your full paragraph.
Speak clearly, then press ENTER when done. The detected emotion and full text will be shown and saved.

📍 File Location
The transcript and emotion log is saved at:

makefile
Copy
Edit
C:\Users\Dell\OneDrive\Desktop\ergolab\ergo refined project\speech2.docx
Change doc_path in the script to update the location.

🔐 Notes
Internet connection is required for Google’s speech recognition API.

Accuracy depends on microphone quality and ambient noise.

Emotions are single-label predictions for simplicity.

📌 To-Do / Improvements
Allow multi-emotion detection with probabilities

Add GUI with Tkinter or Streamlit

Export to CSV or JSON alongside .docx

Batch mode for processing multiple speeches

📜 License
This project is for educational purposes.
Model credit: Bhadresh Savani

🙌 Acknowledgements
SpeechRecognition

Transformers by Hugging Face

GoEmotions Dataset (Google)
