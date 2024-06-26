# Hand-Gesture-Controlled-Math-Problem-Solver
Hand Gesture Math Solver: Python, OpenCV, and Google's generativeai enable real-time math problem solving via webcam gestures (cvzone). Draw, clear canvas, input expressions—AI processes and displays solutions instantly. Enhances learning with interactive, hands-on engagement.

# Project Overview: Hand Gesture Controlled Math Problem Solver
Project Goal:
The goal of this project is to create a real-time interactive application that allows users to solve math problems using hand gestures captured through a webcam. The system detects specific hand gestures to initiate drawing, clearing the canvas, and inputting numerical expressions.

# Key Features:
# Hand Detection and Tracking:

Utilizes the cvzone.HandTrackingModule to detect and track hand movements in real-time from a webcam feed.
Tracks up to two hands simultaneously and identifies landmarks (fingertips) for gesture recognition.

# Gesture-based Interaction:

1. Drawing Mode: Activated when the index finger is raised ([0, 1, 0, 0, 0]). Allows users to draw on a canvas overlay on the video feed by moving their finger.
2. Canvas Clearing: Triggered by raising the thumb ([1, 0, 0, 0, 0]), which clears the drawing canvas.
3. Math Problem Input: Initiated by raising the middle three fingers ([0, 0, 1, 1, 1]). Enables users to input numerical expressions by tracking the position of the index finger tip to form numbers or expressions.
   
# Integration with Generative AI:

Utilizes Google's generativeai library and an API key for content generation.
Once a mathematical expression is inputted, it sends the canvas image and the problem statement to a generative model (gemini-1.5-flash) for processing.
Receives the result back from the model and displays it on the video feed using OpenCV.

# User Interface:

Displays real-time webcam video with overlays for drawing and math problem results.
Uses OpenCV to manage video capture, image processing, and displaying the combined video feed with overlays.
Error Handling and Feedback:

Includes basic error handling for mathematical expression evaluation.
Provides visual feedback to the user through text overlays on the video feed for successful problem solutions or errors.

# Implementation Details:
Technologies Used: Python, OpenCV, cvzone, generativeai, PIL (Pillow).
API Integration: Configured with a Google API key (genai.configure(api_key="......")) for generative content processing.

Mathematical Expression Evaluation: Uses Python's eval() function to evaluate user-inputted numerical expressions.
User Interaction: Users interact with the application by performing specific hand gestures recognized by the system, triggering different functionalities.

Future Enhancements:
Enhanced Gesture Recognition: Improve accuracy and responsiveness of hand gesture detection.
Advanced AI Integration: Explore more complex generative models or AI capabilities for broader problem-solving tasks.
User Interface Refinement: Enhance the visual feedback and interaction elements for a more intuitive user experience.

# Conclusion:
This project showcases the integration of computer vision with generative AI to create an interactive and engaging application. By leveraging hand gestures, users can draw, clear the canvas, and input mathematical expressions to receive instant problem-solving results, providing a novel and educational approach to human-computer interaction.
