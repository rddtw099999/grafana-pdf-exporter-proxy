# Grafana PDF Exporter Dockerfile


Based on following repositories  
-   [kartik468's grafana-generate-pdf-nodejs](https://github.com/kartik468/grafana-generate-pdf-nodejs)
-  [znerol's grafana-pdf-proxy](https://github.com/znerol/grafana-pdf-proxy)

with latest node:slim docker image and add Chinese support.

binding address and backend address can be configured in docker-compose.yaml file.


## How to generate PDF:

 1. Export By links:

	Add links :

	Dashboard -> Settings -> Links -> New Link

	Title: `Export PDF`

	Type: `Links`

	URL: `http://{Binding Address}:{Binding Link}/d/{Dashboard Link}/{Dashboard Name}?orgId=1`

	Icon: `doc`

	 [ `v`] Include current time range

	 [ `v`] Include current template variable
       values
    

 3. Export by command (or add in crontab):
    
    `curl -o /tmp/export.pdf http://{Binding Address}:{Binding Link}/d/{Dashboard Link}/{Dashboard Name}?orgId=1`

