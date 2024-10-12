
# Text to Speech

A simple Python project that converts text from a file into speech using the **gTTS** (Google Text-to-Speech) module and plays the audio using the **os** module. The speech is saved as a `.wav` file.

## Features

- Reads input text from a file (`1.txt`).
- Converts the text to speech.
- Saves the speech as a `.wav` file.
- Automatically plays the `.wav` file.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/text-to-speech.git
    ```

2. Navigate to the project directory:

    ```bash
    cd text-to-speech
    ```

3. Install the required module:

    ```bash
    pip install gtts
    ```

4. **Additional requirements:**
   - For audio playback, you may need to adjust the `os.system` command based on your operating system.

## Usage

1. Create a file named `1.txt` and add the text you want to convert to speech.

2. Use the following Python code:

    ```python
    from gtts import gTTS
    import os

    # Open the text file and read the contents
    f = open('1.txt')
    x = f.read()

    # Set the language
    language = 'en'

    # Convert text to speech
    audio = gTTS(text=x, lang=language, slow=False)

    # Save the speech as a .wav file
    audio.save("1.wav")

    # Play the .wav file
    os.system("1.wav")  # For Windows users, adjust for other OS if necessary
    ```

3. Run the script, and it will convert the text in `1.txt` to speech, save it as `1.wav`, and play the audio file.

## Requirements

- Python 3.x
- `gTTS` for text-to-speech conversion.
