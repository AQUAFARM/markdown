# Как выступить с Haroopad.

간단한 텍스트 표현법 이 이렇게 강력한 기능 을 제공 할 수 있을까? 하루 패드 0.13 버젼 부터는 프리젠 테이션 기능 이 탑재 되었습니다.

기존 의 마크 다운 문법 을 그대로 활용 하였기 때문에 프리젠 테이션 을 위해서 새로운 문법 이나 별도 별도 는 는 없습니다.

## Как написать.

작성법 은 매우 간단 합니다.

```
## Slide title 1

Slide contents 1

***

## Slide title 2

Slide contents 2

```

위에 예시 에서 알 수 있듯이 슬라이드 를 구분 하는 마크 다운 표현 방법 은 ( `***`, `---`) 으로 지정 했습니다.

![presentation.png](http://pad.haroopress.com/docs/ko/how-to-write-presentation/images/presentation.png)

두 가지는 기본적 으로 슬라이드 를 구분 하지만 향후 지원 하는 프리젠 테이션 에서는 에서는, 수직 나눔 의 두 가지 방식 으로 쓰일 예정 예정.

> **이 구문 은 상황 에 따라 더 편리한 방법 을 위해 변경 될 수 수.**

## Как сделать слайд-шоу

위와 같이 작성 했다면 뷰 (Вид) 메뉴 에 `Presentation Mode`메뉴 를 클릭 해보자. 혹은 단축키 Command(или Ctrl) + Alt+P

![menu.png](http://pad.haroopress.com/docs/ko/how-to-write-presentation/images/menu.png)

전체 화면 에 두개 의 슬라이드 가 보이고 원하는 슬라이드 를 클릭 하면 해당 슬라이드 부터 프리젠 테이션 테이션 있게 있게 됩니다.

![слайд-mode.png](http://pad.haroopress.com/docs/ko/how-to-write-presentation/images/slide-mode.png)

esc 키 를 누르면 종료 됩니다.

## правила

한가지 규칙 이 있습니다.

첫번째 슬라이드 의 경우 에는 제목 (#) 을 지정 하는 것은 필수 입니다. 제목 이 없는 경우 검정색 화면 으로 만 표시 됩니다.

그리고 문서 를 작성 하다 보면 슬라이드 커버 나 슬라이드 전체 를 뒤덮는 이미지 가 가 필요할 때가 있습니다. 이 방법 도 간단 하게 가능 합니다.

```
![cover](http://bit.ly/1uGE8FI)

```

![слайд-режим-cover.png](http://pad.haroopress.com/docs/ko/how-to-write-presentation/images/slide-mode-cover.png)

위 의 구문 과 같이 `[cover]`текст alt 위치 에 `cover`라고 입력 하면 됩니다. 만약 입력 하지 않거나 다른 문자 인 경우 에는 이미지 로 처리 처리.

## Мышление Haroopad

프리젠 테이션 은 많은 내용 의 정보 를 전달 해야 할 때 그 내용 내용 축약 수단 효과적으로.

하지만 대부분 에 현대 적인 도구 들은 위지윅 을 통해 다양 하고 성숙한 프리젠 테이션 테이션 기능 을 제공. 좀더 과장 되게 표현 하면 목적 을 넘어서 타이포 그라피 와 슬라이드 전화 효과 등에 시간 을 을.

하루 패드 는 그에 비해 매우 미흡 하지만 마크 다운 을 이용한 프리젠 테이션 기능 은 이런 이런 하지는 않습니다 않습니다.

**프리젠 테이션 목적 에 맞춰 군더더기 없이 전달 하고자 하는 내용 만 간단 하게 하게 하고 하고 이를 테이션 형태 로만 로만 하고 하고 작성자 입니다 입니다 을 입니다 두고 입니다 입니다 입니다 입니다 입니다.**

## Пример Doc

```
# Presentation Title
[Yours Truly](), Famous Inc.

![cover](http://www.dvd-ppt-slideshow.com/images/ppt-background/background-6.jpg)
***

## Header

Typewriter etsy messenger bag [fingerstache](), aesthetic vinyl semiotics twee **DIY** forage chillwave. Thundercats ennui messenger bag, squid carles chillwave shoreditch pickled cliche **letterpress**. DIY beard locavore occupy salvia, whatever single-origin ==coffee== fanny pack 3 wolf moon typewriter gastropub1 kale H20 chips. Ennui keffiyeh thundercats jean shorts biodiesel. Terry richardson, swag blog locavore umami vegan helvetica. Fingerstache kale chips.

<footer>
<p>DIY beard locavore <i>occupy</i> salvia, whatever single-origin <code>coffee</code> fanny pack 3 wolf moon <a href="">typewriter</a> gastropub<sup>1</sup> kale H<sub>2</sub>0 chips. Ennui <strong>keffiyeh</strong> thundercats jean <em>shorts</em> biodiesel. Terry richardson, swag blog locavore umami <b>vegan</b> helvetica. Fingerstache kale chips.</p>
</footer>

***

## Header

Thundercats ennui messenger bag, squid carles chillwave shoreditch pickled cliche letterpress. DIY beard locavore occupy salvia, whatever single-origin coffee fanny pack 3 wolf moon typewriter gastropub kale chips. Ennui keffiyeh thundercats jean shorts biodiesel. Terry richardson, swag blog locavore umami vegan helvetica. Fingerstache kale chips.

Typewriter etsy messenger bag fingerstache.

***

## Lists in English typography

* Ennui keffiyeh thundercats
* Jean shorts biodiesel
* Terry richardson, swag blog
    1. Locavore umami vegan helvetica
    2. Fingerstache kale chips
    3. Keytar sriracha gluten-free
* Before they sold out master

***

## Lists in Russian typography

- Ennui keffiyeh thundercats
- Jean shorts biodiesel
- Terry richardson, swag blog
    1. Locavore umami vegan helvetica
    2. Fingerstache kale chips
    3. Keytar sriracha gluten-free
- Before they sold out master

***

## Lists in English typography

1. Locavore umami vegan helvetica
2. Fingerstache kale chips
3. Keytar sriracha gluten-free

* Ennui keffiyeh thundercats
* Jean shorts biodiesel
* Terry richardson, swag blog

***

## Quote

> Typewriter etsy messenger bag fingerstache, aesthetic vinyl semiotics twee DIY forage chillwave. Thundercats ennui messenger bag, squid carles chillwave shoreditch pickled cliche letterpress. _**Author Name**_

DIY beard locavore occupy salvia, whatever single-origin coffee fanny pack 3 wolf moon typewriter gastropub kale chips.

***

## Table

| Locavore     | Umami        | Helvetica | Vegan     |
|--------------|--------------|-----------|-----------|
| Fingerstache | Kale         | Chips     | Keytar    |
| Sriracha     | Gluten-free  | Ennui     | Keffiyeh  |
| Thundercats  | Jean         | Shorts    | Biodiesel |
| Terry        | Richardson   | Swag      | Blog      |

Typewriter etsy messenger bag fingerstache.

*** 

## Numbered code listing

    <html lang="en">
    <head> <!--Comment-->
        <title>Shower</title>
        <meta charset="UTF-8">
        <link rel="stylesheet" href="s/screen.css">
        <script src="j/jquery.js"></script>
    </head>

***

## You Can <br> Shout This Way

***

## [Linked Shout]()

***

## Growing Shout

***

## Shrinking Shout

```

0

![Вкусно](http://www.delicious.com/static/img/delicious.small.gif)Добавить

0
[вПоделиться](javascript:void(0);)