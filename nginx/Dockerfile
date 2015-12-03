FROM        ubuntu:14.04

# PROJECT VARIABLES
MAINTAINER  Marko Klemetti "marko.klemetti@gmail.com"

# INSTALL NGINX
RUN         apt-get update
RUN         apt-get install -y nginx

# ADD NGINX CONFIGURATION
RUN         rm -v /etc/nginx/nginx.conf
ADD         nginx.conf /etc/nginx/
RUN         echo "daemon off;" >> /etc/nginx/nginx.conf

# START NGINX
EXPOSE      80
CMD         service nginx start
