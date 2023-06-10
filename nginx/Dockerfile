FROM ubuntu:latest  
RUN apt-get update  
RUN apt-get install -y nginx
RUN mv /etc/nginx/sites-enabled/default /tmp/default
COPY ./hosts/application.local.conf /etc/nginx/sites-enabled/application.local.conf
WORKDIR /data  
VOLUME /data  
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]