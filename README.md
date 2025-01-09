# Emogen: Real-time emoji generation using facial expressions

This project implements a real-time emotion detection system using deep learning. It can detect emotions from facial expressions and display corresponding emojis.

## Features

* Detects 7 different emotions in real-time:
    * Angry
    * Disgust
    * Fear
    * Happy
    * Neutral
    * Sad
    * Surprise
* Real-time emotion detection via webcam using a pre-trained CNN
* Displays corresponding emojis for each detected emotion
* Screenshot capture functionality with 'C' key
* Simple GUI with exit controls

2.0 Flash Experimental. Might not work as expected.
You are absolutely right. My apologies! The issue is with how GitHub renders lists inside code blocks. Here are two better ways to represent the project structure in your README:

Option 1: Using a Tree Diagram (Recommended)

This is the clearest way to represent a file structure in a README. You can use backticks for inline code or code blocks for larger sections.

## Project Structure

2.0 Flash Experimental. Might not work as expected.
Here's another way to represent the project structure in your README.md file that avoids relying on indentation within a code block:

Option 1: Using a Table

This approach presents the information in a clear and organized table format.

## Project Structure

| File/Directory | Description |
|---|---|
| `haarcascade_frontalface_default.xml` | Pre-trained face detection model |
| `emojis/` | Folder containing emotion-specific emoji images |
| | angry.jpg | Emoji image for anger |
| | disgust.jpg | Emoji image for disgust |
| | fear.jpg | Emoji image for fear |
| | happy.jpg | Emoji image for happiness |
| | neutral.jpg | Emoji image for neutral expression |
| | sad.jpg | Emoji image for sadness |
| | surprise.jpg | Emoji image for surprise |
| `fer2013.zip` | Facial emotion dataset |
| `emotion_model.h5` | Pre-trained emotion detection model |
| `emotion_detector.py` | Main application script |
| `README.md` | Project documentation |


This option uses a description list with dedicated terms and explanations:

Project Structure
haarcascade_frontalface_default.xml: Pre-trained face detection model
emojis/: Folder containing emotion-specific emoji images
angry.jpg: Emoji image for anger
disgust.jpg: Emoji image for disgust
fear.jpg: Emoji image for fear
happy.jpg: Emoji image for happiness
neutral.jpg: Emoji image for neutral expression
sad.jpg: Emoji image for sadness
surprise.jpg: Emoji image for surprise
fer2013.zip: Facial emotion dataset
emotion_model.h5: Pre-trained emotion detection model
emotion_detector.py: Main application script
README.md: Project documentation


## Installation

1. Clone the repository:

git clone https://github.com/Omadithya07/Emogen-Real-time-emoji-generation-using-facial-expression.git
cd Emogen-Real-time-emoji-generation-using-facial-expression


2. Install dependencies:

bash
pip install -r requirements.txt


3. Verify required files:

* `haarcascade_frontalface_default.xml` for face detection
* `emojis/` folder containing emotion-specific emoji images
* `fer2013.zip` dataset
* `emotion_model.h5` pre-trained model

4. Run the application:

python emogen.py


## How It Works

**Emotion Model**

The system employs a Convolutional Neural Network (CNN) trained on the FER2013 dataset. The model architecture includes:

* Multiple Conv2D layers
* MaxPooling2D layers
* Dense layers
* Batch Normalization
* Output layer with 7 emotion classes

**Face Detection**

OpenCV's pre-trained Haar Cascade classifier is used for real-time face detection in the video feed.

**Emotion Detection Pipeline**

1. Capture video frame from webcam
2. Detect faces using Haar Cascade classifier
3. Preprocess detected face region
4. Pass processed image through CNN model
5. Get emotion prediction
6. Overlay corresponding emoji
7. Display result in real-time

## Controls

* Press 'C' to capture and save screenshot
* Press 'Q' or click 'Exit' button to quit application

## Requirements

* Python 3.x
* OpenCV
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Seaborn

## Important Notes

* Emoji images must be placed in the `emojis/` directory with correct naming:
    * `angry.jpg`
    * `disgust.jpg`
    * `fear.jpg`
    * `happy.jpg`
    * `neutral.jpg`
    * `sad.jpg`
    * `surprise.jpg`
* Face detection performance depends on:
    * Face size in frame
    * Camera quality
    * Lighting conditions
* System initialization time varies based on hardware specifications.

## Troubleshooting

If you encounter issues:

* Ensure all dependencies are correctly installed
* Verify all required files are present and correctly named
* Check camera permissions are granted
* Ensure sufficient lighting for face detection

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
