fzf是一个命令行工具，目前支持bash和zsh。
模糊搜索工具
配合 autojump 和 vim 非常好使

配置
全局定义：~/.fzf.zsh
默认快捷键可以在.fzf/shell/key-bindings.zsh中修改。 推荐将默认的文件搜索快捷键从Ctrl-T改成了Ctrl-J
使用
工作流
命令行下输入 ctl+R 可以进入历史命令，使用fzf模糊搜索
vi has**name<Tab> 模糊查询文件名,回车选中的文件。

原生使用
fzf默认会从STDIN读入数据，然后将结果输出到STDOUT
find * -type f | fzf > selected
上面命令从find的搜索结果中读入，输出到文件selected中
使用指南：
　* 打开方法
　　命令行下执行 fzf 即可展示当前目录下所有文件列表，可以用键盘上下键或者鼠标点出来选择 
　 * 和vim组合使用：
　　vim $(fzf)
* 切换目录：
  cd $(find * -type d | fzf)
* 切换git分之：
  git checkout $(git branch -r | fzf)
* shell命令补全：
 fzf 默认使用 ** 来补全 shell 命令，比起默认的 tab 补全，fzf 补全不知道高到哪里去了。cd, vim, kill, ssh, export… 统统都能补全，好用哭
-----
进阶
文件搜索
要编辑client/templates/lists/lists.coffee文件，只要在命令行中输入vi然后按Ctrl-j， 就进入了fzf搜索界面，只要输入任意层目录中的几个字符，就可以匹配到目标文件， 例如上面lists.coffee文件，只要输入listco就可以匹配到了。 其中当输入到list时，就匹配到了lists文件夹以及下面的两个文件， 这时可以继续输入"co"，直接命中目标，也可以用Ctrl-j/k在列表中上下选择目标
实际上fzf进行目录文件匹配的快捷键是Ctrl-T，但对vi进行了特殊定义，使得用也可以出发fzf搜索。
按Alt-C，选择好目录，可以直接切换到目标目录，相当于cd <Ctrl-T>的快捷版。

Ctrl-R在命令行历史使用模糊匹配。
历史命令搜索
Ctrl-r激活搜索列表，然后模糊匹配；
可以使用多种配置格式，例如前缀、后缀、取反、严格一致等等， 例如搜索单词date（而不是包含d,a,t,e的任何字符串），在Ctrl-R后输入'date, 详见文档对"extended-search mode"的说明。
进程搜索
输入kill然后空格键 按Tab键显示系统进程列表，开始模糊搜索；
