有很多人在群问Wi-Fi callng 怎么开，首先我不是原创只是资源整合：
首先感谢以下大佬：
V2XP跨境交流，奶爸套利、lopruser、虚拟号、BMC
开通wifi 一般有三种方法：
前提准备
软路由、苹果手机6s以上国行外版都可以最好美版、三星、pixei
一、	修改DNS：
WiFi Calling WiFi通话连不上？动动手指，改成国外DNS即可解决。Ultra Mobile和RedPocket都能正常使用 | 美国手机卡在中国使用：
手机设置DNS：
Norton（我自己的电信网络测试下来觉得这个对于WiFi Calling最好用，很快就能连接，也没有出现过掉线的情况）：
199.85.126.10
199.85.127.10
Google：
8.8.8.8
8.8.4.4
Cloudflare：
1.1.1.1
1.0.0.1
这是最简单的如果可以那不要往下看了！如果会断开就保留一个DNS。
二、	修改软路由域名劫持：
路由器DNS劫持设置
把域名：ss.epdg.epc.mnc260.mcc310.pub.3gppnetwork.org
可以指向：
208.54.148.227
208.54.159.227
208.54.39.35
208.54.2.67
208.54.2.163
208.54.37.195
208.54.36.131
 
三、	open clash 分流规则
后面加上你代理的服务组。
IP-CIDR,66.94.0.0/19
IP-CIDR,206.29.177.36/32
IP-CIDR,208.54.0.0/16
DOMAIN-SUFFIX,t-mobile.com
DOMAIN-SUFFIX,3gppnetwork.org
机场必须要支持udp还有FullCone，
记得你自家的网络要说串联。
![image](https://user-images.githubusercontent.com/96309472/211325572-35a6df5f-5f37-41fb-884d-82e7f39a4e19.png)
