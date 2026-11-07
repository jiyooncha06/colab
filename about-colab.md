Google Colab(구글 코랩) 개념 정리
1. Google Colab이란?
**Google Colab(Google Colaboratory)**은 구글에서 제공하는 클라우드 기반의 프로그래밍 개발 환경이다.

웹 브라우저에서 별도의 프로그램 설치 없이 Python 코드를 작성하고 실행할 수 있으며, Google Drive와 연동하여 파일을 저장하고 공유할 수 있다.
주요 특징
- 클라우드 기반: 개인 컴퓨터가 아닌 구글에서 제공하는 서버에서 코드를 실행한다.
- 설치 불필요: 웹 브라우저만 있으면 Python 프로그래밍이 가능하다.
- 무료 사용 가능: 무료로 CPU와 제한적인 GPU 및 TPU 자원을 이용할 수 있다.
- 자동 저장: 기본적으로 Google Drive에 노트북이 저장된다.
- 협업 가능: 다른 사용자와 코드를 공유하고 공동으로 편집할 수 있다.
- 라이브러리 지원: NumPy, Pandas, Matplotlib 등 다양한 Python 라이브러리를 사용할 수 있다.
  
2. Google Colab의 기본 구조
Google Colab은 Jupyter Notebook을 기반으로 하며, 하나의 노트북 파일은 여러 개의 셀(Cell)로 구성된다.
구성 요소	설명
노트북(Notebook)	코드와 설명을 함께 저장하는 문서
코드 셀(Code Cell)	Python 코드를 작성하고 실행하는 공간
텍스트 셀(Text Cell)	Markdown을 사용하여 설명과 필기를 작성하는 공간
런타임(Runtime)	Python 코드가 실제로 실행되는 환경
출력(Output)	코드 실행 결과가 표시되는 영역


코드 셀과 텍스트 셀의 차이
① 코드 셀: Python 코드를 작성하고 실행한다.
a = 10
b = 20
print(a + b)
실행 결과:
30
② 텍스트 셀: Markdown 문법으로 학습 내용을 정리한다.
# Python 기초
## 변수
**변수**는 데이터를 저장하는 공간이다.


3. Google Colab의 주요 기능
① Python 코드 실행
코드 셀에 Python 코드를 입력한 뒤 Shift + Enter를 누르면 실행된다.
② 라이브러리 사용
다양한 라이브러리를 불러와 데이터 분석, 시각화, 인공지능 개발 등에 활용할 수 있다.
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
③ 파일 업로드 및 활용
컴퓨터에 저장된 파일을 Colab에 업로드하거나 Google Drive에 저장된 파일을 불러올 수 있다.
from google.colab import drive
drive.mount('/content/drive')
위 코드는 Google Drive를 Colab 실행 환경에 연결하는 코드이다. 실행 후 계정 인증이 필요할 수 있다.
④ GPU 및 TPU 활용
GPU와 TPU를 사용하여 머신러닝이나 딥러닝 연산을 가속할 수 있다.

설정 방법: 런타임 → 런타임 유형 변경 → 하드웨어 가속기 선택

단, 무료 계정에서는 사용 가능 시간과 자원에 제한이 있다.
  
4. Google Colab과 일반 Python 개발 환경의 차이
구분	Google Colab	VS Code / PyCharm
설치	불필요	일반적으로 필요
실행 환경	클라우드 서버	주로 개인 컴퓨터
인터넷	필요	로컬 실행 시 불필요
파일 형식	.ipynb	주로 .py
GPU 사용	구글 서버 자원 활용 가능	로컬 또는 별도 서버 설정
주요 용도	학습, 데이터 분석, AI	일반 프로그램 및 프로젝트 개발


5. Google Colab과 GitHub 연동
Google Colab에서 작성한 코드는 GitHub에 저장하여 버전 관리와 학습 기록에 활용할 수 있다.

Colab(코드 작성) → GitHub(코드 저장 및 관리)
연동 방법
1. Google Colab에서 Python 코드를 작성한다.
2. 상단 메뉴에서 파일 → GitHub에 사본 저장을 선택한다.
3. GitHub 계정에 접근 권한을 부여한다.
4. 저장할 Repository와 파일 경로를 지정한다.
5. 저장을 완료하면 GitHub에서 .ipynb 파일을 확인할 수 있다.
GitHub에서는 .ipynb 파일의 코드, Markdown 설명, 저장된 출력 결과 등을 확인할 수 있다.
6. Google Colab 사용 시 주의사항
- 런타임 초기화: 일정 시간 사용하지 않거나 연결이 끊기면 실행 환경이 초기화될 수 있다.
- 파일 보존: /content에 저장한 파일은 런타임 종료 후 사라질 수 있으므로 중요한 파일은 Google Drive 등에 저장해야 한다.
- 변수 초기화: 런타임이 재시작되면 기존 변수와 실행 상태가 사라진다.
- 실행 순서: 셀을 실행한 순서에 따라 변수 상태가 달라질 수 있으므로 코드의 실행 순서에 주의해야 한다.
- 보안: 비밀번호, API 키 등 민감한 정보를 코드에 직접 작성하거나 GitHub에 공개하지 않아야 한다.
7. 핵심 요약
Google Colab = 클라우드 기반 Python 개발 환경
- 별도 설치 없이 브라우저에서 Python 실행
- 코드 셀과 Markdown 텍스트 셀로 구성
- Google Drive를 통한 저장 및 공유
- 데이터 분석과 AI 개발에 활용
- GitHub 연동을 통한 코드 관리 가능
- 런타임 종료 시 실행 상태와 임시 파일이 사라질 수 있음

공부 기록을 GitHub에 정리할 때는 Colab의 텍스트 셀에 개념과 설명을 작성하고, 코드 셀에 예제와 실행 결과를 정리한 뒤 .ipynb 파일을 업로드하는 방식이 유용하다. 이렇게 하면 개념 필기와 실제 Python 코드를 하나의 파일로 관리할 수 있다.
