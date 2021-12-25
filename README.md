# WebP & Native Lazy Loading плагин для DLE
![DLE](https://img.shields.io/badge/DLE-14-blue.svg "DLE Version")
![License](https://img.shields.io/github/license/shv0/dle-webp-plugin)

**Что делает плагин:**
* При добавлении новости/публикации модуль автоматически создает копиию изображения в формате **.webp**.
* В тег **img** добавлен **loading="lazy"**, который позволяет использовать нативнаую отложенную загрузку изображений на уровне браузера.
* Изображения оформлены по [рекомендациям Google](https://developers.google.com/search/docs/advanced/guidelines/google-images?hl=ru). Также к тегу img, добавлены атрибуты **width** и **height** с значениями размеров уменьшеной копии картинки, для устранения проблем с Cumulative Layout Shift.

**До:**
```html
<img src="/path/to/pic.png" alt="Picture">
```

**После:**
```html
<picture>
	<source type="image/webp" srcset="/path/to/pic.webp">
	<img loading="lazy" src="/path/to/pic.png" alt="Picture" width="" height="">
</picture>
```

Для **старых публикаций**, нужно запустить перестроение публикаций.

**Требования**
- Плагин разрабатывался и тестировался на DLE 14.
- Библиотека PHP GD2.

**Установка**

В админке DLE: **Утилиты — Управление плагинами — Добавить плагин**. 
