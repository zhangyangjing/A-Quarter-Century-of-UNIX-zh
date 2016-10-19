# 伯克利Unix 第二部分

1978年早期，Richard Fateman教授开始寻找一个有更大内存寻址空间的机器，这样就能在PDP-10上继续做他的Macsyma。Fateman解释说:

> MIT有一个MAC项目，它的程序叫做MACSYMA。为了和VAX只最初只能PDP-10上运行的那个同名项目区分开，我就叫它VAX/Macsyma，有时也会说成vaxima。MIT后来将Macsyma卖了出去，从它的名字也可以看出来，它被卖给了Symbolics公司。接下来所有的后续版本都不被Symbolics所控制，也不被再接下来的所有者马萨诸塞州阿灵顿的Macsyma公司控制，这些版本被称为和Macsyma不一样的名字:

> DOE-Macsyma —— (能源部的版本)
> Paramax —— (Paradigm Associates)
> Maxims —— (德克萨斯州立大学Bill Schelter移植的通用Lisp版本)
> Aljabr —— (Jim O’Dell开发的Macintosh版本)

> 所有这些分支版本在本质上都和vaxima差不多，虽然它们的支持者都声称自己选择了最好的。

不管怎么说，新的DEC VAX 11/780机器看起来符合Fateman的需求，而且Fateman关于NSF的提议和其他13位教员的建议一起得到了部门基金。最初VAX运行的是DEC的VMS操作系统。

但是部门开始变得习惯使用Unix，并且Fabry得到了一份Unix 32V移植到VAX的拷贝，这是霍姆德尔贝尔实验室的John Reiser和Tom London开发的。移植项目的主管是Charlie Roberts，这些是他回忆的那段故事:

> 77年到78年DEC提前宣布了VAX。Dennis和Ken还有Steve和DEC公司变得相当疏远。他们觉得自己的工作已经安装在很多的机器上，DEC仍然拒绝支持Unix并且继续开发VMS。所以当DEC提供给他们一台VAX的时候，他们拒绝了(Doug McIlroy告诉我他们拒绝的另一个原因是“VAX使用让人非常厌烦的复杂指令集，这于Ken和Dennis的价值观非常不一致”)。之后Dennis和Steve为移植到Interdata上工作，Steve称它为“Intersnial”。


