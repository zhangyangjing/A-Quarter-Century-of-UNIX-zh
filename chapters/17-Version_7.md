# V7

Unix第7版在1979年6月由贝尔实验室发布，它有几个主要的提升:它可以使用更大的文件系统，不限制用户的数量，提高了可靠性。Steve Johnson将第7版称之为“第一个可移植的Unix”。这个版本具有极大的影响力因为它增加了很多新的命令。让我列举一部分:

|**命令**||
|:--|:--|
|at|awk|
|calendar|cb|
|cd|cpio|
|cu|deroff|
|expr|f77|
|find|lex|
|lint|m4|
|make|refer|
|sed|tail|
|tar|touch|
|uucp|uux|
|**系统调用**||
|ioctl||
|**子例程**||
|malloc|stdio|
|string||
|**游戏**||
|backgammon||

**awk**(Aho Weinberger Kernighan)，**lint**(Johnson)，**make**(Feldman)，以及**uucp**(Lesk)这几个就足够了，但是第7版远比这更多。

第7版的编程手册增加到了400页，还有两卷400页的附加补充。这个Unix中包含了一个完整的Kernighan和Richie C语言编译器，一个更加成熟的shell sh(Bourne Shell)，Dick Haight的find，cpio和expr，还有很多的包含头文件。

这些所有的放在一起，第7版Unix有了一个缺点:它的性能比大部分的第6版要低一些，特别是这些都已经经过“调优”。人们开始为改善这个问题而工作。伯克利的Bill Joy修改了VAX-11/780机器上Unix文件系统的的数据块大小，他的实现被Jeff Schriebman在1980年1月移植到PDP-11/70上面(他离开伯克利去了UniSoft)。1979年12月，那时还在伯克利的Ed Gould将缓冲区移出内核寻址空间。Joy修改了VAX上的*stdio*库，旧金山加利福尼亚大学的Tom Ferrin又将这个改动移植到了PDP-11。霍姆德尔的Tom London优化了用户空间到内核空间的字符移动。Ferrin还写了一个动态单一总线分配方案。新南威尔士大学的John Lions提议一个新的目录路径名命名规则，新南威尔士大学还提供了一个处理表格搜索的新代码。RAND公司的Bruce Borden提供了symorder程序。Ferrin还重写了`copyseg()`和`clearseg`的部分代码。所有这些来自社区的优化提升被收录到一个PDP-11发行版:2.8.1 BSD。1982年1月Ferrin在加利福尼亚州圣塔莫尼卡举办的USENIX会议上宣布了这个BSD的新版本。用户们因此大幅提高了第7版Unix的性能。

我在这里花费这么多的篇幅是因为第7版是来自工业和学术界，来自美国和澳大利亚。并且所有这些都包含进将来的BSD和AT&T Unix发布版。

第7版同时也在移植方面有所增强:32的XENIX2是第一个可以在8086芯片上运行的Unix(XENIX1是基于第6版)。第7版也可以运行在Z8000和68000芯片上。32V版本(来自Holmdel)则增强了3BSD和它所有的后续版本。

32位Unix的进化故事是Steve Johnson告诉我的:

> 我知道的第一个完整移植的Unix是普林斯顿大学的学生做的。他们移植了很大一部分Unix命令和系统的接口shell到IBM 360上。我想是TSS系统。他们令人惊奇的让Unix在那个系统上运行。他们使用了我们的知识和IBM C语言编译器，这是一件诱人的事情。那个夏天我们雇佣了这些学生中的一位，Tom Lyon，他移植第6版Unix所有的命令到Amdahl。

> 我记得当我们决定移植Unix。我们选择了Interdata。这是一段有趣的经历因为IBM将为我们提供2年半的360机器，但是Dennis不喜欢IBM的程序，他试着自己重写这些东西。
