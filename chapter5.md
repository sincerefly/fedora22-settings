# DNF简单配置

在Fedora 22中，首次默认使用dnf包管理器来代替yum，有一些缺省设置，修改下会更好用。

1，keepcache

编辑 */etc/dnf/dnf.conf* 文件，在行尾添加：
```conf
keepcache = 1
```
这个设置的作用是保持缓存，有些时候安装软件在下载时会卡住。用Ctrl+C结束掉后再次运行发现需要重新下载。开启这个选项就能在上一次的基础上继续下载。(Yum默认是开启的)


---

暂时只需要修改这些，更多 *dnf.conf* 的配置选项可以查阅文档。

```bash
man dnf.conf
```