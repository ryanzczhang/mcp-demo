# MCP Demo

一个用于验证 GitHub → Vercel 自动部署流程的最小静态站点。

## 本地查看

直接用浏览器打开 `index.html`，或在目录中启动任意静态文件服务器。

## 导入 Vercel

1. 将本目录中的文件提交到 GitHub 仓库 `ryanzczhang/mcp-demo` 的 `main` 分支。
2. 登录 Vercel，选择 **Add New → Project**。
3. 从 GitHub 仓库列表中选择 `mcp-demo` 并点击 **Import**。
4. Framework Preset 选择 **Other**。
5. Root Directory 保持 `./`。
6. Build Command 留空。
7. Output Directory 保持 `./` 或留空使用默认值。
8. 点击 **Deploy**。

之后每次向 `main` 分支推送提交，Vercel 都会自动创建新的 Production Deployment；其他分支或 Pull Request 默认会创建 Preview Deployment。

## 当前结构

```text
.
├── index.html
├── README.md
└── .gitignore
```

该示例没有后端、MCP Server 或密钥。不要把 Token、API Key 等敏感信息写入静态 HTML。
