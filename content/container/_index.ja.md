+++
title = "コンテナ関連"
date = 2019-10-13T12:17:07Z
weight = 10
chapter = true
pre = "<b>2. </b>"
+++

### Chapter 2

# コンテナ関連コマンド<br>（DD）

|DD Command|In case of docker command|Description|
|:---|:---|:---|
|[DD](dd/)|docker ps -a|Show all containers|
|[DDps](ddps/)|docker ps|Show running containers in default format|
|[Dpsa](ddpsa/)|docker ps -a|Show all containers in default format|
|[DDstart](ddstart/)|docker start \<container id>|start stopped container|
|[DDstop](ddstop/)|docker stop \<container id>|Stop running container|
|[DDstopa](ddstopa/)|docker stop $(docker ps -q)|Stop all of running container|
|[DDrm](ddrm/)|docker rm \<container id>|Remove a container|
|[DDrma](ddrma/)|docker rm $(docker ps -aq)|Remove all of running containers|
|[DDdown](dddown/)|docker stop \<container id><br>docker rm \<container id>|Stop and remove running container|
|[DDid](ddid/)|docker inspect -f '{{.Id}}' \<container id>|Show container id|
|[DDsh](ddsh/)|docker exec -it \<container id> /bin/sh|Go into container with /bin/sh|
|[DDbash](ddbash/)|docker exec -it \<container id> /bin/bash|Go into container with /bin/bash|
|[DDmysql](ddmysql/)|docker exec -it \<container id> mysql -u root -proot|Go into container with mysql -u root -proot|
|DDmongo|docker exec -it \<container id> mongo -u root -p|Go into container with mongo -u root -p|
|[DDmyadmin](myadmin/)|docker run -d -e PMA_HOST=\<container IP adress> -p 8080:80 phpmyadmin/phpmyadmin|Run phpMyAdmin container and connect to your running container|
|[DDtop](ddtop/)|docker top \<container id>|Display the running processes of a container|
|[DDstats](ddstats/)|docker status|Display a live stream of container|
|[DDlogs](ddlogs/)|docker logs \<container id>|Fetch the logs of a container|
|[DDinspect](ddinspect/)|docker inspect \<container id>|Return low-level information on a container|
|[DDip](ddip/)|docker inspect -f "{{.NetworkSettings.IPAddress}}" \<container id>|Show the IP Address of a container|
|[DDhosts](ddhosts/)|docker exec -it \<container id> cat /etc/hosts|Show the contents in /etc/hosts file |
|[DDenv](ddenv/)|docker exec -it \<container id> env|List defined environment variables|
