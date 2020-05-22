---
title: maupassant主题
---

## 主题安装
安装主题和渲染器：

```
$ git clone https://github.com/tufu9441/maupassant-hexo.git themes/maupassant
$ npm install hexo-renderer-pug --save
$ npm install hexo-renderer-sass --save
```

编辑Hexo目录下的 _config.yml，将theme的值改为maupassant。

注：若npm install hexo-renderer-sass安装时报错，可能是国内网络问题，请尝试使用代理或者切换至淘宝NPM镜像安装，感谢光头强提供的方法。

## 功能配置
默认配置:

```
_config.yml_config.yml
fancybox: true ## If you want to use fancybox please set the value to true.
disqus: ## Your disqus_shortname, e.g. username
uyan: ## Your uyan_id. e.g. 1234567
livere: ## Your livere data-uid, e.g. MTAyMC8zMDAxOC78NTgz
changyan: ## Your changyan appid, e.g. cyrALsXc8
changyan_conf: ## Your changyan conf, e.g. prod_d8a508c2825ab57eeb43e7c69bba0e8b
gitment:
  enable: false ## If you want to use Gitment comment system please set the value to true.
  owner: ## Your GitHub ID, e.g. username
  repo: ## The repository to store your comments, make sure you're the repo's owner, e.g. imsun.github.io
  client_id: ## GitHub client ID, e.g. 75752dafe7907a897619
  client_secret: ## GitHub client secret, e.g. ec2fb9054972c891289640354993b662f4cccc50
gitalk:
  enable: false ## If you want to use Gitment comment system please set the value to true.
  owner:  ## Your GitHub ID, e.g. username
  repo:  ## The repository to store your comments, make sure you're the repo's owner, e.g. gitalk.github.io
  client_id:  ## GitHub client ID, e.g. 75752dafe7907a897619
  client_secret:  ## GitHub client secret, e.g. ec2fb9054972c891289640354993b662f4cccc50
  admin:  ## Github repo owner and collaborators, only these guys can initialize github issues.
valine: ## https://valine.js.org
  enable: false ## If you want to use Valine comment system, please set the value to true.
  appid: ## Your LeanCloud application App ID, e.g. pRBBL2JR4N7kLEGojrF0MsSs-gzGzoHsz
  appkey: ## Your LeanCloud application App Key, e.g. tjczHpDfhjYDSYddzymYK1JJ
  notify: false ## Mail notifier, see https://github.com/xCss/Valine/wiki/Valine-评论系统中的邮件提醒设置
  verify: false ## Validation code.
  placeholder: Just so so ## Comment box placeholders.
  avatar: 'mm' ## Gravatar type, see https://github.com/xCss/Valine/wiki/avatar-setting-for-valine
  pageSize: 10 ## Number of comments per page.
  guest_info: nick,mail,link ## Attributes of reviewers.

google_search: true ## Use Google search, true/false.
baidu_search: false ## Use Baidu search, true/false.
swiftype: ## Your swiftype_key, e.g. m7b11ZrsT8Me7gzApciT
tinysou: ## Your tinysou_key, e.g. 4ac092ad8d749fdc6293
self_search: false ## Use a jQuery-based local search engine, true/false.
google_analytics: ## Your Google Analytics tracking id, e.g. UA-42425684-2
baidu_analytics: ## Your Baidu Analytics tracking id, e.g. 8006843039519956000
show_category_count: false ## If you want to show the count of categories in the sidebar widget please set the value to true.
toc_number: true ## If you want to add list number to toc please set the value to true.
shareto: false ## If you want to use the share button please set the value to true, you must have hexo-helper-qrcode installed.
busuanzi: false ## If you want to use Busuanzi page views please set the value to true.
widgets_on_small_screens: false ## Set to true to enable widgets on small screens.
canvas_nest:
  enable: false ## If you want to use dynamic background please set the value to true, you can also fill the following parameters to customize the dynamic effect, or just leave them blank to keep the default effect.
  color: ## RGB value of the color, e.g. "100,99,98"
  opacity: ## Transparency of lines, e.g. "0.7"
  zIndex: ## The z-index property of the background, e.g. "-1"
  count: ## Quantity of lines, e.g. "150"
donate:
  enable: false ## If you want to show the donate button after each post, please set the value to true and fill the following items according to your need. You can also enable donate button in a page by adding a "donate: true" item to the front-matter.
  github: ## GitHub URL, e.g. https://github.com/Kaiyuan/donate-page
  alipay_qr: ## Path of Alipay QRcode image, e.g. /img/AliPayQR.png
  wechat_qr: ## Path of Wechat QRcode image, e.g. /img/WeChatQR.png
  btc_qr: ## Path of Bitcoin QRcode image, e.g. /img/BTCQR.png
  btc_key: ## Bitcoin key, e.g. 1KuK5eK2BLsqpsFVXXSBG5wbSAwZVadt6L
  paypal_url: ## Paypal URL, e.g. https://paypal.me/tufu9441

menu:
  - page: home
    directory: .
    icon: fa-home
  - page: archive
    directory: archives/
    icon: fa-archive
  - page: about
    directory: about/
    icon: fa-user
  - page: rss
    directory: atom.xml
    icon: fa-rss

widgets: ## Six widgets in sidebar provided: search, category, tag, recent_posts, rencent_comments and links.
  - search
  - category
  - tag
  - recent_posts
  - recent_comments
  - links

links:
  - title: site-name1
    url: http://www.example1.com/
  - title: site-name2
    url: http://www.example2.com/
  - title: site-name3
    url: http://www.example3.com/

timeline:
  - num: 1
    word: 2014/06/12-Start
  - num: 2
    word: 2014/11/29-XXX
  - num: 3
    word: 2015/02/18-DDD
  - num: 4
    word: More

# Static files
js: js
css: css

# Theme version
version: 0.0.0
```

* fancybox - 是否启用Fancybox图片灯箱效果
* disqus - Disqus评论 shortnam
* uyan - 友言评论 id
* livere - 来必力评论 data-uid
* changyan - 畅言评论 appid
* gitment - Gitment评论相关参数
* gitalk - Gitalk评论相关参数
* valine - Valine评论相关参数
* google_search - 默认使用Google搜索引擎
* baidu_search - 若想使用百度搜索，将其设定为true。
* swiftype - Swiftype 站内搜索key
* tinysou - 微搜索 key
* self_search - 基于jQuery的本地搜索引擎，需要安装hexo-generator-search插件使用。
* google_analytics - Google Analytics 跟踪ID
* baidu_analytics - 百度统计 跟踪ID
* show_category_count - 是否显示侧边栏分类数目
* toc_number - 是否显示文章中目录列表自动编号
* shareto - 是否使用分享按鈕，需要安装hexo-helper-qrcode插件使用
* busuanzi - 是否使用不蒜子页面访问计数
* widgets_on_small_screens - 是否在移动设备屏幕底部显示侧边栏
* canvas_nest - 是否使用canvas动态背景
* donate - 是否启用捐赠按钮
* menu - 自定义页面及菜单，依照已有格式填写。填写后请在source目录下建立相应名称的文件夹，并包含index.md文件，以正确显示页面。导航菜单中集成了FontAwesome图标字体，可以在这里选择新的图标，并按照相关说明使用。
* widgets - 选择和排列希望使用的侧边栏小工具。
* links - 友情链接，请依照格式填写。
* timeline - 网站历史时间线，在页面front-matter中设置layout: timeline可显示。
* Static files - 静态文件存储路径，方便设置CDN缓存。
* Theme version - 主题版本，便于静态文件更新后刷新CDN缓存。

### 主题特性
#### 网站图标
若要设置网站Favicon，可以将favicon.ico放在Hexo根目录的source文件夹下，建议的大小：32px*32px。

若要为网站添加苹果设备图标，请将命名为apple-touch-icon.png的图片放在同样的位置，建议的大小：114px*114px。

#### 文章摘要
首页默认显示文章摘要而非全文，可以在文章的front-matter中填写一项description:来设置你想显示的摘要，或者直接在文章内容中插入<!--more-->以隐藏后面的内容。
若两者都未设置，则自动截取文章第一段作为摘要。

#### 添加页面
在source目录下建立相应名称的文件夹，然后在文件夹中建立index.md文件，并在index.md的front-matter中设置layout为layout: page。现已支持添加标签页面，将页面的layout设置为layout: tagcloud即可。若需要单栏页面，就将layout设置为 layout: single-column。

#### 文章目录
在文章的front-matter中添加toc: true即可让该篇文章显示目录。

#### 文章评论
文章和页面的评论功能可以通过在front-matter中设置comments: true或comments: false来进行开启或关闭（默认开启）。

#### 语法高亮
要启用代码高亮，请在Hexo目录的_config.yml中将highlight选项按照如下设置：

```
highlight:
  enable: true
  auto_detect: true
  line_number: true
  tab_replace:
```

数学公式
要启用数学公式支持，请在Hexo目录的_config.yml中添加：

```
mathjax: true
```
并在相应文章的front-matter中添加mathjax: true，例如：

```
title: Test Math
date: 2016-04-05 14:16:00
categories: math
mathjax: true
---
```

数学公式的默认定界符是$$...$$和\\[...\\]（对于块级公式），以及$...$和\\(...\\)（对于行内公式）。

但是，如果你的文章内容中经常出现美元符号“$”, 或者说你想将“$”用作美元符号而非行内公式的定界符，请在Hexo目录的_config.yml中添加：

```
mathjax2: true
```

而不是mathjax: true。 相应地，在需要使用数学公式的文章的front-matter中也添加mathjax2: true。

示例。

#### 支持语言
目前支持简体中文（zh-CN），繁体中文（zh-TW），英语（en），法语（fr-FR），德语（de-DE），韩语（ko）和西班牙语（es-ES），欢迎翻译至其它语言。

#### 问题解决
检查一下终端当前的目录是否为Hexo的根目录，并包含source/和themes/。

使用过程中遇到问题欢迎提交issue。

参考：https://www.haomwei.com/technology/maupassant-hexo.html#disqus_thread