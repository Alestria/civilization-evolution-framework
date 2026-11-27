# Writer 分叉的公开档案试编码

这次试编核查少量历史源码、发布记录、项目公告与代码活动，以检查《文明分化与整合演化哲学》V0.4.3 的连接状态向量能否实际填报。它对应 [§7.2 的四字段](../docs/v0.4.3.md#72-连接状态向量)和 [H9](../docs/v0.4.3.md#119-分叉后的社会关系)。这是目的性档案样本，未预登记方向性研究，也未估计 H9 的效应。

| 字段 | 本轮记录 |
|---|---|
| 接口连续性 | 分叉后所选版本的 Writer ODT 读写配置入口均保留；分叉前仅确认文档级 ODT 基线，未确认源码注册配置。实际打开、保存与跨程序往返不明。 |
| 组织关系连续性 | 找到两端活动与技术传递线索，缺少可比的配对基准和季度覆盖，跨期变化不明。 |
| 身份认同连续性 | 不明，缺少同一观察单位的纵向材料。 |
| 相互承认连续性 | 不明，项目接触意向不足以判定维护者层的持续互认。 |

## 接口连续性试编码（$`I_f`$）

**对象与取样规则。** 以 2010-09-28 分叉为时间锚，完整研究沿用分叉前 12 个月、分叉后 24 个月。试编码抽取三处版本档案。分叉前采用 OpenOffice.org 3.2 同期 Writer 手册和 2010-04-15 的 [Writer 入门指南 ODT 档案](https://wiki.openoffice.org/wiki/Documentation/OOo3_User_Guides/Chapters_ODT#Getting_Started_Guide_-_V3.2) 建立基线。分叉后选 LibreOffice 首个稳定版源码点 3.3.0.4（2011-01-25 发布 3.3），再比较 2012 年 5 月近同期的 LibreOffice 3.5.3.2 与 Apache OpenOffice 3.4.0（AOO340）。后两者相隔不足一周发布。这一比较跨过 OpenOffice.org 进入 Apache 后的治理变更，只用于检查所选技术接口有无共同声明。另核查 [LibreOffice 3.3 发布公告](https://blog.documentfoundation.org/blog/2011/01/25/the-document-foundation-launches-libreoffice-3-3/)、[LibreOffice 3.5.3 公告档案](https://listarchives.libreoffice.org/fr/announce/maillist.html) 和 [Apache OpenOffice 3.4 发布公告](https://www.openoffice.org/news/aoo34.html)。

**编码规则。** 分列四层证据：文档声明、源码入口登记、历史版本实际打开及保存、跨版本往返后预定功能保留。源码登记要求档案同时给出 `.odt` 扩展名、ODF 文本 MIME、Writer 类型和 `IMPORT`／`EXPORT` 两个标志。按版本固定标签读取 `types/writer8.xcu` 与 `filters/writer8.xcu`，提取并比较字段。只有两端都具备入口登记才将该版本对记为“配置入口保留”。运行层另行编码“通过／失败／不明”。双向状态按 A→B→A、B→A→B 分列。单端的读写入口和 ODF 规范声明不用于推断功能保留、默认子版本或双向往返结果。

| 窗口及单位 | 实际核对的档案字段 | 试编码 | 缺失或局限 |
|---|---|---|---|
| 分叉前，OpenOffice.org 3.2 Writer | [2010 年版入门手册](https://wiki.openoffice.org/w/images/archive/e/e1/20100418102930%210100GS3-GettingStartedOOo3.pdf) 标明 Writer 保存 `.odt`，同期档案索引登记 Writer 入门指南为 ODT。 | 文档级 ODT 基线存在。 | ODT 文件索引已定位，文件下载超时，未取得文件哈希，也未在历史程序中打开；未核实该版本源码中的类型与过滤器注册配置。 |
| 分叉初段，LibreOffice 3.3.0.4 | [文件类型](https://github.com/LibreOffice/core/blob/libreoffice-3.3.0.4/filter/source/config/fragments/types/writer8.xcu) 登记 `odt` 和 `application/vnd.oasis.opendocument.text`，指向 `writer8`。[过滤器](https://github.com/LibreOffice/core/blob/libreoffice-3.3.0.4/filter/source/config/fragments/filters/writer8.xcu) 同时登记读入与导出。 | LibreOffice 单端配置入口保留。 | 同期 OpenOffice.org 3.3 手册可查，未将文档级证据替代同口径源码证据。双向运行不明。 |
| 分叉后 2012 年 5 月，LibreOffice 3.5.3.2 ↔ Apache OpenOffice 3.4.0 | [LibreOffice 类型](https://github.com/LibreOffice/core/blob/libreoffice-3.5.3.2/filter/source/config/fragments/types/writer8.xcu) 及[过滤器](https://github.com/LibreOffice/core/blob/libreoffice-3.5.3.2/filter/source/config/fragments/filters/writer8.xcu)、[Apache 类型](https://github.com/apache/openoffice/blob/AOO340/main/filter/source/config/fragments/types/writer8.xcu) 及[过滤器](https://github.com/apache/openoffice/blob/AOO340/main/filter/source/config/fragments/filters/writer8.xcu) 均登记相同的扩展名、MIME 和类型，且都有 `IMPORT` 与 `EXPORT`。 | 两端配置入口均保留。 | LibreOffice 两个版本的各自配置文件哈希相同，属于同一配置沿用，不能当作独立重复观测。两方向运行、往返保真和默认 ODF 子版本均未在运行环境中核验。 |

本轮实际完成历史注册配置的档案编码。未检测到所需历史 Writer 运行环境，因此共同接口的实际可用性仍记“不明”。下一轮可先取得同一份基线 ODT 并固定 SHA-256，再加入预先定义的基础段落样式、表格与编号，以及含注释或修订记录的扩展样本。在独立、隔离的历史运行环境中按相同 ODF 保存配置双向往返，分别记录打开结果、保存结果和各功能是否保留。所选窗口的声明连续性仅可用于改进取样与编码手册。$`O_r`$、$`Rec_{\mathrm{id}}`$ 与 $`Rec_{\mathrm{ack}}`$ 需要独立档案，H9 的方向需要可比版本对及独立观察的组织协作变化。

## 组织关系连续性 $`O_r`$ 的档案试编码

观察对象固定为 Writer 的 ODF 文档读写活动及相应维护者。基准窗为 2009-09-28 至 2010-09-27，后续窗为 2010-09-28 至 2012-09-27，另登记 2011-06-13 的治理转换。此次从公开的项目公告、维护记录和代码历史中挑选判别边界不同的记录，检验编码规则能否区分来源。这个目的样本只适合验证字段和取证流程。

**主要映射规则。** 分叉前，某两人必须出现在同一议题或补丁的互补行为中，例如一人提交、另一人实质审核或复测。分叉后按当期项目中的可追溯维护行为安排两端。双项目活跃者保留双归属，无法定位的一端标为“不明”。按“维护者配对 × 季度”计数。一个去重后的事件只有在双方同时代的档案证实对同一个 Writer ODF 事项存在协作行动时才计作组织联系。公共代码血缘、版权头更换、单向移植、同一作者双投、单方转引和邀请各用单独标签。邮件转引、仓库镜像和同一补丁的重复记录不增加事件数。只有明确覆盖该季度、双方项目及相应记录渠道，才可把未发现计为零。

**替代映射规则。** 用可核验的同一技术任务或问题号取代人名，将两项目的公开处理行为并入“问题 × 季度”记录。单向移植可以登记为技术传递，即使无法识别维护者对。当期资料只证明一端动作时，仍不编码为双方协作。基准仍要求有分叉前的同一任务。分别报告两种映射的结果，保留别名冲突、无法归属和剔除理由。

| 时间和记录 | 观察到的行为 | 主要口径 / 替代口径 |
|---|---|---|
| 2010-09-13，分叉前的 Writer 测试提交，涉及 Writer 段落与文本框测试。[源码历史](https://github.com/LibreOffice/core/commit/ba5bfd3356723ef7a003d41c3402adf79d15235d) | 保留在现今 LibreOffice 源码历史中的早期 Writer 工作，可作为沿革和议题检索入口。该提交只提供一个动作与一个作者。 | 基准中的 Writer 活动可确认。跨分支候选维护者对尚未确认，技术任务动作可记但无法映射为一对协作。 |
| 2010-09-28，TDF 宣布成立和 LibreOffice 项目。[当日公告](https://listarchives.documentfoundation.org/www/announce/msg00000.html) | 公告确认新治理安排与共同项目来源，并记有参与邀请。 | 治理事件和意向单列。两种组织协作口径均不计。 |
| 2011-06-01，TDF 对代码捐赠 Apache 的公开回应。[TDF 公告](https://blog.documentfoundation.org/blog/2011/06/01/statement-about-oracles-move-to-donate-openoffice-org-assets-to-the-apache-foundation/) | 声明表达愿意接触 ASF，并提及对方公开释放的接触意向。未列 Writer ODF 的共同交付。 | 机构接触意向可记录。具体维护者配对及技术任务合作均不明。 |
| 2011-09-22 与 2011-11-30，两方向的代码传递边界样本。[LibreOffice 提交 d543cb2](https://github.com/LibreOffice/core/commit/d543cb25e16b1f80d0b2826dc1046ba752199e81) [Apache OpenOffice 提交 3890ecf](https://github.com/apache/openoffice/commit/3890ecf29ce1933bd0c2429da8f241ce13bbe968) | 前者明确移植 Apache SVN 修订，却改动幻灯放映路径。后者明确基于 LibreOffice 提交，改动俄语词典。 | 两项均有单向传递痕迹，分别排除出 Writer ODF 读写的主要和替代组织结果。 |
| 2012-06-22，LibreOffice 对 Apache 许可代码的重整。[提交 ecf9432](https://github.com/LibreOffice/core/commit/ecf943247fb734739141d6074d1169ab922b2523) | 提交改动了 Writer 的多个头文件。现有记录能定位重整动作与模块，未证实双方在同一 Writer ODF 事项共同工作。 | 单向采用线索。替代口径可登记 Writer 模块涉及该动作，具体 ODF 事项与协作状态仍不明。 |
| 2011-09-30，LibreOffice 的 Writer 字号样式问题链接 OpenOffice.org 同题旧记录。[LibreOffice 41360](https://bugs.documentfoundation.org/show_bug.cgi?id=41360) [OpenOffice.org 4279 的发布快照](https://www.openoffice.org/development/releases/1.9.m79_snapshot.html) [Apache 4279](https://bz.apache.org/ooo/show_bug.cgi?id=4279) | LibreOffice 的索引快照可见同题链接，OpenOffice.org 历史快照可核对编号与主题。Apache 问题正文要求登录，不能核实两端同期维护行为。旧发布快照也早于规定基准窗。 | 可登记跨问题转引，维护者配对和基准窗内双端动作均不明。替代问题映射增加一个可追踪单元，组织结果仍不明。 |
| 2012-11，ApacheCon 记录涉及两项目 OOXML 改进的用户倡议。[Apache 项目报告](https://openoffice.apache.org/blog/apache_openoffice_track_at_apachecon1) | 报告提供跨项目活动的明确主题与参与方。 | 日期超过截止日，格式为 OOXML，排除。保留这条以检验日期和格式筛选能否挡住表面上很接近的案例。 |

两种映射均得到可追溯的沿革、单向传递和接触线索。现有目的样本不足以填入基准与后续季度的合格配对分母，$`O_r`$ 的跨期变化标为“不明”。$`Rec_{\mathrm{id}}`$ 与 $`Rec_{\mathrm{ack}}`$ 未取得同一观察单位的纵向材料，也各自记为“不明”。此次为单次档案试编码，未计算编码一致率，H9 的方向性检验仍缺同口径对照。下一轮应以既定窗口分别提取 Writer 模块的双端提交和对应维护讨论，再由两人独立重编上述边界样本和扩展样本。关于项目层贡献者留存与社区演化，已有不同分析单位的同行研究可供核对。[Gamalielsson 与 Lundell，2014](https://doi.org/10.1016/j.jss.2013.11.1077)

## 独立试复核

另一轮 AI 编码在未看到初编记录的情况下，用同一判定规则复核固定材料。核对了 2012 年两端的类型与过滤器文件、分叉前的 Writer 提交、2011 年接触声明及 2012 年的代码重整提交。两轮均将共同配置入口标为可观察，将历史运行和严格双边 Writer ODF 协作标为不明，并区分了单边代码动作与接触意向。复核范围为小样本规则校准，完整双人编码与一致性估计仍待开展。

复核补定位到分叉前 Writer 测试脚本中的 `hyphenationNew.odt` 和本地打开调用。该记录支持当时以 ODT 为测试样本的做法，未附运行结果，也未识别符合规则的双方维护者配对。2012 年重整提交中核查到的 Writer 过滤器示例仅修改许可头，另作为代码重整记录。见[分叉前测试脚本](https://github.com/LibreOffice/core/blob/ba5bfd3356723ef7a003d41c3402adf79d15235d/testautomation/writer/optional/includes/formatparagraph/w_formatparagraph2.inc#L764-L785)和[过滤器文件改动](https://github.com/LibreOffice/core/commit/ecf943247fb734739141d6074d1169ab922b2523)。
