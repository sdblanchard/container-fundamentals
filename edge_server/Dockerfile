FROM alpine:latest
LABEL org.opencontainers.image.authors="blanchardsky@gmail.com"
LABEL sever_type=edge_server
RUN apk update && apk add nginx && apk cache clean
COPY config/nginx.conf /etc/nginx/nginx.conf
COPY web_content/ /var/www
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]