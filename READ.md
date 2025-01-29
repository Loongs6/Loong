#  <center><font face="楷体" color="red">网络编程有关的命令</font></center>

---


|nc -lu| nc -lp|
|:--:|:--:|
|nc -lu port | nc -lp port|
|nc -u(UDP)对方ip port(端口号)| nc 对方ip port(端口号)|

```c
   1.netstat命令
       (1)功能简介
             用于显示各种网络相关信息，如网络连接，路由表，接口状态
             netstat会显示两部分信息：
                    激活的Internet连接信息
                        就是真正的网络连接，显示TCP和UDP当前激活的连接情况
                    
       (2)常用参数举例
             netstat -h    查看netstat的帮助
             netstat -tu   列出所有处于ESTABLISHED(连接)状态的TCP信息

   2.netcat命令(linux中简称nc)
       (1)功能简介
             netcat，在网络工具中有瑞士军刀美誉，其有Windows和Linux的版本。因为它短小精悍、功能实用，被设计为一个简单、可靠的网络工具，可通过TCP或UDP协议传输数据。
       (2)常用参数举例
             用命令模拟tcp和udp通信
             nc -h  获取nc命令的使用帮助
             nc -lu 50001  启动udp程序，绑定50001
                           你可以在另外一个终端上执行nc -u 对方的ip 50001，然后双方就能键盘输入双向通信了
             nc -lp 50001  启动tcp程序，绑定50001
                           你可以在另外一个终端上执行nc 对方的ip 50001，然后双方就能键盘输入双向通信了
```

