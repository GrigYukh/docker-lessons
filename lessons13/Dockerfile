# Используем образ Ubuntu в качестве базового образа
FROM ubuntu:latest

# Устанавливаем Nginx
RUN apt-get update && \
    apt-get install -y nginx && \
    apt-get clean

# Копируем конфигурационные файлы Nginx в контейнер
COPY nginx.conf /etc/nginx/nginx.conf

# Открываем порт 8080 для внешнего доступа
EXPOSE 8080

# Команда для запуска Nginx в фоновом режиме
CMD ["nginx", "-g", "daemon off;"]
