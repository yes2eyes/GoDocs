# Docker

1. 镜像
2. 容器
3. 构建

> 1. 操作客户端 2. 构建：会写DockerFile 3. 会写复杂的 dokcer-compose 4. 会使用 daocloud 自动化构建



## 1. 镜像

## 2. 容器

## 3. 构建

分层

- FROM  基础镜像
- MAINTINER
- RUN : shell 、exec
- EXPOSE 端口
- CMD ： shell、exec
- ENTRYPOINT
- ADD
- COPY
- VOLUME
- WORKDIR
- ENV
- USER
- ONBUILD
## 4. 常用的容器的组件的操作


## 5. 如何利用开源的免费服务自动构建自己的镜像

- Dockerfile
- TravisCI ：services docker 
- Github(gitlab) + DockerHub | DaoCloud
- Docker-compose 

## 6.

- docker rm $(sudo docker ps -a -q) # 删除停止的容器


## 7 文件操作

```

本地文件移入容器内
docker cp path/file dockerUUID:/path/file

容器内文件移入本地
docker cp dockerUUID:/path/file path/file
```

```

本地文件上传至服务器
scp path/file ip:port:/path

服务器文件下载至本地
scp ip:port:/path/file path
```