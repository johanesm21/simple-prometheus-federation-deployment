# simple-prometheus-federation-deployment
Deployment files for multi node prometheus with federation

There consists of 3 prometheus instance deployed with docker / podman (each of them scrapping prometheus metrics itself):
- prometheus-1 in port 9091
- prometheus-2 in port 9092
- prometheus-3 in port 9093