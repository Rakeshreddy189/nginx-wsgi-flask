
FROM nginx:latest
RUN apt-get update && apt-get install -y gettext
WORKDIR /app
COPY nginx.conf /etc/nginx/nginx.conf
COPY default.conf /tmp/default.conf
COPY start.sh .
RUN chmod +x /app/start.sh
ENV FLASK_SERVER_ADDR=flask-app:8000
CMD ["bash", "/app/start.sh"]
