# Video Transcription Tool

A Python script that leverages OpenAI's Whisper model to automatically transcribe videos to text.

## Overview

This tool processes video files from a specified folder, generates text transcriptions, and saves them as individual text files. It uses Whisper, a state-of-the-art speech recognition model, and can utilize GPU acceleration when available.

## Features

- Automatic speech recognition for video files
- Support for multiple video formats (.mp4, .mkv, .avi, .mov)
- GPU acceleration with CUDA (when available)
- Organized output with one text file per video
- Configurable model size for different accuracy/speed tradeoffs

## Requirements

- Python 3.7+
- PyTorch
- OpenAI Whisper
- CUDA-compatible GPU (optional, for faster processing)

## Installation

1. Install the required packages:

```bash
pip install torch openai-whisper
```

2. For GPU support, ensure you have the appropriate CUDA drivers installed.

## Usage

1. Update the `folder_path` variable to point to your directory of videos:

```python
folder_path = '/path/to/your/videos/'
```

2. Choose your desired Whisper model size by modifying:

```python
model = whisper.load_model("medium", device=device)  # Options: "tiny", "base", "small", "medium", "large"
```

Larger models provide better accuracy but require more computational resources.

3. Run the script:

```bash
python transcribe_videos.py
```

## Output

For each video file processed, a corresponding text file will be created in the same directory with the same name but a `.txt` extension. The transcript is formatted with each speech segment on a new line.

## Performance Notes

- Processing time depends on video length, model size, and hardware
- GPU acceleration significantly improves performance
- The "medium" model offers a good balance between accuracy and speed

## Customization

You can modify the script to:
- Change the target language (default is English)
- Adjust the transcription task type
- Change the output format
- Process different video file extensions

## License

[Include your license information here]

---

