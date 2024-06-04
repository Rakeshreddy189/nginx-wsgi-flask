
FROM python:3.9-slim

WORKDIR /app

COPY . .

# Install Flask, Jinja2, and Gunicorn
RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8000

CMD ["gunicorn", "-w", "3", "-t", "60", "-b", "0.0.0.0:8000", "app:app"]

