<h1 id="ju3pu">零. 前期环境准备</h1>
<h2 id="N77Og">制作系统盘</h2>
硬件需要一个u盘和一台电脑，软件需要Ventoy（<font style="color:rgb(51, 51, 51);">制作启动 U 盘的开源工具</font>）和所要制作的Ubuntu版本镜像（镜像下载地址）：

[Ubuntu 22.04.5 LTS (Jammy Jellyfish)](https://releases.ubuntu.com/jammy/) 统一下载22.04的版本

_注意事项：_

+ _如果发现自己制作的启动盘，在BIOS界面不显示，可能是自己U盘的问题，如果要购买U盘，提前问好商家是否可以制作启动盘。_
+ _制作系统盘时会将U盘格式化，所以要提前将U盘中的文件备份或者干脆使用一个新U盘。_
+ _U盘复写结束之前不能将U盘拔出，否则可能会造成U盘内的数据损坏。_
+ _注意镜像文件的大小不要超过U盘的内存空间，最好预留出足够的空间以供日后使用，最好16G或者32G，看自己选择。  
_![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763479468363-ff6f65ae-d3cf-4af9-af3a-a8c99bae5729.png)

<font style="color:rgb(51, 51, 51);">Ventoy是一个制作启动 U 盘的开源工具，相比于软碟通来说使用Ventoy你的U盘不在局限于某个PE系统,你只需要把 ISO/IMG/EFI 等类型的文件拷贝到U盘里面就可以启动了，无需其他操作。你可以一次性拷贝很多个不同类型的镜像文件，Ventoy 会在启动时显示一个菜单来供你进行选择。</font>

<font style="color:rgb(51, 51, 51);">Ventoy工具下载地址：</font>[Ventoy download](https://www.ventoy.net/cn/)

github仓库指路：[A new bootable USB solution.](https://github.com/ventoy/Ventoy)

    1. <font style="color:rgb(51, 51, 51);">双击运行Ventoy2Disk，开始制作U盘</font>_<font style="color:rgb(51, 51, 51);">（注：当你制作成功后，你的U盘名称会变成Ventoy）</font>_![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763515731606-b453d5b3-5597-472a-ac6e-43ffef860ebc.png)![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763515743139-97b9d709-4af8-4932-a24e-a19c88d1615a.png)![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763515747961-a5fb44e7-a3f3-41b8-aba7-27ab8c89f8ae.png)
    2. <font style="color:rgb(51, 51, 51);">将系统镜像拷贝到U盘中并安装系统，系统盘制作完成</font>_<font style="color:rgb(51, 51, 51);">（注：</font>__<font style="color:rgba(0, 0, 0, 0.75);">ISO 文件最好保存在U盘根目录下</font>__<font style="color:rgb(51, 51, 51);">）</font>_![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763515754861-04d2fc31-cd11-4ae7-a958-1ce53754f80b.png)

<font style="color:rgb(51, 51, 51);">使用效果：将U盘插入服务器将启动项改成U盘启动，你就会发现出现如下界面，此时我们就可以正常安装系统</font>_<font style="color:rgb(51, 51, 51);">（注：你也可以在U盘里面同时放多个操作系统）</font>_![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763515778738-6a5e7945-8e1d-46d5-9527-da26b3337a51.png)![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763515785546-0518c9ee-64e8-4f36-be8e-c84ba6744bdb.png)

<h2 id="cSX5i">安装双系统</h2>
_建议结合该教学视频观看: _[_如何安装和卸载Windows和Ubuntu双系统_](https://b23.tv/aGB9J9I)

1. 关闭自己电脑上的设备加密和BitLocker加密，这个过程可能会花点时间，两分钟到两三个小时不等，请耐心等待![](https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763481004243-3c6c19a5-3513-4ecb-9b8e-4107bb41bf39.jpeg)
2. <font style="color:rgb(51, 51, 51);">预留磁盘空间给Ubuntu,第一次装都装300G,后期重装自己看情况给（1GB = 1024MB，可以简化为1000来计算）</font>

<font style="color:rgb(51, 51, 51);">点击磁盘管理,选择一个内存富裕的分区 ，右击 ->“压缩卷,要注意内存在磁盘上需要是连续的，即最好只从一个盘腾地方,压缩完成之后，在你选择压缩的分区上的图形化显示会出现灰色条，即证明成功</font>

![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763480634992-15806475-187c-4bf7-a83c-b5bc9e698c9f.png)

![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763481210220-79c298d8-bf69-410e-b1b1-f08f15450c02.png)

4. 修改BIOS设置，每个品牌的电脑BIOS界面有所不同，进入BIOS的方式也不同，自己去搜
    1. <font style="color:rgb(51, 51, 51);">禁用电脑的安全引导项 依次选择 Security -> security boot -> disable</font>
    2. <font style="color:rgb(51, 51, 51);">开启U盘启动，保存设置并重启</font>
    3. <font style="color:rgb(51, 51, 51);">插上做好的系统盘后重启，再次进入BIOS界面</font>
    4. <font style="color:rgb(51, 51, 51);">在启动项中将U盘启动调整至第一位，保存设置并重启</font>
    5. <font style="color:rgb(51, 51, 51);">如果上述步骤操作成功则会进入ventoy的选择界面</font>

<details class="lake-collapse"><summary id="u8b4856ab"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">5. 安装Ubuntu</span></summary><ol class="ne-list-wrap"><ol ne-level="1" class="ne-ol"><li id="u22c0edc1" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">语言选择 English,后点击Install Ubuntu</span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763603689720-1b9c740f-4696-495b-bce4-891a71c3a8fa.jpeg" width="853.3333333333334" id="u76240a2d" class="ne-image"></li><li id="u2b113de0" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">键盘布局选择Chinese不变</span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763603719970-4bbcf590-f3f2-4b71-aca1-510660d9da25.jpeg" width="853.3333333333334" id="ub3a627da" class="ne-image"></li><li id="ubcf5ecb9" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">连接wifi（十分必要）</span></li><li id="u1ff81a9f" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">选择最小安装、安装时不更新、安装无线模块及第三方库</span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763603734151-89ffdc7b-5ae9-4aff-827a-872b57255e70.jpeg" width="853.3333333333334" id="u7241a162" class="ne-image"></li><li id="u208308f1" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">选择Something else自己分区,之后继续点Continue</span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763603744298-8ec3c462-0f19-4c3d-81d8-32cb6162f8bd.jpeg" width="853.3333333333334" id="u21d3bff1" class="ne-image"></li><li id="u176a7548" data-lake-index-type="0" style="text-align: left"><span class="ne-text">磁盘分区选中提前空出来的free space</span></li></ol></ol><ol class="ne-list-wrap"><ol class="ne-list-wrap"><ol ne-level="2" class="ne-ol"><li id="u8a758ec0" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">/boot 2G<br /></span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763603812242-aa028057-b5d6-46f7-98f8-e7cf8792e05f.jpeg" width="853.3333333333334" id="u23fb01e1" class="ne-image"></li><li id="u828b2173" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">/swap 2G （图中为16G，根据自己的情况，比如内存16G 那么swap设置8G或16G；若你为32G，那么swap设置为2G）</span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/62863898/1763731947964-2918a369-62e1-490d-a991-e755eae7f8b9.jpeg" width="1280" id="u1cb2713f" class="ne-image"></li><li id="u774d61eb" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">/home &gt;= 200G （图中为200G，根据自己情况， /home目录和/根目录中给 /home多分一些，这就好比Windows中你的D盘和C盘）</span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763603839075-5ddfa6a2-0d5b-4fb5-86a3-a041ae83e1e6.jpeg" width="853.3333333333334" id="u42af5da0" class="ne-image"></li><li id="ud0ada924" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">/ &gt;= 100G （图中为100G，根据自己情况）</span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763603911817-914f92f5-0f5e-4f81-95c5-7b2055dd5b26.jpeg" width="853.3333333333334" id="ub5b9daef" class="ne-image"></li></ol></ol></ol><ol class="ne-list-wrap"><ol start="7" ne-level="1" class="ne-ol"><li id="u6c62c870" data-lake-index-type="0" style="text-align: left"><span class="ne-text">分区完成，进行后续操作</span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763604119063-02ac2e96-fe3d-4683-8c66-0ed6c7e1c90a.jpeg" width="853.3333333333334" id="u1382c2eb" class="ne-image"><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763604113222-ef977057-c644-4e54-b4c6-6676078295f1.jpeg" width="853.3333333333334" id="u2140c09d" class="ne-image"></li><li id="ue7cc8fdf" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">设置名称密码 名称（这个都要简短，可以使用自己姓名首字母小写） </span><span class="ne-text" style="color: rgb(51, 51, 51); background-color: #F297CC; font-size: 16px">密码统一设置为aaa </span><img src="https://cdn.nlark.com/yuque/0/2025/jpeg/60941281/1763604129736-35738e4a-3446-41a1-bb44-d920b7e24b9d.jpeg" width="853.3333333333334" id="K9ulj" class="ne-image"></li><li id="u2e59bc98" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(51, 51, 51); font-size: 16px">安装完成后等待重启，耐心等待提示（自己翻译：拔掉U盘后按enter键）</span></li></ol></ol></details>
6. 开机后进入选择界面，选择第一个进入Ubuntu
7. <font style="color:rgb(51, 51, 51);">连接Wifi</font>![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763548414576-94fd39f7-fcdf-43cc-af2b-cdd5b6e4a58a.png)
8. <font style="color:rgb(51, 51, 51);">系统换源，点击软件与更新，“下载自： ” 选择其他， 选择阿里源,关闭后会出现重新载入,重新载入即可(这里也推荐小鱼ros一键换源 </font>[小鱼一键安装系列](https://fishros.org.cn/forum/topic/20/%E5%B0%8F%E9%B1%BC%E7%9A%84%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E7%B3%BB%E5%88%97)<font style="color:rgb(51, 51, 51);">)</font>![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763548584072-a1a7c4e9-6ca4-42ab-9593-7dc2551afd54.png)![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763550145960-32e1ccb3-0505-4d51-af13-108366196da8.png)![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763550192584-47f52d70-cd2f-47a7-9593-4619aedffb48.png)
9. 进入语言支持安装完整的语言支持![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763550344800-127e6b69-d0d4-47d1-8c75-5e6e14e0d78b.png)![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763550362895-ec18d995-5b9a-40ce-aec5-2b00c1b35e65.png)
10. <font style="color:rgb(51, 51, 51);">再次进入后，打开设置切换语言为中文,换完会提示你登出，登出就行</font>![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763550623086-36382a00-41c4-409b-8e4b-c2f5a36f1a9b.png)
11. <font style="color:rgb(51, 51, 51);">重新登入后</font>_**<font style="color:rgb(51, 51, 51);">保留英文目录名</font>**_<font style="color:rgb(51, 51, 51);"> keep old names，并点击不要再次询问我</font>![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763550668225-36e0199d-8720-4fed-9663-b7ed2a155f0b.png)

<h1 id="1871937f"><font style="color:rgb(51, 51, 51);">一. 主要流程概述</font></h1>
<font style="color:rgb(51, 51, 51);">-> 搜狗拼音 -> 双系统时间同步 -> typora -> 星火(非必要, 但推荐)</font>

<h1 id="AWzoe"><font style="color:rgb(51, 51, 51);">二. 搜狗安装</font></h1>
<font style="color:rgb(51, 51, 51);">官网：</font>[https://pinyin.sogou.com/linux?r=pinyin](https://pinyin.sogou.com/linux?r=pinyin)

<font style="color:rgb(51, 51, 51);">官方教程: </font>[https://shurufa.sogou.com/linux/guide](https://shurufa.sogou.com/linux/guide)

<font style="color:rgb(51, 51, 51);">下载x86_64     ubuntu22.04系统也适用</font>

~~_**在?为什么给了网址还要抄一遍???**_~~

```bash
sudo apt update #更新源
sudo apt 
sudo apt install fcitx
# 语言支持->选择fcitx
sudo cp /usr/share/applications/fcitx.desktop /etc/xdg/autostart/  # 开机自启动
sudo apt purge ibus  # 卸载ibus框架
sudo dpkg -i 安装包名  # 安装
# 安装依赖
sudo apt install libqt5qml5 libqt5quick5 libqt5quickwidgets5 qml-module-qtquick2
sudo apt install libgsettings-qt1
# 重启电脑
reboot
```

<h1 id="35428765"><font style="color:rgb(51, 51, 51);">三. 双系统时间同步问题</font></h1>
```bash
sudo apt install ntpdate
sudo ntpdate time.windows.com
sudo hwclock --localtime --systohc
```

<h1 id="aNBW7">四.Typora安装</h1>
```bash
# add Typora's key
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://typoraio.cn/linux/typora.gpg | sudo tee /etc/apt/keyrings/typora.gpg > /dev/null
# add Typora's repository securely
echo "deb [signed-by=/etc/apt/keyrings/typora.gpg] https://typoraio.cn/linux ./" | sudo tee /etc/apt/sources.list.d/typora.list
sudo apt update
# install typora
sudo apt install typora
```

<h1 id="4816a0a9"><font style="color:rgb(51, 51, 51);">五.星火应用商店安装</font></h1>
星火应用商店官网：[星火应用商店](https://www.spark-app.store/download)

选择对应的计算机架构一般都是intel/AMD架构也就是amd64，少部分人可能是ARM，不明白这是什么意思的可以自己先上网查一下做一下区分

<font style="color:rgb(51, 51, 51);">在星火安装QQ和微信以及其他软件时可以和windows平台一样便捷,主要用来安装QQ和微信等(方便文件传输),但不要依赖,学会命令行操作是基本技能</font>

<font style="color:rgb(51, 51, 51);">下载下来安装包后进入解压即可</font>

```bash
cd ~/Downloads
sudo apt install ./spark-store-*.deb
```

<h1 id="ZHfIm">六.VSCode安装及环境配置</h1>
与过渡阶段的WSL+VSCode的配置大体相同，可参考往期视频

[WSL+VSCode.mp4](https://www.yuque.com/attachments/yuque/0/2025/mp4/60941281/1763960120203-9c6478c2-fe3b-4b4c-89e7-16b29b4a7a3f.mp4)



