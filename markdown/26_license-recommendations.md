# 如何为您自己的作品选择许可证

## 简介

人们经常问，我们建议他们为其项目使用何种许可证。我们此前已经公开编写过关于此问题的文章，然而其信息分散于不同的文章、常见问题集条目，以及许可证评述之间。本文将所有这些信息收集于单一来源之中，以使得人们更加容易遵循和回顾。

这些建议针对的是那些被设计为执行实际任务的作品。这些作品包括软件、文档以及某些其他东西。艺术品以及陈述某种观点的作品属于不同的问题；GNU 计划关于它们应该被如何发布并没有普遍立场，除了它们都应该在没有非自由软件的情况下可用（特别是不带数字限制管理（DRM）[^1]）。然而，您可能想要针对伴随某个特定程序的艺术品遵循以下建议。

这些建议适用于为您所创造的作品提供授权——不论其是对现存作品的修改还是全新原创作品。它们并非应对将基于不同许可证的现存素材合并起来的问题。如果您正在寻求关于此问题的帮助，请查阅我们的 GPL 常见问题集[^2]。

当您看到我们所推荐的方法之后，如果您仍想得到建议，可以发送邮件至[licensing@gnu.org](mailto:licensing@gnu.org)。请注意，许可证团队可能需要花费几个星期才能对您进行反馈；如果您在一个月内没有得到回复，请再发送一次。

## 为现存项目做贡献

当您为某个现存项目做贡献时，您通常应该基于与原始作品相同的许可证发布您的修改版本。最好是同该项目的维护者进行合作，而为您的修改使用不同许可证通常会使得这种合作变得非常困难。您只有在拥有强大的理由支持如此做的时候才应该如此做。

一种有理由使用不同许可证的情况是，您为某个基于非左版许可证的作品作出了重大修改。如果您所创造的版本远比原始版本有用，就值得以左版发布您的作品，由于我们通常推荐左版的相同原因。如果您处于这种情况，请遵循以下关于为新项目提供授权的建议。

无论您出于什么理由而选择基于不同许可证发布您的贡献，您必须保证原始许可证允许将其素材用于您所选择的许可证。出于诚实的缘故，明确展示作品的哪些部分基于何种许可证。

## 软件

我们建议将不同许可证用于不同项目，主要取决于软件的目的。总的来说，我们推荐使用不会干涉该目的的最强左版许可证。我们的文章“什么是左版？”更加详细地阐述了左版的概念，以及为什么它通常是最好的授权许可策略。

对于大多数程序，我们建议您为您的项目使用最新版本的 GNU 通用公共许可证（GPL）。它的强左版性质适合于所有类型的软件，并且包含对于用户的众多保护。

以下是一些例外。

### 小程序

为大多数小程序使用左版会带来不值得的麻烦。我们以 300 行作为基准：如果某个软件包的源代码比它更短，左版带来的好处通常太小，不及确保此许可证的副本总是伴随该软件所带来的不便。

对这些程序，我们推荐 Apache 许可证版本 2.0[^3]。这是一种包容型（非左版）软件许可证，它拥有阻止贡献者和分发者发起专利侵权诉讼的条款。这并不能使得软件对于专利威胁免疫（软件许可证不能做到这一点），但是它确实能够阻止专利持有人设置“诱饵掉包”陷阱，在此，他们基于自由条款发布软件，然后迫使接受者同意专利授权许可种的非自由条款。

在包容型许可证中，Apache 许可证版本 2.0 是最好的；因此如果您不论由于何种原因想要使用包容型许可证，我们推荐使用它。

### 库

对于库，我们区分三种情况。

某些库实现了与限制性标准竞争的自由标准，例如 Ogg Vorbis（它与 MP3 音频竞争）和 WebM（它与 MPEG-4 视频竞争）。对于这些项目，代码的广泛使用对于推进自由软件事业至关重要，相对于该项目代码的左版能够带来更多好处。

对于这些特殊的情况，我们推荐 Apache 许可证版本 2.0。

对于所有其他库，我们推荐某种左版许可证。如果开发者已在使用某种基于非自由许可证或者包容型许可证发布的已经建立起来的替代库，我们建议使用 GNU 宽通用公共许可证（LGPL）。

不像第一种情况，那里的库实现了某种在伦理上更为优越的标准，这里的库就其自身而言的采用并不会实现任何特别的客观目标，因此完全没有理由回避左版。然而，如果您要求使用您的库的开发者基于左版发布他们的整个程序，他们将会简单地使用可用的替代库之一，这样也不能推进我们的事业。LGPL 被设计为填补这些情况之间的中间地带，允许私有软件开发者使用被它覆盖的库，但是提供一种弱左版以赋予用户关于库代码本身的自由。

对于提供了专门功能，并且不会面对根深蒂固的非左版或者非自由的替代库的竞争的库，我们推荐使用简单的 GNU GPL。如需获知原因，请参阅“为何您不应为您的下一个库使用 LGPL”，位于<https://gnu.org/licenses/why-not-lgpl.html>。

### 服务器软件

如果其他人可能会使得您的程序的改良版本在服务器上运行，并且不再将他们的版本分发给任何其他人，而您担心这会将你所发布的版本置于不利地位，我们推荐 GNU Affero 通用公共许可证（AGPL[^4]）。AGPL 的条款和 GPL 的几乎相同；仅有的实质性区别是它拥有一个额外的条款以确保通过网络用此软件的人们能够获得它的源代码。

AGPL 的条件并不能应对**用户**将他们的计算或者数据托付给某些其他人的服务器时可能产生的问题。例如，它不会阻止作为软件替代品的服务（SaaSS）拒绝用户的自由[^5]——但是大多数服务器并不去做 SaaSS。如需获得关于这些问题的更多信息，请阅读“为何使用 AGPL”，位于<https://gnu.org/licenses/why-affero-gpl.html>。

## 文档

我们推荐 GNU 自由文档许可证（GFDL）用于教程、参考手册和其他大型文档作品。它是一个用于教育作品的强左版许可证，最初针对软件文档编写，并且包括了那些具体应对这些作品被分发或者修改时所产生的常见问题的条款。

对于简短、次要的文档作品，诸如参考卡片，最好使用 GNU 全面包容型许可证[^6]，由于一份 GFDL 的副本难以适配进一张参考卡片。不要用 CC-BY，由于它和 GFDL 不兼容。

对于 `man` 页面，如果页面很长，我们推荐 GFDL，而如果它很短，则推荐 GNU 全面包容型许可证。

有些文档包括了软件源代码。例如，一部编程语言手册可能包括供读者模仿的范例。您应该既基于 FDL 的条款在手册中包括它们，又基于另一种适合于软件的许可证来发布它们。如此做有助于使得在其他项目中使用这些代码变得简单。我们推荐您利用 CC0[^7]将小代码片断贡献给公有领域，并且基于相关软件项目所使用的相同许可证分发较大的代码片断。

## 用于程序的其他数据

本节讨论您可能会将其包括在软件中用于实际应用的所有其他作品。例如图标以及其他功能性或者有用的图形、字体和地理数据等。您也可以在艺术中遵循这些，尽管即使您不如此做我们也不会提出批判。

如果您正在专门针对某个软件项目的应用而创作这些作品，我们一般推荐您基于该软件相同的许可证发布您的作品。利用我们推荐的许可证如此做没有问题：GPL v3、LGPL v3、AGPL v3 和 GPL v2 都可以被应用于任何类型的作品——不只是软件——可获版权并且拥有某种用于修改的明确首选形式的作品皆可。使用与软件相同的许可证将会有助于分发者更容易遵守，并且避免任何关于潜在的兼容性问题的疑虑。使用另一种自由许可证可能也是恰当的，如果它提供了某些实践上的好处，例如同其他自由项目之间的更好的合作。

如果您的作品并非为了用于特定软件项目而创作，或者它不适合于使用与该项目相同的许可证，那么我们只能建议您选择一种适合于您的作品的左版许可证。我们在自己的许可证列表中列出了其中的一些[^8]。如果没有许可证看起来特别合适，知识共享：署名——相同方式共享（CC BY-SA[^9]）是一种可用于多种不同作品的左版许可证。

[^1]: 参见我们反对数字限制管理的运动，位于[DefectiveByDesign.org](https://DefectiveByDesign.org)。

[^2]: 位于<https://gnu.org/licenses/gpl-faq.html>。

[^3]: 参见<https://apache.org/licenses/LICENSE-2.0>以获得此许可证的完整文本。

[^4]: 参见<https://gnu.org/licenses/agpl.html>以获得此许可证的完整文本。

[^5]: 参见“服务器真正是在为谁服务？”以获得关于 SaaSS 的问题的更多信息。

[^6]: 参见<https://gnu.org/licenses/license-list.html#GNUAllPermissive>。

[^7]: 参见<https://creativecommons.org/about/cc0>以获得关于此许可证的更多信息。

[^8]: 参见<https://gnu.org/licenses/license-list.html#OtherLicenses>。

[^9]: 参见<https://gnu.org/licenses/license-list.html#ccbysa>以获得关于使用此许可证的更多信息。

著作权所有 (C) 2011, 2013, 2014 自由软件基金会

本文最初于 2011 年发表于<https://gnu.org>。此版本是“自由软件，自由社会：Richard M. Stallman 文选，第三版”（波士顿：GNU Press，2015）的一部分。

本文基于知识共享：署名——禁止演绎（CC BY-ND）4.0 国际版许可证（<https://creativecommons.org/licenses/by-nd/4.0/>）。

[返回目录](00_index.html)

