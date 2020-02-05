# 네이버 지식인 크롤링

네이버 지식인에서 특정 텍스트를 포함한 질문과 응답을 크롤링하기 위해서 제작했습니다.

## 라이브러리
- python 3
- BeautifulSoup
- Selenium
- webdriver
- openpyxl

## 라이브러리 설치
#### 1. BeautifulSoup

```shell
pip install bs4
```

#### 2. Selenium

```shell
pip install selenium
```

#### 3. webdriver
해당 프로젝트는 크롬에서 크롤링을 하도록 만들었습니다. 다른 브라우저를 사용하실 분들은 다른 블로그에 설명이 잘 되어있으니 설명을 생략하겠습니다.

[여기](https://sites.google.com/a/chromium.org/chromedriver/downloads)를 눌러 현재 사용하는 크롬의 버전과 동일한 버전을 다운로드 받습니다.

다운로드 받은 후 코드 상에서 경로를 설정해야하기 때문에 필요한 곳에 넣어두도록 합시다.
```python
# chrome driver 패스 설정
path = "/Users/taehyung/anaconda3/envs/study/chromedriver"
driver = webdriver.Chrome(path)
```

#### 4. openpyxl
엑셀로 이쁘게 저장하기 위해서 쓰는 라이브러리입니다.
```shell
pip install openpyxl
```

## 사용방법 

### 키워드 세팅
```python
keyword = '우한 폐렴'
```

`keyword`에 찾길 원하는 텍스트를 입력합니다.

### 기간 설정
```python
# 크롤링 시작 일자
f = '2019.02.05'
# 크롤링 종료 일자
t = '2020.02.05'
```

`f`와 `t` 는 각각 기간을 나타내며, 서칭하고 싶은 기간을 설정합니다.

### 실행 방법
```shell
python3 project.py
```

## 결과
이후 프로젝트를 시작하면, 크롬이 켜지면서 하나하나 읽기 시작하고 엑셀로 저장합니다. 

![screenshot](screenshot.png)

