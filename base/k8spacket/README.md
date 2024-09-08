 helm upgrade --install k8spacket -f values.yaml --namespace k8spacket k8spacket/k8spacket --create-namespace

 values.yaml ist für Grafana

 Dashboards sind auch da

 Wir brauchen eine weitere scape-config
 (geht aus auch mit servicemonitor?

~~~
- job_name: "k8spacket-metrics"
  metrics_path: /metrics
  scrape_interval: 25s
  static_configs:
  - targets: [k8spacket.k8spacket.svc.cluster.local:8080]
~~~

~~~
kubectl create secret generic additional-scrape-configs --from-file=prometheus-additional.yaml --dry-run -oyaml > additional-scrape-configs.yaml
~~~

~~~
kubectl -n monitoring apply -f additional-scrape-configs.yaml
~~~


Edit prometheus operator


~~~
  additionalScrapeConfigs:
    name: additional-scrape-configs
    key: prometheus-additional.yaml
~~~
