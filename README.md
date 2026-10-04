ESP32 Gesture Recognition System

An ESP32-CAM-based project that detects hand gestures using computer vision and converts recognized gestures into spoken words through a mobile phone.

Features

- Captures images using ESP32-CAM.
- Detects hand gestures using MediaPipe.
- Processes images through a Python Flask server.
- Converts recognized gestures into speech using the phone browser.
- Supports gestures such as thumbs up, open palm, fist, peace, pointing up, and rock.

Technologies Used

- ESP32-CAM (AI Thinker)
- Arduino IDE and C++
- Python and Flask
- OpenCV, NumPy, and MediaPipe
- HTML, JavaScript, and Web Speech API

Project Structure

Esp32_coding/
├── Flask_server_code
├── working esp32_code
└── README.md

Requirements

- ESP32-CAM board
- Computer with Python installed
- Arduino IDE
- Mobile phone with a supported browser
- Wi-Fi or a shared mobile hotspot

Setup

1. Clone the repository

git clone https://github.com/sazil07/Esp32_coding.git
cd Esp32_coding

2. Install Python dependencies

pip install flask numpy opencv-python mediapipe

3. Prepare the server

Place the required "hand_landmarker.task" model file in the server's working directory and run the Flask server:

python Flask_server_code

4. Configure the ESP32-CAM

Open "working esp32_code" in Arduino IDE. Configure your Wi-Fi credentials and Flask server IP address, then upload the program to the ESP32-CAM.

5. Start gesture recognition

Connect your phone and ESP32-CAM to the same network. Open the server's "/speak" page in your phone's browser and press Start to enable speech.

How It Works

1. ESP32-CAM captures an image.
2. The image is sent to the Flask server.
3. MediaPipe identifies hand landmarks, and the server classifies the gesture.
4. The detected gesture is returned through the server API.
5. The phone browser displays and speaks the recognized word.

Future Improvements

- Support more hand gestures.
- Improve recognition accuracy and response time.
- Add a dedicated mobile interface.
- Improve error handling and network security.

Author

Mohammad Sazil

GitHub: "@sazil07" (https://github.com/sazil07)
