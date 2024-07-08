# Project Title: Ball Tracking and Event Detection in Video 

## Objective:
Develop a computer vision program to track the movement of balls of different colors across various quadrants in a video. The program will record events of each ball entering and exiting each numbered quadrant and save the details in a specified format. The processed video will display the tracking information and overlay text indicating entry or exit events.

## Model Details
Two custom YOLOv8x models were used in this project:

- Quadrant Detection Model: This model identifies the quadrants in the video, helping in mapping the ball positions accurately.
  
- Ball Detection Model: This model detects balls in the video, identifies their colors, and tracks their movements to determine entry or exit events.
  
- Combined Model is used for the final detection using casceding object detection and identification method.

## Link to the Colab Notebook - [CLICK HERE](https://colab.research.google.com/drive/1EGUlv8hCES5XOHuVv5tpenP1wSIR0ry1?usp=sharing)

## Model Result-

 - **Confusion Matrices**
The confusion matrices show the performance of the detection models.

<div style="display: flex;">
  <div style="flex: 1; padding: 10px;">
    <h5> Ball Detection Model</h5>
    <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/confusion_matrix(1).png" alt="Image 1" style="width: 50%; max-width: 300px;">
  </div>
  <div style="flex: 1; padding: 10px;">
    <h5>Quarter Detection Model</h5>
    <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/confusion_matrix.png" alt="Image 2" style="width: 50%; max-width: 300px;">
  </div>
</div>

- **Label Analysis**
The label analysis includes the distribution of detected classes and their relationships.

<div style="display: flex;">
  <div style="flex: 1; padding: 10px;">
    <h5> Ball Detection Model</h5>
    <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/labels_correlogram(1).jpg" alt="Image 1" style="width: 100%; max-width: 300px;">
  </div>
  <div style="flex: 1; padding: 10px;">
    <h5>Quarter Detection Model</h5>
    <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/labels_correlogram.jpg" alt="Image 2" style="width: 100%; max-width: 300px;">
  </div>
</div>

- **Detection Results**
The detection results demonstrate the model's accuracy in identifying balls and their events.

<div style="display: flex;">
  <div style="flex: 1; padding: 10px;">
    <h5> Ball Detection Model</h5>
    <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/results(1).png" alt="Image 1" style="width: 100%; max-width: 300px;">
  </div>
  <div style="flex: 1; padding: 10px;">
    <h5>Quarter Detection Model</h5>
    <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/results.png" alt="Image 2" style="width: 100%; max-width: 300px;">
  </div>
</div>

## Output:

### Processed Video:

* Tracks balls with their colors.
* Time Tracker at the Left Top corner
* Detection Boxes with confidence level

Link to the Processed video --> [CLICK HERE](https://drive.google.com/file/d/1c_EzHK5AWmWOBoT0Yf4Q2Zuz8NICl0Jl/view?usp=sharing)


Demo Image Detected by the model

![demo image.png](https://github.com/Anidipta/AI-Assignment/blob/main/demo%20image.png)

### Text File:

* Records events in the format: Time, Quadrant Number, Ball Colour, Type (Entry or Exit).

Link to the TXT File --> [CLICK HERE](cleaned_result.txt)

### Tools and Technologies Used:

* YOLOv8x for object detection
* OpenCV for video processing
* NumPy for data manipulation
* Pandas for data storage and manipulation
* Python for scripting

### Challenges faced:

1. **Object Tracking and Identification**: Maintaining the identity of each ball across frames is challenging due to occlusions and rapid movements.
2. **Real-time Performance**: Processing each frame of the video in real-time with complex models is computationally intensive and slow.
3. **Accuracy of Detection**: Ensuring high accuracy of ball and quarter detection in varied lighting and background conditions is difficult.
4. **State Management**: Correctly identifying and updating the state of balls (new, kept, or left) while tracking multiple objects in dynamic scenes is complex.

   
### Usage Instructions
* Clone the repository and navigate to the project directory.
* Ensure you have the required packages by running:
  
```bash
pip install -r requirements.txt
```

* Place your input video in the project directory.
* Update the paths in the process_video function to point to your input video and desired output locations.
* Run the Jupyter notebook to process the video and generate the output files.
