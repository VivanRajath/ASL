ASL Hand Sign Recognition
This project uses MediaPipe to detect hand landmarks and trains a Random Forest model to recognize American Sign Language (ASL) alphabet letters. It includes real-time prediction using your webcam.

What This Project Does
Uses the ASL Alphabet dataset from Kaggle

Extracts hand landmarks using MediaPipe

Trains a Random Forest model

Tests accuracy on validation data

Predicts hand signs in real time using your webcam

Requirements
You need the following Python libraries:

mediapipe
opencv-python
scikit-learn
joblib
tqdm

Install them using pip or manually add them to your environment.

How to Use
Step 1: Download the ASL dataset from Kaggle and place it inside a folder named 'dataset'

Step 2: Run the training script using train.py to create the model

Step 3: Test the model using test.py

Step 4: Run predict.py to use your webcam for real-time ASL recognition

Make sure your webcam is working. Show your hand clearly in front of the camera. Press 'q' to quit.

Notes
This model does not use raw images. It works on landmark positions of your hand joints.
Make sure your background is clear and your hand is visible for best performance.
The trained model is saved as 'asl_model.pkl' after running the training script.
