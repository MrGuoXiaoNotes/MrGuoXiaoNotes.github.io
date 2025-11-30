# 使用 Hugo 创建和预览草稿文章

## 创建新文章

使用以下命令新建一篇文章：

```bash
hugo new content/posts/my-first-post.md
```

Hugo 会在 `content/posts` 目录下创建文件。用编辑器打开该文件，内容如下：

```toml
+++
title = 'My First Post'
date = 2024-01-14T07:07:07+01:00
draft = true
+++
```

注意：`draft` 的值为 `true`，表示该文章为草稿。默认情况下，Hugo 构建网站时不会发布草稿内容。更多关于草稿、未来发布和过期内容的信息请参考 Hugo 文档。

## 编辑文章内容

在文章正文部分添加 Markdown 内容，例如：

```markdown
+++
title = 'My First Post'
date = 2024-01-14T07:07:07+01:00
draft = true
+++
## 简介

这是 **加粗** 文字，这是 *斜体* 文字。

访问 [Hugo](https://gohugo.io) 官网！
```

无需修改 `draft` 的值。

## 启动开发服务器并预览草稿

保存文件后，使用以下命令启动 Hugo 的开发服务器并包含草稿内容：

```bash
hugo server --buildDrafts
# 或
hugo server -D
```
