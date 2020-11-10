# Конфиг Grid Slider

JSON массив элементами которого являются объекты - "панели"

```json
[
  {},
  {},
  {}
]
```

## Панель
Панель являет я объектом с ключами, содержащими настройки.

`layout` - тип: строка

* раскладка, "трафарет" панели
* определяет количество отображаемых элементов в

```json
"layout": "4"
```

Всего 8 лейаутов:

* `1` - 1 слот на весь лейаут
* `2-1` - 2 слота, вертикальные
* `2-2` - 2 слота, горизонтальные
* `3-1` - 3 слота, верхний большой
* `3-2` - 3 слота, правый большой
* `3-3` - 3 слота, нижний большой
* `3-4` - 3 слота, левый большой
* `4` - 4 слота, сетка 2 на 2

`elements` - тип: массив объектов

* содержимое панели

```json
"elements": [
  {},
  {},
  {}
]
```

## Содержимое `elements`

```json
{
  "image": "//cdn.shopify.com/s/files/1/0987/2678/files/Event-Calendar_650x650.jpg?v=1587570620",
  "link": "/Calendar",
  "category": "",
  "title": "Events Calendar",
  "snippet": "Check our super handy booking system",
  "timerDate": "2020-10-18 22:00",
  "timerText": "Test"
},
```

`image` - тип: строка

* адрес картинки
* рекомендуется использовать относительные пути
* ~~:heavy_exclamation_mark: всегда требуется использовать строго квадратные картинки. При использовании картинки с неровными пропорциями картинка будет "дёргаться" при наведении~~

`link` - тип: строка

* ссылка на раздел
* рекомендуется использовать относительные пути

`category` - тип: строка

* не обязательное
* верхняя подпись категории

`title` - тип: строка

* не обязательное
* крупный заголовок

`snippet` - тип: строка

* не обязательное
* текст

`timerDate` - тип: строка

* не обязательное
* дата/время окончания таймера обратного отсчёта
* формат `YYYY-MM-DD HH:MM`

`timerText` - тип: строка

* не обязательное
* краткий текст рядом с таймером (1-2 слова)

## Пример конфига

```json
[
  {
    "layout": "3-4",
    "elements": [
      {
        "image": "//cdn.shopify.com/s/files/1/0987/2678/files/Division-New_650x650.png?v=1587567374",
        "link": "/the-division-2/",
        "category": "",
        "title": "",
        "snippet": "",
        "timerDate": "",
        "timerText": ""
      },
      {
        "image": "//cdn.shopify.com/s/files/1/0987/2678/files/Event-Calendar_650x650.jpg?v=1587570620",
        "link": "/Calendar",
        "category": "",
        "title": "Events Calendar",
        "snippet": "Check our super handy booking system",
        "timerDate": "",
        "timerText": ""
      },
      {
        "image": "//cdn.shopify.com/s/files/1/0987/2678/files/Eso-Training-Set_650x650.jpg?v=1587567809",
        "link": "/the-elder-scrolls-online/",
        "category": "TESO",
        "title": "Training Sets",
        "snippet": "Gain 78%\n more EXP with training sets",
        "timerDate": "",
        "timerText": ""
      }
    ]
  },
  {
    "layout": "1",
    "elements": [
      {
        "image": "//cdn.shopify.com/s/files/1/0987/2678/files/nyalotha-entr-edited_650x650.jpg?v=1587650062",
        "link": "/WoW-Retail/Specials/Visions-of-N-zoth/",
        "category": "World of Warcraft",
        "title": "Ny'alotha Mythic Raid is Cross-Realm Now",
        "snippet": "Get the best Ny'alotha Mythic raiding gear and other rewards without the need of server transfer",
        "timerDate": "",
        "timerText": ""
      }
    ]
  },
  {
    "layout": "3-1",
    "elements": [
      {
        "image": "https://mmonster.co/media/7e/fa/12/1604323603/destiny-1x2-1-2b.jpg",
        "link": "/destiny-2/",
        "category": "",
        "title": "",
        "snippet": "",
        "timerDate": "",
        "timerText": ""
      },
      {
        "image": "/cdn.shopify.com/s/files/1/0987/2678/files/High-End-Character_650x650.jpg?v=1589822171",
        "link": "/WoW-Retail/WoW-Gear/",
        "category": "World of Warcraft",
        "title": "Fast 460/470 Gear",
        "snippet": "Prepare your character for the end-game",
        "timerDate": "",
        "timerText": ""
      },
      {
        "image": "//cdn.shopify.com/s/files/1/0987/2678/files/Warzone-Weapons_650x650.jpg?v=1587641906",
        "link": "/Call-of-Duty-Warzone/",
        "category": "COD Warzone",
        "title": "Boosting Service",
        "snippet": "Missions Completion, Weapons, Skins and BattlePass Boost.",
        "timerDate": "",
        "timerText": ""
      }
    ]
  }
]
```
