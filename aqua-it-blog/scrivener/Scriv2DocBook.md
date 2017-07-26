# Scriv2DocBook

Scriv2DocBook - простой рабочий процесс для написания технических книг в [Scrivener](http://www.literatureandlatte.com/scrivener.php) , приложение для составления текста из [литературы и Latte](http://www.literatureandlatte.com/) . Конечным результатом является DocBook XML, подходящий для доставки издателю, или рендеринг в другие форматы с использованием инструментов DocBook.

Scriv2DocBook состоит из:

- Метод составления технической книги в качестве проекта Scrivener
- Инструмент для экспорта такого проекта, как DocBook XML
- Инструмент для импорта подмножества DocBook XML обратно в Scrivener

Инструменты специально настроены для написания для [O'Reilly Media](http://www.oreilly.com/) , но результатом является стандартный DocBook.

Инструменты преобразования Scriv2DocBook - это бесплатное программное обеспечение, выпущенное под лицензией Apache, версия 2.0.

## содержание

- Scriv2DocBook
  - [содержание](https://www.dansanderson.com/scriv2docbook/README.html#Contents)
  - [Предостережения](https://www.dansanderson.com/scriv2docbook/README.html#Caveats)
  - [Установка Scriv2DocBook](https://www.dansanderson.com/scriv2docbook/README.html#Installing_Scriv2DocBook)
  - [Настройка Scrivener](https://www.dansanderson.com/scriv2docbook/README.html#Setting_Up_Scrivener)
  - Написание книги
    - [Главы и предисловия](https://www.dansanderson.com/scriv2docbook/README.html#Chapters_and_Prefaces)
    - [Заголовки и идентификаторы разделов](https://www.dansanderson.com/scriv2docbook/README.html#Titles_and_Section_IDs)
    - [Блочные элементы](https://www.dansanderson.com/scriv2docbook/README.html#Block_Elements)
    - [Элементы блока, содержащие параграфы](https://www.dansanderson.com/scriv2docbook/README.html#Block_Elements_Containing_Paragraphs)
    - [Другие особенности XML и DocBook](https://www.dansanderson.com/scriv2docbook/README.html#Other_Features_of_XML_and_DocBook)
  - [Экспорт DocBook XML](https://www.dansanderson.com/scriv2docbook/README.html#Exporting_DocBook_XML)
  - [Импорт проекта DocBook в Scrivener](https://www.dansanderson.com/scriv2docbook/README.html#Importing_a_DocBook_Project_to_Scrivener)
  - [Лицензия](https://www.dansanderson.com/scriv2docbook/README.html#License)

## Предостережения

**Scrivener не является редактором XML. **Я не могу это подчеркнуть. Scriv2DocBook ожидает, что вы разберете XML-разметку вручную в проекте Scrivener. Это подвержено ошибкам, и даже самый опытный машинист XML столкнется с синтаксисом и ошибками проверки. Вы не поймаете эти ошибки до тех пор, пока не будете экспортированы, а отслеживание этих ошибок в исходном тексте вашего проекта Scrivener будет утомительным.

Моя общая рекомендация - *не* использовать Scriv2DocBook! Большинство людей будут счастливее с средой редактирования XML, в идеале, которая проверяет схему при вводе. [Oxygen](http://www.oxygenxml.com/) , [Syntext Serna](http://www.syntext.com/products/serna/) или [Emacs](http://www.gnu.org/software/emacs/) с [режимом nxml](http://www.thaiopensource.com/nxml-mode/) - все это хорошие варианты и очень рекомендуется для редактирования XML в приложении, не подходящем для этой цели. Только продолжайте, если вы, как и я, перегружены другими значительными прелестями Scrivener и готовы взять на себя это бремя.

Я написал Scriv2DocBook для моего собственного использования в проекте для [O'Reilly Media](http://www.oreilly.com/) ( *программирование Google App Engine* , если вам интересно). Эти инструменты разработаны и протестированы вокруг рабочего процесса O'Reilly и стиля дома. Scriv2DocBook не обязательно подходит для всех проектов DocBook во всех ситуациях.

Как и большинство самодельных инструментов для авторов книг, Scriv2DocBook представляет собой способ работы, который мне подходит, и он может вас не устраивать. Я представляю это публично, потому что люди, заинтересованные в том, чтобы что-то подобное, спросили меня об этом.

Требуется знакомство с DocBook XML и соответствующими средствами командной строки.

## Установка Scriv2DocBook

Чтобы использовать Scriv2DocBook, вам необходимо следующее:

- [Scrivener](http://www.literatureandlatte.com/scrivener.php) , версия 2 или новее. Импорт DocBook требует Scrivener 2.1.1 или новее из-за ошибки в OPML-импорте Scrivener, которая была исправлена в этой версии.
- [Xmllint](http://xmlsoft.org/xmllint.html) , средство [проверки](http://xmlsoft.org/xmllint.html) XML-команд командной строки. (Пользователи Mac, у вас уже есть это.)
- [Python](http://www.python.org/) , версия 2.5 или новее. (Пользователи Mac, у вас уже есть это.)
- [Файлы схемы DocBook 4.4](http://www.docbook.org/xml/4.4/docbook-xml-4.4.zip) (zip). (Я не тестировал проверку с помощью DocBook 5, а в архиве схемы DocBook 5 не содержится `catalog.xml`файл `xmllint`. Предложения приветствуются.)

[Загрузите Scriv2DocBook](http://www.dansanderson.com/scriv2docbook/scriv2docbook.zip) и распакуйте архив. В архив входят команды `s2d`и `d2s`команды, которые предназначены для запуска из распакованного каталога.

## Настройка Scrivener

По умолчанию Scrivener действует как редактор «богатого текста», предлагая шрифты с переменной шириной и скромные возможности форматирования, такие как полужирный и курсивный текст. Он также позволяет по умолчанию автоматически использовать типографские символы («умные кавычки»). Эти функции мешают назначению Scriv2DocBook, и лучше отключить их. Вы также захотите использовать шрифт с фиксированной шириной, чтобы упростить чтение встроенных XML-тегов.

1. Откройте панель настроек (для Mac выберите меню **Scrivener** , **Настройки ...** ). На вкладке «Форматирование» в линейке «Стоп-стоп» над образцом текста возьмите маркер абзаца абзаца (маленький прямоугольник) и перетащите его целиком влево, поэтому абзацы не отступаются.

2. Откройте селектор шрифтов (нажмите кнопку «A»), затем выберите «Courier New» или ваш любимый семейство шрифтов с фиксированной шириной. Выберите шрифт и размер шрифта, если хотите.

   ![img](https://www.dansanderson.com/scriv2docbook/README_images/preferences_formatting.png)

3. На вкладке «Исправления» снимите флажок «Использовать интеллектуальные кавычки», «Заменить двойные дефисы с помощью em-тире» и «Заменить тройные периоды эллипсами». Они должны быть сняты, чтобы предотвратить случайное повреждение атрибутов DocBook XML и исходного кода компьютера в тексте, Который должен использовать «прямые кавычки». О'Рейли фактически хочет использовать типографские символы (например, умные кавычки) в источнике DocBook XML для прозы, но инструментальная цепочка O'Reilly заменяет их автоматически и в соответствующих местах при отправке текста.

   Отмените выбор других параметров, если хотите. Лично я оставляю «Проверять орфографию при вводе новых проектов» и отключать все остальное. Цель состоит в том, чтобы заставить Scrivener вести себя как текстовый редактор, насколько это возможно.

   ![img](https://www.dansanderson.com/scriv2docbook/README_images/preferences_corrections.png)

4. На вкладке «Импорт / экспорт» в разделе OPML «Импорт заметок в» подтвердите, что выбран «Основной текст (с синопсисом)». (Это значение по умолчанию).

   ![img](https://www.dansanderson.com/scriv2docbook/README_images/preferences_import_export.png)

См. Также раздел 21.6 руководства Scrivener (выберите меню « **Справка»** , « **Руководство Scrivener»** ), в котором описывается, как сделать что-то подобное для целей MultiMarkdown (другой вариант экспорта Scrivener).

## Написание книги

С помощью Scriv2DocBook вы используете разделы Scrivener для определения структуры вашей книги. При экспорте иерархия разделов Scrivener преобразуется в иерархию глав и разделов DocBook.

Содержание каждого раздела - DocBook XML, с одним основным исключением: абзацы. Чтобы избежать загромождения дисплея `<para>`тегами, Scriv2DocBook распознает блоки текста, разделенные пустой строкой в виде абзацев, и добавляет `<para>`теги во время экспорта.

![img](https://www.dansanderson.com/scriv2docbook/README_images/binder_and_paragraphs.png)

Все остальное, что появляется в тексте, рассматривается как буквальный DocBook XML. Встроенные элементы отображаются непосредственно в тексте абзаца. Элементы блока могут быть отделены от окружающих абзацев пустыми строками и в противном случае появляться в виде окончательного XML.

![img](https://www.dansanderson.com/scriv2docbook/README_images/block_element.png)

### Главы и предисловия

Секции Scrivener верхнего уровня в вашем проекте становятся главами. Каждая глава получает `<chapter>`элемент в выходе XML. Внутренние разделы становятся подразделами глав, в иерархии, представленной в проекте Scrivener; Эти элементы использования .`<sect*#*>`

DocBook имеет специальный элемент для предисловия глав: `<preface>`. Scriv2DocBook будет использовать `<preface>`элемент только в том случае, если заголовок главы `Preface`. Во всех других случаях он использует `<chapter>`.

Scriv2DocBook знает, как создавать предисловия, главы и разделы. Он не поддерживает «части» (уровень иерархии над главами).

### Заголовки и идентификаторы разделов

Главы и разделы имеют названия. Scriv2DocBook использует название раздела Scrivener в качестве названия главы или раздела.

В главах и разделах также есть XML-идентификаторы, которые появляются в источнике XML в качестве `id="..."`атрибутов. Эти атрибуты используются при создании перекрестных ссылок в тексте. Scriv2DocBook автоматически генерирует эти идентификаторы на основе заголовков разделов. Это делается путем замены всех символов, которые не являются буквами или цифрами с символами подчеркивания.

Например, в главе с названием «Объекты, ключи и свойства» есть идентификатор `Entities__Keys__and_Properties`. Обратите внимание, как символы и знаки пунктуации становятся символами подчеркивания. Этот раздел будет упоминаться в тексте с `<xref>`элементом, например:

```
Дополнительные сведения о ключах см. В разделе <xref linkend = "Entities__Keys__and_Properties" />.
```

Идентификатор должен быть уникальным для всех идентификаторов во всем документе. Если Scriv2DocBook находит несколько разделов с одним и тем же заголовком, он генерирует идентификаторы, добавляя число в конце идентификатора, где номер является последовательным в том порядке, в котором разделы отображаются в документе. Например, если каждая из ваших глав заканчивается секцией, озаглавленной «Упражнения», идентификатор первого раздела `Exercises`, второй - `Exerises_1`третий `Exercises_2`, и т. Д.

Это ошибка проверки XML, если атрибут `<xref>`s `linkend`ссылается на идентификатор элемента, который не существует в документе. Scriv2DocBook сообщает об ошибках при проверке вывода. Эти ошибки могут быть трудными для устранения неполадок. Возможно, вы захотите изучить сгенерированный вывод, чтобы подтвердить, что генерируется ID Scriv2DocBook для проблемного раздела.

### Блочные элементы

Как показано выше, вы добавляете абзацы в раздел вашего документа Scrivener, введя их напрямую, опустив `<para>`теги и разделив каждый абзац пустой строкой. Чтобы добавить другой вид элемента блока, например a `<table>`, отделите его от предыдущего и последующих абзацев с пустыми строками.

```
Предложение <code> WHERE </ code> эквивалентно одному или нескольким
фильтры. Это не похоже на предложение SQL <code> WHERE </ code>
И не поддерживает произвольные логические выражения. В частности, это
Не поддерживает тестирование логического-ИЛИ двух условий.

Значение в правой части условия может быть буквальным значением
Который появляется внутри строки запроса. Семь значений хранилища данных
Типы имеют строковые литералы, как показано в <xref
LINKEND = "gql_value_literals" />.

<Table id = "gql_value_literals">
  <Title> Литералы значений GQL для типов хранилищ данных </ title>
  <Tgroup cols = "3">
    <Colspec colname = "c1" />
    <Colspec colname = "c2" />
    <Colspec colname = "c3" />
    <THEAD>
      <Строка>
        <Запись> Тип </ запись>
        <Entry> Литеральный синтаксис </ entry>
        ...
```

### Элементы блока, содержащие параграфы

Некоторые элементы блока могут содержать (или должны) абзацы, такие как `<note>`или `<listitem>`. В этих случаях вы должны ввести теги `<para>`и `</para>`теги, как и в любом другом документе XML. Scriv2DocBook `<para>`автоматически добавляет теги для абзацев верхнего уровня.

```
<Примечание>
  <Para> Обязательно используйте журнал <code> </ code>
  (Например, <code> FINEST </ code>), а не приложение
  Имя уровня двигателя для значений в
  <Имя файла> logging.properties </ имя_файла>. Журнал приложений
  Уровни влияют только на то, как сообщения представлены в Admin
  Консоль. </ Пункт>
</ Примечание>
```

### Другие особенности XML и DocBook

Помимо разделов и секций уровня, ваш проект Scrivener - это просто DocBook XML. Scriv2DocBook берет то, что вы вводите в свой проект, и переносит его непосредственно в документ XML. Результат должен быть действительным XML, а Scriv2DocBook проверяет, что он есть, и сообщает об ошибках.

Легко забыть, что текст, который вы вводите в проект Scrivener, будет интерпретироваться как XML, тем более, что ваш документ опускает структурные теги и `<para>`теги. В частности, вы должны помнить, что символы со специальным значением для XML должны быть набраны как объекты XML, особенно в таких регионах, как образцы кода. Следите за этими тремя персонажами:

| Левая угловая скобка («меньше»)     | `<`  | `&lt;`  |
| ----------------------------------- | ---- | ------- |
| Прямоугольная скобка ("больше чем") | `>`  | `&gt;`  |
| амперсант                           | `&`  | `&amp;` |

Обратите внимание, что вы также должны использовать объекты XML в заголовках разделов, если хотите, чтобы они отображались как символы. Разметка DocBook обычно не допускается в заголовках как предмет стиля.

Также поддерживаются другие функции, такие как элементы, содержащие предварительно отформатированный текст ( `<programlisting>`) и XML. Просто введите их так, как они должны появиться в конечном документе XML в проекте Scrivener.

## Экспорт DocBook XML

Когда у вас есть проект вашего проекта, который вы хотите экспортировать в DocBook, вы используете функцию экспорта Scrivener OPML и `s2d`инструмент для создания DocBook XML.

Чтобы экспортировать проект Scriv2DocBook в формате DocBook XML:

1. В Scrivener выберите главы, которые вы хотите экспортировать. Вы можете сделать это одним из двух способов:

   - Выберите каждый из отдельных разделов верхнего уровня для экспорта, удерживая клавишу командной строки (Mac OS X) или клавишу управления (Windows), а затем выберите несколько вариантов. Каждый раздел, который вы выбираете, становится главой в результате.
   - Выберите раздел «Черновик». Если экспорт содержит только один раздела также Он называется «Черновик», тогда каждый из разделов внутри «Черновик» становится главой в результате.

   ​

2. Выберите меню « **Файл»** , « **Экспорт ...»** , « **Файл OPML ...»** . В диалоговом окне выберите местоположение и введите имя файла. Выберите **заголовки и текст** . Убедитесь, что **экспорт всего связующего** не проверен. Нажмите « **Экспорт»** .

3. В командной строке (например, Mac OS X Terminal) запустите `s2d`команду с экспортированным файлом OPML, путь к выходному каталогу и путь к файлам схемы DocBook с помощью `--schema-dir`аргумента. Это может выглядеть примерно так:

   ```
   ./scriv2docbook/s2d mybook.opml mybook --schema-dir = docbook-xml-4
   ```

   Scriv2DocBook преобразует проект в файлы DocBook XML в данном каталоге (например `mybook/`). Он также проверяет XML. Если XML-ошибки не сообщаются, то XML действителен.

Если вы экспортируете свой проект в первый раз в пустой каталог, обязательно отредактируйте `book.xml`файл, чтобы обновить `<title>`тег с фактическим названием вашей книги.

Если вы пишете O'Reilly, вы можете экспортировать свой проект непосредственно в каталог клиента SVN, содержащий файлы шаблонов, которые O'Reilly предоставил вам для своей книги. `s2d`Сохраняет элементы, `book.xml`не связанные с включением глав.

### Как организован XML

Экспортированный XML-проект состоит из нескольких файлов: `book.xml`файла, представляющего структуру книги, и одного файла для каждой главы. Файлы разделов называются как числом, так и идентификатором главы, чтобы упростить трассировку ошибок проверки XML обратно в проект Scrivener.

Вот файлы для моей книги:

```
book.xml
ch00_Preface.xml
ch01_Introducing_Google_App_Engine.xml
ch02_Creating_an_Application.xml
ch03_Handling_Web_Requests.xml
ch04_Datastore_Entities.xml
ch05_Datastore_Queries.xml
ch06_Datastore_Transactions.xml
ch07_Data_Modeling_with_Python.xml
ch08_The_Java_Persistence_API.xml
ch09_The_Memory_Cache.xml
ch10_Fetching_URLs_and_Web_Resources.xml
ch11_Sending_and_Receiving_Mail_and_Instant_Messages.xml
ch12_Bulk_Data_Operations_and_Remote_Access.xml
ch13_Task_Queues_and_Scheduled_Tasks.xml
ch14_The_Django_Web_Application_Framework.xml
ch15_Deploying_and_Managing_Applications.xml
```

`book.xml`Файл содержит корневой элемент DocBook, книжный `<title>`элемент и директиву XInclude , которые ссылаются на файлы для каждой главы. Например:

```
<? Xml version = "1.0"?>
<! DOCTYPE book PUBLIC "- // OASIS // DTD DocBook XML V4.4 // EN" "http://www.oasis-open.org/docbook/xml/4.4/docbookx.dtd">

<Book id = "I_book_d1e1">
  <Title> Программирование Google App Engine </ title>
  <Xi: включить xmlns: xi = "http://www.w3.org/2001/XInclude" href = "bookinfo.xml" />
  <Xi: include xmlns: xi = "http://www.w3.org/2001/XInclude" href = "dedication.xml" />
  <Xi: include xmlns: xi = "http://www.w3.org/2001/XInclude" href = "ch00_Preface.xml" />
  <Xi: include xmlns: xi = "http://www.w3.org/2001/XInclude" href = "ch01_Introducing_Google_App_Engine.xml" />
  <Xi: включить xmlns: xi = "http://www.w3.org/2001/XInclude" href = "ch02_Creating_an_Application.xml" />
  <Xi: include xmlns: xi = "http://www.w3.org/2001/XInclude" href = "ch03_Handling_Web_Requests.xml" />
  <! - ... ->
  <Индекс />
  <Xi: включить xmlns: xi = "http://www.w3.org/2001/XInclude" href = "colo.xml" />
</ Книга>
```

Если вы экспортируете в каталог, который уже содержит DocBook XML в этой структуре, `s2d`пытается сохранить содержимое `book.xml`и просто заменяет строки, связанные с включением глав. Любой найденный файл главы, имеющий тот же порядковый номер и идентификатор, что и экспортируемая глава, будет перезаписан новым текстом. Все остальные файлы сохранены.

Если `s2d`файлы старого главы используются с использованием этого соглашения об именах, но больше не используются проектом, они не будут удалять их. Вместо этого он отобразит команды, которые вы можете запустить, чтобы удалить файлы. Если ваш выходной каталог является SVN-клиентом, он отобразит команды SVN, необходимые для этого.

## Импорт проекта DocBook в Scrivener

Вы можете использовать этот `d2s`инструмент для импорта проекта DocBook в Scrivener.

**Примечание** . Текущая версия `d2s`не использует настоящий синтаксический анализатор XML, поэтому результаты могут отличаться. Он поддерживает макет, сгенерированный `s2d`( `book.xml`файл с директивами XInclude для каждой из глав), который также является макетом шаблона проекта O'Reilly. Он не поддерживает XInclude в другом месте документа. Инструмент поддерживает однофайловые данные DocBook XML. Он поддерживает `<sect#>`теги, но не вложенные `<section>`теги.

Чтобы импортировать (соответствующий) проект DocBook:

1. Если необходимо, создайте новый проект Scrivener, убедившись, что он использует указанную выше конфигурацию (моноширинные шрифты и т. Д.) Для новых тем.

2. В командной строке (например, Mac OS X Terminal) запустите `d2s`команду в своих данных DocBook, чтобы создать файл OPML. Это может выглядеть примерно так:

   ```
   ./scriv2docbook/d2s mybook / book.xml mybook.opml
   ```

3. Найдите файл OPML в браузере файлов вашего компьютера (например, Mac OS X Finder) и перетащите его в Binder вашего проекта Scrivener. Перед тем, как отпустить, выровняйте индикатор вставки, где вы хотите, чтобы были созданы новые секции Scrivener. В новом проекте это будет один уровень внутри черновика.

4. При появлении запроса подтвердите диалог «Импорт файлов», нажав кнопку «Импорт». Scrivener создает новые разделы.

5. Сохраните проект.

## Лицензия

Scriv2DocBook является авторским правом © 2011 Dan Sanderson.

Лицензируется по лицензии Apache, версия 2.0 («Лицензия»); Вы не можете использовать этот файл, кроме как в соответствии с Лицензией. Вы можете получить копию Лицензии на

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Если это не предусмотрено действующим законодательством или не согласовано в письменной форме, программное обеспечение, распространяемое по лицензии, распространяется на основе «КАК ЕСТЬ», БЕЗ КАКИХ-ЛИБО ГАРАНТИЙ ИЛИ УСЛОВИЙ ЛЮБОГО ВИДА, явных или подразумеваемых. См. Лицензию на конкретном языке, регулирующем разрешения и ограничения по Лицензии.