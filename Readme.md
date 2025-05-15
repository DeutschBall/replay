# 5.16仿真对抗内容：

## 针对地面站的重放攻击

1.攻击者首先弱口令登录地面站，浏览器开发者工具抓包获取**token**值

2.修改`getTaskList.sh `中的**token**值，执行`getTaskList.sh`获取当前活跃的`taskID`

3.修改其他脚本比如`unlock.bat`或者`takeoff.bat`中的`token`值以及`taskID`，执行这些任务，让无人机解锁或者降落



其中sh拓展名脚本用到UNIX shell比如bash/git bash/cygwin等等终端执行

其中bat拓展名脚本可以使用windows CMD执行



## 针对树莓派抛投程序的udp报文攻击

首先确保安装了ncat或者nc

在攻击者设备上执行：

```
echo 1 | ncat 192.168.10.102 8715
```

> 192.168.10.102为树莓派设备ip地址

在树莓派上执行：

```
echo 1 | ncat 127.0.0.1 8715
```



上述两个命令意义相同，但是之前的对抗中异常检测只能发现前者而忽略后者

本次仿真对抗重试









