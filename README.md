🧠 ASL Hand Sign Recognition using MediaPipe & Random Forest
This project uses MediaPipe to extract hand landmarks and a Random Forest classifier to recognize American Sign Language (ASL) letters in real-time via webcam or from static image datasets.

📂 Project Structure
bash
Copy
Edit
ASL-Detector/
│
├── dataset/
│   └── asl_alphabet_train/   # Kaggle dataset folder (A/, B/, ..., Z/)
│
├── train.py                  # Train model from dataset
├── test.py                   # Evaluate model accuracy
├── predict.py                # Real-time ASL detection from webcam
│
├── model.py                  # MediaPipe hand model loader
├── utils.py                  # Landmark extraction and preprocessing
├── requirements.txt          # Python dependencies
├── README.md                 # Project documentation (this file)
└── asl_model.pkl             # Trained model (generated after training)
🧪 Dataset
Use the Kaggle dataset:
🔗 ASL Alphabet

Put it inside the dataset/ folder like this:

bash
Copy
Edit
dataset/asl_alphabet_train/A/
dataset/asl_alphabet_train/B/
...
⚙️ Installation
bash
Copy
Edit
git clone https://github.com/yourusername/ASL-Detector.git
cd ASL-Detector

# Create virtual environment (optional)
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt
🏋️‍♂️ Training
Train the model using MediaPipe hand landmarks:

bash
Copy
Edit
python train.py
This will generate a trained model saved as asl_model.pkl.

📊 Testing
Evaluate the trained model:

bash
Copy
Edit
python test.py
You’ll get the test accuracy printed in the console.

🎥 Real-Time Prediction (Webcam)
Use your webcam to detect ASL signs in real time:

bash
Copy
Edit
python predict.py
✋ Make sure your hand is clearly visible in the camera frame. Press q to exit.

🧰 Utilities
model.py: Initializes MediaPipe hand detection model

utils.py: Extracts 21 hand landmark coordinates (x, y, z)

✅ Requirements
Copy
Edit
opencv-python
mediapipe
scikit-learn
joblib
tqdm
🚀 Future Enhancements
Add GUI with sign history

Use CNN with landmark heatmaps for better accuracy

Train using your own webcam gesture data

📸 Demo
https://github.com/yourusername/ASL-Detector/assets/demo.gif
(Include a short screen recording of your real-time ASL detection)

📄 License
MIT License

