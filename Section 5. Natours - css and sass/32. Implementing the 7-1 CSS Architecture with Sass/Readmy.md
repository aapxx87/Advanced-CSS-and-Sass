__32. Implementing the 7-1 CSS Architecture with Sass__
_Link_: https://www.udemy.com/course/advanced-css-and-sass/learn/lecture/8274478#overview


_Topics_:
- создаем структуру для css стилей



_Steps_:
1) создаем базовую папку для стилей в sass - _base_ -> в ней создаем файл _ _base.scss_ - карйне базовые низкоуровневые параметры: reser, стили для html и тд. partials файлы начинаются с подчеркивания. добавляем так-же _animations.scss, _typography.scss, _utilities.scss

1.1) создаем папку _abstracts_ - сюда мы добавляем код, который не будет конвертироваться в css типа variables, mixins etc - создаем файлы _variables.scss, _mixins.scss, _functions.scss

1.2) создаем папку _components_ для всех компонентов

1.3) создаем папку _layout_ для footer, header и других sections

1.4) создаем папку _pages_ для специфических стилей для различных страниц - в ней создаем файл _home.scss

2) main.scss - добавляем импорт добавленных паршиалс файлов

3) сортируем css код по соответствующим файлам  
