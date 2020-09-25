# Repository

仓库（Repository）是集中存放镜像的地方。

## Docker Hub

Docker 官方维护了一个公共仓库 [Docker Hub](https://hub.docker.com/)。


## 注册

在 https://hub.docker.com 免费注册一个 Docker 账号。

## 登录和退出

docker login

docker logout

## 推送镜像

用户登录后，可以通过 docker push 命令将自己的镜像推送到 Docker Hub。

以下命令中的 username 请替换为你的 Docker 账号用户名。

```
PS D:\Program Files\Docker Toolbox> docker images
REPOSITORY                    TAG                 IMAGE ID            CREATED             SIZE
my-hello-world-nginx          latest              bede1a85d3ee        About an hour ago   7.91MB
redis                         latest              84c5f6e03bf0        2 weeks ago         104MB
jenkins                       latest              cd14cecfdb3a        2 years ago         696MB
kitematic/hello-world-nginx   latest              03b4557ad7b9        5 years ago         7.91MB
PS D:\Program Files\Docker Toolbox> docker tag my-hello-world-nginx:latest qiaoyafeng/my-hello-world-nginx:latest
PS D:\Program Files\Docker Toolbox> docker images
REPOSITORY                        TAG                 IMAGE ID            CREATED             SIZE
my-hello-world-nginx              latest              bede1a85d3ee        About an hour ago   7.91MB
qiaoyafeng/my-hello-world-nginx   latest              bede1a85d3ee        About an hour ago   7.91MB
redis                             latest              84c5f6e03bf0        2 weeks ago         104MB
jenkins                           latest              cd14cecfdb3a        2 years ago         696MB
kitematic/hello-world-nginx       latest              03b4557ad7b9        5 years ago         7.91MB
PS D:\Program Files\Docker Toolbox> docker push qiaoyafeng/my-hello-world-nginx:latest
The push refers to repository [docker.io/qiaoyafeng/my-hello-world-nginx]
1aa98e03e5b3: Pushed
5f70bf18a086: Pushed
b51acdd3ef48: Pushed
3f47ff454588: Pushed
f19fb69b288a: Pushed
b11278aeb507: Pushed
fb85701f3991: Pushed
15235e629864: Pushed
86882fc1175f: Pushed
9e8c93c7ea7e: Pushed
e66f0ebc2eef: Pushed
6a15a6c08ef6: Pushed
461f75075df2: Pushed
latest: digest: sha256:e874f56c0c4c77a60cd8185cea170a7bb2474d44a431d97712e36ac40e0172e3 size: 3433
PS D:\Program Files\Docker Toolbox>

```