# Fasty-slider v1.0
### Simple and fast slider based on CSS transformation
Version 1.0
Early first version / Первая версия слайдера
## Documentation / Руководство
* Необходимая html-структура
* Как подключить
* Настройка
* Внешний вид
---
### Html-структура
Слайдер состоит из контейнера, внутри которого находятся слайды. Класс контейнера может быть произвольным. Класс слайдов должен быть - `.fasty__slide` (два нижних слеша). Количество слайдов - любое.
```html
<div class="elem">
  <div class="fasty__slide"></div>
  <div class="fasty__slide"></div>
  <div class="fasty__slide"></div>
</div>
```
---
###  Как подключить
1. Для начала нужно подключить необходимые файл стилей `fasty.css` или `fasty.min.css`
```css
<link rel="stylesheet" href="css/fasty.min.css">
```
2. Затем необходимо подключить `fasty.js` (`fasty.min.js`) ниже, чем Jquery
```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
<script src="js/fasty.min.js"></script>
```
3. И инициализировать сам скрипт
```html
$('.elem').fasty()  
```
---
### Настройка
Инициализировать слайдер можно, задав начальные параметры таким образом:
```html
$('.elem').fasty({
  option1: 'key1',
  option2: 'key2'
});
```
На данный момент, при инициализации доступны две опции:

**start (String)**

Возможные значения: 
* ``default`` - по умолчанию, обычный порядок слайдов;
* ``reversed`` - показываются не первые три, а последние;

**mode (String)**

Возможные значения: 
* ``normal`` - по умолчанию, слайды можно перелистывать вперед-назад;
* ``sameSize`` - слайды будут одинакового размера;
* ``onlyRight`` - слайды можно листать только в одном направлении, немного другая анимация;

---
### Внешний вид
* Содержимое у слайдов может быть любое.
* Высота слайдов - ``auto``.
* Ширина слайдов по умолчанию ``auto``. Рекомендуемая ширина ``<80%`` от ширины обертки (``.elem``).
* Менять стили слайдов можно, используя класс ``.fasty__slide`` либо любой свой.
* Скорость анимации можно частично менять через
`
.fasty__slide {
  transition: transform 0.8s
}
`, где `0.8s` - время в секундах.
  
