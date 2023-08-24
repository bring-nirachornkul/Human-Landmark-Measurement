Human Pose Length Estimation Without a GPU
Overview
This repository is part of an ongoing project aimed at estimating human body dimensions through pose landmarks. The project focuses on calculating only the landmarks relevant to specific measurements like the length of the shoulder, upper arm, and so on. While the system is partially functional, work is still underway to refine various parameters for enhanced accuracy.

Components
The repository is structured into two primary programs:

1. Camera Calibration
This program is used to calibrate the PC webcam. It performs a series of tasks to estimate the intrinsic and extrinsic parameters of the camera. Specifically, the program calculates the camera matrix, distortion coefficients, translation vectors (tVector), and rotation vectors (rVector). These calibration parameters are then saved into a single file for later use in measurements. The calibration uses the chessboard method proposed by Zhang.

2. Human Landmark Measurement
This program includes the following features:

Joint Angle Calculation: Compute the angles between various joints to gain insights into the pose.

Landmark Mapping: Remaps the original landmark indices as per the project's specific requirements.

CSV Export: Saves the landmark coordinates into a CSV file for further analysis or record-keeping.

Distance Measurement: Measures the distance between pairs of human landmarks. These distances are then used to estimate body part lengths such as shoulder width and upper arm length.

Video Playback: Allows you to record and playback the pose estimation process.

Frame Capture: Takes snapshots from the live video feed every six seconds and saves them as images.

Camera Calibration: This feature is integrated to ensure precise and consistent measurement. It employs Zhang's chessboard calibration method used in the first program.
![frame_138](https://github.com/bring-nirachornkul/Human-Landmark-Measurement/assets/89494368/8ac0899c-28ab-4246-8712-f021bacbd4c5)

This repo contains two programs :
i) Camera calibrate - this program will 

ii) 

iii) 

[Video](https://youtu.be/YNoQ9oRRBbg)


Next mission : Find the estimate points of the movement. [point A to point B]
