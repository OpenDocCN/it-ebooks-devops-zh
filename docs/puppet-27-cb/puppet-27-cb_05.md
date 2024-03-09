# 前言

## 前言

IT 运维的一场革命来了。配置管理工具可以在几秒钟内建立服务器并自动化管理你的整个网络。 要充分利用云计算的力量，建立可靠、可扩展、安全、高性能的系统，像 Puppet 这样的工具是必不可少的，

本书为你带来基础知识的基础上，探讨了 Puppet 的强大功能， 向你展示了如何解决各种现实世界问题和应用的详细步骤。 每一个步骤，向你展示了需要键入什么命令，其中还包括每个处方的完整代码样本。

本书从 Puppet 的基础知识入手，为读者介绍了 Puppet 最新最先进的功能， 使读者对 Puppet 有更深入的理解。同时介绍了 Puppet 社区的最佳实践、如何书写优质的配置清单代码、 扩展 Puppet 的部署规模、提高 Puppet 性能、以及如何为 Puppet 添加自定义的提供者和资源等内容。

本书包含了一些来自生产系统的实例，这些实例介绍了如今世界大量 Puppet 安装正在使用的技术， 包括一个分布式的 Puppet 架构和一个使用 Apache 和 Passenger 实现的高性能 Puppetmaster 解决方案。 通过这个实践指南探索世界上最流行的配置管理系统（Puppet）的强大功能。

# 本书内容

### 本书内容

Chapter 1, Puppet Infrastructure introduces some key techniques for managing your Puppet server and manifests, including version control, automated deployment, file serving, pre-signing and autosigning certificates, scaling with Passenger, and a distributed decentralized Puppet architecture using Git.

Chapter 2, Monitoring, Reporting, and Troubleshooting covers ways that Puppet can report information about what it’s doing, and the status of your systems. This includes graphical and e-mail reports, log and debug messages, dependency graphing, testing and dry-running your manifests, using tags, run stages, and environments, and a guide to some of Puppet’s more common error messages.

Chapter 3, Puppet Language and Style will show you examples of good programming style in Puppet and language constructs that can help you keep your code concise and readable, including conditionals, selectors, case statements, arrays, and regular expressions.

Chapter 4, Writing Better Manifests takes you through structuring your Puppet manifests using node and class inheritance, resource dependencies, and parameterized classes. You’ll also see how to get data in and out of Puppet from the environment using CSV files and shell scripts.

Chapter 5, Working with Files and Packages covers powerful techniques for managing config files, including ERB templates, generating files from snippets, and using the Augeas tool. You’ll also see how to use Puppet to install packages from APT repositories, and how to set up your own APT and Gem repositories.

Chapter 6, Users and Virtual Resources explains how virtual resources can help you manage different combinations of users and packages on different machines, and shows you how to use Puppet’s resource scheduling and auditing features.

Chapter 7, Applications focuses on some specific applications that you may need to manage with Puppet, including complete recipes for Apache and Nginx, MySQL, Drupal, and Rails.

Chapter 8, Servers and Cloud Infrastructure extends the power of Puppet to managing virtual machines, both in the cloud and on your desktop, with recipes for Vagrant and EC2 instances. It also shows you how to set up a Nagios monitoring server, load balancing with HAProxy, firewalls with iptables, network filesystems with NFS, and high-availability services with Heartbeat.

Chapter 9, External Tools and the Puppet Ecosystem looks at the tools that have grown up around Puppet and help you integrate it with the rest of your network, including Puppet Dashboard, Foreman, and MCollective. It also introduces you to some advanced topics including writing your own resource types, providers, and external node classifiers.

# 阅读前提

### 阅读前提

要运行这本书中的例子，你需要一台安装了 Ubuntu Linux 10.04 的电脑，安装 Puppet 并与互联网连接。

虽然不是绝对必要的，但我还是建议准备一台咖啡机或其他形式的含咖啡因的饮料机。

# 适用读者

### 适用读者

本书假定你已经安装过 Puppet，或许已经写过一些基本的配置清单或适于发布的模块。 同时需要一些 Linux 系统的管理经验，包括熟悉的命令行、文件系统和文本编辑等。 但没有编程经验的要求。

# 格式约定

### 格式约定

在这本书中，你会发现一些不同的文本样式以区分不同种类的信息。这里是一些样式的例子及其含义。

正文中的代码样式举例；“你需要一台 Puppetmaster 以及 /etc/puppet 目录下的一些已存在的配置清单。”

一个代码块的样式举例：

```
 #!/bin/sh

  syntax_errors=0
  error_msg=$(mktemp /tmp/error_msg.XXXXXX)

  if git rev-parse --quiet --verify HEAD > /dev/null
  then
  against=HEAD
  fi 
```

一个命令行输入或输出的样式举例：

```
# puppet parser validate/etc/puppet/manifests/site.pp
err: Could not parse for environment production: Syntax error at end
of file at /etc/puppet/manifests/site.pp:3 
```

**新术语**和**重要文字** 以粗体显示。你在屏幕上看到的文字，例如在菜单或对话框中出现的文字样式举例： “单击 **Next** 按钮进入下一个屏幕”。

> ![注记](img/note.png)
> 
> 警告或重要信息的样式。
> 
> ![提示](img/tip.png)
> 
> 技巧和窍门的样式。

# 读者反馈

### 读者反馈

Feedback from our readers is always welcome. Let us know what you think about this book?—?what you liked or may have disliked. Reader feedback is important for us to develop titles that you really get the most out of.

To send us general feedback, simply send an e-mail to feedback@packtpub.com, and mention the book title via the subject of your message.

If there is a book that you need and would like to see us publish, please send us a note in the **SUGGEST A TITLE** form on www.packtpub.com or e-mail suggest@packtpub.com.

If there is a topic that you have expertise in and you are interested in either writing or contributing to a book, see our author guide on www.packtpub.com/authors.

# 客户支持

### 客户支持

Now that you are the proud owner of a Packt book, we have a number of things to help you to get the most from your purchase.

# 下载案例代码

### 下载案例代码

You can download the example code files for all Packt books you have purchased from your account at [`www.PacktPub.com`](http://www.PacktPub.com). If you purchased this book elsewhere, you can visit [`www.PacktPub.com/support`](http://www.PacktPub.com/support) and register to have the files e-mailed directly to you.

# 勘误表

### 勘误表

Although we have taken every care to ensure the accuracy of our content, mistakes do happen. If you find a mistake in one of our books?—?maybe a mistake in the text or the code?—?we would be grateful if you would report this to us. By doing so, you can save other readers from frustration and help us improve subsequent versions of this book. If you find any errata, please report them by visiting [`www.packtpub.com/support`](http://www.packtpub.com/support), selecting your book, clicking on the **errata submission form** link, and entering the details of your errata. Once your errata are verified, your submission will be accepted and the errata will be uploaded on our website, or added to any list of existing errata, under the Errata section of that title. Any existing errata can be viewed by selecting your title from [`www.packtpub.com/support`](http://www.packtpub.com/support).