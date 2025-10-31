<img width="2296" height="304" alt="logoFYL" src="https://github.com/user-attachments/assets/91389c46-fe5f-4eee-88e0-78e4da8562a4" />

**FYL** is a free, open-source script that combines **[Faster-Whisper](https://github.com/SYSTRAN/faster-whisper)** (for transcription) and **[Gemini](https://aistudio.google.com)** (for AI note generation).  
It automatically transcribes your lessons and produces clean, structured Markdown notes — all inside **Google Colab**.  

> This project is meant to be **completely free**.  
> No paywalls. No fake “free tiers.” No bullshit limitations.

---

## 🚀 How to Use

0. **Download** the `.ipynb` file and upload it to [Google Colab](https://colab.research.google.com)  
1. **Sign in** to Colab with your Google account  
2. **Sign in** with the same account on [Google AI Studio](https://aistudio.google.com)  
3. In the bottom-left corner, click **“Get API Key”** and generate a new one  
4. In Colab, open **Secret Manager → Gemini API Keys → Import from Google AI Studio**
5. Run the program to create and useful folder
6. Open your [Google Drive](https://drive.google.com) and upload the file in `asr_in` folder

That’s it.  
The notebook will automatically mount Google Drive, find your latest audio in `asr_in`, transcribe it with **Faster-Whisper**, and create clean Markdown notes in `asr_out` using **Gemini**.

---
## 🎙️ A Few Recommendations
1.	Accepted formats:
> Only .mp3, .flac, and .wav are supported — this is a limitation of the Whisper engine, not FYL.
2.	Use Audacity and export directly in a format that FYL can process
**Recommended Audacity settings:**
   - Format: MP3
   - Bitrate: 96 kbps
   - Sample rate: 44.1 kHz
   - Channels: Mono
---
## 💡 Why Gemini, Colab & GDrive

- **Gemini** — Google currently offers a promo for university students that includes Gemini Pro access  
- **AI Studio** — provides a free Gemini API key with generous usage  
- **Colab** — makes this tool usable by anyone; if you have a strong GPU, connect a local runtime for extra speed  
- **Google Drive** — avoids slow Colab uploads and keeps a persistent cache of the Whisper model  
  - You won’t have to re-download the model every time  
  - Recommended: keep at least **2–3 GB free** for the cache  
  - Tip: use a **dedicated Google account** for FYL (store only models + audio; 15 GB is plenty)

---

## 🧠 Model Cache Size (Drive)

| Model              | Cache Size (Approx.) |
|---------------------|----------------------|
| `tiny`              | 75–80 MB             |
| `base`              | 140–160 MB           |
| `small`             | 450–500 MB           |
| `medium`            | 1.4–1.6 GB           |
| `large-v2`          | 2.8–3.0 GB           |
| `large-v2-distilled`| 1.8 – 2.0 GB         |
| `large-v3`          | 3.0–3.2 GB           |
| `large-v3-distilled`| 2.0–2.2 GB           |

> *Distilled models are smaller and faster, offering similar accuracy at 20–30% less disk usage — great for limited Drive storage.*

---

## 🔮 Future of the Project
- I will write a collections of prompt so you don't have to. Rember that all prompt refer to the [official prompt guide](https://services.google.com/fh/files/misc/gemini-for-google-workspace-prompting-guide-101.pdf)
- [NotebookLM](https://notebooklm.google.com) is already free to use, and my tool is meant primarily for transcription. The AI integration exists only because I’m using it as a substitute for Notion AI — to automatically generate structured lesson notes. This means I won’t develop a UI for flashcards, memory tools, or similar features.
---

## ❤️ Credits & Spirit

Built on top of **[Faster-Whisper](https://github.com/SYSTRAN/faster-whisper)** and **[google-genai](https://pypi.org/project/google-genai/)**.  
Created with curiosity, caffeine, and a touch of rage against overpriced “AI” SaaS 
