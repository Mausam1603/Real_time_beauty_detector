# Real-time Beauty Detection

This project is a real-time beauty detection system using computer vision and deep learning. The system analyzes facial features and ratios based on the Golden Ratio (phi) and provides a beauty score along with suggestions for improvement. It also performs skin tone analysis.

## Features
- **Facial Feature Analysis**: Calculates face, eye, and nose ratios using MediaPipe Face Mesh landmarks.
- **Beauty Score Prediction**: Uses a neural network to predict a beauty score based on facial proportions.
- **Golden Ratio Compliance**: Compares facial proportions with the Golden Ratio for symmetry analysis.
- **Skin Tone Analysis**: Classifies skin tone based on the HSV color space.
- **Real-time Feedback**: Provides suggestions on improving face, eye, and nose proportions based on the score.
  
## Technologies Used
- **OpenCV**: For image processing and video capture.
- **MediaPipe**: For facial landmark detection.
- **TensorFlow**: For building and training a neural network to predict beauty scores.
- **Matplotlib**: For visualizing data and facial feature guidelines.
  
## How It Works
1. **Facial Landmark Detection**: Uses MediaPipe to detect 468 facial landmarks in real time.
2. **Beauty Ratios Calculation**: Calculates the following ratios:
   - Face Ratio (height to width)
   - Eye to Face Ratio
   - Nose to Face Ratio
3. **Score Prediction**: A neural network predicts the beauty score based on the above ratios.
4. **Golden Ratio Comparison**: Compares the calculated ratios with the Golden Ratio (1.618) and provides feedback on symmetry.
5. **Skin Tone Analysis**: Extracts skin tone from the forehead region and classifies it into Light, Medium, or Dark categories.

## Neural Network Model
The model takes three input features:
- Face ratio
- Eye-to-face ratio
- Nose-to-face ratio

The neural network has the following architecture:
- Input layer (3 features)
- 64 neurons in the first hidden layer
- 32 neurons in the second hidden layer
- Output layer with a single neuron using the sigmoid activation function to predict the beauty score (0 to 1).

## Instructions to Run the Code

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/real-time-beauty-detection.git
   cd real-time-beauty-detection
   ```

2. Install the dependencies:
   ```bash
   pip install opencv-python mediapipe tensorflow matplotlib
   ```

3. Run the script:
   ```bash
   python beauty_detection.py
   ```

4. The program will capture video from your webcam, process the frames, and display the beauty score and analysis on each frame. Press `q` to quit.

## Output
An example of the output:

![Output1](https://github.com/user-attachments/assets/909f3a8e-cb2c-49e0-b1cd-c95b076b0b2d)


- **Beauty Score**: 0.72 (Good)
- **Skin Tone**: Light
- Suggestions for improving facial proportions and symmetry.

## Future Improvements
- Enhance the neural network with more training data for better accuracy.
- Add support for additional features like smile detection or age estimation.
- Optimize skin tone analysis for more precise classification.

