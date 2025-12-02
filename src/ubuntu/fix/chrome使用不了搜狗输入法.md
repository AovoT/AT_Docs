<h1 id="h8toy"><font style="color:rgb(51, 51, 51);">前言</font></h1>
<font style="color:rgb(51, 51, 51);">也不知道事由于什么原因，我之前ubuntu用的好好的搜狗输入法，结果不能切换中文了，关键是无法在Chrome浏览器中使用，我仔细测试了一下，比如在vscode编辑器，在文本里面，在firefox浏览器里面都可以，就谷歌浏览器不行。</font>

<h1 id="EzW2y"><font style="color:rgb(51, 51, 51);">解决方法</font></h1>
<h2 id="SGpaj">下载插件</h2>
```bash
sudo apt install fcitx5-frontend-gtk4
```

<h2 id="RbeSj">查看窗口系统</h2>
进入设置如下图所示

![](https://cdn.nlark.com/yuque/0/2025/png/62863898/1763773471494-876b054f-1451-4b93-9167-f96d0a2cf9b5.png)

<h2 id="helhz">更改窗口系统</h2>
有的ubuntu默认的是wayland窗口，需要改为X11



如果你已经进入ubuntu界面，那么先注销ubuntu

![](https://cdn.nlark.com/yuque/0/2025/png/62863898/1763773316171-71047228-301a-4b94-a1a6-84e0aef6c0e3.png)

进入以下界面

更换另外一个选项即可



![](https://cdn.nlark.com/yuque/0/2025/jpeg/62863898/1763775009566-3172f9b0-7693-441d-8b03-34b05cee9aec.jpeg)

