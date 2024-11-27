FROM nginx:latest

RUN apt-get update && apt-get install -y openssl
RUN rm /etc/nginx/conf.d/default.conf #&& mkdir -p /src

RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/certs/self.key -out /etc/ssl/certs/self.crt \
    -subj "/C=RU/ST=Moscow/L=dev/O=local Code/OU=Org/CN=dev.local"
