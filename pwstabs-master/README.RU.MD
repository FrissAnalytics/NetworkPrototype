# [PWS Tabs jQuery Plugin](http://alexchizhov.com/pwstabs)<sup>[1.3.0](#%D0%92%D0%B5%D1%80%D1%81%D0%B8%D1%8F-130-20082015)</sup>

####PWS Tabs адаптивный, функциональный jQuery плагин, с интересными эффектами переключения вкладок выполненных с CSS3.

####PWS TABS теперь адаптивный!
Адаптивность плагина находится в режиме Бета, пожалуйста, помогите протестировать, чтобы найти все возможные недочеты.<br>
![Preview](http://alexchizhov.com/files/themes/ac/page-templates/pwstabs/screenshots/pwstabsresponsive600.jpg) ![Preview](http://alexchizhov.com/files/themes/ac/page-templates/pwstabs/screenshots/pwstabsresponsive600menu.jpg)

## Демо

Онлайн демо(английский): [http://alexchizhov.com/pwstabs](http://alexchizhov.com/pwstabs)

![Preview](http://alexchizhov.com/files/themes/ac/page-templates/pwstabs/screenshots/pwstabs1.2.0.jpg)

## Установка с Bower

`$ bower install pwstabs`


## Документация

### Начало работы

1) Подключите jQuery библиотеку и jQuery PWS Tabs плагин внутри <strong>`<head>`</strong> секции.
```html
<script src="//code.jquery.com/jquery-1.11.2.min.js"</script>

<link type="text/css" rel="stylesheet" href="jquery.pwstabs.css">
<script src="jquery.pwstabs.js"></script>
```

2) Создайте вкладки используя HTML5 `data-pws-*` атрибут, чтобы указать ID и Название вкладок.
```html
<div class="hello_world">

   <div data-pws-tab="anynameyouwant1" data-pws-tab-name="Название вкладки 1">Первая вкладка</div>
   <div data-pws-tab="anynameyouwant2" data-pws-tab-name="Название вкладки 2">Вторая вкладка</div>
   <div data-pws-tab="anynameyouwant3" data-pws-tab-name="Название вкладки 3">Третья вкладка</div>

</div>
```

<strong>`data-pws-tab`</strong> используется для инициализация вкладки и указания ее ID.

<strong>`data-pws-tab-name`</strong> используется для указания Заголовка вкладки.

3) Вызовете плагин на родительском элементе относительно вкладок со 100% шириной и эффектом 'scale'.
```js
jQuery(document).ready(function($){
   $('.hello_world').pwstabs();
});
```

4) Доступные параметры для настройки плагина.
```js
jQuery(document).ready(function($){
   $('.hello_world').pwstabs({

      // scale / slideleft / slideright / slidetop / slidedown / none
      // slace - увеличение
      // slideleft - прокрутка влево
      // slideright - прокрутка вправо
      // slidetop - прокрутка вверх
      // slidedown - прокрутка вниз
      // none - без эффекта
      effect: 'scale', 
 
      // Номер вкладки для отображения по умолчанию
      defaultTab: 1,    
 
      // Установить ширину контейнера
      // Любое значение (размер) (1,2,3.. / px,pt,em,%,cm..)
      containerWidth: '100%',

      // Позиционирование вкладок: horizontal / vertical (горизонтальное / вертикальное)
      tabsPosition: 'horizontal',
 
      // Горизонтальное позиционирование вкладок: top / bottom (верх / низ)
      horizontalPosition: 'top',

      // Вертикальное позиционирование вкладок: left / right (слева / справа)
      verticalPosition: 'left',
      
      // БЕТА: Включить адаптивность контейнера: true / false (!!! БЕТА)
      responsive: false,

      // Доступные темы: default: '' / pws_theme_violet / pws_theme_green / pws_theme_yellow
      // pws_theme_gold / pws_theme_orange / pws_theme_red / pws_theme_purple / pws_theme_grey
      theme: '',
      
      // Поддержка для языков читаемых справа налево (RTL): true / false
      rtl: false

   });
});
```

<p>5) PWS Tabs Plugin поддерживает <strong><a href="http://fortawesome.github.io/" title="Перейти на сайт Font Awesome" target="_blank">Font Awesome 4.4.0</a></strong></p>

<p>5.1) Подключите таблицы стилей Font Awesome из директории /assets:</p>

```html
<link type="text/css" rel="stylesheet" href="../assets/font-awesome/css/font-awesome.min.css">
```

<p>5.2) Используйте HTML5 <strong><code>data-pws-tab-icon</code></strong> атрибут, чтобы установить иконку. Названия иконок можно посмотреть здесь: <a href="http://fortawesome.github.io/Font-Awesome/icons/" target="_blank">Font Awesome Icons</a>.</p>

```html
<div class="hello_world">

  <div data-pws-tab="anynameyouwant1" data-pws-tab-name="Название вкладки 1" data-pws-tab-icon="fa-heart">Первая вкладка</div>
  <div data-pws-tab="anynameyouwant2" data-pws-tab-name="Название вкладки 2" data-pws-tab-icon="fa-star">Вторая вкладка</div>
  <div data-pws-tab="anynameyouwant3" data-pws-tab-name="Название вкладки 3" data-pws-tab-icon="fa-map-marker">Третья вкладка</div>

</div>
```


## Настройки

<table>
<thead>
<tr>
<th>Опция</th>
<th>Стандартно</th>
<th>Описание</th>
<th>Доступные настройки</th>
<th>Тип</th>
</tr>
</thead>
<tbody>
<tr>
<td>effect</td>
<td>scale</td>
<td>Эффект переключения</td>
<td>scale / slideleft / slideright / slidetop / slidedown / none</td>
<td>строка</td>
</tr>
<tr>
<td>defaultTab</td>
<td>1</td>
<td>Выбранная по стандарту вкладка</td>
<td>ID вкладки, начинается с 1 (1,2,3..)</td>
<td>число</td>
</tr>
<tr>
<td>containerWidth</td>
<td>100%</td>
<td>Ширина контейнера со вкладками</td>
<td>Любое значение размера (1,2,3.. / px,pt,em,%,cm..)</td>
<td>строка</td>
</tr>
<tr>
<td>tabsPosition</td>
<td>horizontal</td>
<td>Установить позиционирование</td>
<td>horizontal / vertical</td>
<td>строка</td>
</tr>
<tr>
<td>horizontalPosition</td>
<td>top</td>
<td>Установить горизонтальное позиционирование вкладок</td>
<td>top / bottom</td>
<td>строка</td>
</tr>
<tr>
<td>verticalPosition</td>
<td>left</td>
<td>Установить вертикальное позиционирование вкладок</td>
<td>left / right</td>
<td>строка</td>
</tr>
<tr>
<td>theme</td>
<td>''</td>
<td>Изменить тему оформления вкладок</td>
<td>pws_theme_violet / pws_theme_green<br> pws_theme_yellow / pws_theme_gold<br> pws_theme_orange / pws_theme_red<br> pws_theme_purple / pws_theme_grey<br>pws_theme_dark_violet / pws_theme_dark_green<br> pws_theme_dark_yellow / pws_theme_dark_gold<br> pws_theme_dark_orange / pws_theme_dark_red<br> pws_theme_dark_purple / pws_theme_dark_grey</td>
<td>строка</td>
</tr>
<tr>
<td>responsive</td>
<td>false</td>
<td>!!БЕТА!! Адаптивные вкладки</td>
<td>true / false</td>
<td>логическое</td>
</tr>
<tr>
<td>rtl</td>
<td>false</td>
<td>Поддержка языков справа налево (RTL)</td>
<td>true / false</td>
<td>логическое</td>
</tr>
</tbody>
</table>


## История изменений

### Версия 1.3.0 (20.08.2015)
1) Основные CSS и JS файлы больше не включают номер версии в названии<br>
2) Код почищен и переработан<br>
3) Вкладки теперь имеют короткие классы pws_show и pws_hide взамен старых с названием эффекта<br>
4) Классы стилей теперь применяются к контейнеру, а не вкладкам<br>
5) Новая темная тема для сайтов с белым фоном<br>
6) Исправлена ширина вертикальных вкладок с иконками<br>
7) Исправлены отступы вкладок<br>
8) Папка Font awesome переименована в /font-awesome/<br>
9) Font awesome обновлен до версии 4.4.0

### Версия 1.2.1 (23.01.2015)
1) Чтобы упростить работу со стилями плагина, добавлены SASS файлы в директорию /assets/sass/.<br>
2) Основной файл стилей сгенерирован из нового SASS файла (пара изменений с предыдущей версии).

### Версия 1.2.0 (21.01.2015)
1) Адаптивность плагина.<br>
2) Добавлены темы оформления. 9 цветов на выбор<br>
3) Оптимизирован код плагина.<br>
4) Добавлен файл responsive.html в директорию /examples/.<br>
5) Добавлены примеры цветов в /examples/examples.html

### Версии 1.1.X
1) Базовый функционал плагина
