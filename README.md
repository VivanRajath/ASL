ASL Hand Sign Recognition using MediaPipe & Random Forest
This project performs American Sign Language (ASL) letter recognition using MediaPipe for hand tracking and a Random Forest model trained on landmark data.

📁 Project Structure
ASL-Detector/
├── dataset/ → asl_alphabet_train/ (A/, B/, ..., Z/)
├── train.py → Train the model
├── test.py → Evaluate the model
├── predict.py → Real-time webcam ASL detection
├── model.py → Loads MediaPipe hand model
├── utils.py → Extracts hand landmarks
├── requirements.txt → Python dependencies
├── asl_model.pkl → Trained model (auto-generated)
└── README.md → Project documentation

📦 Installation
Clone this repository:
git clone https://github.com/yourusername/ASL-Detector.git
cd ASL-Detector

(Optional) Create a virtual environment:
python -m venv venv
source venv/bin/activate
(On Windows: venv\Scripts\activate)

Install dependencies:
pip install -r requirements.txt

📂 Dataset Setup
Download the ASL Alphabet dataset from Kaggle:
https://www.kaggle.com/datasets/grassknoted/asl-alphabet

Extract it like this:
dataset/asl_alphabet_train/A/
dataset/asl_alphabet_train/B/
...

🏋️‍♂️ Train the Model
Run:
python train.py

This creates asl_model.pkl.

🧪 Test the Model
Run:
python test.py

🎥 Real-Time ASL Detection
Run:
python predict.py

✋ Show your hand signs in front of your webcam.
Press q to quit.

✅ Requirements
mediapipe

opencv-python

scikit-learn

joblib

tqdm

Install using:
pip install -r requirements.txt

🚀 Future Improvements
GUI for interaction

Deep Learning upgrade

Webcam-based custom training

