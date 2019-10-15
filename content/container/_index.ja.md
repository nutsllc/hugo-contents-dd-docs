+++
title = "コンテナ/イメージ"
date = 2019-10-13T12:17:07Z
weight = 2
chapter = true
pre = "<b>2. </b>"
+++

### Chapter 2

# コンテナ/イメージ<br>（DD Command）

|DD Command|In case of docker command|Description|
|:---|:---|:---|
|[DD](dd/)|docker ps -a|Show all containers|
|[DDimages](DDimages/)|docker images |Show all images|
|[DDps](ddps/)|docker ps|Show running containers in default format|
|[Dpsa](ddpsa/)|docker ps -a|Show all containers in default format|
|[DDstart](ddstart/)|docker start \<container id>|start stopped container|
|[DDstop](ddstop/)|docker stop \<container id>|Stop running container|
|[DDstopa](ddstopa/)|docker stop $(docker ps -q)|Stop all of running container|
|[DDrm](ddrm/)|docker rm \<container id>|Remove a container|
|[DDrma](ddrma/)|docker rm $(docker ps -aq)|Remove all of running containers|
|[DDdown](dddown/)|docker stop \<container id><br>docker rm \<container id>|Stop and remove running container|
|[DDid](ddid/)|docker inspect -f '{{.Id}}' \<container id>|Show container id|
|[DDrmi](ddrmi/)|docker rmi \<image id>|Remove image|
|[DDrmia](ddrmia/)|docker rmi $(docker images -q)|Remove all images|
|[DDnone](ddnone/)|docker rmi $(docker images \| awk '/^<none>/ { print $3 }')|Remove \<none> image|
|[DDidi](ddidi)|docker inspect -f '{{.Id}}' \<image id>|Show image id|
|[DDbash](ddbash/)|docker exec -it \<container id> /bin/bash|Go into container with /bin/bash|
|[DDsh](ddsh/)|docker exec -it \<container id> /bin/sh|Go into container with /bin/sh|
|[DDmysql](ddmysql/)|docker exec -it \<container id> mysql -u root -proot|Go into container with mysql -u root -proot|
|DDmongo|docker exec -it \<container id> mongo -u root -p|Go into container with mongo -u root -p|
|DDmyadmin|docker run -d -e PMA_HOST=\<container IP adress> -p 8080:80 phpmyadmin/phpmyadmin|Run phpMyAdmin container and connect to your running container|
|[DDstats](ddstats/)|docker status|Display a live stream of container|
|[DDtop](ddtop/)|docker top \<container id>|Display the running processes of a container|
|[DDlogs](ddlogs/)|docker logs \<container id>|Fetch the logs of a container|
|[DDhistory](ddhistory/)|docker history \<image id>|Show the history of an image|
|[DDinspect](ddinspect/)|docker inspect \<container id>|Return low-level information on a container|
|[DDip](ddip/)|docker inspect -f "{{.NetworkSettings.IPAddress}}" \<container id>|Show the IP Address of a container|
|[DDhosts](ddhosts/)|docker exec -it \<container id> cat /etc/hosts|Show the contents in /etc/hosts file |
|[DDenv](ddenv/)|docker exec -it \<container id> env|List defined environment variables|
