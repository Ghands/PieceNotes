---
title: 关于本站建设的相关说明
date: 2022-11-20
modify: 2022-11-20
author: Zhenhao Wu
keywords: 
    - website
---

本站建设主要依赖以下工具：
- 网页发布：[GitHub Pages](https://pages.github.com)
- 网页框架：[Docsify](https://docsify.js.org)
- 编辑器：[Zettlr](https://zettlr.com)

# GitHub Pages

GitHub Pages 是 GitHub 方便开源项目建设主页所提供的功能，无成本、向所有人开放。还具有以下功能[^1]：
- 无须自己购买云服务，无需明白过多的操作细节，只需按步骤一步步操作即可；
- 支持的功能多，玩法丰富，可以绑定自己的域名，使用免费的 HTTPS，完全由自己维护；
- 搭建之后只需要专注于内容更新，系统维护、文件存储等事情都由 GitHub 处理。

当然，GitHub Pages 也存在不影响大局的缺点：
- 相关 repo 必须是 `public` 的；
- 必须要熟悉 `git` 的相关操作。

GitHub Pages 的操作非常简单，主要分为以下步骤：
1. 在 GitHub 上创建一个属性为公开的仓库；
2. 在仓库的 `Settings` - `Pages` - `Build and deployment` - `Branch` 中选择一个分支，然后选择网站文件的根目录，如：`main` 分支的 `/` 目录；
3. 可以在 `Custom domain` 中设置域名，但还需要其他的操作，本人未尝试。

# Docsify

一般来说，博客的页面都是 `HTML` 页面，大家的 `Markdown` 文件需要通过手动或 `Github Actions` 转换成 `HTML` 文件，但 Docsify 能直接动态显示 `Markdown` 文件，省去了转换的过程。Docsify 的动态显示虽然需要消耗一定的资源，但考虑以下因素之后，我觉得 Docsify 香：
1. 需要的资源不多；
2. 用的是 Github 的免费资源；
3. 只操作 `Markdown` 文件省心省力。

Docsify 的使用非常简单：
1. 安装 `nodejs` 和包管理工具 `npm`；
2. 使用 `npm` 安装 `docsify`: `npm i docsify-cli -g`；
3. 初始化 Docsify 项目：`docsify init .`，生成 `index.html`，`README.md`，`.nojekyll` 文件；
4. `index.html` 文件中存储 Docsify 项目的相关配置，可以参考 [awesome-docsify](https://github.com/docsifyjs/awesome-docsify) 这个项目中的例子；
5. `README.md` 中记录主页显示的内容；
6. 本地预览：运行`docsify serve .`，然后使用浏览器打开 `localhost:3000` 查看网站效果；
7. 在线发布：将本地内容同步到 GitHub 对应仓库后，进入`https://[name].github.io/[repo]`查看效果，`[name]` 表示 GitHub 账号名，`repo` 表示仓库名。

Docsify 可以通过 `_sidebar.md` 等文件设置侧边栏的内容，具体不再赘述。

# Zettlr

Zettlr 是非常好用的 `Markdown` 编辑器，尤其适合写篇幅长、内容专业、公式多的文章，推荐大家使用。

[^1]: https://sspai.com/post/54608