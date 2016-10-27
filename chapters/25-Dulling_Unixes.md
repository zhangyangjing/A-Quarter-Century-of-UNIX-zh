# Unix间的竞争

直到1978年，Unix都意味着AT&T的操作系统。随着PWB 2.0，V7，32V，和3BSD的出现，它加入了更多东西。但是Unix不只是AT&T的产品，它是一个“电话通讯支持工具”。因为和解协AT&T议被迫离开计算机商业，不允许继续在计算机市场参与竞争。没有了AT&T的支持，Unix的未来命运从科研界转手到了Unix支持小组(USG)。USG在70年代大部分时间掌握着Unix的命运，然后到了1979年，微软和圣克鲁斯操作公司(SCO)推出了XENIX2，伯克利推出了4BSD，这两个系统都是V7的衍生版本。XENIX是Unix针对Intel 8086和其他很多硬件架构的第一个移植版本。虽然它变得和其他版本不再兼容，但它也是一个非常流行的版本。自由软件基金会的Len Tower向我评论说“SCO Unix用起来就像是在向前穿越时间”。

正如Andy Tannenbaum指出的，“贝尔实验室有一个Unix支持小组，但是你从没听说过Unix开发小组。这是因为贝尔公司没有权限开发计算机操作系统...”。1981年Jeff Schriebman创建的UniSoft推出了一个名为UniPlus+的移植版本，它与System III和现在的System V保持兼容。1983年伯克利的一个小组成立了mt Xinu来支持和商业化BSD，其中的成员有Bob Kridle，Alan Tobey，Ed Gould，还有Vance Vaughan。Debbie Scherrer不久后也加入了他们。他们先是销售了更多的4.2BSD，然后是4.3BSD(mt Xinu擅长于客户服务:1986年Debbie自己安装了我的4.3纸带)。

5年的时间中，Apollo，DEC，Eakins，Gould，Integrated Solutions，Masscomp，mt Xinu，NSC，和Wollongong是众多Unix销售公司中的一部分。这些销售AT&T System III或者System V衍生版本的公司有:AT&T，Altos，Apollo，Compaq，Convergent，HP，Honeywell，IBM，ITT，Intel，Interactive，Masscomp，Microport，Microsoft，Motorola，NCR，NUXI，Opus，SCO，Silicon Graphics，Sperry，Sun，Tandy，UniSoft，Wollongong。此外，Amdahl，Apollo，Apple，Cray，DEC，Data General，HP，IBM，Inter，Motorola，Unisys和许多其他的公司提供私有的Unix版本，其中一部分是基于4.2BSD的。

所有的这些版本，不管是AT&T还是BSD的衍生版本，都需要AT&T的授权。最近几个Unix的版本可以不需要这种授权。虽然没有一个商业产品是真正强健的，但BSDI，386/BSD，还有NetBSD都已经可以在任何386/486机器上运行。这些“自由授权”版本都衍生自自由的CSRG发行版，当我写这些的时候它仍然在诉讼中。详细信息可以参见29章。Linus Torvalds写的Linux也运行在386/486机器上，不过没有使用CSRG的代码。这四个系统都使用了大量自由软件基金会的软件。Ritchard M. Stallman创建了自由软件基金会，并为他几近完成的GNU系统写了那些软件。GNU软件包括大多数Unix软件可以自由分发的重制版本(它们在GNU项目中一个叫做‘copyleft’的授权下发行，这意味着原始和改进后的版本必须可以让其他人自由修改和分发源码。如果发布了二进制版本，源码也必须一起发布出来)。**gcc**是GNU的C语言编译器，可能是Steve Johnson的pcc最好的继任者。

最终，这些衍生和克隆版本可以运行在一系列的处理器上:DEC，Intel，MIPS，Motorola，NSC，更多的就不再一一列出。

