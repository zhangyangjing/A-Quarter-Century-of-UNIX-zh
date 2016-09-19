# MAC项目：CTSS和Multics 

MAC项目是1963年春天由J.C.R. Licklider建议在MIT发起的。他的创始主任是MIT的教授Robert M. Fano。根据1965年Fano为MAC项目进度报告写的前言，MAC代表机器辅助认知(Machine Aided Cognition)和多路访问计算机(Multiple Access Computer)。事实上，它之所以有名是因为MIT计算机科学所在的科技广场五楼。Marvin Minsky的人工智能实验室位于被称之为人与计算机(Man and Computer)的九楼(最初实验室是属于Minsky和MacCarthy的，但当LISP的发明人John MacCarthy去了斯坦福后，他爱的名字被取消了)。

1963年MAC项目主办了一个暑期课程。许多知名的的计算机科学家被带到剑桥，他们使用IBM的使用CTSS(the Compatible Timeshare System，兼容分时系统)并讨论计算的未来。MAC项目这时主要的成就是Fernando J. Corbato的CTSS，Victor H. Yngve的COMIT，还有Minsky的人工智能实验室。

在50年代和60年代早期是批处理的时代。但这既浪费时间又浪费资源。桌椅浪费是因为机房里无所不在的签名表。除非你很幸运，刚排队没多久就就让你运行一个像debug这样预约时间为一小时小任务。你的程序运行了40分钟，或者不幸的，你的程序一小时后还没有完成：它将被直接丢弃(已经完成的部分很可能就完全丢掉了)。然后你又要将来的一个半小时(通常在下午的1点，2点或者3点)。解决这个问题的答案是分时。

兼容分时系统(CTSS)是第一个分时系统，它是由Corbato带领团队在MIT计算中心开发的。CTSS运行在增加了32K字节存储的IBM 7094。另一台7904在1965年早期加入进来。通过一台连接到拨号调制解调器的IBM 7750会话控制器，它最高可以让30哥用户通过电话线远程访问(事实上没有人可以拥有一个小时的CPU时间，因为那已经超出了系统失败的时间上限)。


