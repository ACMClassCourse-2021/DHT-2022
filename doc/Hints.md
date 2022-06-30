# Some Hints

> 本文档给出一些建议和推荐资料，你并非必须阅读

1. 关于Go语法

   你需要**重点**掌握的是并发编程([goroutine](https://chai2010.cn/advanced-go-programming-book/ch1-basic/ch1-06-goroutine.html))和远程过程调用([RPC](https://chai2010.cn/advanced-go-programming-book/ch4-rpc/ch4-01-rpc-intro.html))

   其他部分的语法可以初步了解之后边学边用

   > 这里是一份go官方语法[tutorial](https://go.dev/tour/welcome/1)

2. 关于测试程序

   助教下发(并用以评分)的测试程序所做的事情是：在你的电脑上初始化若干个DHT节点，通过网络传输信息并维护结构，用以模拟在若干台分布的服务器运行效果。你**不应**通过网络以外的途径通信(例：内存)，你的程序**应当**能在真正的分布式场景下正确运行。

3. 关于DHT协议

   推荐阅读的综述[blog](https://luyuhuang.tech/2020/03/06/dht-and-p2p.html)，对协议有个初步了解。

   详细技术细节请翻阅两篇paper：[Chord](https://pdos.csail.mit.edu/papers/chord:sigcomm01/chord_sigcomm.pdf) 和 [Kademila](https://pdos.csail.mit.edu/~petar/papers/maymounkov-kademlia-lncs.pdf) (助教非常**希望**每位同学都阅读论文)

   其他辅助参考资料：[Kademila in Go](http://blog.notdot.net/tag/kademlia)  [Chord 解释](https://zhuanlan.zhihu.com/p/53711866) [Kad 解释 ](http://xlattice.sourceforge.net/components/protocol/kademlia/specs.html#intro) 

4. 关于Application

   > 欢迎任何天马行空的想法 以下是示例：

   一个好玩的[网站](https://iknowwhatyoudownload.com/)：嗅探BT网络中ip的资源请求

   P2P资源分享应用：[BitTorrent](https://blog.jse.li/posts/torrent/#putting-it-all-together) 及一些原理解释 [blog](https://www.cnblogs.com/LittleHann/p/6180296.html)