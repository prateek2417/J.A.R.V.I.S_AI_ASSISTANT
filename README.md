🤖 Jarvis - AI Virtual Assistant

Jarvis is a Python-based virtual assistant capable of performing automated tasks and engaging in natural conversation. It uses Google's Gemini 2.5 Pro model for intelligent responses and standard web libraries for browsing and media control.

🚀 Features

🎙️ Voice Activation: Listens for the wake word "Jarvis" to start processing commands.

🧠 Intelligent Chat: Uses Google Gemini API to answer general questions and chat like a human.

📰 Live News: Fetches the latest business headlines using NewsAPI.

🎵 Music Player: Plays songs from your local library or links.

🌐 Web Browsing: Opens websites like Google, YouTube, Facebook, and LinkedIn via voice command.

🗣️ Text-to-Speech: Responds audibly using pyttsx3.

🛠️ Tech Stack

Core: Python

AI Model: Google Gemini (gemini-2.5-pro)

Voice Recognition: SpeechRecognition (Google Speech API)

Text-to-Speech: pyttsx3

HTTP Requests: requests

📂 Project Structure

├── main.py                # The main script containing the Jarvis logic
├── musicLibrary.py        # (Required) Dictionary mapping song names to URLs
├── requirements.txt       # List of dependencies
└── README.md              # Documentation


⚙️ Installation & Setup

1. Clone the Repository

git clone [https://github.com/](https://github.com/)[your-username]/jarvis-assistant.git
cd jarvis-assistant


2. Install Dependencies

You will need to install the required Python libraries. You may also need PyAudio, which can be tricky to install on some systems (like Windows).

pip install google-generativeai speechrecognition pyttsx3 requests gtts pygame pocketsphinx


Note: If pip install pyaudio fails on Windows, try downloading the .whl file for your version of Python from here.

3. API Key Configuration

You need to replace the placeholder keys in main.py with your actual API keys:

Google Gemini API: Get it from Google AI Studio.

Update genai.configure(api_key="YOUR_GEMINI_KEY")

NewsAPI: Get it from NewsAPI.org.

Update the newsapi variable with your key.

4. Create Music Library

Create a file named musicLibrary.py in the same directory. It should contain a dictionary called music:

# musicLibrary.py
music = {
    "skyfall": "[https://www.youtube.com/watch?v=DeumyOzKqgI](https://www.youtube.com/watch?v=DeumyOzKqgI)",
    "faded": "[https://www.youtube.com/watch?v=60ItHLz5WEA](https://www.youtube.com/watch?v=60ItHLz5WEA)",
    "wolf": "[https://www.youtube.com/watch?v=ThCH0U6aJpU](https://www.youtube.com/watch?v=ThCH0U6aJpU)"
}


🏃‍♂️ How to Run

Make sure your microphone is connected.

Run the script:

python main.py


Wait for Initialization: The assistant will say "Initializing Jarvis...".

Wake Word: Say "Jarvis".

Command: Once it responds "Yes Sir", give your command (e.g., "Play Skyfall", "Open Google", "Tell me about Black Holes").

🗣️ Voice Commands

Command

Action

"Jarvis"

Wakes up the assistant.

"Open Google / Youtube..."

Opens the respective website in your browser.

"Play [song name]"

Plays the song defined in musicLibrary.py.

"News"

Reads the top business headlines.

"[Any other question]"

Sends the query to Google Gemini AI for a smart response.

🔮 Future Improvements

Add a GUI using Tkinter or PyQt.

Implement "Stop" or "Sleep" commands.

Integrate Spotify API for better music control.

Secure API keys using .env files.
