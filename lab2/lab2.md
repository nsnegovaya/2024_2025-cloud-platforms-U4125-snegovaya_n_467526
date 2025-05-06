1 шаг. Зайдем в Cloud Run на Google Cloud Platform и нажмем на Deploy.
![telegram-cloud-photo-size-2-5246964806412530541-y](https://github.com/user-attachments/assets/d926c79e-83c0-4990-987f-00ef0b83376e)

2 шаг. Используем существующий сервис hello и выставим минимальные настройки сервиса. Установим 8080 порт. Дадим доступ неавторизованным пользователям.
![telegram-cloud-photo-size-2-5246964806412530544-y](https://github.com/user-attachments/assets/8aa0f59f-ee17-4383-8247-799678282bb6)
![telegram-cloud-photo-size-2-5246964806412530546-y](https://github.com/user-attachments/assets/2ba1ab06-4a8d-44bd-a4d4-9fd923dfaf2d)
![telegram-cloud-photo-size-2-5246840213706241852-y](https://github.com/user-attachments/assets/b77b7f94-b350-43ce-b1b0-efecd09ed21a)

3 шаг. Проверим, что сервис запущен.
![telegram-cloud-photo-size-2-5246964806412530551-y](https://github.com/user-attachments/assets/788f4f33-34b6-4e73-bde2-d29ec087813a)

4 шаг. По ссылке проверим работоспособность сервиса, удостоверяемся, что все сработало.
![telegram-cloud-photo-size-2-5246964806412530557-y](https://github.com/user-attachments/assets/f48b5c1b-06b1-41c8-a438-04120491b6b0)

5 шаг. Просмотрим текущие Logs и Metrics.
![telegram-cloud-photo-size-2-5246964806412530554-y](https://github.com/user-attachments/assets/f9eb961a-cb84-44eb-8ece-21a6e92ce013)
![telegram-cloud-photo-size-2-5246964806412530556-y](https://github.com/user-attachments/assets/eb3f0ed5-5372-4b07-9bd5-01df45d3fdd0)

6 шаг. Выставим для данного Cloud Run 8090 порт и применим трафик на 50%.
![telegram-cloud-photo-size-2-5246964806412530561-y](https://github.com/user-attachments/assets/97186ac0-c456-427d-a46b-178749357c95)


7 шаг. Рассмотрим изменения в метриках и при логах при изменении трафика и порта. 

- В логах видно, что контейнер теперь запускается и слушает порт 8090 вместо 8080.
- Произошло обновление сервиса (ReplaceService), после чего контейнер выводит сообщение о старте на новом порту.
- Container Instance Count: наблюдался всплеск до двух активных экземпляров во время переключения.
- CPU/Memory Utilization: минимальные нагрузки, стабильные показатели (CPU около 1%, память около 10-20%).
- Container Startup Latency: небольшая задержка старта контейнера (примерно 80 мс).
- Max Concurrent Requests: максимум 2 одновременных запроса во время переключения.
<img width="1470" alt="image" src="https://github.com/user-attachments/assets/1f8a503e-bc7a-498f-877c-21737a9860e3" />
<img width="1470" alt="image" src="https://github.com/user-attachments/assets/2a91f072-31fa-4bf4-8ad4-d8e52dab1f03" />
<img width="1470" alt="image" src="https://github.com/user-attachments/assets/e7db9368-8735-4f78-a223-baf1916029ad" />

8 шаг. Удалим Cloud Run.
