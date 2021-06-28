__34. Building a Custom Grid with Floats__
_Link_: https://www.udemy.com/course/advanced-css-and-sass/learn/lecture/8274486#overview


_Topics_:
- how to architect and build a simple grid system
- how the attribute selector works
- how the :not pseudo-class works
- How calc() works, and what's the difference between calc() and simple Sass operations


- создаем тестовый шаблон сетки float layout - simple float grid


_Steps_:
1) index.html - создаем разметку для сетки
2) создаем новый файл для сетки в папке layout - _grid.scss - импортируем его в main.scss
3) _grid.scss - пишем стили
3.1) _variables.scss - variable for grid - ширина и отсуп снизу
3.2) mixins.scss - все элементы в row float, поэтому у самой row пропадает ширина, для решения этой проблемы используем hack clearfix
