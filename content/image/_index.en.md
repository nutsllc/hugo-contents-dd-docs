+++
title = "Image"
date = 2019-10-13T12:17:07Z
weight = 11
chapter = true
pre = "<b>3. </b>"
+++

### Chapter 3

# Image<br>（DD）

|DD Command|In case of docker command|Description|
|:---|:---|:---|
|[DDimages](ddimages/)|docker images |Show all images|
|[DDrmi](ddrmi/)|docker rmi \<image id>|Remove image|
|[DDrmia](ddrmia/)|docker rmi $(docker images -q)|Remove all images|
|[DDnone](ddnone/)|docker rmi $(docker images \| awk '/^<none>/ { print $3 }')|Remove \<none> image|
|[DDidi](ddidi)|docker inspect -f '{{.Id}}' \<image id>|Show image id|
|[DDhistory](ddhistory/)|docker history \<image id>|Show the history of an image|