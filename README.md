## Guide

1. Download YOLOv3 weights from [YOLO website](http://pjreddie.com/darknet/yolo/).
2. Convert the Darknet YOLO model to a Keras model.
3. Run YOLO detection.

```
wget https://pjreddie.com/media/files/yolov3.weights
python convert.py -w yolov3.cfg yolov3.weights model_data/yolo_weights.h5
python yolo.py   OR   python yolo_video.py [video_path] [output_path(optional)]
```
## Choice of Anchor Boxes

YOLO v3, in total uses 9 anchor boxes. Three for each scale. If training YOLO on your own dataset, you should go about using K-Means clustering to generate 9 anchors.

Then, arrange the anchors is descending order of dimensions. Assign the three biggest anchors for the first scale , the next three for the second scale, and the last three for the third.

