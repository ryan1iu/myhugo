---
title: (深入理解JVM) 使用Neovim搭配Clangd阅读和调试jdk12源码
date: 2023-11-08T00:00:00.000Z
draft: false
tags:
  - java
  - jvm
  - neovim
  - clangd
---
这里是《深入理解jvm》读书笔记，本文记录了我使用neovim并使用clangd作为LSP server来搭建优雅的阅读和调试jdk12源码的方式。

在默认情况下，clangd不能很好的工作，原因是无法识别include的头文件，通过查阅相关资料可知，clangd使用`compile_commands.json`数据库文件来包含项目中文件的flag。

最初我通过使用书中所提到的CMakeLists.txt来使用cmake生成该文件，具体过程参考该[文章链接](https://gist.github.com/Strus/042a92a00070a943053006bf46912ae9)，但是未能成功。

在搜索过程中发现openjdk官网有一篇名为[IDE support in the JDK](https://hg.openjdk.org/jdk/jdk/raw-file/tip/doc/ide.html)的文章，其中提到`The make system can generate generic native code indexing support in the form of a Compilation Database that can be used by many different IDEs and source code indexers.`，因此只需要运行`make compile-commands`命令即可生成该文件，最后把生成的文件复制到项目根目录即可。

效果如下图所示，非常丝滑。
![image](https://imgse.com/i/pi17okQ)




