# Как написать выравнивание изображения на Haroopad

문서 를 작성 하다 보면 가장 많이 삽입 되는 외부 요소 가 바로 이미지 이미지. 문서 는 텍스트 로 작성 되고 이미지 는 텍스트 로 묘사 하기 어렵 거나 거나 로 표현 된 정보 문서 에 자주 첨부 됩니다 됩니다.

특히 하루 패드 와 같은 도구 에서 작성 하는 마크 다운 문서 문서 에는 위지윅 의 의 문서 도구 와 는 간단 하고 외우기 쉬운 구문 구문 있습니다 있습니다 있습니다 있습니다 있습니다 있습니다 있습니다 있습니다 있습니다 있습니다.

## Синтаксис изображения

`![]()` 와 같은 느낌표, 대괄호, 소괄호 를 순서 대로 나열한 다음 괄호 안에 필요한 정보 를 추가 하면 이미지 를 표시 할 수 수.

간단 하게 다음 과 같이 컴퓨터 에 있는 이미지 를 표시 할 수 수.

```
![](/path/to/image)
![](C:\Users\Images\myImage.jpg)

```

또한 인터넷 상 에 있는 이미지 도 문서 에 표시 할 수 수.

**마크 다운 표현법**

```
![](http://bit.ly/1g1oUFW)

```

**결과**

![img](http://bit.ly/1g1oUFW)

### Ссылки Стиль изображения

문서 내 에서 자주 사용 되는 로고나 이모티콘 과 같은 이미지 의 경우 고유 고유 를 수도 재.

**마크 다운 표현법**

```
![][id]

[id]: http://bit.ly/1e35InU

```

**결과**

![img](http://bit.ly/1e35InU)

### Alt Text и Title

웹 문서 에서 이미지 요소 의 속성 중에는 지정한 경로 에 이미지 를 텍스트 텍스트 텍스트 (Alt) 와 이미지 를 설명 하는 제목 (название) 이 있습니다.

```
![파리에서 먹었던 후루츠 칵테일](http://bit.ly/1e35InU "내가 좋아하는 과일 칵테일")

```

**결과**

> 이미지 를 표시 할 수 없는 경우 대체 텍스트 가 이미지 영역 에 표시 표시.
> ![img](http://pad.haroopress.com/docs/ko/how-to-use-image-align/images/alt.png)
>
> 이미지 에 마우스 를 오버 할 경우 해당 이미지 에 대한 설명 으로 제목 속성 속성 이 표시 됩니다.
> ![img](http://pad.haroopress.com/docs/ko/how-to-use-image-align/images/title.png)

여기 까지 의 설명 은 기본적인 마크 다운 에 대한 설명 으로 모든 마크 관련 서비스, 도구 에서 통용 됩니다. 다만 문서 를 작성 하다 보면 문서 의 구조 에 따라 이미지 를 정렬 정렬 사이즈 동반 변경.

하지만 표준 마크 다운 에서는 이 부분 을 제외 하고 있어 종종 불편 함 을 을. 그래서 서비스 나 도구 들 에 취향 (ароматизированный) 에 맞게 기본 마크 다운 을 확장, 개선 시켜 사용 하고 있습니다.

하루 패드 도 여러 고민 과 실험 끝에 기본 이미지 구문 `![]()`에 한가지 속성 을 을 더 추가 하였습니다.

## Атрибуты CSS

웹 문서 에서 문서 의 스타일 을 지정 하는 CSS 를 그대로 활용 하였습니다.

```
![](path/to/image "title" "CSS")

```

**마크 다운 표현법**

```
![](http://bit.ly/1g1oUFW "title" "width:200px;height:100px")


![][id]
[id]: http://bit.ly/1g1oUFW "title" "width:200px;height:100px"


![](http://bit.ly/1g1oUFW "right" "width:200px;height:100px;float:right;padding-left:10px;")

```

**결과**

> ![Размер изображения](http://bit.ly/1g1oUFW)
>
> ![правильно](http://bit.ly/1g1oUFW)하루 패드 는 문서 내에 이미지 를 보기 좋게 정렬 시키 거나 에 에 에 에 에 에 에 에 에. 이를 통해 문서 내에 이미지 를 좀더 보기 좋게 표시 할 수 있게 있게.
>
> 이 이미지 의 경우 `width:200px; height:100px; float:right; padding-left:10px`속성 이 추가 되어 문서 내에 우측 정렬 된 이미지 로 로 표현 되고 있습니다.

물론 위 의 예시 에서는 간단한 정렬 과 사이즈 만 변경 하였지만 CSS 를 응용 하면 다양한 방식 으로 문서 내 이미지 를 조절할 수 수.

### Правильно?

과연 경량 의 마크 다운 문법 에 스타일 시트 를 속성 으로 추가 한 것이 사용자 사용자 위한 배려 인가 하루 하루 을 꾸준히 하고 있습니다.

또한 이런 변화 에 대한 우려 와 걱정 도 함께 나눠 좋은 방향 을 잡고 마크 다운 을 리드 리드 노력할 계획 입니다 입니다.

## Узнать больше

- [http://daringfireball.net/projects/markdown/syntax#img](http://daringfireball.net/projects/markdown/syntax#img)
- [https://rawgithub.com/fletcher/human-markdown-reference/master/index.html](https://rawgithub.com/fletcher/human-markdown-reference/master/index.html)
- [http://www.w3schools.com/css/](http://www.w3schools.com/css/)

0

![Вкусно](http://www.delicious.com/static/img/delicious.small.gif)Добавить

54
[вПоделиться](javascript:void(0);)