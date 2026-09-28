
Followed the instructions here:

https://people.ece.ubc.ca/os161/os161-site/install-docker.html


```console
wget https://people.ece.ubc.ca/~os161/download/os161-cpen331-docker.tar.gz
gunzip os161-cpen331-docker.tar.gz
tar -xvf os161-cpen331-docker.tar
cd os161-cpen331-docker
docker build -t os161 .
```

The os161-cpen331-docker.tar.gz file is uploaded here. The docker file contains a `#FROM debian:11` line which I replaced with `FROM debian`. The build was then successful. Note that the docker
file pulls files from the UBC website. I have uploaded those files here as well.
