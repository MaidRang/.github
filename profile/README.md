<div align="center">
  <!-- 로고 이미지 있으면 아래 src만 교체 -->
  <!-- <img src="로고_이미지_URL" width="180" /> -->

  <h2 align="center">MaidRang</h2>

  <p align="center">
    메이드카페 출근표 · 이벤트 · 메이드 정보를 한 곳에서 확인하는 웹 플랫폼<br>
    <br>
    <a href="https://maidrang.site"><strong>Web Service »</strong></a>
    ·
    <a href="https://github.com/MaidRang"><strong>Organization »</strong></a>
    <!-- · <a href="백엔드_레포_URL"><strong>Backend Repo »</strong></a> -->
    <!-- · <a href="프론트엔드_레포_URL"><strong>Frontend Repo »</strong></a> -->
  </p>
</div>

<br>

<details open>
  <summary><strong>&nbsp;📖&nbsp;목차</strong></summary>

1. [🔍 Introduction](#-introduction)
2. [✨ Features](#-features)
3. [📄 Documents](#-documents)
4. [📹 Demo](#-demo)
5. [💡 Tech Stack](#-tech-stack)
6. [🗂️ Database](#%EF%B8%8F-database)
7. [💻 Architecture](#-architecture)
8. [👨‍💻 Team](#-team)

</details>

<br>

## 🔍 Introduction

### 배경

메이드카페의 출근 정보와 이벤트 공지는 주로 SNS, 이미지 공지, 개별 예약 페이지 등에 흩어져 있습니다.
팬 입장에서는 “오늘 누가 출근하는지”, “어떤 이벤트가 있는지”, “관심 있는 메이드의 다음 출근일이 언제인지”를 매번 직접 찾아봐야 하는 불편함이 있습니다.

MaidRang은 이러한 정보를 한 곳에서 확인할 수 있도록 만든 메이드카페 정보 통합 플랫폼입니다.
카페별 메이드 프로필, 출근표, 이벤트, 즐겨찾기 기반 일정 확인 기능을 제공하여 팬은 더 빠르게 정보를 찾고, 운영자는 반복적인 일정 안내 부담을 줄일 수 있도록 설계했습니다.

<br>

## ✨ Features

### 사용자 기능

* **카페별 메이드 조회**
  메이드카페별 소속 메이드 목록과 상세 정보를 확인할 수 있습니다.

* **월별 출근표 확인**
  카페별 출근 일정을 달력 형태로 확인할 수 있습니다.

* **관심 메이드 즐겨찾기**
  자주 확인하는 메이드를 즐겨찾기에 추가하고, 관심 메이드의 출근 일정을 우선적으로 확인할 수 있습니다.

* **이벤트 정보 조회**
  카페별 이벤트와 최신 공지를 확인할 수 있습니다.

* **소셜 로그인**
  카카오·네이버 OAuth2 로그인을 통해 간편하게 서비스를 이용할 수 있습니다.

### 관리자 기능

* **메이드 정보 관리**
  카페별 메이드 등록, 수정, 삭제를 관리할 수 있습니다.

* **출근 일정 관리**
  메이드별 근무 일정을 등록하고 관리할 수 있습니다.

* **이벤트 관리**
  카페 이벤트와 이미지를 등록하여 사용자에게 노출할 수 있습니다.

<br>

## 📄 Documents

* **운영** : 2026 ~ ing
* **Web** : https://maidrang.site
* **Backend API** : Swagger API 문서
* **배포 환경** : AWS EC2 / RDS / GitHub Actions
* **주요 개선 경험**

  * JWT 기반 인증/인가 처리
  * 카카오·네이버 OAuth2 로그인 구현
  * 메이드 출근표 월별 조회 API 설계
  * 즐겨찾기 기반 개인화 일정 조회 기능 구현
  * React + Spring Boot 기반 프론트엔드/백엔드 연동
  * GitHub Actions 기반 자동 배포 파이프라인 구축

<br>

## 📹 Demo

### Main Page

|    홈 화면   |   카페 상세   |    출근표    |
| :-------: | :-------: | :-------: |
| 이미지 추가 예정 | 이미지 추가 예정 | 이미지 추가 예정 |

### User Flow

|    로그인    |   메이드 목록  |    즐겨찾기   |
| :-------: | :-------: | :-------: |
| 이미지 추가 예정 | 이미지 추가 예정 | 이미지 추가 예정 |

<br>

## 💡 Tech Stack

|    Frontend    |   Backend   | Database | Infra / DevOps |       Auth      |
| :------------: | :---------: | :------: | :------------: | :-------------: |
|      React     | Spring Boot |   MySQL  |     AWS EC2    | Spring Security |
|   TypeScript   |     Java    |  AWS RDS | GitHub Actions |       JWT       |
|     Emotion    |     JPA     |          |      Nginx     |      OAuth2     |
| TanStack Query |             |          |                |  Kakao / Naver  |

```text
- Frontend : React, TypeScript, Emotion, TanStack Query
- Backend : Spring Boot, Java, JPA, Spring Security, JWT, OAuth2
- Database : MySQL, AWS RDS
- Deployment : AWS EC2, Nginx, GitHub Actions
- Tool : GitHub, Postman, Swagger
```

<br>

## 🗂️ Database

### MySQL

서비스의 핵심 데이터는 MySQL에 저장합니다.

| 테이블           | 설명          |
| :------------ | :---------- |
| USER          | 사용자 정보      |
| MAID_CAFE     | 메이드카페 정보    |
| MAID          | 메이드 프로필 정보  |
| WORK_SCHEDULE | 메이드 출근 일정   |
| FAVORITE      | 사용자별 관심 메이드 |
| CAFE_EVENT    | 카페 이벤트      |
| EVENT_IMAGE   | 이벤트 이미지     |

<br>

## 💻 Architecture

```text
[ Client ]
React Web

        ↓

[ Backend ]
Spring Boot
Spring Security + JWT
OAuth2 Login

        ↓

[ Database ]
MySQL / AWS RDS

        ↓

[ Infra ]
AWS EC2
Nginx
GitHub Actions CI/CD
```

### System Flow

```text
사용자
  ↓
React Web
  ↓
Spring Boot API Server
  ↓
JPA / Repository
  ↓
MySQL RDS
```

### Auth Flow

```text
사용자
  ↓
Kakao / Naver OAuth2 Login
  ↓
Spring Security OAuth2
  ↓
JWT 발급
  ↓
Access Token 기반 API 요청
```

<br>

## 👨‍💻 Team

|                 박정우                 |
| :---------------------------------: |
|     Backend & Frontend Developer    |
|      Spring Boot / React / AWS      |
| 서비스 기획, 백엔드 API 설계, 프론트엔드 구현, 배포 운영 |
