This repo is an extension on the pilight project.

It contains the following modules:

1. Pilight Dockerfile which can be pulled from hub.docker.com. 
2. And a Qt gui which used the pilight API. (To be created in the near future)

build Dockerfile:
cd docker/stable
docker build -t pilight .
docker run --rm -it -p 5001:5001 pilight
