# **Virtual Navigation Assistance System**

This project integrates **YOLOv11** for real-time object detection and **MiDaS** for depth estimation to create an intelligent pedestrian assistance system. The system identifies objects, calculates their depth, and provides real-time audio instructions to guide users safely in their walking environment.

-----
<div align="right">
  <img src="1.png" alt="Virtual Naviation Assistant" width="300"/>
</div>

## **Features**

1. **Trapezoid ROI**:
   - Focuses object detection and depth estimation on the walking area, ignoring irrelevant regions like the sky.

2. **Object Detection & Depth Estimation**:
   - Detects objects using YOLOv11 and calculates their distance using MiDaS.

3. **Interactive Audio Instructions**:
   - Provides spoken feedback such as:
     - "Path is clear."
     - "Obstacle ahead, move left."
     - "Immediate obstacle nearby, please stop!"

4. **Efficient Processing**:
   - Frames are resized to 15% of the original size for computational efficiency.

5. **Output Video**:
   - Annotated video with bounding boxes, depth values, and walking area overlays.
   - Audio instructions saved as MP3 files for playback.

-------

## **Planned Enhancements**

- **Interactive Audio Assistant**:
  - A conversational assistant to answer user queries.

- **Google Maps Integration**:
  - Dynamic path guidance and navigation.

- **Heygen Integration**:
  - Exploring enhanced interactivity features using Heygen.

-------

## **Setup Instructions**

### **Requirements**
- Python 3.8+
- Required libraries:
  - `torch`
  - `torchvision`
  - `opencv-python`
  - `numpy`
  - `gTTS`
  - `ultralytics`
  - `Pillow`

### **Installation**
1. Clone this repository:
   ```bash
   git clone https://github.com/SheemaMasood381/Virtual-Navigation-Assistance-Yolo11
   cd pedestrian-assistance-system

2. Install Dependencies

To set up the project environment, install the required dependencies:

```bash
pip install -r requirements.txt

### **Download the YOLOv11 Model Weights**

Place the `yolo11n.pt` file in the root directory of your project.

---

### **Usage**

#### **Run the System**
1. Add your video file to the project directory.

2. Update the `video_path` variable in the relevant Jupyter Notebook cell to point to your video file.

3. Execute the cells in the Jupyter Notebook sequentially.

4. The processed video with annotations will be saved as `processed_video.mp4`.

--------

### **Project Workflow**

#### **Preprocessing**
- Resizes the video to 15% of its original size.
- Applies a trapezoid mask to focus on the walking area.

#### **Object Detection**
- Uses YOLOv11 to detect and track objects within the trapezoid region.

#### **Depth Estimation**
- Uses MiDaS to estimate the depth of detected objects.

#### **Audio Instructions**
- Provides actionable instructions such as "Move left" or "Stop."

-------

### **Acknowledgments**

- **YOLOv11**: For robust object detection.
- **MiDaS**: For accurate depth estimation.
- **gTTS**: For generating real-time audio instructions.

-------

### **Contributing**

Contributions are welcome! Feel free to fork this repository, create a feature branch, and submit a pull request.

---

### **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.

