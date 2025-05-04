
# Head Gesture Music Control Application

This application is an accessibility tool that allows users with physica limitationsto control music playback using head gestures and facial expressions, without needing to use their hands. It was created by me, Michael Li. I am a junior at the University of Notre Dame who taught myself to code about a year ago.

# Youtube Link 
https://youtu.be/aip8K8_nnNo

# Where to Download
Full Code in located as one.py 

Actual GUI is located as zip-file
# Core Functionality
The application uses computer vision and facial landmark detection to track a user's face through their webcam and interpret specific movements as commands to control music playback. The primary features include:

Facial and Head Gesture Recognition: The program uses the dlib library with a 68-point facial landmark detector to track:

Head movements (turning left/right, tilting up/down)
Eye movements (blinking, winking)
Mouth movements (smiling, opening)
Eyebrow movements (raising eyebrows)


Music Control: Currently configured for macOS and Spotify using AppleScript, with functions to:

Play/pause music
Skip to next/previous song
Adjust system volume up/down


Customizable Gesture Mapping: Users can assign different actions to various gestures through a graphical interface. For example:

Looking right → Volume up
Looking left → Pause music
Long blink → Next song


# Advanced Combination Gestures: 
The app supports sequences of gestures, such as:

Smile for 3 seconds, then look right → Volume up
Open mouth for 2 seconds, then look left → Previous song


Adjustable Sensitivity: Users can fine-tune detection thresholds for each gesture:

How far to turn the head
How long to hold expressions
Sensitivity for detecting blinks, smiles, etc.



# User Interface
The application has two main components:

Configuration UI: A graphical interface using tkinter with tabs for:

Gesture Mappings: Assign actions to gestures
Sensitivity Settings: Adjust thresholds and timings
Instructions: Help text explaining the program


Camera Visualization: The webcam feed with real-time visual feedback showing:

Facial landmark tracking
Pose estimation (head orientation)
Status of active gestures
Progress bars for duration-based gestures
Text feedback about detected actions



# Technical Implementation
The code implements several sophisticated techniques:

3D Head Pose Estimation: Uses the PnP algorithm to determine head orientation in terms of pitch, yaw, and roll angles from 2D facial landmarks.
Facial Feature Analysis: Calculates ratios and measurements to determine:

Eye aspect ratio for blink detection
Mouth aspect ratio for detecting mouth opening
Smile detection based on mouth corner positions
Eyebrow positioning for raised eyebrow detection


Gesture State Management: Tracks the state, duration, and progress of each possible gesture, including combination gestures.
Configuration Management: Provides saving and loading of user preferences in JSON format.

# Target Users
This application is particularly valuable for users with physical limitations who may find it difficult to use traditional computer interfaces. By providing hands-free control of music playback, it enhances accessibility and autonomy for people with various mobility challenges.
The developer specifically mentions that while it currently only supports macOS and Spotify, there are plans to expand compatibility to include Apple Music and non-macOS platforms.
