FROM nginx:1.21.6-alpine

LABEL maintainer="Andrey"
LABEL version="1.0"

COPY nginx.conf /etc/nginx/
COPY /image/Docker.jpeg /var/www/html/

RUN echo '<html><h3 align=center>Docker work</h3><p align=center><image src="Docker.jpeg"></p><p align=center><i>Author: Andrey</i></p></html>' > /var/www/html/index.html &&\
    chown -R nginx:nginx /var/www &&\
    chmod -R 644 /var/www/html/*

ENTRYPOINT ["/docker-entrypoint.sh"]

EXPOSE 80
EXPOSE 443

STOPSIGNAL SIGQUIT

CMD ["nginx", "-g", "daemon off;"]

