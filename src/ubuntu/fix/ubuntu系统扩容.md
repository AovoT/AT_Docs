<h2 id="e2CMG">前言</h2>
> ubuntu系统安装后出现磁盘大小不足的问题，想要增加系统可用空间，下面给出两种方案
>

<h2 id="e8uyE">windows操作</h2>
+ Win + x 打开磁盘管理，右击想要压缩卷的分区进行压缩卷
+ 如果无法进行压缩卷，可以以管理员身份运行cmd输入（下面的实例是D盘的）：

```plain
chkdsk D: /f /r
```

+ 完成后重启，就能正常压缩了，选定要压缩的大小，关闭windows

<h2 id="SRCky">Ubuntu IOS 启动Live系统 </h2>
> 使用系统盘启动，选定系统盘后选择镜像，例如：然后进入
>

```plain
ubuntu-22.04.5-desktop-amd64.ios
```

+ 进入后，打开左下角菜单，搜索并打开GParted Partltion Edito

![](https://cdn.nlark.com/yuque/0/2025/jpeg/62837594/1764483662424-3114f7f9-177f-4ce8-92a5-c724717addb2.jpeg)

+ 然后可以看到灰色区域就是待分配区域
+ 通过右击分区->resize/move，通过拖拉进行合并，从而扩大对应分区的内存
+ **重要！！！！启动引导项分区一定不要动（截图里的带！的p5分区），否则就完了！！！**

<h2 id="b993v">如果和截图里一样windows和ubuntu系统分区中间夹着启动引导项</h2>
只能将空内存区建立为ubuntu新的内存分区：

右击选择New,标签Label取个英文名如data，File system选择ext4，然后确认，得到分区如：

```plain
/dev/sdb1  ext4
```

创建挂载目录，将新分区挂载到data(例)

```plain
sudo mkdir -p /data
sudo mount /dev/sdb1 /data
```

给权限

```plain
sudo chown -R $USER:$USER /data
```

上面的操作是例子，真正实操时选择自己起的标签名

