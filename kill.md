kill 命令用于强制退出某个进程，例如 kill -9 1099[pid]

但是我一般不这样用，因为进程的pid是未知的，需要查询。

所以我这里有一案例，关闭 Xcode app

案例：

killall Xcode && sudo shutdown -s now

// 关闭 Xcode 成功后立即将Mac 睡眠 -s 是sleep的意思
