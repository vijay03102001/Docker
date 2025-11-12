# Stage 1: Build stage
FROM python:3.9-alpine as build-stage
WORKDIR /app
COPY requirements.txt .

COPY script.py .
RUN pip install --no-cache-dir -r requirements.txt
CMD ["python", "script.py"]
