
ARG NGINX_VERSION=1.20.1
FROM alpine:3.15

# Встановлення пакетів Nginx та supervisord
RUN apk update && apk add nginx  supervisor

# Копіювання конфігураційних файлів в образ
COPY nginx.conf /etc/nginx/nginx.conf
COPY supervisord.conf /etc/supervisord.conf

# Вказання команд, які будуть виконані при старті контейнера
CMD ["supervisord", "-c", "/etc/supervisord.conf"]



# # Використання базового образу Alpine
# FROM alpine

# # Встановлення пакетів Nginx та supervisord
# RUN apk update && apk add nginx supervisor

# # Копіювання конфігураційних файлів в образ
# COPY nginx.conf /etc/nginx/nginx.conf
# COPY supervisord.conf /etc/supervisord.conf

# # Вказання команд, які будуть виконані при старті контейнера
# CMD ["supervisord", "-c", "/etc/supervisord.conf"]
 