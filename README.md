## Object Detection and Speed Estimation using YOLO

**Project Overview**

This project performs object detection and speed estimation on traffic videos using the YOLOv8 model. The primary goal is to identify various traffic objects (cars, trucks, buses) and estimate their speed by tracking their movement across frames. The final output includes annotated video playback with bounding boxes, labels, and traces for each detected object, displayed interactively using Gradio.

**Project Objectives**
- Object Detection: Detect and classify objects in traffic using the YOLOv8 model.
- Perspective Transformation: Apply a custom perspective transformation for accurate speed measurement.
- Speed Estimation: Track and calculate the speed of each object in km/h by analyzing frame-by-frame movement.
- Interactive Video Playback: Display annotated video results with bounding boxes, speed labels, and object traces using Gradio.

**Key Features**
- YOLOv8 Object Detection: Real-time detection of various traffic objects with configurable confidence and IOU thresholds.
- ByteTrack Tracking: Robust object tracking to maintain consistent identifiers across video frames.
- Perspective Adjustment: Custom transformation to alter the camera perspective and improve distance accuracy in speed calculations.
- Gradio-Based Video Playback: Interactive, resizable video playback with annotations, providing a user-friendly interface for real-time feedback.

**Requirements**
- Python 3.x
- Libraries:
   - YOLOv8: For object detection (installable via the ultralytics package)
   - OpenCV: For video processing and frame manipulations
   - ByteTrack: For object tracking across frames
   - NumPy: For numerical computations
   - Gradio: For interactive video playback

Additional libraries for data handling and transformations as needed
Install the required libraries with:

```bash
pip install ultralytics opencv-python numpy gradio
```

**Usage**
1. Clone the repository:

```bash
git clone <repository_url>
cd <repository_name>
```

2. Run the main script: Run the object detection and speed estimation pipeline on a video file by executing the main script:

```bash
python main.py --input <path_to_traffic_video> --confidence <value> --iou <value>
```

   - <path_to_traffic_video>: Path to the input video file.
   - --confidence: Minimum confidence threshold for object detection (e.g., 0.5).
   - --iou: Intersection-over-Union threshold for detection.

3. Interactive Playback: After processing, the video playback will appear in a Gradio interface with annotations.

**Key Components**
- YOLOv8 Model: Detects traffic objects in each video frame.
- Perspective Transformation: Alters object coordinates for accurate real-world measurement.
- ByteTrack: Maintains unique IDs for each object to calculate speed accurately.
- Annotated Video Output: Displays bounding boxes, labels, and speed annotations in an interactive Gradio interface.

**Notes**
- Adjust Confidence and IOU: Tune detection thresholds for optimal results in different traffic scenarios.
- Customization: Modify perspective transformation settings to adapt to different camera angles.

**License**
This project is licensed under the MIT License.
