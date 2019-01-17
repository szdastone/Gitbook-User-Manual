# 安装

​	Gitbook的安装还是比较简单的，本文的介绍都是基于本地安装Gitbook,但如果[官网](https://www.gitbook.com)提供的服务已经满足了您的需求，则可忽略本文档。由于本人使用的window系统，以下介绍也是基于window系统介绍的。

### 本地安装

---

#### 系统要求

安装Gitbook很容易，但是系统必须满足如下要求：

- NodeJS(建议v4.00或以上)

Gitbook可安装在Windows,Linux,Unix或者Mac OS X上。

#### 通过NPM安装

最方便的就是通过NPM来安装Gitbook。在系统终端的提示符下，只需要简单的输入如下命令就可以安装Gitbook。

```
c:\>npm install gitbook-cli -g
```

gitbook-cli是一个可在同一个操作系统下安装和使用多个Gitbook的应用。它能自动安装Gitbook的最合适版本来编译书籍。

由于使用windows系统，安装完成以后却无法使用gitbook命令，后来查资料才搞明白，设置好路径就可以了。一般安装了gitbook-cli后，在C:\使用者\用户登录名\\.gitbook下的versions目录下会有对应版本的gitbook。在npm命令中使用参数-g，则表明将gitbook-cli全局安装到Node对应的路径下。该路径为C:\使用者\用户登录名\\.nodejs\node_global；在该路径下应该可发现gitbook命令，如发现则证明安装正确了，将该路径加入到系统路径即可。设置好后在系统终端就可以使用gitbook命令了。