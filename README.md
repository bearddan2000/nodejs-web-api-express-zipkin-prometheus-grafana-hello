# nodejs-web-api-express-zipkin-prometheus-grafana-hello

## Description
Shows REST api metrics, timings and status code.
Uses prometheus to graph response times
and grafana for low level metrics.

### STEP 1
Once the project is done building, make
some api calls `http://localhost:81`.

### STEP 2
- goto http://localhost
- click on "Find a trace"
  - search by "serviceName"

To see a graph of response times:
- Nav to http://localhost:82
- Classic UI
  - Click Graph tab
    - Search: 'scrape_samples_scrape'
    - Duration 1m

For health check:
- Nav to http://localhost:82
- Targetes

To see Prometheus dashboards:
- Nav to http://localhost:83
- Login with `admin/admin`
- configuration -> datasources
  - Select Prometheus
    - dashboards
      - import and click label

To see Zipkin dashboards:
- Nav to http://localhost:83
- Login with `admin/admin`
- Explore
  - Change datasource to Zipkin

## Tech stack
- nodejs
- prometheus

## Docker stack
- node:latest
- openzipkin/zipkin
- prom/prometheus
- grafana/grafana

## To run
`sudo ./install.sh -u`
- API http://localhost:81
- ZIPKIN DASHBOARD http://localhost
- PROMETHEUS DASHBOARD http://localhost:82
- GRAFANA DASHBOARD http://localhost:83
  - Login with `admin/admin`

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
- https://medium.com/trabe/tracing-express-services-with-zipkin-js-6e5c5680467e
