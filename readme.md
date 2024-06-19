# ConcurrencyEchoServer
> 20种不同的并发模型示例. 

## Logs
- 2024-06-19: Repo forked. 添加`clangd` 插件下的 include path 设置（`.vscode`文件夹中的 `ros2` 环境可以忽略）.

## 1.概述
本仓库通过c++语言，使用了20种不同的并发模型实现了回显服务，并设计实现了简单的应用层协议。

## 2.目录结构
本仓库的目录结构如下所示。
```
.
├── BenchMark
│   ├── benchmark.cpp
│   ├── client.hpp
│   ├── clientmanager.hpp
│   ├── makefile
│   ├── percentile.hpp
│   ├── stat.hpp
│   └── timer.hpp
├── ConcurrencyModel
│   ├── Epoll
│   ├── EpollReactorProcessPoolCoroutine
│   ├── EpollReactorProcessPoolMS
│   ├── EpollReactorSingleProcess
│   ├── EpollReactorSingleProcessCoroutine
│   ├── EpollReactorSingleProcessET
│   ├── EpollReactorThreadPool
│   ├── EpollReactorThreadPoolHSHA
│   ├── EpollReactorThreadPoolMS
│   ├── LeaderAndFollower
│   ├── MultiProcess
│   ├── MultiThread
│   ├── Poll
│   ├── PollReactorSingleProcess
│   ├── ProcessPool1
│   ├── ProcessPool2
│   ├── Select
│   ├── SelectReactorSingleProcess
│   ├── SingleProcess
│   └── ThreadPool
├── common
│   ├── cmdline.cpp
│   ├── cmdline.h
│   ├── codec.hpp
│   ├── conn.hpp
│   ├── coroutine.cpp
│   ├── coroutine.h
│   ├── epollctl.hpp
│   ├── packet.hpp
│   └── utils.hpp
├── readme.md
└── test
    ├── codectest.cpp
    ├── coroutinetest.cpp
    ├── makefile
    ├── packettest.cpp
    ├── unittestcore.hpp
    └── unittestentry.cpp
```
相关的文件和目录的说明如下。
- BenchMark是基准性能压测工具的代码目录。
- ConcurrencyModel是20种不同并发模型的代码目录。
- common是公共代码的目录。
- test目录为单元测试代码的目录。


## References
- 万木春. 《Linux后端开发工程实践》. 2024. ISBN：9787115625625
- [WeChat-腾讯技术工程. 20种不同并发模型示例，带你深入理解并发模型](https://mp.weixin.qq.com/s/aTYie9PHcoXRYYmmIGaOXA)
- [WeChat-腾讯云开发者. 微信程序员压测20种并发模型，性能最强的竟是？](https://mp.weixin.qq.com/s/2HeUctZyOyZKwFx6pzxOrA)