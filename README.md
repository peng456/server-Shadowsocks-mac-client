# server_-Shadowsocks-mac_client
在Amazon EC2 Linux实例上安装Shadowsocks服务器,在mac安装客户端

捣鼓了很久终于成功了。Yeah！！！  
前提你得有一台国外服务器。  
亚马逊需要你有信用卡。注册后可以免费一年。（福利还是不错的，但是不要瞎点别的东西。有可能产生费用）

服务器端：  
按照下面的教程是OK的
https://liyang85.com/install-shadowsocks-server-in-aws-ec2-instance  
其中重要的一点：对/etc/shadowsocks.json 配置中 server 的解释。因为网上好多都是错误的。  

还有要配置 网络  入站规则  
在安全组里面。  
需要配置两组规则： TCP、 UDP  

还有一点mac 客户端ShadowsocksX-NG，有bug.  
macos  10.12.5之后不能翻墙。github 有解决方案。如下  
https://github.com/shadowsocks/ShadowsocksX-NG/issues/371  
```
打开终端，先执行
`cd /Applications/ShadowsocksX-NG.app/Contents/Resources`
然后
`chmod +x ss-local`
```
 
有问题 提 issue。
