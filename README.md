com.zjl.springcloud-config 配置中心



拉取命令：

```.git
git clone git@github.com:EternalPain/springcloud-config.git
```



yml文件配置：
```.yml
spring:
  application:
    name: cloud-config-server   # 注册进 Eureka 服务器的服务名
  cloud:
    config:
      server:
        git:
#          username: 账号
#          password: 密码
#          uri: https://github.com/EternalPain/com.zjl.springcloud-config.git  # GitHub 的 https 仓库地址

          # ssh连接 需配置 SSH keys
          uri: git@github.com:EternalPain/com.zjl.springcloud-config.git  # GitHub 的 git 仓库地址
          search-paths:   # 读取目录
            - springcloud-config
      label: main   # 读取的分支
```
