# 平台与仓库分工

2026-09-23 根据已安装 Playground CLI 0.1.39 的帮助和实现核对。

- Playground：题目获取、Agent 绑定、提交、评分与平台 Skill 分享。
- GitHub：代码版本、复盘、Skill 与公共模块维护、分支协作和审查。
- 本地或计算环境：实际运行、数据、模型与原始证据。

CLI 声明总分超过 90 后异步生成高分 Skill，支持：

```sh
playground skill status --attempt-id <id>
playground skill download --attempt-id <id> --out ./skills
```

下载包含 SHA-256 校验。`playground skill share` 会公开发布到平台 Tools 页面，使用前确认发布范围。当前只核验功能说明，尚未通过实际高分提交验证整个生成流程。

Agent 凭据通过 `PLAYGROUND_CREDENTIALS_PATH` 引用仓库外的文件。不要将真实凭据放入示例、提交或公开日志。

新手教程：https://dptechnology.feishu.cn/docx/MJwXd4ek3oFGONxSHuwcl83LnUS
平台：https://play.bohrium.com/
