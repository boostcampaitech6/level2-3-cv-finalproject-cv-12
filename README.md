# 충돌 예측 시스템
### 단안 카메라로 실시간 충돌을 예측하는 알림 시스템

![Image20240325165755](https://github.com/boostcampaitech6/level2-3-cv-finalproject-cv-12/assets/149575938/9bdf61f5-9198-409b-95e4-34da1f51482d)

## 프로젝트 소개
### 배경
- 자율 주행 기술이 적용된 배달 로봇 등의 상용화로 깊이 추정 기술에 대한 수요가 급증하고 있음
- 기존 거리 추정은 Lidar 센서를 이용하여 가능하나 비용이 비쌈
- 길거리에서 촬영된 영상은 사람들의 얼굴이 나오기 때문에 데이터로써 활용되기 어려움
### 기대효과
- 단안 카메라 거리 측정 기술을 통한 안전 사고 방지
- 단안 카메라의 단점인 기상 악화 상황에서의 한계를 딥러닝을 이용해서 극복
- 비싼 Lidar 센서 대신 단안 카메라를 사용하여 비용 절감
- 영상속 사람들의 얼굴을 모자이크 처리하여 개인 초상권 침해 방지
## 팀원 구성 및 역할
|![Alt text](https://avatars.githubusercontent.com/u/149575938?v=4)|![Alt text](https://avatars.githubusercontent.com/u/90448406?v=4)|![Alt text](https://avatars.githubusercontent.com/u/109489851?v=4)|![Alt text](https://avatars.githubusercontent.com/u/56228633?v=4)|![Alt text](https://avatars.githubusercontent.com/u/83424878?v=4)|
| :--------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------:
|[김세진](https://github.com/Revabo)|[박혜나](https://github.com/heynapark)|[이동우](https://github.com/Dong-Uri)|[진민주](https://github.com/freenozero)|[허재영](https://github.com/jae-heo)|
|프론트엔드 개발 <br> 모델 개발 |모델 개발<br> 알고리즘 개발<br>|모델 개발 <br> 알고리즘 개발 <br>|모델 리서치 <br> 모델 개발 <br>|프론트엔드 개발 <br> 서버 개발 <br>|


## 사용 모델
![image](https://github.com/boostcampaitech6/level2-3-cv-finalproject-cv-12/assets/149575938/40abaac5-2d15-4da3-a366-0b23971196a0)

[YOLO World](https://github.com/AILab-CVC/YOLO-World)<br>
[Depth Anything](https://github.com/LiheYoung/Depth-Anything)


## 프로젝트 구조

```
{proj}
├── back
│   ├── logic
│   ├── pretrained_weights
│   ├── config.py
│   ├── server.py
│   └── requirements_server.txt
├── front
│   ├── common
│   ├── controller
│   ├── resources
│   ├── ui
│   ├── app.py
│   └── beep.mp3
├── model
│   ├── blur
│   ├── calc_depth.py
│   ├── calc_func.py
│   ├── frame_confusion.py
│   ├── inference.py
│   └── plot_dist.ipynb
└── README.md
```

![GuZo](https://github.com/boostcampaitech6/level2-3-cv-finalproject-cv-12/assets/109489851/a8aea2df-ce83-4200-a5c8-06c3dc1ff440)

## 성능 지표
### 절대거리
$$ MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 = 0.3071$$
### 얼굴 모자이크
<p>$$ Accuracy = {모자이크\ 된\ 얼굴\ 수 \over 등장한\ 얼굴이\ 나온\ 사람\ 수}\times 100\% = 82.85\% $$</p>

### 실시간성
$$ FPS = 30 $$

## 프로그램 사용법
각 back, front, model 레포지토리 README 참조

