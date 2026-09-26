# awp-config-github-community — Agent instructions

## 项目
- 这是 aiworkflowpro 组织的默认 GitHub community health 仓。
- 远端仓名为 `.github`；本地四段式目录名是 `awp-config-github-community`。
- GitHub 会向未定义本仓版本的组织仓库提供这些默认文件。

## 目录
- `README.md`：说明本仓用途和适用范围。
- `CODE_OF_CONDUCT.md`：行为准则。
- `CONTRIBUTING.md`：贡献指南。
- `SECURITY.md`：漏洞报告入口。
- `SUPPORT.md`：支持渠道。
- `.github/ISSUE_TEMPLATE/`：问题模板。
- `.github/PULL_REQUEST_TEMPLATE.md`：PR 清单。
- `.github/workflows/`：仓内 GitHub Actions。
- `assets/`：README 等文档引用的资源。

## 可用命令
- 本仓没有包管理器清单或本地 build/test 命令。
- 校验 Markdown 引用时使用实际文件路径逐项核对。
- 检查改动使用 `git diff --check`。
- 检查模板变更使用 `git diff -- .github/`。

## 实现边界
- 默认文件面向整个 aiworkflowpro 组织。
- 改行为准则前核对 README 和 CODE_OF_CONDUCT。
- 改安全入口前核对 SECURITY 中的现有联系渠道。
- 改支持入口前核对 SUPPORT 中的现有说明。
- 改 issue 模板时维持 YAML 格式和字段用途。
- 改 PR 模板时维持现有贡献指南链接。
- 组织级默认设置不能假定覆盖仓库自己的同名文件。
- 不要把仓库专有规则写进组织默认文件。
- 不要改远端名 `.github` 的约定。

## 验证
- 逐项检查修改后的 Markdown 链接。
- 涉及 YAML 时检查缩进与字段。
- 涉及模板时阅读生成后的提交/问题表单。
- 确认变更确实适用于整个组织。

## 工作方式
- 先读本仓 `README.md`（若存在），以当前文件和脚本为准。
- 只改本次任务涉及的文件，不顺手重排其他内容。
- 运行与改动相称的检查，失败时修实现而不改测试结论。
- 提交前检查 `git diff --check` 与 `git status --short`。
- 只暂存本次改动文件，提交信息说明实际改动。
- 不在提交信息里写 AI 工具署名。
- 不把密钥、令牌、真实 `.env` 或运行数据提交进仓。
- 涉及远端、部署或对外可见内容时，先核对现有配置与项目约束。

## 提交前核对
- 文件路径仍与 README 中的入口相符。
- 新增引用指向仓内真实文件或明确的外部地址。
- 本仓已有的无关改动保持原样。
- 验证命令、运行环境和未执行的步骤在回报中写清。

## 查找入口
- 需要更多项目事实时，从 README 中的相应章节继续查。
- 需要执行具体动作时，以本仓当前文件和脚本定义为准。
- 外部服务状态必须实时核对，不从仓内文案推断。
