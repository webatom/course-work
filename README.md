#### Оглавление
- Введение
- Глава 1. Обзор используемых технологий
  - PlayFramework
  - Ebean ORM
  - Heroku
  - SOA
  - Amazon S3
  - Twitter Bootstrap 3.+
  - MVC
  - MVVM
  - KnockoutJS
  - PostgreSQL
  - LESS
  - TinyMCE or ...
  - AJAX
  - Memcached
- Глава 2. Разработка CMS
  - Требования к функциональности
  - Архитектура
    - ER-диограмма
    - Модули приложения
    - Макеты интерфейса
  - Реализация системы
    - Модель
    - Контроллеры
    - ..
  - Апробация
    - Создание интернет магазина
    - Размещение в облаке Heroku
    - Подключение файлового хранилища Amazon backet
  - Заключение
  - Список литературы
  - Приложения


##### Введение 

Целью данной курсовой является разработка системы управления контентом (Content management system, CMS) в соответствии с принципами архитектуры SOA.

Для достижения данной цели были поставлены следующие задачи:

- Анализ функциональности существующих CMS  
- Формирование требований к CMS-проекту
- Разработка архитектуры системы
- Реализация проекта CMS
- Апробация CMS для создания интернет-магазина

######  Актуальность:
 SOA архитектура позволяет работать в облаке и дает возможности неограниченного масштабирования.

###### Новизна:
 SOA архитектура позволяет работать в облаке и дает возможности неограниченного масштабирования.
 REST API ???

##### Глава 1. Обзор предметной области системы

1.1. Системы управления контентом

Система управления — программа, предоставляющая инструменты для добавления, редактирования, удаления информации на сайте.

Большинство современных CMS имеют модульную архитектуру, что позволяет администратору самому выбирать и настраивать те компоненты, которые ему необходимы.

Типичные модули:
- корзина,
- блог,
- новости,
- опросы,
- поиск по сайту,
- статистика посещений,
- гостевая книга и т. д.

Сайты, организованные посредством системы управления контентом, основаны на следующих технологиях: веб-сервер, хранилище данных (зачастую СУБД, например такие как MySQL или PostgreSQL, однако существуют и noSQL CMS), веб-приложение для обеспечения работы самой системы, визуальный (WYSIWYG) редактор страниц, файловый менеджер с веб-интерфейсом для управления файлами сайта, система управления правами пользователей и редакторов сайта.

Существуют разнообразные системы управления сайтом, среди которых встречаются платные и бесплатные, построенные по разным технологиям. Каждый сайт имеет панель управления, которая является только частью всей программы, достаточной для управления сайтом.

Наиболее распространены следующие технологические платформы, используемые в качестве основы веб-приложения, реализующего работу CMS: PHP, Python, .NET, JAVA.

Существует термин контент-менеджер, обозначающий род профессиональной деятельности — редактор сайта или сотрудника, работающего с CMS.

Большая часть современных систем управления содержимым реализуется в виде визуального (WYSIWYG) редактора — программы, которая создаёт HTML-код из специальной упрощённой разметки, позволяющей пользователю проще форматировать текст.


Основные функции CMS
- Предоставление инструментов для создания содержимого, организация совместной работы над содержимым
-	Управление содержимым: хранение, удаление, соблюдение режима доступа, управление потоком документов и т. п..
-	Публикация содержимого.
-	Представление информации в виде, удобном для навигации, поиска.

Сомыми известными и распространенными являются: Wordpress, openCart, DLE, joomla, 1С-битрикс.

1.2. PlayFramework

PlayFramework — это веб-фреймворк для языков программирования Java и Scala от компании Typesafe. Он использует паттерн проектирования Model-View-Controller  С одной стороны, Play обладает гибкостью и простотой в использовании фреймворков типа Django или Mojolicious, с другой — в нем реализованы многие идеи, например, компилируемость, а следовательно и высокая производительность, строгая строгая типизация и т. д., которые мы можем наблюдать, например, в Yesod.

1.3. Heroku

Heroku — облачная PaaS-платформа, поддерживающая ряд языков программирования. Одна из первых облачных платформ, появилась в июне 2007 года и изначально поддерживала только язык программирования Ruby, но на данный момент список поддерживаемых языков также включает в себя Java, Node.js, Scala, Clojure, Python, Go и PHP. На серверах Heroku используются UNIX операционные системы UNIX такие как Debian и Ubuntu.

1.4. Twitter Bootstrap

Bootstrap — свободный набор инструментов для создания сайтов и веб-приложений. Включает в себя HTML и CSS шаблоны оформления для типографики, веб-форм, кнопок, меток, блоков навигации и прочих компонентов веб-интерфейсов, а также JavaScript расширения.

1.5. Amazon S3

Amazon Simple Storage Service (Amazon S3) — онлайновая веб-служба, предлагаемая Amazon Web Services, предоставляющая возможность для хранения и получения любого объёма данных, в любое время из любой точки сети, так называемый файловый хостинг. С помощью Amazon S3 достигается высокая масштабируемость, надёжность, высокая скорость и недорогая инфраструктура хранения данных.
Amazon S3 используется многими другими сервисами для хранения и хостинга файлов. Например, сервисы хранения и обмена файлов Dropbox и Ubuntu One.

1.6. KnockoutJS

Knockout.js—JavaScript библиотека, которая позволяет создавать сложные пользовательские интерфейсы и при этом оставляет расширяемым и хорошо читабельным. Основная задача, которую выполняет Knockout - это автоматическое обновление пользовательского интерфейса при обновлении свойства в JavaScript модели. 


https://htmlpreview.github.io/?https://raw.githubusercontent.com/supAer0/Site/master/onlyViews/admin/index.html
