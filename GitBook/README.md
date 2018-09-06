# 学习资源

* [gitbook 简明教程](http://www.chengweiyang.cn/gitbook/basic-usage/README.html)
* [使用 Gitbook 打造你的电子书](http://www.cnblogs.com/jingmoxukong/p/7453155.html)
* [GitBook 使用教程](https://blog.csdn.net/axi295309066/article/details/61420694)

## 常用命令

```sh
gitbook init //初始化目录文件
gitbook help //列出gitbook所有的命令
gitbook --help //输出gitbook-cli的帮助信息
gitbook build //生成静态网页
gitbook serve //生成静态网页并运行服务器
gitbook build --gitbook=2.0.1 //生成时指定gitbook的版本, 本地没有会先下载
gitbook ls //列出本地所有的gitbook版本
gitbook ls-remote //列出远程可用的gitbook版本
gitbook fetch 标签/版本号 //安装对应的gitbook版本
gitbook update //更新到gitbook的最新版本
gitbook uninstall 2.0.1 //卸载对应的gitbook版本
gitbook build --log=debug //指定log的级别
gitbook builid --debug //输出错误信息
```

## 转换命令

必要操作: 安装 calibre

```sh
gitbook pdf   // 将 GitBook 生成为 PDF
gitbook mobi  // 将 GitBook 生成为 mobi
```

## 关于 `book.json`

如果直接复制的话, 由于 JSON 不支持注释, 需要将 `//` 语句删除.

```json
{
    // 输出文件夹
    // 注意: 它会覆盖命令行传入的参数
    // 不建议在此文件中配置
    "output": null,
    // 产生的书籍的类型
    // 注意: 它会覆盖命令行传入的参数
    // 不建议在此文件中配置
    "generator": "site",
    // 图书标题和描述 (默认从README抽取)
    "title": null,
    "description": null,
    // 对于ebook格式, 扩展名the extension to use for generation (default is detected from output extension)
    // "epub", "pdf", "mobi"
    // 注意: 它会覆盖命令行传入的参数
    // 不建议在此文件中配置
    "extension": null,
    // GitHub 信息(defaults are extracted using git)
    "github": null,
    "githubHost": "https://github.com/",
    // 插件列表, can contain "-name" for removing default plugins
    "plugins": [],
    // 插件通用配置
    "pluginsConfig": {
        "fontSettings": {
            "theme": "sepia",
            "night" or "white",
            "family": "serif" or "sans",
            "size": 1 to 4
        }
    },
    // 模版中的链接 (null: default, false: remove, string: new value)
    "links": {
        // Custom links at top of sidebar
        "sidebar": {
            "Custom link name": "https://customlink.com"
        },
        // Sharing links
        "sharing": {
            "google": null,
            "facebook": null,
            "twitter": null,
            "weibo": null,
            "all": null
        }
    },
    // PDF 参数
    "pdf": {
        // Add toc at the end of the file
        "toc": true,
        // Add page numbers to the bottom of every page
        "pageNumbers": false,
        // Font size for the fiel content
        "fontSize": 12,
        // Paper size for the pdf
        // Choices are [u’a0’, u’a1’, u’a2’, u’a3’, u’a4’, u’a5’, u’a6’, u’b0’, u’b1’, u’b2’, u’b3’, u’b4’, u’b5’, u’b6’, u’legal’, u’letter’]
        "paperSize": "a4",
        // Margin (in pts)
        // Note: 72 pts equals 1 inch
        "margin": {
            "right": 62,
            "left": 62,
            "top": 36,
            "bottom": 36
        }
    }
}
```

## 支持数学公式

Use it for your book, by adding to your book.json:
在你的 book 根目录添加 `book.json`, 配置如下

```json
{
    "plugins": [
        "mathjax", "katex"
    ]
}
```

然后, 运行 `gitbook install` 即可.

具体参考: [Math typesetting using KaTex](https://plugins.gitbook.com/plugin/katex)

## 支持中文搜索

具体见 [gitbook-plugin-search-pro-kui](https://plugins.gitbook.com/plugin/search-pro-kui)