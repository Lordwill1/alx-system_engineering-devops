#!/usr/bin/env bash
# sets up a new 404 error page
sudo apt-get update
sudo apt-get install -y nginx 
echo "Hello World!" > index.html
sudo mv index.html /var/www/html


echo "Ceci n'est pas une page" > 404.html
sudo mv 404.html /var/www/html
echo "server {
   listen 80 default_server;
   listen [::]:80 default_server;
   
   root /var/www/html;
   index index.html;
   location /redirect_me {
      return 301 https://www.youtube.com/watch?v=QH2-TGUlwu4;
   }
   error_page 404 /404.html;
   location = /404.html{
      internal;
   }
}" > default
sudo mv -f default /etc/nginx/sites-available/default
sudo service nginx restart
