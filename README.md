# OpenGesture

This is an algorithm that links 2 other algorithms (Openpose and ofxGVF) for gesture recognition.

While Openpose delivers a real-time human pose estimation, ofxGVF can instantaneously adapt and recognize the gesture input for 1 point (either 2D or 3D)

So far, this code doesn't do it in real-time. 

User may first read the video of interest with Openpose and save the .json files (from Openpose) for ulterior analyses of ofxGVF.

Files for templates are stored in the folder "openpose/output/coco/", while files for recognition should be stored in the folder "openpose/gesto/coco/".

Recording a gesture template:

as described in ofxGVF page, you may first choose the option for "recording" and then enter the name of the gesture you want to save as template. In this repository, examples coming from folders "openpose/output/coco/" + "braccia1x" are provided. 
Evidently, you can choose the names and paths to store these gestures...

Following (gesture to be recognized):

thi mode will make inference of the gesture you want to recognize. Again, you must specify the folder path with the .json files storing the gesture output by Openpose. In this repository, examples are given by the path "openpose/gesto/coco/" + "claudio/bracciaG/braccia1x" or + "riccardo/bracciaG/braccia1x".

Attention: you should alter the path for the directory in the main.cpp file. Otherwhise the algorithm will not find the .json files to read.

Also, the filesystem.hpp may need its whole path declared at the very beginning of the script:
#include <filesystem.hpp> // line 14

