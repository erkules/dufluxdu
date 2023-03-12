certmanager für lokale Certs verwenden

Grafana soll ausserhalb von Monitoring lauschen:
   z.B. wegen kyverno-reporter Dashboards   <-- Könnten das im Reporter-Helmchart setzen, aber das ist nicht unsere Idee


sshwifty hat eigentlich auch eine Abhängigkeit zum ngingx. Nur haben wir Abhängigkeiten mit Helmreleases aufgebaut. 
  sshwifty ist aber ein schlichtes Deployment.
