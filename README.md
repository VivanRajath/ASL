ASL Hand Sign Recognition using MediaPipe & Random Forest
This project uses MediaPipe to extract hand landmarks and a Random Forest classifier to recognize American Sign Language (ASL) letters in real-time via webcam or from static image datasets.

Project Structure

ASL/
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
Use the Kaggle dataset: https://www.kaggle.com/datasets/grassknoted/asl-alphabet

⚙️ Installation
git clone https://github.com/yourusername/ASL.git
cd ASL

# Create virtual environment (optional)
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt
🏋️‍♂️ Training
Train the model using MediaPipe hand landmarks:


python train.py
This will generate a trained model saved as asl_model.pkl.

Evaluate the trained model:


python test.py
You’ll get the test accuracy printed in the console.

Real-Time Prediction (Webcam)
Use your webcam to detect ASL signs in real time:

python predict.py
✋ Make sure your hand is clearly visible in the camera frame. Press q to exit.

Utilities
model.py: Initializes MediaPipe hand detection model

utils.py: Extracts 21 hand landmark coordinates (x, y, z)

Requirements
opencv-python
mediapipe
scikit-learn
joblib
tqdm
🚀 Future Enhancements
Add GUI with sign history

Use CNN with landmark heatmaps for better accuracy

Train using your own webcam gesture data


📄 License
MIT License

