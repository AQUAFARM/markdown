# 하루 패드

**하루 패드** 는 웹 친화적 인 문서 를 작성 하기 위한 마크 다운 에디터 에디터.

여러분 은 간단한 마크 다운 문법 을 이용해 웹 문서 를 생성 하거나 하거나, 이메일 그리고 복잡한 리포트 문서 를 작성할 수 수.

그리고 하루 패드 는 윈도우, 리눅스, 맥 을 지원 하여 여러분 이 원하는 플랫폼 에서 똑같은 문서 편집 경험 을 얻을 수 수.

![Значок haroopad](http://pad.haroopress.com/assets/images/logo-small.png)

### **새로운 기능 (v0.13.1)**

- 신규 기능
  - 완료 되지 않는 타스크 수 를 앱 뱃지 로 표시
  - Завтра-ночь яркий, зенбурн 에디터 테마 추가

### **중요 변경 사항**

- 버그
  - [윈도우, 리눅스] - 시스템 설정 언어 로 변경 되지 않는 문제 수정
  - [윈도우] 프린트 가 되지 않는 문제 수정
  - [윈도우] 숫자 6 키보드 동작 오류 수정
  - [프리젠 테이션] - 커버 이미지 를 로컬 이미지 로 설정 하는 경우 표시 되지 않는 오류 수정
  - `code` 문법 граница 스타일 없어지 는 문제 수정
  - 수학 표현식 이 추가 된 문서 오픈 시 오류 수정
  - 수학 표현식 이 블럭 으로 만 렌더링 되는 문제 수정
  - 마크 다운 단축키 랩핑, 언 랩핑 문제 수정
  - 찾기 입력 창 에 붙여 넣기 가 되지 않던 문제 수정
- 개선
  - [윈도우] Ctrl-Y 단축키 문제 개선
  - 타스크 목록 과 리스트 목록 의 텍스트 시작 정렬 개선

### 주요 기능

- 크로스 플랫폼 을 지원

  - Окно
  - Mac OS X
  - Linux 32/64

- 에디터 테마 추가 (30) 및 코드 하이라이팅 지원

  - Solaraized Dark & Light 등 30 여 가지 의 테마
  - Ruby, Python, PHP, Javascript, C, HTML, CSS
  - CodeMirror 기반

- 라이브 뷰 테마 를 지원

  - Меньше 를 기반 으로 한 7 가지 의 테마
  - [Markdown-css](https://github.com/rhiokim/markdown-css) 프로젝트 기반

- 코드 문법 하이라이팅 스타일 을 지원

  - 112 가지 의 언어 에 대한 문법 강조 를 지원
  - Солоноватый, завтра 등 49 가지 의 스타일
  - Highlight.js 기반

- 프리젠 테이션 기능 - 

  ​

  http://pad.haroopress.com/page.html?f=how-to-write-presentation

   - v0.13

  - Душ 기반

- 다이어그램 (플로우 차트, 시퀀스 다이어그램 등) - 

  ​

  http://pad.haroopress.com/page.html?f=how-to-draw-diagram

   - v0.13

  - Русалка 기반

- 마크 다운 자동 완성 기능

  - 마크 다운 문법 의 자동 완성 을 이용해 문서 의 작성 의 효율 을 을 높힐 수.

- 사용자 테마 강화

  - 에디터, 뷰어 테마 를 CSS 기반 으로 좀더 쉽게 제공

- 폰트 사이즈 조절 기능

  - 환경 설정 혹은 단축키 를 이용해 에디터 와 뷰어 의 폰트 사이즈 를 조절

- 스타일 적용 된 HTML 복사 기능

  - 위지윅 에디터 HTML 모드 에 붙여 넣으면 에디터 와 동일 하게 표시

- 리치 미디어 콘텐츠 스마트 임베딩 - v0.8

  - 영상, 음악, 3D 데이터, 텍스트, 오픈 그래프 등과 같은 웹 콘텐츠 임베딩
  - 전세계 주요 (유튜브, 사운드 클라우드, 플리커 등) 100 여개 웹 서비스 지원
  - 드래그 앤 드랍 콘텐츠 임베딩 지원

- 뷰 모드 전환 기능 - v0.8

  - 기본, 리버스 (뷰어: 에디터), 에디터, 뷰어 (Вид> Режим)

- 현재 시간 입력 기능 - v0.8

  - 현재 시간 을 다양한 포맷 으로 입력 (Вставка> Дата и время)

- HTML 마크 다운 전환 기능 - v0.8

  - 브라우저 인용 하고 싶은 문서 를 선택 하고 하루 패드 로 드래그 드랍 드랍.

- 마크 다운 파서 옵션 설정 기능 추가

- CLI (интерфейс командной строки) 지원 - v0.12.1

  - `$ haroopad -f [ /path/to/a.md ./path/to/b.md ]`: 파일 옵션

  - ```
    $ haroopad --mode
    ```

    : 뷰 или 에디팅 모드 옵션

    - `$ haroopad --mode view`: 뷰 모드
    - `$ haroopad --mode edit`: 에디팅 모드

- 개요 보기 기능

- Vim 키 바인딩 을 지원

- PDF, HTML 출력 지원

- 자동 임시 저장 및 복원

- 들여 쓰기 탭 과 스페이스 지원

- 2,3 단 컬럼 레이아웃 지원

- 마크 다운 구문 헬프 윈도우

- 마크 다운 폴딩 지원

- 환경 설정 백업 내보내기 / 가져 오기 지원

### 국제화

- 영어 (английский)
- 한국어 (Корея)
- 스페인 (Español) - [davegomez](https://github.com/davegomez)
- 중국어 간체 (中文) - [туалетная вода](https://github.com/toiletfreak)
- 독일어 (Deutsch) - [Тобиас Мюкш](https://github.com/tobiasmuecksch)
- 베트남 (вьетнамский) - [nguyenkinh](https://github.com/nguyenkinh)
- 러시아 (русский) - [aprilix](https://github.com/aprilix)
- 그리스어 (греческий) - [pdudis](https://github.com/pdudis)
- 포루투칼 (португальский) - [alexandre mbm](https://github.com/alexandre-mbm)
- 일본어 (японский) - [Тосиюки Тега](https://github.com/Toshiyuki-Tega)
- 이태리어 (Italiano) - [Zeriuno](https://github.com/Zeriuno)
- 인도어 (Bahasa Indonesia) - [Реза Файз А. Рахман](https://github.com/rezafaizarahman)
- 터키어 (Türkçe) - [Eray AYDIN](https://github.com/erayaydin)
- 프랑스어 (Français) - [MarcBoyer](https://github.com/MarcBoyer) , [Daniel Ménard](https://github.com/daniel-menard)

### 향상된 마크 다운 문법

- ```
  [TOC]
  ```

   문법 추가

  - 문서 의 목차 를 문서 에 손쉽게 포함 할 수 있습니다.
  - 왼쪽 정렬: `[TOC "float:left"]`
  - 오른쪽 정렬: `[TOC "float:right"]`

- ```
  ![]()
  ```

   이미지 스타일 속성 추가

  - `![alt text](url "title" "css")`

- Github Flavord Markdown 지원

  - 구문 강조
  - 테이블
  - URL 자동 링크
  - 취소 선
  - Нахал, выскочка, пижон

- 수학 표현식 (Математическое выражение)

  - `$$$...$$$` 인라인 표현식
  - `$$...$$` 블럭 표현식
  - 인라인 수학 표현식 ( **$** , $$$) 선택적 옵션 추가

- 위첨자, 아래 첨자 문법 추가

  - `위첨자^superscript^`, `아래첨자~subscript~`

- 이미지 문법 확장

  - 만약 `![](path/*.mp3)`과 같이 аудио 확장자 (mp3, ogg) 인 경우 аудио 요소 로 표시
  - 만약 `![](path/*.mp4)`와 같이 видео 확장자 (mp4, ogv, webm) 인 경우 видео 요소 로 표시

- 각주 문법

  - 각주: `[^1]`

  - 각주 참조: 

    ```
    [^1]: text
    ```

    - 각주 참조 내용 에 마크 다운 문법 지원

- Список заданий - 

  ​

  http://pad.haroopress.com/page.html?f=how-to-manage-tasklist

   - v0.13.0

  - Задача: `- [ ]`
  - Задача (Готово): `- [x]`

### 곧 출시 될 기능

### 추가 정보

- 공식 사이트: [http://pad.haroopress.com](http://pad.haroopress.com/)
- 공식 블로그 및 메뉴얼: [http://pad.haroopress.com/page.html](http://pad.haroopress.com/page.html)
- 사용자 에코 시스템: [http://haroopad.userecho.com](http://haroopad.userecho.com/)

하루 패드 트위터 계정 과 [@haroopad](https://twitter.com/haroopad) 개발자 계정 [@rhiokim](https://twitter.com/rhiokim) 을 팔로 윙 하고 최신 소식 을 들으 세요.

의견 이나 버그 리포팅 이 필요 하시면 `Help`메뉴 에 `User Echo`메뉴 를 통해 남겨 남겨.

0

![Вкусно](http://www.delicious.com/static/img/delicious.small.gif)Добавить

54
[вПоделиться](javascript:void(0);)