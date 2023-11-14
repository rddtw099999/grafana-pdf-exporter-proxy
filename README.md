# Grafana PDF Exporter Dockerfile


Based on following repositories  
-   [kartik468's grafana-generate-pdf-nodejs](https://github.com/kartik468/grafana-generate-pdf-nodejs)
-  [znerol's grafana-pdf-proxy](https://github.com/znerol/grafana-pdf-proxy)

with latest node docker image and add Chinese support

backend address binds on http://grafana:3000 ,and api exposed on. [http://{containeraddress}:8083](http://%7Bcontaineraddress%7D:8083)

