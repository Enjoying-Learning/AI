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