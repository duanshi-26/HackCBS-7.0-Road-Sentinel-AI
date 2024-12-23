# DrowsyGuard: Real-Time Drowsiness Detection System

DrowsyGuard is a real-time drowsiness detection system designed to help prevent accidents caused by drowsy driving. Using computer vision techniques with OpenCV, dlib, and other relevant libraries, this system detects signs of drowsiness such as yawning and sleepy eyes. Upon detecting drowsiness, it triggers an alert sound to wake up the user.

## Key Features

- **Real-time Monitoring**: Detects drowsiness signs using facial landmarks
- **Alert System**: Triggers a sound alert when drowsiness is detected
- **Eye & Yawn Detection**: Utilizes the Eye Aspect Ratio (EAR) and lip distance to identify signs of drowsiness
- **Non-intrusive Operation**: The system works efficiently without requiring manual intervention

## How It Works

1. **Facial Landmark Detection**: The system uses dlib's pre-trained shape predictor model to detect key facial landmarks, focusing on the eyes and mouth to monitor for drowsiness signals.

2. **Eye Aspect Ratio (EAR)**: The Eye Aspect Ratio (EAR) is calculated by measuring the vertical and horizontal distances between specific eye landmarks. A decrease in EAR below a set threshold indicates that the eyes are closed, which may indicate drowsiness.

3. **Yawning Detection**: By calculating the distance between the upper and lower lips, the system detects yawning, another common sign of fatigue.

4. **Alert Mechanism**: When drowsiness or yawning is detected continuously for a set duration, the system triggers a sound alert to help the user stay awake.

## Getting Started

### Prerequisites

- Python 3.x
- OpenCV
- dlib
- imutils
- scipy
- numpy

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/duanshi-26/HackCBS-7.0-Road-Sentinel-AI/tree/main
   cd Drowsiness_detection_using_dlib_and_cv
   ```

2. **Install required Python libraries:**
   Create a virtual environment and install dependencies by running:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download the Shape Predictor Model:**
   - Download the pre-trained shape predictor file (`shape_predictor_68_face_landmarks.dat`) from dlib's official website
   - Extract the `.dat` file and place it in the root directory of your project

4. **Run the System:**
   Start the drowsiness detection system with the following command:
   ```bash
   python drowsiness_detection.py --webcam 0
   ```
   This will start the webcam and begin real-time drowsiness detection.

## Usage

The system will continuously analyze the user's face for signs of drowsiness. When the following conditions are met:
- The Eye Aspect Ratio (EAR) falls below the threshold indicating closed eyes
- Yawning is detected by the distance between the upper and lower lips

The system will trigger an alert sound to prevent the user from falling asleep.

### Adjusting Settings

The threshold for EAR detection and yawning sensitivity can be adjusted in the `drowsiness_detection.py` file depending on user needs.

## License

This project is licensed under the MIT License – see the LICENSE file for details.

## Acknowledgments

- The dlib library is used for facial landmark detection
- OpenCV is utilized for video capture and image processing
- The project is inspired by the need for better driver safety and awareness
