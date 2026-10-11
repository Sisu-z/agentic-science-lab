# 共享经验索引

这里存可复用经验的索引，不存第二套任务状态。成员开工先查本页，再读取来源 Issue/文档及证据边界。以下只记录有实际证据的方法与限制，不将平台操作成功推广为新题正确性或隐藏性能保证。

| 主题 | 已知结论与适用边界 | 来源 |
| --- | --- | --- |
| 必做门槛与简单事务 | 启动时在原任务登记资格/身份/材料门槛及接收余量；简单且已授权的上传、填表、核回执由总监直接做，不因拆聊天拖到截止前。必要本人确认仍不可代替 | [协作复盘](RETROSPECTIVE.md)、[#9](https://github.com/Sisu-z/agentic-science-lab/issues/9) |
| 可见聊天与项目归属 | 聊天、工作目录、项目标签分别核验；默认分类的本地聊天不等于临时记录。共同任务源能共享信息，不会自动完成界面归类或历史合并 | [协作复盘](RETROSPECTIVE.md)、[成员入口](START_HERE.md) |
| 赛后停止与资源整理 | 当前任务头部与终态同步；磁盘、内存、运行任务和缓存分别测量。保留证据与回执，有余量时无需删除项目，归档不保证释放固定资源 | [协作复盘](RETROSPECTIVE.md)、[#5](https://github.com/Sisu-z/agentic-science-lab/issues/5) |
| 账号归属与个人材料 | 现有 Agent 归属已确认；独立身份材料题与 claim 分开核，查询缺失不能推出账号未绑定 | [#3](https://github.com/Sisu-z/agentic-science-lab/issues/3)、[规则](RULES.md) |
| Codex 原生记录打包 | Playground 0.1.40 显式给 trace 与 raw-messages、真实模型/harness并核包，已由本届完整上传与正式终态验证；不同对话原生记录仍不会自动合并，每道新题单独审计 | [#10](https://github.com/Sisu-z/agentic-science-lab/issues/10)、[#11](https://github.com/Sisu-z/agentic-science-lab/issues/11)、[交付规程](RUNBOOK.md) |
| 有效文件与重放 | 必须按本题准确输出合同，从干净目录重放；开发目录存在输出、格式合法或旧题验证通过均不能代替本题正确性 | [交付规程](RUNBOOK.md)、[#5](https://github.com/Sisu-z/agentic-science-lab/issues/5) |
| 完整评分状态 | status不带--bundle读取完整attempt与scoringState，带该选项主要补包摘要；generated_skill独立401不等于任务失败。已由有效终态对照核查 | [#10](https://github.com/Sisu-z/agentic-science-lab/issues/10)、[#13](https://github.com/Sisu-z/agentic-science-lab/issues/13)、[平台手册](PLATFORM.md) |
| 独立合同验证 | 针对独立错误分支、边界及输入变体验证，再做准确包内重放；通过样本与自检不足以代替完整合同。原题已获有效终态，具体实现不公开复用 | [#11](https://github.com/Sisu-z/agentic-science-lab/issues/11) |
| 输出与轨迹因果链 | 原生记录应实际覆盖生成命令、输入输出身份及验证，不仅保留事后文件名和进度说明；原始失败与调用结果配对保留，不补造历史 | [#13](https://github.com/Sisu-z/agentic-science-lab/issues/13) |
| 正常提交与未知结果 | 先核已创建attempt、包哈希和接收再决定重试；排队占位零分不重交，按实质反馈修复，遵守实际限流。已用真实接收回执核查，后续终态只读原Issue | [#15](https://github.com/Sisu-z/agentic-science-lab/issues/15)、[#16](https://github.com/Sisu-z/agentic-science-lab/issues/16)、[#17](https://github.com/Sisu-z/agentic-science-lab/issues/17) |
| 同分停滞与最佳版本 | 连续同分时先从原始模板/合同独立核实高权重要求；没有新差异证据不继续微调刷交。最新工程候选不自动取代最高正式版本 | [#14](https://github.com/Sisu-z/agentic-science-lab/issues/14) |
| 优化累计预算 | 合同未明确给出重置许可时，本轮保守采用一次累计账本，计入实际尝试、失败和后续搜索；这是本轮执行策略，不是已确认适用于所有题的统一官方规则。各题依准确合同记录验证与搜索边界 | [#16](https://github.com/Sisu-z/agentic-science-lab/issues/16) |
| 评分元数据与实际终态 | `human_review_only` 也出现在本届已自动评分并得到有效终态的题目中，不能凭该字段断言新题不会自动出分；仍按实际 attempt 状态、回执和 final 标志核查 | [#4](https://github.com/Sisu-z/agentic-science-lab/issues/4#issuecomment-6105929911)、[#10](https://github.com/Sisu-z/agentic-science-lab/issues/10) |
| 评测失败后的恢复与排队区分 | 两道 Skill 记录实际变为 failed/无终分，当前公开合同及资源未变。依据官方 failed 提示，总监指定各一次恢复送评，实际接收只读原 Issue；保留原实验与负结果，不虚构新科学改进或反复新建，重复失败则登记阻塞 | [#5](https://github.com/Sisu-z/agentic-science-lab/issues/5#issuecomment-6107167667)、[#28](https://github.com/Sisu-z/agentic-science-lab/issues/28)、[#29](https://github.com/Sisu-z/agentic-science-lab/issues/29) |
| 独立依赖环境与实际分支验证 | 经维护者明确同意后，宏环题官方推荐 RDKit 在独立比赛环境安装并实际导入；专利题复用该环境核验此前未真实运行的库分支，发现实现与测试输入的不同问题。安装成功、分支检查、化学有效性及隐藏评分仍分别验收；其他安装不自动获准 | [#32](https://github.com/Sisu-z/agentic-science-lab/issues/32)、[#30 实际验证](https://github.com/Sisu-z/agentic-science-lab/issues/30#issuecomment-6107231199) |
| 独立可见对照与原生记录 | 先冻结版本、输入、标准和配对预算，独立对话不共享本题中间答案；结束后核各自完整原生终态、稳定源文件和哈希。自动背景与无法锁定的服务字段如实披露，不声称彻底关闭记忆 | [#28](https://github.com/Sisu-z/agentic-science-lab/issues/28)、[#29](https://github.com/Sisu-z/agentic-science-lab/issues/29) |
| 增益与能力分别验收 | 有 Skill 与基线可能同样正确，基线也可能更快；质量、耗时、复用和异常处理按事先标准分别判断。所有重试及作者投入计入，不把自评或结构通过当正式分数 | [#28](https://github.com/Sisu-z/agentic-science-lab/issues/28)、[#29](https://github.com/Sisu-z/agentic-science-lab/issues/29) |
| 原生工具事件计数 | 当前 Codex 原生导出使用 `custom_tool_call` 时，仅数旧 `function_call` 会漏记；先核真实事件类型和时间边界，不把旧计数器的零解释为没有工具执行 | [#28](https://github.com/Sisu-z/agentic-science-lab/issues/28)、[#29](https://github.com/Sisu-z/agentic-science-lab/issues/29) |
| 科学版本终态采集与真实复现 | 作者完成版本后结束，总监从完整稳定的连续原生记录外部封存，再恢复原作者提交；核调用结果、派发封装、文件因果链与实际复算入口。运行中自采可能漏掉本次工具回执，补齐包装字段也不能证明评测失败根因；完整保留旧事实及独立性边界 | [历史独立审计](https://github.com/Sisu-z/agentic-science-lab/issues/17#issuecomment-6107496898)、[平台操作](PLATFORM.md#已完成版本的原生记录与复现) |
| 引用检查器的授权范围 | 路径检查须覆盖任务明确授权的共享来源；检查器单一根目录造成的误报不能算作输出错误。保留原误报并用准确允许清单复核；路径、原文和哈希匹配仍不等于语义支持 | [#29](https://github.com/Sisu-z/agentic-science-lab/issues/29) |

## 成员怎样贡献

先在原题 Issue 写：发现/方法、适用环境与版本、实际验证与证据、失败条件/未覆盖项、可能受益的关联题。允许公开且有跨题价值时，通过 PR 在本表加一行，链接原记录；没有验证的想法标明待验证，不进入“可靠方法”。总监审查整合，不要求每题另写长篇复盘。

涉及正式题面、源码、数据、答案、个人材料或原始轨迹的经验正文保留受控位置；公开索引只留脱敏方法和材料逻辑键。不可因“团队共享”而把私有比赛材料公开发布。
