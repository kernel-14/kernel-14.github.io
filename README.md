# 我的个人主页

这是一个整合了两个GitHub主页的个人网站项目。

## 项目结构

- **主页面**: 基于 arctanxarc.github.io 的 Jekyll 学术主页
- **博客功能**: 整合了 plmsmile.github.io 的 VitePress 博客系统

## 功能特点

1. **学术主页**: 展示个人简介、教育背景、新闻、出版物、荣誉奖项等
2. **博客系统**: 通过导航栏的"Blog"链接访问，包含LLM、强化学习、算法等技术笔记

## 本地运行

### 运行主页 (Jekyll)

```bash
# 安装依赖
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 访问 http://localhost:4000
```

### 运行博客 (VitePress)

博客部分已经是编译好的静态文件，位于 `blog/` 目录下。
当你运行Jekyll服务器时，可以通过 http://localhost:4000/blog/ 访问博客。

## 部署到 GitHub Pages

1. 将此项目推送到你的 GitHub 仓库（仓库名格式：`你的用户名.github.io`）
2. 在仓库设置中启用 GitHub Pages
3. 选择主分支作为发布源
4. 网站将自动部署到 `https://你的用户名.github.io`

## 自定义

### 修改个人信息

编辑 `_config.yml` 文件，修改以下内容：
- 网站标题和描述
- 作者信息（姓名、头像、简介等）
- 社交媒体链接

### 修改主页内容

编辑 `_pages/about.md` 文件来更新主页内容。

### 修改导航栏

编辑 `_data/navigation.yml` 文件来调整导航栏链接。

## 技术栈

- **Jekyll**: 静态网站生成器
- **VitePress**: Vue 驱动的静态网站生成器
- **GitHub Pages**: 免费的静态网站托管服务

## 许可证

请参考原项目的许可证文件。
