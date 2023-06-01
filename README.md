# opensw23-support

## Team Introduction
  
  > 박지원, 201812317, Everything
  
## Topic Introduction
  > PyTorch를 기반으로 MSG-Net 및 Neural Style을 구현해 원하는 그림의 스타일을 MSG-Net을 통해 학습하여 원하는 그림을 해당 스타일의 그림처럼 변경해 줄 수 있다.
  
  
## Results
  > ![output](https://github.com/parkji1on/opensw23-support/assets/103587652/0addbac1-cf7b-457d-ab0a-dcf97c9751e4)
  
## Analysis/Visualization


## Installation

### 프로젝트 가져오기
```
git clone https://github.com/parkji1on/PyTorch-Multi-Style-Transfer.git
```
원본
```
git clone https://github.com/zhanghang1989/PyTorch-Multi-Style-Transfer
```
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
cd PyTorch-Style-Transfer/experiments
bash models/download_model.sh
```
### 미리 학습된 모델을 통해 이미지 변경하기
```
python main.py eval --content-image images/content/venice-boat.jpg --style-image images/21styles/candy.jpg --model models/21styles.model --content-size 1024 --cuda=0
```

## Presentation
