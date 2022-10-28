# 知识学杂了!

## linux

#### linux 查看当前时间和时区

```linux
date -R
```

#### 查询当前服务器外网ip

```linux
clush -w crawler[001-060] 'curl -L ip.tool.lu'
```

#### 安装chromedriver

```linux
使用命令将解压后的文件复制到   /usr/local/bin/chromedriver
命令为：sudo mv chromedriver /usr/local/bin/chromedriver
改变用户权限：
命令为：sudo chmod u+x,o+x   /usr/local/bin/chromedriver
```

#### 安装Miniconda3

```linux
下载包后
bash Miniconda3-latest-Linux-x86_64.sh
一路enter yes

创建环境
 conda create -n python3 python=3.6
其中python3为环境名称

激活环境
source activate python3
```

#### 安装chrome

```linux
yum install -y google-chrome-stable_current_x86_64_94.0.4606.81.rpm
一路回车
```

#### 安装node

```linux
https://blog.csdn.net/lh155136/article/details/111194424

tar -xvf node-v16.14.2-linux-x64.tar.xz 解压缩

mv /usr/local/node-v14.15.1-linux-x64 /usr/local/node 更改名称

vi /etc/profile 更改环境变量
export PATH=$PATH:/usr/local/node/bin 最后一行加上

source /etc/profile 加载环境变量
```

#### 安装go

```
下载压缩包地址：https://studygolang.com/dl
https://studygolang.com/dl/golang/go1.15.6.linux-amd64.tar.gz

上传至 /usr/local/src 路径下
解压缩  tar -C /usr/local/src -xzf go1.15.6.linux-amd64.tar.gz 

配置环境变量：
修改/etc/profile   
添加以下内容  
export PATH=$PATH:/usr/local/src/go/bin


source /etc/profile

go version 校验命令
```



#### 导入中文字体

```linux
mkdir -p /usr/share/fonts/chinese/        #创建中文字体目录

cp songti.ttf /usr/share/fonts/chinese/     #将字体文件拷贝
到/usr/share/fonts/chinese/中

cd /usr/share/fonts/chinese/

fc-cache -fv                              #为刚加入的字体设置缓存使之有效

fc-list                                   #查看系统中的字体
```

#### 修改用户密码

```linux
chage -M 99999 neusoft # 将用户密码设置为永久不过期
chage -l root  # 查看用户密码状态
```

#### curl

```linux
curl --proxy "代理" "url"
```

#### ssh 远程免密登录

```
1.在Server1输入：ssh-keygen (三次提示都按回车即可)  --生成密钥
2.在Server1输入：ssh-copy-id Server2的ip  --将密钥拷贝到要配置的服务器上
3.配置完成，在Server1输入：ssh Server2的ip ，即可完成免密登录。

常见问题:REMOTE HOST IDENTIFICATION HAS CHANGED!
ssh-keygen -R 接收方ip
```

#### zasbbix-agent安装

```
1.rpm -Uvh https://repo.zabbix.com/zabbix/5.0/rhel/7/x86_64/zabbix-release-5.0-1.el7.noarch.rpm   #换源 不同源配置文件不同
2.yum clean all #清理yum源
3.yum install zabbix-agent
4.修改/etc/zabbix/zabbix_agentd.conf
5.systemctl restart zabbix-agent #启动
6.systemctl enable zabbix-agent
```

#### 关机

```
shutdown -h now
```

#### 更改主机名

```
修改/etc/hostname
sudo hostname <新主机名>
```





## Redis

#### redis 切换db

```
SELECT 2 
切换到db2
```

#### redis 获取键的具体值

```
GET ahhuali.com
```





## Python

#### 字符串截取

```python
str = '12345678'
print str[0:1]  # 注意是:不是,
>> 1			# 输出str位置0开始到位置1以前的字符
```

#### 字符串删除空格

```python
a.strip()
```

#### 字符串转byte

```python
s = "abc"             # string
s = "abc".encode()    # bytes，encode默认编码方式是utf-8
s = b"abc"            # bytes
```

#### python 批量安装所需依赖 

```linux
pip install pipreqs #安装依赖
pipreqs .   # 生成依赖清单 
pip install -r requirements.txt
```





## bug解决

#### selenium.common.exceptions.WebDriverException: Message: ‘chromedriver‘解决

找到对应本地浏览器的chromedriver 放置到python根目录下就行了

#### pip安装依赖时 出现无法卸载

pip -V 找到base环境的文件夹site-packages的绝对路径

删除无法删除的依赖

rm -rf ruamel*

重新安装

## 各种安装包

#### typora-windows

https://wws.lanzouj.com/iGkwhk5vpyf