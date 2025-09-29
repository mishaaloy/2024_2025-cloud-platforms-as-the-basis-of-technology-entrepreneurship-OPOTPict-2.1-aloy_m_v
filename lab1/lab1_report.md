University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Cloud platforms as the basis of technology entrepreneurship](https://) ADD link
Year: 2024/2025
Group: OPOTPICT2-1
Author: Aloy Mikhail Victorovich
Lab: Lab1
Date of create: 28.09.2025
Date of finished: 29.09.2025

1. Получил доступ к Google Cloud.
2. Перешел во вкладку Service Accounts, навесил роль Storage Admin
<img width="1076" height="486" alt="Снимок экрана 2025-09-29 в 03 42 08" src="https://github.com/user-attachments/assets/513e96cc-487b-4dcb-91e3-546977f6bd42" />
3. Перешел в Computer Engine — VM Instances и создал минимальный compute engine с Machine type e2-micro в режиме spot
<img width="1465" height="323" alt="Снимок экрана 2025-09-29 в 03 54 13" src="https://github.com/user-attachments/assets/dbc1a7a4-b9fc-4974-88de-5d21cd1782dc" />
4. Перешел на SSH виртуальной машины и использовад gsutils, чтобы найти бакет lab1-bucket-itmo и скопировать 3 файла в локальную папку на VM
<img width="1194" height="638" alt="Снимок экрана 2025-09-29 в 04 01 42" src="https://github.com/user-attachments/assets/bdd5a957-ba1e-49f4-84c0-16985ad37253" />
5. Поменял роль. Вернулся в SSH и все равно смог повторить копирование
<img width="1160" height="543" alt="Снимок экрана 2025-09-29 в 04 05 29" src="https://github.com/user-attachments/assets/6203129d-9939-4b8e-94a4-09f01be5c341" />
<img width="505" height="202" alt="Снимок экрана 2025-09-29 в 04 12 06" src="https://github.com/user-attachments/assets/4469f7ab-88d7-46c8-971e-b1c096ff9776" />
