Шаг 1.
В разделе IAM & Admin на вкладке Service Accounts создан новый сервисный аккаунт.
<img width="910" alt="image" src="https://github.com/user-attachments/assets/a7dc1a53-ee04-4470-b48d-df4d0e19c2e2" />

Шаг 2.
При создании задано название сервисного аккаунта в соответствии с маской, указанной в лабораторной работе, затем выполнен переход к следующему этапу.
<img width="618" alt="Снимок экрана 2025-05-06 в 16 24 45" src="https://github.com/user-attachments/assets/cb56bc3d-bff8-49bd-975e-bb4aa7d6bca9" />

Шаг 3.
Выбрана роль Storage Admin, после чего сервисный аккаунт успешно создан.
<img width="618" alt="Снимок экрана 2025-05-06 в 16 24 45" src="https://github.com/user-attachments/assets/f7c30ed6-e1da-4ec9-a13e-f02f585a91fe" />
<img width="532" alt="image" src="https://github.com/user-attachments/assets/ebf67007-169c-4860-867e-eefc39e5ee9e" />

Шаг 4.
Открыт раздел Compute Engine, на вкладке VM instances нажата кнопка Create instance для создания виртуальной машины.
<img width="809" alt="image" src="https://github.com/user-attachments/assets/3bbcf9ea-5f9b-4e2d-b5ab-74f14a41ce19" />

Шаг 5.
Настроены параметры виртуальной машины согласно заданию. Проверена итоговая стоимость — $3.44.
![Frame 17](https://github.com/user-attachments/assets/81a0dd82-8a78-4eeb-bf6b-64796e76d8e2)
<img width="634" alt="image" src="https://github.com/user-attachments/assets/9f4a0b9d-18b5-424f-b9d7-899f8d571be4" />
<img width="1047" alt="image" src="https://github.com/user-attachments/assets/7b987384-3114-438a-995b-f1728c57d2c4" />

Шаг 6.
Выполнено подключение к созданной виртуальной машине через SSH.
<img width="1049" alt="image" src="https://github.com/user-attachments/assets/793c7477-0419-4884-a36e-f84aeaa6063d" />

Шаг 7.
В окне подключения выполнены команды для создания новой папки и копирования в неё необходимых файлов. После выполнения операций SSH-сессия завершена.
![telegram-cloud-photo-size-2-5204257932248740085-y](https://github.com/user-attachments/assets/3e57edcf-9922-489c-ad26-04b86bd1f766)

Шаг 8.
В разделе IAM & Admin на вкладке Service Accounts для созданного сервисного аккаунта добавлена роль Compute Viewer.
<img width="945" alt="image" src="https://github.com/user-attachments/assets/c78cfecd-5559-42bd-8602-6b1997352f06" />

Шаг 9.
Повторно выполнено подключение к виртуальной машине через SSH. При попытке переноса данных получена ошибка, свидетельствующая о недостаточности прав доступа.

Шаг 10.
Виртуальная машина и сервисный аккаунт удалены.
