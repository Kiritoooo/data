#

nginx

docker run -d -p 80:80 -p 443:443 -v /data/nginx:/etc/nginx -v /data/ssl:/etc/nginx/ssl -v /data/log:/var/log/nginx -v /data/www:/www --name nginx --restart=always nginx


