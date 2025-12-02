<h1 id="CS8PR">什么是yaml文件？</h1>
**yaml文件是一种易读的数据序列化格式，可以在****<font style="color:#DF2A3F;">不修改源代码</font>****，****<font style="color:#DF2A3F;">不重新编译的</font>****情况下更改一些配置信息，yaml文件和python文件有一定的相似性，同样通过****<font style="color:#DF2A3F;">缩进</font>****来表示层级关系。**

比如，创建一个camera.yaml文件，内容为：

![](https://cdn.nlark.com/yuque/0/2025/png/58545606/1764329219475-c297455a-5897-47a3-9cf7-9b204ffa8d60.png)

在需要使用相机配置信息的代码中导入信息：

![](https://cdn.nlark.com/yuque/0/2025/png/58545606/1764329280115-1add2e90-4b31-48ba-9845-a0946a7861e5.png)

在需要更改相机配置信息的时候，可以直接修改.yaml文件中的参数，而不需要重新编译。

[更多，有关yaml文件的详细介绍](https://b23.tv/hzQPvY5)



