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
|[DDimages](DDimages/)|docker images |Show all images|
|[DDrmi](ddrmi/)|docker rmi \<image id>|Remove image|
|[DDrmia](ddrmia/)|docker rmi $(docker images -q)|Remove all images|
|[DDnone](ddnone/)|docker rmi $(docker images \| awk '/^<none>/ { print $3 }')|Remove \<none> image|
|[DDhistory](ddhistory/)|docker history \<image id>|Show the history of an image|