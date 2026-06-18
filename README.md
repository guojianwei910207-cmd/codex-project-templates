# Codex Project Templates

用于保存和分发 Codex 本地开发项目的通用接手规则与模板。仓库设为 Private，不应写入任何项目密钥、生产数据或个人敏感信息。

## 文件说明

* `codex-local-development-rules.md`：可复制到 Codex 个性化设置的全局规则。
* `codex-project-handoff-rules.md`：用于创建项目根目录 `AGENTS.md`。
* `codex-handoff-template.md`：用于创建项目根目录 `HANDOFF.md`。

## 新电脑配置

1. 登录有权访问本仓库的 GitHub 账号。
2. 克隆本仓库到任意长期保留的本地目录：

   ```powershell
   git clone https://github.com/guojianwei910207-cmd/codex-project-templates.git
   ```

3. 打开 `codex-local-development-rules.md`，仅复制“个性化设置正文”到 Codex 个性化设置。
4. 拉取包含 `AGENTS.md` 和 `HANDOFF.md` 的具体项目仓库，让 Agent 按项目文档接手。

## 新项目建档

1. 将 `codex-project-handoff-rules.md` 的模板正文复制为项目根目录 `AGENTS.md`。
2. 将 `codex-handoff-template.md` 的模板正文复制为项目根目录 `HANDOFF.md`。
3. 根据项目实际情况填写，删除无用占位内容。
4. 检查 `.gitignore` 和敏感信息。
5. 经用户确认后，将接手文档提交并推送到该项目的远程仓库。

## 文档职责

* 个性化设置只保存所有项目通用的短规则。
* `AGENTS.md` 只保存项目长期有效的规则、关键目录和固定命令。
* `HANDOFF.md` 只保存当前 baseline、工作状态、验证结果、下一步和风险。
* 版本历史、重大决策和复盘分别写入 `VERSION.md`、`decision-log.md` 和 `LESSONS.md`，确有需要时再创建。

## 更新模板

更新前先执行：

```powershell
git status --short --branch
git pull --ff-only
```

修改后检查 diff、UTF-8 编码和敏感信息。未经用户确认，不执行 commit 或 push。
