#!/usr/bin/env bash
# Fixes a web server to run Nginx as the nginx user listening on port 8080.
sed -i "s/#user www-data/user nginx/" /etc/nginx/nginx.conf
sed -i "s/80/8080/g" /etc/nginx/sites-available/default
chmod 644 /etc/nginx/nginx.conf
pkill apache2
sudo -u nginx service nginx start
