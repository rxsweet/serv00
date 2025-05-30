# 保活 - 大佬库
```
本仓库用于定时自动化登录serv00的SSH连接执行指令并推送通知，
可以实现定期登录保号，
访问我的博客了解更多信息www.zzzwb.com

利用GitHub的Actions实现serv00定时登录自动保号
https://www.zzzwb.com/2024/07-11-serv00-automation.html
通过cloudflare提供的免费cdn给serv00节点加速
https://www.zzzwb.com/2024/07-21-serv00-cloudflare.html
```
https://github.com/bin862324915/serv00-automation


# 安装Vmess  - 大佬库
```
在serv00服务器上部署vmess免费节点,并通过Cloudflare的CDN加速节点，提升上网速度
```
https://github.com/ansoncloud8/am-serv00-vmess

https://github.com/eooce/Sing-box

# 使用到的命令

显示进程PID: ps aux
关闭进程(PID): kill PID
关闭进程(进程名w): pkill -f w

pgrep -x w > /dev/null || nohup /home/rx/.rxv1/w run -c /home/rx/.rxv1/c.json >/dev/null 2>&1 &
```
这条命令是一个组合命令，用于检查进程是否存在，如果不存在则启动一个后台进程。让我分解解释：
pgrep -x w > /dev/null
pgrep -x w：精确查找(-x)名为"w"的进程
> /dev/null：将输出重定向到空设备，即不显示任何输出
||：逻辑"或"操作符，如果前面的命令失败（返回非零状态码）则执行后面的命令
nohup /home/rx/.rxv1/w run -c /home/rx/.rxv1/c.json >/dev/null 2>&1 &
nohup：让命令在用户退出登录后继续运行
/home/rx/.rxv1/w run -c /home/rx/.rxv1/c.json：运行w程序，带run命令和-c配置文件参数
>/dev/null 2>&1：将标准输出和标准错误都重定向到空设备
&：在后台运行
整体含义：检查是否有名为"w"的进程正在运行，如果没有，则以后台方式启动/home/rx/.rxv1/w程序，使用指定的配置文件，并且不显示任何输出。
这种命令常用于确保某个程序持续运行，通常可以放在启动脚本或定时任务中。
```
