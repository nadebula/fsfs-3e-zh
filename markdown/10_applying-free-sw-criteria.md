# 应用自由软件判据

四项基本自由为判断某一特定代码片断是否为自由的（即尊重用户自由）提供了判据。[^1]我们应当如何将它们应用于判断软件包、操作系统、计算机、或是网页是否适合被推荐使用呢？

一个程序是否是自由的首先影响到的是我们对于自己的私人行为的决定：为了捍卫我们的自由，我们需要拒绝那些将会剥夺我们的自由的程序。然而，这也会影响到我们应当对别人怎样说和怎样做。

非自由程序是一种不公。发布非自由程序、向他人推荐非自由程序、或是更为普遍地将它们引入课程以诱导人们使用非自由软件，这些行为意味着引导人们放弃自己的自由。可以肯定的是，引导人们使用非自由软件并不等同于在他们的计算机上安装非自由软件，但我们不应该将人们引入歧途。

在更深层次上，我们必须拒绝将非自由软件呈现为一种解决方案，由于这将会赋予其合法性。非自由软件是一种问题；将其呈现为一种解决方案的做法否认了这一问题的存在。[^2]

本文解释了我们应当如何应用自由软件的基本判据以判断不同种类的事物，由此我们就能决定是否应该推荐它们。

## 软件包

一个软件包若要成为自由的，其中所有代码都必须是自由的。但这不仅限于代码。由于文档文件包含手册、自述、更新日志等，这些都是软件包的必要的技术组成部分，它们必须也是自由的。[^3]一个软件包通常与众多其他软件包一起使用，并且与其中的一些进行交互。与非自由软件进行的何种交互才是伦理上可接受的呢？

我们着手开发 GNU 的目的是带来一款自由的操作系统，由于在 1983 年还没有这样的自由操作系统。当我们于 20 世纪 80 年代开发出最初的 GNU 组件时，其中每个组件都依赖非自由软件是不可避免的。例如，没有任何一个 C 程序可以离开非自由 C 编译器而运行，直到 GCC 可以正常工作，并且它们也不能离开 Unix libc 而运行，直到 glibc 可以正常工作。每个组件都只能运行在非自由操作系统上，由于当时所有操作系统都是非自由的。

每当我们发布一款可以运行在某些非自由操作系统上的组件，用户将其移植到其他非自由操作系统上。从伦理上讲，这些移植并不比我们开发这些组件所需的平台限定的代码更坏，因此我们整合了他们的修补程序。

当 Linux 内核于 1992 年成为自由的之时，它填补了 GNU 操作系统的最后一块空缺。（Linux 最初于 1991 年以一种非自由许可证发布。）GNU 和 Linux 的组合成为了一种完全自由的操作系统——GNU/Linux。[^4]

此时，我们可以选择移除对于非自由平台的支持，但是我们决定不如此做。非自由操作系统是一种不公，但是用户运行非自由操作系统并不是我们的过错。支持该非自由操作系统上的自由软件并不构成这种不公。并且这将会是有用的，不仅仅是对于那些系统的用户，对于吸引更多人为开发该自由软件做贡献也是如此。

然而，在自由操作系统上运行的非自由软件则是一个完全不同的问题，由于这是在诱导用户在自由之路上倒退。在某些情况下我们完全禁止如此做：例如 GCC 禁止任何非自由插件。[^5]如果一个程序允许非自由的扩展，它至少不应该引导用户使用它们。例如，我们更倾向于选择 LibreOffice 而非 OpenOffice，由于后者提示用户使用非自由扩展，而 LibreOffice 则拒绝它们。我们开发冰猫（IceCat）[^6]起初也是为了避免向用户推广由火狐（FireFox）建议使用的非自由扩展。

事实上，如果冰猫解释如何在 MacOS 上运行冰猫，这将不会引导用户去运行 MacOS。但是如果它介绍了一些非自由扩展，它将会鼓励冰猫用户安装这些非自由扩展。因此，冰猫软件包及其手册和网站不应该介绍这些东西。

有时，一个自由软件和一个非自由软件协同工作，但是其中任何一方都不是基于另一方的。我们针对这种情况的规则是，如果该非自由软件非常有名，我们应当告知人们如何使用我们的自由软件与之共同工作；但是如果该非自由软件鲜为人知，我们不应该暗示其存在。有时我们会在该非自由软件已被安装的情况下提供互操作支持，但避免告知用户如此做的可能性。

我们拒绝任何仅可用于某种非自由操作系统的“增强组件”。它们会鼓励人们使用该非自由操作系统而非 GNU，如同自摆乌龙。

## GNU/Linux 发行版

随着 Linux 于 1992 年成为自由的，人们开始开发 GNU/Linux 发行版（distro）。只有少数发行版是完全由自由软件构成的。

适用于软件包的规则也适用于发行版：一个符合伦理的发行版必须仅仅包含自由软件并且只将用户导向自由软件的方向。但是，对于发行版而言，“包含”某个特定软件包是什么意思呢？

某些发行版通过作为其发行版的一部分的二进制包安装软件；而其他发行版从上游源代码构建每个软件，并且从字面意义上讲，它们所**包含**的只是需要下载并构建的列表。对于自由的问题，发行版怎样安装一个给定的软件包并不重要；如果它将某个软件包作为可选项而提供，或者它的网站如此做，我们称该发行版“包含”该软件包。

自由操作系统的用户拥有对它的控制权，于是他们可以安装他们想要安装的任何东西。自由发行版提供了用户可用于安装他们自己的程序以及他们对于自由软件的修改版本的通用工具；他们也可以安装非自由软件。在这些发行版中提供这些通用工具并不是伦理瑕疵，由于该发行版的开发者对于用户基于其自身的主动性获取并安装什么软件并不负有责任。

然而，当开发者引导用户朝向非自由软件的时候，他们对于用户安装非自由软件的行为就负有责任了——例如，将其置于该发行版的软件包列表中，或者从它们的服务器进行分发，或者将其呈现为一种解决方案而非一种问题。这正是为何大多数 GNU/Linux 发行版具有伦理瑕疵的问题之所在。

自行安装软件包的用户通常具有一定水平的技能：如果我们告诉他们“Baby 包含非自由代码，而 Gbaby 是自由的”，我们可以期望他们能够留心记住哪个是哪个。但是，发行版是推荐给那些不会记住这些细节的普通用户的。他们将会想，“我应该使用他们所说的哪一个呢？我想它应该是 Baby”。

因此，要想向公众推荐一款发行版，我们坚持要求它们的名字不能与我们所拒绝的某个发行版相似，唯有如此，我们关于仅仅推荐自由发行版的信息才能被可靠地传达。

发行版和软件包之间的另一个区别在于向其中添加非自由代码的可能性。程序开发者会仔细检查他们向其中添加的代码。如果他们决定使该程序成为自由的，他们不太会向其中添加非自由代码。不过也有例外，包括向 Linux 内核中添加“二进制 blob”这样的极其恶劣的案例，但是它们与现存的自由软件相比只占一小部分。

与之相反，一个 GNU/Linux 发行版通常包含数千个软件包，并且其开发者可能每年都会向其中添加数百个新的软件包。如果未能尽力避免那些包含某种非自由软件的包，肯定会有一些非自由软件混入其中。由于自由发行版的数量很少，作为列出这些发行版的条件，我们要求自由发行版的每一位开发者都承诺保持该发行版成为自由软件，通过移除任何非自由代码或恶意软件。参见 GNU 自由操作系统发行版指导意见，它位于<https://gnu.org/distros/free-system-distribution-guidelines.html>。

我们不要求自由软件包的开发者也做出这样的承诺，这是不现实的，而幸运的是，这也不是必需的。得到超过 3 万个自由软件的开发者的关于保持其自由的承诺将会避免少数问题，但是其代价是极大地增加自由软件基金会（FSF）员工的工作量；此外，这些开发者中的大部分与 GNU 计划并无关系，可能也没有关于向我们作出任何承诺的兴趣。因此我们只需在发现问题的时候应对这些使自由软件变为非自由软件的少数案例。

## 外设

计算机外设要求计算机中的软件被操作系统加载到其中以使其工作——这些软件可以是驱动程序或者固件。因此，一件外设是可被接受以供使用和推荐的，如果它可以在一台未安装任何非自由软件的计算机上使用——如果该外设的驱动程序以及任何需要由操作系统加载到其中的固件都是自由的。

验证这一点是简单的：将该外设连接到一台运行完全自由的 GNU/Linux 发行版的计算机上并且观察它是否正常工作。但是大多数用户想要在购买外设**之前**获知这一点，因此我们在 [h-node.org](https://h-node.org) 列出了关于众多外设的信息，这是一个用于完全自由的操作系统的硬件数据库。

## 计算机

一台计算机在不同的层次上包含不同的软件。我们应当基于什么判据来确定一台计算机是否“尊重您的自由”呢？

显而易见的是，操作系统及其上的任何东西都必须是自由的。在 20 世纪 90 年代，引导程序（当时是基本输入/输出系统，BIOS）成为可替换的，并且由于它运行在中央处理器（CPU）上，它与操作系统所存在的是同一类的问题。因此，诸如不论是安装在操作系统中还是随操作系统一起安装的固件和驱动程序等软件，或是引导程序等等都必须是自由的。

如果一台计算机拥有某些要求在操作系统中安装非自由驱动程序或者固件的硬件特性，我们可能仍然能够推荐它。如果它在没有那些特性的情况下仍然可用，并且我们认为大部分人不会为了使得该特性可用而被引导安装非自由软件，那么我们仍然能够推荐它们。否则我们就不能。这将是一种主观判断。

一台计算机可能在较低的层级上带有预装的可修改的固件和微码。它也可能在真正的只读存储器中拥有代码。我们决定在我们今天所使用的认证判据中忽略这些程序，如若不然就没有任何计算机可以满足，这也是由于不会被常规地更改的固件在伦理上与电路相同。因此我们的认证判据仅仅覆盖那些运行在计算机的主处理器上而非真正的只读存储器中的代码。如果并且随着其他处理层级上的自由软件成为可能，我们也会要求这些层级上的软件是自由的。

由于认证一款产品是对它的积极推广，我们要求它们的贩卖者以支持我们作为回报，这可以通过谈论自由软件而非“开源”[^7]以及将 GNU 和 Linux 的结合体称为“GNU/Linux”[^8]来做到。我们没有义务积极推广那些不认可我们的工作或是不支持我们的运动的项目。

参见<https://www.fsf.org/resources/hw/endorsement/criteria>以获知我们的认证判据。

## 网页

现在，很多网页包含复杂的 JavaScript 程序并且需要它们才能工作。这是一种恶劣的实践，由于它阻碍了用户对他们自己的计算的控制。更进一步地，这些程序中的大部分是非自由的，是一种不公。JavaScript 代码通常窥探用户。[^9] JavaScript 已经变成了一种对用户自由的攻击。

为了解决这一问题，我们开发了 LibreJS，这是一种用于阻止非平凡的非自由 JavaScript 代码的火狐浏览器扩展。（没有必要阻止简单的脚本，如果它们只是实现一些次要的用户界面修改。）我们请求网站使它们的 JavaScript 程序成为自由的，并且标记其许可证以便 LibreJS 识别。

与此同时，链接至一个包含非自由 JavaScript 程序的网页是否符合伦理呢？如果我们坚决不做任何妥协，我们将只能链接至自由的 JavaScript 代码。然而，很多网页即使不运行它们的 JavaScript 代码也能工作。并且，您遭遇非自由 JavaScript 代码的最通常的方式并非跟踪我们的链接；为了避免这些情况，您必须使用 LibreJS。因此，我们决定做出让步并且链接那些不运行非自由 JavaScript 程序也能工作的网页，同时鼓励用户在普遍意义上保护自己不受来自非自由 JavaScript 程序的威胁。

然而，如果某个网页若不运行非自由 JavaScript 代码就不能实现其功能，链接到它将会不可避免地要求人们运行该非自由 JavaScript 代码。我们在原则上不会链接到这些网页。

## 结论

将**软件应当是自由的**这一基本理念应用到不同的场合要求不同的实践策略。随着新情况的出现，GNU 计划和 FSF 将会适配我们的自由判据以便将计算机用户引向自由，不论是在实践上还是在原则上。通过仅仅推荐尊重自由的程序、发行版和硬件产品，并且宣示您的策略，您可以为自由软件运动提供它所急需的支持。

[^1]: 参见“什么是自由软件”以获知自由软件的完整定义。

[^2]: 作者的文章“避免破坏性的妥协”详细论述了这一问题。

[^3]: 参见“自由软件需要自由文档”以获知关于这一问题的更多细节。

[^4]: 参见“Linux 和 GNU 系统”一文以获知更多信息。

[^5]: 如需获知为何 GCC 拒绝任何非自由插件，参见作者在 GCC 邮件列表中的回复，它位于<https://gcc.gnu.org/ml/gcc/2014-01/msg00247.html>。

[^6]: 参见<https://directory.fsf.org/wiki/IceCat>。

[^7]: 参见“自由软件在今天更加重要”和“为何开源错失自由软件的关键”。

[^8]: 参见“命名的涵义”。

[^9]: 参见“JavaScript 陷阱”。

著作权所有 (C) 2015 Richard Stallman

本文是“自由软件，自由社会：Richard M. Stallman 文选，第三版”（波士顿：GNU Press，2015）的一部分。

本文基于知识共享：署名——禁止演绎（CC BY-ND）4.0 国际版许可证（<https://creativecommons.org/licenses/by-nd/4.0/>）。

[返回目录](00_index.html)

