# Docker

## build docker images from Dockerfile on the current directory with name <name>

> docker build . -t <name> --no-cache

## create buildx buildkit instance (untuk cross build ke prosesor intel) ini cuma run sekali aja

> docker buildx create --use --name buildx_instance

## build docker image amd64 and save to tar

> docker buildx build -f Dockerfile --platform linux/amd64 -t <name> . --load

## save image to tar.gz

> docker save <images-name> | gzip > <image-file-name>.tar.gz

## copy to server

> scp /tmp/<image-file-name>.tar.gz remote_username@remote_ip:/tmp

## login ssh to server

> ssh remote_username@remote_ip

## Load docker image from tar file

> docker load -i /tmp/<image-file-name>.tar.gz
