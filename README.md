# OBJECT-DETECTION-USING-YOLO
This project involves object detection and speed estimation using YOLO (You Only Look Once) model on a traffic video. Here are four key points:

1. **Object Detection**: Utilizes the YOLOv8 model to detect various objects (e.g., cars, trucks, buses) from a traffic video with specific confidence and IOU thresholds.
   
2. **Perspective Transformation**: Applies a custom view transformer to convert the detected objects' coordinates to a different perspective for more accurate speed estimation.

3. **Speed Estimation**: Tracks objects across frames using ByteTrack and calculates their speed in km/h based on positional changes over time.

4. **Video Processing and Playback**: Annotated results (bounding boxes, labels, traces) are rendered on the video, which is resized and played using Gradio for an interactive display.
