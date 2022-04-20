#

nginx
docker run -d -p 80:80 -p 443:443 -v /data/nginx:/etc/nginx -v /data/ssl:/etc/nginx/ssl -v /data/log:/var/log/nginx -v /data/www:/www --name nginx --restart=always nginx

mysql
docker run -d -e MYSQL_ROOT_PASSWORD=password --name mysql --restart=always mysql

redis
docker run -d --name redis --restart=always redis


cloudreve
docker run -d -v /data/cloudreve/conf.ini:/cloudreve/conf.ini -v /data/cloudreve/avatar:/cloudreve/avatar -v /data/cloudreve/uploads:/cloudreve/uploads -v /data/cloudreve/downloads:/cloudreve/downloads --name cloudreve --restart=always cloudreve/cloudreve

docker exec -it {CONTAINER NAME} bash
