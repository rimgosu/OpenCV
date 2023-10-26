![image](https://github.com/rimgosu/OpenCV/assets/120752098/aab33cb3-03a9-461b-b9eb-beb0c36dc3b8)


# OpenCV

### 10월 11일
- https://learnopencv.com/ : 프로젝트에 활용하기 좋은 다양한 코드 제공
- https://github.com/spmallick/learnopencv/tree/master/ : 파이토치로 된 좋은 예시 코드
- https://github.com/spmallick/learnopencv/blob/master/README.md?ck_subscriber_id=1390420859



### 10월 13일 

![image](https://github.com/rimgosu/OpenCV/assets/120752098/499562d3-5355-4eeb-bd6f-b4b68dda5dee)

#### Anaconda Prompt 환경설정
1. opencv 용 환경 설정
```
conda create -n opencv python=3.8
```
- conda create : 환경 만들겠다
- -n : opencv = opencv 이름의 환경을 만들겠다
- python : python 3.8 버전으로 환경 만들겠다

2. 만든 환경에 접속
- 기존 환경 : (base)
- 새로운 환경 : (opencv)
```
activate opencv
```

```
(base) c:\Users\newny> activate opencv
(opencv) c:\Users\newny>
```

3. 라이브러리 설치
```
pip install numpy pandas matplotlib scikit-learn opencv-python mediapipe jupyter
```


4. jupyter notebook 접속
```
jupyter notebook
```

5. 다음 경로에서 가상환경이 설치된 것을 볼 수 있다

![image](https://github.com/rimgosu/OpenCV/assets/120752098/07c0274d-e091-465e-ab63-d75f2a28d206)



### 10월 23일

> OPENCV_006_템플릿매칭.ipynb

> OPENCV_007_이미지합성하기.ipynb

- 만들어진 환경 확인하기

```
conda env list
```
```
(base) C:\Users\newny>conda env list
# conda environments:
#
base                  *  C:\ProgramData\anaconda3
opencv                   C:\Users\newny\.conda\envs\opencv
```


### 10월 24일 - 미디어파이프

#### 미디어파이프 - 얼굴 합성1
> OPENCV_008_Mediapipe.ipynb

![image](https://github.com/rimgosu/OpenCV/assets/120752098/1872f016-9a05-44b2-ba71-4dfb4b1b4a8e)

- [미디어파이프 공식 홈페이지](https://developers.google.com/mediapipe)
- [Face landmark detection guide](https://developers.google.com/mediapipe/solutions/vision/face_landmarker#get_started)
- 실습 mediapipe Version: 0.10.7

- 미디어 파이프 설치

```
pip install mediapipe
```

- 미디어파이프 불러오기

```
import mediapipe as mp
```



#### 미디어파이프 - 가위바위보

![image](https://github.com/rimgosu/OpenCV/assets/120752098/12e447e7-d869-4164-bb94-f0fc85cdfbaf)

> OPENCV_009_Mediapipe_Hand.ipynb
- <https://developers.google.com/mediapipe/solutions/vision/hand_landmarker#get_started>






### 10월 26일 - 객체 탐지의 역사

| 항목                     | One-Stage Detector 예: YOLO, SSD  | Two-Stage Detector 예: Faster R-CNN, R-CNN |
|------------------------|-----------------------------------|------------------------------------------|
| 속도                    | 빠름(30~50fps)                              | 상대적으로 느림(10~15fps)                          |
| 정확도                  | 상대적으로 낮음(0.7)                    | 높음(0.8)                                     |
| 복잡도                  | 단순                              | 복잡                                     |
| 작동 방식               | 이미지를 한 번에 분석             | 두 단계(Region Proposal, Classification)  |
| 메모리 사용량           | 일반적으로 적음                    | 높음                                     |
| 실시간 적용 가능성       | 높음                              | 낮음                                     |
| 하이퍼파라미터 조정 필요성 | 적음                            | 많음                                     |
| 입력 이미지 크기         | 고정된 크기 가능                    | 다양한 크기 가능                          |
| 사용 사례               | 실시간 객체 탐지, 임베디드 시스템  | 고품질 객체 탐지, 연구                   |

