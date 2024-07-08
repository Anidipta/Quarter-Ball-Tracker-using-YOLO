# Project Title: Ball Tracking and Event Detection in Video 

## Objective:
Develop a computer vision program to track the movement of balls of different colors across various quadrants in a video. The program will record events of each ball entering and exiting each numbered quadrant and save the details in a specified format. The processed video will display the tracking information and overlay text indicating entry or exit events.

## Model Details
Two custom YOLOv8x models were used in this project:

- Quadrant Detection Model: This model detects and identifies the quadrants in the video frame.
- Ball Detection Model: This model detects and tracks balls of different colors, identifying their positions relative to the quadrants.
- Combined Model is used for the final detection using casceding object detection and identification method.

## Link to the Colab Notebook - [CLICK HERE](https://colab.research.google.com/drive/1EGUlv8hCES5XOHuVv5tpenP1wSIR0ry1?usp=sharing)

## Output:

### Processed Video:

* Tracks balls with their colors.
* Time Tracker at the Left Top corner
* Detection Boxes with confidence level

  Link to the Processed video --> [CLICK HERE](https://drive.google.com/file/d/1c_EzHK5AWmWOBoT0Yf4Q2Zuz8NICl0Jl/view?usp=sharing)

### Text File:

* Records events in the format: Time, Quadrant Number, Ball Colour, Type (Entry or Exit).

### Tools and Technologies Used:

* YOLOv8x for object detection
* OpenCV for video processing
* NumPy for data manipulation
* Pandas for data storage and manipulation
* Python for scripting


### Usage Instructions
* Clone the repository and navigate to the project directory.
* Ensure you have the required packages by running:
  
```bash
pip install -r requirements.txt
```

* Place your input video in the project directory.
* Update the paths in the process_video function to point to your input video and desired output locations.
* Run the Jupyter notebook to process the video and generate the output files.
