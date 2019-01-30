# 发布

这里介绍是将书籍发布到Github Pages。如需要了解Github Pages，请参考[Github Pages主页](https://pages.github.com/)。

为了将书籍构建好后放在Github Pages中，需要在本地构建出site格式。这样，就可以通过如下地址进行访问了：

~~~
<username>.github.io/<project>
~~~

#### 发布到gh-pages分支

首先需要先安装gh-pages。在系统终端输入如下命令：

```
c:\>npm i gh-pages -g
```

这时在系统终端可输入gh-pages命令了，如要查看怎么使用，可在终端输入如下命令：

```
c:\>gh-pages --help
```

如已经通过gitbook build命令构建书籍了，则会在目录下有个_book子目录，该目录就是本书籍的静态网页了。通过gh-pages发布到Github就可以了。在终端输入如下命令:

```
c:\>gh-pages -d _book
```

如发布成功后，则会发现在github的书籍项目中除了master分支多了一个gh-pages分支了。这是就需要明白这2个分支的作用。

- master分支：保存书籍的源码
- gh-pages分支：保存书籍编译以后的静态网页

#### 上传源码到master分支

好了，现在我们需要将源码都上传到master分支。

首先，我们必须在书籍目录下建立文件.gitignore，不需要上传的文件忽略掉；文件.gitignore的内容如下代码。

~~~
*~
_book
node_modules
~~~

然后将目录下除了.gitignore忽略的文件都上传到master分支。

~~~
c:\>book\git add.
c:\>book\git commit -m "add source"
c:\>book\git push -u origin master
~~~

好了。我们可以通过```<username>.github.io/<project>```来访问本书籍了。

