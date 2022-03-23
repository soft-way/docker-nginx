# About this Repo
This repo is based on below official Docker image. Thie repo built from source code and some dev tools added.

This is the Git repo of the official Docker image for [nginx](https://registry.hub.docker.com/_/nginx/). See the
Hub page for the full readme on how to use the Docker image and for information
regarding contributing and issues.

The full readme is generated over in [docker-library/docs](https://github.com/docker-library/docs),
specifically in [docker-library/docs/nginx](https://github.com/docker-library/docs/tree/master/nginx).

The changelog for NGINX releases is available at [nginx.org changes page](https://nginx.org/en/CHANGES).


# Build steps
```bash
git clone https://github.com/soft-way/docker-nginx.git
cd docker-nginx/mainline/alpine

#
# if you under proxy, please add proxy build arg as below
# --build-arg https_proxy=http://10.10.10.10:8080/
# if you need more dev tools, add below package list
# --build-arg dev_apk_list="bash bind-tools loksh pigz tcpdump xz"
# if you want to enable debug log, add below arg
# --build-arg debug=yes
#
docker build -t nginx:1.21.6-alpine-3.15 .
```

# Know issues
1. There is issue "make dir permission issue" in docker-ce (19.03.8), please upgrade docker-ce to 20.10.13+
