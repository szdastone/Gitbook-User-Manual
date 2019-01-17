# 插件

插件是扩展Gitbook功能(电子书和网站)的最佳方式。现有的插件功能繁多：可支持数学公司，谷歌分析等。

#### 怎么找插件呢？

可以在[plugins.gitbook.com](plugins.gitbook.com)查找或者在[NPM](https://www.npmjs.com/)或者[Github](https://github.com/GitbookIO/gitbook)上找插件。

Gitbook的插件在NPM上都是以gitbook-plugin开头的，很容易查找的。

#### 插件的安装和配置

插件安装很简单，只需要在book.json的plugins中增加相应插件就可以了。配置则需要根据不同插件来分别对待，但都是保存在pluginsConfig下的。



下面就常用的几款插件进行简单介绍下。

##### Disqus

[Disqus](https://plugins.gitbook.com/plugin/disqus)是个非常流行的网站继承评论系统工具。Gitbook添加了该插件，则可以让读者在网页下面进行评论。

要使用该插件，则在book.json中增加如下代码。

```
{
    "plugins": ["disqus"],
    "pluginsConfig": {
        "disqus": {
            "shortName": "XXXXXXX"
        }
    }
}
```

代码中的shortName是在[disqus官网](https://disqus.com/)上创建的website获得的唯一关键字。

但是如果某一个页面不想使用disqus的话，则可在页面中指定，如下代码。

```
---
disqus: false
---

# My Page without disqus
```

