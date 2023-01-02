# Название проекта: Научится учится
## Описание проекта:
Это учебный проект для формирования навыков работы с:
* форматирование и верстка HTML страницы с использование CSS по методологии БЭМ
* видео, iframe, embed, API.
* анимаций и трансформацией.
* путей к файлам и организацией файлов по БЭМ.
## Структура проекта:
1. **Шапка страницы (header).**
2. **Основное наполнение страницы (content):**
   * Секция *Главные проблемы в обучении* (description).
   * Секция *Техники обучения* (techniques).
   * Секция *Видео нa TED* (video).
   * Секция *История Барбары Оакли.* (oakley).
   * Секция *Метод Фейнмана* (feynman).
   * Секция *Цифры и факты* (digits).
   * Секция *Салман Хан* (khan).
   * Секция *Принципы обучения от Джоша Кауфмана* (kaufman).
   * Секция *Полезные ресурсы* (resources).
3. **Подвал сайта (footer).**
## Технологии, которые применялись в проекте:
1. Все ссылки на странице при наведении мыши плавно становятся немного прозрачными:
```css
transition: opacity .5s linear;
}
.footer__column-links:hover {
  opacity: 0.5;
}
```
   * Прозрачность 50%.
   * Время перехода 0.5 секунд.

2. Использование iframe контейнера, в который помещаюется информация (видео) с другого сайта ([*YouTube.com*](https://www.youtube.com "YouTube сайт-видеохостинг")).

``` HTML
<div class="video__iframes">
          <iframe id="ytplayer" type="text/html" src="https://www.youtube.com/embed/arj7oStGLkU" frameborder="0"
            allowfullscreen class="video__iframe">
          </iframe>
          <iframe id="ytplayer" type="text/html" src="https://www.youtube.com/embed/5MgBikgcWnY" frameborder="0"
            allowfullscreen class="video__iframe">
          </iframe>
        </div>
```

  * Для вставки видео использовался [*YouTube API-конструктор видео*](https://developers.google.com/youtube/iframe_api_reference?hl=ru "API YouTube"). Он даёт возможность снабдить встраиваемое видео атрибутами вне стандартов HTML.
  * Ссылка на видео [ _Tim Urban: Inside the mind of a master procrastinator_](https://www.youtube.com/watch?v=arj7oStGLkU)
  * Ссылка на видео [ _The first 20 hours -- how to learn anything_](https://www.youtube.com/watch?v=5MgBikgcWnY)

3. Реализована анимация: поворот с равномерной скоростью по часовой стрелке. Фигура поворачивается на 360 ̊  за 20 секунд и двигается бесконечно.

``` css
@keyframes rotation {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}
```
  * Использeтся микс, чтобы запустить анимацию там, где нужно.<br>Фигура поворачивается на 360 ̊  за 20 секунд с равномерной скоростью и двигается бесконечно.
``` css
  /*запуск анимации*/
    animation:rotation 20s linear infinite;
}
```
## Планы по доработке проекта:
1. Подключить другие шрифты.
2. Добавить образовательные видео в новый раздел.
3. Улучшить код для кроссбраузерности, добавить вендорные префиксы.
4. Создать форму обратной связи, через которую пользователи, посетители сайта смогут отправлять комментарии.
