                                                          GUIDE

1. Download YOLOv3 weights from YOLO website.                  wget https://pjreddie.com/media/files/yolov3.weights
2. Convert the Darknet YOLO model to a Keras model.            python convert.py yolov3.cfg yolov3.weights model_data/yolo.h5
3. Run YOLO detection.                       python yolo.py     OR     python yolo_video.py [video_path] [output_path(optional)
