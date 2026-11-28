# OpenOffice 与 LibreOffice 分叉研究的证据索引

[返回研究正文](README.md)

## 1. 事件索引

| 编号 | 时间 | 原始材料所见 | 用途与限制 |
| --- | --- | --- | --- |
| G01 | 2010-09-28 | 社区发起者公布 LibreOffice 项目和文档基金会倡议，并邀请 Oracle 参与。基金会正式注册发生在后来。[当日公告](https://listarchives.documentfoundation.org/www/announce/msg00000.html) | 分叉时间锚与参与意向。 |
| G02 | 2011-01-25 | 文档基金会公布 LibreOffice 3.3。[发布公告](https://blog.documentfoundation.org/blog/2011/01/25/the-document-foundation-launches-libreoffice-3-3/) | 单独发布的组织事件及早期技术档案定位。 |
| G03 | 2011-06 至 2011-10 | 6 月 1 日提出源码捐赠，6 月 13 日 Apache 孵化项目获准，8 月 29 日源码导入 ASF 的 SVN。10 月 14 日 ASF 已公开说明其持有项目商标及官方代码。文档基金会 6 月 1 日的回应表达了接触意向。[孵化档案](https://incubator.apache.org/projects/openofficeorg.html) · [ASF 声明](https://news.apache.org/foundation/entry/the_apache_software_foundation_statement) · [文档基金会回应](https://blog.documentfoundation.org/blog/2011/06/01/statement-about-oracles-move-to-donate-openoffice-org-assets-to-the-apache-foundation/) | 分别定位治理交接和机构意向，商标转移具体日期未核实。 |
| G04 | 2011-06-15 | 文档基金会列出咨询委员会的首批机构成员。[基金会公告](https://blog.documentfoundation.org/blog/2011/06/15/first-tdf-advisory-board-members-demonstrate-wide-corporate-support-for-libreoffice/) | 外部支持来源线索，无法转化为资金或人力依赖份额。 |
| G05 | 2012-02 至 2012-10 | 文档基金会于 2 月 17 日在柏林正式成立。Apache OpenOffice 于 5 月 8 日发布 3.4，ASF 董事会 10 月 17 日通过建立项目管理委员会的决议。[基金会注册公告](https://blog.documentfoundation.org/blog/2012/02/20/the-document-foundation-officially-incorporated-in-berlin-germany/) · [Apache 发布](https://www.openoffice.org/news/aoo34.html) · [ASF 董事会决议](https://whimsy.apache.org/board/minutes/OpenOffice.html) | 两端组织里程碑，无法据此判断维护者之间有无协作。 |
| G06 | 2012-11 | LibreOffice 提交明确引用 Apache SVN r1220836 的 SVG 修改，Apache 项目随后也发表说明。[LibreOffice 提交](https://github.com/LibreOffice/core/commit/44cfc7cb6533d827fd2d6e586d92c61d7d7f7a70) · [Apache 项目说明](https://blogsarchive.apache.org/OOo/entry/good_news_libreoffice_is_integrating) | 一次有明确方向的代码采用，超出 Writer ODT 范围。 |
| G07 | 2012-05、2013-07 | Apache OpenOffice 3.4 发布公告指明 Apache License 2.0。LibreOffice 4.1.0.4 的 Writer 类型文件头注明 MPL 2.0，并保留所含 Apache 代码的许可说明。[Apache 发布公告](https://www.openoffice.org/news/aoo34.html) · [LibreOffice 类型文件](https://github.com/LibreOffice/core/blob/libreoffice-4.1.0.4/filter/source/config/fragments/types/writer8.xcu) | 分别记录发布许可与单文件的许可声明，可供追查代码来源，未借此推断双方的制度互认或许可兼容范围。 |

## 2. Writer ODT 配置档案

**基准与取样。** 分叉前采用 2010 年 OpenOffice.org 3.2 的同期手册核对 Writer 的 ODT 保存入口，另见当时调用 ODT 测试文档的脚本。未取得同口径的分叉前源码注册记录或历史测试的执行结果。2011 年仅确认 LibreOffice 3.3.0.4 这一端的两份注册文件。此后从 2012—2015 年每年选一组发布时间相距不超过一个月的发行版，重查 2012 年试编码样本并新增后面三组。这里的取样用于档案对照，版本之间的月份仍有空档。[分叉前手册](https://wiki.openoffice.org/w/images/archive/e/e1/20100418102930%210100GS3-GettingStartedOOo3.pdf) · [分叉前测试脚本](https://github.com/LibreOffice/core/blob/ba5bfd3356723ef7a003d41c3402adf79d15235d/testautomation/writer/optional/includes/formatparagraph/w_formatparagraph2.inc#L764-L785) · [LibreOffice 3.3 类型](https://github.com/LibreOffice/core/blob/libreoffice-3.3.0.4/filter/source/config/fragments/types/writer8.xcu) · [LibreOffice 3.3 过滤器](https://github.com/LibreOffice/core/blob/libreoffice-3.3.0.4/filter/source/config/fragments/filters/writer8.xcu)

以下链接固定到发布标签下的 `types/writer8.xcu` 和 `filters/writer8.xcu`，表中给出所读文件的 Git blob 标识。发布日期取自项目公开记录。[Apache 发布列表](https://wiki.openoffice.org/wiki/Product_Release) · [LibreOffice 3.5.3 发布](https://blog.documentfoundation.org/blog/2012/05/02/the-document-foundation-announces-libreoffice-3-5-3/) · [LibreOffice 4.1 日期](https://blog.documentfoundation.org/blog/2015/07/29/the-road-to-libreoffice-5-0/) · [LibreOffice 4.3 发布](https://pt-br.blog.documentfoundation.org/2014/07/30/libreoffice-4-3-a-suite-office-sem-igual-so-para-voce/) · [LibreOffice 5.0.3 发布](https://blog.documentfoundation.org/blog/2015/11/03/the-document-foundation-announces-libreoffice-5-0-3-fresh-and-libreoffice-4-4-6-still/)

| 发布日期 | 版本 | 类型文件 | 过滤器文件 | 类型检测组件（省略 `com.sun.star.`） | 类型记录的 `Preferred` |
| --- | --- | --- | --- | --- | --- |
| 2012-05-02 | LibreOffice 3.5.3.2 | [`b57dbde222f29956f330d1859dfbdd710bfe02f2`](https://github.com/LibreOffice/core/blob/libreoffice-3.5.3.2/filter/source/config/fragments/types/writer8.xcu) | [`bcfd55640e79f43c5f1ea74093101e77233c9248`](https://github.com/LibreOffice/core/blob/libreoffice-3.5.3.2/filter/source/config/fragments/filters/writer8.xcu) | `text.FormatDetector` | `false` |
| 2012-05-08 | Apache OpenOffice 3.4.0 | [`e86e1d94b7da87d3854b947c9a8499e666d97dbf`](https://github.com/apache/openoffice/blob/AOO340/main/filter/source/config/fragments/types/writer8.xcu) | [`be99a6dba2bfafdd55c8e7f8d1358056d842d3ce`](https://github.com/apache/openoffice/blob/AOO340/main/filter/source/config/fragments/filters/writer8.xcu) | `text.FormatDetector` | `false` |
| 2013-07-23 | Apache OpenOffice 4.0.0 | [`e86e1d94b7da87d3854b947c9a8499e666d97dbf`](https://github.com/apache/openoffice/blob/AOO400/main/filter/source/config/fragments/types/writer8.xcu) | [`be99a6dba2bfafdd55c8e7f8d1358056d842d3ce`](https://github.com/apache/openoffice/blob/AOO400/main/filter/source/config/fragments/filters/writer8.xcu) | `text.FormatDetector` | `false` |
| 2013-07-25 | LibreOffice 4.1.0.4 | [`7ba69bb20b175f6f818ca33be593276c64d3784d`](https://github.com/LibreOffice/core/blob/libreoffice-4.1.0.4/filter/source/config/fragments/types/writer8.xcu) | [`fd938e72ba13166ac26b47ebb4acafc1b1c841c9`](https://github.com/LibreOffice/core/blob/libreoffice-4.1.0.4/filter/source/config/fragments/filters/writer8.xcu) | `text.FormatDetector` | `false` |
| 2014-07-30 | LibreOffice 4.3.0.4 | [`c5cf5dd4e5b38a3abb6d2894f5109e22a39d24d8`](https://github.com/LibreOffice/core/blob/libreoffice-4.3.0.4/filter/source/config/fragments/types/writer8.xcu) | [`fd938e72ba13166ac26b47ebb4acafc1b1c841c9`](https://github.com/LibreOffice/core/blob/libreoffice-4.3.0.4/filter/source/config/fragments/filters/writer8.xcu) | `comp.filters.StorageFilterDetect` | `false` |
| 2014-08-21 | Apache OpenOffice 4.1.1 | [`e86e1d94b7da87d3854b947c9a8499e666d97dbf`](https://github.com/apache/openoffice/blob/AOO411/main/filter/source/config/fragments/types/writer8.xcu) | [`be99a6dba2bfafdd55c8e7f8d1358056d842d3ce`](https://github.com/apache/openoffice/blob/AOO411/main/filter/source/config/fragments/filters/writer8.xcu) | `text.FormatDetector` | `false` |
| 2015-10-28 | Apache OpenOffice 4.1.2 | [`e86e1d94b7da87d3854b947c9a8499e666d97dbf`](https://github.com/apache/openoffice/blob/AOO412/main/filter/source/config/fragments/types/writer8.xcu) | [`be99a6dba2bfafdd55c8e7f8d1358056d842d3ce`](https://github.com/apache/openoffice/blob/AOO412/main/filter/source/config/fragments/filters/writer8.xcu) | `text.FormatDetector` | `false` |
| 2015-11-03 | LibreOffice 5.0.3.2 | [`8a2effbdea0e3b2e243383f0e79454c986b11aaf`](https://github.com/LibreOffice/core/blob/libreoffice-5.0.3.2/filter/source/config/fragments/types/writer8.xcu) | [`410b3a77e7172f347fdca5244d88dc9a193291aa`](https://github.com/LibreOffice/core/blob/libreoffice-5.0.3.2/filter/source/config/fragments/filters/writer8.xcu) | `comp.filters.StorageFilterDetect` | `true` |

八个版本均声明 `Extensions=odt`、`MediaType=application/vnd.oasis.opendocument.text`、`PreferredFilter=writer8`，过滤器均登记 `Type=writer8`，其标志包含 `IMPORT` 与 `EXPORT`，文档服务均为 `com.sun.star.text.TextDocument`。这些字段满足“共同配置入口”的判据。Apache 一侧四个时点沿用同一对文件，整张表共九个不同的 blob。表中的检测组件和 `Preferred` 描述源代码配置。内部 `FileFormatVersion=6800` 无法据以确定默认保存的 ODF 规范版本或实际处理结果。

## 3. 互操作档案

| 编号 | 档案 | 可登记的观察 | 不能从该记录推出的结果 |
| --- | --- | --- | --- |
| T01 | 2013 年 LibreOffice 大会演讲摘要，列出 LibreOffice 4.0/4.1 和 Apache OpenOffice 3.4/4.0 等参与比较的版本。[演讲摘要](https://conference.libreoffice.org/2013/en/program/open-document-format/a-multiplatform-tool-for-document-interoperability-testing.html) | 已有跨版本互操作测试工作。 | 摘要没有公开逐版本的测试结果。 |
| T02 | 2014 年伦敦 ODF Plugfest 的当年报道，记载 LibreOffice、Apache OpenOffice 和 EuroOffice 参与修订记录的互操作演示。[活动报道](https://www.collaboraonline.com/blog/major-announcements-from-the-odf-plugfest/) | 可登记一次特定功能的跨软件演示，报道由活动参与方发布。 | 未注明相关版本、文件、交换方向及结果明细，无法复现该次演示或外推到其他文档。 |
| T03 | 2015 年海牙 ODF Plugfest 主办方报告中“Day 2 – Plugtesting”的被测软件名单。[主办方报告](https://www.odfplugfest.org/2015-thehague/report.html) | 列出了 LibreOffice 4.3/5.0，没有列出 Apache OpenOffice。 | 该次活动未计入双项目运行证据。 |
| T04 | 2015 年 11 月 Apache OpenOffice 用户论坛，一位回复者说用 LibreOffice 5.0.3 转存 ODT，提问者随后确认文件可以打开。[同一讨论串](https://forum.openoffice.org/en/forum/viewtopic.php?t=80148) | 一份文档，LibreOffice → Apache OpenOffice 方向，论坛自报。提问时列出的环境为 Apache OpenOffice 4.1.1 与 Windows Vista，确认时未重述版本。 | 反向交换、往返保真、修订或样式保留均不明。表中的 4.1.2 无法从此记录获得运行结果。 |

本次未运行历史版本，也未收录论坛附件。以上演示和用户记录只按各自公开描述使用。资料来源及观察单位不同，未合计成功率。

## 4. 组织、身份与承认的编码边界

沿用旧试编码的同事项标准。两项目在同一 Writer ODT 议题或补丁上各有可辨认的实质行动时，才登记跨项目维护关系。编码单位为维护者配对 × 季度，备选单位为问题 × 季度。共同版本库历史、许可证允许复用、单向引用和贡献者在两个项目登记各记原有类别。2012 年 6 月 LibreOffice 对 Apache 许可代码的重整涉及 Writer 头文件，但未确认对侧参与同一 ODT 事项。没有分叉前配对和双端季度覆盖，组织连续性的变化仍不明。[重整提交](https://github.com/LibreOffice/core/commit/ecf943247fb734739141d6074d1169ab922b2523) · [维护事项试编码](../../case-studies/writer-fork-pilot.md)

身份认同需要同一观察单位在不同时点表达归属，相互承认需要两侧的接纳、资格认可或拒绝行为。机构更名、合作邀请和使用同一开放格式均保留为背景事件。目前两个连续性字段均不明。G04 可以证明咨询支持安排的存在，不能判定是否共享人员、经费或基础设施。本阶段为回顾性档案比较，选择、纳入与排除理由有记录，未作事前登记或本研究样本的全量独立双人编码。

## 5. 研究基线

Gamalielsson, J., & Lundell, B. (2014). Sustainability of Open Source software communities beyond a fork: How and why has the LibreOffice project evolved? *Journal of Systems and Software, 89*, 128–145. [https://doi.org/10.1016/j.jss.2013.11.1077](https://doi.org/10.1016/j.jss.2013.11.1077)

复核时重点看原文 §3 的观察窗和资料来源、§4.2 的跨项目参与以及 §7.1 的时间与样本限制。论文的版本库记录涵盖多种模块和贡献类别，12 位访谈对象来自 LibreOffice 一侧。已有研究提供了贡献者流动的项目级基线。本研究用到的具体 Writer ODT 交换、发布配置及同一维护事项采用上文的单位单独登记。
