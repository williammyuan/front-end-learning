### 一、工欲善其事必先利其器（二）

#### 1、命令行

​	编程就会遇到命令行，也不要害怕，现在介绍的都是简单的命令，更加深入的后续再讲再学习，现在只需要记住一些简单到不能再简单的命令（这里主要是针对window下面的命令行）。

​	**win7下调出命令行：**

​		左下角，单击开始，在搜索和程序文件中 输入 cmd，选择cmd.exe单击打开就可以看到黑框。

​	**win10下调出命令行：**

​		右下角 右击开始，打开运行，输入【cmd】，回车即可看到黑框。

​	**可选操作：**

​	window下的dos界面比较丑，推荐一个神器，[cmder](https://www.jeffjade.com/2016/01/13/2016-01-13-windows-software-cmder/)，这里可以有详细的教程，把 **cmder** 加到环境变量这一步可能有问题，这一步有问题，可以随时联系我来解决。

####2、nodejs的安装

​	在day1中提到的写代码的工具，一开始是不推荐直接安装各种软件来进行开发，一来没有编程基础，安装各种ide会很容易迷惑，也会有知识太多，感觉一下学习不完的慌乱感。所以综合考虑，先用runjs来编码，但是，最后真正工作生活还是会在ide上进行开发的，所以今天主要介绍两个工具的使用。

​	**这里安装nodejs只要是使用npm，nodejs后面会有介绍，不着急。**

##### 	2.1npm是什么？

​		官方有[定义](https://www.npmjs.com.cn/getting-started/what-is-npm/)

​		人话版：npm为我们提供了web开发过程中所需要的工具集合，类比一个仓库。我需要的各种东西可以从仓库里获取，我也可以分享自己的工具到仓库里供其他人使用。

##### 	2.2 安装nodejs

​		1、打开[nodejs中国网站](https://nodejs.org/zh-cn/download/)，下载对应版本后正常安装即可，一路next即可，现在window下已经默认将nodejs添加到路径中，不需要操心太多。

​		2、安装完成后，打开命令行，

​		输入

```shell
node -v
```

​		即可看到版本号，

​		输入

```
npm -v
```

​		即可看到npm的版本号，表示npm安装成功，如果看不到，请及时联系我解决问题。

##### 2.3 安装cnpm

​	npm因为国内有墙的原因，导致很多包安装很慢，或者安装失败，这里推荐使用cnpm来代替，cnpm安装也很简单，只要在npm的基础上使用以下命令即可完成：

```shell
 npm install -g cnpm --registry=https://registry.npm.taobao.org
```

​	安装完成后，以后安装包只需要使用即可安装：

```shell
cnpm install [name]
```

3、**安装第一个实用工具browsersync**

​	该工具主要完成以下功能：在用软件写代码过程中，当你保存之后，会自动刷新浏览器，写的代码会立刻在浏览器中显示出来，避免手动刷新浏览器，耗费更多时间。

​	安装过程参考[官网](http://www.browsersync.cn/#install)，从第2步中开始安装，以为2.2中已经安装了nodejs，安装完成后使用：

​	比如我的代码在如下路径：

​	D:\web\index.html

​	那么正确的操作是，打开命令行，输入

```powershell
cd d:\web
d:
browser-sync start --server --files "*.*"
```

​	之后，浏览器会自动打开网址，即可看到代码的效果，如果没有看到效果，注意按如下排查：

​	1、路径是否正确

​	2、文件名是不是index.html，如果不是需要在url中自动补充文件名，比如文件名是test.html，那么在浏览器中打开类似于：localhost:3000/test.html

#### 4、今天任务

​	4.1 正确安装nodejs，npm，cnpm，正确拿到node和npm、cnpm的版本号

​	4.2 正确安装browser-sync，并正确使用

#### 5、拓展知识

​	5.1 [环境变量](https://www.cnblogs.com/itren/p/3677838.html)​