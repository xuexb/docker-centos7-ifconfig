# docker-centos7-ifconfig

用于测试发布的第一个镜像，虽说代码就几行，但这也表示我要研究 Docker 了。

主要用来运行 `ifconfig` 命令。

## 使用

```bash
docker run -it xuexb/docker-centos7-ifconfig
```

### --net=none

无网络

### --net=bridge

默认值，桥接。会自动分配 IP ，打开的不同容器可以互相 `ping` 通。

### --net=host

多个容器共用一个 IP ，容器间可以 `ping` 通。

### --net=container:name

克隆对应容器的网络信息。