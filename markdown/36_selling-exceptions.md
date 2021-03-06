# 关于 GNU GPL 的贩卖例外

> 贩卖许可证例外的实践成为了热门话题，当我联合签署知识生态国际（KEI）的信函，警告 Oracle 收购 MySQL（加上 Sun 的其余部分）对于 MySQL 来说可能不是好事的时候。

> 如同下文所解释的那样，我对于贩卖许可证例外的感受是混合的。显而易见的是，基于 GNU GPL 开发强大且复杂的软件包而不贩卖例外是可能的，并且我们如此做。MySQL 也可以通过这样的方式开发。然而，贩卖例外已经被 MySQL 开发者所应用。应该由谁决定是否继续如此做？我不认为将关于自由软件项目的重大决策托付给一家大型私有竞争者是明智的，它可能自然而然地使得该项目发展得更少而非更多。

> 一种完全没有意义的想法是将 MySQL 的许可证改为某种非左版。这将会消除贩卖例外的可能性，但是也会允许各种各样的私有修改版本。无论 MySQL 走向何方，其目的地都不应该是那里。

当我共同签署了反对 Oracle 收购 MySQL [^1]（以及 Sun 的其余部分）的计划的信函的时候，有些自由软件支持者对于我赞成 MySQL 开发者已经使用过的贩卖许可证例外的实践感到惊讶。他们以为我会完全谴责这种实践。本文解释了我对于这种实践的想法以及为何这样想。

贩卖例外指的是代码的版权持有人基于自由软件许可证将其发布给公众，然后允许客户付费以获得基于不同条款使用相同代码的许可，例如允许将其包含于私有应用软件之中。

我们必须将贩卖例外的实践同某些根本不同的东西区分开来：自由软件的完全私有扩展或者完全私有版本。这两种行为，即使是由一家公司同时实践，也是不同的问题。对于贩卖例外，适用例外的相同代码作为自由软件而对于公众可用。仅在私有许可证下可用的扩展或者修改版本是私有软件，并且不比任何其他私有软件好，简单直白。本文关注的是严格地涉及并且仅仅涉及贩卖例外的情况。

我自 20 世纪 90 年代始就将贩卖例外看作可接受的，并且有时我向公司如此建议。有时这种方法已经使得重要程序成为自由软件成为可能。

KDE 桌面于 20 世纪 90 年代基于 Qt 库开发。Qt 那时是私有软件，而 TrollTech 为将其嵌入私有应用软件中的许可收费。TrollTech 允许 Qt 在自由应用软件中的免费使用，但这并不会使其成为自由软件。因此完全自由的操作系统不能包括 Qt，于是也就不能使用 KDE。

在 1998 年，TrollTech 的管理人员认识到他们可以使得 Qt 成为自由软件，同时继续为将其嵌入私有软件的许可收费。我不记得此建议是否来自于我，但我确实乐于看到这个改变，这使得在自由软件世界中使用 Qt 以及由此使用 KDE 成为可能。

最初，他们使用自己的许可证，Q 公共许可证（QPL）——就自由软件许可证而言颇具限制性，并且与 GNU GPL 不兼容。其后，他们转到了 GNU GPL；我想我为他们解释了为何这可以达到此目的。

贩卖例外根本上依赖于为自由软件发布使用诸如 GNU GPL 等左版许可证。左版许可证允许将软件嵌入某个更大的程序，仅当整个合并的程序基于该许可证发布；这是它为何能够确保扩展版本同样自由的理由。因此，想要使得合并的程序成为私有的用户需要得到特定许可。只有版权持有人可以授予此种许可，而贩卖例外就是如此做的一种样式。基于 GNU GPL 或者其他左版许可证收到此代码的其他人不能授予例外。

当我首次听说贩卖例外的实践时，我问自己这种实践是否符合伦理。如果某人购买例外以便将某个程序嵌入更大的私有软件，此人正在作恶（具体地说，构建私有软件）。这是否能够得出结论，即贩卖例外的开发者也在作恶？

如果这种暗示是合理的，它也适用于基于诸如 X11 许可证等非左版自由软件许可证发布相同的程序。这也允许此类嵌入。因此，我们要么必须得出结论，即基于 X11 许可证发布任何东西都是错误的——这是一种我认为极端得不可接受的结论——要么拒绝这种暗示。使用非左版许可证是软弱的，并且通常是较坏的选择，但它并非错误。

换言之，贩卖例外允许有限制地将代码嵌入私有软件，但是 X11 许可证走得更远，允许代码（及其修改版本）在私有软件中的无限制使用。如果这并不使得 X11 许可证成为不可接受的，它也不会使得贩卖例外成为不可接受的。

FSF 不实践贩卖例外有三个原因。其一是它并不通往 FSF 的终极目标：确保我们的软件的每一位用户的自由。这是我们编写 GNU GPL 的目的，最为彻底地实现这一点的方法就是基于 GPL 版本 3 或者更新版本发布软件，并且不允许将其嵌入私有软件。贩卖例外不能实现这一点，正如基于 X11 许可证发布软件不能做到一样。因此我们通常不会做这两种事情之任何一者。我们仅仅基于 GPL 发布软件。

我们仅仅基于 GPL 发布软件的另一个原因是为了禁止那些相对于我们的自由软件呈现实践上的好处的私有扩展。那些不把自由看作价值的用户可能会选择非自由版本，而非它们所基于的自由版本——并且失去他们的自由。我们不想鼓励这种情况的发生。

但是偶尔会有这样的情况，在此，出于特殊的策略原因，我们确定为某个程序使用相对包容的许可证对于自由软件事业更为有利。在这些情况下，我们基于此相对包容的许可证对每个人发布此程序。

这是由于 FSF 所遵循的另一个伦理原则：无差别对待所有用户。为了实现自由的理想主义运动不应当歧视任何人，因此 FSF 献身于为所有用户提供同样的许可证。FSF 从不贩卖例外；我们所基于它或者它们发布程序的任何许可证，对于每一个人都可用。

但是我们不需要坚持要求商业公司也遵循此原则。我认为对于商业公司而言贩卖例外是可接受的事情，并且我将会在适当的时机将其提议为使得程序成为自由的一种方式。

[^1]: James Love 和 Malini Aisola（KEI），Richard Stallman（FSF），Jim Killock（开放权利集团），致 Neelie Kroes（欧洲联盟委员会竞争事务专员）函，2009 年十月 19 日，<https://keionline.org/sites/default/files/ec_letter_mysql_oct19.pdf>。

著作权所有 (C) 2009, 2010 Richard Stallman

本文的此版本是“自由软件，自由社会：Richard M. Stallman 文选，第三版”（波士顿：GNU Press，2015）的一部分。

本文基于知识共享：署名——禁止演绎（CC BY-ND）4.0 国际版许可证（<https://creativecommons.org/licenses/by-nd/4.0/>）。

[返回目录](00_index.html)

