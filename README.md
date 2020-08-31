我是光年实验室高级招聘经理。
我在github上访问了你的开源项目，你的代码超赞。你最近有没有在看工作机会，我们在招软件开发工程师，拉钩和BOSS等招聘网站也发布了相关岗位，有公司和职位的详细信息。
我们公司在杭州，业务主要做流量增长，是很多大型互联网公司的流量顾问。公司弹性工作制，福利齐全，发展潜力大，良好的办公环境和学习氛围。
公司官网是http://www.gnlab.com,公司地址是杭州市西湖区古墩路紫金广场B座，若你感兴趣，欢迎与我联系，
电话是0571-88839161，手机号：18668131388，微信号：echo 'bGhsaGxoMTEyNAo='|base64 -D ,静待佳音。如有打扰，还请见谅，祝生活愉快工作顺利。

<img src="doc/pictures/logo-3.png" height=80></img>

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/CodisLabs/codis?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Build Status](https://travis-ci.org/CodisLabs/codis.svg)](https://travis-ci.org/CodisLabs/codis)

Codis is a proxy based high performance Redis cluster solution written in Go. It is production-ready and widely used at [wandoujia.com](http://wandoujia.com) and many companies. You can see [Codis Releases](https://github.com/CodisLabs/codis/releases) for latest and most stable realeases.

## Donation
Donate if you want to help us maintaining this project. Thank you!
[See this issue for details](https://github.com/CodisLabs/codis/issues/976)

## Compared with Twemproxy and Redis Cluster
<table>
<tr><th></th><th>Codis</th><th>Twemproxy</th><th>Redis Cluster</th></tr>
<tr><td>resharding without restarting cluster</td><td>Yes</td><td>No</td><td>Yes</td></tr>
<tr><td>pipeline</td><td>Yes</td><td>Yes</td><td>No</td></tr>
<tr><td>hash tags for multi-key operations</td><td>Yes</td><td>Yes</td><td>Yes</td></tr>
<tr><td>multi-key operations while resharding</td><td>Yes</td><td>-</td><td>No(<a href="http://redis.io/topics/cluster-spec#multiple-keys-operations">details</a>)</td></tr>
<tr><td>Redis clients supporting</td><td>Any clients</td><td>Any clients</td><td>Clients have to support cluster protocol</td></tr>
</table>
"Resharding" means migrating the data in one slot from one redis server to another, usually happens while increasing/decreasing the number of redis servers.

## Other Features
* GUI website dashboard & admin tools
* Supports most of Redis commands, Fully compatible with Twemproxy(https://github.com/twitter/twemproxy)
* Proxies can register on zk/etcd, clients can avoid dead proxies, see "High Availability" section.

## Tutorial

[简体中文](doc/tutorial_zh.md)
[English (WIP) ](doc/tutorial_en.md)

## FAQ

[简体中文](doc/FAQ_zh.md)
[English (WIP) ](FAQ_en.md)

## High Availability

[简体中文](doc/tutorial_zh.md#3-jodis-与-ha)
[English (WIP) ](doc/tutorial_en.md#ha)

## Architecture

![architecture](doc/pictures/architecture.png)

## Snapshots

Proxy
![proxy](doc/pictures/snapshots1.png)

Slots
![slots](doc/pictures/snapshots2.png)

Group
![group](doc/pictures/snapshots3.png)

Sentinel
![sentinel](doc/pictures/snapshots4.png)

##Benchmarks
[See benchmark results](doc/benchmark.md)

##Authors

Active authors:
* [@spinlock9](https://github.com/spinlock) [微博@斯宾洛克](http://weibo.com/spinlock9)
* [@yangzhe1991](https://github.com/yangzhe1991) [微博@\_杨肉\_](http://weibo.com/yangzhe1991)

Emeritus authors:
* [@goroutine](https://github.com/ngaut) [微博@goroutine](http://weibo.com/u/1923497393)
* [@c4pt0r](https://github.com/c4pt0r) [微博@Dongxu\_Huang](http://weibo.com/c4pt0r)

Thanks:
* [@ivanzhaowy](https://github.com/ivanzhaowy)
* [@Apache9](https://github.com/apache9) [微博@Apache9](http://weibo.com/u/1876829375)

## License

Codis is licensed under MIT， see MIT-LICENSE.txt

-------------
*You are welcome to use Codis in your product, and feel free to let us know~ :)*
