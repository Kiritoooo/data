#

nginx
docker run -d -p 80:80 -p 443:443 -v /data/nginx:/etc/nginx -v /data/ssl:/etc/nginx/ssl -v /data/log:/var/log/nginx -v /data/www:/www --name nginx --restart=always nginx

mysql
docker run -d -e MYSQL_ROOT_PASSWORD=password --name mysql --restart=always mysql

redis
docker run -d --name redis --restart=always redis


cloudreve
docker run -d -v /data/cloudreve/conf.ini:/cloudreve/conf.ini -v /data/cloudreve/avatar:/cloudreve/avatar -v /data/cloudreve/uploads:/cloudreve/uploads -v /data/cloudreve/downloads:/cloudreve/downloads --name cloudreve --restart=always cloudreve/cloudreve

aria2

docker run -d -e PUID=0 -e PGID=0 -e UMASK_SET=022 -e RPC_SECRET=password -e RPC_PORT=6800 -e LISTEN_PORT=6888 --log-opt max-size=1m -v /data/aria2/config:/config -v /data/aria2/downloads:/downloads --name aria2 --restart unless-stopped p3terx/aria2-pro

docker exec -it {CONTAINER NAME} bash
