# mailu setting
```
docker container ls --filter name=^mailu_ --format "{{ .Names }}"
docker inspect -f "{{ .NetworkSettings.Networks.mailu_default.IPAddress }}" mailu_smtp_1

docker cp mailu_front_1:/etc/nginx/nginx.conf .

docker exec -it mailu_admin_1 /bin//sh

docker-compose -p mailu up -d

docker-compose -p mailu rm

docker-compose -p mailu exec admin flask mailu admin admin mydevpc.pe.kr 'death100'

docker-compose -p mailu exec admin flask mailu user dave mydevpc.pe.kr 'death100'

docker container exec mailu_front_1 nginx -t

docker container exec mailu_front_1 nginx -s reload

apk update
apk add busybox-extras
apk add vim
```
