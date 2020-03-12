# Introduction

This repository hosts Dashboards for Grafana

# Dashboards

## cplace Logs
> File: cplace_logs.json  
> Datasource: Elasticsearch (JSON)

This dashboard uses the Elasticsearch datasource and displays logs of the cplace appliction which are forwarded by fluent-bit
to Elasticsearch. cplace logs are generated as JSON.

## cplace Metrics
> File: cplace_metrics.json  
> Datasource: Prometheus

This dashboard uses the Prometheus datasource and displays the cplace application specific internals.
The data is scraped by Prometheus from each cplace instance by calling the prometheus.txt endpoint.

## cplace Elasticsearch Logs
> File: cplace_es_logs.json  
> Datasource: Elasticsearch (Text)

This dashboard displays logs from the Elasticsearch service used by the cplace solution.

## cplace Jetty Logs
> File: cplace_jetty_logs.json  
> Datasource: Elasticsearch (JSON)

This dashboard visualizes logs from the embedded Jetty server from cplace.

## Kubernetes System Logs
> File: k8s_logs.json  
> Datasource: Elasticsearch (Text)

This dashboards shows logs from the Kubernetes System (kube-system namespace) in a Table.

## Fluent-bit Metrics
> File: fluentbit_metrics.json  
> Datasource: Prometheus

This dashbard visualizes the metrics provided by the fluent-bit log forwarder.

# Exporting new Dashboard Version
When a new dashboard version is exported from Grafana, please ensure:

* Set uid key to **null**: ```"uid": null,```
* Empty filter options: ```"options": [],```
* Ensure version key is incremented