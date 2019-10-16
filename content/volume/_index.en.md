+++
title = "Volume"
date = 2019-10-13T12:17:07Z
weight = 13
chapter = true
pre = "<b>5. </b>"
+++

### Chapter 5

# Volume<br>（DV Command）

|Docker DD|In case of docker command|Description|
|:---|:---|:---|
|DV|docker volume ls|Show all volumes|
|DVrm|docker volume  rm \<volume name>|Remove a volume|
|DVid|docker volume inspect -f "{{.Name}}" \<volume name>|Show a volume name|
|DVmp|docker volume inspect -f "{{.Mountpoint}}" \<volume name>|Show the directory path stored real data|
|DVinspect|docker volume inspect \<volume name>|Display detailed information on volume|

