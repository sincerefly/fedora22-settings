# 安装音频视频解码器

*安装解码器需要安装rpmfusion源*

```bash
sudo dnf install gstreamer1-plugins-bad-free-extras gstreamer1-plugins-base-tools gstreamer1-plugins-ugly gstreamer1-plugins-bad-freeworld gstreamer1-libav
```
安装后即可播放MP4等格式的视频。

值得一提的是，Fedora自带的播放器并不强大，甚至比较弱...

我们来安装强大的mplayer，gnome-mplayer是其前端界面。

```bash
sudo dnf install mplayer gnome-mplayer
```
安装完成后，在“**系统**” - “**详细信息**”中修改设置其为默认播放器

---

可能遇到的问题：

`2015-01-31 09:19`

莫名播放视频有画面无声音，最后找到解决方法：

安装totem，然后打开，发现声音上是关闭的。开启声音，再回到gnome mplayer，声音正常
