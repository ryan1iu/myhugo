---
title: "Neovim 与 LSP"
date: 2023-10-30T21:08:49+08:00
draft: true
---

LSP: Language Server Protocol，语言服务器协议。是由微软提出的开源协议。
以往，不同的IDE为不同的编程语言添加例如自动补全、跳转到定义、列出引用、悬停文档等功能需要付出巨大的努力，这些功能需要由Language Server来实现。不同的IDE工具通常都定义了不用的API来实现上述相同的功能，通过制定protocol来实现进程间的通信。
LSP的想法是标准化或统一化这些实现不同但功能相同的Language Server与IDE通信的协议，这样可以使得一个针对特定语言开发的Language Server 能够在不同的IDE中被使用。使得Language Server从针对特定IDE转向针对特定语言，也在一定程度上促进了Language Server的繁荣发展。


