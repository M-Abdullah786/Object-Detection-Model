# Object-Detection-Model
The above model is a real-time image classification system designed to predict the class of objects (e.g., fruits and vegetables) captured through a live video feed from a webcam. It uses a pre-trained deep learning model loaded from a .h5 file to classify images into predefined classes.

---

# **Real-Time Image Classification using Pre-Trained Model**

This repository contains a Python program for real-time image classification. It uses a pre-trained deep learning model to classify objects (e.g., fruits and vegetables) from a live video feed captured through a webcam or mobile camera.

---

## **Features**
- **Live Video Feed Classification**: Predicts object classes in real-time from video frames.
- **Customizable Classes**: Easily update the class names to match your dataset.
- **Time Tracking**: Measures and displays the time taken to process each frame.
- **Real-Time Overlay**: Displays the predicted class name on the video feed.
- **User-Friendly Interface**: Press 'q' to stop the video feed.

---

## **Setup and Installation**

### **Prerequisites**
- Python 3.8 or higher
- Required Python libraries:
  - `opencv-python`
  - `numpy`
  - `tensorflow`

Install the required dependencies using:
```bash
pip install -r requirements.txt
```

### **Files**
- **`fruit_veg_classifier.h5`**: The pre-trained model file.
- **`main.py`**: The Python script for running the program.

---

## **Usage**

1. Place your pre-trained `.h5` model file in the same directory as the script.

2. Run the program:
   ```bash
   python main.py
   ```

3. The program will start capturing frames from your webcam. If using a mobile camera, replace the webcam capture URL with the mobile camera stream URL.

---

## **Program Description**

The script captures live video, processes each frame, and predicts the object's class in real time. Predictions are displayed on the video feed, along with the time taken for processing each frame.

### **Key Components**
1. **Preprocessing**:
   - Frames are resized to `(224, 224)` and normalized.
2. **Prediction**:
   - The model generates predictions for each frame, mapped to predefined class names.
3. **Overlay**:
   - Predicted class and processing time are displayed on the video feed.

---

## **Customization**

1. **Update Class Names**:
   Modify the `class_names` list in `main.py` to match the classes in your dataset:
   ```python
   class_names = ['class1', 'class2', 'class3']
   ```

2. **Change Video Source**:
   Replace `cv2.VideoCapture(0)` with the IP stream URL or another video source:
   ```python
   stream_url = "http://<IP>:<PORT>/video"
   cap = cv2.VideoCapture(stream_url)
   ```

3. **Adjust Model**:
   Replace `fruit_veg_classifier.h5` with your model trained on custom data.

---

## **License**

This project is free to use. Feel free to modify, distribute, or use it for any purpose.

---

Enjoy real-time classification with this simple yet powerful tool! 🚀
