+++
title = "Network"
date = 2019-10-13T12:17:07Z
weight = 12
chapter = true
pre = "<b>4. </b>"
+++

### Chapter 4

# Network<br>（DN Command）

|Docker DD|In case of docker command|Description|
|:---|:---|:---|
|DN|docker network ls|Show all networks|
|DNrm|docker network rm \<network id>|Remove a network|
|DNid|docker network inspectm -f '{{.Id}}' \<network id>|Show a network id |
|DNgateway|docker network inspect -f '{{range .IPAM.Config}} {{.Gateway}} {{end}}' \<network id>|Show the Gateway IPv4 Address of a network|
|DNsubnet|docker network inspect -f '{{range .IPAM.Config}} {{.Subnet}} {{end}}' \<network id>|Show the Subnet IPv4 Address of a network|
|DNnode|docker network inspect -f '{{range .Containers}} {{.Name}} {{end}}'|List containers connected a network|
|DNinspect|docker network inspect \<network id>|Display detailed information on network|