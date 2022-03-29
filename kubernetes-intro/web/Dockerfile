FROM nginx:latest

RUN rm -rf /usr/share/nginx/html/* && \
    rm -rf /etc/nginx/conf.d/*
COPY ./app/homework.html /app/homework.html
COPY /app /usr/share/nginx/html
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf

RUN chown -R nginx:nginx /usr/share/nginx/html && \
    chown -R nginx:nginx /etc/nginx && \
    chown -R nginx:nginx /app

RUN usermod -u 1001 nginx

EXPOSE 8000

ENTRYPOINT ["nginx", "-g", "daemon off;"]
