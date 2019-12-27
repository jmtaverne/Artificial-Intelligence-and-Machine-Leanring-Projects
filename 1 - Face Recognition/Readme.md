# Face recognition using Raspberry Pi and OpenCV

# Required Hardware
* Raspberry Pi 3/3B or 4
* Raspicam

# 1 Configuring your Raspberry Pi

1.1 Install OpenCV
To install OpenCV, please follow following tutorial: https://www.pyimagesearch.com/opencv-tutorials-resources-guides/. If you have OpenCV already installed, please continue to the next point. 


1.2 Install Virtual Environment (optional):
If you want to to work within a virtual environment, please make sure to activate it with 
```
workon <your env name>
```
Here is a good tutorial how to install a virtual environment: https://secondrobotics.com/installing-python-virtual-environment/

Please make sure you have Python installed within this virtual environment.


1.3 Install required libraries
Please install following libraries:
```
pip install dlib
pip install face_recognition
pip install imutils
```

# 2 Download Code 
2.1 Download this project repository
For downloading this project you have 2 options.
 - Download as .zip file and extract it
 - Download using terminal
 ```
 cd <your folder>
 git clone https://github.com/jmtaverne/Artificial-Intelligence-and-Machine-Leanring-Projects.git
 cd 1 - Face Recognition
 ```
 2.2 Project structure:
  * ```dataset/``` This directory should contain sub-directories for each person you would like your facial recognition system to recognize.
  * ```encode_faces.py``` This file will find faces in our dataset and encode them into 128-d vectors.
  * ```build_face_dataset.py``` This file will create images of you or the people you want to recognize. 
  * ```haarcascade_frontalface_default.xml``` In order to detect and localize faces in frames we rely on OpenCV’s pre-trained Haar cascade file.
  * ```pi_face_recognition.py``` This is our main execution script. This script is going to start the video stream as well as the face recognition. 
  
 # 3 Gather your faces dataset
 3.1 open your console / terminal and go to your project directory. 
 3.2 run ``` python3 build_face_dataset.py```
 The python script is going to ask you following two information:
   1. The path to the Haar cascade file on disk.
   2. The path to the output directory. Images of faces will be stored in this directory and I recommend that you name the directory after the name of the person. If your name is “John Smith”, you might place all images in dataset/john_smith .
   
# 4 Compute your face recognition embeddings
We will be using a deep neural network to compute a 128-d vector (i.e., a list of 128 floating point values) that will quantify each face in the dataset. 

4.1 open your console / terminal and go to your project directory. 
4.2 run ``` python3 encode_faces.py```

This will create your "encodings.pickle" file. 

# 5 Recognize faces in video streams on your Raspberry Pi
To start the video stream, which shows the recognized faces, please follow following steps. 

5.1 open your console / terminal and go to your project directory. 
5.2 run ``` python3 pi_face_recognition.py```

 
 
