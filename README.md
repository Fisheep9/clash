# clash 

## 软件下载

| <a href="https://github.com/clash-verge-rev/clash-verge-rev/releases/download/v1.7.6/Clash.Verge_1.7.6_x64-setup.exe">Windows</a> | <a href="https://github.com/clash-verge-rev/clash-verge-rev/releases/download/v1.7.6/clash-verge_1.7.6_amd64.deb">Ubuntu</a> | <a href="https://github.com/clash-verge-rev/clash-verge-rev/releases/download/v1.7.6/Clash.Verge_1.7.6_aarch64.dmg">MacOS(M series)</a> | <a href="https://github.com/clash-verge-rev/clash-verge-rev/releases/download/v1.7.6/Clash.Verge_1.7.6_x64.dmg">MacOS(Intel)</a> |



## 导入订阅链接

<p float="left">
  <img src="image/import from url.png?raw=true" width="80%" />
</p>

## 设置代理模式（系统代理 or Tun模式）

- 系统代理（关闭Tun模式，打开系统代理，混合端口可选7890）
<p float="left">
  <img src="image/open system proxy.png?raw=true" width="80%" />
  <img src="image/system proxy.png?raw=true" width="80%" />
  <img src="image/open port.png?raw=true" width="80%" />
</p>

- Tun模式（关闭系统代理，打开Tun模式）
<p float="left">
  <img src="image/Tun mode.png?raw=true" width="80%" />
</p>

## 设置路由模式（规则 or 全局）

<p float="left">
  <img src="image/route mode.png?raw=true" width="80%" />
</p>

# 常见名词

## 什么是代理模式

| 代理模式决定本机网络请求程序发出的流量如何抵达监听在本地的代理程序，即入站。

| 代理模式 | 说明 | 优点 |
| --- | --- | --- |
| **系统代理** | 代理程序会在系统级“拦截”特定的流量（如HTTP请求、系统级应用等）。设置好代理程序监听的特定端口后，进行网络请求的应用会将其流量发送到这个端口，代理服务器处理后转发到目标服务器。不同的代理方式将决定如何处理这些流量，例如通过直连或通过代理服务器转发。 | 1. 易于部署，网络请求程序必须使用“代理”配置以使流量走代理；代理程序根据预先定义的规则操作。<br>2. 不能代理 UDP 流量（如游戏数据包）。 |
| **Tun 模式** | 代理程序会创建一张虚拟网卡，通过虚拟网卡截获系统的网络流量。这使得代理可以接管所有的网络流量，代理程序通过虚拟网卡接收并处理这些网络请求。与系统代理不同的是，该步骤发生在网络请求程序发出请求之后，因此这种方法不依赖于人员的意愿。 | 1. 提供彻底的流量管理（TCP / UDP 都能完全控制的代理方式）。<br>2. 需要代理程序支持特殊的配置。 |

| 实际上两者在流量以及资源消耗上没多少区别，但即使某些软件原生不支持系统代理，用Tun也可以实现代理

## 什么是路由模式

| 路由模式决定监听在本地的代理程序的流量如何出去，即出站。

| 路由模式 | 说明 |
| --- | --- |
| **规则模式** | 根据预设的规则（例如地区、IP等）进行流量处理，决定流量是否走代理或者直接连接。例如，可以设置规则仅将访问国外网站的流量通过代理，而国内网站直接访问。 |
| **全局模式** | 所有流量均通过代理的特定端口或服务器进行。（更消耗节点流量） |
| **直连模式** | 所有流量均不通过代理直接连接。 |

| 无论是使用系统代理还是Tun模式，都可以实现规则判断、全局代理以及直连的策略

## 本地流量与节点流量

| 类型 | 说明 |
| --- | --- |
| **本地流量** | 在本地网络内部传输的部分，本地流量通常不会产生额外费用。 |
| **节点流量** | 通过你购买或订阅的远程代理服务器（节点）传输的数据。这部分流量通常是有成本的。 |


# 参考资料

https://github.com/clash-verge-rev/clash-verge-rev

https://clash-verge-rev.github.io/guide/term.html