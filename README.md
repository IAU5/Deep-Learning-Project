# Deep-Learning-Project
# AI Card Detection Assistant

This project implements a real-time desktop application that assists visually impaired individuals in identifying playing cards using object detection and audio feedback.

## Project Overview

The system uses a webcam to capture video input and a YOLOv8 object detection model to identify playing cards in real time. Detected card labels are mapped to human-readable names and then vocalized using an offline text-to-speech engine. The application features a graphical interface designed for accessibility, with options for light and dark mode themes.

## Features

- Real-time detection of all 52 standard playing cards
- Offline voice feedback (no internet required)
- Lightweight and fast inference with YOLOv8n
- User-friendly GUI with accessible controls
- Packaged as a standalone Windows `.exe` file

## Technologies Used

| Component           | Technology                            |
|---------------------|----------------------------------------|
| Object Detection    | YOLOv8n (Ultralytics)                  |
| Language            | Python 3.11                            |
| Webcam Integration  | OpenCV                                 |
| Voice Feedback      | pyttsx3 (offline TTS engine)           |
| Graphical Interface | Tkinter                                |
| Packaging           | PyInstaller                            |

## System Workflow

1. Webcam captures live video.
2. YOLOv8n detects and classifies playing cards.
3. Detected class ID is mapped to a readable label.
4. Text-to-speech engine vocalizes the card name.
5. GUI displays the video feed and detection results.

## Installation

### Requirements

- Python 3.10 or newer (for source version)
- Windows OS (for `.exe` executable)
- Functional webcam

### Run from Source

```bash
python gui_card_detector.py
```

Make sure the `best.pt` model file is in the project directory.

Or just Run the .exe file included in the source.

### Run the Windows Executable

Download and run `AI_Card_Assistant.exe`. No installation required.

## Model Evaluation

| Metric       | Value     |
|--------------|-----------|
| mAP@50       | 98.3%     |
| mAP@50-95    | 90.4%     |
| Precision    | 99.8%     |
| Recall       | 99.8%     |
| Inference    | ~30 ms per frame (CPU)

## Use Case

The goal of this project is to make recreational card games more accessible to individuals who are blind or visually impaired. By combining deep learning and speech synthesis, it provides a practical and inclusive solution without requiring specialized hardware.

## Future Improvements

- Voice command input support
- Android/iOS deployment via TFLite
- Multilingual voice synthesis
- Integration with game-tracking systems

## License

This project is open-source and released under the MIT License.
