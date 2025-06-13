[] Contour läuft nicht mit Certificate
  base/contour/values.yaml -> self-signed enablen und cluster-vars verwenden wegen domain
  alternativ mit certmanager 
[] Wir wollen flux mit KSM monitoren
   https://github.com/fluxcd/flux2-monitoring-example/blob/bcae1ef44963da89caabe962a93280c0dfad3381/monitoring/controllers/kube-prometheus-stack/kube-state-metrics-config.yaml#L114-L132

[]certmanager für lokale Certs verwenden


[]sshwifty hat eigentlich auch eine Abhängigkeit zum ngingx. Nur haben wir Abhängigkeiten mit Helmreleases aufgebaut. 
  sshwifty ist aber ein schlichtes Deployment.


[done]Prometheus soll out of the box nach annotations scrapen (wie früher)

[done]Was ist mit dummy-object.yaml im Keda

./prometheus/prometheus-release.yaml <- hier depends_on raus genommen wohl wieder rein

[] Redesign all. Wir haben Kreispendencies
[] oauth-proxy mit basic-auth

[]Doppelt!!
loki-promtail/grafana-datasource.yaml
./loki/grafana-datasource.yaml

[]Grafana braucht nen sidecar welchen configmaps via api synct

