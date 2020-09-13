# Grafana docker image for Ganesha

Files to create a Docker image for Grafana, pre-configured with dashboards for NFS Ganesha.

The Grafana instance connects to a Prometheus instance on the same host on tcp port 9090.

## To build image:
docker build -t my_image_tag -f Dockerfile.grafana  .

## To run image:
docker run -d --restart=unless-stopped --name grafana -p 3000:3000 my_image_tag
