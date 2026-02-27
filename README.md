# 个人博客

基于 Jekyll 和 GitHub Pages 搭建的个人博客，使用 Markdown 编写文章。

## 本地开发

### 环境要求

- Ruby 3.0+（macOS 可用 `brew install ruby` 或 rbenv 安装较新版本）
- Bundler：`gem install bundler`

> 若本地 Ruby 版本较旧，`bundle install` 可能失败，但推送后 GitHub Pages 会在云端构建，部署不受影响。

### 运行

```bash
bundle install
bundle exec jekyll serve
```

访问 http://localhost:4000 预览。Ruby 3.0+ 若报错，可执行 `bundle add webrick`。

## 撰写文章

在 `_posts/` 目录下新建 Markdown 文件，命名格式：`YYYY-MM-DD-标题.md`

```markdown
---
layout: post
title: "文章标题"
date: 2025-02-27 10:00:00 +0800
categories: 分类名
---

正文内容...
```

## 部署

推送代码到 `main` 分支后，GitHub Pages 会自动构建并部署到 https://lizirui.github.io

首次部署需在仓库 Settings → Pages 中确认发布源为 `main` 分支的根目录。
