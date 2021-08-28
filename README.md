# 愿景 Discord <-> QQ 互通桥

## 本库安装使用方式
### 一、启动MCL (mirai一键安装环境工具)
> 使用Docker的方式
1. 修改文件 `mcl-1.1.0-beta.1/config/Console/AutoLogin.yml` 添加属于你的qq账号
2. 直接运行命令 `docker-compose up`
正常情况，bot收到消息后，控制台会看的到就成功了

> 非Docker的方式

1. 安装java jdk 并且11以上的版本，配置好java环境变量， 控制台输入`java --version` 能看到版本信息就正常
2. 修改文件 `mcl-1.1.0-beta.1/config/Console/AutoLogin.yml` 添加属于你的qq账号
3. 进入`mcl-1.1.0-beta.1`目录，运行`./mcl`
正常情况，bot收到消息后，控制台会看的到就成功了
   
> 注： 推荐使用docker的方式，不只是本地，部署到云环境也方便

### 二、运行

初始化及测试
```shell script
npm install
npm run start:dev
```

### 生产发布

```shell script
npm run build
```

> pm2管理（推荐）
```shell script
## 启动
pm2 start dist/main.js --name bridge
## 停止
pm2 stop bridge
## 重启
pm2 restart bridge
## 查看
pm2 ls
```

> node 直接运行
```shell script
node dist/main.js
```


### 声明
> 本项目基于 @rabbitkiller-dev 的互通桥改编

> 原项目链接：https://github.com/rabbitkiller-dev/discord-qq-bridge