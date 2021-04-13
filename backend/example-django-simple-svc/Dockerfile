FROM python:3.9-slim-buster


COPY app /app

COPY requirements.txt /app/requirements.txt

RUN pip3 install -r requirements.txt

WORKDIR /app

EXPOSE 8000
