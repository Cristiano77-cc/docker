# docker
学习笔记
安装docker 指定版本，离线安装
设置仓库
安装所需的软件包。yum-utils 提供了 yum-config-manager ，并且 device mapper 存储驱动程序需要 device-mapper-persistent-data 和 lvm2。
$ sudo yum install -y yum-utils \
  device-mapper-persistent-data \
  lvm2

设置stable镜像仓库
推荐
yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo

更新yum软件包索引
yum makecache fast

安装DOCKER CE
yum list docker-ce --showduplicates | sort -r
通过其完整的软件包名称安装特定版本，该软件包名称是软件包名称（docker-ce）加上版本字符串（第二列），从第一个冒号（:）一直到第一个连字符，并用连字符（-）分隔。例如：docker-ce-18.09.1。
$ sudo yum install docker-ce-<VERSION_STRING> docker-ce-cli-<VERSION_STRING> containerd.io

yum install -y docker-ce-19.03.12-3.el7 docker-ce-cli-19.03.12-3.el7 containerd.io

启动docker
systemctl start docker
