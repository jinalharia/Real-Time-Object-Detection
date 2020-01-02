# Realtime Obejct Recognition

Realtime object recognition using the OpenCV dnn module + pretrained MobileNetSSD caffemodel.

[![Realtime object recognition](https://img.youtube.com/vi/LGUR4Rn_kWs/0.jpg)](https://www.youtube.com/watch?v=LGUR4Rn_kWs)

## Installation
All the dependencies can be installed using `pip`. Just use the following command from the root directory of the project.
```bash
pip3 install -r requirements.txt
```

## How to run this script?
There are two options for video source:

 * Webcam
 * Android device running IP Camera (https://play.google.com/store/apps/details?id=com.pas.webcam&hl=en)

To run the script using webcam as source :

```bash
python3 real_time_object_detection.py --prototxt MobileNetSSD_deploy.prototxt.txt --model MobileNetSSD_deploy.caffemodel --source webcam
```

To run the script using IP Webcam as source, open the `real_time_object_detection.py` and edit the following line to match your host :

```python
host = 'http://192.168.0.101:8080/'
```

Then to run the script using IP as source :

```bash
python3 real_time_object_detection.py --prototxt MobileNetSSD_deploy.prototxt.txt --model MobileNetSSD_deploy.caffemodel --source web
```

## Usage

To do object detection on an image

```python
python deep_learning_object_detection.py \
	--prototxt models/MobileNetSSD_deploy.prototxt.txt \
	--model models/MobileNetSSD_deploy.caffemodel --image images/example_06.jpg
```

For real time object detection:

```python
python real_time_object_detection.py \
	--prototxt MobileNetSSD_deploy.prototxt.txt \
	--model MobileNetSSD_deploy.caffemodel \
	--source webcam
```

For any questions, create an issue in this repository.
