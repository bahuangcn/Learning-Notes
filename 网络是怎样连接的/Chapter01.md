# 浏览器生成消息 —— 探索浏览器内部

## 1.1 生成 HTTP 请求消息

URL：Uniform Resource Locator，统一资源定位符

URI：Uniform Resource Identifier，统一资源标识符

网址是 URL 的一种。

URL的各种格式

![URL 的各种格式](/网络是怎样连接的/img/1-1.png)

URL开头的文字，即 “http:” "ftp:" "file:" "mailto:" 这部分文字都表示浏览器应当使用的访问方法。

浏览器的第一步工作就是对URL进行解析。

### HTTP 协议

HTTP 协议定义了客户端和服务器之间交互的消息内容和步骤。

交互步骤：

1. 客户端向服务器发送请求消息，消息中包括URI和方法。URI即访问目标，方法主要是 GET、POST、DELETE、PUT等。
2. 服务器在收到请求消息后，会对其中的内容进行解析， 通过URI和方法的要求来完成自己的操作，最后将结果房子响应消息中。
3. 响应消息被发送回客户端，客户端收到后从中读取数据并显示。

HTTP 的主要方法

![HTTP 的主要方法](/网络是怎样连接的/img/1-2.png)

![HTTP 消息格式](/网络是怎样连接的/img/1-3.png)

## 1.2 向 DNS 服务器查询 Web 服务器的 IP 地址

网络号分配给子网，主机号分配给子网中的计算机，合在一起就是 IP 地址。实际的IP地址是一串32比特的数字，将IP地址按照8比特（1字节）为一组分成4组，分别用十进制表示然后用圆点隔开，就形成了我们常见的IP地址格式。