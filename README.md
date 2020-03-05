# Introduction

This repository hosts Dashboards for Grafana

# Dashboards

## cplace Logs
This dashboard uses the Elasticsearch datasource and displays logs of the cplace appliction which are forwarded by fluent-bit
to Elasticsearch. cplace logs are generated as JSON.

## cplace Metrics
This dashboard uses the Prometheus datasource and displays the cplace application specific internals.
The data is scraped by Prometheus from each cplace instance by calling the prometheus.txt endpoint.

# Exporting new Dashboard Version
When a new dashboard version is exported from Grafana, please ensure:

* Set uid key to **null**: ```"uid": null,```
* Empty filter options: ```"options": [],```
* Ensure version key is incremented