# TTS


## Getting Started

colab 을 기반으로 경로 설정을 하였으니 경로에 주의해주세요. (colab 사용 권장) 

[colab notebook](https://colab.research.google.com/drive/1bsdjDcknb-jJrNeCVCm-IAVBRacumsYi#scrollTo=RHJFSi2vtEwi)


### Installing 

현 프로젝트에 필요한 모듈 설치

```
git clone https://github.com/sce-tts/g2pK.git
!pip install -q --no-cache-dir "konlpy" "jamo" "nltk" "python-mecab-ko"
!pip install -q --no-cache-dir -e 

git  https://github.com/sce-tts/TTS.git -b sce-tts
pip install -q --no-cache-dir -e 

```

Flask 환경 설정

```
pip3 install flask-ngrok flask_cors pyttsx3

```


## Running the tests 

Flask App 실행

```
python run.py
```



### 동작

Flask App 이 실행이 되면 연결 가능한 
로컬 호스트 주소/링크가 생성이 된다.

그 중 http://127.0.0.1:5000 -> 코랩 실행 시 연결 잘 안 되는 경우가 많음.

ngrok 주소로 들어가기를 권장 


