搜索的艺术：find & grep

搜索优于导航 搜索需求分为两大类：

按文件名搜索文件

按文件内容的keyword搜索文件 tips： Ctrl-r进入搜索模式 搜索命令行记录

find: 文件名搜索

grep: 文件内容搜索

例：

将目前目录及其子目录下所有延伸档名是 c 的文件列出来。·find . -name "*.c"

按name找到 **目录下的jinyuyoulong find dev/blog/github -name jinyuyoulong

注：Mac下使用的是bsd，Linux使用的是GNU，bsd find第一个参数必须指定目录路径 ,gnu 下可以省略第一个参数

根据内容搜索“搜索的艺术”
```
grep 搜索的艺术 * -r
source/_posts/2013-01-07-ubuntu-efficient-software.markdown:## 搜索的艺术：find & grep
```
* 是指搜索当前目录的所有文件， -r 是指递归当前目录进行搜索。
