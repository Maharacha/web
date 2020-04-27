docker-compose -f docker-compose.yml -f nginx/docker-compose.yml -f finedr/docker-compose.yml -f owncloud/docker-compose.yml build internal-nginx
docker-compose -f docker-compose.yml -f nginx/docker-compose.yml -f finedr/docker-compose.yml -f owncloud/docker-compose.yml up -d internal-nginx

docker logs --tail 50 --follow --timestamps nginx

sudo ifconfig wlp4s0:0 192.168.0.10 netmask 255.255.255.0 up
