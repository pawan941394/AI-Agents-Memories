# Memories Chat Bot

A simple, persistent chat application powered by Google's Gemini AI that remembers your conversation history across sessions.

## Overview

This project uses the [Agno](https://github.com/agno-ai/agno) framework to create a chat interface with Google's Gemini AI model. The key feature of this application is that it maintains conversation history in a SQLite database, allowing the AI to "remember" previous interactions even after restarting the application.

## Features

- Interactive command-line chat interface
- Persistent memory using SQLite database storage
- Powered by Google Gemini 2.0 Flash AI model
- Maintains context over multiple conversations
- Easy to set up and run

## Prerequisites

- Python 3.7+
- Google Gemini API key

## Installation

1. Clone this repository
   ```
   git clone https://github.com/yourusername/memories-chatbot.git
   cd memories-chatbot
   ```

2. Install required dependencies
   ```
   pip install -r requirements.txt
   ```

3. Replace the API key in `memories.py` with your own Google Gemini API key
   ```python
   model=Gemini(id="gemini-2.0-flash-exp", api_key='YOUR_API_KEY_HERE')
   ```

## Usage

Run the application with:
```
python memories.py
```

Chat with the AI by typing your messages after the "You: " prompt.

To exit the conversation, type any of the following: "exit", "quit", or "q".

## How it Works

The application:

1. Initializes an AI agent using Google's Gemini model
2. Sets up SQLite storage for maintaining conversation history
3. Presents a simple chat interface
4. Loads previous conversation context for each new interaction
5. Saves each interaction to maintain continuity across sessions

## Project Structure

```
.
├── memories.py        # Main application file
├── requirements.txt   # Python dependencies
└── tmp/
    └── data.db        # SQLite database storing conversation history
```

## Customization

You can adjust the following parameters in `memories.py`:

- `num_history_runs`: Change how many past conversation turns are included for context
- `session_id`: Modify to create different conversation threads
- Model settings: Switch to different Gemini models as needed

## License

[Add your preferred license here]

## Acknowledgments

- [Agno AI](https://github.com/agno-ai/agno) for the framework
- Google for the Gemini AI model

---

Created by [Your Name]
