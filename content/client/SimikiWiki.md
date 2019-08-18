---
title: "SimikiWiki"
layout: page
collection: Blog
date: 2019-08-18 21:16
---
## Simiki wiki

**[REFERNECE](http://simiki.org/zh-docs/)**

> 配置文件参数
> _config.yml：http://simiki.org/zh-docs/configuration.html

### 1.Prepare

```shell
# 1> install python
$ brew install python3
# 2> install simiki depend
$ pip3 install simiki 
$ pip3 show simiki
$ pip3 install fabric
$ pip3 install fabric3
$ pip3 install ghp-import 
# 3> create <uname>.github.io ---> https://pages.github.com/
```

### 2.[Init](http://simiki.org/zh-docs/deploy.html)

```shell
# clone your wiki.git
$ git clone git@github.com:uname/wiki.git
# create branch gh-pages
$ git checkout -b gh-pages
$ git rm -rf .

# checkout your master branch init
$ git checkout master
$ simiki init
$ simiki g

# 目录结构
$ ls wiki
.
├── _config.yml # 配置文件
├── content		# *.md
├── fabfile.py	# deploy script
├── output		# html
└── themes
    └── simple2
```

### 3.Deploy Github Pages

1)配置_config.yml中的deploy配置项：6.\_config.yml
2)确认本地与远程仓库的关联`git remote -v` 
3)fab deploy 实际执行[ghp-import](https://github.com/davisp/ghp-import) `ghp-import -p -m "Update output documentation" -r origin -b gh-pages output`，

```shell
# 以git底层命令 git fast-import遍历output目录所有推送gh-pages分支
$ fab deploy
```

### 4.Simiki [Command](http://simiki.org/zh-docs/usage.html)

```shell
# 查看 simiki 命令帮助文档
$ simiki -h

# 生成静态页面到output目录 (需要在站点根目录下执行)
$ simiki g

# 生成静态页面(包括草稿)到output目录 (需要在站点根目录下执行)
$ simiki g --draft

# 本地预览模式(开发模式)
$ simiki p

# 本地预览模式指定绑定IP和端口, 如绑定到所有IP的8888端口
$ simiki p --host 0.0.0.0 --port 8888

# 本地预览模式监控content目录, 有变更自动更新生成相应静态页面
$ simiki p -w

# 升级Simiki后检查和更新本地内置的脚本及主题(如fabfile.py, simple2主题)
$ simiki update
```

### 5.[Collection/Tag](http://simiki.org/zh-docs/collection_and_tag.html)

**集合(collection)**

```shell
---
title: "Git"
date: 2019-01-01 00:00
collection: Version Control
---

---
title: "SVN"
date: 2019-01-02 00:00
collection: Version Control
---
```

**标签(tag)**
标签使多篇Wiki之间互相有关联性。

```shell
---
title: "Practical Vim"
date: 2014-11-13 22:11
tag: vim  # 以逗号分隔的字符串方式配置tag
---

==> content/tool/vim.md <==
---
title: "Vim"
date: 2013-08-17 07:32
tag:  # 以列表的方式配置tag
  - vim
---
```

### 6._config.yml [REFERNECE](http://simiki.org/zh-docs/configuration.html)

```yml
# Document:
# http://simiki.org/docs/configuration.html
url: http://NAME.github.io/wiki
title: NAME's WIKI
keywords:
description:
author: AUTHOR
theme: yasimple_x2
#theme: simple2

root: /wiki
source: content
destination: output
themes_dir: themes

##### Parser #####
markdown:
  - fenced_code
  - extra
  - codehilite(css_class=hlcode, linenums=False)
  - toc(title=Table of Contents)

default_ext: md
pygments: true
debug: false

#category:
#  - name: linux  # 目录名
#    label: Linux/运维  # 目录的别名, 生成首页时可以使用
#  - name: database
#    label: 数据库
#

##### Deploy #####
deploy:
  - type: git
    remote: origin
    branch: gh-pages
```

