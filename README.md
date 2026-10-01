# PyQt5 Media Player 🎬

A simple desktop media player built with **Python and PyQt5**.

The application provides a graphical interface for opening and playing video files, with basic playback controls and a seek slider.

## Overview

This project was created to practice building a desktop GUI application using Python and PyQt5.

It uses PyQt5's multimedia functionality to load local video files and provides a simple interface for controlling playback.

## Features

* 🎬 Open local video files
* ▶️ Play and pause videos
* ⏸️ Toggle playback using a single control button
* 🔎 Seek through the video using a timeline slider
* 📺 Video playback through `QVideoWidget`
* 🖥️ Desktop graphical user interface
* ⚠️ Basic media error handling
* 🎨 Simple dark/black player interface

## Technology Stack

| Technology   | Purpose                     |
| ------------ | --------------------------- |
| Python       | Application logic           |
| PyQt5        | GUI framework               |
| QMediaPlayer | Media playback              |
| QVideoWidget | Video rendering             |
| QFileDialog  | Selecting local video files |
| QSlider      | Video position / seeking    |
| Git          | Version control             |

## Application Architecture

The application is built around the PyQt5 event-driven architecture.

```text
┌──────────────────────────┐
│        PyQt5 GUI         │
│                          │
│  Open Video              │
│  Play / Pause            │
│  Seek Slider             │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│      QMediaPlayer        │
│                          │
│  Load Media              │
│  Play / Pause            │
│  Track Position          │
│  Track Duration          │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│      QVideoWidget        │
│                          │
│     Video Playback       │
└──────────────────────────┘
```

## How It Works

### 1. Open a Video

The **Open Video** button opens a file-selection dialog using `QFileDialog`.

The selected local file is passed to `QMediaPlayer` using a `QMediaContent` object.

### 2. Play / Pause

The play button checks the current state of `QMediaPlayer`.

If the video is currently playing, it pauses the video. Otherwise, playback starts.

The button icon also changes between the standard **Play** and **Pause** icons.

### 3. Seek Through the Video

The horizontal slider represents the current playback position.

The application listens for:

* `positionChanged` — updates the slider as the video plays.
* `durationChanged` — sets the slider range according to the video's duration.
* `sliderMoved` — changes the playback position when the user moves the slider.

## Project Structure

```text
mediaPlayer/
│
├── mediaPlayer.py
│   └── Main PyQt5 media player application
│
├── .gitignore
│   └── Git ignore configuration
│
└── README.md
    └── Project documentation
```

## Requirements

* Python 3.x
* PyQt5

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/shubham-ch/mediaPlayer.git
cd mediaPlayer
```

### 2. Install PyQt5

Install the required Python package using pip:

```bash
pip install PyQt5
```

## Running the Application

Run the main Python file:

```bash
python mediaPlayer.py
```

The PyQt5 media player window will open.

Click **Open Video** to select a local video file.

## Basic Usage

```text
1. Start the application
        ↓
2. Click "Open Video"
        ↓
3. Select a local video file
        ↓
4. Click Play
        ↓
5. Use the slider to seek
        ↓
6. Click Play/Pause to control playback
```

## Concepts Practiced

This project provided practical experience with:

* Python GUI development
* PyQt5 widgets and layouts
* Event-driven programming
* Signals and slots
* Object-oriented programming
* File selection dialogs
* Media playback
* Video position tracking
* GUI state management
* Working with third-party Python libraries

## Future Improvements

Possible extensions to the project include:

* Audio file support
* Volume control
* Full-screen playback
* Stop button
* Playlist support
* Previous/next media controls
* Playback speed control
* Display of current time and total duration
* Improved error messages
* Custom application styling

## Author

**Shubham**

GitHub:
https://github.com/shubham-ch

## License

This project is intended for educational and personal use.
