# 发布

这里介绍是将书籍发布到Github Pages。如需要了解Github Pages，请参考[Github Pages主页](https://pages.github.com/)。

为了将书籍构建好后放在Github Pages中，需要在本地构建出site格式。这样，就可以通过如下地址进行访问了：

~~~
<username>.github.io/<project>
~~~

首先需要先安装gh-pages。在系统终端输入如下命令：

```
c:\>npm i gh-pages -g
```

这是在系统终端可输入gh-pages命令了，如要查看怎么使用，可在终端输入如下命令：

```
c:\>gh-pages --help
```

如已经通过gitbook build命令构建书籍了，则会在目录下有个_book子目录，该目录就是本书籍的静态网页了。通过gh-pages发布到Github就可以了。在终端输入如下命令:

```
c:\>gh-pages -d _book
```

