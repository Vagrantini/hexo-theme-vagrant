# vagrant

[English](README.en.md) | [简体中文](README.md)

一个简洁轻量化的响应式[Hexo](https://hexo.io/)博客主题。

- 点击预览[【深色主题】](https://chaooo.github.io/)、[【浅色主题】](https://chaoo.oschina.io/)

[vagrant template preview](https://vagrantini.com) 

## 安装

### 安装主题和渲染:

```shell
$ git clone https://github.com/Vagrantini/hexo-theme-vagrant.git themes/vagrant
$ npm install hexo-renderer-jade@0.3.0 --save
$ npm install hexo-renderer-stylus --save
```
### 启用

在Hexo配置文件（`hexo/_config.yml`）中把主题设置修改为`vagrant`。
```  bash
theme: vagrant
```
如果你想生成压缩后的css，在（`hexo/_config.yml`）中添加：
``` yml
stylus:
  compress: true
```


### 更新

``` bash
cd themes/vagrant
git pull
```

## 配置
打开`themes/vagrant/_config.yml`进行配置。

``` yml
##########################
## Site Config Settings ##
##########################

# Theme version
version: 2.0.2

# Theme tone
dark: false #true/false  #切换为true,即可体验深色主题

# Header
menu:
  - page: home
    directory: .
    icon: fa-home
  - page: archive
    directory: archives/
    icon: fa-archive

# Sidebar
widgets:
  - recent_posts
  - category
  - tag
  - archive
  #- weibo
  - links

# Toc
toc:
  enable: true
  number: false

# Static files
js: js
css: css

#Local search
local_search: true ## Use a javascript-based local search engine, true/false.

#Copyright
copyright: 
  enable: true #display article copyright information, true/false.
  describe: #copyright description
  
# MathJax Support
mathjax:
  enable: false  #true/false.
  cdn: //cdn.bootcss.com/mathjax/2.7.1/latest.js?config=TeX-AMS-MML_HTMLorMML

# Analytics
google_analytics: ## Your Google Analytics tracking id, e.g. UA-42025684-2
baidu_analytics: ## Your Baidu Analytics tracking id, e.g. 1006843030519956000

# Miscellaneous
show_category_count: true ## If you want to show the count of categories in the sidebar widget please set the value to true.
widgets_on_small_screens: true ## Set to true to enable widgets on small screens.
busuanzi: true ## If you want to use Busuanzi page views please set the value to true.

# Friend link
links:
  - title: site-name1
    url: http://www.example1.com/
  - title: site-name2
    url: http://www.example2.com/
  - title: site-name3
    url: http://www.example3.com/
```

- **version** - 用于自动刷新CDN上的静态文件。
- **menu** - 导航菜单。
- **widgets** - 侧边栏中的窗口小部件。
- **Toc** - 文章目录
- **Static files** - 静态文件目录，以方便CDN使用。
- **Local search**
- self_search - 默认本地JS搜索.
- **links** - 友情链接。
- **Miscellaneous**
- show_category_count - 是否在侧边栏分类中显示类别的数量（true/false）.
- widgets_on_small_screens - 小屏幕下侧边栏在底部显示.
- busuanzi - 用[Busuanzi](http://busuanzi.ibruce.info)来统计网站访问量.
- google_analytics - [Google Analytics](https://www.google.com/analytics/) tracking ID。
- baIDu_analytics - [Baidu Analytics](http://tongji.baidu.com) tracking ID。

## 特征

#### 站点图标
您可以准备一张ico格式并命名为** favicon.ico **，请将其放入hexo目录的`source`文件夹，建议大小：32px * 32px。

您可以为苹果设备添加网站徽标，请将名为** apple-touch-icon.png **的图像放入hexo目录的“source”文件夹中，建议大小为：114px * 114px。

#### 添加站点关键字
请在hexo目录的“hexo/_config.yml”中添加`keywords`字段，如：
```YAML
# Site
title: Hexo
subtitle: 副标题
description: 网站简要描述,如：Charles·Zheng's blog.
keywords: 网站关键字, key, key1, key2, key3
author: Charles
language: zh-CN
```

#### 设置阅读全文
您可以在文章的 front-matter 中添加 description，并提供文章摘录，或在文章中使用‘‘`<!--more-->`’’手动进行截断（Hexo推荐的方式）。

#### 自定义page页面
在`source`文件夹中创建文件夹`index.md`来添加页面，并在`index.md`的`front-matter'中添加`layout：page`。
Create folders inlcuding `index.md` in `source` folder to add pages, and add a `layout: page` in `front-matter` of `index.md`.

#### 代码语法高亮
请在hexo目录的“hexo/_config.yml”中设置“highlight”选项，如下所示：
```YAML
highlight:
  enable: true
  auto_detect: true
  line_number: true
  tab_replace:
```

#### 本地搜索
如果要使用本地站点搜索，您必须安装插件[hexo-generator-json-content](https://github.com/alexbruno/hexo-generator-json-content)来创建JSON搜索文件 ，然后将配置添加到`hexo/_config.yml`：
```shell
$ npm install hexo-generator-json-content@2.2.0 --save
```
然后在`hexo/_config.yml`添加配置：
```YAML
jsonContent:
  meta: false
  pages: false
  posts:
    title: true
    date: true
    path: true
    text: true
    raw: false
    content: false
    slug: false
    updated: false
    link: false
    permalink: false
    excerpt: false
    categories: false
    tags: true
```

#### 语言
该主题目前有七种语言：简体中文（zh-CN），繁体中文（zh-TW），英语（en），法语（fr-FR），德语（de-DE），韩语 （ko）,西班牙语（es-ES）,欢迎修改主题并翻译成其他语言。

## Solutions
- 检查您当前的hexo的根目录，是否包含`source /`，`themes /`等。

## 浏览器支持
![Imgur](http://i.imgur.com/iO9L5ty.png)

## License
[MIT License](LICENSE)

## 贡献
欢迎各种形式的贡献（增强功能，添加新功能，撰写文档，改进代码，提交问题和检查BUG...）。

期待您的pull request。
