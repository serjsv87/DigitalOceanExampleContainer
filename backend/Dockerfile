# backend/Dockerfile
FROM python:3.8-slim

WORKDIR /usr/src/app

COPY ./requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt
COPY . .

CMD ["gunicorn", "app:app", "--bind", "0.0.0.0:8000"]
