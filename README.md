# YOLO_V8_Object_Detection
This is only for NVIDIA Jetson NANO

Here's a comprehensive `README.md` file based on the report and additional instructions for adding a video link.

### README.md

```markdown
# YOLOv8 Object Detection on Jetson Nano

This project demonstrates the implementation of YOLOv8 for real-time object detection on the Jetson Nano.

## Author
**Darshan Anand**  
Pre-final Year CSE-AIML Student  
Dayananda Sagar University  
Email: darshananand004@gmail.com  

## Installation Steps

1. **Install Jetpack 4.6 on Jetson Nano**  
   Ensure Jetpack 4.6 (L4T 32.6.1) is installed on the Jetson Nano.

2. **Update and Install Dependencies**  
   Open a terminal and run the following commands:
   ```bash
   sudo apt update
   sudo apt install -y python3.8 python3.8-venv python3.8-dev python3-pip \
   libopenmpi-dev libomp-dev libopenblas-dev libblas-dev libeigen3-dev libcublas-dev
   ```

3. **Clone the YOLOv8 Repository**  
   ```bash
   git clone https://github.com/ultralytics/ultralytics
   cd ultralytics
   ```

4. **Create and Activate a Python 3.8 Virtual Environment**  
   ```bash
   python3.8 -m venv venv
   source venv/bin/activate
   ```

5. **Update Python Packages**  
   ```bash
   pip install -U pip wheel gdown
   ```

6. **Download and Install Pre-built PyTorch and TorchVision Packages**  
   ```bash
   # PyTorch 1.11.0
   gdown https://drive.google.com/uc?id=1hs9HM0XJ2LPFghcn7ZMOs5qu5HexPXwM
   # TorchVision 0.12.0
   gdown https://drive.google.com/uc?id=1m0d8ruUY8RvCP9eVjZw4Nc8LAwM8yuGV
   python3.8 -m pip install torch-*.whl torchvision-*.whl
   ```

7. **Install YOLOv8 Python Package**  
   ```bash
   pip install .
   ```

8. **Execute Object Detection**  
   ```bash
   yolo task=detect mode=predict model=yolov8n.pt source=0 show=True
   yolo task=segment mode=predict model=yolov8n-seg.pt source=0 show=True
   ```

## Observations and Results

### Object Detection Output 1
![Output 1](![image](https://github.com/DarshanAnand007/YOLO_V8_Object_Detection/assets/93935699/39266898-4351-448c-9e9a-7604062ec0bc)
)  
480x640 1 person, 170.5ms ...

### Object Detection Output 3
![Output 3](![image](https://github.com/DarshanAnand007/YOLO_V8_Object_Detection/assets/93935699/4bcbd9d8-94ad-4232-b3ac-e974689fd92e)
)  
480x640 1 person, 163.8ms ...


## Performance Metrics

The YOLOv8 model achieved the following FPS (frames per second) on the Jetson Nano for object detection and segmentation tasks:

| Model    | Detect FPS | Segment FPS |
|----------|------------|-------------|
| yolov8n  | 6.1        | 4.2         |
| yolov8s  | 3.1        | 2.2         |
| yolov8m  | 1.3        | 0.96        |
| yolov8l  | 0.77       | 0.61        |
| yolov8x  | 0.48       | 0.38        |

## Conclusion

The project successfully demonstrated the implementation of YOLOv8 for real-time object detection on the Jetson Nano. The setup and installation were straightforward, and the model performed adequately given the hardware constraints of the Jetson Nano.

YOLOv8, which stands for You Only Look Once version 8, is the latest iteration of a series of models known for their speed and accuracy in object detection tasks. It builds upon the successes of its predecessors by incorporating more advanced techniques and optimizations, making it a suitable choice for real-time applications on resource-constrained devices like the Jetson Nano.

One of the primary challenges encountered during this project was managing the limited computational resources of the Jetson Nano. Despite this, YOLOv8 performed remarkably well, achieving a respectable frame rate that would be sufficient for many real-time applications. This speaks volumes about the efficiency of the YOLOv8 architecture.

Future improvements to this project could include further optimization of the YOLOv8 model for the Jetson Nano. This could involve techniques such as model pruning and quantization to reduce the model size and increase inference speed. Additionally, exploring other versions of YOLOv8 (like yolov8s, yolov8m, yolov8l, and yolov8x) could provide insights into the trade-offs between speed and accuracy.

Another potential area of exploration is integrating YOLOv8 with other sensors and systems on the Jetson Nano. For instance, combining YOLOv8 with depth sensors could enhance object detection capabilities by providing additional context about the environment. Similarly, integrating with robotic systems could enable autonomous navigation and interaction based on real-time object detection.

Overall, this project demonstrates the viability of deploying advanced AI models on edge devices, opening up numerous possibilities for real-time, on-device intelligence in various applications.

## Video Demonstration

For a video demonstration of this project, please watch [this video](https://youtu.be/your_video_link).

## Contact

**Darshan Anand**  
Email: darshananand004@gmail.com  
Dayananda Sagar University  
CSE - AIML Pre-final Year Student
```

### Adding a Video Link

To add a video link that plays directly within your GitHub `README.md`, you can use an embedded YouTube link. Here’s how to do it:

1. Upload your video to YouTube or Google Drive.
2. Copy the video link.
3. Replace `https://youtu.be/your_video_link` in the `README.md` file with your actual video link.

If you're using Google Drive, make sure the link is set to public and anyone with the link can view the video. Use the following format for embedding a YouTube video:

```markdown
For a video demonstration of this project, please watch [this video](https://youtu.be/your_video_link).
```

If you follow these steps, your `README.md` will be comprehensive and include all necessary information for others to replicate your project. You can then push this `README.md` along with other project files to your GitHub repository.
