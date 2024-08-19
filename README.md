# Project Title: Ball ⚽ Tracking  and Event Detection in Video 🎥

## **Objective:**
Develop an advanced computer vision program to track and classify the movement of balls in various colors across different quadrants within a video. The system will record each ball's entry and exit events from each numbered quadrant, displaying this information overlayed on the processed video.

## **Model Details:**

Two custom YOLOv8x models were employed in this project:

- **🔲 Quadrant Detection Model**: Identifies quadrants in the video to accurately map ball positions.
  
- **🏀 Ball Detection Model**: Detects balls, classifies their colors, and tracks their movements to log entry and exit events.

- **⚙️ Combined Model**: Integrates the above models using a cascading object detection approach for comprehensive detection and identification.

## **Links and Results:**

- **📔 Link to the Colab Notebook**: [CLICK HERE](https://colab.research.google.com/drive/1EGUlv8hCES5XOHuVv5tpenP1wSIR0ry1?usp=sharing)

### **🔍 Model Results:**

- **Confusion Matrices**
  - **Ball Detection Model**: 
    <div style="display: flex;">
      <div style="flex: 1; padding: 10px;">
        <h5>📊 Ball Detection Model</h5>
        <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/confusion_matrix(1).png" alt="Ball Detection Confusion Matrix" style="width: 100%; max-width: 300px;">
      </div>
      <div style="flex: 1; padding: 10px;">
        <h5>📊 Quadrant Detection Model</h5>
        <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/confusion_matrix.png" alt="Quadrant Detection Confusion Matrix" style="width: 100%; max-width: 300px;">
      </div>
    </div>

- **Label Analysis**
  - **Ball Detection Model**: 
    <div style="display: flex;">
      <div style="flex: 1; padding: 10px;">
        <h5>📈 Ball Detection Model</h5>
        <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/labels_correlogram(1).jpg" alt="Ball Detection Label Analysis" style="width: 100%; max-width: 300px;">
      </div>
      <div style="flex: 1; padding: 10px;">
        <h5>📈 Quadrant Detection Model</h5>
        <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/labels_correlogram.jpg" alt="Quadrant Detection Label Analysis" style="width: 100%; max-width: 300px;">
      </div>
    </div>

- **Detection Results**
  - **Ball Detection Model**: 
    <div style="display: flex;">
      <div style="flex: 1; padding: 10px;">
        <h5>🔍 Ball Detection Model</h5>
        <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/results(1).png" alt="Ball Detection Results" style="width: 100%; max-width: 300px;">
      </div>
      <div style="flex: 1; padding: 10px;">
        <h5>🔍 Quadrant Detection Model</h5>
        <img src="https://github.com/Anidipta/AI-Assignment/blob/main/Image/results.png" alt="Quadrant Detection Results" style="width: 100%; max-width: 300px;">
      </div>
    </div>

## **Output:**

### **🎬 Processed Video:**

- Tracks balls with color identification.
- Displays time stamps in the top left corner.
- Shows detection boxes with confidence levels.

- **🔗 Link to the Processed Video**: [CLICK HERE](https://drive.google.com/file/d/1c_EzHK5AWmWOBoT0Yf4Q2Zuz8NICl0Jl/view?usp=sharing)

- **🖼️ Demo Image Detected by the Model:**
  ![Demo Image](https://github.com/Anidipta/AI-Assignment/blob/main/demo%20image.png)

### **📄 Text File:**

- Records events with format: Time, Quadrant Number, Ball Color, Type (Entry or Exit).

- **🔗 Link to the TXT File**: [CLICK HERE](cleaned_result.txt)

## **Tools and Technologies Used:**

- **🧠 YOLOv8x** for advanced object detection.
- **🔧 OpenCV** for video processing.
- **🔢 NumPy** for efficient data manipulation.
- **📊 Pandas** for data management and analysis.
- **🐍 Python** for scripting and integration.
- **🔒 Kaggle** for storing videos and models.
- **🗂️ Roboflow** for dataset preparation (training, testing, and validation).

## **Challenges Faced:**

1. **🔄 Object Tracking and Identification**: Maintaining ball identity across frames despite occlusions and rapid movement.
2. **⏱️ Real-time Performance**: Processing each video frame in real-time while managing complex models.
3. **🎯 Accuracy of Detection**: Achieving high detection accuracy under varied lighting and backgrounds.
4. **🔄 State Management**: Correctly updating the state of balls while tracking multiple objects in dynamic scenes.

## **Usage Instructions:**

1. Clone the repository and navigate to the project directory.
2. Ensure all required packages are installed by running:

   ```bash
   pip install -r requirements.txt
   ```

3. Place your input video in the project directory.
4. Update the paths in the `process_video` function to point to your input video and desired output locations.
5. Run the Jupyter notebook to process the video and generate output files.
