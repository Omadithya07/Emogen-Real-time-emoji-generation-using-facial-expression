# Emogen-Real-time-emoji-generation-using-facial-expression

Real-time emotion detection system using deep learning to detect emotions from facial expressions and display corresponding emojis.
Features

Detects 7 different emotions in real-time:

Angry
Disgust
Fear
Happy
Neutral
Sad
Surprise


Real-time emotion detection via webcam using a pre-trained CNN
Displays corresponding emojis for each detected emotion
Screenshot capture functionality with 'C' key
Simple GUI with exit controls

Project Structure
Copy├── haarcascade_frontalface_default.xml    # Pre-trained face detection model
├── emojis/                                # Folder containing emoji images
│   ├── angry.jpg
│   ├── disgust.jpg
│   ├── fear.jpg
│   ├── happy.jpg
│   ├── neutral.jpg
│   ├── sad.jpg
│   └── surprise.jpg
├── fer2013.zip                           # Facial emotion dataset
├── emotion_model.h5                      # Pre-trained emotion detection model
├── emotion_detector.py                   # Main application script
└── README.md                            # Project documentation
Installation

Clone the repository:
bashCopygit clone https://github.com/your-username/emogen.git
cd emogen

Install dependencies:
bashCopypip install -r requirements.txt

Verify required files:

haarcascade_frontalface_default.xml for face detection
emojis folder containing emotion-specific emoji images
fer2013.zip dataset
emotion_model.h5 pre-trained model


Run the application:
bashCopypython emotion_detector.py


How It Works
Emotion Model
The system employs a Convolutional Neural Network (CNN) trained on the FER2013 dataset. The model architecture includes:

Multiple Conv2D layers
MaxPooling2D layers
Dense layers
Batch Normalization
Output layer with 7 emotion classes

Face Detection
OpenCV's pre-trained Haar Cascade classifier is used for real-time face detection in the video feed.
Emotion Detection Pipeline

Capture video frame from webcam
Detect faces using Haar Cascade classifier
Preprocess detected face region
Pass processed image through CNN model
Get emotion prediction
Overlay corresponding emoji
Display result in real-time

Controls

Press 'C' to capture and save screenshot
Press 'Q' or click 'Exit' button to quit application

Requirements

Python 3.x
OpenCV
TensorFlow
Keras
NumPy
Matplotlib
Seaborn

Important Notes

Emoji images must be placed in the emojis/ directory with correct naming:

angry.jpg
disgust.jpg
fear.jpg
happy.jpg
neutral.jpg
sad.jpg
surprise.jpg


Face detection performance depends on:

Face size in frame
Camera quality
Lighting conditions


System initialization time varies based on hardware specifications

Troubleshooting
If you encounter issues:

Ensure all dependencies are correctly installed
Verify all required files are present and correctly named
Check camera permissions are granted
Ensure sufficient lighting for face detection

License
This project is licensed under the MIT License - see the LICENSE file for details.
Contributing
Contributions are welcome! Please feel free to submit a Pull Request.Last edited just now
