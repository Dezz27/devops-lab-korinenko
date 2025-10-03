# Используем базовый образ python:3.9-slim
FROM python:3.9-slim

# Устанавливаем рабочую директорию /app
WORKDIR /app

# Устанавливаем системные пакеты: curl и vim
RUN apt-get update && \
    apt-get install -y --no-install-recommends curl vim && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Копируем файл с зависимостями и устанавливаем Python пакеты
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Создаем пользователя appuser с UID 1000
RUN useradd -m -u 1000 appuser

# Копируем файл app.py в контейнер
COPY app.py .

# Переключаемся на пользователя appuser
USER appuser

# Открываем порт 5000
EXPOSE 5000

# Устанавливаем переменную окружения FLASK_ENV=production
ENV FLASK_ENV=production

# Запускаем приложение командой python app.py
CMD ["python", "app.py"]