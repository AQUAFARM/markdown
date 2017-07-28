# Приступая к работе с Grunt

[Главная](https://webref.ru/) / [Веб-технологии](https://webref.ru/dev) / Приступая к работе с Grunt /

[0 комментариев](https://webref.ru/dev/grunt-getting-started#disqus_thread)

![Grunt](https://webref.ru/assets/images/getting-started-with-grunt/grunt.png)

Во время процесса веб-разработки возникает много задач, которые нам требуется периодически выполнять. Это задачи вроде минимизации JavaScript и CSS-файлов, модульного тестирования, проверки файлов на наличие ошибок, компиляции препроцессорных файлов (Less, Sass) в CSS и многое другое. [Grunt](http://gruntjs.com/) предназначен для запуска задач, а значит повторяющиеся задачи, с которыми мы имеем дело каждый день, становятся **автоматизированы**. Это лишь простой взгляд на то, как запускается и работает Grunt. Мы рассмотрим как выполнять следующие основные задачи:

- анализ JS-файлов;
- минимизация JS-файлов;
- компиляция Less-файлов;
- минимизация CSS-файлов;
- отслеживание изменения файлов и выполнение вышеперечисленных задач.

Исходные файлы вы можете [взять из хранилища GitHub](https://github.com/scotch-io/grunt-getting-started).

## Быстрый взгляд на Grunt в действии

Предположим, что вы хотите проверить свой JavaScript-файл на наличие ошибок. После установки Grunt просто запустите:

```
$ grunt jshint
```

И вы увидите ошибки в файлах JavaScript!

![img](https://webref.ru/assets/images/getting-started-with-grunt/grunt-jshint.png)

Использовать Grunt довольно просто. Только установите его, а затем запустите желаемую задачу. Grunt **выполнит** задачу за вас. Это то, что официальный сайт Grunt называет запуском задач.

## Делаем всё супер просто

Существует много учебников, в них говорится о замечательных вещах которые вы можете делать с Grunt. Это хорошие учебники, но порой они могут запутать масштабными настройками людей, только начинающих знакомиться с Grunt. **Это же руководство по основам Grunt** и созданию невероятно простых и легко настраиваемых для управления задач, упомянутых выше. Оно научит вас основам, но позволит задуматься, как мы можем расширить Grunt для будущего продвинутого применения.

## Приступаем к работе

Чтобы использовать Grunt нам требуется уже установленный [Node.js](http://nodejs.org/). Не волнуйтесь, вы можете использовать Grunt в любом желаемом приложении, будь то Node-приложение, PHP-приложение, WordPress или просто старый добрый сайт на HTML/CSS/JS. Node и его менеджер пакетов (npm) применяется для получения необходимых пакетов. Каждый пакет выполняет свою функцию, вроде минимизации или анализа. Если Node ещё не установлен на вашем компьютере, [возьмите](http://nodejs.org/) его и мы начнём работать с Grunt. Чтобы убедиться, что Node и npm у вас установлены, перейдите к командной строке и наберите node -v и npm -v. Если видите номера версий, это значит что вы готовы к работе!

## Обзор

Файлы нашего проекта хранятся довольно просто. Вот структура файлов для примеров, показанная ниже. Начните с создания папок и файлов, но пока оставьте сами файлы пустыми, мы наполним их позже.

```
- dist              // содержит все наши финальные файлы (минимизированные)
----- css
----- js
- src               // хранит исходные файлы
----- css
---------- style.css
---------- pretty.less
----- js
---------- magic.js
Gruntfile.js        // конфигурация Grunt
package.json        // конфигурация npm (какие пакеты мы тянем)
```

Обратите внимание на папки **src** и **dist**. Все наши рабочие файлы хранятся внутри папки **src**, затем Grunt минимизирует эти файлы и сохраняет их в папку **dist**. Файлы внутри этой папки предназначены для применения на финальном сайте.

## Получение необходимых пакетов для Grunt

При использовании npm мы определяем все необходимые нам пакеты в файле package.json. Давайте перейдём к этому файлу и добавим в него требуемые пакеты. Что делает каждый пакет объясним позже.

```
// package.json

{
  "name": "grunt-getting-started",
  "version": "0.1.0",
  "devDependencies": {
  "grunt": "~0.4.4",
  "grunt-contrib-jshint": "latest",
  "jshint-stylish": "latest",
  "grunt-contrib-uglify": "latest",
  "grunt-contrib-less": "latest",
  "grunt-contrib-cssmin": "latest",
  "grunt-contrib-watch": "latest"
  }
}
```

Здесь мы определили имя нашего проекта через name, его версию (version) и необходимые пакеты (devDependencies). На первый взгляд это выглядит загадочно, особенно для того, кто ранее ещё не работал с Node и npm, но скоро вы поймёте, что npm — очень классный менеджер пакетов для проекта.

## Пакеты Grunt

Вы удивитесь узнав, что все эти пакеты grunt-contrib-**** делают. Вот сведённые в таблицу популярные пакеты.

| Плагин                                   | Описание                                 |
| ---------------------------------------- | ---------------------------------------- |
| [contrib-jshint](https://www.npmjs.org/package/grunt-contrib-jshint) | Валидация файлов через jshint.           |
| [contrib-uglify](https://www.npmjs.org/package/grunt-contrib-uglify) | Минимизация JS-файлов с помощью UglifyJS. |
| [contrib-watch](https://www.npmjs.org/package/grunt-contrib-watch) | Запуск задач, которые следят за изменением файлов. |
| [contrib-clean](https://www.npmjs.org/package/grunt-contrib-clean) | Очистка файлов и папок.                  |
| [contrib-copy](https://www.npmjs.org/package/grunt-contrib-copy) | Копирование файлов и папок.              |
| [contrib-concat](https://www.npmjs.org/package/grunt-contrib-concat) | Объединение файлов в один.               |
| [contrib-cssmin](https://www.npmjs.org/package/grunt-contrib-cssmin) | Сжатие CSS-файлов.                       |
| [contrib-less](https://www.npmjs.org/package/grunt-contrib-less) | Компиляция Less-файлов в CSS.            |
| [contrib-imagemin](https://www.npmjs.org/package/grunt-contrib-imagemin) | Уменьшение PNG, JPG и GIF.               |
| [contrib-compass](https://www.npmjs.org/package/grunt-contrib-compass) | Компиляция Sass в CSS через Compass.     |
| [contrib-htmlmin](https://www.npmjs.org/package/grunt-contrib-htmlmin) | Минимизация HTML-файлов.                 |

Для получения полного списка пакетов посетите [хранилище плагинов Grunt](http://gruntjs.com/plugins). Теперь, когда мы определили нужные нам пакеты, давайте их установим.

## Установка пакетов

После подготовки файла package.json перейдите в командную строку и наберите:

```
$ npm install
```

Вы увидите, что npm делает своё дело и тянет эти пакеты в недавно созданную папку** node_modules**. Теперь у нас есть эти пакеты и они готовы к использованию в проекте. Установка завершена, так что давайте перейдём к настройке задач для Grunt!

[Grunt](https://webref.ru/metki/grunt)](http://htmlbook.ru/metki/grunt)









# Установка и настройка Grunt

[Главная](https://webref.ru/) / [Веб-технологии](https://webref.ru/dev) / [Приступая к работе с Grunt](https://webref.ru/dev/grunt-getting-started) / Установка и настройка Grunt /

[1 комментарий](https://webref.ru/dev/grunt-getting-started/setup#disqus_thread)

Чтобы задать настройки для Grunt мы воспользуемся файлом Gruntfile.js. Это то место, где по умолчанию хранится конфигурация для запуска.

### Базовый Gruntfile

Перейдём к Gruntfile.js и добавим в него основные вещи, которые нужны для нашего проекта.

```
// Gruntfile.js

// наша функция-обёртка (требуется для Grunt и его плагинов)
// все настройки располагаются внутри этой функции
module.exports = function(grunt) {

  // ===========================================================================
  // НАСТРОЙКА GRUNT ===========================================================
  // ===========================================================================
  grunt.initConfig({

    // получить конфигурацию из package.json 
    // так мы можем использовать штуки вроде name и version (pkg.name)
    pkg: grunt.file.readJSON('package.json'),

    // вся наша конфигурация будет здесь
 
  });
 
  // ===========================================================================
  // ЗАГРУЗКА ПЛАГИНОВ GRUNT ===================================================
  // ===========================================================================
  // мы можем их загрузить, только если они находятся в нашем package.json
  // убедитесь, что вы запустили npm install, чтобы наше приложение могло их найти
  grunt.loadNpmTasks('grunt-contrib-jshint');
  grunt.loadNpmTasks('grunt-contrib-uglify');
  grunt.loadNpmTasks('grunt-contrib-less');
  grunt.loadNpmTasks('grunt-contrib-cssmin');
  grunt.loadNpmTasks('grunt-contrib-watch');

};
```

 

Будем использовать функцию module.exports (обёртка). Это способ показать нашу конфигурацию остальной части приложения. Не беспокойтесь чересчур по этому поводу, но если вам интересно прочитайте эту [замечательную статью](http://openmymind.net/2012/2/3/Node-Require-and-Exports/) по теме. Внутри grunt.initConfig() получаем информацию из package.json и сохраняем её в pkg. За счёт этого допустимо использовать атрибуты из нашего файла package.json. Можно вызвать имя проекта используя pkg.name и версию через pkg.version. Можно расширить и даже добавить автора. **Зачем это надо?** Хороший вопрос. Мы увидим как применять это дальше, но одна из классных штук, которую можно делать — это использовать упомянутые атрибуты для добавления комментариев в верхней части файлов с названием проекта, автором, датой создания и версией! Довольно наглядно. Также загружаем необходимые плагины Grunt через grunt.loadNpmTasks(). Это способ применения плагинов, которые мы получили ранее через npm.

### Настройка пакета

Базовая конфигурация Grunt готова и теперь взглянем на настройки одного из наших пакетов. Начнём с пакета JSHint который анализирует наши файлы JavaScript и сообщит о возникновении каких-либо ошибок. Это способ указать Grunt, какие файлы мы хотим анализировать, минимизировать или сделать с ними что-то ещё. Для настройки пакета переходим в раздел grunt.initConfig(), который содержит следующую базовую структуру:

```
// Gruntfile.js

grunt.initConfig({

  // настройка jshint для валидации JS-файлов
  jshint: {
    options: {
      reporter: require('jshint-stylish') // используйте jshint-stylish для наглядного представления ошибок
    },

    // при запуске этой задачи анализируется файл Gruntfile.js и все JS-файлы в src
    build: ['Gruntfile.js', 'src/**/*.js']
  }

});
```

Это основной формат для настройки наших пакетов. В нём происходит:

- Вызов пакета по его имени (jshint).
- Настройка параметров, если они нужны. Обычно их можно найти в документации для каждого конкретного пакета.
- Создание атрибута build и переход к файлам, папкам или куда-то ещё при желании.

### Соглашения по именам

При обозначении задач мы назовём нашу главную задачу build. Вы можете назвать её как пожелаете и к тому же создать несколько задач. При запуске Grunt все задачи будут выполнены автоматически. Если вы хотите создать задачи через настройку jshint, то можете назвать их dev и production. Тогда позднее мы можем вызвать задачу через jshint:dev или jshint:production. Теперь, когда мы рассмотрели базовую настройку пакета Grunt, перейдём к конфигурации наших задач.

## Анализ JavaScript-файлов

Вот конфигурация для анализа файлов JavaScript. Она такая же, как и в приведённом выше примере. Мы также обращаемся к пакету jshint-stylish, чтобы получить наглядный вывод ошибок.

```
// Gruntfile.js

grunt.initConfig({

  // настройка jshint для валидации JS-файлов
  jshint: {
    options: {
      reporter: require('jshint-stylish') // используйте jshint-stylish для наглядного представления ошибок
    },

    // при запуске этой задачи анализируется файл Gruntfile.js и все JS-файлы в src
    build: ['Gruntfile.js', 'src/**/*.js']
  }

});
```

Добавим некоторый JS в файл src/js/magic.js.

```
// src/js/magic.js

var hello = 'Я есть Grunt!'

var awesome = 'Да, это здорово!'
```

Теперь если мы выполним

```
$ grunt jshint
```

в командной строке, то увидим анализ Gruntfile.js и всех JS-файлов внутри папки **src**.

![img](https://webref.ru/assets/images/getting-started-with-grunt/grunt-jshint-errors.png)

Мы можем указать следить за всеми JS-файлами в нашем приложении, определёнными файлами или всеми файлами в данной папке с помощью ***\*** для всех папок и ***** для всех файлов. С анализом закончили, теперь перейдём к минимизации.

[Grunt](https://webref.ru/metki/grunt)







# Минимизация JavaScript-файлов

[Главная](https://webref.ru/) / [Веб-технологии](https://webref.ru/dev) / [Приступая к работе с Grunt](https://webref.ru/dev/grunt-getting-started) / Минимизация JavaScript-файлов /

[0 комментариев](https://webref.ru/dev/grunt-getting-started/minify-js#disqus_thread)

Будем использовать тот же формат. Вызовем пакет uglify, настроим его и укажем, какие файлы задействовать и создать.

```
// Gruntfile.js
grunt.initConfig({

  // получить конфигурацию из package.json 
  // так мы можем использовать штуки вроде name и version (pkg.name)
  pkg: grunt.file.readJSON('package.json'),

  ...
 
  // настройка uglify для минимизации JS-файлов
  uglify: {
    options: {
      banner: '/*\n <%= pkg.name %> <%= grunt.template.today("yyyy-mm-dd") %> \n*/\n'
    },
    build: {
      files: {
        'dist/js/magic.min.js': 'src/js/magic.js'
      }
    }
  }

});
```

Здесь настраивается параметр с именем banner, он добавит хороший комментарий вверху нашего минимизированного файла. Обратите внимание, что мы используем pkg.name из файла package.json. Внутри build мы определяем файл, который желаем создать (dist/js/magic.min.js) из исходного файла (src/js/magic.js). Нам нужно больше кода в файле, чем просто какие-то две строки сделанных ранее, так что поработаем с гигантским файлом для минимизации. Возьмём jQuery. Скопируйте содержимое [несжатого файла](http://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.js) jQuery и вставьте его в src/js/magic.js. Видите, какой у них классный комментарий в начале файла? Мы сделаем такой же с помощью параметра banner. Теперь пора минимизировать наш файл. Перейдите в консоль и наберите:

```
$ grunt uglify
```

![img](https://webref.ru/assets/images/getting-started-with-grunt/grunt-uglify.png)

Мы уменьшили оригинальный файл размером 360 Кб до скромных 97.1 Кб!

## Минимизация нескольких файлов в один

Можно сделать гораздо больше, чем просто минимизировать единственный файл — взять несколько файлов и уменьшать их все в один выходной файл. Это может ускорить наши сайты, поскольку мы обрабатываем только один JS-файл для посетителей. Настройка нескольких файлов довольно проста:

```
// Gruntfile.js
grunt.initConfig({

 // получить конфигурацию из package.json 
  // так мы можем использовать штуки вроде name и version (pkg.name)
  pkg: grunt.file.readJSON('package.json'),
  ...
 
  // настройка uglify для минимизации JS-файлов
  uglify: {
    options: {
      banner: '/*\n <%= pkg.name %> <%= grunt.template.today("yyyy-mm-dd") %> \n*/\n'
    },
    build: {
      files: {
        'dist/js/magic.min.js': ['src/js/magic.js', 'src/js/magic2.js']
      }
    }
  }

});
```

В данном примере мы берём два указанных файла и минимизируем их в magic.min.js. Можно также применить краткую форму, которую мы узнали ранее и просто сказать минимизировать все JS-файлы в папке **src**. Для этого вы должны использовать src/**/*.js.

[Grunt](https://webref.ru/metki/grunt)



# Компиляция Less в CSS

[Главная](https://webref.ru/) / [Веб-технологии](https://webref.ru/dev) / [Приступая к работе с Grunt](https://webref.ru/dev/grunt-getting-started) / Компиляция Less в CSS /

[0 комментариев](https://webref.ru/dev/grunt-getting-started/less#disqus_thread)

Для этого примера мы воспользуемся Less. Чтобы сделать то же самое для Sass вы можете использовать пакет grunt-contrib-compass. Вот наши настройки для компиляции Less-файлов. Как и в примере с минимизацией JavaScrip в параметрах определяются исходные и выходные файлы.

```
// Gruntfile.js
grunt.initConfig({

 ...
 
  // компиляция Less в CSS
  less: {
    build: {
      files: {
        'dist/css/pretty.css': 'src/css/pretty.less'
      }
    }
  }

});
```

В данном примере мы не устанавливаем какие-либо параметры, просто компилируем файл src/css/pretty.less в dist/css/pretty.css.

Для начала добавим немного Less в наш исходный файл.

```
/* src/css/pretty.less */

@red        : #CC594A;
@yellow     : #B8CC24;
@blue       : #8BC5FF;
@purple     : #6F3596;

body        { 
  background:@red;
  color:@yellow;
}

button      {
  background:@blue;
}

div         {
  background:@purple;
}
```

Мы определили несколько переменных Less и применили их к элементам. Теперь запустим нашу задачу!

```
$ grunt less
```

![img](https://webref.ru/assets/images/getting-started-with-grunt/grunt-less-compile.png)

Создаётся файл dist/css/pretty.css содержащий результат компиляции Less в CSS и теперь он выглядит как обычный стилевой документ.

```
/* dist/css/pretty.css */

body {
  background: #cc594a;
  color: #b8cc24;
}
button {
  background: #8bc5ff;
}
div {
  background: #6f3596;
}
```

Давайте взглянем ещё на пару вещей, которые мы можем сделать с помощью Grunt.

[Grunt](https://webref.ru/metki/grunt)





# Минимизация CSS-файлов

[Главная](https://webref.ru/) / [Веб-технологии](https://webref.ru/dev) / [Приступая к работе с Grunt](https://webref.ru/dev/grunt-getting-started) / Минимизация CSS-файлов /

[0 комментариев](https://webref.ru/dev/grunt-getting-started/minify-css#disqus_thread)

Подобно минимизации JS-файлов настройки для такой задачи довольно простые. Мы уже это проходили, так что создайте такую конфигурацию.

```
// Gruntfile.js
grunt.initConfig({

  ...
  // параметры cssmin для минимизации CSS-файлов
  cssmin: {
    options: {
      banner: '/*\n <%= pkg.name %> <%= grunt.template.today("yyyy-mm-dd") %> \n*/\n'
    },
    build: {
      files: {
        'dist/css/style.min.css': 'src/css/style.css'
      }
    }
  }

});
```

Если теперь мы выполним

```
$ grunt cssmin
```

то получим новый минимизированный файл dist/css/style.min.css.

[Grunt](https://webref.ru/metki/grunt)



# Запуск нескольких задач одновременно

[Главная](https://webref.ru/) / [Веб-технологии](https://webref.ru/dev) / [Приступая к работе с Grunt](https://webref.ru/dev/grunt-getting-started) / Запуск нескольких задач одновременно /

[1 комментарий](https://webref.ru/dev/grunt-getting-started/multiple-tasks#disqus_thread)

После того как мы увидели как работают наши задачи, давайте сделаем нечто более эффективное и выполним всё сразу с помощью только одной задачи. Это гораздо лучше, чем отдельное выполнение grunt uglify, grunt jshint и т. д.

### Задача по умолчанию

С помощью Grunt вы можете создавать задачи, которые будут запускать несколько задач одновременно. Например, мы хотим выполнить все перечисленные выше задачи, просто вызвав grunt. При запуске grunt из командной строки Grunt будет искать задачу с именем default. Давайте создадим её, чтобы узнать как это выглядит.

```
// Gruntfile.js

grunt.initConfig({

  ...

  // ============= // СОЗДАЁМ ЗАДАЧИ ========== //
  grunt.registerTask('default', ['jshint', 'uglify', 'cssmin', 'less']); 

});
```

Теперь просто выполняем:

```
$ grunt
```

и все наши задачи внутри default будут запущены!

Теперь посмотрим, как мы можем определить различные задачи для разных условий.

[Grunt](https://webref.ru/metki/grunt)





# Различные задачи для разных условий

[Главная](https://webref.ru/) / [Веб-технологии](https://webref.ru/dev) / [Приступая к работе с Grunt](https://webref.ru/dev/grunt-getting-started) / Различные задачи для разных условий /

[0 комментариев](https://webref.ru/dev/grunt-getting-started/different-tasks#disqus_thread)

Скажем, мы хотим, чтобы Grunt работал в процессе разработки, а затем, когда мы перейдём к рабочему сайту, нам потребуются другие задачи для выполнения. Мы можем определить несколько задач внутри каждой конфигурации. Например:

```
// Gruntfile.js

grunt.initConfig({

  // получить конфигурацию из package.json 
  // так мы можем использовать штуки вроде name и version (pkg.name)
  pkg: grunt.file.readJSON('package.json'),

  ...

  // параметры uglify для минимизации JS-файлов
  uglify: { 
    options: { 
      banner: '/\n <%= pkg.name %> <%= grunt.template.today("yyyy-mm-dd") %> \n/\n' 
    }, 
    dev: { 
      files: { 'dist/js/magic.min.js': ['src/js/magic.js', 'src/js/magic2.js'] } 
    }, 
    production: { 
      files: { 'dist/js/magic.min.js': 'src/**/*.js' } 
      } 
    }
});
```

Теперь мы можем вызвать их по-разному, используя двоеточие. Давайте создадим задачу для разработки и публикации.

```
// Gruntfile.js

grunt.initConfig({

  // ========= // СОЗДАЁМ ЗАДАЧИ =========
 
  // задача по умолчанию проходит через все конфигурации (dev и production) 
  grunt.registerTask('default', ['jshint', 'uglify', 'cssmin', 'less']);

  // эта задача будет выполняться только для конфигурации dev
  grunt.registerTask('dev', ['jshint:dev', 'uglify:dev', 'cssmin:dev', 'less:dev']);

  // только для конфигурации production
  grunt.registerTask('production', ['jshint:production', 'uglify:production', 'cssmin:production', 'less:production']);

});
```

Теперь мы можем выполнить задачи для разработки запустив:

```
$ grunt dev
```

Или задачи для рабочего сайта запустив:

```
$ grunt production
```

Как видите, мы можем создать несколько конфигураций для наших задач и по разному вызывать их.

И последняя вещь, которую мы сейчас изучим. Будем следить за файлами и запускать Grunt каждый раз при их изменении!

[Grunt](https://webref.ru/metki/grunt)





# Следим за изменениями и запускаем задачи

[Главная](https://webref.ru/) / [Веб-технологии](https://webref.ru/dev) / [Приступая к работе с Grunt](https://webref.ru/dev/grunt-getting-started) / Следим за изменениями и запускаем задачи /

[0 комментариев](https://webref.ru/dev/grunt-getting-started/watching#disqus_thread)

Задача watch будет выполняться каждый раз при изменении и сохранении файла. Всё, что нам надо сделать, это следить за определёнными файлами и сказать что делать, когда эти файлы изменятся. Давайте отойдём от базовой конфигурации build, которую мы использовали ранее и сделаем разделение на стили и скрипты. Мы делаем так потому, что хотим задать разные задачи для каждого типа файлов.

```
// Gruntfile.js

grunt.initConfig({

  ...
  
  // параметры watch для автообновления
  watch: {
  
    // для стилей следим только за CSS и Less-файлами
    // и запускаем less и cssmin: { 
    files: ['src//*.css', 'src//*.less'], 
    tasks: ['less', 'cssmin'] },

    // для скриптов запускаем jshint и uglify 
    scripts: { 
      files: 'src/**/*.js', tasks: ['jshint', 'uglify'] 
    } 
  }

});
```

Мы настроили watch, чтобы следить за файлами стилей и скриптов. В консоли выполните:

```
$ grunt watch
```

![img](https://webref.ru/assets/images/getting-started-with-grunt/grunt-watch-example.png)

Теперь мы можем видеть как Grunt следит за изменениями и выполняет необходимые задачи.

На данном рисунке показано, что JavaScript и CSS-файлы были изменены. Соответствующие задачи выполнились и мы можем переходить к разработке! Это очень мощный инструмент, потому что каждый раз при сохранении файлов мы можем делать их анализ, компилировать Less и даже [минимизировать изображения](https://www.npmjs.org/package/grunt-contrib-imagemin).

## Заключение

Надеюсь, этот упрощённый взгляд на Grunt вдохнёт в вас некоторые идеи о том, как использовать Grunt для конкретного процесса. Начать работать просто — **установите пакет**, **настройте его** и наберите **grunt**! Обязательно посмотрите официальную [документацию](http://gruntjs.com/) и [список плагинов](http://gruntjs.com/plugins), чтобы получить больше идей о применении Grunt.

[Grunt](https://webref.ru/metki/grunt)
