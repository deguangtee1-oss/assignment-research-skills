# APA 7 引用核查

本文件是项目 APA 7 类型字段和详细核查步骤的**唯一主要维护源**。可单独复制的短指令见 [`prompts/04-APA7引用检查.md`](../../../prompts/04-APA7引用检查.md)。

## 适用范围与权威依据

先检查当前 Coursework、Rubric 和教师指示；当前作业明确规定的格式优先。若没有作业级说明，核对 [TAR UMT Library 当前官方引用指南](https://library.tarc.edu.my/training-support/apa-referencing-style)及适用的课程/学科例外。TAR UMT Library 指南将 APA 7 列为主要引用风格，同时说明部分课程可能采用其他风格。只有在 APA 7 确认适用于当前作业时才使用本清单；适用规则尚未确认时标记「待确认」，不因一般 APA 7 细节直接判定违规，也不静默套用其他风格。

编写及核对本清单时查阅了 APA Style 官方资料（核对日期：2026-10-25）：

- [Reference Examples](https://apastyle.apa.org/style-grammar-guidelines/references/examples)：按作品类型选择例子；其中说明政府报告属于报告类别，网站上的一般网页才使用网页类别。该目录含期刊文章、书籍、编辑书籍章节、报告、网页等不同类型。
- [Elements of Reference List Entries](https://apastyle.apa.org/style-grammar-guidelines/references/elements-list-entry)：作者、日期、标题、来源四个条目组成部分，并按来源情况处理相应元素。
- [DOIs and URLs](https://apastyle.apa.org/style-grammar-guidelines/references/dois-urls)：DOI/URL 的纳入和显示取决于作品及获取来源；链接存在不等于书目字段准确。
- [Missing Reference Information](https://apastyle.apa.org/style-grammar-guidelines/references/missing-information)：说明缺失作者、日期、标题或来源时的处理方式；执行时仍需根据具体作品类型查阅对应示例。
- [Journal Article References](https://apastyle.apa.org/style-grammar-guidelines/references/examples/journal-article-references)、[Book/Ebook References](https://apastyle.apa.org/style-grammar-guidelines/references/examples/book-references)、[Chapter in an Edited Book/Ebook References](https://apastyle.apa.org/style-grammar-guidelines/references/examples/edited-book-chapter-references)、[Report by a Government Agency References](https://apastyle.apa.org/style-grammar-guidelines/references/examples/report-government-agency-references)、[Webpage on a Website References](https://apastyle.apa.org/style-grammar-guidelines/references/examples/webpage-website-references)：对应来源类型的示例及条件说明。
- [Basic Principles of Citation](https://apastyle.apa.org/style-grammar-guidelines/citations/basic-principles)：说明文内引文与参考文献表的对应关系。

APA Style 页面说明其指南依据第七版 Publication Manual / Concise Guide，并会在相关页面记载更新；实施核查时应重新查看现行页面和本次教师要求。涉及官方示例未覆盖、规则有歧义或当前要求不同的情形，标为「待确认」，不得凭记忆补规则。

## 1. 检查前输入

请提供或确认：

- 当前 Assignment 草稿及 References；
- 教师对此次作业的引用格式指示；若没有，提供学校当前正式引用指南；
- 允许进行的在线查询范围；
- 若要核实论点支持，提供相关来源原文或可访问材料及目标主张。

缺少必要材料时，先报告可完成的有限检查和缺项。不要把格式检查描述成来源内容核验。

## 2. 每条参考文献的状态字段

每条来源分别记录以下状态；不可合并为单一的「已验证」：

| 项目 | 记录内容 | 建议状态 |
|---|---|---|
| 来源存在性 | 是否找到与该作品匹配的出版者、期刊、机构或其他可复查记录；记录核查链接 | 已找到记录（尚未核实）/ 存在性已核实 / 本次查询未找到（不代表不存在）/ 查询失败 / 记录冲突 / 待确认 |
| 书目信息 | 按类型核对适用字段；保留来源值、核查值和核查依据 | 已核实 / 部分核实 / 缺失 / 待确认 / 不适用 |
| DOI/URL | 是否存在、是否能访问、是否指向所引作品；记录检查结果 | 存在且可访问 / 存在但无法访问 / 未找到 / 待确认 / 不适用 |
| 阅读范围 | 实际看过的材料 | 全文 / 摘要 / 元数据 / 指定部分 / 未读 |
| 具体主张支持 | 实际阅读材料支持被引用主张到什么程度 | 直接支持 / 部分支持 / 间接支持 / 不支持 / 待确认 |

DOI/URL 可访问只能说明链接状态，不能独立证明书目信息正确、作品真实可信或原文支持论点。只读摘要、元数据或部分内容时，不能声称阅读全文或超出阅读范围概括支持结论。

## 2A. 免费公开来源与查询限制

- 优先使用 Crossref [公开 REST API](https://www.crossref.org/documentation/retrieve-metadata/rest-api/access-and-authentication/) 核对 DOI 和其登记元数据；无需注册。官方当前限额为 Public 池 5 次/秒、并发 1；Polite 池 10 次/秒、并发 3。默认使用 Public 池即可；不要为了提高额度发送个人邮箱。返回记录反映登记元数据，不是全文或内容真实性担保。
- OpenAlex 可用于免费元数据检索：其官方当前说明无 Key 访问每日预算为 $0.10，免费 Key 为 $1/日（需要账户和邮箱确认）；基本无 Key 请求上限为 10 次/秒，Key 为 30 次/秒。只有在无需新建账户/Key 的免费无 Key 额度内使用；预算用尽即停止，等待免费额度重置或改用人工公开页面，严禁启用按量付费。OpenAlex PDF/XML 下载目前按文件收费，因此不得调用付费全文下载功能。核对当天规则：[认证/限额](https://help.openalex.org/api/authentication/)、[定价](https://help.openalex.org/access/pricing/)。
- Semantic Scholar 多数 API 端点可匿名使用；官方说明未认证请求共用 1000 次/秒的全局池，高峰时可能进一步限流；API Key 的入门额度是 1 次/秒，但本流程不要求或索取 Key。仅使用当前公开免费端点；遇到限流立即停止。([官方 API 说明](https://www.semanticscholar.org/product/api))
- 遇到 HTTP 429、配额/限额提示、超时、服务故障、登录墙或不一致记录时立即停止该次接口查询；记录为“查询失败”“限额”或“记录冲突”，可改查无需付费的出版方/机构公开页面，仍无法确认则标“待确认”。不得自动转到付费服务、购买额度或绕过访问限制。
- 只向公开服务发送核验所需的最少标识（如 DOI、标题或作者检索词）；不发送整份作业、私人课程资料、未发表文本或认证秘密。
- 每个服务的可用记录、免费额度和 API 条款均可能变化；以服务官方页面的当前说明和响应为准。一个服务未返回记录不等于来源不存在；检索结果、摘要、DOI 和书目数据均不替代原文主张核查。

## 3. 按来源类型选择字段

下表是核查字段类别，不表示每一栏对所有作品都必需。先判断作品类型，再对每个字段填写：**要求分类**（必需 / 条件适用 / 不适用）、**实际值**、**核查依据**、**结果状态**（已核实 / 缺失 / 待确认 / 不适用）及原因。类型无法判定或 APA 官方示例不足时先标待确认。

| 来源类型 | 按官方示例重点检查的字段与条件 | 核查提示 |
|---|---|---|
| 期刊文章 | 作者；日期；文章标题；期刊名称；卷；期（若该期刊/文章有）；页码或文章编号；DOI（作品有 DOI 时）；URL（适用的无 DOI 在线作品） | 使用期刊文章专门示例；不要把数据库登录信息一概加入，也不要把缺少页码/期号自行补齐。若期刊确实没有相应元素，按官方缺项示例判断。 |
| 书籍/电子书 | 作者/编者；日期；书名；版次/卷册信息（如适用）；出版社；DOI 或稳定 URL（依作品与获取来源适用） | APA 官方示例区分作者书、编者书及特殊重印作品；电子书平台/设备不能凭记忆决定是否列入。 |
| 编辑书籍中的章节 | 章节作者；日期；章节标题；编者及角色；书名；章节页码（有分页时）；版次（如适用）；出版社；章节 DOI 或稳定 URL（适用时） | 先确认是编辑书章节还是作者书中的一章；APA 官方示例对作者书章节有单独说明，不能机械套用编辑书章节格式。 |
| 网页 | 个人或团体作者；具体日期（页面可确认时）；网页标题；网站名称（按作者与网站名称关系判断）；URL；检索日期（仅在官方条件适用时） | 先确认作品本身是否其实属于报告、期刊文章、书籍等其他类型；不能只因内容托管在网站就把它归为网页。 |
| 机构/政府报告 | 个人或机构作者；日期；报告标题；报告编号（如存在）；出版机构/来源；DOI 或 URL（依作品及获取情况适用） | 先按作品性质识别为报告；官方示例指出报告与一般网页分类不同。组织层级和作者/出版机构的具体处理须对照相应官方示例。 |

若实际作业涉及其他类型（例如新闻、数据集、论文、社交媒体或预印本），不要套用上述五类；从 APA 官方 Reference Examples 选择对应类别并补充核查依据。没有查到适用权威示例时标「待确认」。

## 4. DOI 与 URL 核查

1. 先确认是否有 DOI 或适用 URL；不要因为引用中缺少链接就猜测 DOI。
2. 若有 DOI，核对 DOI 指向的作品，并与出版者/期刊记录比较书目字段；若是 URL，核对页面是否指向所引作品并能否供读者访问。
3. 按作品类型及获取方式核对 APA Style 的 DOI/URL 纳入条件；链接可用性与 APA 字段/格式各自报告。
4. 链接跳转到错误作品、无法访问、只到登录页或内容不匹配时，标明具体情形；不要静默替换为猜测的地址。

## 5. 文内引用与 References 双向匹配

分别制作两方向核对结果：

1. **正文到 References：**从正文、表格、图、脚注或附录中识别引用，查找对应参考文献；核对作者拼写和日期。未匹配项列出所在位置。
2. **References 到正文：**逐条查找正文是否有相应引用；未匹配项列出条目。
3. 另列重复条目、作者/日期不一致、同名同年可能歧义及无法确定对应关系的记录。
4. 对 APA 官方规则中的例外（例如特定不可检索的个人通信或元分析中的参考列表）先确认其确实适用，再按相应规则处理；不要把例外泛化到普通来源。

APA Style 的基本原则是引用作品应与参考文献条目对应，但具体例外须按官方当前指导判断。不可仅凭文内作者年份相同就认定书目记录及来源支持均正确。

## 6. 论点支持及阅读范围

将每个被引用来源关联到正文中的具体主张；若可访问原文，记录页码、段落、表格或数据位置，并说明支持范围和限制。只读书目/元数据时，最多报告来源记录或书目信息核查，论点支持保持待确认。只读摘要时仅对摘要实际支持的有限主张作判断，并明确标明「仅摘要」。

## 7. 标准输出

按每条来源报告：

| 条目 | 来源类型及适用指南 | 字段要求/值/依据/状态 | 来源与 DOI/URL 状态 | 阅读范围 | 主张及原文支持 | 文内—References 匹配 | 问题与下一步 |
|---|---|---|---|---|---|---|---|

最后汇总：适用格式及其来源、双向匹配问题、书目字段问题、实际完成的链接检查、阅读范围、论点支持状态、未核实项目和用户需人工完成事项。不得虚构修复字段，不得无依据评分，也不得把未执行的核查描述成通过。

## English

This file is the **single primary maintenance source** for detailed APA 7 type-specific fields and checks. The independently copyable short prompt is [`prompts/04-APA7引用检查.md`](../../../prompts/04-APA7引用检查.md).

### Scope and authoritative basis

Check the current Coursework, Rubric, and instructor instructions first; explicit requirements for the assignment take precedence. If assignment-level instructions are absent, consult the [current official TAR UMT Library referencing guide](https://library.tarc.edu.my/training-support/apa-referencing-style) and any applicable programme/course exception. The TAR UMT Library guide identifies APA 7 as the main referencing style while recognizing that some programmes may use another style. Use this checklist when APA 7 is confirmed to apply. If the applicable style is unconfirmed, mark it to be confirmed and do not declare a violation based only on general APA 7 details.

This checklist was checked against APA Style official materials on 2026-10-25: [Reference Examples](https://apastyle.apa.org/style-grammar-guidelines/references/examples), [Elements of Reference List Entries](https://apastyle.apa.org/style-grammar-guidelines/references/elements-list-entry), [DOIs and URLs](https://apastyle.apa.org/style-grammar-guidelines/references/dois-urls), [Missing Reference Information](https://apastyle.apa.org/style-grammar-guidelines/references/missing-information), the official examples for [journal articles](https://apastyle.apa.org/style-grammar-guidelines/references/examples/journal-article-references), [books/ebooks](https://apastyle.apa.org/style-grammar-guidelines/references/examples/book-references), [edited-book chapters](https://apastyle.apa.org/style-grammar-guidelines/references/examples/edited-book-chapter-references), [government reports](https://apastyle.apa.org/style-grammar-guidelines/references/examples/report-government-agency-references), [webpages](https://apastyle.apa.org/style-grammar-guidelines/references/examples/webpage-website-references), and [Basic Principles of Citation](https://apastyle.apa.org/style-grammar-guidelines/citations/basic-principles).

APA Style states that its guidelines describe the seventh-edition manuals and that updates are noted on relevant pages. Recheck current pages and the instructor's current requirements when applying this checklist. Mark uncovered or ambiguous cases “to be confirmed”; do not fill gaps from memory.

### 1. Required inputs

Request the current draft and References, instructor requirements, the institution's current official guide when needed, permitted online-query scope, and original source text when claim support is to be assessed. If material is missing, state the limited checks possible. Do not describe formatting review as content verification.

### 2. Separate status fields

For every source, report separately:

| Object | Meaning | Suggested values |
|---|---|---|
| Source existence | Whether a matching work was found in a checkable publisher, journal, institution, or other reliable record | Record found (not yet verified) / existence verified / not found in this search (does not prove nonexistence) / query failed / records conflict / to be confirmed |
| Bibliographic accuracy | Whether applicable fields match authoritative records | Verified / partly verified / missing / to be confirmed / not applicable |
| DOI/URL | Whether it exists, resolves, and points to the cited work | Exists and accessible / exists but inaccessible / not found / to be confirmed / not applicable |
| Reading scope | Material actually examined | Full text / abstract / metadata / specified portion / unread |
| Claim support | What the examined source material actually supports and to what extent | Directly supported / partly supported / indirectly supported / not supported / to be confirmed |

Link accessibility does not establish bibliographic accuracy, source quality, or claim support. Do not claim full-text reading after examining only metadata, an abstract, or part of a source.

### 2A. Free public sources and query limits

- Prefer the free public [Crossref REST API](https://www.crossref.org/documentation/retrieve-metadata/rest-api/access-and-authentication/) for DOI and deposited metadata checks. No registration is required. Its current official limits are 5 requests/second and 1 concurrent request on the Public pool, and 10 requests/second and 3 concurrent requests on the Polite pool. The Public pool is sufficient by default; do not send a personal email just to obtain a higher rate. Returned records reflect deposited metadata and do not establish full-text content or claim truth.
- OpenAlex can be used for free metadata queries: its current official documentation lists a $0.10/day no-key budget and $1/day for a free key (account and email confirmation required); basic rate limits are 10 requests/second without a key and 30 with a key. Use only the no-key free budget without creating a new account/key; stop when the budget is exhausted, wait for the free reset or use a free public page manually, and never enable pay-as-you-go. OpenAlex PDF/XML downloads are currently charged per file and must not be used. Check the current [authentication/rate limits](https://help.openalex.org/api/authentication/) and [pricing](https://help.openalex.org/access/pricing/) on the day of use.
- Most Semantic Scholar API endpoints are available anonymously. Its official documentation describes a shared unauthenticated pool of 1,000 requests/second that may be throttled further, and a 1 request/second introductory rate for API keys; this workflow does not require or request a key. Use public free endpoints only and stop immediately if throttled. ([official API information](https://www.semanticscholar.org/product/api))
- Stop the current API query at HTTP 429, quota/limit notice, timeout, service failure, login wall, or conflicting records. Record “query failed,” “limited,” or “records conflict”; a free publisher/institution page may be checked manually, otherwise mark the item to be confirmed. Never switch automatically to a paid service, buy credits, or bypass access controls.
- Send only the minimum identifiers needed (e.g. DOI, title, or author query) to public services. Do not send a full assignment, private course material, unpublished text, or authentication secrets.
- Available records, free quotas, and API terms can change. Follow each provider's current official documentation and responses. A missing result from one service does not prove nonexistence; search results, abstracts, DOIs, and metadata do not replace claim checks against original text.

### 3. Select a source type and assess its fields

For each applicable field, record its requirement classification (required / conditional / not applicable), observed value, verification basis, result (verified / missing / to be confirmed / not applicable), and reason. A field's classification depends on the source type and authoritative example; if uncertain, mark it to be confirmed.

| Type | Fields to assess from the official example | Notes |
|---|---|---|
| Journal article | Author; date; article title; journal title; volume; issue when assigned; page range or article number; DOI when the work has one; URL for applicable online works without a DOI | Use the journal example. Do not invent missing volume, issue, pages, or article number. Follow the official treatment for database information and genuinely absent elements. |
| Book/ebook | Author/editor; date; title; edition/volume when applicable; publisher; DOI or stable URL when applicable | The official examples distinguish authored and edited books and special republication cases. Do not infer platform/device formatting. |
| Chapter in an edited book | Chapter author; date; chapter title; editor(s) and role; book title; page range when paginated; edition when applicable; publisher; chapter DOI or stable URL when applicable | Distinguish an edited-book chapter from a chapter of an authored book; consult the official example for the latter. |
| Webpage | Individual/group author; specific date when available; page title; website name as applicable; URL; retrieval date only when official conditions apply | First determine whether the work is actually a report, periodical article, book, or another category hosted on a website. |
| Institutional/government report | Individual/group author; date; report title; report number if present; publisher/source; DOI or URL as applicable | Identify the work as a report rather than a webpage merely hosted on a site. Follow the official example for agency hierarchy and author/publisher roles. |

For other types (e.g., news, datasets, theses, social media, or preprints), select the relevant APA Style Reference Examples category rather than forcing it into these five types. If no applicable authoritative example can be checked, mark the item to be confirmed.

### 4. DOI and URL checks

Check whether a DOI or applicable URL exists without guessing one. Verify that it points to the cited work and compare bibliographic details with a publisher or other authoritative record. Apply APA Style's inclusion rules for the work type and retrieval context. Report a broken, inaccessible, login-only, or mismatched link distinctly; never silently substitute a guessed address.

### 5. Two-way citation/reference matching

1. **In-text citation to References:** identify citations in text, tables, figures, footnotes, and appendices; locate the corresponding entry and compare author spelling/date. List unmatched citations with their location.
2. **References to in-text citation:** check each entry for a corresponding citation; list unmatched entries.
3. Separately flag duplicates, author/date discrepancies, possible same-author/same-date ambiguity, and unresolved matches.
4. Apply APA exceptions only after confirming they fit the case (e.g., certain non-recoverable personal communications or reference-list entries in a meta-analysis). Do not generalize exceptions to ordinary sources.

### 6. Claim support and reading scope

Map each cited source to a specific claim. When original text is available, record page, paragraph, table, or data location and explain support scope and limitations. Metadata-only review cannot establish claim support. Abstract-only review must be labeled and restricted to what the abstract actually supports.

### 7. Output

Report each source's type and applicable guide, field classifications/values/bases/statuses, source and DOI/URL checks, reading scope, claim support, two-way matching, issues, and next action. Summarize unresolved items and manual checks. Never fabricate fields or claim a check passed when it was not performed.
