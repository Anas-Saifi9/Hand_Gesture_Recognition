✋ AI-Powered Hand Gesture Recognition
AI-based hand gesture and sign language recognition system aimed at reducing the communication barrier between individuals who are unable to speak and the general public. This project also lays the foundation for gesture-controlled personal systems in the future.

📌 Project Motivation
With over 430 million people worldwide affected by hearing loss, there's a dire need for accessible, real-time tools that can interpret sign language. This system aims to enable inclusive communication through AI and computer vision, especially in education, healthcare, and public spaces.

🎯 Project Goals
Enable real-time translation of hand gestures and sign language into text or audio.
Support gesture-based control for smart systems (e.g., play music with a "Thumbs Up").
Build a scalable, robust system using AI, accessible to all with just a webcam.

🔍 Problem Statement
Lack of accurate real-time systems to interpret hand gestures/sign language.
Absence of sign language interpreters in many public environments.
Limited gesture recognition solutions for real-world use cases.

🧠 Technologies Used
Python, OpenCV, Streamlit
MediaPipe for hand tracking
Keras / TensorFlow for deep learning
Text-to-Speech (pyttsx3) for voice output

🗃️ Dataset & Preprocessing
Dataset	Classes	Samples	Format
ASL (Kaggle)	26	~87,000	64×64 Grayscale
Custom (OpenCV)	26	~2,000+	64×64 Grayscale
MediaPipe	26+	Real-time	42D Landmarks
Data augmented by rotation, zoom, and flip.
Input normalized for faster inference.

🧩 Model Architecture
CNN for static gesture recognition.
Input: 64×64×1 grayscale images
Layers:Conv2D → MaxPooling → Dropout → Dense → Softmax
Accuracy: ~94–97% on test data
For dynamic gestures, LSTM is optionally used on hand landmark sequences.
🔄 Inference Pipeline
Capture live video (via OpenCV & Streamlit)
Detect hand landmarks (MediaPipe)
Preprocess ROI & feed to CNN
Output class prediction (e.g., “A”, “Thumbs Up”)
Display result + optional text-to-speech
Trigger actions (e.g., play music on "Thumbs Up")

⚡ Performance
Inference Speed: ~30–60ms/frame
FPS: 15–25 depending on hardware
Real-world accuracy: ~92–95%

💡 Future Scope
Dynamic sentence-level sign language interpretation
Mobile version using TensorFlow Lite or ONNX
Voice-to-sign gesture conversion
Smart home integration using gestures

👨‍💻 Team Falcons
Mohd. Anas (Leader)
Naman Choudhary
Prashant Singh
Ritik Thakur
