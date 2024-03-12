# 一，OSI七层模型

### MVC架构

视图层 + 控制器 + 服务层 + 模型层 + 数据库

### 分层模型

* 应用层：网络服务与最终用户的一个接口（提供网络与用户应用软件之间的接口服务 => HTTP）
* 表示层：数据的表示、安全、压缩（提供格式化的表示和转换数据服务，如加密和压缩）
* 会话层：建立、管理、终止会话（提供包括访问验证和会话管理在内的建立和维护应用之间通信的机制）
* 传输层：定义传输数据的协议端口号，以及流控和差错校验（提供建立、维护和取消传输连接功能，负责可靠的传输数据 => TCP）
* 网络层：进行逻辑地址寻址，实现不同网络之间的路径选择（处理网络间路由，确保数据及时传送 => 路由器）
* 数据链路层：建立逻辑连接，进行硬件地址寻址，差错校验等功能（负责无错传输数据，确认帧、发错重传等 => 交换机）
* 物理层：建立、维护、断开物理连接（提供机械、电气、功能和过程特性 => 网卡、网线、双绞线、同轴电缆、中继器）

### 不同层中的称谓

* 比特流：
* 数据帧（Frame）：是一种信息单位，它的起始点和目的点都是数据链路层。
* 数据包（Packet）：也是一种信息单位，它的起始和目的地是网络层。
* 段（Segment）：通常是指起始点和目的地都是传输层的信息单元。
* 消息（message）：是指起始点和目的地都在网络层以上（经常在应用层）的信息单元。

# 二、TCP/IP参考模型

5层模型

* 应用层：HTTP、FTP、TFTP、SMTP、SNMP、DNS
* 传输层：TCP、UDP
* 网络层：IP、ARP、RARP、ICMP、IGMP
* 数据链路层
* 物理层

### 常见协议

* HTTP
* FTP
* SMTP
* DNS
* TCP
* UDP
* IP
* ARP：地址解析协议，即ARP（Address Resolution Protocol），是根据IP地址获取物理地址的一个TCP/IP协议
* RARP：反向地址转换协议（RARP：Reverse Address Resolution Protocol） 反向地址转换协议（RARP）允许局域网的物理机器从网关服务器的 ARP 表或者缓存上请求其 IP 地址

# 三、网络接口层

网络接口层是TCP/IP模型的最底层，负责接收从上一层交来的数据报并将数据报通过底层的物理网络发送出去，比较常见的就是设备的驱动程序，此层没有特定的协议

### 1、物理层

* 计算机在传递数据的时候传递的都是0和1的数字，而物理层关心的是用什么信号来表示0和1，是否可以双向通信，最初的连接如何建立以及完成连接如何终止,物理层是为数据传输提供可靠的环境
* 尽可能的屏蔽掉物理设备和传输媒介，使数据链路层不考虑这些差异，只考虑本层的协议和服务
* 为用户提供在一条物理传输媒体上提供传送和接收比特流的能力
* 需要解决物理连接、维护和释放的问题

#### 1.1 非归零编码

0101010110111000

#### 1.2 曼彻斯特编码

* 内部自含时钟
* 每个自带变化

> 缺点：编译码较复杂、占用更多的信道带宽

### 2、数据链路层

### 2.1 以太网

以太网（Ethernet）是一种计算机局域网技术。IEEE组织的IEEE 802.3标准制定了以太网的技术标准，它规定了包括物理层的连线、电子信号和介质访问层协议的内容

### 2.2 总线型拓扑

### 2.3 MAC地址

### 2.4 以太网帧格式

### 2.5 ARP协议

* 地址解析协议，即ARP（Address Resolution Protocol），是根据IP地址获取物理地址的一个TCP/IP协议
* 主机发送信息时将包含目标IP地址的ARP请求广播到网络上的所有主机，并接收返回消息，以此确定目标的物理地址；收到返回消息后将该IP地址和物理地址存入本机ARP缓存中并保留一定时间，下次请求时直接查询ARP缓存以节约资源
* 地址解析协议是建立在网络中各个主机互相信任的基础上的，网络上的主机可以自主发送ARP应答消息，其他主机收到应答报文时不会检测该报文的真实性就会将其记入本机ARP缓存
* 由此攻击者就可以向某一主机发送伪ARP应答报文，使其发送的信息无法到达预期的主机或到达错误的主机，这就构成了一个ARP欺骗

# 四、网络层

位于传输层和网络接口层之间,用于把数据从源主机经过若干个中间节点传送到目标主机,并向传输层提供最基础的数据传输服务,它要提供路由和选址的工作

### 1、选址

交换机是靠MAC来寻址的，而因为MAC地址是无层次的,所以要靠IP地址来确认计算机的位置,这就是选址

### 2、路由

在能够选择的多条道路之间选择一条最短的路径就是路由的工作

### 3、IP

在网络中，每台计算机都有一个唯一的地址，方便别人找到它，这个地址称为IP地址。

### 3.4 子网掩码

### 3.5 ipv6

# 五、传输层

# 六、应用层

* 路由表


