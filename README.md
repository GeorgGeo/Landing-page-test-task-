# Layout-1

## Требования
> — Соблюдение современных стандартов и требований, _семантичность_, _адаптивность_, _HTML5/CSS3_, _CSS анимация_
---
## Реализация (с помощью каких инструментов)

> - Работа с графическим редактором Photoshop
> - Вёрстка HTML/CSS (включительно <img width="25" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/html/html.png">/CSS3_)
> - Адаптивность, annimation CSS, валидация формы
> - JavaScript
> - jQuery
> - Фреймворк **Bootstrap**
> - **Плагины** (_применены_ _при_ _вёрстке_)
>    - [x] Slickslider
>    - [x] NoUiSlider
>    - [x] Ion.tabs
>    - [x] Progresscircle
>    - [x] Popper(tooltip)
>    - [x] Form Styler
>    - [x] jQuery.selectric
>    - [x] MyScript (script для tabs => см. ниже)
---
## MyScript (Code)
```js
    <script>
      const tabsBtn = document.querySelectorAll('.tabs__nav-btn')
      const tabsItems = document.querySelectorAll('.tabs__item')

      tabsBtn.forEach((item) => {
        item.addEventListener('click', (e) => {
          // save current button
          let currentBtn = item
          // get attribute by click on button
          let tabId = currentBtn.getAttribute('data-tab')
          // select el on id
          let currentTab = document.querySelector(tabId)

          if (!currentBtn.classList.contains('active')) {
            // delete class active (after click pass on all buttons)
            tabsBtn.forEach((item) => {
              item.classList.remove('active')
            })
            //
            tabsItems.forEach((item) => {
              item.classList.remove('active')
            })

            currentBtn.classList.add('active')
            currentTab.classList.add('active')
          }
        })
      })
    </script>
```
---
## Макет
<br>
<img height="500" width="500" src="https://github.com/GeorgGeo/Layout-1/blob/master/web_coder_test.png">
</br>
