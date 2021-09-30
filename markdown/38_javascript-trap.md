# JavaScript 陷阱

> 您可能每天都在您的计算机上运行非自由软件而毫无察觉——通过您的浏览器。

在自由软件社区，非自由软件虐待它们的用户这一理念为人们所熟知。我们中的一些人完全拒绝安装任何私有软件，众多其他人将非自由视为不采用该软件的一大理由。很多用户注意到这一问题同样适用于浏览器提供安装的插件，由于它们可以是自由或者非自由的。

但是，浏览器会运行那些它们不会询问您，甚至不会告知您的其他非自由软件——网页中包含的或者链接到的程序。这些程序通常由 JavaScript 编写，尽管其他语言也被使用。

JavaScript（官方名称为 ECMAScript，但是很少有人使用这个名字）曾经用于网页中的次要修饰部分，例如精巧但不重要的导航和显示特性。将这些仅仅看作 HTML 标记语言的扩展而非真正的软件曾经是可以接受的；它们并不构成主要问题。

众多网站仍然以这种方式使用 JavaScript，但是有些网站将其用于执行大型任务的主要程序。例如 Google Docs 将会向您的设备下传一个大约 0.5 MB 的 JavaScript 程序，此程序采用一种我们称之为模糊脚本（Obfuscript）的紧密格式编写，由于其中没有注释，也几乎没有任何空白字符，而方法的名称只有一个字母长。程序的源代码是用于修改它的首选形式；这种紧密代码不是源代码，而此程序的真正源代码对于其用户不可用。

浏览器通常不会告知您它们于何时加载 JavaScript 程序。大多数浏览器提供了一种完全禁用 JavaScript 的方式，但是没有浏览器可以检查非平凡、非自由的 JavaScript 程序。即使您注意到了这个问题，要想识别并阻止这些程序可能会给您带来相当大的麻烦。然而，即使是在自由软件社区内，大部分用户也并未觉察到这一问题；浏览器的沉默倾向于掩盖这个问题。

有可能将一个 JavaScript 程序作为自由软件发布，通过在自由软件许可证下分发其源代码。但是，即使程序的源代码可获得，并没有一种简易的方法来运行您的修改版本而非原始版本。当前的自由浏览器并没有提供这样一种功能来使用您的修改版本而非网页自带的版本。这种效果可以和“TiVo 化”（tivoization）相比，尽管并不是那么难以克服。

JavaScript 并非网站发送给用户的程序所使用的唯一语言。Flash 支持通过 JavaScript 的一种扩展变体进行编程。我们需要研究 Flash 的问题来给出适当的建议。Silverlight 看起来将会带来类似于 Flash 的问题，只不过它比 Flash 更坏，由于微软将其用作私有编码译码器（codec）的平台。Silverlight 的自由替代品并不能为自由世界作出贡献，除非它常规地自带编码译码器的自由替代品。

Java 小程序（applet）也是在浏览器中运行的，也会带来类似的问题。一般来说，任何类型的小程序系统都会带来这类问题。拥有自由的小程序执行环境只能将我们带到足以克服这个问题的地方。

已经发展起了一场声势浩大的运动号召网站仅仅通过自由的（有些人称之为“开放的”）格式和协议进行通讯；也就是说，它们的文档是公开的，并且任何人都可以自由地实现它们。由于程序在网页中的存在，这样的判据是必需的，但并不足够。JavaScript 作为一种格式，其本身是自由的，并且在网站中使用 JavaScript 并不一定坏。然而，如同我们在上文所见，这也不一定好。当网站向用户发送某个程序时，该程序是用一种有文档、不受限的语言所编写的这一点并不足够；该程序本身也必须是自由的。“只有自由软件才能被传送到用户”必须成为网站的恰当行为判据的一部分。

静默地加载并运行非自由软件是“网络应用程序”所带来的若干问题之一。“网络应用程序”这一短语被设计为抹煞传送给用户的软件与在服务器上运行的软件之间的根本区别。它可以指代在浏览器中运行的专用客户端程序；也可以指代专用服务器软件；还可以指代与专用服务器软件共同工作的专用客户端程序。客户端和服务器端将会引起不同的伦理问题，即使它们整合得如此紧密，以至于它们可以被认为是构成了单一程序的组成部分。本文仅仅讨论客户端软件带来的问题。我们将会单独讨论服务器的问题。

在实践层面，我们怎样才能应对网站中的非自由 JavaScript 程序的问题呢？第一步当然是避免运行它们。

我们之前提到的“非平凡”是指什么呢？这指的是一种程度，因此这是一个关于设计出一种能够得到良好结果的简单的判据，而非找到唯一正确答案的问题。

我们试着提出的策略将某个 JavaScript 程序看作非平凡的，如果：

* 它会提交异步 JavaScript 与 XML（AJAX）请求，或者与提交 AJAX 请求的脚本被一同加载；
* 它会动态加载外部脚本，或者与动态加载外部脚本的脚本被一同加载；
* 它定义了这样的函数或方法，这些函数或方法要么（从 HTML）加载外部脚本，要么被作为外部脚本加载；
* 它使用了不对程序进行解释就难以分析的动态 JavaScript 结构，或者与使用了这样的结构的脚本被一同加载。这些结构包括：
    * 使用了 `eval` 函数；
    * 使用方括号标记调用方法；
    * 将除了字符串字面量以外的结构用于某些方法（例如 `Obj.write`、`Obj.createElement` 等）。

我们如何判断 JavaScript 代码是否自由呢？我们在本文末尾提出了一种约定。根据这种约定，网页中的非平凡 JavaScript 程序可以使用样式化的注释说明其源代码的统一资源定位符（URL），以及说明它的许可证。

最后，我们还需要修改自由浏览器使其检测并阻止网页中的非平凡非自由 JavaScript 代码。LibreJS 程序能够检测并阻止您所访问的网页中的非平凡非自由 JavaScript 代码[^1]。LibreJS 是 IceCat 和 IceWeasel（还有 Firefox）的插件。

浏览器用户还需要一款简便的工具以指定想要使用的 JavaScript 代码，**而非**特定网页中的 JavaScript 代码。（此指定的代码可以是该网页中的自由 JavaScript 程序的完全替代品或者修改版本。）Greasemonkey 几乎可以实现这一点，但仍有欠缺，由于它不能保证在网页中的程序开始被执行之前完成对其 JavaScript 代码的修改。使用本地代理能够解决问题，但是现在其便捷程度尚不足以使其成为真正的解决方案。我们需要构建一种兼具可靠性与便捷性的解决方案，以及用于分享这些修改的网站。GNU 计划将会推荐那些仅仅专注于自由的修改的网站。

这些特性将会使得网页中包含的 JavaScript 程序有可能在真正与实际的意义上成为自由的。JavaScript 将不再是实现我们的自由的一种特别障碍——就像现在的 C 语言和 Java 那样不成为障碍。我们将能够拒绝甚至替换网页中的非平凡非自由 JavaScript 程序，正如我们能够拒绝或者替换通过常规方式提供安装的非自由软件包那样。我们要求网站将其 JavaScript 代码自由化的运动就可以展开。

与此同时，确实这样有一种情况，在此运行非自由 JavaScript 程序是可接受的：向网站运行者发送投诉，告知其应当移除或者自由化该网站中的 JavaScript 代码。不要犹豫，马上暂时允许 JavaScript 以进行投诉——然后记得重新关闭它。

## 附录 A：用于发布自由 JavaScript 程序的一种约定

对于相应源代码的引用，我们建议

    // @source:

后面跟着 URL。这种方式满足 GNU 通用公共许可证（GNU GPL）对于分发源代码的要求。如果源代码位于另一站点，您必须妥善处理这种情形。要想使得程序成为自由的，源代码是必需的。

如需指出嵌入此网页的 JavaScript 代码的许可证，我们建议将授权通知置于这种形式的两处注释之间：

    @licstart The following is the entire license notice for the
    JavaScript code in this page.
    ...
    @licend The above is the entire license notice
    for the JavaScript code in this page.

    @licstart 以下内容为此网页中的 JavaScript 代码的完整授权通知
    ...
    @licend 以上内容为此网页中的 JavaScript 代码的完整授权通知

当然，所有这些内容应当位于多行注释之间。

同众多其他自由软件许可证一样，GNU GPL 要求连同程序的源代码和二进制形式一同分发一份许可证的副本。然而，由于 GNU GPL 过于冗长，将其同 JavaScript 程序一同包含在页面中可能带来不便。对于您拥有版权的代码，您可以移除这条要求，代之以类似这样的许可证声明：

    Copyright (C) YYYY Developer
    
    The JavaScript code in this page is free software: you can
    redistribute it and/or modify it under the terms of the GNU
    General Public License (GNU GPL) as published by the Free Software
    Foundation, either version 3 of the License, or (at your option)
    any later version. The code is distributed WITHOUT ANY WARRANTY;
    without even the implied warranty of MERCHANTABILITY or FITNESS
    FOR A PARTICULAR PURPOSE. See the GNU GPL for more details.
    
    As additional permission under GNU GPL version 3 section 7, you
    may distribute non-source (e.g., minimized or compacted) forms of
    that code without the copy of the GNU GPL normally required by
    section 4, provided you include this license notice and a URL
    through which recipients can access the Corresponding Source.

    著作权所有 (C) 年份 开发者
    
    此网页中的 JavaScript 代码是自由软件：您可以基于自由软件基金会发布的 GNU 通用公共许可证（GPL）版本 3 或者（根据您的选择）任何更新版本的条款分发和/或修改此程序。此代码以不带任何质保的方式被分发；甚至不带适售性或者适用于某种特定用途所暗示的质保。参见 GNU GPL 版本 3 第 7 条以获得更多细节。
    
    作为 GNU GPL 版本 3 第 7 条之下的附加许可，您可以分发此代码的非源代码（例如最小化或者紧密）形式，而不带第 4 条所通常要求的 GNU GPL 副本，如果您包含了此条许可证声明以及接受者可以访问相应源代码的 URL。

感谢 Jaffar Rumith 提醒我关注这一问题。

## 附录 B：以网站管理员身份发布自由的 JavaScript 程序

如果您是一位在您的网站上部署自由的 JavaScript 软件的管理员，明晰并且一致地发布这些文件的许可证信息和源代码有助于您的访问者确定他们正在运行自由软件，并且有助于您遵守这些许可条件。

声明这些许可证的一种方式如上文附录 A 所述。另一种方法，称为 JavaScript 许可证网络标签，可能对于精简的 JavaScript 代码库更为便捷，尤其当它们并非您所编写时。

[^1]: LibreJS 项目（<https://gnu.org/software/librejs/>）是 JavaScript 程序员所必需的。如果您拥有必需的技能，请帮助我们维护这个价值连城的浏览器扩展。

著作权所有 (C) 2009−2013 Richard Stallman

本文最初于 2009 年发表于<https://gnu.org>。此版本是“自由软件，自由社会：Richard M. Stallman 文选，第三版”（波士顿：GNU Press，2015）的一部分。

本文基于知识共享：署名——禁止演绎（CC BY-ND）4.0 国际版许可证（<https://creativecommons.org/licenses/by-nd/4.0/>）。

[返回目录](00_index.html)

