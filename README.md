# baota_docker
```bash
mkdir -p /home/baota
cd /home/baota
# 解压缩www到当前目录
tar xf baota_www-lnmp_8.0.3.tar.gz

# 拉取镜像（阿里云）
docker pull registry.cn-shanghai.aliyuncs.com/jf177/pub:baota-centos7.9-lnmp-base.8.0.3

# 运行容器
docker run -itd  --name baota -h baota -v ./www:/www --network host registry.cn-shanghai.aliyuncs.com/jf177/pub:baota-centos7.9-lnmp-base.8.0.3

# 宝塔面板访问链接 http://IP:40035/127127
# username: baota.baota.baota
# password: 127.0.0.127
# 务必登录之后修改关键配置
