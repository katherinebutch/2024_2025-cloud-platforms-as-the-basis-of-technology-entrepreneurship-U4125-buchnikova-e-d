<b>University:</b> [ITMO University](https://itmo.ru/ru/) <br>
<b>Faculty:</b> [FTMI](https://ftmi.itmo.ru) <br>
<b>Course:</b> [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/) <br>
<b>Year:</b> 2024/2025 <br>
<b>Group:</b> U4125 <br>
<b>Author:</b> Buchnikova Ekaterina Dmitrievna  <br>
<b>Lab:</b> Lab1 <br>
<b>Date of create:</b> 05.05.2025 <br>
<b>Date of finished:</b> 06.05.2025<br>

<h1>Отчет по лабораторной работе №4 </h1>

Задание https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/education/labs2023-2024/lab4/lab4/#_5

**Тестовый вариант:** Веб-сервис, подсказывающий, как одеваться по погоде в одном из 30 городов России.

Сервер: cloud.ru.
База данных: Supabase
ИИ-помощник: Cursor.
Источник данных: API Яндекс.Погоды.
BI-платформа: [DataLense](https://datalens.yandex.cloud/jsqbdxpqqkj65-itmo-dashboard-course)
Язык программирования/фреймворки: Flask, JavaScript

![2025-05-06 15.43.04.jpg](https://github.com/katherinebutch/2024_2025-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-buchnikova-e-d/blob/main/lab4/2025-05-06%2015.43.04.jpg?raw=true)

Стоимость - платим только за хостинг сайта и доменное имя 

Минусы: 

В Supabase используется на бесплатном плане: 

- Ограничение на количество запросов в минуту
- Невозможно легко масштабировать без ручного вмешательства

При большом количестве запросов в сутки — начнутся задержки или ошибки

Нет промежуточного кэширования — одинаковые запросы от разных пользователей каждый раз грузят API => Можно внедрить кэширование погоды на 5–10 минут по городу.

В принипе не выдерживает любую нормальную нагрузку. 

