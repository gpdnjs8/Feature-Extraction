# Feature-Extraction 

## Introduction
PCA를 이용한 feature extraction을 whitening을 적용한 경우와 적용하지 않은 경우로 나누어 구현하고 비교한다.   
데이터셋 LWF(labeled faces in the world)를 이용해 feature extraction에 사용한다.   
Whitening을 적용한 경우와 적용하지 않은 경우로 나누어 구한 feature extraction을 이용해 KNN 모델을 학습시킨다. 그 후, 분류모델의 평가지표 중 하나인 f1 score를 이용해 두 KNN 분류 결과를 출력하여 비교한다.  

## Algorithm
1. PCA  
    - QR 분해 구현
    - Gram-schmidt process와 QR 분해
    - 고유값, 고유 벡터 추출
    - 상위 n개의 파라미터 추출
    - PCA with Whitening : PCA 적용 전에 데이터 자체를 평균을 빼고, 표준편차를 나누어 적용한다. 
2. KNN  
KNN은 지도학습에서 사용되는 분류 알고리즘 중 하나이다. K-최근접 이웃으로, 특정 데이터를 k개의 인접한 요소를 기반으로 예측한다. k값이 너무 작으면 과적합이 
될 수 있고 값이 너무 크면 과소적합이 될 수 있다. 데이터와 가장 가까운 k개의 이웃 데이터를 찾아 데이터의 클래스와 값을 예측한다.  