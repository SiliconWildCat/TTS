# TextToSpeech


## Getting Started

1. colab 을 기반으로 경로 설정을 하였으니 경로에 주의해주세요. (colab 사용 권장) 
2. model.zip 다운 받아 colab에 올려놓아야 합니다.
3. 앞서 처음에 보여드렸을 때는 say it 버튼을 누르면 소리가 나오도록 하였는데 현재 버전은 wav 파일이 results.wav로 저장되도록 
   코드를 수정하였습니다.   
4. 로컬에서 사용 시 config.json, inference.py, run.py 내 경로 설정을 체크해주세요!!!! >> 중요
 
>> [colab notebook](https://colab.research.google.com/gist/thfla1105/f36e94bc7efdda7fd9d67479eb6e430d/tts-web-service-git.ipynb)


### Installing 

현 프로젝트에 필요한 모듈 설치

```
%cd /content/TTS/g2pK
git clone https://github.com/sce-tts/g2pK.git
!pip install -q --no-cache-dir "konlpy" "jamo" "nltk" "python-mecab-ko"
!pip install -q --no-cache-dir -e 
%cd /content/TTS/TTS
git  https://github.com/sce-tts/TTS.git -b sce-tts
pip install -q --no-cache-dir -e 

```

Flask 환경 설정

```
pip3 install flask-ngrok flask_cors pyttsx3
```

### Model Upload

new!! 모델 경로 수정 없이 run.py 해주시면 됩니다!
_다운받은 model.zip을 colab에 올려 놓은 뒤

```
unzip model.zip
```

압축 해제 한 후 파일 옮기기

best_model.pth.tar -> TTS/glowtts-v2 로 이동 

best_model_372791.pth.tar-> TTS/hifigan-v2로 이동

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


