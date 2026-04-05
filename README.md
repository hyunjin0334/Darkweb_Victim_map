# Ransomware Victim Location Visualization Service

## Overview
본 프로젝트는 랜섬웨어 피해 기업의 정보를 수집하고 이를 지도 기반으로 시각화하는 서비스를 개발하는 것을 목표로 한다.  
최근 랜섬웨어는 기업에 심각한 피해를 입히고 있으며, 이에 대한 대응 및 예방은 중요한 보안 과제가 되고 있다.  

이 프로젝트에서는 랜섬웨어 피해 기업의 위치 정보를 수집하고 지도 위에 시각적으로 표현함으로써, 기업 및 보안 전문가들이 피해 현황을 직관적으로 파악하고 대응 전략을 수립할 수 있도록 지원한다.

---

## Purpose
- 랜섬웨어 피해 기업의 위치 기반 정보 제공
- 다크웹 기반 랜섬웨어 활동 동향 분석
- 보안 대응 및 예방 전략 수립에 기여

---

## Data Collection
본 프로젝트는 다크웹에서 공개된 랜섬웨어 피해 기업 데이터를 수집한다.  

특히 다양한 국가와 산업군을 대상으로 공격을 수행하는 랜섬웨어 그룹인 LockBit을 중심으로 피해 기업 데이터를 수집 및 분석하였다.

---

## Key Features

### 1. Dark Web Crawling
- Python과 BeautifulSoup을 활용하여 다크웹 내 랜섬웨어 피해 기업 정보 자동 수집
- 기업 이름 및 관련 정보 추출

### 2. Google Maps Integration
- 수집된 기업 이름을 기반으로 URL 인코딩 수행
- Google Maps 검색 링크 자동 생성
- 검색 결과 페이지 응답 데이터 수집

### 3. Geolocation Extraction
- Google Maps 페이지 소스에서 위도(latitude)와 경도(longitude) 정보 추출
- 위치 데이터를 정제하여 활용 가능하도록 처리

### 4. Visualization
- 추출된 좌표를 기반으로 지도에 피해 기업 위치 표시
- 피해 기업의 지리적 분포 시각화

---

## Tech Stack
- Python  
- BeautifulSoup  
- Selenium  
- Flask  
- Requests  

---

## Project Workflow
1. 다크웹 접속 및 랜섬웨어 그룹 조사  
2. 크롤러를 통해 피해 기업 정보 수집  
3. 기업 이름 기반 Google Maps 검색 링크 생성  
4. 지도 페이지에서 좌표 정보 추출  
5. 지도 위에 위치 시각화  

---

## How to Run

### 1. Clone repository
git clone https://github.com/yourname/yourrepo.git
cd yourrepo

### 2. Create virtual environment (권장)
python -m venv venv
Windows:venv\Scripts\activate
Linux / WSL:source venv/bin/activate

### 3. Install dependencies
pip install -r requirements.txt

### 4. Run server
python main.py
또는 Flask 실행:
set FLASK_APP=main.py
flask run

### 5. Access
브라우저에서 접속: http://127.0.0.1:5000

---

## Output
- 랜섬웨어 피해 기업 위치 지도
- JSON 데이터 결과
- 피해 분포 시각화

---

## Notes
- 다크웹 접근은 Tor 환경을 기반으로 수행됨  
- 일부 기업 정보는 정확한 위치 매칭이 어려울 수 있음  
- Google Maps 구조 변경 시 파싱 로직 수정이 필요할 수 있음  

---

## Author
Hyunjin Kim
