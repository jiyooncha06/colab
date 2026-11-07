
# Google Colab 개념 정리

## 1. Google Colab이란?

**Google Colab(Google Colaboratory)**은 구글에서 제공하는 클라우드 기반의 프로그래밍 개발 환경이다.

웹 브라우저에서 별도의 프로그램 설치 없이 Python 코드를 작성하고 실행할 수 있으며, Google Drive와 연동하여 파일을 저장하고 공유할 수 있다.

### 주요 특징

- **클라우드 기반:** 개인 컴퓨터가 아닌 구글에서 제공하는 서버에서 코드를 실행한다.
- **설치 불필요:** 웹 브라우저만 있으면 Python 프로그래밍이 가능하다.
- **무료 사용 가능:** 무료로 CPU와 제한적인 GPU 및 TPU 자원을 이용할 수 있다.
- **자동 저장:** 기본적으로 Google Drive에 노트북이 저장된다.
- **협업 가능:** 다른 사용자와 코드를 공유하고 공동으로 편집할 수 있다.
- **라이브러리 지원:** NumPy, Pandas, Matplotlib 등 다양한 Python 라이브러리를 사용할 수 있다.

---

## 2. Google Colab의 기본 구조

Google Colab은 **Jupyter Notebook**을 기반으로 하며, 하나의 노트북 파일은 여러 개의 셀(Cell)로 구성된다.

### 주요 구성 요소

| 구성 요소 | 설명 |
|---|---|
| 노트북(Notebook) | 코드와 설명을 함께 저장하는 문서 |
| 코드 셀(Code Cell) | Python 코드를 작성하고 실행하는 공간 |
| 텍스트 셀(Text Cell) | Markdown을 사용하여 설명과 필기를 작성하는 공간 |
| 런타임(Runtime) | Python 코드가 실제로 실행되는 환경 |
| 출력(Output) | 코드 실행 결과가 표시되는 영역 |

### 코드 셀과 텍스트 셀의 차이

#### ① 코드 셀(Code Cell)

Python 코드를 작성하고 실행하는 공간이다.

**예제 코드**

```python
a = 10
b = 20

print(a + b)
```

**실행 결과**

```text
30
```

#### ② 텍스트 셀(Text Cell)

Markdown 문법을 사용하여 개념 설명, 제목, 표, 링크 등을 작성하는 공간이다.

**Markdown 작성 예시**

```markdown
# Python 기초

## 변수

**변수**는 데이터를 저장하는 공간이다.

- 정수형: int
- 실수형: float
- 문자열: str
```

---

## 3. Google Colab의 주요 기능

### ① Python 코드 실행

코드 셀에 Python 코드를 입력한 뒤 `Shift + Enter`를 누르면 실행된다.

```python
name = "Google Colab"

print("Hello,", name)
```

**실행 결과**

```text
Hello, Google Colab
```

### ② 라이브러리 사용

Google Colab에서는 다양한 Python 라이브러리를 사용할 수 있다.

대표적인 라이브러리는 다음과 같다.

| 라이브러리 | 주요 용도 |
|---|---|
| NumPy | 수치 계산 및 배열 연산 |
| Pandas | 데이터 분석 및 처리 |
| Matplotlib | 그래프 및 데이터 시각화 |
| TensorFlow | 머신러닝 및 딥러닝 |
| PyTorch | 인공지능 모델 개발 |

**라이브러리 불러오기**

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

필요한 라이브러리가 설치되어 있지 않다면 다음 명령어로 설치할 수 있다.

```python
!pip install 패키지이름
```

### ③ Google Drive 연동

Google Colab은 Google Drive와 연동하여 파일을 불러오거나 저장할 수 있다.

**Google Drive 연결 코드**

```python
from google.colab import drive

drive.mount('/content/drive')
```

위 코드를 실행하면 Google Drive 접근을 위한 인증 과정이 진행된다.

연결 후에는 Google Drive에 저장된 파일을 Python 코드에서 사용할 수 있다.

### ④ GPU 및 TPU 활용

Google Colab에서는 CPU뿐 아니라 GPU와 TPU를 활용할 수 있다.

- **CPU:** 일반적인 프로그램 실행 및 연산
- **GPU:** 병렬 연산에 특화된 장치로, 딥러닝 학습 등에 활용
- **TPU:** 머신러닝 연산을 가속하기 위해 설계된 장치

**설정 방법**

1. 상단 메뉴에서 `런타임(Runtime)` 선택
2. `런타임 유형 변경(Change runtime type)` 클릭
3. 하드웨어 가속기에서 GPU 또는 TPU 선택
4. 저장 후 실행

> **주의:** 무료 계정에서는 GPU 및 TPU의 사용 시간과 자원에 제한이 있다.

---

## 4. Google Colab과 일반 Python 개발 환경 비교

| 구분 | Google Colab | VS Code / PyCharm |
|---|---|---|
| 설치 | 불필요 | 일반적으로 필요 |
| 실행 환경 | 클라우드 서버 | 주로 개인 컴퓨터 |
| 인터넷 연결 | 필요 | 로컬 실행 시 불필요 |
| 주요 파일 형식 | `.ipynb` | `.py` |
| GPU 사용 | 구글 서버 자원 활용 가능 | 로컬 또는 별도 서버 설정 |
| 주요 용도 | 학습, 데이터 분석, AI | 일반 프로그램 및 프로젝트 개발 |
| 협업 | 노트북 공유 및 공동 편집 | Git 등을 활용한 협업 |

### Google Colab의 장점

1. 별도의 개발 환경을 설치할 필요가 없다.
2. 인터넷만 연결되어 있으면 다양한 컴퓨터에서 사용할 수 있다.
3. Python 학습과 데이터 분석에 적합하다.
4. GPU 및 TPU를 활용한 AI 개발이 가능하다.
5. Google Drive 및 GitHub와 연동할 수 있다.

### Google Colab의 단점

1. 인터넷 연결이 필요하다.
2. 런타임 연결이 끊어질 수 있다.
3. 무료 사용자의 컴퓨팅 자원에는 제한이 있다.
4. 런타임이 초기화되면 변수와 임시 파일이 사라질 수 있다.
5. 복잡한 소프트웨어 프로젝트에서는 로컬 개발 환경이 더 편리할 수 있다.

---

## 5. Google Colab과 GitHub 연동

Google Colab에서 작성한 코드는 GitHub에 저장하여 버전 관리와 학습 기록에 활용할 수 있다.

### GitHub에 저장하는 방법

1. Google Colab에서 Python 코드를 작성한다.
2. 상단 메뉴에서 `파일(File)`을 선택한다.
3. `GitHub에 사본 저장(Save a copy in GitHub)`을 클릭한다.
4. GitHub 계정 접근 권한을 부여한다.
5. 저장할 Repository와 파일 경로를 선택한다.
6. 저장을 완료한다.

### 주요 파일 형식

| 확장자 | 설명 |
|---|---|
| `.ipynb` | 코드, Markdown 설명, 출력 결과 등을 저장하는 Jupyter Notebook 파일 |
| `.py` | Python 소스 코드 파일 |
| `.md` | Markdown 문서 파일 |

### GitHub에 공부 내용을 정리하는 방법

다음과 같은 폴더 구조로 정리할 수 있다.

```text
colab/
│
├── README.md
│
├── about-colab.md
│
├── python-basic/
│   ├── variables.ipynb
│   ├── conditions.ipynb
│   └── loops.ipynb
│
└── python-practice/
    ├── practice01.ipynb
    └── practice02.ipynb
```

- `README.md`: Repository 전체 소개
- `about-colab.md`: Google Colab 개념 정리
- `python-basic/`: Python 기초 개념 및 예제
- `python-practice/`: Python 실습 코드

---

## 6. Google Colab 사용 시 주의사항

### ① 런타임 초기화

Google Colab은 클라우드 환경에서 코드를 실행하기 때문에 일정 시간 사용하지 않거나 연결이 끊어지면 런타임이 초기화될 수 있다.

런타임이 초기화되면 기존에 선언한 변수와 실행 상태가 사라진다.

### ② 파일 저장

Colab의 `/content` 폴더에 저장된 파일은 런타임 종료 후 사라질 수 있다.

따라서 중요한 파일은 Google Drive나 GitHub 등에 별도로 저장해야 한다.

### ③ 코드 실행 순서

Colab에서는 코드 셀을 원하는 순서대로 실행할 수 있다.

하지만 변수가 선언되기 전에 사용하면 오류가 발생할 수 있다.

**잘못된 예시**

```python
print(a)

a = 10
```

**올바른 예시**

```python
a = 10

print(a)
```

### ④ 보안

API 키, 비밀번호 등 민감한 정보를 코드에 직접 작성하거나 공개 GitHub Repository에 업로드하지 않도록 주의해야 한다.

---

## 7. 핵심 요약

> **Google Colab = 클라우드 기반 Python 개발 환경**

- 별도의 설치 없이 웹 브라우저에서 Python 실행 가능
- Jupyter Notebook을 기반으로 동작
- 코드 셀과 Markdown 텍스트 셀로 구성
- Google Drive를 통한 파일 저장 및 공유 가능
- 데이터 분석과 인공지능 개발에 활용
- GPU 및 TPU를 제한적으로 무료 사용 가능
- GitHub 연동을 통한 코드 관리 가능
- 런타임 종료 시 변수와 임시 파일이 사라질 수 있음

### 공부할 때 활용하는 방법

1. **텍스트 셀:** Python 개념 및 문법 정리
2. **코드 셀:** 예제 코드 작성 및 실행
3. **Google Drive:** 노트북 파일 저장
4. **GitHub:** 학습 기록 관리 및 버전 관리

---

## 참고 링크

- [Google Colab 공식 사이트](https://colab.research.google.com/)
- [Google Colab 공식 안내](https://colab.research.google.com/notebooks/intro.ipynb)
- [GitHub 공식 사이트](https://github.com/)
- [Python 공식 문서](https://docs.python.org/3/)
