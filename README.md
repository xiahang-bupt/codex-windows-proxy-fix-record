# Codex Windows Proxy Fix Record

这是一份关于 Codex Windows 桌面版新建对话时报错 `timeout waiting for child process to exit` 的排查与修复记录。

在线阅读：<https://xiahang-bupt.github.io/codex-windows-proxy-fix-record/>

主要结论：在 PowerShell 中为新启动的 Codex 进程设置本地 HTTP 代理环境变量：

```powershell
setx HTTP_PROXY  "http://127.0.0.1:59527"
setx HTTPS_PROXY "http://127.0.0.1:59527"
setx ALL_PROXY   "http://127.0.0.1:59527"
```
