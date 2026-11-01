# ming

一个可直接部署到 GitHub Pages 的 Hugo 博客骨架，使用 PaperMod 主题，并包含 GitHub Actions 自动发布。

## 已包含

- 首页、文章列表、文章详情页
- 归档页、标签页、关于页
- 基于 Fuse.js 的本地搜索
- RSS、站点地图、robots.txt
- 中文界面和示例文章
- GitHub Actions 自动构建与部署
- 响应式布局、浅色/深色模式

## 本地预览

安装 Hugo Extended 和 Git 后，在项目根目录运行：

```bash
hugo server -D
```

打开 `http://localhost:1313`。

如果使用 Windows，也可以先安装：

```powershell
winget install --id Hugo.Hugo.Extended -e
winget install --id Git.Git -e
```

## 当前配置

- GitHub 用户名：`ChenXiaoming233`
- 站点名称：`ming`
- 推荐仓库名：`ChenXiaoming233.github.io`
- 站点地址：`https://chenxiaoming233.github.io/`

站点名称、作者、描述和首页文案都集中在 `hugo.yaml`，个人介绍在 `content/about.md`。

## 创建 GitHub 仓库并上线

1. 在 GitHub 新建仓库，命名为 `ChenXiaoming233.github.io`。
2. 在项目目录执行：

```bash
git add .
git commit -m "init blog"
git branch -M main
git remote add origin https://github.com/ChenXiaoming233/ChenXiaoming233.github.io.git
git push -u origin main
```

3. 打开 GitHub 仓库的 `Settings → Pages`。
4. 将 `Build and deployment → Source` 设置为 `GitHub Actions`。
5. 等待 Actions 完成，访问 `https://chenxiaoming233.github.io/`。

## 写文章

创建文章：

```bash
hugo new content posts/my-new-post.md
```

编辑生成的文件，把 `draft: true` 改为 `draft: false`，然后预览：

```bash
hugo server -D
```

发布：

```bash
git add .
git commit -m "post: my new post"
git push
```

图片放在 `static/images/`，文章中这样引用：

```markdown
![图片说明](/images/example.jpg)
```

## 自定义域名

1. 在 `Settings → Pages → Custom domain` 填写域名。
2. 在 DNS 服务商添加解析：

```text
www.example.com  CNAME  chenxiaoming233.github.io
```

根域名通常使用 GitHub Pages 的 A 记录：

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

3. 在 GitHub Pages 设置中启用 `Enforce HTTPS`。
4. 将 `hugo.yaml` 的 `baseURL` 改为 `https://example.com/`。

## 更新主题

主题以 Git submodule 形式安装。更新主题：

```bash
git submodule update --remote --merge themes/PaperMod
git add themes/PaperMod
git commit -m "chore: update PaperMod"
```

## 说明

- `public/` 是构建产物，不应提交到仓库。
- GitHub Actions 会递归拉取主题 submodule，因此不要删除 `.gitmodules`。
- 免费 GitHub 账户的 Pages 通常要求仓库公开。
- PaperMod 使用 MIT License，主题版权归原作者所有。
