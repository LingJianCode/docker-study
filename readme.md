## start docker mysql
```bash
sudo docker run -e MYSQL_ROOT_PASSWORD="123456" --name mysql_test mysql:8.0
```
---
## check all docker ip
```bash
sudo  docker inspect -f='{{.Name}} {{.NetworkSettings.IPAddress}} {{.HostConfig.PortBindings}}' $(sudo docker ps -aq)
sudo  docker inspect -f='{{.Name}} {{.NetworkSettings.docker_default.IPAddress}} {{.HostConfig.PortBindings}}' $(sudo docker ps -aq)
```
---
## docker compose up (v2)
```bash
sudo docker compose -f mysql.yaml up -d
```
---
## docker exec
```bash
sudo docker exec -it container_id /bin/bash
```
---
gtid replica
```bash
change replication source to source_host='172.18.0.3', source_port=3306,source_user='repl',source_password='repl',source_auto_position=1;
```
