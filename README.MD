# 🚀 Вадим Кузьмицкий — Python-разработчик и инженер данных

Пишу код, который читает город. Разрабатываю решения для извлечения, нормализации и анализа открытых данных: от градостроительных планов до судебных решений. Публиковался в «Деловом Петербурге» и на Хабре.

📍 Санкт-Петербург (гибрид / удалённо)  
📬 [@alfablen](https://t.me/alfablen) | 📧 alfablend@gmail.com  
🔗 [GitHub](https://github.com/alfablend) | [Хабр](https://habr.com/ru/users/alfablend/) | [Публикации в «ДП»](https://www.dp.ru/tag/vadim-kuzmitskij)

---

## 🧠 Основной AI-проект: ROSTRAL

**rostral.io** — инженерный MVP-проект на Python с GPT4All API, модульной архитектурой и полноценной документацией.  
Цель: создание системы для семантической обработки документов и автоматизированной аналитики.

🔗 [Репозиторий](https://github.com/alfablend/rostral.io) | [Статья на Хабре](https://habr.com/ru/articles/927938/) | [Спецификация](https://github.com/alfablend/rostral.io/blob/main/docs/TECHNICAL_SPEC.md)

### 💡 Что реализовано

- CLI-интерфейс, с модульной логикой пайплайнов  
- Нормализация PDF/HTML-документов и извлечение метаданных  
- Интеграция GPT4All — чат с документами, вопросы к фрагментам  
- Архитектурная спецификация: фолбэки, маршруты, зоны ответственности  
- Документация в Markdown, roadmap по RAG и Telegram-интерфейсу

### 📌 Особенности

- Система ориентирована на прикладную обработку документов — от жилищного мониторинга до теханализа  
- Открытый код, прозрачная логика, потенциальная масштабируемость для мультиагентных систем

---


## 🧰 VKPMONBOT

Система автоматического мониторинга градостроительной документации Петербурга  
→ [Репозиторий vkpmonbot](https://github.com/alfablend/vkpmonbot)

**Что делает:**
- Следит за разрешениями на строительство, градпланами, согласованиями и экспертизами
- Парсит HTML/PDF, извлекает текст и изображения
- Отображает результаты на карте OpenStreetMap
- Отправляет уведомления через Telegram-бота
- Обеспечивает веб-интерфейс и поддержку подписок по типу документа

**Технологии:** Python, Flask, BeautifulSoup, PyPDF2, OCRmyPDF, SQLite, rosreestr2coord, telebot, cron, threading

---

## 🧱 Проект: реконструкция центра Петербурга

Анализ проектной активности в охраняемом центре: сопоставление градпланов (ГПЗУ) и зданий (памятники, средовые).  
→ [Код](https://github.com/alfablend/data-engineering/tree/main/center_reconstruction) | [Статья](https://www.dp.ru/a/2025/06/17/v-centre-peterburga-potencialno)

**Что делает:**
- Загружает объекты культурного наследия и участки с ГПЗУ
- Производит spatial join (пересечение зданий с участками)
- Визуализирует интерактивную карту и собирает статистику
- Даёт вывод: ~17% охраняемых зданий попали под проектирование

**Технологии:** Pandas, GeoPandas, shapely, folium, rosreestr2coord, WFS/WKT, spatial join

---


## 🧭 Инженерное ТЗ: определение часового пояса

→ [Проект tz-detection-spec](https://github.com/alfablend/tz-detection-spec)

**Что внутри:**
- Чёткое техническое задание на нормализацию и определение поясов
- Примеры данных, каскадная логика, фолбэки, DQ-требования
- Формат: Markdown + JSON, готово к реализации

📁 Репозиторий: `tz-detection-spec`

---

## 🧩 Вклад в open source

🔄 **`changedetection.io`: добавление переменных в POST-запросы**  
→ [Issue #2502](https://github.com/dgtlmoon/changedetection.io/issues/2502) | [Merged in #2740](https://github.com/dgtlmoon/changedetection.io/pull/2740)  
Инициировал поддержку Jinja2-переменных в теле POST-запросов.  
📌 Использовалось для мониторинга сайта [Госстройнадзора СПб](http://expertiza.spb.ru/), где требовалась передача текущей даты в запросах для получения актуальной информации.

---

## 📌 Кейсы прикладной аналитики

🧯 **Отключения ГВС:** выгрузка графиков с сайтов Теплосети и ТЭК  
→ [Статья](https://www.dp.ru/a/2025/06/10/suhoj-zakon-kakie-doma-v) | [Код](https://github.com/alfablend/data-engineering/tree/main/hot_water_outages)

🎬 **Кино в Петербурге:** где и что снимают  
→ [Читать](https://www.dp.ru/a/2024/07/23/po-zakonam-zhanra-bolee-sotni)

🛣️ **Трасса М–7:** какие дома попадут под снос  
→ [Читать](https://www.dp.ru/a/2024/09/17/proekt-trassi-m7-cherez-udelnij)

🏬 **Магазины с алкоголем в жилом фонде**  
→ [Читать](https://www.dp.ru/a/2024/06/25/chislo-magazinov-s-alkogolem)

🧽 **Трекинг коммунальной техники (WebSocket)**  
→ [Читать](https://www.dp.ru/a/2025/03/31/litri-na-kilometri-kak-chistjat)

📄 **20 000 HTML-отчётов по капремонту**  
→ [Хабр](https://habr.com/ru/articles/891704/)

📎 [Полный список из 17+ кейсов со ссылками](#📌-кейсы-анализа-городских-данных)

---

## 💼 Другие проекты

- [`alfablend.github.io`](https://github.com/alfablend/alfablend.github.io): визуализации, карты

---

## 🛠 Технологический стек

| Компонент         | Технологии                                                                 |
|-------------------|----------------------------------------------------------------------------|
| Backend           | Flask, SQLite, cron, threading, logging                                    |
| Парсинг и OCR     | BeautifulSoup4, PyPDF2, OCRmyPDF, Regex                                    |
| AI/LLM            | GPT4All (saiga_yandexgpt_8b.gguf)                                           |
| Обработка данных  | Pandas, Geopandas, osmnx, Pyrosm                                            |
| Визуализация      | Folium, matplotlib, rosreestr2coord                                         |
| Интеграции        | Telegram Bot API, Kontur.Focus, DaData, API КГА                            |
| 🛰️ Мониторинг сайтов | `changedetection.io` (инициировал поддержку Jinja2-переменных в POST — [issue](https://github.com/dgtlmoon/changedetection.io/issues/2502)) |
| Инфраструктура    | Docker, REST, cron, WebSocket                                               |

> Используется, например, для мониторинга сайта [Госстройнадзора СПб](https://gosstroynadzor.gov.spb.ru), где обновления зависят от параметров текущей даты в теле запроса.

---

## 🎯 Цель

Хочу развиваться как Python backend или Data Engineer: API, интеграции, обработка текстов и пространственных данных, визуализация, автоматизация. Уверенно работаю с неструктурированными источниками и превращаю данные в результат — будь то Telegram-бот, карта или CSV. Открыт к интересным задачам и развитию в команде.

📬 [@alfablen](https://t.me/alfablen) | 📧 alfablend@gmail.com
