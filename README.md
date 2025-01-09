# Emogen-Real-time-emoji-generation-using-facial-expression

This project implements an emotion detection system using deep learning. The system detects emotions from a person's face in real-time using a webcam and overlays an emoji corresponding to the detected emotion.

Features:
Detects 7 different emotions: angry, disgust, fear, happy, neutral, sad, surprise.
Real-time emotion detection via webcam using a pre-trained Convolutional Neural Network (CNN).
Displays corresponding emojis for each detected emotion.
Provides an option to save a screenshot with the detected emotion and corresponding emoji when the "C" key is pressed.
A GUI with an "Exit" button to terminate the application.
Project Structure:
python
Copy code
├── haarcascade_frontalface_default.xml  # Pre-trained face detection model
├── emojis/                            # Folder containing emoji images for each emotion
│   ├── angry.jpg
│   ├── disgust.jpg
│   ├── fear.jpg
│   ├── happy.jpg
│   ├── neutral.jpg
│   ├── sad.jpg
│   └── surprise.jpg
├── fer2013.zip                         # The dataset containing facial emotion images
├── emotion_model.h5                   # Pre-trained emotion detection model
├── emotion_detector.py                 # Main script for running the detection
└── README.md                           # Project documentation
Installation:
Clone this repository:

bash
Copy code
git clone https://github.com/your-username/emogen.git
cd emogen
Install the necessary dependencies using pip:

bash
Copy code
pip install -r requirements.txt
Ensure you have the following files in place:

haarcascade_frontalface_default.xml for face detection.
A folder called emojis with emoji images named after the emotions.
The dataset fer2013.zip (you can extract the dataset as shown in the code).
Run the script:

bash
Copy code
python emotion_detector.py
How It Works:
Emotion Model:

The system uses a deep learning model trained on the FER2013 dataset, which classifies images into 7 different emotions.
The model architecture is a CNN with Conv2D layers, MaxPooling2D, Dense layers, and Batch Normalization.
Face Detection:

The system uses OpenCV's pre-trained face detection model (haarcascade_frontalface_default.xml) to detect faces in real-time.
Emotion Prediction:

Once a face is detected, the model predicts the emotion based on the grayscale image of the face.
Emoji Display:

After predicting the emotion, the system overlays a corresponding emoji image (from the emojis/ folder) onto the webcam feed.
Save Screenshot:

Press the "C" key to capture and save the screenshot with the detected face and emotion overlayed.
Exit Application:

Press the "Exit" button in the GUI or press "Q" to quit the application.
Notes:
Make sure to place the emoji images in the emojis/ directory with the following names: angry.jpg, disgust.jpg, fear.jpg, happy.jpg, neutral.jpg, sad.jpg, surprise.jpg.
The face detection may not work properly if the face is too small or the camera quality is low.
The model and system may take some time to initialize, depending on your hardware.
Requirements:
Python 3.x
OpenCV
TensorFlow
Keras
NumPy
Matplotlib
Seaborn
License:
This project is licensed under the MIT License - see the LICENSE file for details.
