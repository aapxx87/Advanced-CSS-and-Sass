__Lecture name: 27. NPM Packages: Let's Install Sass Locally__

  _Link_: https://www.udemy.com/course/advanced-css-and-sass/learn/lecture/8274462#overview


  _Topics_:
  - инициализирцем npm
  - устанавливаем sass компилятор


  _Steps_:

  1)сначала в любом новом проекте нужно инициализировать файл package.json, который содержит параметры нашего проекта и в нем NPM будет записывать пакеты, которые мы будем использовать, то есть мы можем потом легко восстановить все пакеты имея только один данный файл. Для данной инициализации мы в командной строке в папке нашего проекта вводим команду _npm init_  -> дальше можно ввести названия проекта и прочие параметры прямо в командной строке.

  2) теперь нужно установить sass compile - для этого вводим в терминале команду _npm install node-sass --save-dev_ - сохраняем в девелопер зависимости, так как будем использовать для разработки этот пакет -> пакет появляется в package.json в devDependencies

  3) нам не обязательно сохранять папку node modules, главное иметь package.json, из него мы можем потом легко восстановить node modules - для этого достаточно ввести в терминале команду _npm install_

  4) если мы хотим удалить какой-то пакет то используем команду _npm uninstall название-пакета --save_ - --save добавляем, чтобы удалить пакет из файла package.json
<!-- end -->




__28. NPM Scripts: Let's Write and Compile Sass Locally__

  _Link_: https://www.udemy.com/course/advanced-css-and-sass/learn/lecture/8274462#overview


  _Topics_:
  - прописываем sass компилятор и настраиваем процесс конвертации css в sass


  _Steps_:
  1) создаем папку в корневом каталоге, где будем хранить sass файлы - sass
  2) в sass создаем файл main.scss
  3) весь код из style.css переносим в main.scss
  4) main.scss - добавим переменные для цвета и заменим на них в цвета .header
  5) package.json - скомпилируем код из scss в css, используем для это часть scripts. Удаляем предустановленный скрипт "test": "echo \"Error: no test specified\" && exit 1" и вместо него пишем наш:

  _"compile:sass"_ - название скрипта (может быть произвольным) и затем саму команду: _"node-sass sass/main.scss css/style.css -w"_ (-w - flag watching, мониторинг изменений и апдейт css на лету)

  итог: _"compile:sass": "node-sass sass/main.scss css/style.css -w"_

  где node-sass - имя пакета, дальше определяем входящий sass файл и исходящий css файл

  для запуска компилятора в терминале запускаем команду _npm run compile:sass_ - после этого весь код из main.scss компилируется и заносится в style.css

  Если все ок то видим что-то типа:
  Rendering Complete, saving .css file...
  Wrote CSS to /Users/anatolpd/Documents/GitHub/Advanced-CSS-and-Sass/Section 3. Introduction to sass and NPM/28. NPM Scripts Write and Compile Sass Locally/css/style.css
<!-- end -->
