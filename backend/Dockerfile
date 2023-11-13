# backend/Dockerfile
FROM python:3.8-slim

WORKDIR /usr/src/app

COPY ./requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt
RUN pip install gunicorn  # Add this line to install gunicorn

COPY . .

CMD ["gunicorn", "app:app", "--bind", "0.0.0.0:8000"]
