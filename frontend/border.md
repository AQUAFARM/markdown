# border

[Главная](https://webref.ru/) / [Справочник CSS](https://webref.ru/css) / border /

[Комментариев: 5](https://webref.ru/css/border#disqus_thread)

## Содержание

- [Краткая информация](https://webref.ru/css/border#field_css_info)
- [Синтаксис](https://webref.ru/css/border#field_css_syntax)
- [Значения](https://webref.ru/css/border#field_css_value)
- [Пример](https://webref.ru/css/border#field_css_example)
- [Примечание](https://webref.ru/css/border#field_css_note)
- [Спецификация](https://webref.ru/css/border#field_css_spec)
- [Браузеры](https://webref.ru/css/border#field_css_browser)

Универсальное свойство border позволяет одновременно установить толщину, стиль и цвет границы вокруг элемента. Значения могут идти в любом порядке, разделяясь пробелом, браузер сам определит, какое из них соответствует нужному свойству. Для установки границы только на определённых сторонах элемента, воспользуйтесь свойствами border-top, border-bottom, border-left, border-right.

## Краткая информация

| Значение по умолчанию | Зависит от использования |
| --------------------- | ------------------------ |
| Наследуется           | Нет                      |
| Применяется           | Ко всем элементам        |
| Анимируется           | Да                       |

## Синтаксис [?]()

```
border: border-width || border-style || border-color
```

## Значения

Значение border-width определяет толщину границы. Для управления ее видом предоставляется несколько значений border-style. Их названия и результат действия представлен на рис. 1.

![Стили рамок](https://webref.ru/assets/images/css/border_style.png)

Рис.1. Стили рамок

border-color устанавливает цвет границы, значение может быть в любом допустимом для CSS формате.

## Пример

- HTML
- Результат

** JSFiddle

```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>border</title>
  <style>
   .brd {
    border: 4px double black; /* Параметры границы */
    background: #fc3; /* Цвет фона */
    padding: 10px; /* Поля вокруг текста */
   }
  </style>
 </head> 
 <body>
  <div class="brd">
   Познание текста, не учитывая количества слогов, стоящих между 
   ударениями, дает ямб. Эти слова  совершенно справедливы, 
   однако генеративная поэтика аннигилирует урбанистический скрытый смысл.
   </div>
 </body>
</html>
```

В данном примере вокруг блока добавляется двойная граница. Результат показан на рис. 2.

![Применение свойства border](https://webref.ru/assets/images/css/css_border.png)

Рис. 2. Применение свойства border

## Объектная модель

*Объект*.style.border

## Примечание

Браузер Internet Explorer до шестой версии включительно при толщине границы 1px отображает dotted как dashed. При толщине 2px и выше значение dotted работает корректно. Эта ошибка исправлена в IE7, но только для всех границ толщиной 1px. Если одна из границ блока имеет толщину 2px и выше, то в IE7 значение dottedпревращается в dashed.

Стиль границы в разных браузерах может несколько различаться при использовании значений groove, ridge, inset или outset.

## Спецификация [?]()

| Спецификация                             | Статус                 |
| ---------------------------------------- | ---------------------- |
| [CSS Backgrounds and Borders Module Level 3](http://dev.w3.org/csswg/css3-background/#the-border-shorthands) | Возможная рекомендация |
| [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/box.html#border-shorthand-properties) | Рекомендация           |
| [CSS Level 1](http://www.w3.org/TR/CSS1/#border) | Рекомендация           |

## Браузеры [?]()

- [Настольные](https://webref.ru/css/border#desktop)
- [Мобильные](https://webref.ru/css/border#mobile)

| Internet Explorer | Chrome | Opera | Safari | Firefox |      |
| ----------------- | ------ | ----- | ------ | ------- | ---- |
| 4                 | 7      | 1     | 3.5    | 1       | 1    |

[Границы](https://webref.ru/css/type/border)