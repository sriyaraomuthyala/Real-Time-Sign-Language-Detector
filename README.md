# Real-Time Sign Language Detector

## Overview

The Real-Time Sign Language Detector is an innovative project aimed at creating an efficient and accurate system to detect and interpret American Sign Language (ASL) in real-time using a webcam. This project leverages advanced machine learning techniques, computer vision, and deep learning frameworks to recognize and translate hand gestures into meaningful text.

## Objectives

1. **Real-Time Detection:** Enable real-time sign language detection using a webcam.
2. **High Accuracy:** Achieve a high level of accuracy in interpreting various sign language gestures.
3. **User-Friendly Interface:** Provide an intuitive interface for users to interact with the system.
4. **Extensibility:** Ensure the system can be extended to include more gestures and languages in the future.

## Snippets Of Model In Action
![Screenshot 2024-02-27 162134](https://github.com/user-attachments/assets/11a907c2-1ad0-4cb3-9cf5-0422d3f5f47f)
![Screenshot 2024-02-27 162328](https://github.com/user-attachments/assets/20dc4bcf-baf5-4043-a7a4-975b83f0e69e)
![Screenshot 2024-02-27 163516](https://github.com/user-attachments/assets/b43ed8b4-aae2-4036-ae99-f512d414a089)
![Screenshot 2024-02-27 163637](https://github.com/user-attachments/assets/09553b63-3878-4e73-8b31-55abf50f6bf8)
![Screenshot 2024-02-27 163415](https://github.com/user-attachments/assets/2829aa84-f15a-44da-b09b-e158e034ed22)

## Key Components

### 1. Data Collection

Data collection involves capturing video sequences of different ASL gestures. For each gesture:
- 30 video sequences are recorded.
- Each sequence consists of 30 frames.
- The gestures include common phrases such as "hello," "how are you," "thank you," and others.

### 2. Feature Extraction

Using the Mediapipe library, key points from the face, hands, and pose are extracted from each frame. These key points serve as the features for the machine learning model:
- Face landmarks
- Pose landmarks
- Left hand landmarks
- Right hand landmarks

### 3. Model Training

A Long Short-Term Memory (LSTM) neural network is trained on the extracted key points. The LSTM network is chosen for its effectiveness in handling sequential data. The architecture of the neural network includes:
- Multiple LSTM layers to capture the temporal dynamics of the gestures.
- Dense layers for classification.
- Softmax activation in the final layer to output probabilities for each gesture class.

### 4. Real-Time Prediction

In the real-time detection phase:
- The webcam feed is processed frame by frame.
- Key points are extracted and fed into the trained LSTM model.
- The model predicts the gesture being performed.
- The predicted gesture is displayed on the screen, along with a visualization of prediction probabilities.

## Model Performance

The final trained model achieved an accuracy of approximately **93.33%** on the test dataset. This high accuracy indicates the model's effectiveness in recognizing and interpreting ASL gestures accurately.

### Usage

### Setup

1. **Dependencies:** Ensure all required dependencies are installed, including TensorFlow, OpenCV, Mediapipe, Scikit-learn, and Matplotlib.
2. **Data Preparation:** Prepare the dataset by recording and storing gesture sequences.
3. **Model Training:** Train the LSTM model on the prepared dataset.
4. **Real-Time Detection:** Run the real-time detection script to start recognizing gestures through the webcam.

### Running the Application

1. **Start Webcam Feed:** Launch the real-time detection script.
2. **Perform Gestures:** Perform the ASL gestures in front of the webcam.
3. **View Predictions:** See the predicted gesture and probability visualization on the screen.

### Customization

- **Adding New Gestures:** Record new gesture sequences and retrain the model.
- **Improving Accuracy:** Collect more data, fine-tune the model, and experiment with different model architectures.

## Conclusion

The Real-Time Sign Language Detector provides a powerful tool for bridging the communication gap between sign language users and non-users. With its high accuracy and real-time capabilities, it has the potential to be integrated into various applications, enhancing accessibility and inclusivity. The project serves as a foundation for further research and development in the field of sign language recognition and human-computer interaction.
