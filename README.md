## SxSSHManager
SSH连接管理工具


## 前置
需要安装 expect 

## 下载
直接下载或git下来
```
git clone https://github.com/seeruo/SxSshManager.git
```

## 配置
#### 配置文件
配置文件在`./config-ssh/config.lst`,按照配置示例配置即可
```
序号|    主机IP地址    | 端口 | 账户 | 密码/证书名字 | 说明
----|------------------|------|----|--------|---------------------
101|192.168.200.101|22|root|password|密码连接[配置示例]
102|192.168.200.102|22|root|keys.pem|证书连接[配置示例]
```
#### 密码连接
密码连接直接配置密码即可

#### 证书连接
证书连接配置证书的名字
**证书存放位置统一放在`./config-ssh/keys/`文件夹下面**


## 使用
在根目录下执行
```
./ssh
```

输出格式如下:
```
####################################################
**************** SSH连接管理工具 *******************
####################################################
----------------------------------------------------
序号|    主机IP地址    | 端口 | 说明
----|------------------|------|---------------------
 101|   192.168.200.101|    22|密码连接[配置示例]
 102|   192.168.200.102|    22|证书连接[配置示例]
----|------------------|------|---------------------
 201|   192.168.200.201|    22|开发服务器1
 202|   192.168.200.202|    22|开发服务器2
----------------------------------------------------
[*] 选择主机: 
```
#### 连接
如果想要连接`192.168.200.101`，直接输入`101`回车即可连接

#### 退出
退出主机连接
```
# exit
```
退出管理工具
`q`,`quit`,`command+c`

