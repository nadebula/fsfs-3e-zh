# 服务器真正是在为谁服务？

如需获得关于此问题的更多信息，参见“无人被允许理解的 bug”一文，它位于<https://gnu.org/philosophy/bug-nobody-allowed-to-understand.html>。

**在互联网上，私有软件并非剥夺您的自由的唯一方式。“作为软件替代品的服务”，或者 SaaSS，是另一种赋予其他人支配您的计算的权力的途径。**

SaaSS 指的是使用由他人实现的服务来替代运行您的软件副本。这是我们创造的短语；文章和广告并不会使用它，它们也不会告知您某种服务是否为 SaaSS。与之相反，它们很可能蔽之以含混不清并且转移您的注意力的术语，“云”。这将 SaaSS 与其他实现混为一谈，不论是坏是好。通过本文的解释和示例，您将能够区分某种服务是否为 SaaSS。

## 背景知识：私有软件是如何剥夺您的自由的

数字技术可以赋予您自由；它也可以剥夺您的自由。对于我们掌控自己的计算的首要威胁来自**私有软件**：用户所不能控制的软件，由于其拥有者（诸如苹果、微软等商业公司）控制着它。其拥有者通常会利用这种不公的权力，通过向其中植入恶意特性，诸如间谍软件、后门、数字限制管理（DRM，在它们鼓吹中被引用为“数字版权管理”）[^1]。

我们针对这个问题的解决方案是开发**自由软件**并且拒绝私有软件。自由软件意味着您作为用户拥有四项基本自由： (0) 以任何目的运行该软件的自由； (1) 研究和修改源代码以使其做您所期望的事情的自由； (2) 再分发相同副本的自由； (3) 再分发您的修改版本的副本的自由。（参见“什么是自由软件”一文。）

只要有了自由软件，我们作为用户就能夺回对于我们的计算的控制权。私有软件仍然存在，但是我们可以将其排除在我们的生活之外，并且我们中的很多人已经如此做。然而现在，我们面对对于自己的计算的控制权的新威胁：作为软件替代品的服务（SaaSS）。为了捍卫我们的自由，我们必须同样拒绝 SaaSS。

## 作为软件替代品的服务是如何剥夺您的自由的

作为软件替代品的服务（SaaSS）指的是使用某种服务来替代运行您的软件副本。具体地说，它指的是由某人架设一台网络服务器，它包含某种计算任务——例如，修改一幅照片，或者将文本翻译为另一种语言等——然后邀请用户通过那台服务器进行计算。服务器的用户将其本人的数据发送至服务器，后者对以此方式提供的数据进行**用户自己的计算**，再将结果返回用户，或者直接以用户的名义行事。

这种计算属于**用户自己的**，由于根据假设，用户在原则上能够通过在其本人的计算机上运行某个程序以达到此目的（不论该用户当时能否获得此程序）。当这种假设不成立时，这就不是 SaaSS。

这些服务器比私有软件更加残酷地剥夺用户的控制权。对于私有软件，用户一般会得到一份可执行文件而非源代码。这使得用户难以研究正在运行的代码，因而难以判定此程序真在做什么，并且难以对其进行修改。

对于 SaaSS，用户连用于进行他们的计算的可执行文件都得不到：它位于某些其他人的服务器上，用户不能企及。因此用户不可能确认它到底在做什么，也不可能对其进行修改。

进一步讲，SaaSS 将会自然而然地引起与某些私有软件中的恶意特性相当的后果。

例如，一些私有软件是“间谍软件”：它们将会发送与用户的计算活动相关的数据[^2]。微软 Windows 向微软发送用户活动相关信息。微软 Windows Media Player 报告每位用户播放的东西。亚马逊焚书机（Kindle）报告用户于何时阅读哪本书的第几页。愤怒的小鸟报告用户的地理位置历史记录。

与私有软件不同的是，SaaSS 并不依赖隐秘代码以获取用户数据。与之相反，用户必须将其数据发送到服务器以便使用它。这与间谍软件具有相同的效果：服务器运行者可以不费吹灰之力得到用户数据——由于 SaaSS 的天性。Amy Webb，此人刻意避免发布她的女儿的任何照片，犯了使用 SaaSS（Instagram）来编辑女儿的照片的错误。最终这些照片通过这种途径泄露[^3]。

一些私有操作系统拥有通用后门，允许某人远程安装软件更改。例如，Windows 拥有通用后门，微软可以通过它强制更改设备上的软件。几乎所有的移动电话也拥有通用后门。一些私有应用程序也拥有通用后门；例如 Steam 的 GNU/Linux 客户端允许开发者远程安装修改版本。

对于 SaaSS 而言，服务器运行者可以更改服务器上所用的软件。他应该能够如此做，由于那是他的计算机；但是，其结果等同于使用带有通用后门的私有应用程序：某人拥有这样的权力以偷偷改变用户的计算的完成方式。

因此，使用 SaaSS 相当于运行带有间谍软件和通用后门的私有软件。这赋予了服务器运行者凌驾于用户之上的不公权力，而这种权力是我们必须坚决反对的。

## SaaSS 和 SaaS

最初，我们将这种有问题的实践称为“SaaS”，意为“软件即服务”（Software as a Service）。这个常用短语指的是在服务器上设置软件而非向用户提供副本。我们曾经认为它准确地描述了发生这种问题时的情形。

然后，我们开始意识到，SaaS 这一短语有时用于指代通讯服务——这一问题并不适用于这种行为。此外，“软件即服务”这一短语并未解释**为何**这是一种坏的实践。于是我们打造了“作为软件替代品的服务”这一短语，它更为清晰地定义了这种坏的实践，并且解释了它都有哪些坏处。

## 理清 SaaSS 带来的问题和私有软件带来的问题

SaaSS 和私有软件将会带来相似的后果，但其机制并不相同。对于私有软件，其机制是您拥有并且使用一份副本，而对其进行修改是困难和/或非法的。而对于 SaaSS，其机制是您并不拥有一份用于进行您的计算的软件副本。

这两类问题通常被混淆，而这种混淆并非偶然。网络开发者使用含混不清的短语“网络应用程序”将服务器软件和在您的设备上的浏览器中运行的程序混为一谈。一些网页会在您的浏览器中安装非平凡甚至是大型的 JavaScript 程序而不会告知您。如果这些 JavaScript 程序是非自由的[^4]，它们将会造成与任何其他非自由软件同样的不公。然而，我们在此将会专注于使用服务本身带来的问题。

众多自由软件支持者设想，SaaSS 带来的问题将会通过开发自由的服务器软件而解决。对于服务器运行者而言，服务器上的程序最好是自由的；如果它们是私有的，其拥有者便可拥有控制服务器的权力。这对于服务器运行者是不公的，并且根本不会使用户受益。但是，即使服务器上的程序是自由的，这也不能保护**该服务器的用户**免受 SaaSS 的影响。这些程序解放了服务器运行者，而非服务器的用户。

公开服务器软件的源代码确实会使社区受益：这使得具有适当技能的用户能够架设类似的服务器，也许还能更改软件本身。我们建议为通常在服务器上使用的软件使用 GNU Affero 通用公共许可证（GNU Affero GPL）[^5]。

但是，这些服务器都不能使您控制您在其上进行的计算，除非那是**您自己的**服务器。也许对于某些工作，您可以信任您的朋友的服务器，如同您可能会请求朋友维护您自己的计算机上的软件。除此之外，这些服务器对您来说都是 SaaSS。SaaSS 总是迫使您屈从于服务器运行者的权力，而唯一的解决方式就是**不要使用 SaaSS**！不要使用任何其他人的服务器来对您自己提供的数据进行您自己的计算。

这个问题解释了“开源”和“自由”之间存在多么深刻的区别。“开源”的源代码几乎都是自由的[^6]。但是“开源软件”服务[^7]的理念，其涵义为这样一种服务的服务器软件是开源和/或自由的，并不能解决 SaaSS 的问题。

服务与软件有着根本区别，因而由服务引起的伦理问题与由软件引起的问题有着根本区别。为了避免这种混淆，我们避免将一项服务描述为“自由”或者“私有”的。[^8]

## 区分 SaaSS 和其他网络服务

哪些在线服务属于 SaaSS？最清楚的例子是翻译服务，（例如）将英文文本翻译为西班牙文。为您翻译一段文本是一种完全属于您自己的计算。您可以在您自己的计算机上运行软件进行翻译。（为了符合伦理，该软件应该是自由的。）翻译服务替代了该程序，因此它是一种作为软件替代品的服务，即 SaaSS。由于它拒绝您对于您的计算的控制权，它对您作了恶。

另一个清楚的例子是使用诸如 Flickr 或者 Instagram 等服务来修改照片。修改照片是一种人们已经在自己的计算机上进行了几十年的行为；在服务器而非您自己的计算机上进行此操作是一种 SaaSS。

拒绝 SaaSS 并不意味着拒绝使用任何由其他人而非您运行的网络服务器。大部分服务器并非 SaaSS，由于它们所执行的任务并非用户自己的计算。

网络服务器的初衷并非为您做计算，而是发布信息以供您访问。即使在今天，这也是大部分网站所做的，这并不会带来 SaaSS 的问题，由于访问由某人发布的信息并非做您自己的计算。通过博客网站或者诸如 Twitter、StatusNet 等微博服务发布您的个人素材也不是。（当然，这些服务可能会有其他问题。）其他并非有意成为私密的通讯，例如群聊，也是如此。

从本质上说，社交网络是一种通讯和出版的形式，而非 SaaSS。然而，一项以社交网络为主要功能的服务可能拥有属于 SaaSS 的特性或者扩展。

如果一项服务不属于 SaaSS，这并不意味着它就是没有问题的。服务可能存在其他伦理问题。例如，Facebook 以 Flash 格式分发视频，这将迫使用户运行非自由软件；它要求运行非自由 JavaScript 代码；它给了用户一种关于隐私的具有误导性的印象，同时引诱用户在 Facebook 上暴露他们的生活。那些都是重要的问题，不同于 SaaSS 的问题。

诸如搜索引擎等一些服务将会从网络上搜集数据以供您检索。浏览它们所收集的数据在通常意义上并不属于您自己的计算——由于您并不提供那些数据——因此使用这样的服务搜索网络并非 SaaSS。然而，使用他人的服务器来实现用于您自己的网站的搜索工具**是**一种 SaaSS。

在线购物不是 SaaSS，由于这种计算不是**您自己的**；相反，这是由您和卖家为了共同目的而共同实现的。在线购物的真正问题是您能否将您的钱财和其他个人信息（首当其冲的是您的名字）托付给对方。

诸如 Savannah 或者 SourceForge 等版本库网站在本质上不是 SaaSS，由于版本库的任务是发布那些提供给它的数据。

使用联合项目的服务器不是 SaaSS，由于您以这种方式所做的计算不是您自己的。例如，如果您编辑 Wikipedia 上的页面，您并非在进行您自己的计算；与之相反，您正在参与 Wikipedia 的计算。Wikipedia 控制着它自己的服务器，但是如果任何组织或者个人使用他人的服务器进行他们自己的计算，他们将会遇到 SaaSS 问题。

有些网站提供多种服务，如果其中之一不是 SaaSS，其他服务有可能是 SaaSS。例如，Facebook 的主要服务是社交网络，那不是 SaaSS；然而，它还支持第三方应用程序，其中有些是 SaaSS。Flickr 的主要服务是分发照片，这不是 SaaSS，但它也会提供照片编辑特性，这就是 SaaSS。类似地，使用 Instagram 发布一幅照片并非 SaaSS，但用它转换照片则是。

Google Docs 向我们展示了评估单一的服务到底可以有多么复杂。它邀请用户通过运行大型非自由 JavaScript 程序[^9]来编辑文档，这无疑是坏的。然而，它还提供了用于以标准格式上传或下载文档的应用程序接口（API）。自由的编辑器软件可以通过这个 API 工作。这种应用场景不是 SaaSS，由于它仅仅将 Google Docs 用作版本库。将您的所有数据展示给一家商业公司不是好事，但这属于隐私问题，而非 SaaSS；依赖这样的服务来访问您的数据不是好事，但这属于风险问题，而非 SaaSS。另一方面，使用这种服务转换文档格式**是**一种 SaaSS，因为这是您可以通过在您自己的计算机上运行适当的程序（最好是自由的）来实现的。

当然，通过自由的编辑器使用 Google Docs 的情形并不常见。更为常见的情形是，人们通过非自由 JavaScript 程序使用它，它和任何其他非自由软件一样坏。这种应用场景可能也会涉及 SaaSS；这取决于编辑工作的哪部分由 JavaScript 程序完成而哪部分由服务器完成。我们不清楚，但是既然 SaaSS 和私有软件都对用户作了相似的恶，弄清这个问题并不重要。

通过他人的版本库进行出版并不会引起隐私的问题，但是通过 Google Docs 进行出版则会遇到一个特别的问题：如果不运行非自由 JavaScript 代码，甚至不可能在浏览器中**查看**一篇 Google Docs 文档中的文本。因此，您应该避免使用 Google Docs 出版任何东西——然而其问题并不在于 SaaSS。

信息技术（IT）业界阻碍用户作出这样的区分。这正是它们的行话“云计算”的用意之所在。这个短语是那么地含混不清，以至于它可以指代有关互联网的几乎所有应用。它包括了 SaaSS 以及众多其他网络应用实践。在任何给定的上下文环境中，一位作者（如果是一位技术工作者）在写出“云”这个词的时候，其脑海中可能有一种具体的涵义，但是通常并不会解释这个词在其他文章中拥有其他具体的涵义这一点。这个短语将会诱导用户将那些他们本应单独思考的实践一般化。

如果“云计算”确实有一种涵义，这并不是一种进行计算的方式，而是一种对于计算的思考的方式：一种不顾一切的方式，它如是说，“什么也不要问；不要关心谁控制着您的计算、谁掌握着您的数据；在像鱼饵一样吞下我们的服务之前也不要去检查里面是否藏着鱼钩……毫不犹豫地信任商业公司。”换言之，“做一个没有独立思想的人”。思想中的阴云是进行清晰思考的障碍。为了能够对计算进行清晰的思考，让我们避免使用“云”这个概念。

## 应对 SaaSS 所带来的问题

只有小部分网站提供 SaaSS；大部分网站并不会带来这样的问题。但是，对于那些带来了 SaaSS 问题的网站，我们又该如何应对？

对于简单的情形，如果您正在对于您所掌控的数据进行您自己的计算，解决方案很简单：使用您自己的自由软件副本。使用您的诸如 GNU Emacs 等自由的文本编辑器或者自由的文字处理器的副本进行您自己的文本编辑。使用您的诸如 GIMP 等自由软件的副本进行您自己的照片编辑。如果没有可用的自由软件呢？私有软件或者 SaaSS 将会剥夺您的自由，因此您不应使用它们。您可以贡献您的时间或钱财来支持开发自由的替代品。

与他人一起作为一个小组进行协作的情况又如何呢？直到现在，不借助服务器可能难以实现这一目的，并且您的小组可能不知道如何运行自己的服务器。如果您使用他人的服务器，至少不要信任由商业公司运营的服务器。一纸作为客户的合同并不能带来任何保护，除非您能够抓住其中的漏洞并且真正能够进行诉讼，而商业公司很可能会如此编写它的合同，以允许其大范围的滥用行为。国家可以从商业公司那里传唤您和任何其他人的数据，如同奥巴马对电话公司所做的，假如该公司不像之前那些为布什非法监听其客户的美国电话公司那样主动上交这些信息。如果您不得不使用服务器，选择那些其运行者能够给予您基本信任而非仅仅是一层商业关系的服务器。

然而，在长远的时间尺度上，我们可以创造出对于使用服务器的替代方案。例如，我们可以创造一种点对点的程序，使得协作者可以通过它分享加密数据。自由软件社区应该为关键的“网络应用程序”开发分布式的点对点替代品。将它们在 GNU Affero GPL 许可证下发布可能是明智的，由于它们可能成为候选者供其他人将其转换为基于服务器的程序[^10]。GNU 计划正在寻找志愿者以致力于这些替代品。我们还邀请其他自由软件项目在其设计中考虑这一问题。

与此同时，如果一家商业公司邀请您使用它的服务器来进行您自己的计算任务，不要屈服；也不要使用 SaaSS。不要购买或者安装所谓的“瘦客户端”，它们只不过是低性能计算机，以迫使您在服务器上进行真实的工作，除非您打算配合**您自己的**服务器使用它们。使用一台真实的计算机并且将您的数据保存在此。使用您自己的自由软件副本来进行您自己的计算，这是为了您的自由。

[^1]: 请加入我们的运动一起反对 DRM，它位于[DefectiveByDesign.org](https://DefectiveByDesign.org)。

[^2]: 如需获得关于监控在业界蔓延的方式的一份日益增长的清单，参见<https://gnu.org/philosophy/proprietary/proprietary-surveillance.html>。

[^3]: Amy Webb，“恭喜您在网上找到了我的女儿的照片”，2013 年九月 12 日，<https://slate.com/articles/technology/data_mine_1/2013/09/privacy_facebook_kids_don_t_post_photos_of_your_kids_on_social_media.html>。

[^4]: 参见“JavaScript 陷阱”一文以获得更多信息。

[^5]: 参见“如何为您自己的作品选择许可证”一文以获得我们关于许可证选择的建议。

[^6]: 参见“作为软件类别的自由软件和开源之间的关系如何”一文，位于<https://gnu.org/philosophy/free-open-overlap.html>以获得更多信息。

[^7]: 如需获知“开源软件服务定义”，参见<https://opendefinition.org/ossd/index.html>。

[^8]: 如需获得更多信息，参见我的文章“网络服务器无所谓自由或者非自由；它们引起的是其他问题”一文，位于<https://gnu.org/philosophy/network-services-arent-free-or-nonfree.html>。

[^9]: 参见“JavaScript 陷阱”一文以获得更多信息。

[^10]: 参见“为何使用 Affero GPL”一文，位于<https://gnu.org/licenses/why-affero-gpl.html>以获得完整解释。

著作权所有 (C) 2010, 2013, 2015 Richard Stallman

本文最初于 2010 年三月 8 日以“服务器真正是在服务什么”为题发表于《波士顿评论》在线版。此版本是“自由软件，自由社会：Richard M. Stallman 文选，第三版”（波士顿：GNU Press，2015）的一部分。

本文基于知识共享：署名——禁止演绎（CC BY-ND）4.0 国际版许可证（<https://creativecommons.org/licenses/by-nd/4.0/>）。

[返回目录](00_index.html)

