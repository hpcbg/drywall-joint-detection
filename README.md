# Drywall joint detection

Drywall joint detection is done by using two approaches. 

## Train and detect joints by splitting the image into tiles.
For easy demonstration, see the Google Colab version of the notebook.
https://drive.google.com/file/d/1DS7xbfMOcG4hd5qwytQzTbtdASre9lil/view?usp=sharing

The following code could be used for creating your own dataset.
https://github.com/hpcbg/crack-detection-opencv

## Using image segmentation techniques for the entire joint
For this approach YOLOv5 is used.

Download YOLOv5 and install the requirements.
https://github.com/ultralytics/yolov5

Export the dataset prepared using robotflow in "YOLO v5 PyTorch" format
https://universe.roboflow.com/defectdetection-w2xhs/drywall-joint-detection/dataset/3

```bash
python3 train.py --data data.yaml --weights yolov5s.pt --img 640
```