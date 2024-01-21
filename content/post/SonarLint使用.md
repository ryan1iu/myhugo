---
title: SonarLint使用指南
draft: false
date: 2024-01-19T00:00:00.000Z
---
# 安装
在IDEA插件商店搜索sonarlint,找到下图所示插件，安装即可，后续可通过右键找到并打开

![](https://imagebed-1300955178.cos.ap-beijing.myqcloud.com/202312061006149.png)

# 基本概念
## Clean Code attribute（干净代码属性)
>有助于编写整洁代码的特征，被分为四类：consistent（一致性）、intentional(有意义)、adaptable(可适应)、responsible（负责任).
- consistent 一致性
	- formatted 格式化：代码呈现具有系统性和规律性。非语义选择，如间距、缩进和字符放置，在整个代码库中保持一致，确保在文件和作者之间保持统一性。
	- conventional 符合规范：代码执行任务的方式符合预期的指令。面对同样好的选择时，代码在所有实例中坚持选择一种，优先使用语言规范。这包括使用适当的编程接口和语言特性。
	- identifiable 可识别：标识符遵循基于语言规范的规律结构。标识符中使用的大小写、词分隔符、后缀和前缀具有目的，没有任意差异。
- intentional 有意义
	- clear 清晰，自说明的
	- logical 没有矛盾的、不可预测的逻辑
	- complete 是全面的，被充分而适当地使用
	- efficient 在没有不必要浪费的情况下利用资源
- adaptable 可适应，代码结构易于演进和拓展
- responsible 负责任，合法的、值得信赖的
## Software qualities 软件质量
> 整洁的代码会导致安全、可靠和可维护的软件。在Sonar解决方案中，这三个方面被称为软件质量，它们有助于提高软件的长期价值。
   当在代码中检测到问题时，它会对这三个软件质量中的一个或多个产生不同程度的影响。影响的程度决定了问题的严重程度，可以是高、中或低。

![](https://imagebed-1300955178.cos.ap-beijing.myqcloud.com/202312060942199.png)
## 结合上述概念理解IDEA中的issues
SonarLint会按照问题的严重程度进行排序，对于一个特定的问题，sonarlint会给出该问题所存在的违反干净代码准则的原因和影响软件质量的严重程度

![](https://imagebed-1300955178.cos.ap-beijing.myqcloud.com/202312060956722.png)

## 进一步了解
上面是一些基本的操作，想要进一步发挥插件的能力，可以查看官方说明文档https://docs.sonarsource.com/sonarlint/intellij/usingsonarlint/investigating-issues/


