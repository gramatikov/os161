
This document provides a path for setting up System/161 and OS/161. I followed the instructions here:

https://people.ece.ubc.ca/os161/os161-site/install-docker.html

```console
wget https://people.ece.ubc.ca/~os161/download/os161-cpen331-docker.tar.gz
gunzip os161-cpen331-docker.tar.gz
tar -xvf os161-cpen331-docker.tar
cd os161-cpen331-docker
docker build -t os161 .
```

The os161-cpen331-docker.tar.gz file is uploaded here. The docker file contains a `#FROM debian:11` line which I replaced with `FROM debian`. My docker build was then successful. Note that the docker
file pulls files from the UBC website. I have uploaded a files.txt with the urls. Some of these files were large (gcc, gdb, binutils) and were therefore not uploaded here. However if the UBC links no longer work, I believe they are also hosted on http://www.os161.org/.


Running the container

The following command mounts the home directory. I replaced "/home/OS_BASE".

```console
docker run -dit --mount type=bind,src=/home/OS_BASE,target=/root/os161 --rm --name os161 os161
```
You now have to get the container ID by running `docker ps`. Then run 

```console
docker exec -it <ID> /bin/bash
```
with your ID.
