#!/usr/bin/env bash
# installs nginx and configures it on a remote server

apt-get -y update
apt-get -y install nginx
ufw allow 'Nginx HTTP'
echo 'Hello World!' > /var/www/html/index.nginx-debian.html
service nginx start
