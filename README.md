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
<pre><code>python train.py --img 640 --batch 16 --epochs 20 --data ~/dataset/data.yaml --cfg ./models/yolov5s.yaml --weights yolov5s.pt --name yolov5_coco</code></pre>


#### Detection
<pre><code>python detect.py --source ./inference/images/ --weights runs/exp()/weights/best.pt --conf 0.5</code></pre>

--img : 이미지 크기
--batch : 배치 크기
--epochs : epoch 크기
--data : 데이터파일 (data.yaml 파일 경로 지정)
--cfg : 위에서 정한 모델 크기 (yolov5/models 폴더에 yaml파일로 저장되어 있음)
--weights : 미리 학습된 모델로 학습할 경우 (yolov5s.pt 등의 형식으로 다운로드 가능)
--name : 학습된 모델의 이름
