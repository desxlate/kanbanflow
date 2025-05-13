# KanbanProjectManager

**KanbanProjectManager** — это полнофункциональное веб-приложение на FastAPI + SQLite, реализующее систему управления задачами по принципу канбан-досок.  
Поддерживает регистрацию, авторизацию, разграничение доступа и работу с задачами и участниками.

---

## Стек технологий

- **Back-end:** FastAPI, SQLAlchemy, Pydantic, JWT
- **База данных:** SQLite
- **Аутентификация:** OAuth2, JWT
- **Front-end:** HTML, CSS, JS (Vanilla)
- **Dev tools:** Uvicorn, python-dotenv, Passlib

---

## Структура проекта

KanbanProjectManager/
├── app/
│ ├── main.py # Точка входа в приложение
│ ├── database.py # Подключение к БД
│ ├── models.py # SQLAlchemy модели
│ ├── schemas.py # Pydantic схемы
│ ├── auth.py # JWT, хеширование
│ ├── dependencies.py # Зависимости
│ ├── crud/ # Бизнес-логика (CRUD)
│ └── routers/ # Роутеры FastAPI
├── frontend/ # HTML + JS клиент
│ ├── index.html # Страница входа
│ ├── register.html # Регистрация
│ ├── boards.html # Интерфейс досок и задач
│ ├── dashboard.html # Кабинет пользователя
│ ├── script.js # Логика взаимодействия
│ └── style.css # Стили
└── requirements.txt # Зависимости pip


---

## ⚙️ Установка и запуск

### 🔹 1. Клонируй репозиторий
```bash
git clone https://github.com/yourusername/KanbanProjectManager.git
cd KanbanProjectManager
```

### 🔹 2. Создай виртуальное окружение
```bash
python -m venv .venv
.venv\Scripts\activate    # Windows
# source .venv/bin/activate  # Linux/macOS
```
### 🔹 3. Установи зависимости
```bash
pip install -r requirements.txt
```

### 🔹 4. Настрой переменные окружения
Создай .env файл в корне:

```ini
SECRET_KEY=your-secret-key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=60
DATABASE_URL=sqlite:///./kanban.db
```


### 🔹 5. Запусти сервер
```bash
uvicorn app.main:app --reload
```
Сервер будет доступен по: http://127.0.0.1:8000

## Swagger UI
API-документация доступна по адресу:
http://127.0.0.1:8000/docs
