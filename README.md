📘 날씨 일기 프로젝트 (Weather Diary Project)
📌 프로젝트 소개

날씨 일기 프로젝트는 외부에서 제공하는 날씨 데이터를 활용하여 개인 일기를 기록하는 웹 애플리케이션입니다.
사용자는 특정 날짜를 선택해 일기를 작성할 수 있으며, 이때 해당 날짜의 실제 날씨 정보를 자동으로 불러와 함께 저장합니다.

✔ “날씨 데이터를 활용해 일기를 저장하고 관리하는 프로젝트”

🎯 주요 기능
➤ 1. 날씨 데이터 수집

외부 데이터 소스를 활용해 실시간 또는 특정 날짜의 날씨 정보를 가져옵니다.

데이터 수집 방식:

크롤링(웹 스크래핑)

공개(Open) API 활용

사용 가능한 데이터 예:

기온(temperature)

습도(humidity)

강수 확률(precipitation probability)

풍속(wind speed)

➤ 2. 날씨 기반 일기 작성

사용자가 일기를 작성하면 시스템이 자동으로 해당 날짜의 날씨를 조회

날씨 + 일기 내용을 함께 저장

날짜별로 조회 가능

저장된 일기 수정/삭제 가능

🌤️ 날씨 데이터 소스 선택
🔎 후보 1. 네이버 날씨 크롤링

‘서울 날씨’를 검색 후 HTML 데이터를 직접 크롤링

수집 가능 데이터: 기온, 강수확률, 습도, 바람 등

장점: 회원가입 없이 사용 가능

단점: HTML 구조 변경 시 유지보수 필요

🔎 후보 2. 기상청 오픈API

공공데이터포털에서 제공하는 공식 데이터

계정 발급 후 API Key 사용

특징:

국가 공식 데이터

신뢰도 높음

필요 기술:

API Key 발급 및 인증

XML/JSON 데이터 파싱

🔎 후보 3. OpenWeatherMap API

전 세계 날씨 데이터를 제공하는 글로벌 API

1분 60회 요청까지 무료

제공 데이터:

현재 날씨

시간별 / 일별 날씨

위도·경도 기반 데이터

장점: 국제 프로젝트에도 사용 가능

단점: 무료 플랜은 제한적

🛰️ 공개 API를 고르는 기준
✔ 1. 문서(API Documentation) 품질

Endpoint 설명이 정확한가?

요청/응답 예시가 제공되는가?

✔ 2. 데이터 범위

과거 데이터/실시간 데이터 제공 여부

지역 범위(국내/전 세계)

✔ 3. 요금 정책

무료 호출량

초과 사용 시 비용

🛠 사용 기술 스택
Backend

Java

Spring Boot

IDE

IntelliJ IDEA

Weather API

Naver Weather Crawling (Optional)

기상청 오픈API

OpenWeatherMap API

📚 API 문서화 도구

프로젝트 내 API 명세를 확인하기 위해 다음 도구를 활용했습니다.

Swagger (OpenAPI UI)

실시간 API 테스트 기능 제공

ReDoc

Swagger 문서를 기반으로 깔끔한 문서 렌더링

GitBook

프로젝트 기술 문서, 설명서 작성

기타 API 문서 생성 및 관리 도구

📁 프로젝트 구성 예시
📦 weather-diary
├─ 📂 controller
├─ 📂 service
├─ 📂 repository
├─ 📂 domain
├─ 📂 dto
├─ 📂 config
└─ 📄 application.yml (또는 properties)

📌 핵심 포인트 요약

외부 데이터(날씨)를 활용하여 일기 작성 자동화

크롤링 또는 오픈 API를 이용한 데이터 수집

Spring Boot 기반 날씨 조회 + 일기 저장 서비스 구축

Swagger/ReDoc 등을 이용한 API 문서화
