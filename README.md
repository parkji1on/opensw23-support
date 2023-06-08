# opensw23-support

## Team Introduction
  
  > 박지원, 201812317, Everything
  
## Topic Introduction
  > PyTorch를 기반으로 MSG-Net 및 Neural Style을 구현해 원하는 그림의 스타일을 MSG-Net을 통해 학습하여 원하는 그림을 해당 스타일의 그림처럼 변경해 줄 수 있다.
  
  input
  
    1. --content-image : 다른 스타일로 그림을 변경하고 싶은 이미지 파일 1개
    
    2. --style-image : 원하는 스타일의 이미지 파일 1개
    
    3. --model : 원하는 스타일로 변경을 도와주는 학습된 모델

  output
  
    --style-image의 스타일 같이 변경된 --content-image의 이미지 파일 (output.jpg)
  
  
## Results

  > ![background4](https://github.com/parkji1on/opensw23-support/assets/103587652/276d246d-614d-4373-a606-1309580b0617)
  > ![background4_output](https://github.com/parkji1on/opensw23-support/assets/103587652/e0f77217-d474-4748-8aec-966ac429871c)
  > ![error1](https://github.com/parkji1on/opensw23-support/assets/103587652/313f784b-1a52-49c4-85bd-5d396eff4e5c)
  > ![error1_output](https://github.com/parkji1on/opensw23-support/assets/103587652/2a3c86e4-069e-49c3-899d-5e25fee8c624)
  > ![background3](https://github.com/parkji1on/opensw23-support/assets/103587652/57c86f3f-e63d-43f0-a51f-72b1e9757d06)
  > ![background3_output](https://github.com/parkji1on/opensw23-support/assets/103587652/f881ec7b-1061-424d-8157-b5d5f173e2bf)
  > ![background6](https://github.com/parkji1on/opensw23-support/assets/103587652/5433e328-0747-42ae-81b9-d0c850f36d6b)
  > ![background6_output](https://github.com/parkji1on/opensw23-support/assets/103587652/b439d636-2deb-480a-99c5-fdd61d03ca99)


## Analysis/Visualization
  > ![content_output](https://github.com/parkji1on/opensw23-support/assets/103587652/03bf994c-03a7-4a16-a1cb-000f51bf7709)
  > ![model_output](https://github.com/parkji1on/opensw23-support/assets/103587652/f4c2ed5e-a33d-4779-886e-4d418c093148)

사진별로, 모델별로 시간이 다르게 걸리는 것을 보고 한번 이를 측정해 보았습니다.
서로 같은 화풍으로 다른 사진을 변환한 결과는 차이가 많이 났습니다. 첫번째 그림이 이에 대한 결과입니다. 약간의 오차는 있었지만 대체로 사진의 크기가 큰 사진은 오래 걸리고 사진의 크기가 작은 사진은 적게 걸렸습니다.
  (x축 : 사진의 이름 , 빨간선 : 사진의 크기, 파란선 : 변환하는데 걸리는 시간)
서로 다른 화풍으로 같은 사진을 변환해 본것은 두번째 사진입니다. 이때에는 시간은 일정하게 나타나는 것을 볼 수 있습니다.
  (x축 : 화풍의 그림 이름, 빨간선 : 화풍 그림의 크기, 파란선 : 변환하는데 걸리는 시간)
  

## Installation

  > ![순서도](https://github.com/parkji1on/opensw23-support/assets/103587652/2fbb2803-44e0-4d2c-8b99-3c440efbfb03)

### 프로젝트 가져오기
```
git clone https://github.com/parkji1on/opensw23-support.git
```
원본
```
git clone https://github.com/zhanghang1989/PyTorch-Multi-Style-Transfer
```
### 개발자의 환경
Macbook Pro
mac OS 13.0.1(22A400)
프로세서 2.3 GHz 8코어 Intel Core i9
### 필요한 라이브러리 설치
```
numpy==1.21.0
opencv_python==4.2.0.32
Pillow==9.0.1
torch==1.5.0
torchfile==0.1.0
torchvision==0.6.0a0+82fd1c8
tqdm==4.62.3
```
```
pip install (필요한 라이브러리)
```
### 이미 학습된 모델 가져오기
```
cd opensw23-support/experiments
bash models/download_model.sh
```
### 미리 학습된 모델을 통해 이미지 변경하기
experiments 파일안에서 실행하기!
```
python main.py eval --content-image images/content/venice-boat.jpg --style-image images/21styles/candy.jpg --model models/21styles.model --content-size 1024 --cuda=0
```
결과 파일은 experiments 파일안에 output.jpg로 저장되어 있음

## Presentation

https://youtu.be/tM-T7UYBu0Y
