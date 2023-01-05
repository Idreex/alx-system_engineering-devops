#!/usr/bin/env bash
# Configures an Nginx server to listen on port 80.
ln -sf /etc/nginx/sites-available/default /etc/nginx/sites-enabled/default
service nginx start
kill "$(pgrep 'nginx' | head -1)"
