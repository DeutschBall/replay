针对地面站的重放攻击：
1.首先登录地面站，获取token值
2.修改getTaskList.sh 中的token值，执行getTaskList.sh获取当前活跃的任务ID
3.修改其他脚本比如unlock.bat或者takeoff.bat中的token值以及taskID，执行这些任务，让无人机解锁或者降落

sh拓展名脚本用到UNIX shell比如bash/git bash/cygwin等等终端执行
bat拓展名脚本可以使用windows CMD执行
