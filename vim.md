Vim

自带教程 终端输入 `vimtutor`

两种模式状态
1. 命令模式
2. 编辑模式

命令模式下的操作

## 命令
- :vsplit 垂直分割窗口
- :e file 打开文件
- :quite 关闭最后一个窗口 :close 也是关闭窗口
- ctl+w 切换窗口

## 快捷键
- dd 删除一行;三行：3dd
- y(yard 提取) 复制
- d()剪切
- p(paste)粘贴
- :wq 或 ZZ 或 保存退出 :q! 强制退出
- / 搜索 命令模式下 /user 搜索 user 关键字 shift+n 或 n 定位下一个
- i 所有非hjkl的字符 进入编辑模式
- 0 或 shift+6 回到行首
- $ 回到行尾
- 数字+回车 下移n行
- shift+g
- shift+e
- ctl+f ctl+b 翻页
- u undo 撤回操作 ctl+r 反向撤销
- ctl+w 切换窗口

## 剪切板
- cmd模式输入v进入 选择模式，光标选中后输入"+yy 复制到系统剪切板
- "+y 选取到默认的vim 剪切版
### 编辑模式
文字编辑器

### 配置
.vimrc
.vim/colors/solarized.vim

```
syntax enable
set background=dark
colorscheme solarized

" Indentation & Tabs

set autoindent

set smartindent

set tabstop=4

set shiftwidth=4

set expandtab

set smarttab

" Display & format

set number

set textwidth=80

set wrapmargin=2

set showmatch

" Search

set hlsearch

set incsearch

set ignorecase

set smartcase

" Browse & Scroll

set scrolloff=5

set laststatus=2

" Spell

set spell spelllang=en_us

" Miscellaneous

set nobackup

set noswapfile

set autochdir

set noundofile

set visualbell

set errorbells

```
