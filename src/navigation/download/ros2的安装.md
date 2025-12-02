先阅读蓝链[小鱼一键安装系列](https://fishros.org.cn/forum/topic/20/%E5%B0%8F%E9%B1%BC%E7%9A%84%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E7%B3%BB%E5%88%97)

```shell
wget http://fishros.com/install -O fishros && . fishros
```

wget [http://fishros.com/install](http://fishros.com/install) -O fishros && . fishros

<h1 id="p55fI">安装流程</h1>
大致如下，我直接复制的

<h2 id="Nk4vx"><font style="color:rgb(77, 77, 77);">输入密码</font></h2>
![](https://cdn.nlark.com/yuque/0/2025/png/62863898/1763772077737-046f6510-ed14-4343-b758-4f5dba79898a.png)

<h2 id="Z1ntp"><font style="color:rgb(77, 77, 77);">然后就会看见选择安装界面，我们看界面可以看到小鱼的脚本还可以支持很多工具安装，这里我们选择 1 ROS安装</font></h2>
![](https://cdn.nlark.com/yuque/0/2025/png/62863898/1763772161623-26d52ee7-9271-4707-9230-70881d1fa1c0.png)

<font style="color:rgb(77, 77, 77);">大家可以看到这里会显示出你当前的Linux发行版版本，而且他还支持arm平台（我在jetson nano试过，可以）。</font>**<font style="color:rgb(77, 77, 77);">让你选择是否按照他提供的源进行安装，因为我己经换了源了这里 选择 2，如果没换源可以选 1。</font>**

**<font style="color:rgb(77, 77, 77);">如果你没有换源的话，你跟着他推荐的选项走即可</font>**

![](https://cdn.nlark.com/yuque/0/2025/png/62863898/1763772213761-398f8b3b-d5e2-442e-a5b1-defce25798ee.png)

<font style="color:rgb(77, 77, 77);">这里是</font>**<font style="color:rgb(77, 77, 77);">选择ros镜像源，这里选择1中科大镜像源</font>**

![](https://cdn.nlark.com/yuque/0/2025/png/62863898/1763772334680-acbb7036-95ca-477c-9902-5abc9d94e8ec.png)

<font style="color:rgb(77, 77, 77);">到这里就是</font>**<font style="color:rgb(77, 77, 77);">选择ROS版本 ，这里我选择 1 humble(ROS2)</font>**

![](https://cdn.nlark.com/yuque/0/2025/png/62863898/1763772358197-02bd61a2-edbe-4a05-a6ea-37758c0126b8.png)

Desktop 版 (推荐)包含: ROS, RViz, demos, tutorials。base版仅包含：Communication libraries, message packages, command line tools.。不包含 GUI tools。(新手直接选桌面版) 这里选 1，后面就进行安装了（大概几分钟）

![](https://cdn.nlark.com/yuque/0/2025/png/62863898/1763772390322-1c6d7766-772a-4462-961f-a005f084753c.png)

<font style="color:rgb(77, 77, 77);">显示这个表示ROS2安装完成</font>

![](https://cdn.nlark.com/yuque/0/2025/png/62863898/1763738380360-7a075baa-aef4-4167-939c-5bfd50121d5a.png)

