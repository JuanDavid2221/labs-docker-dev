## Descarga ubuntu

@JuanDavid2221 ➜ /workspaces/labs-docker-dev (main) $ docker pull ubuntu
Using default tag: latest
latest: Pulling from library/ubuntu
9c704ecd0c69: Pull complete 
Digest: sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
Status: Downloaded newer image for ubuntu:latest
docker.io/library/ubuntu:latest

## Descarga pyton 3.9

@JuanDavid2221 ➜ /workspaces/labs-docker-dev (main) $ docker pull python:3.9
3.9: Pulling from library/python
ca4e5d672725: Pull complete 
30b93c12a9c9: Pull complete 
10d643a5fa82: Pull complete 
d6dc1019d793: Pull complete 
c7d45ab0573c: Pull complete 
564d1c451ea7: Pull complete 
ddfb50ba1977: Pull complete 
91b87d81d4c8: Pull complete 
Digest: sha256:65438c2e26dbf9f5db4b5553e332747fa20722c1b7c7ccc6f8480396ff4186db
Status: Downloaded newer image for python:3.9
docker.io/library/python:3.

## Ejecutar contenedor

@JuanDavid2221 ➜ /workspaces/labs-docker-dev (main) $ docker run -d -p 8000:80 httpd
Unable to find image 'httpd:latest' locally
latest: Pulling from library/httpd
efc2b5ad9eec: Pull complete 
fce1785eb819: Pull complete 
4f4fb700ef54: Pull complete 
f214daa0692f: Pull complete 
05383fd8b2b3: Pull complete 
88ad12232aa1: Pull complete 
Digest: sha256:932ac36fabe1d2103ed3edbe66224ed2afe0041b317bcdb6f5d9be63594f0030
Status: Downloaded newer image for httpd:latest
1f5c0bcdce3ab2024ca56d0aa434eaaa121117ec98349bd29a6639ab9a43e3ff
 
 ## Contenedor de Ubuntu 

 @JuanDavid2221 ➜ /workspaces/labs-docker-dev (main) $ docker run -it ubuntu bash
root@83bf65b5a87a:/# ls -a
.  ..  .dockerenv  bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@83bf65b5a87a:/# 

## Eliminar contenedores

@JuanDavid2221 ➜ /workspaces/labs-docker-dev (main) $ docker ps -a
CONTAINER ID   IMAGE     COMMAND              CREATED          STATUS                        PORTS                                   NAMES
83bf65b5a87a   ubuntu    "bash"               24 minutes ago   Exited (129) 15 seconds ago                                           trusting_edison
14bd9faa34cd   httpd     "httpd-foreground"   24 minutes ago   Created                                                               infallible_zhukovsky
1f5c0bcdce3a   httpd     "httpd-foreground"   28 minutes ago   Up 28 minutes                 0.0.0.0:8000->80/tcp, :::8000->80/tcp   awesome_meninsky
b9a8a324fd37   ubuntu    "bash"               30 minutes ago   Exited (129) 28 minutes ago                                           competent_engelbart
@JuanDavid2221 ➜ /workspaces/labs-docker-dev (main) $ docker rm 83bf65b5a87a
83bf65b5a87a
@JuanDavid2221 ➜ /workspaces/labs-docker-dev (main) $ docker container prune
WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
14bd9faa34cd9965b8f0875659bcb1b32d68f28d2c0d4663c3dc20d5ca1b042f
b9a8a324fd379cc92eae970cb1b30d292cc4e106f49cf505a86a3662150317a1

Total reclaimed space: 88B