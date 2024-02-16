# simple-prometheus-federation-deployment
Deployment files for multi node prometheus with federation

There consists of 3 prometheus instance deployed with docker / podman (each of them scrapping prometheus metrics itself):
- prometheus-1 in port 9091
- prometheus-2 in port 9092
- prometheus-3 in port 9093

## How to deploy:
- download this code to your server
```shell
wget https://github.com/johanesm21/simple-prometheus-federation-deployment.git
```
- change directory to downloaded code
```shell
cd simple-prometheus-federation-deployment
```
- create directories and change its ownership to 589821:589821 (because Prometheus's data directory by default owned by 589821:589821)
```shell
mkdir ./prometheus-1/data/ ; sudo chown 589821:589821 ./prometheus-1/data/
mkdir ./prometheus-2/data/ ; sudo chown 589821:589821 ./prometheus-2/data/
mkdir ./prometheus-3/data/ ; sudo chown 589821:589821 ./prometheus-3/data/
```
- run with docker / podman compose
```shell
podman compose up -d
```