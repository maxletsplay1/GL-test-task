## Настройка

```bash
npm install
```


---

## Запуск дев сервера

```bash
npm run dev
```


---

## Цель приложения

Создание одностраничного фронтенд-приложения, которое при нажатии на кнопку генерирует расклад из 5 случайных карт Таро. Каждая карта содержит изображение, название и описание.


---

## Структура данных

Все карты хранятся в JSON-файле `assets/cards.json`. Каждая карта представлена объектом следующего вида:

{   

 	"id": 0,
	"name": "Башня",   
	"description": "Резкие перемены, разрушение старого, внезапные события.",   
	"picture": "/images/the-tower.jpg"
 
}


---

## Интерфейс приложения

### Основные элементы:
- Кнопка **«Сделать расклад»**.
- Область расклада с пятью картами, отображающимися горизонтально.
- Под каждой картой — название.
- При наведении мыши на карту появляется всплывающее описание.


---

## Логика работы

1. При загрузке страницы JSON с картами загружается один раз и сохраняется в состоянии.

2. При нажатии на кнопку **«Сделать расклад»**:
    - Очищается текущий расклад.
    - Из массива карт выбираются 3 случайные, **без повторений**
    - Отображаются 3 карточки поочередно с задержкой на усмотрение(от 0,5с до 2с) с изображением и названием. Появление надо анимировать.
    - При наведении на любую карту показывается описание (в виде tooltip, всплывающего блока или оверлея на самой карте).
    - Кнопка меняет текст на "изменить судьбу".


---

## Технологии

- **NUXT** с Composition API.
- Модули для **Nuxt**:
	- UI - [primevue](https://nuxt.com/modules/primevue)
	- Стили — [Tailwind CSS](https://nuxt.com/modules/tailwindcss)
- Анимации можно любой **JS** либой, плагином для **NUXT** или через CSS🫣


---

## Как выполнить задание
1. **Форкнуть** основной репозиторий с шаблоном проекта на свой GitHub-аккаунт.
2. В своем форке **создать новую ветку**.
3. **Реализовать функциональность** приложения в этой ветке
4. Закоммитить изменения и **запушить ветку** на GitHub.
5. **Создать Merge Request (Pull Request)** из своей ветки в `main` **основного репозитория** (откуда был сделан форк).
