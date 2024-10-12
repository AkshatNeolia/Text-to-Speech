
# Text to Speech

A simple Python project that converts text into speech using the **gTTS** (Google Text-to-Speech) module and plays the audio using the **os** module. The speech is saved as a `.wav` file.

## Features

- Converts input text to speech.
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

3. Install the required modules:

    ```bash
    pip install gtts
    pip install pydub
    ```

4. **Additional requirements:**
   - For audio conversion, you need to have [FFmpeg](https://ffmpeg.org/download.html) installed. You can install it using your system's package manager or from the website.

## Usage

1. Create a Python file and import the required modules:

    ```python
    from gtts import gTTS
    import os
    from pydub import AudioSegment
    ```

2. Define the text you want to convert:

    ```python
    text = "Hello, welcome to the text-to-speech project!"
    ```

3. Convert text to speech:

    ```python
    speech = gTTS(text=text, lang='en', slow=False)
    ```

4. Save the speech as an mp3 file, convert it to `.wav`, and play the audio:

    ```python
    speech.save("output.mp3")
    
    # Convert mp3 to wav
    sound = AudioSegment.from_mp3("output.mp3")
    sound.export("output.wav", format="wav")
    
    # Play the wav file
    os.system("start output.wav")  # For Windows users
    ```

> **Note:** Replace `start` with `open` for macOS, or `xdg-open` for Linux users.

## Requirements

- Python 3.x
- `gTTS` for text-to-speech conversion.
- `pydub` for audio format conversion.
- FFmpeg for handling audio file conversions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
