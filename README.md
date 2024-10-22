Chest_Image_Segmentation
-----------------------
![스크린샷 2024-10-22 204553](https://github.com/user-attachments/assets/d0d25508-43ad-4925-86ef-f87e53e64e93)

U-Net 기법을 활용하여 COVID-19 관련 폐 질환의 이미지 세분화(Image Segmentation)를 구현한 코드입니다.

TensorFlow Dataset을 생성하여 의료 기반에 최적화된 U-Net 아키텍처 모델에 입력하도록 설계하였습니다.

프로젝트 소개
---
이 프로젝트는 환자의 X-ray 이미지를 지속적으로 세분화하여, 질병의 진행 상태를 추적하고 치료 반응을 평가하는데 사용하기위해서 만들었습니다.

주요 기능
-----
● 데이터 로딩 및 전처리 : COVID-19 관련 폐 질환 이미지를 OpenCV를 사용하여 로드하고 , RGB로 변환 후 , 해당 이미지와 관련된 마스크를 함께 저장

● 데이터 증강 : Tensorflow의 tf.keras.Sequential을 활용하여 랜덤 회전 및 수평 반전과 같은 데이터 증강 기법을 적용하여 모델의 일반화 성능을 향상

● Tensorflow 데이터셋 생성 : tf.data.Dataset API를 사용하여 이미지를 텐서플로우 데이터셋으로 변환하고, 전처리 및 증강 작업을 적용.

배치 처리와 데이터 프리패치를 통해 성능 최적화

● U-Net 모델 설계 : U-Net 아키텍처를 기반으로 한 모델을 정의. 인코더와 디코더 구조로 구성되어 있으며, 각 레이어에서 배치 정규화 및 활성화 함수를 사용하여 성능 개선

● 모델 컴파일 및 훈련 : Adam 옵티마이저와 크로스 엔트로피 손실 함수를 사용하여 모델을 컴파일.

조기 중단(Early Stopping)콜백을 설정하여 검증 손실이 개선되지 않을 경우 훈련 조기 종료

개발 환경
-----
● Google Colab : 클라우드 기반 Python 개발 환경으로 , GPU를 사용한 딥러닝 모델 학습에 사용

● Python : 주요 프로그래밍 언어로 사용

● Google Drive : 데이터를 저장하고 불러오는 파일 시스템으로 사용

기술 스택
----
● Tensorflow & Keras : 딥러닝 모델 구축 및 학습을 위해 사용. CNN 기반 모델과 데이터 증강 기법 사용

● OpenCV : 이미지 전처리 및 변환에 사용(이미지 파일 로드 및 색상 변환 등)

● Scikit-learn : 학습 데이터와 검증 데이터를 분리하는 데 사용 (train_test_split 함수)

● Matplotlib : 학습 과정에서의 정확도 및 손실 그래프 시각화

● tf.data API : Tensorflow 데이터셋 생성 및 배치 처리에 사용

● Data Augmentation : 랜덤 회전 , 수평 플립 , 대비 조정 등을 사용하여 데이터 증강

프로젝트 전체 과정
---
![image](https://github.com/user-attachments/assets/d8f79432-1519-4199-a93b-241d49e23de0)

