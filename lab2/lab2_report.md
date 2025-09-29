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
<img width="1466" height="672" alt="Снимок экрана 2025-09-29 в 21 23 00" src="https://github.com/user-attachments/assets/c9caa683-c19c-4028-a4ff-c5b1a4db7e9e" />

2. Проверил работоспособность
<img width="1059" height="794" alt="Снимок экрана 2025-09-29 в 21 24 29" src="https://github.com/user-attachments/assets/9f9b1be7-a93b-4eca-9103-fc90ffa8fab3" />

3. Зафиксировал логи и метрики
<img width="1309" height="585" alt="Снимок экрана 2025-09-29 в 21 30 36" src="https://github.com/user-attachments/assets/fa7a01b4-0a38-42d8-bc9e-f23012e96818" />
<img width="1336" height="253" alt="Снимок экрана 2025-09-29 в 21 30 53" src="https://github.com/user-attachments/assets/4db81d57-9008-499b-adb6-2f6b916b2baa" />

4. Поменял порт на 8090 и изменил трафик между версиями
<img width="1167" height="596" alt="Снимок экрана 2025-09-29 в 21 41 05" src="https://github.com/user-attachments/assets/c01d0845-ba45-4ea2-bbb0-2793f9965b8b" />

5. Проанализировал логи и метрики:
   — Логи показывают успешный старт контейнера
   - Видно, что приходили HTTP-запросы к сервису, то есть сервис работал корректно
   - После изменения порта вот такой лог: Cloud Run! The container started successfully and is listening for HTTP requests on port 8090
   - Дальше Cloud Run создает новую ревизию и начинает перераспределять трафик. В логах видно: DEPLOYMENT_ROLLOUT - Instance started due to traffic shifting
   - В логах при переключении видно миграцию трафика и запуск новых контейнеров
