
# 🖐️ ASL Hand Sign Recognition

This project uses [MediaPipe](https://google.github.io/mediapipe/) to extract hand landmarks and a **Random Forest** model to recognize American Sign Language (ASL) alphabet letters. It also includes **real-time sign recognition** using your webcam.

---

## 📌 Features

- 📁 Uses the [ASL Alphabet dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet) from Kaggle  
- 🧠 Extracts hand landmarks using MediaPipe  
- 🌲 Trains a Random Forest classifier on landmark data  
- 📊 Tests accuracy on validation data  
- 📷 Predicts ASL hand signs in real-time via webcam  

---

## 🛠 Requirements

Install the required Python libraries:

```
pip install mediapipe opencv-python scikit-learn joblib tqdm
```

---

## 🚀 How to Use

### 📥 Step 1: Download Dataset

1. Download the ASL Alphabet Dataset from Kaggle:  
   https://www.kaggle.com/datasets/grassknoted/asl-alphabet  
2. Extract it and place it inside a folder named `dataset` in the root of this project.

### 🏋️‍♂️ Step 2: Train the Model

Run the training script:

```
python train.py
```

This will train and save the model as `asl_model.pkl`.

### ✅ Step 3: Test the Model

Evaluate the model:

```
python test.py
```

### 🔮 Step 4: Real-Time Prediction

Start real-time webcam recognition:

```
python predict.py
```

- Ensure your webcam is working.  
- Show your hand clearly in front of the camera.  
- Press **q** to quit.

---

## ⚙️ How It Works

- MediaPipe detects **21 hand landmarks** (x, y, z coordinates).  
- These landmarks are used as features.  
- A Random Forest classifier is trained on this feature set to predict ASL letters.  
- OpenCV manages real-time webcam access and display.

---

## 📝 Notes

- The model uses **landmark coordinates**, not raw images, for better efficiency.  
- For best results: use a clean background and keep your hand visible and centered.  
- Supports static ASL letters (A–Z), excluding motion-based gestures like "J" and "Z".

---

## 🤝 Contributing

Pull requests are welcome! Feel free to fork or open an issue.

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Vivan Rajath**  
GitHub: https://github.com/VivanRajath
