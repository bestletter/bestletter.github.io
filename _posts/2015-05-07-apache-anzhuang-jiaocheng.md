---
layout: post
title: Apache安装教程
---

虽然easyphp已经够用，但为了体验一下Apache还是重新安装了一遍，也遇到些问题，记录在这里（我是windows64位系统）。

 1. 下载[Apache](http://www.apachehaus.com/cgi-bin/download.plx)地址：`http://www.apachehaus.com/cgi-bin/download.plx`
 2. 下载后解压，将文件包放到喜欢的存储盘（这里以D盘为例，位置：D:\Apache24）；
 3. 修改环境变量：我的电脑 > 属性 > 高级系统设置 > 环境变量 > 修改path > 加上D:\Apache24\bin。如图：
 <br>
<center><img src="http://i.imgur.com/BzvNAE3.png"/></center>
 <br>
 4. 修改httpd.conf文件（D:\Apache24\conf）：用编辑器打开httpd.conf，找到`Define SRVROOT "/Apache24"和ServerRoot "${SRVROOT}"`，修改为：`Define SRVROOT "D:\Apache24"和ServerRoot "D:\Apache24"`，保存。
 5. 运行命令`httpd.exe`，检测是否安装成功：在浏览器中访问http://localhost，看是否出现测试界面。
 6. 安装服务运行命令`httpd -k install`，成功后就可以啦。
 7. 其他命令：

    Stop Apache	 	        httpd -k stop
    Restart Apache	                httpd -k restart
    Uninstall Apache Service	httpd -k uninstall
    Test Config Syntax	        httpd -t
    Version Details	                httpd -V
   Command Line Options List	httpd -h

 8. 最后可以通过`ApacheMonitor.exe`（D:\Apache24\bin）进行管理。
<center> <img src="http://i.imgur.com/uuoEByz.png"/></center>
