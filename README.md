# TEST USE CASES 


# 1. Python script to export metadata from Kubernetes cluster
  PATH="/root/SECURE-DEMO/api"
  ENV = SYSAWS
  
#### SYSDIG_PYTHON CLIENT : https://github.com/draios/python-sdc-client

- python get_data.py <API_TOKEN> (Review "metrics") 
- python create_dashboard.py <API_TOKEN> (Review "view") 

# 2. Create custom dashboard for Kubernetes objects including PVs
IBMDASHBOARD
 


# 3. Possibility of automating the custom dashboard creation in a new sysdig environment rather than creating from scratch


### Download Dashboards  (REPLACE DASHBOARD ID 133729 with ORIGINAL DASHBOARD ID)


#### curl -X GET https://app.sysdigcloud.com/api/v2/dashboards/133729 -H 'Authorization: Bearer <TOKEN>' -H 'Content-Type: application/json' > dashboard.json

### Create dashboards 

#### curl -X POST https://app.sysdigcloud.com/api/v2/dashboards -H 'Authorization: Bearer <TOKEN>' -H 'Content-Type: application/json' -d @dashboard.json 
 

# 4. View to show the affinity with external services (outside kubernetes cluster) and export of the same
- /root/SECURE-DEMO/sysdig_demo/externaldb

Kubernetes
WEBFRONT                                               
http://ec2-13-234-209-96.ap-south-1.compute.amazonaws.com:32301 (Within Cluster)
 |
 |
 |
 |
ExternalDB 
ClusterIP   10.109.56.152 (Within Cluster) 
 |
 |
 |
EP : 15.206.49.8:3306 (Outside Cluster) 

NS - externaldb
Metrics - Topology MAP Response Time 




# USECASES
## Connection alerts
1. External service availability
2. Database connection
3. AMQ availability

## POD
1. Deployments
2. Availability
3. Memory /JVM

## Scaling
1. Response time (DB Call, service call)

## Database
1. Space alerts
2. long running queries
3. no. of connections







