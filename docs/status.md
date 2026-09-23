# 当前进度

更新：2026-09-23

- 公开项目仓库已初始化；尚未开始解题或产生正式提交。
- 用户提供的新手教程文本已原样归档，并接入 Agent 必读入口；图片和同步块未包含在该文本内，参见教程目录的完整性说明。
- Playground CLI 0.1.39、Bohr CLI 2.7.7 已在维护者本机验证可用；数据工具健康检查通过。
- 参赛 Agent 与维护者账号的绑定已确认生效。凭据存储在仓库之外。
- 本次查询可见题目 6,887 道；教程指定 S4 Round 6，但列表只检出 S4 Round 1、2、3 的标记。正式计分范围仍需确认。

## 候选题目

| 题目 | 用途 | 已知边界 |
| --- | --- | --- |
| Terminal-Bench Science: symbolic-regression | 优先练习训练、验证与提交全过程 | 只能修改指定预测文件，禁止安装额外包；尚未运行 |
| Focused imaging and resolution characterisation from unfocused plane-wave recordings | 成像重建、数值计算与指标验证 | S4 Round 3；须达到实际分辨率要求；尚未运行 |
| FIB Sim-to-Real：少样本参考数据分割挑战 | 视觉与模拟到真实域迁移实践 | 题面仍标注公开预览，自动评分适配未完成；尚未运行 |

## 正在进行

已按维护者指示开始 [symbolic-regression 首次独立尝试](../tasks/terminal-bench-science-v0-1-0-symbolic-regression-3bceeb08/README.md)。仅由 Sisu Codex 执行，不使用子 Agent。

当前阻塞：Playground 认证有效，但 Bohrium 尚未登录，Wenyon 训练数据下载返回 401。未训练、未提交、无得分。维护者完成官方登录后继续。

已核对正式赛事页：计分题每周五发布，24 小时提交窗口；其他题目用于不限次练习，不计入赛季排名。本次按练习任务执行。
