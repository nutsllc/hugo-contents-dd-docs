+++
title = "コンテナ関連"
date = 2019-10-13T12:17:07Z
weight = 2
chapter = true
pre = "<b>2. </b>"
+++

### Chapter 2

# コンテナ/イメージ<br>（DD Command）

|DD Command|In case of docker command|Description|
|:---|:---|:---|
|DD|docker ps -a|Show all containers|
|DDimages|docker images |Show all images|
|DDps|docker ps|Show running containers in default format|
|DDpsa|docker ps -a|Show all containers in default format|
|DDstart|docker start \<container id>|start stopped container|
|DDstop|docker stop \<container id>|Stop running container|
|DDstopa|docker stop $(docker ps -q)|Stop all of running container|
|DDrm|docker rm \<container id>|Remove a container|
|DDrma|docker rm $(docker ps -aq)|Remove all of running containers|
|DDdown|docker stop \<container id><br>docker rm \<container id>|Stop and remove running container|
|DDid|docker inspect -f '{{.Id}}' \<container id>|Show container id|
|DDrmi|docker rmi \<image id>|Remove image|
|DDrmia|docker rmi $(docker images -q)|Remove all images|
|DDnone|docker rmi $(docker images \| awk '/^<none>/ { print $3 }')|Remove \<none> image|
|DDidi|docker inspect -f '{{.Id}}' \<image id>|Show image id|
|DDbash|docker exec -it \<container id> /bin/bash|Go into container with /bin/bash|
|DDsh|docker exec -it \<container id> /bin/sh|Go into container with /bin/sh|
|DDmysql|docker exec -it \<container id> mysql -u root -proot|Go into container with mysql -u root -proot|
|DDmongo|docker exec -it \<container id> mongo -u root -p|Go into container with mongo -u root -p|
|DDmyadmin|docker run -d -e PMA_HOST=\<container IP adress> -p 8080:80 phpmyadmin/phpmyadmin|Run phpMyAdmin container and connect to your running container|
|DDstats|docker status|Display a live stream of container|
|DDtop|docker top \<container id>|Display the running processes of a container|
|DDlogs|docker logs \<container id>|Fetch the logs of a container|
|DDhistory|docker history \<image id>|Show the history of an image|
|DDinspect|docker inspect \<container id>|Return low-level information on a container|
|DDip|docker inspect -f "{{.NetworkSettings.IPAddress}}" \<container id>|Show the IP Address of a container|
|DDvol|docker |List volumes of a container mounted|
|DDhosts|docker exec -it \<container id> cat /etc/hosts|Show the contents in /etc/hosts file |
|DDenv|docker exec -it \<container id> env|List defined environment variables|
