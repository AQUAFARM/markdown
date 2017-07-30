# outline

[Главная](https://webref.ru/) / [Справочник CSS](https://webref.ru/css) / outline /

[1 комментарий](https://webref.ru/css/outline#disqus_thread)

## Содержание

- [Краткая информация](https://webref.ru/css/outline#field_css_info)
- [Синтаксис](https://webref.ru/css/outline#field_css_syntax)
- [Значения](https://webref.ru/css/outline#field_css_value)
- [Пример](https://webref.ru/css/outline#field_css_example)
- [Спецификация](https://webref.ru/css/outline#field_css_spec)
- [Браузеры](https://webref.ru/css/outline#field_css_browser)

Универсальное свойство, одновременно устанавливающее цвет, стиль и толщину внешней границы на всех четырёх сторонах элемента. В отличие от линии, задаваемой через border, свойство outline не влияет на положение блока и его ширину. Также нельзя задать параметры линии на отдельных сторонах элемента, outline применяется сразу ко всем четырём сторонам.

## Краткая информация

| Значение по умолчанию | Нет               |
| --------------------- | ----------------- |
| Наследуется           | Нет               |
| Применяется           | Ко всем элементам |
| Анимируется           | Да                |

## Синтаксис [?]()

```
outline: outline-color || outline-style || outline-width
```

## Значения

- outline-color

  Задаёт цвет линии в любом допустимом для CSS формате.

- outline-style

  Стиль линии.

- outline-width

  Толщина границы.

## Пример

- HTML
- Результат

** JSFiddle

```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>outline</title>
  <style>
   .photo img {
    padding: 20px; /* Поля вокруг изображения */
    margin-right: 10px; /* Отступ справа */
    margin-bottom: 10px; /* Отступ снизу */
    outline: 1px solid #666; /* Параметры рамки */
    background: #f0f0f0; /* Цвет фона */
    float: left; /* Обтекание по правому краю */
   }
  </style>
 </head> 
 <body> 
  <div class="photo">
   <img src="image/girl.jpg" alt="Девочка с муфтой">
   <img src="image/owl.jpg" alt="Сова">
   <img src="image/boy.jpg" alt="Эвенкийский мальчик">
  </div>
 </body>
</html>
```

Результат данного примера показан на рис. 1.

![Использование свойства outline](https://webref.ru/assets/images/css/css_outline.png)

Рис. 1. Использование свойства outline

## Объектная модель

Объект.style.outline

## Спецификация [?]()

| Спецификация                             | Статус         |
| ---------------------------------------- | -------------- |
| [CSS Basic User Interface Module Level 3](http://dev.w3.org/csswg/css3-ui/#outline) | Рабочий проект |
| [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/ui.html#propdef-outline) | Рекомендация   |

## Браузеры [?]()

- [Настольные](https://webref.ru/css/outline#desktop)
- [Мобильные](https://webref.ru/css/outline#mobile)

| Internet Explorer | Chrome | Opera | Safari | Firefox |
| ----------------- | ------ | ----- | ------ | ------- |
| 8                 | 1      | 7     | 1.2    | 1.5     |

[Границы](https://webref.ru/css/type/border)