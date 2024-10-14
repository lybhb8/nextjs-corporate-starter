
- [英文](./README.md) 

- [中文](./README_CN.md)

**重点提示:**

感谢所有精彩的人的支持——这个项目太棒了！随着 Strapi 5 的发布，@Mcastres 推出了一个更棒的演示/入门项目，名为 **LaunchPad**。

您可以在[此处](https://strapi.io/blog/launchpad-demo-app) 了解有关   **LaunchPad** 应用程序的更多信息, 查看项目 repo：https://github.com/strapi/LaunchPad 。

这意味着什么？我们将存档此项目，并以 **LaunchPad** 作为新的启动项目和 demo 继续前进。

如果您有兴趣将此项目更新至 Strapi 5，您可以在以下[branch](https://github.com/strapi/nextjs-corporate-starter/tree/strapi-5-update-process "分支")中找到代码，我已经在此[blog post](https://strapi.io/blog/how-to-migrate-your-project-from-strapi-4-to-strapi-5 "博客文章")中概述了相关步骤。

如果您对迁移有任何疑问，请随时在此处提问或在 **Discord** 的开放办公时间加入我们，我将现场为您解答。

上午会议：加入我们美国中部标准时间凌晨 4 点（格林威治标准时间上午 9 点）的早会，非常适合我们的全球社区成员！

下午会议：不要忘记我们 CST 下午 12:30（GMT 下午 6:30）的常规会议，这是下午休息和聊天的好时机！

https://discord.com/invite/strapi

# Strapi Starter Next 14, Tailwind, Typescript and Strapi

注意：这个项目是由 [Trecia](https://github.com/TreciaKS), [Daniel](https://github.com/malgamves)、和[Paul](https://github.com/PaulBratslavsky) 精心发起的。我们都是 Next 14 和 Typescript 的新手。如果您发现任何错误或需要改进，请随时创建问题。感谢大家的支持和参与。

![demo-site](https://user-images.githubusercontent.com/6153188/231865321-0da5e81f-4832-4cce-bcd1-ecd79e9b9cc3.gif)


## Hello Strapi

Strapi Community Edition (社区版)是一款免费的开源无头 CMS，可让您在任何地方管理任何内容。

- **自托管或云：** 您可以按照自己想要的方式托管和扩展 Strapi 项目。您可以通过部署到Strapi Cloud或部署到您想要的托管平台来节省时间**：AWS、Azure、Google Cloud、DigitalOcean。
- **现代管理窗格：** 优雅、完全可定制且完全可扩展的管理面板。
- **多数据库支持**：您可以选择您喜欢的数据库：PostgreSQL、MySQL、MariaDB 和 SQLite。
- **可定制**：您可以通过完全定制 API、路线或插件来快速构建您的逻辑，以完美满足您的需求。
- **极快且强大**：Strapi 基于 Node.js 和 TypeScript 构建，提供可靠而稳定的性能。
- **前端自由**：使用任何前端框架（React、Next.js、Vue、Angular 等）、移动应用程序甚至物联网。
- **默认安全**：可重复使用的策略、CORS、CSP、P3P、Xframe、XSS 等。
强大的 CLI：即时搭建项目和 APIs

## Features

- **Content Types Builder** (内容类型构建器)：为内容管理员构建最灵活的发布体验，让他们可以自由地使用字段、组件和动态区域创建任何页面。
- **Media Library** (媒体库)：将图片、视频、音频或文档上传到媒体库。轻松找到合适的资产，编辑并重复使用。
- **Internationalization** (国际化)：国际化 (i18n) 插件允许 Strapi 用户创建、管理和分发不同语言的本地化内容，称为“语言环境
- **Role Based Access Control** (基于角色的访问控制)：为管理员和最终用户创建无限数量的自定义角色和权限。
- **GraphQL or REST**：使用 REST 或 GraphQL 使用 API .

您可以解锁[Strapi Cloud](https://cloud.strapi.io/login?source=github1) or [Strapi Enterprise](https://strapi.io/enterprise?source=github1) 中的其他功能，例如 SSO、审计日志、审查工作流。

## Getting Started

如果你喜欢指导你完成设置过程的视频，可以在[这里](https://github.com/strapi/nextjs-corporate-starter/issues/71)找到。

1. 克隆项目到本地(Clone the repository locally):

```bash
  git clone https://github.com/strapi/nextjs-corporate-starter.git
    or
  gh repo clone strapi/nextjs-corporate-starter
```

2. 前端(frontend)和后端(backend)分别安装依赖(Run `yarn` command to setup  and backend dependencies):

提示：为了加快下载速度，先重新设置 yarn 镜像源地址。

设置为淘宝镜像源，可以使用下面的命令：
```bash
yarn config set registry https://registry.npmmirror.com
```
切回原镜像源，可以使用下面的命令：
```bash
yarn config set registry https://registry.yarnpkg.com
```
提前设置 **sharp** 包的镜像地址（不然国内,在下面安装依赖时，可能出现 "install sharp Command failed"
```bash
yarn config set sharp_binary_host https://npmmirror.com/mirrors/sharp

yarn config set sharp_libvips_binary_host https://npmmirror.com/mirrors/sharp-libvips
```


然后执行：

```bash
# cd frontend
  yarn
```

```bash
# cd backend
 yarn
```

3. 接下来，导航到 /backend 目录并设置您的.env文件。可以使用 .env.example 文件作为参考：

```bash
HOST=localhost
PORT=1337
APP_KEYS="toBeModified1,toBeModified2"
API_TOKEN_SALT=tobemodified
ADMIN_JWT_SECRET=tobemodified
JWT_SECRET=tobemodified
TRANSFER_TOKEN_SALT=tobemodified
```

4. 在 /backend 目录，通过运行以下命令启动您的项目(backend)：

```bash
  yarn build
  yarn develop
```

(在chrome/Edge 浏览器中) 系统提示您创建第一个管理员用户。

![admin-user](https://user-images.githubusercontent.com/6153188/231865420-5f03a90f-b893-4057-9634-9632920a7d97.gif)

太棒了! 现在项目已运行。让我们添加一些数据。

## Seeding The Data（导入数据）

我们将使用DEITS 功能，它可以轻松地将数据导入您的项目。

可以在[此处](https://docs.strapi.io/dev-docs/data-management)的文档中了解更多信息。

在项目根目录中，有我们的 **seed-data.tar.gz** 文件。将使用它来导入数据。

1. 打开 **终端** 并确保仍在 /backend 文件夹中。

2. 运行以下命令来播种您的数据：

```bash
  yarn strapi import -f ../seed-data.tar.gz
```

![after-import](https://user-images.githubusercontent.com/6153188/231865491-05cb5818-a0d0-49ce-807e-a879f7e3070c.gif)

这会将您的数据导入本地。重新登录管理面板即可查看新导入的数据。

以下是一个简短的视频，介绍初始设置和数据导入。

https://github.com/strapi/nextjs-corporate-starter/assets/6153188/80f00bf5-d17b-449d-8a0d-7f0d9614f40b

## Setting Up The Frontend(前端设置)

提示：这个过程很重要，涉及前端与后端的数据交互，必须正确设置。可以参考：[操作演示视频](https://www.youtube.com/watch?v=a23JvssqrrQ&t=199s)

接下来我们需要切换到我们的 '/frontend' 目录并创建我们的 '.env'文件并粘贴以下内容。

```bash
NEXT_PUBLIC_STRAPI_API_TOKEN=your-api-token
NEXT_PUBLIC_PAGE_LIMIT=6
NEXT_PUBLIC_STRAPI_FORM_SUBMISSION_TOKEN=your-form-submission-token
NEXT_PUBLIC_STRAPI_API_URL=http://localhost:1337

```

在启动我们的 Next JS 应用程序之前，我们需要进入我们的 **Strapi Admin** 并创建两个令牌，我们将使用它们提交表单和显示我们的内容。

在您的 Strapi 管理面板中导航至 `Settings` -> `API Tokens`并单击 `Create new API Token` .

![api-tokens](https://user-images.githubusercontent.com/6153188/231865572-cebc5538-374c-4050-91cd-c303fae25a3d.png)


```bash
# 中文

这是我们的令牌设置

名称：公共 API 令牌内容
描述：访问公共内容。
令牌有效期：无限制
令牌类型：自定义
```
在权限中授予以下访问权限。

|内容|	权限|
|---|---|
|文章	|find 和 findOne|
|作者	|find 和 findOne|
|类别	|find 和 findOne|
|全球的	|find|
|页	|find 和 findOne|
|产品特色	|find 和 findOne|



```bash
# 英文
Here are our Token Settings

Name: Public API Token Content
Description: Access to public content.
Token duration: Unlimited
Token type: Custom
```

In Permissions lets give the following access.

| Content         |   Permissions    |
| --------------- | :--------------: |
| Article         | find and findOne |
| Author          | find and findOne |
| Category        | find and findOne |
| Global          |       find       |
| Page            | find and findOne |
| Product-feature | find and findOne |



![permissions](https://user-images.githubusercontent.com/6153188/231865625-a3634d89-0f40-4a6d-a356-8f654abd88b9.gif)

---

1. PUBLIC API TOKEN

获得令牌后，将其添加到文件 `NEXT_PUBLIC_STRAPI_API_TOKEN` 中的变量名中`.env`(从后端<strapi-admin> 复制到前端 .env)。

**或者**：您可以创建一个 `Read-only` 只读令牌，为所有端点提供读取权限。

在这个特定的项目中，这不是问题。虽然以上是推荐的方法，但我也想在这里向您展示这个选项。

创建令牌时，只需 `Read-only` 从令牌类型下拉菜单中选择选项。

<img width="1093" alt="create-read-only-token" src="https://github.com/strapi/nextjs-corporate-starter/assets/6153188/3ea6c029-b296-4bbc-a5ce-33eedac52a03">

---

2. Public API Form Submit TOKEN

接下来创建一个允许我们提交表单`submit our form`的令牌`token` 。

```bash
# 中文
名称：公共 API 表单提交
描述：表单提交。
令牌有效期：无限制 
令牌类型：自定义
```

在权限中授予以下访问权限

| 内容 | 权限|
| --------| :---------: |
| 潜在客户表单提交 | 创建  |



```bash
# 英文
Name: Public API Form Submit
Description: Form Submission.
Token duration: Unlimited
Token type: Custom
```

In Permissions lets give the following access.

| Content              | Permissions |
| -------------------- | :---------: |
| Lead-Form-Submission |   create    |



将令牌添加到文件 `NEXT_PUBLIC_STRAPI_FORM_SUBMISSION_TOKEN` 中的变量名称 `.env` 中(从后端<strapi-admin> 复制到前端 .env)。

3. Next JS frontend running (前端运行)

设置了环境变量，就可以通过运行来启动前端应用程序 `yarn dev`

```bash
yarn dev
```

您现在应该可以看到您的 Next JS 前端。

![frontend](https://user-images.githubusercontent.com/6153188/231865662-d870051f-4503-4a01-bc6b-635c7c5ca40d.png)

## Start Both Projects Concurrently（两个项目同时启动）

我们还可以使用该concurrently包用一个命令启动两个项目。

package.json 可以在根文件夹内的文件中找到该设置。

```bash
{
  "scripts": {
    "frontend": "yarn dev --prefix ../frontend/",
    "backend": "yarn dev --prefix ../backend/",
    "clear": "cd frontend && rm -rf .next && rm -rf cache",
    "setup:frontend": "cd frontend && yarn",
    "setup:backend": "cd backend && yarn",
    "setup": "yarn install && yarn setup:frontend && yarn setup:backend",
    "dev": "yarn clear && concurrently \"cd frontend && yarn dev\" \"cd backend && yarn develop\""
  },
  "dependencies": {
    "concurrently": "^7.6.0"
  }
}

```

转到根文件夹，先运行安装包 `yarn `命令
```bash
yarn
```


然后运行 `yarn dev` 来同时启动项目下的两个应用程序


```bash
yarn dev
```
OK，这个 demo 项目设置完成了，可以运行演示了！

## Conclusion

Hope you find this starter useful, it is a bare-bone example to help you get started quickly.

Would love to hear what you will build using it.

If you find bugs or have suggestions feel free to create issues.

Thank you and stay awesome.

# Contributing to the Next.js Corporate Starter repository

We're so excited that you're thinking about contributing to the Next.js Corporate Starter open-source project! If you're unsure or afraid of anything, just know that you can't mess up here. Any contribution is valuable, and we appreciate you!

This document aims to provide all the necessary information for you to make a contribution.

## Prerequisites

Before you can contribute, you need to have the following installed:

- Node.js and npm: You can download these from the official [Node.js website](https://nodejs.org/).
- Git: You can find installation instructions for Git in the official [Git Book](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

## Steps to Contribute

### 1. Fork the Repository

In your web browser, navigate to [https://github.com/strapi/nextjs-corporate-starter](https://github.com/strapi/nextjs-corporate-starter). Click the 'Fork' button in the upper right-hand corner of the page. This creates a copy of the repository in your GitHub account.

### 2. Clone your Fork

Now, go to your version of the repository. You can do this by navigating to https://github.com/USERNAME/nextjs-corporate-starter (replace 'USERNAME' with your GitHub username). Here, click the 'Clone' button and then 'Copy to clipboard' to copy the git URL.

Next, you need to open your terminal, navigate to where you want to store the project, and type the following command, followed by 'Enter':

```bash
git clone PASTE_CLONED_REPOSITORY_URL
```

Replace 'PASTE_CLONED_REPOSITORY_URL' with the URL you copied earlier. This command downloads your fork to your computer.

### 3. Add Upstream Repository

Before you can start contributing, you have to set up a reference to the original repository. You can do this with the following command:

```bash
git remote add upstream https://github.com/strapi/nextjs-corporate-starter.git
```

This command adds a new remote, named 'upstream', that points to the original repository.

### 4. Synchronize your Fork

Before you start making changes, you should synchronize your forked repository with the latest changes from the upstream. Here are the steps:

a. Fetch the branches and their respective commits:

```bash
git fetch upstream
```

b. Checkout to the main branch of your fork:

```bash
git checkout main
```

c. Merge changes from the upstream's main branch into your local main branch:

```bash
git merge upstream/main
```

This brings your fork's main branch into sync with the upstream repository, without losing your local changes.

### 5. Create a Branch

When you're making a contribution, it's best to make your changes in a new branch instead of the main branch. You can create a new branch and switch to it using the following command:

```bash
git checkout -b BRANCH_NAME
```

Replace 'BRANCH_NAME' with a name that describes the change you're planning to make.

### 6. Make your Changes

Now, you can start making changes to the project. Feel free to make changes that you think will enhance the project.

### 7. Commit your Changes

When you've made your changes, you need to commit them. This is like creating a save point in a game. You can do this using the following commands:

```bash
git add -A
git commit -m "Your detailed commit message"
```

Replace "Your detailed commit message" with a description of the changes you made.

### 8. Push your Changes

After committing your changes, you need to push them to your forked repository on GitHub. You can do this with the following command:

```bash
git push origin BRANCH_NAME
```

Replace 'BRANCH_NAME' with the name of the branch you created earlier.

### 9. Create a Pull Request

After you've pushed your changes, you're ready to create a pull request (PR). Navigate to your forked repository in your web browser and click on 'Pull request' (near the top of the page), then on 'New pull request'. Ensure that the base fork is the original repository and the base is 'main', and that the head fork is your fork and the compare is the branch you created.

Enter a title for your PR and describe the changes you made. Once you're ready, click 'Create pull request'.

### Congrats! 🎉

You've just made a contribution to the Next.js Corporate Starter project! The team will review your changes and may suggest some modifications or improvements. Once your changes have been approved, they will be merged into the main codebase.

Thank you for your contribution. We appreciate you!

Remember, everyone was new to open-source at some point. If you're unsure about something, don't hesitate to ask for help. Good luck and happy hacking!

### Psst...

If you find yourself contributing frequently, we've provided a script in the package.json to help keep your local project synchronized with the main branch of the upstream (original) project. Simply execute the following command:

```bash
yarn repo:upstream
```

## FAQ

### How do I add additional pages?
Check out [this video](https://youtu.be/EoVrTNA3geM) where I will guide on how to do this.

### How do I update my Strapi version?
Check out this [this issue comment](https://github.com/strapi/nextjs-corporate-starter/issues/17#issuecomment-1558149967)

