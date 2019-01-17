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

这里再说下shortName，希望大家能明白。

在[disqus官网](https://disqus.com/)先注册一个账号，或者通过google,twitter,facebook账号授权注册都行。注册完了在Account页面可以看到Username，这个Username就是需要填写的shortName。

是不是这样就OK了呢？肯定不行，这是页面加载不上Disqus，为啥呢？需要你为你的网页增加一个site，登录后点击[Admin](https://disqus.com/admin/)，进入到管理页面。在管理页面选择[Installing Disqus](https://disqus.com/admin/install/)；然后在这个页面选择[Create a Site](https://disqus.com/admin/create/)，按要求填写后就可以管理你的Site了，在Site的设置页面填写好Website Name以及Website URL就可以了。注意的是Website URL是你访问的域名，比如<username>.github.io。

设置好了，再次编译，发布以后就可以正常看到Disqus了。

