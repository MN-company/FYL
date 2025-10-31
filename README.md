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
| `tiny-distilled`    | 60–70 MB             |
| `base`              | 140–160 MB           |
| `base-distilled`    | 120–130 MB           |
| `small`             | 450–500 MB           |
| `small-distilled`   | 400–420 MB           |
| `medium`            | 1.4–1.6 GB           |
| `medium-distilled`  | 1.1–1.3 GB           |
| `large-v2`          | 2.8–3.0 GB           |
| `large-v3`          | 3.0–3.2 GB           |

> *Distilled models are smaller and faster, offering similar accuracy at 20–30% less disk usage — great for limited Drive storage.*

---

## 🔮 Future of the Project

- FYL is already in a **semi-final stage** — it started as a weekend project tailored to my own workflow  
- I plan to rewrite it using [**Insanely Fast Whisper**](https://github.com/Vaibhavs10/insanely-fast-whisper)  
  - Faster-Whisper is stable and precise but not fast enough for very large files  
  - Early tests with Insanely Fast Whisper showed **VRAM spikes** on long recordings  
  - For now, FYL sticks with **Faster-Whisper** and **safe Colab parameters** — slower, but reliable  
> Because not everyone has infinite Drive space, FYL will soon include:  
  - 🧹 an **auto-cleanup system** that removes old audio files automatically after successful transcription
  - 🎧 a **compression tool** that converts transcribed audio to smaller formats (e.g. `.opus` or `.flac` with reduced bitrate)  
> → so you can keep everything in one Drive folder without running out of space.

---

## ❤️ Credits & Spirit

Built on top of **[Faster-Whisper](https://github.com/SYSTRAN/faster-whisper)** and **[google-genai](https://pypi.org/project/google-genai/)**.  
Created with curiosity, caffeine, and a touch of rage against overpriced “AI” SaaS 
