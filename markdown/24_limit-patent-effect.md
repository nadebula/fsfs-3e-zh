# 保护软件领域免受专利限制

另请参阅我的文章“专利改革并不足够”，位于<https://gnu.org/philosophy/patent-reform-is-not-enough.html>。

专利会对每一位软件开发者构成威胁，我们长久以来一直担忧的专利战争终于打响了。软件开发者和软件用户——我们的社会中的大多数人——需要保证软件不受专利限制。

对我们构成威胁的那一类专利通常称为“软件专利”，但这个短语是带有误导性的。这些专利并非针对任何具体的程序。与之相反，每一项专利描述了某种实践上的想法，并且宣称试图实施这样的思想的任何人将会被起诉。因此，将它们称为“计算思想专利”更为清楚。

美国专利体系并不会为每一项专利贴标签，称这项专利属于“软件专利”而那项不属于。是由软件开发者来区分那些将会对我们构成威胁的专利——那些覆盖了可能在软件中实施的想法的专利——以及其他的专利。例如，如果一项具有专利的想法是关于物理结构或者化学反应的，没有程序可以实现那种想法；这项专利并不对软件领域构成威胁。但是，如果一项具有专利的想法是一种计算，那么该专利的炮筒是对准软件开发者和用户的。

这并不意味着计算思想专利仅仅会禁止软件。这些想法也可以被实施在硬件中——并且它们中的很多已经被实施在硬件中。每项专利通常同时覆盖关于某种想法的硬件**和**软件实现。

## 关于软件的特别问题

软件领域仍然是计算思想专利将会造成特别的问题的地方。在软件中，在一个程序中同时实施数千种想法是很容易做到的。如果它们中的 10% 具有专利，这意味着该程序受到数百项专利的威胁。

当供职于公共专利基金会（PUBPAT）的 Dan Ravicher 于 2004 年对一款大型软件（Linux，即 GNU/Linux 操作系统的内核）进行研究时，发现了 283 项美国专利看起来可能覆盖了该程序的源代码中实施的计算思想。同年，一家杂志预计 Linux 约占整个 GNU/Linux 操作系统的 0.25%。将 300 乘以 400，我们可以得到这样的数量级估计，即该系统作为一个整体正在**受到大约 10 万项专利的威胁**。

如果那些专利中的半数由于“品质不良”——即由于专利体系本身的错误——而被判无效，这并不能真正带来改观。不论是 10 万项专利还是 5 万项专利，都是同样的灾难。这是为什么将我们对于软件专利的批判局限于“专利流氓”或者“劣质专利”是一种错误的原因。当今最坏的专利侵略者是苹果，它不仅仅是通常定义上的“专利流氓”；我不清楚苹果的专利是否属于“优质”，但是那些专利的“质量”越好，其所带来的威胁就越大。

我们需要解决全部的问题，而非部分。

关于在立法层面解决这一问题的常见建议包括修改专利授予的判据——例如，禁止为关于计算实践以及实现它们的系统授予专利。这种方式有两个明显的缺陷。

其一，专利律师精于变换专利的表达方式，使其能够适合规则所能适用的任何东西；他们将任何旨在限制专利实质的尝试化解为仅仅是形式上的要求。例如，美国的很多计算思想专利描述了这样一种系统，它包括一个算术单元、一个指令顺序器、一块内存，再加上用于执行特定计算的控制器。这是对于一台计算机运行一个程序以进行某种计算的一种古怪描述；它是被设计为使得专利申请满足美国专利体系据信在一段时间内所要求的判据的。

其二，美国已经有了数千项计算思想专利，更改判据以阻止批准更多专利并不能摆脱已有的那些。我们不得不等上将近 20 年，才能等到这一问题通过那些专利过期而彻底解决。我们可以展望立法废除那些现存的专利，但是这很可能不符合宪法。（美国最高法院不顾一切地坚称国会有权以牺牲公众权利为代价延伸私人特权，而不是相反。）

## 另一种方式：限制专利的效果，而非专利的可获得性

我的建议是改变专利的**效果**。我们应当立法规定，在通用计算硬件上开发、分发、运行程序并不构成专利侵权。这种方式有几个好处：

* 不再需要区分专利或者专利申请到底属于“软件”还是“非软件”；
* 可以对开发者和用户提供保护，不论是针对现存的还是未来潜在的计算思想专利；
* 专利律师不能通过以不同方式编写专利申请来挫败这种有意而为的效果。

这种方式并不会使现存的计算思想专利完全失效，因为它们仍然可以被应用于基于特殊目的硬件的实现。这是一种好处，由于它消除了关于这一计划在法律上的有效性的争论。几年之前，美国曾经通过一项法律，保护外科医生不受专利起诉，因此即使一些外科手术流程具有专利，外科医生仍然是安全的。这样的实践为这种解决方案提供了先例。

软件开发者和软件用户需要保护以免受专利限制。这是唯一能够提供对所有人的全面保护的法律解决方案。然后我们可以回到竞争或者合作……无需担忧某些陌生人会抹除我们的工作成果。

著作权所有 (C) 2012, 2013 自由软件基金会

本文的某个版本最初以“既然我们不能消灭软件专利，让我们限制它的效果”为题发表于 _Wired_ 网站（_Wired_，2012 年十一月 1 日，<https://wired.com/opinion/2012/11/richard-stallman-software-patents/>）。本文于 2012 年发表于<https://gnu.org>。此版本是“自由软件，自由社会：Richard M. Stallman 文选，第三版”（波士顿：GNU Press，2015）的一部分。

本文基于知识共享：署名——禁止演绎（CC BY-ND）4.0 国际版许可证（<https://creativecommons.org/licenses/by-nd/4.0/>）。

[返回目录](00_index.html)

