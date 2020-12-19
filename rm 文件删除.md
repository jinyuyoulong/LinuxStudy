系统自带的 rm 命令删除文件有很高的的风险，一旦删错，就不在好恢复。

trash-cli是一个使用 python 开发的软件包，包含trash-put、restore-trash、trash-list、trash-empty、trash-rm等命令.

我们可以通过这写命令，将文件移动到回收站，或者还原删除了的文件。

trash-put命令会把我们想要删除的文件移动到~/.local/share/Trash/files 中，

相关信息记录在~/.local/share/Trash/info中。
