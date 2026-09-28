
Followed the instructions here:

https://people.ece.ubc.ca/os161/os161-site/install-docker.html




```console
wget https://people.ece.ubc.ca/~os161/download/os161-cpen331-docker.tar.gz
gunzip os161-cpen331-docker.tar.gz
tar -xvf os161-cpen331-docker.tar
cd os161-cpen331-docker
docker build -t os161 .
```

The docker file contains a `#FROM debian:11` line which I replaced with `FROM debian`. The build was then successful.
