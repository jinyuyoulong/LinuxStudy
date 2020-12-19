scp 文件传输

本地上传数据到Server:

scp -P 123 bin/gin root@0.0.0.0:/home/git/

scp -P 端口号 本地目录 用户名@IP:服务器目录 

scp是secure copy的简写，用于在Linux下进行远程拷贝文件的命令，和它类似的命令有cp，不过cp只是在本机进行拷贝不能跨服务器，而且scp传输是加密的。

从服务器下载文件

scp username@servername:/path/filename /tmp/local_destination
