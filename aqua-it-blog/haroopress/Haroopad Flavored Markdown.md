# Haroopad Flavored Markdown

이번 0,8 을 기준 으로 하루 패드 에는 3 가지 의 새로운 마크 다운 문법 이 추가 되었습니다.

하루 패드 는 앞으로도 John Gruber 의 마크 다운 과 Github Flavored Markdown 을 기반 으로 하루 패드 에 어울리는 마크 다운 포맷 이 추가 될 예정 예정.

여기서 중요한 것은 사용자 에게 문서 작성 에 편의성 을 앞장 세워 마크 다운 문법 이 추가 추가.

늘 표준 에 가깝고 마크 다운 커뮤니티 에서 지향 하는 방향 을 지키며 조금씩 변화 변화 할 계획 입니다.

이 문서 에서는 하루 패드 에서만 동작 하는 문법 에 대해서 설명 설명.

### Выделение (не подсветка синтаксиса)

**Выделение** (и подсветка, выделение и т. Д.) Может означать:

```
Syntax ==highlighting==, **display of text** in different colors and/or fonts, depending upon its meaning in context (e.g. different parts of speech in a sentence, or ==function==  vs. ==variables names== in computer source code)

```

Синтаксис **подсветка** , **отображение текста** в различных цветах и / или шрифты, в зависимости от его значения в контексте (например , различные части речи в предложении или **функции** vs. **имена переменных** в исходном коде компьютера)

### Содержание

Оглавление, обычно возглавляемое просто «Содержание» и сокращенно неформально как TOC, представляет собой список частей книги или документа, организованных в том порядке, в котором появляются детали.

```
[TOC]

# Chapter 1: Getting Started
...

## Introduction
...

## Next Steps
...

```

- Глава 1: Начало работы
  - [Введение](http://pad.haroopress.com/page.html?f=haroopad-flavored-markdown)
  - [Следующие шаги](http://pad.haroopress.com/page.html?f=haroopad-flavored-markdown)

**пример**

TOC этого документа

> 
>
> - Haroopad Flavored Markdown
>   - - [Выделение (не подсветка синтаксиса)](http://pad.haroopress.com/page.html?f=haroopad-flavored-markdown#highlight(not-syntax-highlight))
>     - [Содержание](http://pad.haroopress.com/page.html?f=haroopad-flavored-markdown#table-of-contents)
>     - [Media Embed](http://pad.haroopress.com/page.html?f=haroopad-flavored-markdown#media-embed)
>     - [презентация](http://pad.haroopress.com/page.html?f=haroopad-flavored-markdown#presentation)
>     - [Список заданий](http://pad.haroopress.com/page.html?f=haroopad-flavored-markdown#tasklist)
>     - [схема](http://pad.haroopress.com/page.html?f=haroopad-flavored-markdown#diagram)
>
> 

### Media Embed

OEmbed - это формат, позволяющий встроенное представление URL-адреса на сторонних сайтах. Простой API позволяет веб-сайту отображать встроенный контент (например, фотографии или видео), когда пользователь отправляет ссылку на этот ресурс, без необходимости непосредственно анализировать ресурс.

Просто используйте `@[]()`синтаксис для ссылки на внешние ресурсы

```
@[caption](content-url 'stylesheets')
@[](http://www.youtube.com/watch?v=jo_B4LTHi3I)
@[](http://www.flickr.com/photos/bees/2362225867/ 'width:300px')

```

### презентация

- [Как написать презентацию](http://pad.haroopress.com/page.html?f=how-to-write-presentation) 문서 에서 자세히 확인할 수 있습니다.

### Список заданий

- [Как управлять списком задач](http://pad.haroopress.com/page.html?f=how-to-manage-tasklist) 문서 에서 자세히 확인할 수 있습니다.

### схема

- [Как нарисовать диаграмму](http://pad.haroopress.com/page.html?f=how-to-draw-diagram) 문서 에서 자세히 확인할 수 있습니다.

0

![Вкусно](http://www.delicious.com/static/img/delicious.small.gif)Добавить

54
[вПоделиться](javascript:void(0);)