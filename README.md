# 个人主页

基于 Jekyll 和 GitHub Pages 的个人博客网站，用于发布工作心得和技术分享。

## 功能特点

- 📝 使用 Markdown 编写文章，简单高效
- 🎨 简洁现代的 UI 设计，响应式布局
- 🚀 自动部署到 GitHub Pages
- 📱 完全响应式，支持移动端访问
- 🔍 SEO 优化，支持搜索引擎索引

## 技术栈

- **Jekyll**: 静态站点生成器
- **GitHub Pages**: 免费托管服务
- **Markdown**: 文章编写格式

## 本地开发

### 前置要求

- Ruby 3.1 或更高版本
- Bundler gem

### 安装步骤

1. 克隆仓库：
```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

2. 安装依赖：
```bash
bundle install
```

3. 启动本地服务器：
```bash
bundle exec jekyll serve
```

4. 在浏览器中访问 `http://localhost:4000`

## 部署到 GitHub Pages

### 方法一：使用 GitHub Actions（推荐）

1. 将代码推送到 GitHub 仓库
2. 在仓库设置中：
   - 进入 Settings > Pages
   - Source 选择 "GitHub Actions"
3. 每次推送到 `main` 或 `master` 分支时，GitHub Actions 会自动构建并部署网站

### 方法二：使用 Jekyll 构建

1. 在仓库设置中：
   - 进入 Settings > Pages
   - Source 选择 "Deploy from a branch"
   - Branch 选择 `main` 或 `master`，文件夹选择 `/ (root)`
2. GitHub 会自动使用 Jekyll 构建网站

## 添加新文章

1. 在 `_posts/` 目录下创建新的 Markdown 文件
2. 文件名格式：`YYYY-MM-DD-文章标题.md`
3. 文件开头添加 front matter：

```markdown
---
layout: post
title: 文章标题
date: 2024-01-15
author: Your Name
---

文章内容...
```

4. 提交并推送到 GitHub，网站会自动更新

## 自定义配置

编辑 `_config.yml` 文件来自定义网站：

- 修改站点标题、描述和作者信息
- 配置导航菜单
- 添加社交链接
- 调整其他 Jekyll 设置

## 项目结构

```
.
├── _config.yml          # Jekyll 配置文件
├── _posts/              # 博客文章目录
├── _layouts/            # 布局模板
├── _includes/           # 可复用组件
├── assets/              # 静态资源（CSS、图片等）
├── index.html           # 首页
├── about.md             # 关于页面
├── .github/
│   └── workflows/       # GitHub Actions 工作流
├── Gemfile              # Ruby 依赖
└── README.md            # 项目说明
```

## 许可证

MIT License

## 联系方式

如有问题或建议，欢迎通过以下方式联系：

- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com
