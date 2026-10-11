# 共享平台操作手册

适用于本次招募赛的项目内题目对话。2026-10-10 已核本机 Playground 0.1.40、Bohr 2.7.7，并重新核对下列命令帮助。成员直接复用现有环境和账号；无需重新注册、claim、安装或从旧教程重搭环境。换机器或发现版本差异才补核，不把既有检查当作远端环境保证。

## 手册与来源入口

| 需要了解什么 | 直接入口及边界 |
| --- | --- |
| 本届赛事与岗位 | [官方比赛专区](https://play.bohrium.com/competition/zhuiguang)、[赛事完整版说明](https://dplightchasers-recruit.app.workbuddy.host/)、[本项目核验规则](RULES.md)；各题正式合同和最新通知优先 |
| 完整新手流程 | [已归档原文及完整性说明](../../references/asc-beginner-guide/README.md)、[原文全文](../../references/asc-beginner-guide/original.txt)、[项目提醒](../../references/asc-beginner-guide/agent-notes.md)；副本含图片/同步块缺口，版本和赛季文字是历史内容 |
| 飞书原始教程 | [Agentic Science Challenge 新手教程](https://dptechnology.feishu.cn/docx/MJwXd4ek3oFGONxSHuwcl83LnUS)，需要缺失图片/同步块时回源，不重新让用户解释 |
| 账号接入 | [官方 Agent 接入文档](https://play.bohrium.com/api/docs/agent-integration)，已有本人绑定有效，不重复 claim |
| 原生轨迹 | [官方轨迹阅读说明](https://play.bohrium.com/api/docs/reading-a-trace)、[ARM 协议参考](https://play.bohrium.com/api/docs/dev/ARM_PROTOCOL_REFERENCE.md) |
| API 排错 | [官方 Agent API 文档](https://play.bohrium.com/api/docs/dev/AGENT_API.md)，仅按具体缺口查，不遍历无关用户记录 |
| 本题材料 | 原 Issue 的稳定 challenge ID、材料逻辑键、固定 manifest 和合同校验值；本机材料索引负责解析实际位置 |

教程副本已在仓库，无需重新上传或让维护者搬运。官方动态文档若当前环境打不开，沿用已核结论并明确具体缺口；不要声称已读不可达页面。官方安装示例不是本次安装授权。

## 1. 进入已准备的本机环境

本机工作根 AGENTS.md → 受控共同目录 README → platform-local.md，给出已有凭据文件引用与本机材料位置。只引用现有配置，不输出凭据内容、不打印环境全集、不把环境文件装进提交包。外部聊天没有本机文件/终端能力时，先在 Issue 标明权限缺口，由总监安排有共同结果路径的执行方式；一个公开链接不等于拥有本机材料。

必要的只读检查（沿用已有健康证据；异常、换环境或恢复前再查）：

```sh
playground --version
playground auth status
playground doctor
bohr version
```

已有归属已核。auth失败先查凭据引用和环境，不能默认重新注册或覆盖配置。Playground认证与Bohrium数据访问认证分别定位；需要本人登录时整理一次明确请求。Wenyon有更新提示但固定资源元数据查询已成功，提示本身不构成升级理由。

## 2. 本题合同和数据

先从 Issue 的材料键读取已捕获的本题官方合同及公开资源清单，避免重新全平台搜题。稳定字符串 ID 优先，不使用易变的列表序号。只有合同/资源变化或材料缺失时再获取。

```sh
playground task list --limit 20 --json
# 必要时只获取题目元数据/说明，不自动拉全部数据集：
playground task download --challenge-id CHALLENGE_ID --out task --skip-datasets
# 固定资源版本的清单元数据：
bohr wenyon dataset files DATASET_ID --version VERSION --output json
# 按官方 manifest 白名单取本题允许的公开文件：
playground data pull --dataset DATASET_ID --version VERSION --paths PATH1,PATH2 --out inputs
```

以上是替换占位符后的操作形状，成员先核本题输入白名单，不直接执行占位命令。下载参数以当前帮助为准。核 manifest版本、文件hash及本地hash；不得为探索目录而展开 hidden tests/checker/solution。题目下载不会自动下载模型权重；数据清单可读不证明完整文件或模型已到位。

## 3. 实际解题与记录

每题独立工作目录，区分 inputs、scripts、outputs、evidence；outputs仅含题面指定成果，其他脚本/日志放外部。实际执行、正确性检查、失败和修正均留证据。输入/输出合同、允许联网和依赖按本题执行；不能照搬其他题限制或旧教程例子。主实现对话从自己的原生会话记录定位完整日志，不使用总监整段聊天或别题日志替代。

## 4. 本地打包与正式提交

先做本地预检，核准确候选、outputs层级、完整原生记录及包内无无关敏感材料：

```sh
playground trace validate --trace OWN_NATIVE_TRACE
playground submit --challenge-id CHALLENGE_ID --outputs outputs --trace OWN_NATIVE_TRACE --raw-messages OWN_NATIVE_TRACE --model ACTUAL_MODEL --harness ACTUAL_HARNESS --no-auto-skills --bundle-out candidate.zip --dry-run
```

0.1.40创建接口以文件方式传raw_messages；应同时显式传trace和raw-messages。该路径已由本届正式题目的准确包、原生内容核对及有效评分证实，来源见 [#10](https://github.com/Sisu-z/agentic-science-lab/issues/10)、[#11](https://github.com/Sisu-z/agentic-science-lab/issues/11)。这不替代新题的包审计。核包中的原生文件、raw_messages、结构化事件和manifest及产物关联；不截断、拼造或补写过程。身份个人材料题的暂停决定仍只读其原 Issue，不能从其他题提交授权推导个人材料授权。

正式提交必须经本题验收且在已有明确授权范围，由 Issue 指定的唯一操作者执行；仅此时移除 --dry-run。保留receipt、attempt ID、候选校验值与接收时间。正式提交、包上传和平台Skill公开分享均不是只读检查。

```sh
# 完整attempt、scoringState与任务终态：
playground status --attempt-id ATTEMPT_ID
# 包与scorecard摘要补充；缺少完整状态字段不代表未评分：
playground status --attempt-id ATTEMPT_ID --bundle
# 仅在已创建attempt、Worker上传失败且核清可重试时：
playground submit --challenge-id CHALLENGE_ID --attempt-id ATTEMPT_ID --bundle candidate.zip --trace OWN_NATIVE_TRACE
```

按实际帮助核重试参数，不盲目创建重复attempt。queued/running/scoring不是终态；本地通过、已接收、任务分、轨迹审核和最终分开报告。原始回执留受控目录，公开Issue仅回填可公开摘要。

维护者已授权的正常闭环是：独立验证有效候选 → 提交并核接收 → 查看实际反馈 → 有实质修复和验证后再提交。不要重复征求已有提交授权；不要因排队占位零分、独立generated_skill接口401或同版等待而另建attempt。维护者转述平台限制恶意高频提交，本项目据此禁止同版刷交、绕过限流；不编造统一冷却时间，遵守实际429/冷却提示。最高已接受版本与最新工程版本分别保留。

## 5. 常见卡点直接这样处理

| 现象 | 第一项有效检查 |
| --- | --- |
| 认证失败 | 凭据引用/账号环境，区分Playground与Bohrium认证；不重复注册 |
| 数据404/权限问题 | 稳定题号、固定dataset版本、官方manifest路径；保存错误与已成功步骤 |
| 缺依赖/模型 | 区分准备脚本和真正权重，核已有运行环境；新增安装/付费按授权处理 |
| 包/输出失败 | 本题确切文件名、父目录层级、多余文件/符号链接、格式、字节限制 |
| 本地对但低分 | 单位、顺序、边界、缺失分项、真实计算及独立验证；不读隐藏评测 |
| 轨迹解析/包审计失败 | 查看原生格式、包manifest和审计脚本兼容性；保留原件，不补造轨迹 |
| 上传报错/长期评分中 | 保存已有attempt和响应，查询原attempt，核错误层次再重试 |
| status摘要缺字段/独立Skill接口401 | 不带--bundle读取完整attempt；任务终态与generated_skill结果分开核，不能由后者推断提交失败 |
| 题面自动计分但元数据仅人工评审 | 本届已有同样元数据却自动出有效终态的反例，不能仅凭标签认定不会自动出分；保存差异与回执，按实际状态报告，不为等分重复上传。来源见 [#4](https://github.com/Sisu-z/agentic-science-lab/issues/4#issuecomment-6105929911) |

成员把复现步骤、环境/版本、错误、已排除项及下一检查回填原 Issue；跨题有用的经验链接到 [EXPERIENCES.md](EXPERIENCES.md)。总监自行读取，不让维护者重新搭对话或转述技术报告。
