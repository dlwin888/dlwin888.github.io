---
title: Hello World
tags: hexo
categories: hexo
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)



## sitemap & rss

切换到blog根目录下，输入：

```javascript
$ npm install hexo-generator-feed
$ npm install hexo-generator-sitemap
```

之后重启博客，访问`/atom.xml`和`/sitemap.xml`，会发现已经生成了。可以把sitemap提交到搜索引擎的站长平台来增加收录。



### 2.1 Google 版本

进入到根目录下，打开`CMD`，运行下面的命令：

```powershell
npm install hexo-generator-sitemap --save
```

### 2.2 [Baidu 版本](https://zhida.zhihu.com/search?content_id=121687672&content_type=Article&match_order=1&q=Baidu+版本&zhida_source=entity)

进入到根目录下，打开`CMD`，运行下面的命令：

```text
npm install hexo-generator-baidu-sitemap --save
```



# 给博客增加 Sitemap 和 Robots（Hexo）

Hexo 生成的静态网站，默认没有集成 Sitemap 功能。而我们的网站，如果想要更好的被搜索引擎收录，建议给站点增加 Sitemap。下面是操作步骤：



## 1. 安装 hexo-generator-sitemap

在 Hexo 生成站点的根目录下执行以下命令：

```
npm install hexo-generator-sitemap --save
```

因为我用的是 `pnpm` 包管理工具，所以我这里执行的命令是：

```
pnpm add hexo-generator-sitemap
```

## 2. 配置 sitemap.xml

安装完插件后，编辑站点根目录下的 `_config.yml` 配置文件，寻找是否有 sitemap 字样，如果没有则增加配置：

```
# Sitemap
sitemap:
  path:
    - sitemap.xml
  tags: true
```

我这里配置了在 sitemap 中显示标签，如果不想显示标签，可以把 `tags: true` 删掉。

## 3. 配置站点 URL

还是在 `_config.yml` 中，查看 `url` 字段是否配置正确。

```
url: https://www.guozhenyi.com
```

如果没有正确配置 `url`，生成的 `sitemap.xml` 可能会缺少正确的链接结构。

## 4. 生成 Sitemap

在站点根目录下执行：

```
hexo clean && hexo g
```

生成完成后，即可在 `public/` 目录下看到 `sitemap.xml` 文件。

## 5. 增加 robots.txt

同样的，Hexo 没有自带 `robots.txt` 文件，为了对搜索引擎更友好，建议在 `source/` 目录下创建 `robots.txt` 文件，内容为：

```
User-agent: *
Disallow:
Sitemap: https://www.guozhenyi.com/sitemap.xml
```

请把里面的域名换成你自己的域名。
