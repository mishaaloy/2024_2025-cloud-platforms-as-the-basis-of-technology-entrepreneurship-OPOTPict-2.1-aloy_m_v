University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Cloud platforms as the basis of technology entrepreneurship](https://) ADD link
Year: 2024/2025
Group: OPOTPICT2-1
Author: Aloy Mikhail Victorovich
Lab: Lab4
Date of create: 29.09.2025
Date of finished: 30.09.2025

Описание: AI-сервис анализирует погодные условия, волны и течения на ключевых спотах Бали (Kuta, Uluwatu, Canggu и др.) и дает текстовые рекомендации, когда лучше всего выходить в воду.

##Начальное состояние
Схема:
<img width="893" height="259" alt="Снимок экрана 2025-09-30 в 13 27 05" src="https://github.com/user-attachments/assets/0cb56a5a-c9eb-411a-b5b1-80650e1f2a27" />

Инструменты и обоснование выбора:
1. Фронт: Firebase Hosting — бесплатный хостинг для статических сайтов, SSL по умолчанию. Бессерверная NoSQL БД, которая автоматически масштабируется, что избавляет нас от администрирования на старт
2. Бэк: Cloud Functions (Python) — платим только за вызовы и время выполнения
3. Кэш и логи: Firestore. NoSQL база от Google. Простая интеграция с Firebase и Cloud Functions
4. AI/ML: Vertex AI (PaLM API / Gemini Pro). Не нужно разворачивать свои модели, латим за количество символов
5. Внешний сервис: OpenWeatherMap API. Простое и доступное апи для получения данных о погоде

Финансовая модель (месяц, USD):
<img width="588" height="132" alt="Снимок экрана 2025-09-30 в 15 19 37" src="https://github.com/user-attachments/assets/170c35fd-ef20-4e55-ac06-764bb3b51769" />

##Тестирование партнерами
Схема:
<img width="799" height="275" alt="Снимок экрана 2025-09-30 в 14 57 09" src="https://github.com/user-attachments/assets/9aba3641-6190-440f-9513-b82fd23160e3" />

Инструменты и обоснование выбора:
1. Фронт: Cloud Run + CDN — ыносим фронтенд в отдельный контейнер для большей гибкости. CDN кэширует статику и снижает нагрузку
2. Бэк: Cloud Run (Python/Go) — получаем более предсказуемую производительность и длительные фоновые процессы
3. Кэш: Memorystore (Redis) — кэширует ответы от погодного API и рекомендации AI на 10-15 минут. Снижает затраты на внешние API
4. База данных: Cloud SQL (PostgreSQL) — реляционная СУБД для структурированных данных партнеров, сложных запросов аналитики и надежности
5. AI/ML: Vertex AI Prediction Endpoint — создаем свою настроенную модель для большей точности рекомендаций. Endpoint еще обеспечивает стабильность SLA
6. Мониторинг: Cloud Monitoring — пЧозволяет партнерам видеть метрики производительности и ошибки в реальном времени

Финансовая модель (месяц, USD):
<img width="574" height="166" alt="Снимок экрана 2025-09-30 в 15 19 43" src="https://github.com/user-attachments/assets/0b8e8457-b04c-4ead-8e8b-4210976e4ddd" />

##Продовое решение
Схема:
<img width="885" height="240" alt="Снимок экрана 2025-09-30 в 15 08 15" src="https://github.com/user-attachments/assets/a005c594-582a-4dd9-aff8-e6bb0d86a0f7" />

Инструменты и обоснование выбора:
1. Оркестрация: GKE Autopilot — автоматическое управление нодами, безопасностью и масштабированием. Экономит на DevOps по сравнению с ручным GKE
2. База данных: Cloud Spanner — ключевой элемент для отказоустойчивости. горизонтально масштабируемая, глобально распределенная SQL-база
3. AI/ML: Vertex AI с выделенными ресурсами (TPU/GPU) — генерирует рекомендации мгновенно даже при большой нагрузке
4. Асинхронность: Pub/Sub + Cloud Functions — очередь для обработки логирования, аналитики и других фоновых задач
5. Сеть: Global Load Balancer + CDN — для направления пользователей в ближайшие и ненагруженные регионы

Финансовая модель (месяц, USD):
<img width="579" height="147" alt="Снимок экрана 2025-09-30 в 15 19 47" src="https://github.com/user-attachments/assets/8c2014b2-fffe-49ba-a044-81eda6c5fab7" />
