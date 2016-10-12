# Introduce

本项目用于构建星火计划中的以太坊节点。

项目使用[docker](https://docs.docker.com/engine/installation/) 和
[compose](https://docs.docker.com/compose/install/)，请预先安装

# usage

* 启动(以geth为例)

```bash
# cp docker-compose-geth.yml docker-compose.yml
# <所有的自定义内容都在 docker-compose.yml 文件中>
# <用户至少需要修改下面两条：>
#     instance: 用于在dashboard上显示你的节点名
#     contact_details: 用于提供本节点的维护者联系方式，通常是邮箱
# docker-compose up -d
```


* volume目录

唯一和宿主机相关的信息是 volume 目录，用户在初次使用时需要设定映射关系

`其它时候（包括重建容器）都不需要修改 volume 信息`

* 升级/降级

用户唯一需要做的就是指明目标版本，修改后重建容器节点即可。

```bash
# < edit image version on docker-compose.yml >
# docker-compose down
# docker-compose up -d
```

