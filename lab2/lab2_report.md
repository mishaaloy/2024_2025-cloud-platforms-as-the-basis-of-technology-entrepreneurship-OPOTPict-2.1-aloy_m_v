University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Cloud platforms as the basis of technology entrepreneurship](https://) ADD link
Year: 2024/2025
Group: OPOTPICT2-1
Author: Aloy Mikhail Victorovich
Lab: Lab2
Date of create: 29.09.2025
Date of finished: 29.09.2025

1. Создал сервак с Cloud Run с минимальным кол-вом ресурсов


2. Проверил работоспособность


3. Зафиксировал логи и метрики


4. Поменял порт на 8090 и изменил трафик между версиями

5. Проанализировал логи и метрики:
   — Логи показывают успешный старт контейнера
   - Видно, что приходили HTTP-запросы к сервису, то есть сервис работал корректно
   - После изменения порта вот такой лог: Cloud Run! The container started successfully and is listening for HTTP requests on port 8090
   - Дальше Cloud Run создает новую ревизию и начинает перераспределять трафик. В логах видно: DEPLOYMENT_ROLLOUT - Instance started due to traffic shifting
   - В логах при переключении видно миграцию трафика и запуск новых контейнеров
