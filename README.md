# Human Pose Length Estimation Without a GPU

![frame_138](https://github.com/bring-nirachornkul/Human-Landmark-Measurement/assets/89494368/8ac0899c-28ab-4246-8712-f021bacbd4c5)

## Overview

This repository is part of an ongoing project aimed at estimating human body dimensions through pose landmarks. The focus is on calculating only the landmarks that are relevant for specific measurements like the length of the shoulder, upper arm, and so on. While the system is partially functional, work is still underway to refine various parameters for enhanced accuracy.

## Components

The repository is structured into two main programs:

### 1. Camera Calibration

This program is designed to calibrate your PC's webcam. It performs a series of tasks to estimate the intrinsic and extrinsic parameters of the camera. Specifically, it calculates the camera matrix, distortion coefficients, translation vectors (`tVector`), and rotation vectors (`rVector`). These calibration parameters are then saved into a single file for later use in measurements. The calibration process employs Zhang's method using a chessboard pattern.

### 2. Human Landmark Measurement

This program includes the following features:

- **Joint Angle Calculation:** Computes the angles between various joints to provide insights into the pose.
  
- **Landmark Mapping:** Remaps the original landmark indices based on the project's specific needs.
  
- **CSV Export:** Saves the coordinates of the landmarks into a CSV file for further analysis or record-keeping.
  
- **Distance Measurement:** Measures the distances between pairs of human landmarks. These distances are then used to estimate the lengths of body parts like the shoulders and upper arms.
  
- **Video Playback:** The program offers a feature to record and playback the pose estimation process.
  
- **Frame Capture:** Takes snapshots from the live video feed every six seconds and saves them as images.
  
- **Camera Calibration:** This feature is integrated to ensure accurate and consistent measurements. It employs Zhang's chessboard calibration method.

## Usage

### Prerequisites

1. **Install Required Libraries:** To install the necessary Python packages, run the following command:
    ```bash
    pip install -r requirements.txt
    ```

2. **Chessboard for Calibration:** You need to print a chessboard pattern for calibrating the camera. Below are the specifications for the chessboard pattern:

    - **Rows:** 8
    - **Columns:** 11
    - **Checker Width:** 20 mm
  
    You can generate a suitable chessboard pattern from this website: [Camera Calibration Pattern Generator](https://calib.io/pages/camera-calibration-pattern-generator)

### Running the Programs

1. **Camera Calibration:**
    - Run the `Calibrate_camera.py` program.
    - Make sure to update the input path in this file before running.
    
    This will generate a calibration file that will be used for pose estimation.

2. **Human Landmark Measurement:**
    - Run the `Human-Landmark-Measurement-V1.0` program.
    - Don't forget to update the input path in this file before running.
    
    The output images and data will be saved in the `output_image` folder.

> **Note:** The programs rely on camera calibration. Without a chessboard pattern, they will not function correctly.


## Requirements




Next mission : Find the estimate points of the movement. [point A to point B]
