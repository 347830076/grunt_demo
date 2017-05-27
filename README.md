npm常用指令

1、npm install moduleNames：安装Node模块

安装完毕后会产生一个node_modules目录，其目录下就是安装的各个node模块。

node的安装分为全局模式和本地模式。

一般情况下会以本地模式运行，包会被安装到和你的应用程序代码的本地node_modules目录下。

在全局模式下，Node包会被安装到Node的安装目录下的node_modules下。

全局安装命令为$npm install -g moduleName。

获知使用$npm set global=true来设定安装模式，$npm get global可以查看当前使用的安装模式。

示例：
npm install express 

默认会安装express的最新版本，也可以通过在后面加版本号的方式安装指定版本，如npm install express@3.0.6
npm install <name> -g 

将包安装到全局环境中
但是代码中，直接通过require()的方式是没有办法调用全局安装的包的。全局的安装是供命令行使用的，就好像全局安装了vmarket后，就可以在命令行中直接运行vm命令

npm install <name> --save 

安装的同时，将信息写入package.json中项目路径中如果有package.json文件时，直接使用npm install方法就可以根据dependencies配置安装所有的依赖包，这样代码提交

到github时，就不用提交node_modules这个文件夹了。
2、npm view moduleNames：查看node模块的package.json文件夹

注意事项：如果想要查看package.json文件夹下某个标签的内容，可以使用$npm view moduleName labelName
3、npm list：查看当前目录下已安装的node包

注意事项：Node模块搜索是从代码执行的当前目录开始的，搜索结果取决于当前使用的目录中的node_modules下的内容。$ npm list parseable=true可以目录的形式来展现

当前安装的所有node包

4、npm help：查看帮助命令

5、npm view moudleName dependencies：查看包的依赖关系

6、npm view moduleName repository.url：查看包的源文件地址

7、npm view moduleName engines：查看包所依赖的Node的版本

8、npm help folders：查看npm使用的所有文件夹

9、npm rebuild moduleName：用于更改包内容后进行重建

10、npm outdated：检查包是否已经过时，此命令会列出所有已经过时的包，可以及时进行包的更新

11、npm update moduleName：更新node模块

12、npm uninstall moudleName：卸载node模块

13、一个npm包是包含了package.json的文件夹，package.json描述了这个文件夹的结构。访问npm的json文件夹的方法如下：

$ npm help json 

此命令会以默认的方式打开一个网页，如果更改了默认打开程序则可能不会以网页的形式打开。

14、发布一个npm包的时候，需要检验某个包名是否已存在

$ npm search packageName

15、npm init：会引导你创建一个package.json文件，包括名称、版本、作者这些信息等

16、npm root：查看当前包的安装路径

npm root -g：查看全局的包的安装路径

17、npm -v：查看npm安装的版本

18、npm list --depth=0：查看所有高级的npm moudles

19、npm list --depth=0 -global：查看所有全局安装的模块
选装cnpm

1、说明：因为npm安装插件是从国外服务器下载，受网络影响大，可能出现异常，如果npm的服务器在中国就好了，所以我们乐于分享的淘宝团队干了这事。！来自官

网：“这是一个完整 npmjs.org 镜像，你可以用此代替官方版本(只读)，同步频率目前为 10分钟 一次以保证尽量与官方服务同步。”；
2、官方网址：http://npm.taobao.org；

3、安装：命令提示符执行npm install cnpm -g --registry=https://registry.npm.taobao.org；  注意：安装完后最好查看其版本号cnpm -v或关闭命令提示符重新打开，安装完直

接使用有可能会出现错误；
注：cnpm跟npm用法完全一致，只是在执行命令时将npm改为cnpm（以下操作将以cnpm代替npm）。

1、说明：因为npm安装插件是从国外服务器下载，受网络影响大，可能出现异常，如果npm的服务器在中国就好了，所以我们乐于分享的淘宝团队干了这事。！来自官

网：“这是一个完整 npmjs.org 镜像，你可以用此代替官方版本(只读)，同步频率目前为 10分钟 一次以保证尽量与官方服务同步。”；

2、官方网址：http://npm.taobao.org；

3、安装：命令提示符执行npm install cnpm -g --registry=https://registry.npm.taobao.org；  注意：安装完后最好查看其版本号cnpm -v或关闭命令提示符重新打开，安

装完直接使用有可能会出现错误；

注：cnpm跟npm用法完全一致，只是在执行命令时将npm改为cnpm（以下操作将以cnpm代替npm）。