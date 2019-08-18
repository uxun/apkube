---
title: "Atom"
layout: page
collection: Editor
date: 2019-06-02 00:00
---
## Atom (OS X)
### Install
`brew cask install atom`
### Theme
[atom-material-ui](https://atom.io/themes/atom-material-ui) + [atom-material-syntax](https://atom.io/themes/atom-material-syntax) 
[monokai](https://atom.io/themes/monokai)
[Dracula](https://draculatheme.com/atom/)
[Lucario](https://github.com/raphamorim/lucario)

### Plugin
| Plugin               | Comment                       |
| -------------------- | ----------------------------- |
| Highlight-line       | 高亮行                        |
| Highlight-selected   | 高亮所选文字                  |
| File-icons           | 文件图标                      |
| Autocomplete-paths   | 自动补全路径                  |
| Autocomplete-modules | 自动补全模块名                |
| Activate-power-mode  | 震震果实                      |
| linter+linter-eslint | 代码校验工具                  |
| Atom-beautify        | 格式化代码：ctrl-alt-b        |
| Docblockr            | 快速生成注释                  |
| Markdown             | mardown语法                   |
| Expose               | 分屏-依赖 Minimap ，fileicons |
| Split-diff           | 比较文件差异 ctrl-alt-t       |
| Git-plus             | Git插件 ，需配置email ，user  |

### Command
**project**

| Command      | Comment                   |
| ------------ | ------------------------- |
| ctrl-0       | 切换到目录树 （Esc 返回） |
| h            | 展开选择的目录            |
| L            | 隐藏选择的目录            |
| ctrl-alt-]   | 所有目录展开              |
| ctrl-alt-[   | 所有目录隐藏              |
| a            | new file                  |
| m            | 修改所选文件路径          |
| d            | 所选文件复制另存          |
| crtl-shift-c | 复制所选文件路径          |

**movement**

| Command        | Comment              |
| -------------- | -------------------- |
| cmd-up         | 文件开头             |
| cmd-down       | 文件结尾             |
| ctrl-cmd-up    | 整行上移             |
| ctrl-cmd-down  | 整行下移             |
| ctrl-g         | 移动到指定行         |
| ctrl-cmd-left  | 选中内容左移         |
| ctrl-cmd-right | 选中内容右移         |
| ctrl-shift-P   | 向上选择             |
| ctrl-shift-N   | 向下选择             |
| ctrl-shift-F   | 向左选择             |
| ctrl-shift-B   | 向右选择             |
| ctrl-m         | 括号跳转             |
| ctrl-cmd-m     | 括号tag 之间文本选取 |

**Multi-line cursor**

| Command         | Comment                  |
| --------------- | ------------------------ |
| cmd-d           | 选词 and 当前相同下一个  |
| ctrl-cmd-g      | 选择当前文档所有相同的词 |
| ctrl-shift-up   | 当前光标上方加入新光标   |
| ctrl-shift-down | 当前光标下方加入新光标   |
| cmd-Shift-L     | 将多行选择转换为多光标   |

**Other**

| Command                | Comment                    |
| ---------------------- | -------------------------- |
| cmd-shift-o            | 打开目录                   |
| ctrl - T               | 交换光标处两侧字符         |
| ctrl-k                 | 删除光标后到本行结尾的内容 |
| ctrl-k                 | 删除光标后到本行结尾的内容 |
| cmd-shift-d            | 复制当前行                 |
| ctrl-shift-K           | 删除当前行                 |
| alt-h                  | 删除当前词到词首           |
| alt-d                  | 删除当前词到词末           |
| ctrl-Shift-M           | 预览Markdwon               |
| cmd-j                  | 将下一行拼接到当前行末     |
| cmd-l                  | 选中一行                   |
| ctrl-shift-u           | 激活文件编码菜单           |
| cmd-k + cmd-u          | 当前词转化为大写           |
| cmd-k + cmd-L          | 当前词转化为小写           |
| cmd-b                  | 打开文件之间切换           |
| crtl-shift-l           | 语法高亮                   |
|                        |                            |
| 代码折/缩进            |                            |
| alt-cmd-shift-[        | 折叠所有                   |
| alt-cmd-shift-]        | 展开所有                   |
| alt-cmd-[              | 折叠代码                   |
| alt-cmd-]              | 展开代码                   |
| cmd-[                  | 左缩进                     |
| cmd-]                  | 右缩进                     |
| cmk-k+ cmd-n           | n层折叠                    |
| cmd-r                  | 方法                       |
|                        |                            |
| 书签                   |                            |
| cmd+ fn-2              | 新增本行书签               |
| f2                     | 当前文件下一个书签         |
| shift-f2               | 当前文件上一个书签         |
| ctrl-f2                | 列出当前文件所有书签       |
| ctrl f  正则替换空白行 | \n[\t]*\n                  |

