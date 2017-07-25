## 하루 패드 스타일 사용자 화

CSS (каскадные таблицы стилей) 를 이용해 원하는 스타일 스타일 커스터마이즈 기능 은 스타일 스타일 을 을 의 배경 배경 과 스타일 스타일 을 을 을.

이 기능 은 하루 패드 v0.11 부터 지원 합니다.

### 사용자 테마 설정 하기

사용자 테마 는 환경 설정> 에디터 (혹은 뷰어)> 사용자 스타일 섹션 에서 선택할 수 있습니다. 하루 패드 에서는 기본적인 по умолчанию 테마 가 지정 되어 있습니다.

이 테마 는 사용자 테마 를 위한 기본 스타일 로 아무런 스타일 이 지정 되어 있지 않고 스타일 스타일 되어 되어 있습니다.

![img](http://pad.haroopress.com/docs/ko/customizing-editor-style/images/001.png)

에디터 버튼 을 클릭 하면 파일 브라우저 가 띄워 지고 `default.css`만 존재 존재.

![img](http://pad.haroopress.com/docs/ko/customizing-editor-style/images/002.png)

`default.css`파일 을 `myStyle.css`로 복사 하고 이 파일 에 지정된 CSS 만을 이용해 에디터 의 스타일 을 지정 합니다.

#### 나만 의 폰트 설정

```
editor {
  font-family: "Malgun Gothic", "Trebuchet MS", Helvetica, sans-serif !important;
}

```

#### 헤더 스타일 변경 하기

```
header {
  color: red;
}

```

### 하루 패드 에디터 스타일 스펙

**Правило CSS 만 사용할 수 있습니다.**

**тема**

| имя          | стиль                                 |
| ------------ | ------------------------------------- |
| редактор     | Цвет, шрифт-семья, текст-тень, фон- * |
| номер строки | Цвет, шрифт-семья, текст-тень, фон- * |
| activeline   | задний план-*                         |

**текст**

| имя         | стиль                   |
| ----------- | ----------------------- |
| заголовок   | Цвет, шрифт, текст-тень |
| комментарий | Цвет, шрифт, текст-тень |
| BLOCKQUOTE  | Цвет, шрифт, текст-тень |
| li1         | Цвет, шрифт, текст-тень |
| li2         | Цвет, шрифт, текст-тень |
| li3         | Цвет, шрифт, текст-тень |
| час         | Цвет, шрифт, текст-тень |
| IMG         | Цвет, шрифт, текст-тень |
| a           | Цвет, шрифт, текст-тень |
| Эм          | Цвет, шрифт, текст-тень |
| сильный     | Цвет, шрифт, текст-тень |

#### 웹 폰트 사용 하기

위 의 지정된 스타일 이외에 `@import`를 지원 합니다. 이를 통해 구글 웹 폰트 도 사용할 수 있습니다.

다음 은 **Open Sans** 라는 구글 웹 폰트 를 내 스타일 로 지정해 보도록 보도록.

- [http://www.google.com/fonts#UsePlace:use/Collection:Open+Sans](http://www.google.com/fonts#UsePlace:use/Collection:Open+Sans)

```
@import url(http://fonts.googleapis.com/css?family=Open+Sans);

editor {
    font-family: "Open Sans" !important;
}

```

위 의 링크 를 보면 `@import`할 수 있는 코드 를 제공 제공. 이 소스 를 복사 해 위 의 과정 에서 처럼 myStyle.css 제일 상단 에 넣고 저장 저장 환경 환경 창 에 `Reload`버튼 을 클릭 클릭 하면 확인할 수 있습니다 있습니다.

###### 참조

- Веб-шрифты Google: [http://www.google.com/fonts](http://www.google.com/fonts)
- Google Best Web Fonts: [http://www.awwwards.com/best-20-webfonts-from-google-web-fonts-and-font-face-embedding.html](http://www.awwwards.com/best-20-webfonts-from-google-web-fonts-and-font-face-embedding.html)

#### 유의 사항

하루 패드 v0.11 버젼 에서 사용자 테마 백업 기능 은 제공 되지 않기 때문에 별도로 관리 해야 해야.

0

![Delicious](http://www.delicious.com/static/img/delicious.small.gif)Добавить

54
[вПоделиться](javascript:void(0);)