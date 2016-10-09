# 实用工具

每个Unix机器上都安装着数目繁多的程序，不管是系统原生的还是厂商附加的。这其中包括编辑器，格式器，编译器。实用工具使得用户有一个字母列表跟踪程序或者文档的不同版本，去“伸手戳一下”其他用户。这章将用来讲述它们中的一部分:非常早期的——troff，eqn，tbl，yacc，mail，make，awk，还有最近出现的——UUCP，TCP/IP。最后两个又引发了其他的实用工具(Mike Muuss的ping和Earl Cohen的finger就是很好的例子)，并且几乎立即就出现了一个世界范围的由各种不同用户组成的社区。这个社区对Unix来时及其重要。各种问题，解决方案，程序，抱怨，宣告等等都在社区里自由的交换传送。整个社区建立在大约3000万到3500万的网络用户之上——就像John Quarterman所说的，比加拿大的总人口都要多。

mail和roff以及ed一样，在Unix第一版时就存在了。Morris曾经将roff移植到635上，McIlroy用BCPL语言将它重写。Thompson将它移植到了Unix。但Joe Ossanna不久又将roff合并到了troff，一个真正针对电传打字机文档的格式器。Ossanna死于1977年11月28，McIlroy告诉我:

> 
