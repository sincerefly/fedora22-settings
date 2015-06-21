# 安装Chrome及插件

下载Chrome：[http://getchrome.sinaapp.com/](http://getchrome.sinaapp.com/)

选择对应的Linux稳定版本

安装方法和其它本地安装方法相同

```bash
sudo dnf install google-chrome-stable_current_x86_64.rpm
```

---

**下面来推荐几个强大插件**

---

（一）Proxy SwitchyOmega + Shadowsocks-QT5

优化出国线路，方便快捷易用，配置方面不多介绍，需要的自行了解，此处只说明软件及插件的安装。

在优化线路之前不能安装插件，但是不安装插件就不能优化线路，真是个矛盾的事情，在网上找到别人的度盘分享，先凑合用吧
下载地址：[http://yun.baidu.com/s/1i3orYsP](http://yun.baidu.com/s/1i3orYsP)

下载后在chrome中访问[chrome://extensions/](chrome://extensions/)
将SwitchyOmega.crx文件拉到界面即可安装

在F22下，你可以直接执行如下命令安装Shadowsocks-QT5：

```bash
sudo dnf copr enable librehat/shadowsocks
sudo dnf makecache
sudo dnf install shadowsocks-qt5
```

其它版本可以参考《Shadowsocks-QT5安装指南》：[https://github.com/librehat/shadowsocks-qt5/安装指南](https://github.com/librehat/shadowsocks-qt5/wiki/%E5%AE%89%E8%A3%85%E6%8C%87%E5%8D%97)

---

（二）uBlock Origin

>一款高效的网络请求屏蔽工具，占用极低的内存和 CPU

也就是传说中的广告屏蔽插件，非常好用，值得尝试

---

（三）惠惠购物助手

>【网易出品】在您网购浏览商品的同时，自动对比其他优质电商同款商品价格，并提供商品价格历史，帮您轻松抄底，聪明网购不吃亏！

如果你喜欢网购，怎么没有这个的帮助呢，看看搞活动的商品是否提前加价

---
（四）百度网盘助手

>可以方便的把百度网盘的下载地址导出到aria2/aria2-rpc，支持YAAW。

在Linux下，度盘没有客户端，然而下载文件如果用浏览器下载，速度是有限制的，使用这个插件，点击一个文件，在网盘“离线下载”一排会出现“导出下载”的按钮，点击“导出下载”，复制里面的命令到终端下，即可下载，速度很快，基本上可以跑满你的带宽，非常推荐


未完，待续...
