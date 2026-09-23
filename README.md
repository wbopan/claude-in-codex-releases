# Claude in Codex

在正常启动的 Codex App 中使用本机的 Claude Code。Claude in Codex 是一个 macOS 菜单栏 App：打开后，Codex App 的模型选择器会增加 Claude 模型，Claude Code Session 和 GPT 任务在同一个 App 里并行运行。

Use your local Claude Code inside the Codex desktop app. This repository hosts the signed and notarized builds.

## 下载与安装

1. 从 [最新 Release](https://github.com/wbopan/claude-in-codex-releases/releases/latest) 下载 `Claude-in-Codex-<版本>-arm64.zip`。
2. 解压，把 **Claude in Codex.app** 拖到「应用程序」文件夹。
3. 先打开 Codex App，再打开 Claude in Codex。菜单栏的云朵睁开眼睛，表示已接入。

App 由 Developer ID 签名并经过 Apple 公证，可以直接打开。

**要求**：Apple 芯片的 Mac，macOS 14 或更新版本，已安装并登录的 [Claude Code](https://docs.anthropic.com/en/docs/claude-code)，以及官方 Codex App（`/Applications/ChatGPT.app`）。

## 更新

App 默认每 6 小时检查一次新版本，也可以在主窗口「设置 › 更新」中手动检查或关闭自动检查。安装更新前，App 会先等正在执行的 Claude Code Session 完成，再重启到新版本。更新包带有 EdDSA 签名，App 只接受签名匹配的更新。

Codex App 更新后，如果接入失败，通常是新版 Codex App 改了内部结构。App 会停止接入并显示原因，修复版本会通过自动更新送达。每个版本已验证的 Codex App 版本写在 Release 说明里。

## 卸载

1. 从菜单栏选择「退出 Claude in Codex」，等待任务完成。
2. 删除「应用程序」中的 Claude in Codex.app。
3. 如需清除数据，删除 `~/Library/Application Support/Claude in Codex` 和 `~/Library/Logs/Claude in Codex`。

## 隐私

接入只在本机进行，只改变正在运行的 Codex App 与本机 Claude Code 之间的连接。Claude 的对话和认证由 Claude Code 自己处理。App 只额外访问 GitHub，用来检查和下载更新，不收集使用数据。

## 反馈

问题和建议请提交到本仓库的 [Issues](https://github.com/wbopan/claude-in-codex-releases/issues)。

---

Claude in Codex 是独立项目，与 Anthropic、OpenAI 没有关联。Claude、Claude Code 是 Anthropic 的商标，Codex、ChatGPT 是 OpenAI 的商标。App 附带的第三方组件许可证见 `Claude in Codex.app/Contents/Resources/THIRD_PARTY_NOTICES.txt`。
