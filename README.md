# caffe-yolov2

## Reference

> YOLO9000: Better, Faster, Stronger

> http://pjreddie.com/yolo9000/

> https://github.com/yeahkun/caffe-yolo

> https://github.com/hustzxd/z0

> https://github.com/hustzxd/z1

> https://github.com/weiliu89/caffe.git

## modifications

1. add reorg_layer

2. convert yolo weights to caffemodel

3. add detection output layer

4. add detection evaluate layer

## Usage

1. create yolo.prototxt

   Use the yolo.prototxt provided in the folder, which correspond to the yolov2.cfg version of the darknet webpage.

2. Download the weights from the official darknet page. To work with the previous prototxt, download the YOLOv2 608x608 weights.

3. convert yolo weights to caffemodel

   Use the convert_weights_to_caffemodel.py script:
  
   python convert_weights_to_caffemodel.py yolo.prototxt yolo.weights yolo.caffemodel

4. Test the model on images using the yolo_detect.py script:
   
   python yolo_detect.py yolo.prototxt ./caffemodel/yolo.caffemodel ./images/img.jpg
   
## Results

![alt text](https://raw.githubusercontent.com/Serge3006/caffe-yolov2/yolo_detection.png)
