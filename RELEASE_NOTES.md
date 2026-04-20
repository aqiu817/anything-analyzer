# Anything Analyzer v3.3.7

## Bug 修复

- **修复追问时 FOREIGN KEY 约束错误** — AI Report 追问期间，若用户切换或删除 Session，LLM 响应后持久化消息会因 report 被级联删除而报错。现在通过 `activeChatReports` 机制保护正在追问的 report 不被删除，确保追问消息正常持久化
- **修复第三方 LLM 中转站兼容性** — 针对非标准 API 供应商（中转/代理站）返回 HTML 错误页、非标准 JSON 格式等情况，增加安全 JSON 解析和响应结构验证，避免 `Unexpected token '<'` 和 `Cannot read properties of undefined` 等崩溃，改为显示清晰的错误信息
- **修复 LLM 错误信息双重包装** — HTTP 错误（如 404）不再被网络诊断函数二次包装，错误提示更简洁准确

## 下载

| 平台 | 文件 |
|------|------|
| Windows | `Anything-Analyzer-Setup-3.3.7.exe` |
| macOS (Apple Silicon) | `Anything-Analyzer-3.3.7-arm64.dmg` |
| macOS (Intel) | `Anything-Analyzer-3.3.7-x64.dmg` |
| Linux | `Anything-Analyzer-3.3.7.AppImage` |
