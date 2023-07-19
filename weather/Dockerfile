# pull official base image (Указываем базовый образ)
FROM python:3.11-alpine

# set environment variables
ENV PIP_DISABLE_PIP_VERSION_CHECK 1
# ↑ Отменяет проверку pip при каждом запуске на обновление
ENV PYTHONDONTWRITEBYTECODE 1
# ↑ Означает, что python не будет пытаться записывать .pyc файлы
ENV PYTHONUNBUFFERED 1
# ↑ гарантирует, что наш консольный вывод не буферизуется Docker-ом
# Устанавливаем переменную окружения PYTHONUNBUFFERED в значение 1

# set work directory (Устанавливаем рабочую директорию внутри контейнера)
WORKDIR /app

COPY requirements.txt /app/

# install dependencies
RUN pip install -r requirements.txt

# copy project (Копируем все файлы в контейнер)
COPY . .
