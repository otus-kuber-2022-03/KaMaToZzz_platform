FROM nginx:latest

COPY ./app /app
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf
WORKDIR /app
RUN chown -R nginx:nginx /etc/nginx && \
    chown -R nginx:nginx /app

RUN usermod -u 1001 nginx

EXPOSE 8000

CMD ["nginx", "-g", "daemon off;"]
