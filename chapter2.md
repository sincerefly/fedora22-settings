# 添加rpmfusion源

rpmfusion是Fedora的第三方源，其中包括大量的软件，在之后的章节，我们安装的播放器解码器就是它提供的，安装它是非常有必要的。。

在终端运行
```bash
su -c 'dnf install --nogpgcheck http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm http://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm'
```

如果你的Fedora版本<22，那么使用下面条命令安装
```bash
su -c 'yum localinstall --nogpgcheck http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm http://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm'
```

安装完成后我们使用如下命令建立缓存：

```bash
sudo dnf makecache
```








