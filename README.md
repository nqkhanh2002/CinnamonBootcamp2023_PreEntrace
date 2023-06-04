<a name="readme-top"></a>
<div align="center">
  <p align="center">
    <a href="https://www.youtube.com/channel/UCKaMI0RBxF26f6j0Q8RRyTw">View Demo</a>
    ·
    <a href="https://github.com/nqkhanh2002/CinnamonBootcamp2023_PreEntrace/issues">Report Bug</a>
    ·
    <a href="https://github.com/nqkhanh2002/CinnamonBootcamp2023_PreEntrace/pulls">Request Feature</a>
  </p>
</div>

<h1 align="center">LANE DETECTION APPLICATION IN SELF-DRIVING CAR</h1>

<div align="center">
  <img src="intro.gif" alt="Result Example" width="800px">
</div>

**Lane detection** is a computer vision task that involves identifying the boundaries of driving lanes in video or image scenes. The goal is to accurately locate and track the lane markings in real-time, even in challenging conditions such as low light, glare, or complex road layouts.

This repository develops a lane detection and tracking solution for self-driving cars. It is a crucial component of an autonomous driving system, ensuring safety and efficiency for the driver and passengers on the road.

# Project Structure
> **This is an English version and an improved repository based on [the original repository](https://github.com/nqkhanh2002/Lane-Detection-for-Self-Driving-Cars), which represents the previous research results and my independent work.**

# Pipline
The implementation problem consists of 3 parts:
1. Traditional image processing method
2. Deep Learning Method
3. Build a user interface (GUI) to deliver a quick demo application
------- 
## Traditional image processing method
1. Compute the camera calibration matrix and distortion coefficients.
2. Apply a distortion correction to raw images.
3. Apply a perspective transform to generate a “bird’s-eye view” of the image.
4. Use color transforms, gradients, etc., to create a thresholded binary image.
5. Detect lane pixels and fit to find the lane boundary.
6. Determine the curvature of the lane and vehicle position with respect to center.
7. Warp the detected lane boundaries back onto the original image and display information for ADAS System. Information displayed includes:
* LKAS: Lane Keeping Assist System with Vietnamese traffic signs
* LDWS: Lane Departure Warning System ((Not aiming to develop in this method but develop in Deep Learning method)
* Vehicle position from center
## Deep Learning Method
> **This method is still in development because I train the model on ONNX and TensorRT so I'm stuck with NVIDIA GPUs and I don't have time to solve this Pre-Entrance test.**
1. Lane Detector: Ultra Fast Lane Detection ([V1](https://github.com/cfzd/Ultra-Fast-Lane-Detection) & [V2](https://github.com/cfzd/Ultra-Fast-Lane-Detection-v2)) on backbone ResNet (18 & 34)
2. Vehicle Detector: [YOLOv8 (v8m & v8l)](https://github.com/ultralytics/ultralytics) [ONNX](https://github.com/ibaiGorordo/ONNX-YOLOv8-Object-Detection) 
## Build a user interface (GUI) to deliver a quick demo application

## Cách chạy chương trình
1. Cài đặt các thư viện cần thiết bằng lệnh sau:
```
pip install -r requirements.txt
```
2. Chạy chương trình bằng lệnh trong file command_pipline.txt
- main.py [--video] INPUT_PATH OUTPUT_PATH 

Trong đó tham số INPUT_PATH là đường dẫn đến video hoặc ảnh đầu vào, OUTPUT_PATH là đường dẫn đến video hoặc ảnh đầu ra, [--video] là tham số để chương trình biết INPUT_PATH là video hay ảnh.
- Ví dụ:
```
python Image_Processing/main.py --video Test_Video/video_test_01.mp4 Results/output_test_01.mp4
```
3. Báo cáo kỹ thuật trong file Report.pdf
4. [Link colab cho triển khai nhanh source code](https://colab.research.google.com/drive/1ymFbIRuQhlgN0u20zoaH9lyR3gm5emF0?usp=sharing)
