FROM nginx:latest
COPY ./app/homework.html /app/homework.html

WORKDIR /app

RUN rm -rf /usr/share/nginx/html/* \
    rm -rf /etc/nginx/conf.d/*
COPY /app /usr/share/nginx/html

RUN usermod -u 1001 nginx

COPY ./nginx/nginx.conf /etc/nginx/nginx.conf

EXPOSE 8000

ENTRYPOINT ["nginx", "-g", "daemon off;"]