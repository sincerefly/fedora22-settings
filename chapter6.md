# 安装VirtualBox

*此部分根据个人需要阅读*
*Vbox可以安装个Windows来应急，也可以安装Fedora来做实验，或者是其它发行版折腾*

1， 安装过rpmfusion源后，在Fedora 22下直接就可以安装VirtualBox
```bash
sudo dnf install VirtualBox
```

2，先更新下系统先
```bash
sudo dnf update
```

3，现在打开虚拟机，加载镜像，配置完成，点击启动，是不能运行的，很多工具都没有安装，需要自己安装。

```bash
sudo dnf groupinstall "Development Tools"
sudo dnf install gcc-c++
sudo dnf install kernel-modules-extra
sudo dnf install kernel-devel kernel-headers
```

4，安装 *kmod-VirtualBox*

```bash
sudo dnf install kmod-VirtualBox
```

但是在这里我没有安装成功。

```html
错误：nothing provides kernel-uname-r = 4.0.2-300.fc22.x86_64 needed by kmod-VirtualBox-4.0.2-300.fc22.x86_64-4.3.28-1.fc22.x86_64
```
如果报错，那就安装个 *akmod-VirtualBox* 吧，它是用来生成kmod-VirtualBox的

```bash
sudo dnf install akmod-VirtualBox
```

之后运行
```bash
sudo akmods --force
```

重启系统后VBox就可以正常运行了。

---

如果还是有些问题，那么运行如下命令试试。
```bash
/etc/init.d/vboxdrv setup
```
如果没有报错。重启后就应该正常了，如果还有问题，那就Google吧，祝你好运～



