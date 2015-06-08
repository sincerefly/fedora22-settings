# 修改目录语言

安装Fedora22选择中文环境可能会在使用中方便很多，但是也带来一问题，比如文件夹名称，会是“文档”、“下载”、“音乐”等，这将使得终端下难以访问文件。

解决办法如下：
```bash
export LANG=en_US
xdg-user-dirs-gtk-update
```
软件会询问是否修改目录名，点击“是”。

之后使用命令将环境改中文。
```bash
export LANG=zh_CN
```
重启系统，会再次出界面询问是否变更目录名称，勾选“**不再询问**”并点击“**否**”。

---

如果你在第一次询问的时候勾选了“不再询问”并点击了否或是重启后点击了“不再询问”并“改回中文名”。不要担心，我们还可以再次“激活”*xdg-user-dirs-gtk-update*。

在*~/.conf/* 下有两个文件，*~/.config/user-dirs.dirs* 和 *~/.config/user-dirs.locale*

我们只需要修改后者，使用你熟悉的编辑器打开 *~/.config/user-dirs.locale*

其中保存着“en_US”或是“zh_CN”

我们先看一张表：

user-dirs.dirs|user-dirs.locale|LANG|xdg-user-dirs-gtk-update
---|---|---|---
en|en|en|no
en|zh|en|no
en|en|zh|yes
en|zh|zh|no
zh|en|en|no
zh|en|zh|no
zh|zh|en|yes
zh|zh|zh|no

简单解释下，上表的 *user-dirs.dirs* 为en代表文件中的路径名是英文的，zh为中文。*user-dirs.locale*为en代表着文件中中保存着en_US，反之则为zh_CN，LANG为en代表在终端执行 *export LANG=en_US*，zh则为zh_CN，最后的*xdg-user-dirs-gtk-update*为yes则为可再次激活，no则不可激活。

---

简单来说，要想再次激活你的*xdg-user-dirs-gtk-update*进行设置，首先你需要打开*~/.config/user-dirs.dirs* 文件来查看以下这个文件里存储的目录为英文的还是中文的。然后打开 *~/.config/user-dirs.locale*文件，设置其中的语言，与*~/.config/user-dirs.dirs*中的语言相对应。然后再终端上*export LANG=**这里的语言要与上两个文件中的语言不一样。

再次运行*xdg-user-dirs-gtk-update*，设置界面是不是又出现了呢～












