<table width="100%">
  <tr>
    <td align="left" width="120">
      <img src="https://raw.githubusercontent.com/OpenCut-app/OpenCut/main/apps/web/public/logos/opencut/logo.png" alt="OpenCut Logo" width="100" />
    </td>
    <td align="right">
      <h1>OpenCut</h1>
      <h3 style="margin-top: -10px;">一个免费、开源的视频编辑器，适用于 Web、桌面和移动设备。</h3>
    </td>
  </tr>
</table>

## 赞助商

感谢 [Vercel](https://vercel.com?utm_source=github-opencut&utm_campaign=oss) 和 [fal.ai](https://fal.ai?utm_source=github-opencut&utm_campaign=oss) 对开源软件的支持。

<a href="https://vercel.com/oss">
  <img alt="Powered by Vercel" src="https://img.shields.io/badge/Powered%20by-Vercel-000000?style=flat&logo=vercel&logoColor=white" />
</a>

<a href="https://fal.ai">
  <img alt="Powered by fal.ai" src="https://img.shields.io/badge/Powered%20by-fal.ai-000000?style=flat&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyIDJMMTMuMDkgOC4yNkwyMCAxMEwxMy4wOSAxNS43NEwxMiAyMkwxMC45MSAxNS43NEw0IDEwTDEwLjkxIDguMjZMMTIgMloiIGZpbGw9IndoaXRlIi8+Cjwvc3ZnPgo=" />
</a>

## 为什么选择 OpenCut？

- **隐私保护**：您的视频保留在本地设备上
- **免费功能**：CapCut 的大部分基础功能现已收费
- **简单易用**：人们需要易于使用的视频编辑器 —— CapCut 证明了这一点

## 功能特性

- 时间线编辑
- 多轨道支持
- 实时预览
- 无水印、无订阅
- 由 [Databuddy](https://www.databuddy.cc?utm_source=opencut) 提供分析服务，100% 匿名且无侵入性。
- 博客由 [Marble](https://marblecms.com?utm_source=opencut) 提供支持，无头 CMS。

## 项目结构

- `apps/web/` – Next.js 主 Web 应用
- `src/components/` – UI 和编辑器组件
- `src/hooks/` – 自定义 React Hooks
- `src/lib/` – 工具函数和 API 逻辑
- `src/stores/` – 状态管理（Zustand 等）
- `src/types/` – TypeScript 类型定义

## 快速开始

### 前置要求

- [Bun](https://bun.sh/docs/installation)
- [Docker](https://docs.docker.com/get-docker/) 和 [Docker Compose](https://docs.docker.com/compose/install/)

> **注意**：Docker 是可选的，但推荐用于运行本地数据库和 Redis。如果只想开发前端功能，可以跳过 Docker。

### 安装步骤

1. Fork 并克隆仓库

2. 复制环境文件：

   ```bash
   # Unix/Linux/Mac
   cp apps/web/.env.example apps/web/.env.local

   # Windows PowerShell
   Copy-Item apps/web/.env.example apps/web/.env.local
   ```

3. 启动数据库和 Redis：

   ```bash
   docker compose up -d db redis serverless-redis-http
   ```

4. 安装依赖并启动开发服务器：

   ```bash
   bun install
   bun dev:web
   ```

应用将在 [http://localhost:3000](http://localhost:3000) 可访问。

`.env.example` 中的默认配置与 Docker Compose 配置相匹配 —— 开箱即用。

### 使用 Docker 自托管

使用 Docker 运行所有服务（包括应用的生产构建）：

```bash
docker compose up -d
```

应用将在 [http://localhost:3100](http://localhost:3100) 可访问。

## 贡献指南

我们欢迎贡献！虽然我们正在积极开发和重构某些领域，但仍然有很多机会可以有效贡献。

**🎯 重点领域：** 时间线功能、项目管理、性能优化、错误修复以及预览面板之外的 UI 改进。

**⚠️ 目前避免：** 预览面板增强（字体、贴纸、效果）和导出功能 —— 我们正在使用新的二进制渲染方法重构这些功能。

查看我们的 [贡献指南](https://github.com/OpenCut-app/OpenCut/blob/main/.github/CONTRIBUTING.md) 了解详细的设置说明、开发指南和完整的方向指引。

**贡献者快速入门：**

- Fork 仓库并克隆到本地
- 按照 CONTRIBUTING.md 中的设置说明操作
- 创建功能分支并提交 PR

## 基于

本项目基于 [OpenCut](https://github.com/OpenCut-app/OpenCut) 开源项目。

## 许可证

[MIT 许可证](https://github.com/OpenCut-app/OpenCut/blob/main/LICENSE)

---

![Star History Chart](https://api.star-history.com/svg?repos=opencut-app/opencut&type=Date)
