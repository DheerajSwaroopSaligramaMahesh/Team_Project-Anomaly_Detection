# Multi-Camera AI Video Analytics with NVIDIA DeepStream 7.1

This project implements a **real-time multi-camera anomaly detection system** on the **NVIDIA Jetson Orin Nano** using the **DeepStream SDK 7.1**.  
It extends NVIDIA’s anomaly detection reference app to support **live Intel RealSense D455 cameras**, enabling scalable AI-powered video analytics at the edge.

---

## Features
- **Multi-camera support** using Intel RealSense D455
- **Real-time video analytics** at 1280×720 and 30 FPS
- **AI inference** via ResNet-18 anomaly detection model
- **Motion detection** using `dsdirection` plugin
- **Dual-view display** (raw + AI-processed outputs)
- **Automated shell scripts** for multi-camera setup, synchronization, and GStreamer previews
- **GPU benchmarking** with `jtop` on Jetson Orin Nano

---

## Project Structure
├── configs/ &nbsp;&nbsp;&nbsp;# DeepStream pipeline and model configs<br>
├── scripts/ &nbsp;&nbsp;&nbsp;&nbsp;# Shell scripts for automation<br>
├── models/ &nbsp;&nbsp;&nbsp;# ResNet-18 anomaly detection TensorRT engine<br>
├── src/ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Pipeline adaptation and plugin integration<br>
└── README.md &nbsp;&nbsp;&nbsp;# Project documentation<br>


---

## Requirements
- **Hardware**
  - NVIDIA Jetson Orin Nano
  - Intel RealSense D455 (x2)

- **Software**
  - JetPack (latest release for Orin Nano)
  - NVIDIA DeepStream SDK 7.1
  - GStreamer with `v4l2src`, `nvinfer`, `dsdirection`
  - CUDA 12.6
  - TensorRT
  - `jtop` (for benchmarking)

---

## How to Run
1. **Clone the repository**
   ```bash
   git clone https://github.com/DheerajSwaroopSaligramaMahesh/Team_Project-Anomaly_Detection.git

2. cd /opt/nvidia/deepstream/deepstream-7.1/sources/apps/sample_apps/Anomaly_Detection_Camera/deepstream_reference_apps/anomaly/apps/deepstream-anomaly-detection-test

3. sudo make

4. Please modify the camera inputs for the ./deepstream-anomaly-detection-app and gst-streamer, specify the correct sources
  
5. Run command: sh ./run_deepstream_anomaly_detection_app.sh


## Additional Resources

For more information, refer to the project report and included commands/scripts in this repository.

[Paper Link](https://github.com/DheerajSwaroopSaligramaMahesh/Team_Project-Anomaly_Detection/blob/main/Anomaly_Detection_Project/Nvidia_Multi-Cam_AI_Video_Analytics_Using_DeepStream_SDK_7.1.pdf)

[Report Link](https://github.com/DheerajSwaroopSaligramaMahesh/Team_Project-Anomaly_Detection/blob/main/Anomaly_Detection_Project/Report_Nvidia_Orin_Nano_ss25.pdf)

[Commands to run Link](https://github.com/DheerajSwaroopSaligramaMahesh/Team_Project-Anomaly_Detection/blob/main/Anomaly_Detection_Project/Commands.txt)
