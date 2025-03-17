FROM python:3.9
WORKDIR /app
COPY requrements.txt .
RUN pip install -r requrements.txt --no-cache-dir
COPY . .
RUN python manage.py collectstatic
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "kittygram_backend.wsgi"]
