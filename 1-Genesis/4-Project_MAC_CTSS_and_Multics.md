# MAC项目：CTSS和Multics 

MAC项目是1963年春天由J.C.R. Licklider建议在MIT发起的。他的创始主任是MIT的教授Robert M. Fano。根据1965年Fano为MAC项目进度报告写的前言，MAC代表机器辅助认知(Machine Aided Cognition)和多路访问计算机(Multiple Access Computer)。事实上，它之所以有名是因为MIT计算机科学所在的科技广场五楼。Marvin Minsky的人工智能实验室位于被称之为人与计算机(Man and Computer)的九楼(最初实验室是属于Minsky和MacCarthy的，但当LISP的发明人John MacCarthy去了斯坦福后，他爱的名字被取消了)。

1963年MAC项目主办了一个暑期课程。许多知名的的计算机科学家被带到剑桥，他们使用IBM的使用CTSS(the Compatible Timeshare System，兼容分时系统)并讨论计算的未来。MAC项目这时主要的成就是Fernando J. Corbato的CTSS，Victor H. Yngve的COMIT，还有Minsky的人工智能实验室。

在50年代和60年代早期是批处理的时代。但这既浪费时间又浪费资源。桌椅浪费是因为机房里无所不在的签名表。除非你很幸运，刚排队没多久就就让你运行一个像debug这样预约时间为一小时小任务。你的程序运行了40分钟，或者不幸的，你的程序一小时后还没有完成：它将被直接丢弃(已经完成的部分很可能就完全丢掉了)。然后你又要将来的一个半小时(通常在下午的1点，2点或者3点)。解决这个问题的答案是分时。

兼容分时系统(CTSS)是第一个分时系统，它是由Corbato带领团队在MIT计算中心开发的。CTSS运行经过修改的的IBM 7094，它通过添加两块IBM 720A增加了32K字节存储。另一台7904在1965年早期加入进来。通过一台连接到拨号调制解调器的IBM 7750会话控制器，它最高可以让30哥用户通过电话线远程访问(事实上没有人可以拥有一个小时的CPU时间，因为那已经超出了系统失败的时间上限)。

CTSS作为MAC项目的分时部分，既是一台服务设备，又是系统编程员的实验室。这是这个附加功能(当时7094还在调整)导致了Multics的诞生(Multiplexed Information and Computing Service，多路复用信息和计算服务)。

Multics是第二代分时系统，目的是成为一个“计算机公用程序”的原型。它在1964年作为MAC项目，贝尔实验室，以及通用电气的合作项目开始进行。Corbato是开发计划的主要领导人，项目有九个主要目标：

> * 方便的使用远程终端
* 像电话系统一样的连续运行
* 广泛的系统配置
* 可靠的内部文件系统
* 支持选择性的信息分享
* 层次结构的信息分类
* 支持大量的应用程序
* 支持多个环境和接口
* 系统进化的能力

Berkley Tague在1962年加入贝尔实验室，又于1965年作为项目三人组的秘书加入Multics项目组。他说在1967年就可以很明显的看出项目不会成功，因为“三个成员有着互相冲突的目的”。他去新泽西惠帕尼的AT&T工作了三年，在那里他工作于一个防护项目。1970年又重新回到纽约默里山。

MIT的Jack Dennis教授在Multics早期贡献了几个很有影响的架构建议。当需要寻找一个计算机厂商支持新的操作系统时，人们说IBM将要生产叫做360/65的机器。Doug McIlroy告诉我：

> 这是真的，但是Amdahl不会制造虚拟机。最后时刻IBM让Gerry Blaauw主导360/67，但是为时已晚。

IBM的员工对MAC项目组关于分页的主意不感兴趣。那时还是MIT讲师的Joseph Weizenbaum向在通用电气的前同事们介绍了MAC项目组，前同事们对于分段分页机制非常热心，在他们的提议下产生了GE-645(635的升级版本)。就这样通用电气成为Multics项目的一部分。

MIT，贝尔实验室和通用电气一致同意合作。分别来自三个公司的三个人人组成了三人决策组，他们是MIT的Fano，贝尔实验室的E.E.David，和通用电气的C.W.Dix。还有三个人负责具体的实际管理，分别是MIT的Corbato，通用电气的A.L.Dean，贝尔实验室的Peter G.Neumann。值得注意的特性包括分段内存，虚拟内存，高级语言(PL/I)，多处理器共享内存，多语言支持，还有在线配置。

1964年PL/I被选为编程语言。其他候选的还有MAD(the Michigan Algorithm Display)和AED-0(an MIT display)。实现完整的PL/I比预料的还要困难。贝尔实验室和两个外部人员签订了奖励协议。但是一年过去了，两人没有拿出一个PL/I编译器。Bob Morris和Doug McIlroy制定了一个备用计划，在7094上使用McClure的TMG语言，这个语言也被称为EPL(早期PL/I)。McIlroy回忆道：

> 1965年5月3号，我们突然发现协议无法按时完成，马上就就开始自己建造它。我们在年前一段时间就有顾客。Morris的66到67年的学术休假被完整的使用了。我们雇佣的签约人员没有做出任何有价值的东西。所以EPL一直被推迟到1970年通用电气一个精湛的团队做出真正的编译器。

> Morris编写了TMG的前端，它输出单路ASCII代码。每个地址都注释着“基址，偏移，模式，精度”这些让人不知所云的东西。我用TMG语言做了代码生成器，它输出汇编语言。Dolores Leagus加入进来做数据结构编译。我们排除了占据PL/I一半语法的输入输出部分，单精度，属性声明，跨段序列，但实现了一个显著的子集，包括IBM早期版本性感的“引用”属性(“引用”使得序列的大小信息可以保留在数据结构的元素中)。

> Jim Gimpel加入进来负责数据封装。Multics有着种类繁多的数据结构，我们将一些三路代码加入的中间语言以消除很少使用的临时变量。编译器缺少某些功能，它只能输出“语法错误”和“多重声明”这两种错误提示，当数据越界时提示“非法数据结构”的警告。

> McClur将TMG的汇编代码从CDC 1600翻译为7090的编码格式，我在千里之外帮他调试。Clem Pease随后又通过将IBM指令定义为635宏将将它移植到GE 635。

编译器将编译结果送入EPLBSA(EPL引导汇编器)。编译过程非常缓慢。

等待PL/I编译器最终可用的时候，团队编写了Multics系统编程人员手册。它一共有3000页，每一节都经过几轮修订，还有几节重写或者大改了几次。

Tom Van Vleck说：

> 在68年到69年系统已经延期并且资金紧张有被取消的风险。或许这恰好鼓舞了团队精神(相比于表面的士气)。1968年ARPA(the Advanced  Research Proect Agency of the Department of Defense)的一次审查是我们最接近被取消的时候，不过他们建议我们继续下去。但为时已晚，贝尔实验室在1969年四月正式退出。

直到1993年仍有Multics机器在运行，它们是稀有物种。Van Vleck像我提供了下面的清单，标记型号的是未能确认的站点：

> ACTC (加拿大 亚伯达 卡尔加里)
Air Force Data Service (华盛顿哥伦比亚特区) *
Bull System-M (亚利桑那州凤凰城)
Credit Lyonnais (发过巴黎)
Department of National Defence (加拿大 新斯科舍省 哈里法克斯)
Ford Motor Company (密歇根州 迪尔伯恩)
General Motors(密歇根州 沃伦)
Ministerie van Sociale Zaken en Werkgelegenheid (荷兰 海牙) *
National Security Agency (马里兰州 林西克姆)
Societe Europeenne de Propulsion (法国 弗农)




---
**译者注**

[Multics System Programmers' Manual](http://multicians.org/mspmtoc.html)
