# 为Firefox添加Flash

火狐浏览器没有内置Flash，所以无法观看视频或是正常访问一些使用Flash网站。

1，到[https://get.adobe.com/cn/flashplayer/](https://get.adobe.com/cn/flashplayer/) 下载yum版本的flash，也可直接下载
```bash
wget http://linuxdownload.adobe.com/adobe-release/adobe-release-x86_64-1.0-1.noarch.rpm
```

2，使用命令安装
```bash
sudo rpm -ivh adobe-release-x86_64-1.0-1.noarch.rpm
```

3，在*/etc/yum.repos.d*目录下会出现一个flash的源文件

4，刷新缓存，安装flash
```bash
sudo dnf makecache
sudo dnf install flash-plugin
```

