# yolov4-darknet-easyone
 YOLOv4 using darknet made Easy

## Introduction
This repository is a fork of [AlexeyAB/darknet](

## Installation
### Requirements
- [CUDA](https://developer.nvidia.com/cuda-downloads) >= 10.0
- [cuDNN](https://developer.nvidia.com/cudnn) >= 7.6.5
- [OpenCV](https://opencv.org/releases/) >= 3.4.0
- [CMake](https://cmake.org/download/) >= 3.12
- [Visual Studio](https://visualstudio.microsoft.com/downloads/) >= 2017 (Windows only)

### Clone the repository
```bash
git clone 
```

## Testing
### Download the pre-trained weights


### Run on webcam
```bash
./darknet detector demo cfg/coco.data weights/yolov4.cfg weights/yolov4-tiny.weights -c 0
```

### Run on video
```bash
./darknet detector demo cfg/coco.data weights/yolov4.cfg weights/yolov4-tiny.weights -c 0 -ext_output -dont_show <video file>
```

## Training
### Download the pre-trained weights
```bash
wget
```

### Download the COCO dataset
```bash
wget
```

### Train
```bash
./darknet detector train cfg/coco.data cfg/yolov4.cfg weights/yolov4.conv.137 -dont_show
```



# Installing OpenCv from Source in ubuntu 22.04

## Installing Dependencies

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install build-essential cmake unzip pkg-config
sudo apt-get install libjpeg-dev libpng-dev libtiff-dev
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
sudo apt-get install libxvidcore-dev libx264-dev
sudo apt-get install libgtk-3-dev
sudo apt-get install libatlas-base-dev gfortran
sudo apt-get install python3-dev
```

## Downloading OpenCV

```bash
cd ~
wget -O opencv.zip
wget -O opencv_contrib.zip
unzip opencv.zip
unzip opencv_contrib.zip
```

## Installing Python

```bash
sudo apt-get install python3-pip
pip3 install numpy
```

## Compiling OpenCV

```bash
cd ~/opencv-4.5.3/
mkdir build
cd build
cmake -D CMAKE_BUILD_TYPE=RELEASE \
    -D CMAKE_INSTALL_PREFIX=/usr/local \
    -D INSTALL_PYTHON_EXAMPLES=ON \
    -D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib-4.5.3/modules \
    -D BUILD_EXAMPLES=ON ..
```

## Installing OpenCV

```bash
make -j4
sudo make install
sudo ldconfig
```

## Testing OpenCV

```bash
python3
>>> import cv2
>>> cv2.__version__
'4.5.3'
```

