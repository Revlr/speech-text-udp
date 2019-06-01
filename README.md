1. Cloud Speech API key  발급

https://console.cloud.google.com/apis/dashboard 에서 API 키를 발급 받아야 한다.

대시보드 >프로젝트 만들기 >만들기 > 프로젝트 이름을 설정 후 만들기

API 및 서비스 사용 설정 > "Cloud Speech API" 검색 후 선택 > 사용 설정

사용자 인증 정보 > 사용자 인증 정보 만들기 > 서비스 계정 키 > 서비스 계정을 새 서비스 계정으로 선택 > 서비스 계정 이름 입력 후 역할은 프로젝트에 소유자로 > 키 유형은 json으로 하고 생성

시스템 환경 변수에 OOGLE_APPLICATION_CREDENTIALS로  C:\Users\사용자이름\Downloads\서비스계정키이름.json을 등록



2. Cloud SDK 설치

https://cloud.google.com/sdk 에서  Google Cloud SDK installer 다운 후 설치 (옵션 변경 없이 next만 쭉)

설치 후 명령창이 실행되는데 Y 누르고 웹브라우저 나오면 허용 누르고 다시 명령창에서 사용 할 프로젝트 선택 



3.  파이썬 

python 3.7을 제외한 버전에서

> pip install virtualenv

> pip install virtualenvwrapper-win

후에 디렉토리를 생성 후 그 디렉토리에서 가상 환경을 만들어 준다

> .\env\Scripts\activate

> pip install --upgrade google-cloud-storage

> pip install google-cloud-speech

> gcloud auth activate-service-account --key-file="C:\Users\사용자이름\Downloads\키파일 이름"

> pip install pyaudio         --> 파이썬 버전 때문에 고생할 수 있으니 버전 체크를 꼭 하자...





이제 모든 준비가 끝났고 소스코드를 가상 환경 안에서 실행시키면 된다.
