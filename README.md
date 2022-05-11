# Yolov5-Custom-Training

#### YoloV5 다운 : <https://github.com/ultralytics/yolov5>
#### Annotation Tool labelme : <https://github.com/wkentaro/labelme>

#### 디렉토리 구조
yoloV5 폴더 안에 coco128 폴더 생성

#### 본인 PC 기준
* yoloV5
  - coco128
    + images
      + train2017
    + labels
      + train2017    
    
    
#### 공식 디렉토리 구조 
* yoloV5
* data
    - images
      + train
      + valid
    - labels
      + train
      + valid
      

####  coco128.yaml 수정
* data
    - coco128.yaml -> detection 할 객체로 수정

<img src="https://user-images.githubusercontent.com/49273782/167886115-5f422531-6ecd-4f1b-bc42-0097096f0dd7.png" width="500" height="250">

#### Training
<pre><code>python train.py --img 640 --batch 8 --epochs 50 --data=C:/Users/MSDL-DESK-02/yolov5/data/custom.yaml --cfg=C:/Users/MSDL-DESK-02/yolov5/models/yolov5s.yaml --device 0</code></pre>


