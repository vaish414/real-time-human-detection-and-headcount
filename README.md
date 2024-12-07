\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage{hyperref}

\title{Real-Time Human Detection and Headcount}
\author{}
\date{}

\begin{document}

\maketitle

\section*{Overview}
The \textbf{Real-Time Person Counting System} is designed to provide a robust and scalable solution for monitoring the number of individuals in a given space in real-time. With the growing need for smarter campus environments, this system offers an effective way to manage occupancy levels, enhance security, and optimize resource usage.

The project leverages advanced computer vision techniques, including YOLO (You Only Look Once), ResNet, and Optical Flow, to detect, classify, and track individuals in various environments, such as classrooms, laboratories, and open spaces. By integrating multiple methodologies, the system ensures high accuracy and adaptability to different scenarios, such as seated individuals in classrooms or individuals moving in real-time.

\section*{Objectives}
The primary objectives of the project include:
\begin{itemize}
    \item Providing accurate, real-time headcount data for specific areas.
    \item Enhancing detection capabilities for seated or stationary individuals.
    \item Offering a scalable and adaptable solution for diverse room layouts and movement scenarios.
    \item Supporting smart campus initiatives by integrating with existing CCTV systems for efficient space and resource management.
\end{itemize}

\section*{Features}
\begin{enumerate}
    \item \textbf{Real-Time Headcount Calculation}
        \begin{itemize}
            \item Tracks the number of individuals present in specific areas.
            \item Differentiates between individuals \textquotedblleft inside\textquotedblright{} and \textquotedblleft outside\textquotedblright{} based on virtual line segmentation.
        \end{itemize}
    \item \textbf{Dual-Method Approach}
        \begin{itemize}
            \item \textbf{YOLO Virtual Line Tracking:} Simplifies headcounting in areas with straightforward movement patterns.
            \item \textbf{Optical Flow with ResNet:} Enhances detection for seated or stationary individuals in complex layouts.
        \end{itemize}
    \item \textbf{Dynamic Tracking}
        \begin{itemize}
            \item Adapts to both mobile and stationary individuals.
            \item Provides consistent headcounts even in challenging scenarios like lecture halls or large open spaces.
        \end{itemize}
    \item \textbf{Scalable System}
        \begin{itemize}
            \item Can be integrated into existing security or monitoring setups.
            \item Suitable for various applications, including classrooms, laboratories, or event spaces.
        \end{itemize}
\end{enumerate}

\section*{Methodology}
The system employs two complementary methodologies to ensure robust detection and tracking:

\subsection*{1. Virtual Line Tracking with YOLO}
\begin{itemize}
    \item \textbf{YOLO (You Only Look Once):} A high-speed object detection algorithm that generates bounding boxes around detected individuals.
    \item \textbf{Virtual Line:} A reference line is drawn within the frame to classify individuals as \textquotedblleft inside\textquotedblright{} or \textquotedblleft outside\textquotedblright{}.
    \item \textbf{Headcount Calculation:} Tracks the movement of individuals across the line for accurate counting.
\end{itemize}

\subsection*{2. Optical Flow and ResNet for Enhanced Detection}
\begin{itemize}
    \item \textbf{Challenges Addressed:} YOLO struggles with detecting seated or minimally mobile individuals.
    \item \textbf{ResNet:} A convolutional neural network (CNN) model used for more reliable detection of stationary individuals.
    \item \textbf{Optical Flow:} Focuses on regions of movement within the frame, enhancing YOLO’s accuracy in detecting individuals in these areas.
\end{itemize}

\section*{Tools and Technologies}
\begin{itemize}
    \item \textbf{Programming Language:} Python
    \item \textbf{Deep Learning Models:}
        \begin{itemize}
            \item \textbf{YOLOv3:} Used for real-time object detection.
            \item \textbf{ResNet:} Deployed for reliable image classification, especially for stationary individuals.
        \end{itemize}
    \item \textbf{Computer Vision Techniques:}
        \begin{itemize}
            \item \textbf{Optical Flow:} Tracks motion within the frame to identify regions of interest.
        \end{itemize}
    \item \textbf{Libraries and Frameworks:}
        \begin{itemize}
            \item \textbf{OpenCV:} For image processing and motion tracking.
            \item \textbf{TensorFlow/Keras:} For training and implementing deep learning models.
            \item \textbf{PyTorch:} As an alternative deep learning framework for experimentation.
        \end{itemize}
\end{itemize}

\section*{Results and Performance}
\subsection*{Evaluation Metrics:}
\begin{itemize}
    \item \textbf{Accuracy:} Headcount accuracy of up to 93\% in controlled environments.
    \item \textbf{Stability:} Improved stability in headcounting for classrooms and single-entry spaces.
\end{itemize}

\subsection*{Observations:}
\begin{itemize}
    \item The virtual line method works best in environments with single-entry/exit points.
    \item Optical Flow integration significantly enhances detection for seated or minimally mobile individuals.
\end{itemize}

\section*{Limitations and Future Scope}
\subsection*{Limitations}
\begin{itemize}
    \item \textbf{Inconsistent Tracking in Multi-Entry Rooms:} The virtual line method struggles with rooms having multiple entry/exit points.
    \item \textbf{Challenges with Rapid Movement:} YOLO’s performance may degrade with individuals moving quickly across the frame.
    \item \textbf{Hardware Dependency:} Real-time processing requires high-performance computing resources.
\end{itemize}

\subsection*{Future Scope}
\begin{itemize}
    \item \textbf{Interactive Dashboard:}
        \begin{itemize}
            \item Develop a dashboard for live monitoring of occupancy levels.
            \item Visualize movement patterns and trigger alerts for overcrowding.
        \end{itemize}
    \item \textbf{Integration with Face Recognition:}
        \begin{itemize}
            \item Enhance security by identifying individuals in real-time.
            \item Support attendance tracking and access control systems.
        \end{itemize}
    \item \textbf{Application in Smart Cities:}
        \begin{itemize}
            \item Extend the system for use in public spaces, transportation hubs, and event management.
        \end{itemize}
\end{itemize}

\section*{Applications}
\begin{itemize}
    \item \textbf{Campus Management:}
        \begin{itemize}
            \item Monitor classroom and laboratory occupancy.
            \item Optimize space and resource utilization.
        \end{itemize}
    \item \textbf{Security Enhancement:}
        \begin{itemize}
            \item Detect unauthorized access or overcrowding.
            \item Support surveillance systems in sensitive areas.
        \end{itemize}
    \item \textbf{Event Management:}
        \begin{itemize}
            \item Track audience numbers in real-time during events or gatherings.
        \end{itemize}
    \item \textbf{Smart Cities:}
        \begin{itemize}
            \item Enable real-time monitoring in urban environments, such as parks, stations, and malls.
        \end{itemize}
\end{itemize}

\section*{Contributors}
This project was developed by a team of undergraduate students from the Department of Computer Science and Engineering at GSFC University, Vadodara:
\begin{itemize}
    \item \textbf{Vaishnavi Dave}
    \item \textbf{Kareena Gangwani}
    \item \textbf{Megh Patel}
\end{itemize}

\section*{References}
\begin{enumerate}
    \item Redmon, J., Divvala, S., Girshick, R., \& Farhadi, A. (2016). \textit{You Only Look Once: Unified, Real-Time Object Detection}. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2016.
    \item He, K., Zhang, X., Ren, S., \& Sun, J. (2015). \textit{Deep Residual Learning for Image Recognition
