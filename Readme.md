# ✉바이트

<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/로고_수정.png"/></p>

바이트는 데이터 처리, 저장, 전송의 기본적인 단위로 널리 사용되며, 이러한 개념이 이벤트 처리, 저장, 전송과 관련된 기능을 통합한 VITE 플랫폼과 유사하게 연결됩니다. 또한, 초대하다는 의미를 가진 INVITE에서 VITE를 채용함으로써, 두 가지 의미를 동시에 담고 있습니다.

### 팀명 : 사고뭉치

### 팀원

| |
|---|---|---|---|---|---|
|[박고은](https://github.com/goeunpark123) | [배성민](https://github.com/mini-xi) | [이예원](https://github.com/onelee521) | [장민석](https://github.com/ms1011) | [정우진](https://github.com/Wrinkk) | [한소혜](https://github.com/Sosohy)|

## 목차
### [프로젝트 개요](#-프로젝트-개요)<br/>
&nbsp;&nbsp;[1. 프로젝트 소개](#1-프로젝트-소개)<br/>
&nbsp;&nbsp;[2. 프로젝트 필요성](#2-프로젝트-필요성)<br/>
&nbsp;&nbsp;[3. 프로젝트 주요 기능](#3-프로젝트-주요-기능)<br/>
### [기술스택](#-기술스택)<br/>
### [WBS](#WBS)<br/>
### [요구사항](#-요구사항)<br/>
### [DB 모델링](#-DB-모델링)<br/>
&nbsp;&nbsp;[1. 개념 모델링](#1-개념-모델링)<br/>
&nbsp;&nbsp;[2. 논리 모델링](#2-논리-모델링)<br/>
&nbsp;&nbsp;[3. 물리 모델링](#3-물리-모델링)<br/>
### [주요 쿼리](#주요-쿼리)<br/>
### [테스트](#테스트)<br/>
### [회고](#회고)<br/>

## 🎈 프로젝트 개요

### 1. 프로젝트 소개

바이트는 이벤트에 대한 `초대장 발송 서비스`를 제공하는 플랫폼입니다.  이벤트 정보를 담은 초대장을 원하는 디자인의 템플릿으로 게스트들에게 이메일 또는 SMS로 전송하고, 이벤트 페이지를 통해 소통할 수 있습니다. 특별한 날을 기념하여 호스트가 원하는 선물을 등록할 경우, 게스트들이 펀딩 형식으로 선물을 구매할 수도 있습니다. 특별한 날을 더욱 특별하게 만들어줄 초대장을 통해 기억에 남을 즐거운 이벤트를 진행할 수 있습니다.

### 2. 프로젝트 필요성

멀리 사는 지인에게 평범한 이메일이나 문자가 아닌 특별한 초대장을 보낼 수 있습니다.

<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/news1.png" width="50%" height="50%"/></p>
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/news2.png" width="50%" height="50%"/></p>
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/news3.png" width="50%" height="50%"/></p>



최근 뉴스에 따르면 모바일 초대장이 개인 행사뿐만 아니라 지역 행사나 회사에서도 널리 사용되고 있습니다. 모임 통장의 보편화로 소규모 모임이 늘어나고 있으며, 연말, 연시 등 다양한 개인 및 인간 관계의 기념일이 다양화되고 있어서 초대장의 역할이 더욱 중요해졌습니다.

초대장 발송은 더 이상 단순한 의사소통 수단을 넘어서 새로운 경험의 수단으로 강조되고 있습니다. 이러한 흐름에 따라 초대장은 모임의 품질을 높일 수 있는 방안으로 강조되고 있습니다. 초대장을 통해 이벤트 참여자들과 소통할 수 있는 커뮤니티 기능이나 선물 교환 기능 등을 활용하면, 초대장이 단순한 통보 수단에서 벗어나 상호작용의 중심지로서 강조될 수 있습니다. 이는 사용자들에게 참여 동기를 부여하고, 이벤트 참여와 즐거움 공유의 기회를 제공합니다.

초대장은 이제 행사의 시작점에 머물러 있지 않고, 새로운 인연의 시작을 의미하는 중요한 역할을 합니다. 이에 따라, 미래에는 더 다양하고 흥미로운 초대장 서비스의 등장이 기대되고 있습니다.

</aside>

### 3. 프로젝트 주요 기능

1. 이벤트 초대하기/RSVP(초대 확인)
    - 이메일 또는 전화번호로 다른 사람에게 이벤트를 발송한다.
    - 초대받은 게스트는 이벤트 정보를 확인하고 참석 여부를 등록할 수 있다.
    - 이벤트의 호스트와 초대받은 회원은 이벤트 페이지에서 댓글을 통해 소통할 수 있다.

2. 초대장템플릿 구매/적용
    - 회원은 이벤트에 적용할 초대장템플릿을 구매할 수 있다.
    - 이벤트 생성 시, 호스트는 보유한 템플릿을 이벤트에 적용할 수 있다.

3. 선물/펀딩
    - 호스트는 이벤트에 받고 싶은 선물을 등록할 수 있다.
    - 회원인 게스트들은 호스트가 등록한 선물에 원하는 만큼 결제하여 선물할 수 있다.

4. 다른 이벤트 확인하기
    - 이벤트 공유 페이지를 통해 다른 사람의 이벤트를 참고할 수 있다.
    - 현재 인기가 많은 이벤트 형식이 무엇인지 확인할 수 있다.

## 📟 기술스택
|DA#|ubuntu|mariaDB|
|---|---|---|
|<img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/da%23.png" height="150" />|<img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/ubuntu.png" height="150" />|<img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/mariadb.png" height="150" />|   

## WBS

## 📘 요구사항

<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/요구사항1.PNG"/></p>
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/요구사항2.PNG"/></p>
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/요구사항3.PNG"/></p>
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/요구사항4.PNG"/></p>

<details>
<summary><b>VITE 상세정책</b></summary>
    
- 회원등급 관련
    - 일반: 할인 혜택 없음
    - VIP : 3% 할인 (누적결제금액 3만원 이상)
    - VVIP : 5% 할인 (누적결제금액  5만원 이상)
    - 운영자
    
- 운영자 권한
    - 회원의 게시물 및 댓글 수정/삭제
    - 회원 관리 및 계정 정지
    - 공지사항 작성
    - 문의사항 답변
    - 초대장 템플릿 등록
    
- 회원 권한
    - 이벤트/이벤트댓글/게시글 작성
    - 이벤트 초대 받기/RSVP
    - 선물 결제
    - 템플릿 결제
    
- 비회원 권한
    - 이벤트 초대 받기/RSVP
    
- 결제 및 환불 관련 정책
    - 템플릿 환불
        - 템플릿 사용 전 환불 100%
        - 템플릿 사용 후 환불 불가
    - 선물 펀딩 환불
        - 금액을 달성하지 못하면 참여 게스트 전액 환불(은행API의 기능)
    - 선물 펀딩 성공 시
        - 호스트에게 모인 금액 전송(은행API의 기능)
</details>

## 💭 DB 모델링

### 1. 개념 모델링
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/개념 모델링.png"/></p>

### 2. 논리 모델링(Barker 표기법)
(전체)
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/바커수정.PNG"/></p>
(L)
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/바커수정1.PNG"/></p>
(R)
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/바커수정2.PNG"/></p>

### 3. 물리 모델링
(전체)
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/물리모델링_수정.PNG"/></p>
(L)
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/물리모델링_수정1.PNG"/></p>
(R)
<p align="center"><img src="https://github.com/beyond-sw-camp/be04-1st-4goda-vite/blob/main/PNG/Readme/물리모델링_수정2.PNG"/></p>

## 주요 쿼리

## 테스트

## 회고

