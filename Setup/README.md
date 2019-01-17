# 配置

其实Gitbook是零配置的。如果不想做出其他效果，那么就可以不进行任何配置。

如要进行配置的话，那么需要自己建立一个book.json文件在书籍目录下。

先了解下book.json的基本配置吧。

#### 基本配置

| 变量       | 描述                                                    |
| ---------- | ------------------------------------------------------- |
| root       | 包含书籍所有文件的根文件夹                              |
| structure  | 指定README,SUMMARY,GLOSSARY等的路径                     |
| title      | 书籍的标题，缺省值从README获取                          |
| decription | 书籍的描述，缺省值从README获取                          |
| author     | 书籍的作者                                              |
| isbn       | 书籍的ISBN                                              |
| language   | 书籍的语言，缺省为en                                    |
| direction  | 文字的排版方向。可以为rtl或ltr,缺省值因爱language的设定 |
| gitbook    | Gitbook将使用的版本，可指定版本或接受如“>=3.0.0”的条件  |

#### 插件Plugins

插件以及其配置都是指定在book.json中。从3.0.0版本以后，Gitbook可使用主题。

| 变量          | 描述             |
| ------------- | ---------------- |
| plugins       | 要加载的插件列表 |
| pluginsConfig | 插件的配置       |

#### Structure

除了root变量外，可为gitbook指定README,SUMMARY,GLOSSARY,LANGUAGES等文件的名称，比如README使用缺省名称为README.md。这些文件将放在书籍的根目录(或者放在不同语言的根目录下)。形如dir/MY_README.md的路径是不接受的。

| 变量                | 描述                                |
| ------------------- | ----------------------------------- |
| structure.readme    | Readme文件的名称，缺省README.md     |
| structure.summary   | Summary文件的名称，缺省SUMMARY.md   |
| structure.glossary  | Glossary文件的名称，缺省GLOSSARY.md |
| structure.languages | Languages文件的名称，缺省为LANGS.md |

#### PDF选项

PDF的输出可在book.json中配置，支持的参数如下：

| 变量              | 描述                                                         |
| ----------------- | ------------------------------------------------------------ |
| pdf.pageNumbers   | 在每页的底部增加页码数，缺省为true                           |
| pdf.fontSize      | 设置字体大小，缺省为12                                       |
| pdf.fontFamily    | 设置字体，缺省为Arial                                        |
| pdf.paperSize     | 设置纸张大小，可选为'a0', 'a1', 'a2', 'a3', 'a4', 'a5', 'a6', 'b0', 'b1', 'b2', 'b3', 'b4', 'b5', 'b6', 'legal', 'letter'，缺省为a4 |
| pdf.margin.top    | 页眉，缺省为56                                               |
| pdf.margin.bottom | 页尾，缺省为56                                               |
| pdf.margin.right  | 右边距，缺省为62                                             |
| pdf.margin.left   | 左边距，缺省为62                                             |

