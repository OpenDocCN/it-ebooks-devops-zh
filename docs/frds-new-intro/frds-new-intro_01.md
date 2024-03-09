# 序

FreeRADIUS 新手入门包含了大量实际的练习来帮助你学会从基础的安装到更高级的配置像集成 LDAP 和 Active Directory 的一切.这本书将会帮助你理解在 FreeRADIUS 里面的 authentication, authorization 和 accounting 使用现在最流行的 linux 发行版. 使用 realms 和 fail-over 配置的更大规模的部署也在 tips 里面涵盖到了. 每个章节最后有一个课堂测试来验证你的理解.

## 这本书涵盖了哪些内容

这本书可以被划分为 3 个部分:

1.  介绍和安装(第一章到第三章)
2.  FreeRADIUS 的 AAA 功能(第四章到第七章)
3.  高级话题(第八章到第十三章)

让我们来看看每一章的内容:

第一章, 介绍 AAA 和 RADIUS, 介绍 FreeRADIUS 和 RADIUS 协议. 他着重介绍了一些关键的 RADIUS 概念, 帮助用户避免常见的误解.

第二章, 安装, 描述在流行的 linux 发行版上如何从源码编译和安装 FreeRADIUS. 也涵盖了使用流行的 linux 发行版的预编译的 FreeRADIUS 的安装包来安装. Ubuntu, SUSE, 和 CentOS 将会被使用来确保广泛的覆盖.

第三章, 开始使用 FreeRADIUS, 简要的介绍 FreeRADIUS 的许多组件. 也讨论了处理一个基本 authentication 请求的过程.

第四章, Authentication, 教授 authentication 方法和他们如何工作. EAP(Extensible Authentication Protocol)在后面一个专门的章节讲解.

第五章, 用户名和密码的来源, 涵盖许多用户名/密码组合可以存储的地方. 他显示了哪些模块被包含并且怎样配置 FreeRADIUS 来实现这些存储.

第六章, Accounting, 讨论 accounting 的需求和记录 accounting 数据的可选项. 也讨论了实现一个 policy, 包含限制 sessions 和/或时间和/或数据.

第七章, Authorization, 讨论了 authorization 的许多方面, 包括 unlang 的使用.

第八章, 虚拟服务器, 讨论了虚拟服务器的许多方面和他们可能被潜在地使用的地方.

第九章, 模块, 讨论了 FreeRADIUS 使用的许多模块和如何配置某个模块的 multiple instances.

第十章, EAP, 一个专门讨论 EAP 的章节, 是一个一站式 EAP(802.11x 和 WiFi)的章节.

第十一章, 字典, 介绍字典, 用来映射管理员看到和使用的名字, 到 RADIUS 协议使用的数字.

第十二章, 漫游和代理, 处理 RADIUS 协议, 允许 authorization 和 accounting 请求的代理. 这个让漫游成为可能. 这章包含了关于 FreeRADIUS 中使用代理的许多方面.

第十三章, 排查问题, 解答许多常见问题, 给出例子如何去搜索, 和如何修复问题.

## 阅读这本书的前提

你需要熟悉 linux 和对 TCP/IP 有扎实的理解. 不需要提前知道 RADIUS 和 FreeRADIUS.

为了最好的实践练习, 你需要一个干净安装的 Ubuntu, SUSE 或者 CentOS.

## 这本书是为了谁写的?

如果你是一个 IPS 或者网络管理者, 需要跟踪和控制网络使用, 那么这本书是为你准备的.

## 读者反馈

来自我们的读者的反馈永远是欢迎的. 让我们知道你对这本书的看法 -- 无论你是否喜欢. 读者的反馈对我们来说是重要的. 读者的反馈是重要的对于我们来写出你最能好好利用的话题.

为了给我发送反馈, 简单低发送一封邮件到 feedback@packtpub.com, 并且提到书名在你的邮件的主题中.

如果有本书你需要并且想要看到我们发布, 请发送给我们通过[`packtpub.com`](http://packtpub.com)网站上的`SUGGEST A TITLE`或者发送邮件到 suggest@packtpub.com

如果有一个话题你有经验并且感兴趣, 想要写或者贡献一本书, 可以看网站[`packtpub.com/authors`](http://packtpub.com/authors)上的`author guide`.

## 客户支持

由于你是 Packet 书的骄傲的拥有者, 我们有许多东西来帮会组你来充分利用你的购买.

### 下载这本书的样例程序

你可以在网站[`www.PacktPub.com`](http://www.PacktPub.com)上通过你的购买账号下载所有你购买的书的样例程序. 如果你在其他地方购买, 你可以访问[`www.PacktPub.com/support`](http://www.PacktPub.com/support)并且注册来让邮件直接发送给你.

## 勘误表

尽管我们已经已经很小心的确保我们内容的准确性, 错误也会发生. 如果你在我们其中的一本书中发现错误--也许是文字中错误或者代码中错误--我们将会感激如果你愿意报告给我们. 通过这样做, 你可以让其他读者避免挫折并且帮助我们改进这本书的子版本. 如果你发现任何错误, 请访问[`www.packtpub.com/support`](http://www.packtpub.com/support)来报告他们, 选择你的书, 点击`errata submission form`链接, 并且输入你的错误的细节. 一旦你的错误被验证, 你的提交将会被接受并且勘误将会被上传到我们的网站, 或者被添加到任何现有的勘误列表, 在那个书名的勘误部分. 任何现有的看屋可以通过选择你的书名从[`www.packtpub.com/support`](http://www.packtpub.com/support)来查看.

## 版权侵权

互联网上内容的版权侵权是一个一直存在的问题, 包括任何媒介. 在 Packt, 我们会认真保护我们的版权和许可证. 如果你偶然发现任何我们作品的非法拷贝, 以任何形式, 在互联网上, 请立即提供给我们地址或者网址, 这样我们可以追踪补救.

请通过 copyright@packtpub.com 联系我们, 附带一个怀疑侵权的链接.

我们欣赏你保护我们作者的帮助, 这样我们能够给你有价值的内容.

## 问题

你可以通过 questions@packtpub.com 联系我们, 如果你关于这本书的任何方面有问题, 这样我们将会尽我们最大努力查出他.