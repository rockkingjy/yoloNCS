# YOLO for Intel/Movidius Neural Compute Stick (NCS)

## Download Pretrained Caffe Models to ./weights/

* YOLO_tiny: https://drive.google.com/file/d/0Bzy9LxvTYIgKNFEzOEdaZ3U0Nms/view?usp=sharing

## Compilation

* Compile .prototxt and corresponding .caffemodel (with the same name) to get NCS graph file:
```
mvNCCompile prototxt/yolo_tiny_deploy.prototxt -w weights/yolo_tiny_deploy.caffemodel -s 12
```
* The compiled binary file "graph" has to be in main folder after this step.

## Single Image Script

* Run
```
python3 py_examples/yolo_example.py dog.jpg
```

## Camera Input Script

* Run 
```
python3 py_examples/object_detection_app.py
```
* Press "q" to exit app.

