# Hand-Gesture-Controlled-Tic-Tac-Toe

## Project Description

Hand Gesture Controlled Tic-Tac-Toe is an interactive computer vision game built using Python. The game allows the player to play Tic-Tac-Toe against an AI opponent using hand gestures instead of a mouse or keyboard.

The program uses a webcam to detect the player's hand and track the position of the index finger. The finger acts as a cursor on the screen. By holding the finger over a grid cell for a short duration (dwell time), the player places an "X" in that cell. The AI then responds with its own move using the Minimax algorithm.

The game combines computer vision, artificial intelligence, and real-time graphics to create a touchless gaming experience.

## Objective

The objective of this project is to demonstrate how machine learning based hand tracking can be integrated with a game engine to build gesture-controlled applications. It also showcases the implementation of the Minimax algorithm for an unbeatable Tic-Tac-Toe AI.

## Features

* Hand gesture based game control
* Real-time hand tracking using webcam
* Touchless gameplay using index finger position
* Smooth cursor movement using interpolation
* Dwell-based selection (hold finger to select a cell)
* AI opponent using the Minimax algorithm
* Real-time camera background
* Visual pointer tracking
* Animated selection arc while placing a move
* Game result detection (Win / Lose / Draw)
* Restart option after game ends

## Technologies and Libraries Used

Python 3

Libraries:

* OpenCV (cv2) – Used for webcam video capture and frame processing
* MediaPipe – Used for machine learning based hand landmark detection
* Pygame – Used for creating the game interface and rendering graphics
* NumPy – Used for board representation and game logic calculations
* Time – Used for dwell-time interaction
* OS – Used for locating the hand tracking model file

## Machine Learning Model

The project uses the MediaPipe Hand Landmarker model to detect and track hand landmarks. The index finger tip landmark is used to control the cursor position on the screen.

Model file required:
hand_landmarker.task

This file must be placed in the same directory as the Python script.

## How the Game Works

1. The webcam captures live video from the user.
2. MediaPipe processes each frame and detects hand landmarks.
3. The index finger tip is used as a pointer on the screen.
4. The pointer position determines the grid cell being targeted.
5. If the finger remains inside a cell for more than 2 seconds, a move is placed.
6. The player places an "X".
7. The AI responds with an "O" using the Minimax algorithm.
8. The system checks for a win, loss, or draw after each move.
9. If the game ends, a result message is displayed.

## Game Controls

Hand Movement
Move your index finger to control the cursor.

Hold Gesture (Dwell)
Keep your finger inside a grid cell for about 2 seconds to place your move.

Keyboard Controls
Press **R** to restart the game after it ends.

Close Window
Close the window to exit the game.

## Game Board Representation

The Tic-Tac-Toe board is stored as a 3x3 NumPy array.

Values used:
0  = Empty cell
1  = Player move (X)
-1 = AI move (O)

## Artificial Intelligence

The AI uses the **Minimax algorithm**, which evaluates all possible future moves and selects the optimal one. This ensures that the AI never loses if it plays perfectly.

Possible outcomes evaluated by the algorithm:

* Win
* Loss
* Draw

## How to Run the Program

Step 1: Install required libraries

pip install opencv-python mediapipe pygame numpy

Step 2: Download the MediaPipe hand tracking model

hand_landmarker.task

Step 3: Place the model file in the same directory as the Python script.

Step 4: Run the program

python gesture_tictactoe.py

Step 5: Allow access to your webcam.

The game window will open and begin tracking your hand.

## System Requirements

* Python 3.8 or later
* Webcam
* Basic GPU/CPU capable of real-time video processing

## Possible Improvements / Future Work

* Add sound effects and background music
* Add multiplayer gesture mode
* Implement difficulty levels for AI
* Improve gesture recognition accuracy
* Add hand gesture click instead of dwell selection
* Add score tracking system
* Add visual hand landmark display
* Improve UI design and animations

## Conclusion

This project demonstrates the integration of computer vision, machine learning, and game development using Python. It creates an innovative touchless gaming experience where players interact with the game using hand gestures captured through a webcam.
