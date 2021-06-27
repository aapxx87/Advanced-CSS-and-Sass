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
