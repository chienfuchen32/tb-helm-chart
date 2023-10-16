# tb helm chart
## prerequisite
* helm version: v3.12.3
* Azure Kubernetes Service, version: 1.26.3
* Azure Postgresql Flexible server, version: 14.8, `Standard_D2ds_v4` * 1
* Azure Managed Cassandra, version: 4.0 ,`Standard_D8s_v5` * 3
* Azure Cache for Redis, version: 6, `P1` * 1
* Azure Application Gateway, `WAF_V2` auto scale (2 - 10 instance)

## Installation guide
```bash
$ kubectl create ns thingsboard
$ helm install -f values.yaml thingsboard -n thingsboard .
$ helm upgrade -f values.yaml thingsboard -n thingsboard .
$ helm uninstall thingsboard -n thingsboard
```
