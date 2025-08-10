
# Hand Gesture Recognition Using Leap Motion (Infrared Images)

This project implements a **deep learning-based hand gesture recognition system** utilizing grayscale infrared images captured from the **Leap Motion Controller**. The model classifies **10 distinct hand gestures in real-time** via a webcam, enabling intuitive **Human-Computer Interaction (HCI)**.

---

## 🔍 Project Overview

- **📸 Input:** Grayscale infrared images of hands performing gestures  
- **🧠 Model:** Convolutional Neural Network (CNN) developed using **TensorFlow/Keras**  
- **🎯 Output:** Real-time classification of gestures (e.g., *palm*, *L*, *fist*, *down*, etc.)  
- **🎥 Interface:** Real-time webcam feed with on-screen gesture predictions  

---

## 📁 Dataset Information

- **Dataset:** Leap Motion Hand Gesture Dataset (Infrared)  
- **Source:** [LeapGestRecog – Kaggle](https://www.kaggle.com/datasets/gti-upm/leapgestrecog)  
- **Structure:**
```

leapGestRecog/
├── 00/
│   ├── 01\_palm/
│   ├── 02\_l/
│   ├── ...
│   └── 09/
├── 01/
├── ...
└── 09/

````
- **10 subjects** (`00`–`09`)  
- **10 gesture classes** (palm, L, fist, down, etc.)  
- **Format:** Grayscale `.png` images  

---

## 🧠 Model Training

Train the CNN model:
```bash
python train_gesture_model.py
````

* Saves trained model: `gesture_model.h5`
* Saves label encoder: `label_encoder.pkl`
* Generates accuracy plot: `training_accuracy.png`

---

## 🎥 Real-Time Prediction

Run the webcam-based gesture recognition:

```bash
python predict.py
```

* Opens webcam feed
* Displays predicted gesture label in real time
* Press **ESC** to exit

---

## 📂 File Structure

```
.
├── gesture_model.h5          # Trained CNN model
├── label_encoder.pkl         # Encoded class labels
├── train_gesture_model.py    # Model training script
├── predict.py                # Real-time prediction script
├── training_accuracy.png     # Accuracy visualization
├── README.md                 # Project documentation
```

---

## 📈 Performance

* **Validation Accuracy:** 99.96%
* **Overfitting:** No significant signs detected
* **Generalization:** Performs well across multiple subjects

---

## 📚 Future Work

* Gesture-based control for media and applications
* Voice feedback for recognized gestures
* Model deployment using **Flask** or **Streamlit**

```


