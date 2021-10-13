# 自由硬件和自由硬件设计

> 自由软件思想在多大程度上延伸到硬件？使得我们的硬件设计成为自由的是否属于道德义务，正如使得我们的软件成为自由的那样？要想维护我们的自由是否需要拒绝生产自非自由设计的硬件？

## 定义

**自由软件**关乎自由而非价格；宽泛地说，这意味着用户可以自由地使用该软件，以及复制和再分发该软件，不论是否收取费用。更精确地说，其定义是根据四项基本自由而形成的[^1]。为了强调“free”指的是自由而非价格，我们经常将法语或者西班牙语的“libre”一词和“free”连用。

如果将同样的概念直接应用于硬件，则**自由硬件**指的是用户可以自由地使用以及复制和再分发，不论是否收取费用的硬件。然而除了钥匙、脱氧核糖核酸（DNA）以及塑料制品的外形以外，并没有用于硬件的复制设备。大多数硬件是按照某种设计装配出来。设计先于硬件而存在。

因此，我们真正需要的概念是**自由硬件设计**的概念。这是简单直白的：它指的是这样一种设计，允许用户使用它（即根据它装配硬件）并且复制和再分发，不论是否收取费用。这种设计必须提供定义了自由软件的同样的四项基本自由。

这样我们就可以将生产自自由设计的硬件说成是“自由硬件”或者“自由设计的硬件”以避免可能的误解。

首次接触自由软件思想的人们经常认为它意味着您可以免费获得一份副本。很多自由软件确实可以零价格获取，因为下载您自己的副本不会使您失去什么，但这并非“free”在此处的涵义（诸如 Flash 播放器和愤怒的小鸟等某些间谍软件确实是免费的，尽管它们并不自由）。将“libre”和“free”连用有助于澄清这一点[^2]。

对于硬件而言，这种混淆趋于另一方向；硬件生产需要花费资金，于是商业化生产的硬件不会是免费的（除非是亏本销售或者搭配销售），但是这并不妨碍其设计成为自由的。您利用自己的三维打印机生产出来的东西可以非常廉价，但是并非精确地免费，由于您必须购买原材料。就道德而言，自由的问题完全胜过价格的问题，由于拒绝其用户的自由的设备不要也罢。

短语“开放硬件”和“开源硬件”被某些人用于表达与“自由硬件”相同的具体涵义，但是这些短语对作为一个问题的自由进行了轻描淡写。它们衍生自“开源软件”这一短语，它或多或少指的是自由软件，但是并未谈论自由，或者将此问题呈现为是非问题[^3]。为了强调自由的重要性，每当与自由相关时，我们就会强调谈论自由；因为“open”一词做不到这一点，不要用它来取代“free”一词。

## 硬件和软件

硬件和软件在根本上不同。一个程序，即使是以编译后的可执行文件形式存在，也是一组可以被解释为计算机指令的数据集合。类似于任何其他数字作品，它可以利用计算机来复制和更改。程序的副本没有内在的物理形式或者体现。

与之相反，硬件是一种物理结构，其物质性是关键。尽管硬件设计可以被表示为数据，甚至在某些情况下被表示为程序，设计毕竟不是硬件。针对中央处理器（CPU）的设计不能执行程序。您不会在试图利用针对键盘的设计打字或者利用针对屏幕的设计显示像素时取得很多成果。

更进一步地，尽管您可以使用计算机来修改或者复制硬件设计，计算机并不能将该设计转化为其所描述的物理结构。这需要装配设备。

## 硬件和软件之间的界限

在数字设备中，硬件和软件之间的界限是什么？它可以从定义推断。软件是设备中的可以由计算机进行复制和更改的可使用的部分，而硬件则是不可如此操作的可使用的部分。这是进行区分的正确方法，由于它关系到实际产生的结果。

硬件和软件之间有一处灰色地带，它包含**可以**被升级或者替换，但其本意并非在产品售出以后被更新或者替换的固件。就概念而言，这个灰色地带十分狭窄。在实践上，它很重要，因为很多产品落在其范围内。我们可以通过少量引申将这样的固件看作硬件。

有些人说，预安装的固件程序和现场可编程逻辑门阵列（FPGA）“模糊了硬件和软件之间的界限”，但是我认为这是对事实的错误解读。在使用中安装的固件是软件；设备内部自带并且不可修改的固件就本质而言属于软件，但是我们可以将其视同电路。如对 FPGA，FPGA 本身是硬件，但是加载到 FPGA 中的逻辑门模式是一种固件。

在 FPGA 上运行自由的逻辑门模式可以潜在地成为一种制造在电路层级上成为自由的数字设备的有用方法。然而为了使得 FPGA 可用于自由世界，我们需要针对它们的自由开发工具。其障碍在于，加载至 FPGA 的逻辑门模式文件的格式是私密的。多年以来，没有一种型号的 FPGA 的相关文件能够无需非自由（私有）工具而创建。

到了 2015 年，通过以某种硬件描述语言（HDL）编写的输入来为 Lattice iCE40[^4]这种通用型号的 FPGA 编程的自由软件工具成为可用。现在利用自由工具编译 C 语言程序并且在 Xilinx Spartan 6 LX9 FPGA 上运行它们也已成为可能[^5]，但是这些工具并不支持 HDL 输入。我们建议您拒绝其他型号的 FPGA，直到它们也能被自由工具支持。

对 HDL 代码本身，它可以作为软件（如果它被运行于模拟器上或者加载至 FPGA 中），也可以作为硬件设计（如果它被实现于不可变的晶片或者电路板中）。

## 关于三维打印机的伦理问题

在伦理上，软件必须是自由的[^6]；非自由软件是一种不公。我们是否应当对硬件设计持有同样的观点？

我们确实应该，在三维打印（或者更普遍地，任何类型的个人装配行为）可以处理的领域。用于制造有用的、实际使用的物品（即功能性而非装饰性）的打印模式**必须**是自由的，因为它们是用于实际使用的作品。用户理应拥有对于这些作品的控制，正如他们理应得到对于他们所使用的软件的控制。分发一种非自由的功能性物品的设计和分发非自由软件一样错误。

请仔细选择那些能够完全利用自由软件工作的三维打印机；自由软件基金会认可这样的打印机[^7]。有些三维打印机是按照自由硬件设计制造的，但是 MakerBot 的硬件设计属于非自由[^8]。

## 我们是否必须拒绝非自由数字硬件？

非自由数字[^9]硬件设计是否属于一种不公？我们是否必须为了我们的自由而拒绝所有根据非自由设计制造出来的数字硬件，如同我们必须拒绝非自由软件那样？

由于硬件设计和软件源代码在概念上的平行，众多硬件黑客立即谴责非自由硬件设计，就像对于非自由软件那样。我并不同意，因为硬件和软件所处的环境不同。

当今的芯片和板卡装配技术类似于印刷机：它适合于在工厂中进行量产。相对于在今天复制软件，它更像在 1950 年复制书籍。

复制和修改软件的自由是一种道德上的必要性，因为这些活动对于使用软件的人们来说是可行的：允许您使用软件的设备（计算机）同样足以用于复制和修改它。今天的移动计算机过于弱小而不适合此目的，但是任何人都能找到足够强大的计算机。

更进一步地，计算机足以用于下载并运行由那些知道如何修改软件的人们修改的版本，即使您不是程序员。确实，非程序员每天都在下载并且运行软件。这就是为何自由软件对于非程序员而言具有真正的影响的原因。

这在多大程度上适用于硬件？并非能够使用数字硬件的每一个人都知道如何修改电路设计或者芯片设计，但是拥有个人计算机（PC）的任何人都拥有从事这项任务所需的设备。到此为止，硬件平行于软件，但是接下来就是重大区别了。

您不能在您的计算机上构建并且运行电路设计或者芯片设计。构造大型电路是大量艰苦的工作，这时您才能得到电路板。装配芯片在今天对于个人而言并不可行；只有量产才能使得它们足够廉价。利用今天的硬件技术，用户不能下载并且运行硬件黑客对于某种数字硬件设计的修改版本，如同他们能够运行软件黑客对于某个程序的修改版本那样。因此，四项基本自由不能赋予今天的用户对于硬件设计的集体控制，如同它们赋予用户对于程序的集体控制那样。这就是说明了为何所有软件必须自由的理由不能应用于今天的硬件技术的原因。

在 1983 年还没有自由操作系统，但是显而易见的是，一旦我们拥有了一种，我们可以立刻使用它并且获得软件自由。所缺少的一切就是这样一种自由操作系统的代码。

在 2014 年，如果我们拥有适合于 PC 的 CPU 芯片的自由设计，根据该设计量产的芯片并不能在硬件领域赋予我们同样的自由。如果我们将要购买在工厂中量产的产品，对于工厂的依赖会造成与非自由设计相同的大部分问题。为了使得自由设计赋予我们硬件自由，我们需要未来的装配技术。

我们可以展望这样的未来，彼时我们的个人生产者能够制造芯片，而我们的机器人可以将芯片同变压器、开关、按键、显示器、风扇等组装并且焊接在一起。在这样的未来，我们都将制造自己的计算机（以及装配设备和机器人等），而且我们将能够利用由了解硬件的人们作出的修改设计。彼时，关于拒绝非自由软件的论述将同时适用于非自由硬件设计。

这种未来距今至少有很多年。在此期间，原则上无需拒绝基于非自由设计的硬件。

## 我们需要自由数字硬件设计

尽管我们在今天的环境下无需拒绝基于非自由设计制造出来的数字硬件，我们仍需开发自由设计，并且应该在每当可行时使用它们。它们已经在今天提供了优势，而且在未来它们可能是使用自由软件的唯一方式。

自由硬件设计提供了实际上的优势。众多商业公司可以装配一台自由硬件，这减少了对于单一厂商的依赖。团体可以相互协调以便量产它们。拥有电路图或者 HDL 代码使得研究设计以排查错误或者恶意功能成为可能（NSA 在一些计算机硬件中安插恶意漏洞之事已经为人所知）。更进一步地，自由设计可以作为构建模块而用于设计计算机及其他复杂设备，它们的规格将会公开，并且拥有更少能够被用于反对我们的部件。

自由硬件设计可能可用于我们的计算机和网络中的某些部件以及嵌入式系统，在我们能够以此种方式制造整机之前。

自由硬件设计甚至可能在我们能够个人装配硬件之前就变得至关重要，如果它成为了避免非自由软件的唯一方法。随着普通的商业化硬件日益被设计为迫使用户屈服，由于私密的规格，以及要求代码经过某些其他人而非您的签名，它们日益同自由软件不兼容。蜂窝电话的调制解调器芯片以及甚至是某些图形加速器已经要求固件经过厂商签名。您的计算机上的任何允许某些其他人而非您修改的程序都是用于为您施加不公权力的工具；施加了这种要求的硬件是恶意硬件。对于蜂窝电话调制解调器芯片的案例，现在可用的所有型号都是恶意的。

有朝一日，自由设计的数字硬件可能是允许运行自由操作系统的唯一平台。让我们致力于在那一天之前拥有必要的自由数字硬件设计，并且希望我们有办法足够廉价地为所有用户制造它们。

如果您设计硬件，请使得您的设计成为自由的。如果您使用硬件，请敦促并且向商业公司施压，使其让硬件设计成为自由的。

## 设计的层级

软件拥有实现的层级；例如某个软件包可能包括库、命令和脚本。但是这些层级对于软件自由没有明显影响，因为使得所有这些层级都自由是可行的。设计程序组件与设计将其组合在一起的代码是同一类工作；类似地，从源代码构建组件与从源代码构建组合起来的程序是同一类操作。使得整体自由只要求持续工作直到我们完成整个任务。

因此，我们坚持要求程序在全部层级上自由。对于一个有资格称为自由的程序，构成它的每一行源代码都必须是自由的，于是您能够完全从自由的源代码重建该程序。

与之相反，物理物体经常是由已经在不同类型的工厂中设计并且制造好的组件构造而成的。例如，计算机由芯片构成，但是设计（或者装配）芯片与从芯片设计（或者装配）计算机非常不同。

因此，我们需要区分数字产品（可能还有某些其他类型的产品）的设计中的**层级**。连接芯片的电路是一个层级；每个芯片的设计是另一个层级。在 FPGA 中，基本单元间的互连是一个层级，而基本单元本身是另一个层级。在理想的未来，我们想要设计在所有层级上都是自由的。在当前环境下，仅仅使得一个层级成为自由的已经是重大进展。

然而，如果一项设计在同一个层级上组合了自由和非自由的部分——例如一个整合了私有的“软核微处理器”的“自由”HDL 电路——我们必须得出这样的结论，此设计在该层级作为一个整体属于非自由。类似地，对于非自由的“向导”或者“宏”，如果它们指定了芯片之间的部分互连或者芯片中以可编程的方式连接的部分。其自由部分可以看作朝向自由设计的未来目标迈出的一步，但是达到这一目标涉及替换非自由的部分。它们在自由世界中是不可接受的。

## 自由硬件设计的许可证和版权

您可以通过基于自由许可证发布硬件设计使其成为自由设计。我们建议使用 GNU 通用公共许可证（GNU GPL）版本 3 或者更新版本。我们利用这种用途的观点而设计 GPL 版本 3。

电路和非装饰性的物体形状上的左版，不会取得人们想象的那么大的效果。这些设计的版权仅仅适用于该设计被画出或者写下的方式。左版是一种利用版权法的方式，因此其效果同版权法的效果的范围相当。

例如电路作为拓扑结构不能被授予版权（因此不能使用左版）。由 HDL 编写的电路定义可以被授予版权（因此可以使用左版），但是左版只能覆盖该 HDL 代码表达细节，而非它所生成的电路拓扑结构。类似地，电路的绘图或者布局可以被授予版权，因此可以使用左版，但是仅仅覆盖此绘图或者布局，而非电路拓扑结构。任何人都可以以外观不同的方式合法地绘制同样的电路拓扑结构，或者写出一种能够生成相同电路的不同的 HDL 定义。

版权并不覆盖物理电路，因此当人们构建电路的实例的时候，该设计的许可证对于他们利用他们已经构建出来的设备做什么并没有法律效力。

对于物体的绘图以及三维打印模型而言，版权并不覆盖以不同的方式绘制同样的完全功能性的物体的外观。它也不会覆盖按照该绘图制造出来的功能性的物理实体。就版权所关注的范围而言，每一个人都可以自由地制造并使用它们（而这是我们迫切需要的自由）。在美国，版权并不覆盖该设计所描述的功能性的方面[^10]，但是确实覆盖装饰性的方面。如果某个物体既有装饰性又有功能性的方面，您将陷入棘手的境地[^11]。所有这一切在您的国家可能也是如此，或者并非如此。在商业性生产或者量产某些东西之前，您应该咨询当地律师。版权并非您需要关注的唯一问题。您可能会遭到专利攻击，它们最有可能被那些与构建您正在使用的设计毫无关系的实体所持有，并且可能还有其他法律问题。

时刻记住版权法和专利法完全不同。假设它们拥有任何共同点都是错误。这就是为何“知识产权”这一术语纯属一种混淆并且应该被完全拒绝的原因[^12]。

## 通过版本库推广自由硬件

促使已发表的硬件设计成为自由的最有效方式是通过这些设计在其中发表的版本库的规则。版本库的运行者应当将使用该设计的人们的自由置于作出这些设计的人们的偏好之上。这意味着将要求关于实用物品的设计成为自由的作为发表它们的条件。

对于装饰性的物品，该论述并不适用，因此我们无需坚持要求它们必须是自由的。然而，我们应该坚持要求它们是可分享的。因此，既能处理装饰性物品模型也能处理功能性物品模型的版本库应该每于每一类都拥有适当的授权许可政策。

对于数字设计，我建议版本库坚持要求 GNU GPL 版本 3 或者更新版本、Apache 版本 2.0，或者 CC-0。对于功能性的三维设计，版本库还应该请求该设计的作者选择下列四种许可之一：GNU GPL 版本 3 或者更新版本、Apache 版本 2.0、CC-BY-SA、CC-BY，或者 CC-0。对于装饰性的设计，它应该选择 GNU GPL 版本 3 或者更新版本、Apache 版本 2.0、CC-0，或者任何知识共享（CC）许可证。

该版本库应当要求所有设计都以源代码形式发表，而仅仅对于私有设计软件可用的私密格式的源代码并不真正满足要求。对于三维模型而言，STL 格式并非用于修改设计的首选格式，因此不属于源代码，所以版本库不应该接受此格式，除非它们可能伴随着真正的源代码。

没有理由仅仅为硬件设计的源代码选择单一格式，但是仍然不能被自由软件处理的源代码格式至多只应该被勉强接受。

## 自由硬件与质保

一般而言，自由硬件设计的作者没有为基于该设计进行制造的人们提供任何质保的道德义务。这与贩卖物理硬件属于不同的问题，后者应该带有来自销售者和/或制造者的质保。

## 结论

我们已经有了使得我们的硬件设计成为自由的适当的许可证。我们需要的是作为一个社区将其认可为我们应当做的事情，并且在我们自行装配物品时坚持自由设计。

[^1]: 参见“什么是自由软件”一文以获知四项基本自由的列表。

[^2]: 如需获得关于监控在业界蔓延的方式的一份日益增长的清单，参见<https://gnu.org/philosophy/proprietary/proprietary-surveillance.html>。

[^3]: 参见“为何‘开源’错失自由软件的关键”一文。

[^4]: 参见<https://clifford.at/icestorm/>。

[^5]: 参见<https://github.com/Wolfgang-Spraul/fpgatools>。

[^6]: 参见“自由软件现在变得更加重要”一文。

[^7]: 参见<https://fsf.org/resources/hw/endorsement>。

[^8]: Rich Brown，“退出开源硬件，MakerBot 激怒了某些支持者”，2012 年九月 27 日，<https://cnet.com/news/pulling-back-from-open-source-hardware-makerbot-angers-some-adherents/>。

[^9]: 在此处的用法中，“数字硬件”包括那些除了数字部件以外还拥有某些模拟电路和部件的硬件。

[^10]: 参见美国版权局关于“实用物品”的定义，位于<https://copyright.gov/register/va-useful.html>。

[^11]: Public Knowledge 的一篇文章（“为您的三维打印素材提供授权许可的三个步骤”，2015 年三月 6 日，<https://publicknowledge.org/assets/uploads/documents/3_Steps_for_Licensing_Your_3D_Printed_Stuff.pdf>）给出了对于美国而言有用的关于这种复杂性的信息，尽管它犯了使用欺骗性的概念“知识产权”以及不应和版权关联使用的鼓吹的概念“保护”等常见错误。参见“需要避免使用（或者谨慎使用）的词语，由于它们是不公正的或者具有迷惑性的”一文以获知其原因。

[^12]: 参见“您说过‘知识产权’吗？这是一种诱惑性的幻景”一文。

著作权所有 (C) 2015 Richard Stallman

本文的大部分内容分为两部分发表于 _Wired_ 网站，分别为“为何我们需要自由数字硬件设计”（_Wired_，2015 年三月 11 日，<https://wired.com/2015/03/need-free-digital-hardware-designs>）和“硬件设计应该是自由的，以下是如何实现它”（_Wired_，2015 年三月 18 日，<https://wired.com/2015/03/richard-stallman-how-to-make-hardware-designs-free>）。

本文于 2015 年发表于<https://gnu.org>。此版本是“自由软件，自由社会：Richard M. Stallman 文选，第三版”（波士顿：GNU Press，2015）的一部分。

本文基于知识共享：署名——禁止演绎（CC BY-ND）4.0 国际版许可证（<https://creativecommons.org/licenses/by-nd/4.0/>）。

[返回目录](00_index.html)
