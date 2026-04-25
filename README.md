Object Detection + Distance Estimation for Robotics Navigation - Satyam Shinde

## Candidate
Satyam Shinde

## Overview
Built a robotics perception pipeline using YOLOv8 for object detection and monocular distance estimation from camera images.

The system detects navigation-relevant objects such as cones, barriers, stop signs, and vehicles, then estimates approximate distance from the robot camera view.

The model was further optimized for edge deployment using ONNX export and INT8 quantization.

---

## Dataset

- Primary Dataset: BDD100K
- Transfer learning performed using pretrained YOLOv8 model

---

## Features

- Object detection using YOLOv8
- Bounding box annotation with confidence score
- Monocular distance estimation
- ONNX export for deployment
- INT8 quantization for edge devices
- CPU benchmarking

---

## Distance Estimation Method

Used geometric approximation:

distance = (real_object_height × focal_length) / bounding_box_pixel_height

This provides approximate real-world distance from a single camera.

---

## Benchmark Results

| Variant | Size (MB) | FPS | Latency (ms) |
|---|---:|---:|---:|
| PyTorch FP32 (CPU) | 6.55 | 5.46 | 183.27 |
| ONNX FP32 (CPU) | 12.85 | 5.86 | 170.72 |
| ONNX INT8 (CPU) | 3.50 | 3.85 | 259.92 |

---

## Optimization Summary

- Exported model to ONNX
- Applied INT8 dynamic quantization
- Reduced model size from 12.85 MB to 3.50 MB
- Suitable for edge deployment

---

## Sample Outputs

See images in `docs/deliverables/demo_images/`

---

## Project Structure

```text
README.md
eric_robotics_assignment.ipynb
docs/
src/
configs/




## Contact Information

- Name: Satyam Shinde
- GitHub Username: SatyamShinde77
- Contact Number: 9529902376
- Email Address: satyamshinde56@gmail.com