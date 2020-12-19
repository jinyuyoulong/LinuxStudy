
正常工作流：
j singo 直接跳转到 singo 目录

主要目的是提高目录跳转效率

安装这两个包后

通过 history 命令你可以找到最近用过的命令，比如

history | grep "git clone"

通过上述命令就能找到近期 clone 了哪些库，省却了写一堆代码的功夫。autojump 就是通过记录你在 history 中的行为把你访问过的文件夹路径都 cache 下来，当你进行如下操作时：
autojump node
他会直接跳到之前访问的 ~/barretlee/work/tb/node 目录下。他还有一个快捷方式：
j node
