# Граница в CSS

[Главная](https://webref.ru/) / [Учебные курсы](https://webref.ru/course) / [Блочная модель в CSS](https://webref.ru/course/box-model) / Граница в CSS /

[Комментариев: 7](https://webref.ru/course/box-model/border#disqus_thread)

- [Описание](https://webref.ru/course/box-model/border#content)
- [Задания](https://webref.ru/course/box-model/border#task)

Так как элемент HTML отображается в виде прямоугольника, у элемента может быть до **четырёх границ**: сверху, снизу, слева и справа. Вы можете установить границу со всех сторон сразу или на каждой стороне отдельно.

Типы границ и их положение

Граница в CSS состоит из трёх свойств:

- border-color определяется с помощью [единиц цвета](https://webref.ru/course/css-basics/color);
- border-style может быть solid, dashed, dotted и др.;
- border-width определяется с помощью [единиц размера](https://webref.ru/course/css-basics/size).

Также граница может быть задана на четырёх возможных сторонах:

- border-top
- border-bottom
- border-left
- border-right

```
blockquote { border-color: yellow; border-style: solid; border-width: 1px; }
```

Сокращённое свойство border позволяет определить все три свойства сразу:

```
blockquote { border: 1px solid yellow; }
```

## Единственная граница

Если вы хотите установить границу только на одной из четырёх сторон, вам необходимо включить **положение**границы в свойство CSS. К примеру, для нижней границы вы можете написать:

```
blockquote { border-bottom-color: yellow; border-bottom-style: solid; border-bottom-width: 1px; }
```

Что касается свойства border, у *каждой* стороны есть своя сокращённая версия:

```
blockquote { border-bottom: 1px solid yellow; }
```

**Что делать, если мне надо три границы? Должен ли я установить их отдельно?**

Как вы уже догадались, самый быстрый способ получить три границы — это установить все четыре из них, а затем удалить ту, которую вы не хотите:

```
blockquote { border: 1px solid yellow; border-left: none; }
```

## Сокращённые комбинации

Поскольку существуют три *свойства* границы и четыре *положения* границ, получается 12 возможных комбинаций:

| border        | border-color        | border-style        | border-width        |
| ------------- | ------------------- | ------------------- | ------------------- |
| border-top    | border-top-color    | border-top-style    | border-top-width    |
| border-bottom | border-bottom-color | border-bottom-style | border-bottom-width |
| border-left   | border-left-color   | border-left-style   | border-left-width   |
| border-right  | border-right-color  | border-right-style  | border-right-width  |

Доступно довольно много свойств. В конечном итоге вы будете обычно использовать только **пять сокращённых версий**:

- border
- border-top
- border-bottom
- border-left
- border-right

[Перейти к заданиям](https://webref.ru/course/box-model/border#lesson-tabs)