# Docker-compose sample for Apache Bigtop-Manager

### How to run
Prepare
* copy files from bigtop-manager
  * copy `bigtop-manager-server/target/bigtop-manager-server` to `./bigtop-manager/bigtop-manager-server`
  * copy `bigtop-manager-agent/target/bigtop-manager-agent` to `./bigtop-manager-agent/bigtop-manager-agent`
* build images
  * `docker-compose build bm-master`
  * `docker-compose build bm-node1`

Run mysql first
* `docker-compose up -d bm-mysql`

Run bigtop-manager-server
* `docker-compose up -d bm-master`

Run nodes
* `docker-compose up -d bm-node1 bm-node2 bm-node3`

### Access Web UI

Browse http://localhost:18080, then login with `admin`/`admin`

Swagger UI from http://localhost:18080/swagger-ui/index.html 

# Current Status
* Could not make cluster and/or host from UI
* Could not call `stacks` directory from resources