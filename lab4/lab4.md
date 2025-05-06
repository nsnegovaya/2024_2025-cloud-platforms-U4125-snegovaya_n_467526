Решение представлено на доске в MIRO: https://miro.com/app/board/uXjVI5AHevQ=/?share_link_id=712379161800

В рамках лабораторной работы рассматривается пример приложения с тремя стадиями жизненного цикла:

1) Начальная разработка
2) Тестирование партнерами
3) Продовое (production) решение

Для каждой стадии будет:
- Представлена схема архитектуры
- Рассчитана приблизительная стоимость эксплуатации
- Обоснован выбор сервисов Google Cloud Platform

**1) Начальная разработка**

Описание архитектуры:
_Фронтенд:_ Статический хостинг (Netlify/Vercel).
_Бэкенд:_ Сервер на AWS Lightsail/VPS (1 ядро, 2 ГБ RAM).
_AI-модель:_ Предобученная модель на CPU (например, FastAPI + Hugging Face).
_База данных:_ SQLite или Managed PostgreSQL (Supabase/Neon).
_CI/CD:_ GitHub Actions.

Цель: Минимальные затраты, быстрый старт.
<img width="747" alt="image" src="https://github.com/user-attachments/assets/332c5272-7201-4843-8a3f-914a398f6303" />
Итого: ~$10–50/мес.



**2) Тестирование партнерами**

Описание архитектуры:
_Фронтенд:_ Cloudflare Pages + CDN.
_Бэкенд:_ Kubernetes (EKS/GKE) с 2-3 нодами.
_AI-модель:_ GPU-инстанс (NVIDIA T4) для инференса.
_База данных:_ Amazon RDS PostgreSQL / Aurora Serverless.
_Мониторинг:_ Prometheus + Grafana.

Цель: Стабильность, масштабируемость, подготовка к продакшену.
<img width="723" alt="image" src="https://github.com/user-attachments/assets/a2265bfc-00ec-4703-bba5-02915af4d6cf" />
Итого: ~$500–600/мес.



**3) Продовое (production) решение**

Описание архитектуры:
_Фронтенд:_ Global CDN (Cloudflare/Amazon CloudFront).
_Бэкенд:_ Auto-scaling группой в AWS/GCP (4+ ядер, 8+ ГБ RAM).
_AI-модель:_ Dedicated GPU-кластер (A100) + Kubernetes с Horizontal Pod Autoscaler.
_База данных:_ Шардированный PostgreSQL или DynamoDB для высокой нагрузки.
_Безопасность:_ WAF, DDoS-защита, Secrets Manager.

Цель: Отказоустойчивость, глобальная доступность, высокая производительность.
<img width="722" alt="image" src="https://github.com/user-attachments/assets/c2f82c3d-c639-4bb0-a302-5ae37b8deddc" />
Итого: ~$12,000–15,000/мес.

**Выводы по экономической модели**
- MVP: Оптимально дешево (~$50/мес.), но ограничено по масштабируемости.
- Тестирование: Баланс цены и производительности (~$600/мес.), можно масштабировать.
- Продакшен: Дорого ($12K+), но необходимо для глобального запуска.

