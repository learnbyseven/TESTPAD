# TESTPAD
# TEST USE CASES 


### Python script to export metadata from Kubernetes cluster
  PATH="/root/SECURE-DEMO/api"
  ENV = SYSAWS
  
### SYSDIG_PYTHON CLIENT : https://github.com/draios/python-sdc-client

- python create_dashboard.py <API_TOKEN>
- python get_data.py <API_TOKEN>
- Review create_dashboard.py, get_data.py
 


# Possibility of automating the custom dashboard creation in a new sysdig environment rather than creating from scratch


## Download Dashboards  (REPLACE DASHBOARD ID 133729 with ORIGINAL DASHBOARD ID)


### curl -X GET https://app.sysdigcloud.com/api/v2/dashboards/133729 -H 'Authorization: Bearer <TOKEN>' -H 'Content-Type: application/json' > dashboard.json

## Create dashboards 

### curl -X POST https://app.sysdigcloud.com/api/v2/dashboards -H 'Authorization: Bearer <TOKEN>' -H 'Content-Type: application/json' -d @dashboard.json 
 

# View to show the affinity with external services (outside kubernetes cluster) and export of the same
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


