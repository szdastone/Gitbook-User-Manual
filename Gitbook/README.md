# 命令

这里介绍下gitbook的几个常用命令。

#### 初始化init

gitbook init命令可初始化书籍目录。

在使用这个命令时，首先需要新建立一个目录，然后在这个目录下新增加README.md与SUMMARY.md；如新建目录为book,则该目录结构为：

```
c:\>tree book /f
	README.md
	SUMMARY.md
```

其中README.md是对本书籍的介绍，这个是必须文件。

SUMMARY.md是本书籍的目录结构。比如内容为：

```
# Summary

* [Introduction](README.md)
* [第一章](chapter1/README.md)
    * [第一节](chapter1/section1.1.md)
    * [第二节](chapter1/section1.2.md)
* [第二章](chapter2/README.md)
```

以上为示例。大家可根据自己实际需要来编写目录；

编号目录后再系统终端的命令提示符下，输入命令：

```
c:\>book\gitbook init
```

命令完成后，你会发现按你所编写的目录结构生成了初始的文件，只需要按每个文件编写内容即可了。

#### 预览serve

如你编写好了内容要预览的话，可使用如下命令：

```
c:\>book\gitbook serve
```

该命令成功以后，则可以在本地浏览器通过http://localhost:4000 来查看gitbook运行的效果了。

#### 生成build

如编写好书籍后，可通过build命令来生成静态网页：

```
c:\book\gitbook build
```

通过build命令后，会发现在book目录下会有一个新的目录_book，所有静态网页的内容都在这个目录下，可将这个目录的所有内容放在服务器上运行。其实在运行serve命令时就会首先运行build命令来生成静态网页，然后serve自行打开一个web服务器并通过监控4000端口来发布静态网页。

#### 其它命令

注意的是gitbook-cli和gitbook是2个不同软件，gitbook-cli会将gitbook不同版本下载到C:\使用者\用户登录名\\.gitbook中，但可通过设置GITBOOK_DIR环境变量来指定不同的文件夹。

#### gitbook-cli的帮助信息

```
c:\>gitbook --help
```



##### 列出gitbook所有能用的命令

```
c:\>gitbook help
```

##### 指定版本

GItbook CLI会使用缺省的最新Gitbook版本，但你也可以通过参数--gitbook来指定版本，如：

```
c:\>gitbook build ./book --gitbook=2.0.1
```

可列出指定版本可用的命令：

```
c:\>gitbook help --gitbook=2.0.1
```

#### 版本管理

##### 列出所有版本

```
c:\>gitbook ls
```

##### 列出NPM上可用的版本

```
c:\>gitbook ls-remote
```

##### 安装指定版本

```
c:\>gitbook fetch 2.1.0
# 或者前一个版本
c:\>gitbook fetch beta
```

##### 更新到最新版本

```
c:\>gitbook update
```

##### 卸载指定版本

```
c:\>gitbook uninstall 2.0.1
```

##### 使用本地文件夹做GitBook的版本(用于开发)

```
c:\>gitbook alias ./mygitbook latest
```

##### 调试

可使用参数选项--log=debug 和--debug来得到各详细错误信息，以便能进行排错；如：

```
c:\>gitbook build ./ --log=debug --debug
```

