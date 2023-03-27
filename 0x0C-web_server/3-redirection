#!/usr/bin/env bash
# Installs, configures, and starts the server
apt-get update
apt-get -y install nginx
sudo ufw allow 'Nginx HTTP'
mkdir -p /var/www/html/
sudo chmod -R 755 /var/www
echo 'Hello World!' > /var/www/html/index.html
SERVER_CONFIG=\
"server {
	listen 80 default_server;
	listen [::]:80 default_server;
	root /var/www/html;
	index index.html index.htm index.nginx-debian.html;
	server_name _;
	location / {
		try_files \$uri \$uri/ =404;
	}
	if (\$request_filename ~ redirect_me){
		rewrite ^ https://sketchfab.com/bluepeno/models permanent;
	}
}"

bash -c "echo -e '$SERVER_CONFIG' > /etc/nginx/sites-enabled/default"

if [ "$(pgrep -c nginx)" -le 0 ]; then
	service nginx start
else
	service nginx restart
fi
