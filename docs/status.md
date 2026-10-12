# 当前进度

更新：2026-10-10

## 2026-10-10 招募赛组织

当前比赛组织见 [总监指挥入口](contests/lightseeker-20261010/README.md)，实时任务以 [GitHub Issues](https://github.com/Sisu-z/agentic-science-lab/issues) 为准。已开展远端手册、前次流程及平台预检；组织与文档验收不代表正式赛题通过。历史实验分支和待评分 PR 未在本次合并，不能将下方旧状态当作今日状态。

## 2026-09-23 历史初始化快照

- 公开项目仓库已初始化；已完成首次独立解题实验，官方提交状态见下文。
- 用户提供的新手教程文本已原样归档，并接入 Agent 必读入口；图片和同步块未包含在该文本内，参见教程目录的完整性说明。
- Playground CLI 0.1.39、Bohr CLI 2.7.7 已在维护者本机验证可用；数据工具健康检查通过。
- 参赛 Agent 与维护者账号的绑定已确认生效。凭据存储在仓库之外。
- 本次查询可见题目 6,887 道；教程指定 S4 Round 6，但列表只检出 S4 Round 1、2、3 的标记。正式计分范围仍需确认。

## 候选题目

| 题目 | 用途 | 已知边界 |
| --- | --- | --- |
| Terminal-Bench Science: symbolic-regression | 优先练习训练、验证与提交全过程 | 只能修改指定预测文件，禁止安装额外包；已完成弱基线实验 |
| Focused imaging and resolution characterisation from unfocused plane-wave recordings | 成像重建、数值计算与指标验证 | S4 Round 3；须达到实际分辨率要求；尚未运行 |
| FIB Sim-to-Real：少样本参考数据分割挑战 | 视觉与模拟到真实域迁移实践 | 题面仍标注公开预览，自动评分适配未完成；尚未运行 |

## 正在进行

已按维护者指示开始 [symbolic-regression 首次独立尝试](../tasks/terminal-bench-science-v0-1-0-symbolic-regression-3bceeb08/README.md)。仅由 Sisu Codex 执行，不使用子 Agent。

Bohrium 授权与公开数据下载已完成。首次独立尝试比较 25 个模型，最终留出 macro-F1 为 0.566667，尚不足以证明解题成功。原 CLI 创建提交时发送空轨迹，被服务器拒绝；本地副本改为发送真实轨迹后成功。attempt 45932、worker job 24198 已接收排队。暂无官方得分；最新回执为 pending_review，评审服务暂时不可用，恢复后重评。显示的 0 分不是最终成绩。

已核对正式赛事页：计分题每周五发布，24 小时提交窗口；其他题目用于不限次练习，不计入赛季排名。本次按练习任务执行。
