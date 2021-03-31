# bolierplate_tensorflow2-yolov4


[![GitHub license](https://img.shields.io/github/license/vmMachineLearning/bolierplate_tensorflow2-yolov4)](https://github.com/vmMachineLearning/bolierplate_tensorflow2-yolov4/blob/main/LICENSE)

This repository provides a generic boilerplate for object detection and object counting applications. It contains files and directory in an organized manner which are must and needed for any future object detection projects using **YOLOv4** and **Tensorflow2** libraries. 

## Usage of files

### 1. Yaml files
The `.yaml` files namely `conda-cpu.yml` and `conda-gpu.yml` are used to store and add dependencies and modules which are required to facilitate the smooth running of the current project. **Anaconda** and **conda** distribution is must to run this projects because it facilitates the usage of GPU version with ease. However, requirements.txt for `pip` can also work.
### 2. data directory
The data directory contains various subdirectories and a **yolov4 wights file whose link is present in the yolov4Weights.txt file.** The file was very large so please do not push it directly into the repo.
**NOTE: Already added the `data/*.weights` in .gitignore to not push the file to repo.**
#### Subdirectories of data directory
##### 1. images
This folder will contain all the input images which needs to be recognized.
##### 2. videos
This folder will contain all the input videos which needs to be recognized.
##### 3. dataset
This folder will contain the dataset on which our tensorflow model trains. This folder currently contains `COCO` dataset. Please read [**this**](https://cocodataset.org/#home) for further information.
##### 4. classes
This folder will contain text files which indicates labels and details about the classes on which our model is trained. *for example: airplanes, person, cell-phone, chair, etc.*. For our case we only need **construction bricks.**
##### 5. anchors [TO BE UPDATED]
This folder is a must to have but currently I'm unaware about why it is being used. Will update once have the information.

### 3. Python files [TO BE UPDATED]
1. The `convert_tflite.py` file converts the trained tensorflow model to light version in order to use it for mobile and edge-devices.
2. The `detect_video.py` file is used to recognize and return the pattern from a video file.

## Getting started
---

##### conda[needs to be run in conda terminal]
```bash
# Tensorflow CPU
$ conda env create -f conda-cpu.yml
$ conda activate yolov4-cpu

# Tensorflow GPU
$ conda env create -f conda-gpu.yml
$ conda activate yolov4-gpu
```

### Concepts::
- Contour Detection
- Edge Dtection  

/*
* https://cv-tricks.com/opencv-dnn/edge-detection-hed/#:~:text=Edge%20detection%20is%20useful%20in,text%20analysis%20and%20many%20more.
* https://medium.com/analytics-vidhya/detecting-and-counting-objects-with-opencv-b0f59bc1e111
# https://stackoverflow.com/questions/55169645/square-detection-in-image 
Compact Prediction Tree
* https://stackoverflow.com/questions/53021082/recognizing-the-bricks-in-a-brick-wall
* https://stackoverflow.com/questions/55832414/extract-a-fixed-number-of-squares-from-an-image-with-python-opencv
* https://answers.opencv.org/question/224166/how-to-count-2d-grid-squares-using-python-and-opencv/
* https://stackoverflow.com/questions/59182827/how-to-get-the-cells-of-a-sudoku-grid-with-opencv

--to be seen--
https://medium.com/analytics-vidhya/introduction-to-computer-vision-opencv-in-python-fb722e805e8b
https://www.pyimagesearch.com/2015/04/20/sorting-contours-using-python-and-opencv/
----
*/
