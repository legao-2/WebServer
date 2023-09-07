# WebServer
用C++实现的高性能WEB服务器，经过webbenchh压力测试可以实现上万的QPS
# 功能
- 使用同步I/O方式模拟出Proactor模式
- 利用IO复用技术Epoll与线程池实现多线程的Reactor高并发模型；
- 利用字符串分割与状态机解析HTTP请求报文，实现处理静态资源的请求；
- 基于升序链表实现的定时器，关闭超时的非活动连接；
# 环境要求
- Linux
- C++
# 项目启动
`./myserver port`
# 压力测试
`./webbench -c 1000 -t 5 http://192.168.106.128:10000/index.html`
