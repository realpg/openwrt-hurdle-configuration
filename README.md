# openwrt-hurdle-configuration
### 跨栏飞人刘翔的openwrt配置方案
   
----
  
  一种无须建立服务器的跨栏高手openwrt配置方案，可额外修改基本配置用于更多已开启HSTS的网站。幸运的是，主流的跨栏高手的国际比赛地,比如google, github, youtube, facebook, twitter, tumblr, instagram, openwrt.org, composer, packagist, 均已加入HSTS。

**感谢某HKT的劫持缓存系统提供根本保障。**

----
**Requirements:**

* 一个安装了openwrt的路由器硬件，推荐采用近年主流的MTK 762x CPU + 128M RAM + 16M ROM的硬件
* 软件包 nginx
* 软件包 dnsmasq(默认编译包含)
* 软件包 iptables(默认编译包含)

**备注：由于NGINX编译后的软件包文件并不是很小，低于8M ROM的机型可能无法让nginx和图形界面管理LuCI共存；且NGINX启动需要的RAM也应该充分考虑，在低于64M RAM的设备上可能无法良好运行**

**Tested devices:**

* 极路由1S(旧) HC5661 (MT7620 128M 16M)
* 小米路由器mini (MT7620 128M 16M)
* TPLINK WR703n (Hacked 16M ROM + 64M RAM)
* 小米路由青春版 （MT7628n 64M 16M)
* Linksys WRT1900ACS v1 (Marvell ARM + 512M +128M)

**How-tos:** 

由于路由器上大多没有git，直接clone到本机，然后将配置文件拷贝到路由器即可。
所有配置文件均可根据自己需要进行调整。


