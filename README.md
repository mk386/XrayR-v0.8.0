# XRayR
A Xray backend framework that can easily support many panels.

一个基于Xray的后端框架，支持V2ay,Trojan,Shadowsocks协议，极易扩展，支持多面板对接

Find the source code here: [XrayR-project/XrayR](https://github.com/XrayR-project/XrayR)（已遁入虚空）

v0.8.0 最后之作

# 详细使用教程

[教程](https://crackair.gitbook.io/xrayr-project/)

# 一键安装

```
bash <(curl -Ls https://raw.githubusercontent.com/jue0115/XrayR/main/install.sh)
```

# Docker 安装

```
docker pull jue115/xrayr:latest && docker run --restart=always --name xrayr -d -v ${PATH_TO_CONFIG}/config.yml:/etc/XrayR/config.yml --network=host jue115/xrayr:latest
```

# Docker compose 安装
0. 安装docker-compose: 
```
curl -fsSL https://get.docker.com | bash -s docker
curl -L "https://github.com/docker/compose/releases/download/1.26.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```
1. `wget -N --no-check-certificate https://raw.githubusercontent.com/jue0115/XrayR/main/docker-compose.yml`
2. `chmod +x docker-compose.yml`
3. 编辑config。
配置文件基本格式如下，Nodes下可以同时添加多个面板，多个节点配置信息，只需添加相同格式的Nodes item即可。
4. 启动docker：`docker-compose up -d`

## Docker compose升级
在docker-compose.yml目录下执行：
```
docker-compose pull
docker-compose up -d
```
