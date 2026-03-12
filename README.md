# 划词翻译 (Simple Select Translate)

一个轻量的 Chrome / Edge 划词翻译扩展，无需安装任何依赖，无构建步骤。

## 功能

- **划词翻译** — 选中文字后出现小圆点「译」，悬停即显示翻译结果
- **语音朗读** — 自动朗读原文（Web Speech API）
- **AI 解释** — 可选接入 OpenAI 兼容 API，流式输出词义与例句
- **单词本** — 记录查询历史，支持按日期导出

## 安装

1. 下载或克隆本仓库
2. 打开 `chrome://extensions`（或 `edge://extensions`），启用**开发者模式**
3. 点击**加载已解压的扩展程序** → 选择本仓库根目录

## 使用

选中任意网页文字 → 悬停出现的「译」圆点 → 查看翻译与 AI 解释。

中文 → 翻译为英文；其他语言 → 翻译为中文。

## AI 配置（可选）

点击扩展图标打开设置，填入 OpenAI 兼容的 API 信息：

| 字段 | 说明 |
|------|------|
| API URL | 如 `https://api.openai.com/v1/chat/completions` |
| API Key | `sk-...` |
| 模型名称 | 如 `gpt-3.5-turbo` |

不填则仅使用 Google 翻译。

## 文件结构

```
├── content.js       # 核心逻辑（划词、翻译、AI 流式输出）
├── content.css      # 圆点与浮窗样式
├── background.js    # MV3 Service Worker
└── popup/           # 设置页面
```

## License

MIT
