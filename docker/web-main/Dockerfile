FROM nginx:1.16.1

RUN rm /etc/nginx/conf.d/default.conf
RUN mkdir -p /etc/nginx/sites-enabled

COPY files/nginx.conf /etc/nginx/
COPY files/default /etc/nginx/sites-available/

RUN ln -s /etc/nginx/sites-available/default /etc/nginx/sites-enabled/

COPY files/index.html /var/www/html/
COPY files/styles.css /var/www/html/

RUN nginx -t

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
