# 主题

从版本3.0.0以后，Gitbook能定制主题了。缺省书籍使用了theme-default主题。

#### 主题的结构

其实主题也是一个插件，但它包含了模板和资源。任意主题都是继承自缺省主题，但可选覆盖任何主题模板。

| 目录                       | 描述                                           |
| -------------------------- | ---------------------------------------------- |
| _layouts                   | 包含了所有模板的主目录                         |
| _layouts/website/page.html | 单一页面模板                                   |
| _layouts/ebook/page.html   | 在ebook生成时用到的单一页面模板(PDF<ePub,Mobi) |

#### 扩展/定制主题

作者可通过书籍的源代码直接扩展主题的模板(不需要另外创建主题)。模板首先会在数据的_layouts文件夹中解析，然后在安装插件/主题。

#### 主题插件

Gitbook缺省的主题一般都够用了。除了用户可自行扩展主题外，还可通过NPM搜索主题插件。在NPM上，gitbook的主题插件一般都是以gitbook-theme开头的。

下面介绍几种常用主题插件。

##### theme-default

这个是缺省插件。这里将showLevel设为true，这样就会显示标题前面的数字索引，默认是不显示的。

```
{
    "theme-default": {
        "showLevel": true
    }
}
```

##### theme-comscore

comscore可以为标题增加颜色，而缺省主题都是黑白色的。

[插件地址](https://plugins.gitbook.com/plugin/theme-comscore)

要使用该插件，只需要将如下代码加入到book.json中。

```
{
	"plugins": [
        "theme-comscore"
 	]
 }
```

