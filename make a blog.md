# 买服务器

[注册账号](www.vultr.com)	   www.vultr.com 

# 买域名

去阿里云买即可

#影梭                            

[服务器安装shadowsocks](http://zhuangold.com/vultr-vps%E4%B8%BB%E6%9C%BA%E5%BF%AB%E9%80%9F%E5%AE%89%E8%A3%85shadowsocks%EF%BC%88ss%EF%BC%89%E6%95%99%E7%A8%8B/)  

http://zhuangold.com/vultr-vps%E4%B8%BB%E6%9C%BA%E5%BF%AB%E9%80%9F%E5%AE%89%E8%A3%85shadowsocks%EF%BC%88ss%EF%BC%89%E6%95%99%E7%A8%8B/

root用户下执行此命令，安装shadowscoks

```command
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```

若需要卸载shadowscoks

```comammd
./shadowsocks-all.sh uninstall
```

# 登陆防护

用putty进去后对VPS做一下安全防护

新建一个用户test

```command
useradd test
```



修改用户密码，会提示你输入密码和重复输入密码

```command
passwd test
```



禁止root用户用户登录，修改#PermitRootLogin yes为PermitRootLogin no

```command
nano /etc/ssh/sshd_config
```

### 这样只能用test登陆，然后看切换到root;此时别人想暴力破解须知：服务器ip、用户名、用户名密码；





#安装lnmp(官网最详细)

[install lnmp ](https://lnmp.org/install.html)        

https://lnmp.org/install.html

此过程需十几分钟到一小时不等，请耐心

安装时的password of Mysql要自己记住//不输入则默认为root

#安装虚拟主机 (官网最详细)	             

[add host](https://lnmp.org/faq/lnmp-vhost-add-howto.html)           

https://lnmp.org/faq/lnmp-vhost-add-howto.html

安装时的datebase name and password of Mysql要自己记住



#安装wordpress   (官网最详细)    

[add wordpress](https://codex.wordpress.org/zh-cn:%E5%AE%89%E8%A3%85_WordPress)           

https://codex.wordpress.org/zh-cn:%E5%AE%89%E8%A3%85_WordPress



# 常见问题及注意事项



此处注意事项：

1.在home/wwwroot/www.***.cn/里执行下载安装wordpress

2.wordpress安装目录里的文件应移动到www.***cn

3.在wordpress里执行此命令

```command
mv * ../
```




IP或者网址/wp-admin	登录管理员博客



###wordpress 更换主题是会出现FTP问题，看下面教程教程

[WordPress安装主题/插件提示输入FTP账户信息](https://www.joyhwong.com/archives/1459)

https://www.joyhwong.com/archives/1459



1.在你的服务器上Wordpress的安装目录为

```command
/home/wwwroot/wwww.***.com
```

修改网站Wordpress的权限

2.如果提示chmod: changing permissions of ‘/home/wwwroot/joyhowng.com/.user.ini’: Operation not permitted可以忽略

```command
chmod -R 755 /home/wwwroot/www.***.com
```

3.再把网站目录下所有文件的属主改为www

如果提示chown: changing ownership of ‘/home/wwwroot/joyhwong.com/.user.ini’: Operation not permitted可以忽略

```command
chown -R www /home/wwwroot/www.***.com
```



###若提示*******已存在，去服务器把他说的那个文件删了就行







###此处有一链接可供参考整个流程

[教程](https://www.jianshu.com/p/56750622cac9)            https://www.jianshu.com/p/56750622cac9

