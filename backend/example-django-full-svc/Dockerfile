FROM python:3.9-slim-buster

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

COPY app /app

WORKDIR /app

RUN pip install -r requirements.txt

EXPOSE 8000
CMD ["sh", "run.sh"]
