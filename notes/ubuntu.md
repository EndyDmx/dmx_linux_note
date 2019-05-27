## ubuntu18.04.1 开机默认进入命令行模式/用户图形界面
``` 
一、开机默认进入命令行模式
 1、输入命令：
    sudo systemctl set-default multi-user.target 
 2、重启：
    reboot
 要进入图形界面，只需要输入命令
    startx
 从图形界面切换回命令行：
    ctrl+alt+F7    
二、开机默认进入图形用户界面
 1、输入命令：
    sudo systemctl set-default graphical.target 
 2、重启：
    reboot
要进入命令行模式：
    ctrl+alt+F2
从命令行切换到图形界面：
    ctrl+alt+F7
```
## 解决Ubuntu中vi命令的编辑模式下不能正常使用方向键和退格键的问题
```
在Ubuntu中，进入vi命令的编辑模式，发现按方向键不能移动光标，而是会输出ABCD，以及退格键也不能正常删除字符。
这是由于Ubuntu预装的是vim-tiny，而我们需要使用vim-full，解决方法很简单，只需要以下两步： 
    步骤一，输入下述命令以卸载vim-tiny：
        sudo apt-get remove vim-common
    步骤二，输入下述命令以安装vim-full：
        sudo apt-get install vim
```
## 分辨率设置
```
在开机启动时，先不进入系统，长按shift，进入boot选项，按“c”进入grub命令行
使用命令vbeinfo查看当前支持的分辨率
使用命令reboot重启；

打开：/etc/default/grub
搜索：#GRUB_GFXMODE=640x480
编辑：640x480改成你想要的分辨率，并取消前面的#
例如：GRUB_GFXMODE=1024x768x32 
更新：sudo update-grub
重启 

```
