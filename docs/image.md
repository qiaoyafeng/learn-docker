#  Docker 镜像使用

- 1、管理和使用本地 Docker 主机镜像
- 2、创建镜像

## 列出镜像列表

docker images  列出本地主机上的镜像。


```
REPOSITORY                    TAG                 IMAGE ID            CREATED             SIZE
my-hello-world-nginx          latest              bede1a85d3ee        32 minutes ago      7.91MB
redis                         latest              84c5f6e03bf0        2 weeks ago         104MB
jenkins                       latest              cd14cecfdb3a        2 years ago         696MB
kitematic/hello-world-nginx   latest              03b4557ad7b9        5 years ago         7.91MB
```

各个选项说明:
- REPOSITORY：表示镜像的仓库源
- TAG：镜像的标签
- IMAGE ID：镜像ID
- CREATED：镜像创建时间
- SIZE：镜像大小



## 使用镜像来运行容器

docker run -t -i jenkins:latest /bin/bash

```
PS D:\Program Files\Docker Toolbox> docker run -t -i jenkins:latest /bin/bash
jenkins@0482efe9a7f1:/$

```

参数说明：

- -i: 交互式操作。
- -t: 终端。
- ubuntu:15.10: 这是指用 ubuntu 15.10 版本镜像为基础来启动容器。
- /bin/bash：放在镜像名后的是命令，这里我们希望有个交互式 Shell，因此用的是 /bin/bash。


## 获取一个新的镜像
在本地主机上使用一个不存在的镜像时 Docker 就会自动下载这个镜像。如果我们想预先下载这个镜像，我们可以使用 docker pull 命令来下载它。

## 查找镜像

docker search httpd

## 拖取镜像

docker pull httpd

## 删除镜像

docker rmi hello-world