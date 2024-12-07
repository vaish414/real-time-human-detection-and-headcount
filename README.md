# Real-Time Human Detection and Headcount

## Overview
The **Real-Time Person Counting System** is designed to provide a robust and scalable solution for monitoring the number of individuals in a given space in real-time. With the growing need for smarter campus environments, this system offers an effective way to manage occupancy levels, enhance security, and optimize resource usage.

The project leverages advanced computer vision techniques, including YOLO (You Only Look Once), ResNet, and Optical Flow, to detect, classify, and track individuals in various environments, such as classrooms, laboratories, and open spaces. By integrating multiple methodologies, the system ensures high accuracy and adaptability to different scenarios, such as seated individuals in classrooms or individuals moving in real-time.

## Objectives
The primary objectives of the project include:
- Providing accurate, real-time headcount data for specific areas.
- Enhancing detection capabilities for seated or stationary individuals.
- Offering a scalable and adaptable solution for diverse room layouts and movement scenarios.
- Supporting smart campus initiatives by integrating with existing CCTV systems for efficient space and resource management.

## Features
1. **Real-Time Headcount Calculation**
   - Tracks the number of individuals present in specific areas.
   - Differentiates between individuals “inside” and “outside” based on virtual line segmentation.
   
2. **Dual-Method Approach**
   - **YOLO Virtual Line Tracking:** Simplifies headcounting in areas with straightforward movement patterns.
   - **Optical Flow with ResNet:** Enhances detection for seated or stationary individuals in complex layouts.
   
3. **Dynamic Tracking**
   - Adapts to both mobile and stationary individuals.
   - Provides consistent headcounts even in challenging scenarios like lecture halls or large open spaces.
   
4. **Scalable System**
   - Can be integrated into existing security or monitoring setups.
   - Suitable for various applications, including classrooms, laboratories, or event spaces.

## Methodology
The system employs two complementary methodologies to ensure robust detection and tracking:

### 1. Virtual Line Tracking with YOLO
- **YOLO (You Only Look Once):** A high-speed object detection algorithm that generates bounding boxes around detected individuals.
- **Virtual Line:** A reference line is drawn within the frame to classify individuals as “inside” or “outside.”
- **Headcount Calculation:** Tracks the movement of individuals across the line for accurate counting.

### 2. Optical Flow and ResNet for Enhanced Detection
- **Challenges Addressed:** YOLO struggles with detecting seated or minimally mobile individuals.
- **ResNet:** A convolutional neural network (CNN) model used for more reliable detection of stationary individuals.
- **Optical Flow:** Focuses on regions of movement within the frame, enhancing YOLO’s accuracy in detecting individuals in these areas.

## Tools and Technologies
- **Programming Language:** Python
- **Deep Learning Models:**
  - **YOLOv3:** Used for real-time object detection.
  - **ResNet:** Deployed for reliable image classification, especially for stationary individuals.
- **Computer Vision Techniques:**
  - **Optical Flow:** Tracks motion within the frame to identify regions of interest.
- **Libraries and Frameworks:**
  - **OpenCV:** For image processing and motion tracking.
  - **TensorFlow/Keras:** For training and implementing deep learning models.
  - **PyTorch:** As an alternative deep learning framework for experimentation.

## Results and Performance

### Evaluation Metrics:
- **Accuracy:** Headcount accuracy of up to 93% in controlled environments.
- **Stability:** Improved stability in headcounting for classrooms and single-entry spaces.

### Observations:
- The virtual line method works best in environments with single-entry/exit points.
- Optical Flow integration significantly enhances detection for seated or minimally mobile individuals.

## Limitations and Future Scope

### Limitations:
- **Inconsistent Tracking in Multi-Entry Rooms:** The virtual line method struggles with rooms having multiple entry/exit points.
- **Challenges with Rapid Movement:** YOLO’s performance may degrade with individuals moving quickly across the frame.
- **Hardware Dependency:** Real-time processing requires high-performance computing resources.

### Future Scope:
- **Interactive Dashboard:**
  - Develop a dashboard for live monitoring of occupancy levels.
  - Visualize movement patterns and trigger alerts for overcrowding.
- **Integration with Face Recognition:**
  - Enhance security by identifying individuals in real-time.
  - Support attendance tracking and access control systems.
- **Application in Smart Cities:**
  - Extend the system for use in public spaces, transportation hubs, and event management.

## Applications
- **Campus Management:**
  - Monitor classroom and laboratory occupancy.
  - Optimize space and resource utilization.
- **Security Enhancement:**
  - Detect unauthorized access or overcrowding.
  - Support surveillance systems in sensitive areas.
- **Event Management:**
  - Track audience numbers in real-time during events or gatherings.
- **Smart Cities:**
  - Enable real-time monitoring in urban environments, such as parks, stations, and malls.

## Contributors
This project was developed by a team of undergraduate students from the Department of Computer Science and Engineering at GSFC University, Vadodara:
- **Vaishnavi Dave**
- **Kareena Gangwani**
- **Megh Patel**

## References
1. Redmon, J., Divvala, S., Girshick, R., & Farhadi, A. (2016). *You Only Look Once: Unified, Real-Time Object Detection*. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2016.
2. He, K., Zhang, X., Ren, S., & Sun, J. (2015). *Deep Residual Learning for Image Recognition*.
