---
id: U1jPkSOTGBUnj2E2rB4HG
title: DNSpoisoning
desc: ''
updated: 1644809473480
created: 1644809473480
---

DNS投毒（DNS Poisoning）是 #GFW 的一个重要手段，是利用传统的域名解析服务的公开性进行篡改后返回错误的IP地址。在加密通讯技术越来越普及的世代，因为DNS本身的发展的限制，这个方法仍然非常有效。

## DNS投毒的原理、

由于防火长城是一个通路的（on-path）/旁观者（man-on-the-side）的系统 ，所以它没办法通过修改或者简单丢弃互联网上传输的那些被封锁的域名的 DNS 查询响应。但是由于 DNS 使用无状态、未加密的 UDP 协议进行传输，所以 GFW 可以通过可以实时监测互联网上的流量，当在用户的 DNS 查询中检测到受审查的内容时，注入错误的响应。

当一个子域名被封锁时，顶级域名可能不会被封锁。例如，cs.colorado.edu 被防火长城封锁了，而 colorado.edu 却没有被封锁，这说明GFW 有时候也考虑到过渡封锁带来的[[censorship.collateraldamage]]。

## DNS投毒的实例

2021年12月25日，中国的游戏用户报告 Steam 游戏平台在中国无法访问，域名解析指向了一个错误的 IP 地址。国外用户查验后没有同样的问题，之后用户报告在中国工信部网站上,Steam 的社区域名（steampowered.com）已经列入黑名单。


## DNS投毒的影响

[[censorship.collateraldamage]]，影响国民和全球经济。

DNS投毒给了GFW发动资源耗尽攻击（resource exhaustion attacks）的可能性。 一旦 GFW 将 DNS 查询的结果大量导向某个 IP 地址，受影响的组织将在服务器上付出不可忽视的开销。

## 参考资料

- [The Great Firewall of China: A Digital Black Hole](https://www.catchpoint.com/blog/great-firewall-of-china) 