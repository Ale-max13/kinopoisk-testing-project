# Тестирование веб-приложения Кинопоиск 

  

### *Кинопоиск * ([https://www.kinopoisk.ru](https://www.kinopoisk.ru/)) — это мультимедийная платформа для поиска и просмотра информации о фильмах, актёрах, рецензиях и рейтингах.

 Пользователи могут искать фильмы по названию, просматривать подробную информацию о фильме, узнавать об актёрах, смотреть постеры, рейтинги и т.д.

### **Цель тестирования** — убедиться в корректной работе ключевых пользовательских сценариев:  

- поиск фильмов
- просмотр информации о фильме
- просмотр информации об актёре.

  

### **__Объекты тестирования:__**

1. Поиск фильмов по ключевым словам  
2. Страница фильма
3. Страница актёра

### __Виды тестирования:__

- Функциональное
- Smoke-тестирование
- Нефункциональное (UI/UX, производительность, кросс-браузерность — для сайта)  
- API тестирование (по документации <https://kinopoisk.dev>)
- Негативное тестирование

### **__Инструменты:__**

- **Браузер (Chrome, Firefox, Яндекс Браузер, Opera)** — ручное тестирование функционала и UI
- **Qase.io** — оформление smoke-тест-кейсов
- **Google Sheets** — чек-листы и API-тест-кейсы
- **Postman** — выполнение и экспорт API-запросов
- **Yonote** — тест-план, баг-репорты, улучшения
- **OBS Studio / Zoom** — запись видео-защиты проекта

  

## 🎯__Отчёт о тестировании:__

:white_check_mark: Smoke-тестирование сайта .pdf (Qase.io):

[AP-Smoke+test_+Kinopoisk.pdf 52422](attachment:/api/attachments.redirect?id=e5b417c8-acef-433e-b73b-985d140317a9)

**Smoke-тест** успешно завершён: все 3 сценария (поиск, карточка фильма, переход к актёру) выполнены, статус — **Passed**. Претензий к ключевой функциональности нет.  


:white_check_mark: Чек-лист сайта .pdf (Google Sheets):

[Kinopoisk_Чек-лист.pdf 70463](attachment:/api/attachments.redirect?id=92ed895d-2402-49af-a213-80815553d576)


Проверки ключевых функций сайта Кинопоиск - 38 проверок: 

поиск, карточки фильмов и актёров, UI/UX, кросс-браузерность и производительность. Чек-лист разбит по типам тестирования.

   

:white_check_mark: API-коллекция .json (Postman):

[Kinopoisk_FP.postman_collection.json 10847](attachment:/api/attachments.redirect?id=a776a3bd-8b13-4ab4-a116-880ce3e81661)

:white_check_mark: API-test-run .json (Postman - результаты прогона):

[Kinopoisk_FP.postman_test_run.json 7283](attachment:/api/attachments.redirect?id=1b531a2b-6155-4937-9bd5-dba44b487e99)

**Круговая диаграмма, показывающая результаты тест-рана API в Postman:**  

- **70% Passed** — 7 успешных тестов
- **30% Failed** — 3 теста с ошибками

 ![](/api/attachments.redirect?id=30e1c4b6-49d7-40c6-bd55-b434abe4579b "aspect=0.5102040816326538")

:white_check_mark: Коллекция API тест-кейсов .pdf (Google Sheets):

[Kinopoisk_API.xlsx - Тест-кейсы.pdf 74980](attachment:/api/attachments.redirect?id=ef5a8327-9965-4f56-86c0-938dade40d62)

Проведено тестирование API поиска фильмов по названию. Включены позитивные и негативные сценарии: проверка работы с валидными запросами, спецсимволами, пустыми значениями и отсутствием авторизации. Оформлены коллекция тестов, результаты прогона и таблица с тест-кейсами.  


🪲**__Баг-репорты__:**
В рамках API-тестирования составлены 3 баг-репорта (BUG-001 — BUG-003). 

Каждый баг оформлен на отдельной подстранице внутри коллекции **"Тестирование веб-приложения"**. Описаны шаги воспроизведения, ожидаемый и фактический результат, окружение и прикреплены доказательства в виде скриншотов.  


### 🔐 __Инструкция по получению Bearer Token для доступа к API:__

1. Перейти на официальный сайт проекта: <https://kinopoisk.dev>
2. На странице нажать кнопку Telegram-бота: **@kinopoiskdev_bot**
3. В Telegram-боте пройти простую регистрацию, выбрать тариф **FREE**
4. После подтверждения, бот выдаст персональный Bearer Token
5. Токен можно использовать в Postman 
6. При необходимости, можно присоединиться к официальному Telegram-чату сообщества (ссылка в боте)

📌 Token выдаётся мгновенно. Тариф FREE даёт доступ ко всем основным возможностям API для тестирования.


### __Сроки выполнения проекта:__

🕔Временные затраты включали проработку всех этапов тестирования (подготовка кейсов, прогон тестов, оформление багов и документации). Работа выполнялась поэтапно, в свободное время, с акцентом на качество и полноту.  


  ✅ **__Выводы по результатам тестирования:__**

- **Ключевые сценарии сайта работают корректно.** 

  Smoke-тестирование показало, что пользователь может выполнить основные действия: найти фильм, открыть карточку фильма и перейти к актёру.
- **По API найдены несоответствия ожидаемому поведению.** 

  Некоторые запросы возвращают нерелевантные данные или не обрабатываются как ошибки. Это нарушает логику фильтрации и может сбивать пользователя с толку.
- **UI и кросс-браузерность не вызвали проблем.** 

  Интерфейс корректно отображается в актуальных версиях Chrome и Firefox.
- **Производительность в норме.** 

  Время отклика API и сайта находится в пределах допустимого, задержек и сбоев не обнаружено.
- **Оформлено 3 баг-репорта.** 

  Все баги зафиксированы и подкреплены доказательствами. Основные проблемы касаются обработки пустых и некорректных значений в API.
- **Предложены улучшения по сайту.** 

  Создана отдельная подстраница внутри коллекции **"Тестирование веб-приложения"** с предложениями по улучшению сайта. 

  

  

### ⚙️ **__Окружение тестирования:__**

**🖥️Операционная система:**
 ▪ Windows 11 Home (64-bit)

**🖥️Браузеры:**
 ▪ Google Chrome — версия 135.0.7049.96
 ▪ Opera — версия 117.0.5408.197
 ▪ Mozilla Firefox — версия 137.0.2 (64-bit)
 ▪ Яндекс Браузер — версия 25.2.6.697 (64-bit)

**🖥️Инструменты:**
 ▪ Postman — v11.41.7
 ▪ Google Sheets — оформление чек-листа и тест-кейсов
 ▪ Qase.io — создание smoke-тестов
 ▪ Yonote — финальный отчёт, баг-репорты, предложения
 ▪ OBS Studio — запись демонстрации проекта

  

### **🔧 __Рекомендации для разработчиков__**__:__

По результатам тестирования API рекомендуется реализовать валидацию параметра query, чтобы исключить обработку некорректных значений. При пустом, числовом или содержащем только специальные символы query, API должен возвращать либо пустой список, либо сообщение об ошибке с соответствующим статусом (например, 400 Bad Request). Это повысит предсказуемость поведения API, улучшит фильтрацию и сократит риск получения нерелевантных данных.  

### 

  