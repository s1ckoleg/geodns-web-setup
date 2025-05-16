FROM nginx:1.27.5

RUN apt-get -y update; apt-get -y install curl

RUN rm /etc/nginx/conf.d/default.conf
RUN mkdir -p /etc/nginx/sites-enabled

COPY files/bundle.crt /etc/ssl/
COPY files/certificate.key /etc/ssl/

COPY files/nginx.conf /etc/nginx/
COPY files/sites-enabled /etc/nginx/sites-enabled/

COPY files/index.html /var/www/html/

RUN chmod 644 /etc/ssl/bundle.crt
RUN chmod 600 /etc/ssl/certificate.key

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
