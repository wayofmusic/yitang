---
title: 柴翔：Gemini 3 应用花式部署指南（小白必看版）
node_token: Lepiw0B1FixSK1k6D3Jceq4Bns9
source: https://www.feishu.cn/wiki/Lepiw0B1FixSK1k6D3Jceq4Bns9
space: 一堂学习
obj_type: docx
synced: 2026-09-26 05:28
course_line: AI能力线
stage: AI认知与基本功
train: AI认知与基本功
form: 课程逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
# 柴翔：Gemini 3 应用花式部署指南（小白必看版）

## 背景

**核心目标：** 将 Google AI Studio 生成的有趣应用，免费部署成你自己可以访问、分享的网站。

**用到工具：** **Google AI Studio、GitHub、Vercel/Netlify/EdgeOne**、以及 AI 编程工具（如 **Github deskeop**/**Cursor/VS Code**）。

---

## 第一部分：部署“无AI功能”的静态应用

**（适合纯展示类的网页、小游戏，不需要消耗Token）**

### 1. 生成并保存代码

- **步骤：** 打开 Google AI Studio，点击左侧 `Build`，输入提示词生成应用（或者选择官方样列，例如“量化研究可视化”或“3D跑酷游戏”）。
- **操作：** 点击右上角 `保存到 GitHub` 图标。点击右下角 save

  - 如果没登录 GitHub，**按提示登录。**
  - 给仓库起个名字（Repository name），点击 `Create git repo`。

  - 点击  `Create Git repo`，点击右下角 `Stage and cpmmit all changes`

  - 点击顶部弹出的链接进入 GitHub 仓库页面。

### 2. 关键修改：修复入口文件（这是很多小白容易卡住的地方！）

- **步骤：** 在 GitHub 仓库页面，找到并点击 `index.html` 文件。

- **操作：**

  1. 点击右上角的“铅笔”图标（编辑模式）。

  1. 滑到代码最底部，在 `</body>` 标签上方，添加一行代码引用 React 入口文件：

     ```HTML
     <script type="module" src="/index.tsx"></script>
     ```

  1. 点击右上角 `Commit changes` 保存修改。

### 3. 选择平台进行部署（任选其一）

#### 方案 A：使用 Vercel 部署（推荐，速度快）

1. 打开 [Vercel 官网](https://vercel.com/)，点击 `Log in`，选择 `Continue with GitHub`。

，点击`Log in`，选择`Continue with GitHub`”的操作步骤。](https://feishu.cn/file/Oj1GbYYa3o4pX1xQkiTcwxYxnTh)

1. 点击 `Add New...` -> `Project`。

1. 在左侧列表中找到刚才保存的项目，点击 `Import`。
2. **配置环境变量（关键点）：**

   - 展开 `Environment Variables`。

   - Key 填：`GEMINI_API_KEY`
   - Value 填：`12345` （**注意：** 因为是无AI功能的静态项目，这里随便填个假的占位即可，千万别填真的！）

3. 点击 `Deploy`。等待片刻，出现撒花特效即成功。

   - *提示：****Vercel 分配的域名国内可能无法直连****，可以在 Settings -> Domains* ***绑定自己的域名****。*

#### 方案 B：使用 Netlify 部署（备选）

1. 打开 Netlify 官网，GitHub 登录。
2. 点击 `Add new project` -> `Import an existing project` -> `GitHub`。
3. 授权后选择你的项目仓库。
4. 同样添加环境变量：Key 填 `GEMINI_API_KEY`，Value 随便填。

1. 点击 `Deploy`。Netlify 分配的域名国内通常可以直接访问。

#### 方案 C：使用腾讯云 EdgeOne Pages（国内访问最快）

- 操作步骤与 Vercel/Netlify 基本一致，生成的域名国内可直连。

---

## 第二部分：部署“有AI功能”的应用

**（例如 SVG 生成器、AI 对话工具，需要调用 API）**

**⚠️ 安全警告：** 纯前端项目直接部署会将你的 API Key 暴露给所有人（别人右键查看源代码就能偷走你的 Key）。我们需要更高级的部署方法。

### 方法一：使用 Google Cloud 部署（官方、自动保护）

- **前提：** 你需要有 **Google Cloud 账号并绑定了信用卡**（开启结算功能）。
- **操作：**

  1. 在 AI Studio 编辑器右上角，点击“火箭图标”（Deploy）。

  1. 选择 `Deploy app on Google Cloud`。

  1. 选择一个已绑卡的项目（Project）。

  1. 点击部署。谷歌会自动通过网关隐藏你的 Key。

### 方法二：代码改造 + Vercel 部署（免费、安全、推荐！）

**原理：** 利用 AI 编程工具，将项目改造成前后端分离（Next.js），把 API Key 藏在后端。

#### 1. 克隆项目到本地

- 使用 [**`GitHub Desktop`**](https://desktop.github.com/download/)**（点击下载）** 软件：File -> Clone repository -> 搜索你的项目 -> Clone 到本地文件夹。
- 或者 **下载zip解压缩，再打开**

#### 2. 本地修复与 AI 改造

1. **修复 index.html：** 同样先在本地把 `index.html` 缺少的 `<script...>` 代码补上。

滑到代码最底部，在 `</body>` 标签上方，添加一行代码引用 React 入口文件：

> <script type="module" src="/index.tsx"></script>

1. **AI 改造（核心）：** 打开 AI 编程工具（如 Codex、Cursor 或 ChatGPT）

   - **提示词：** “把这个项目改造成一个 Next.js 的前后端应用，注意 GEMINI_API_KEY 要安全的存放在后端，在后端调用 AI 功能，确保我的 API Key 不会泄露。”
   - 等待 AI 帮你重写代码结构（通常会生成 `app/api` 目录用于后端）。

#### 3. 本地测试

1. 在项目根目录新建文件 `.env.local`。
2. 去 AI Studio 获取真实的 API Key。
3. 在 `.env.local` 中写入：`GEMINI_API_KEY=你的真实Key`。

1. 在终端输入 `npm run dev` 启动测试，确保功能正常。

#### 4. 上传并部署

1. **提交代码：** 在 **GitHub Desktop** 中填写提交信息，点击 `Commit to main`，然后点击 `Push origin`。

2. **Vercel 部署：**

   - 回到 Vercel，导入这个新改造的项目。
   - **关键点：** 在 Environment Variables 中，Key 填 `GEMINI_API_KEY`，Value 填 **你真实的 API Key**（因为这次是在后端调用，是安全的）。
   - 点击 `Deploy`。

#### 5. 验证安全

- 打开部署好的网站，F12 打开开发者工具 -> 网络（Network）。
- 你会发现请求是发给自己网站的后端接口（如 `/api/generate`），而不是直接发给 Google，且请求头里看不到 Key。

---

## **总结：**

- **没AI功能的网页：** 只要补一行代码，随便找个平台部署，**Key 填假的。**
- **有AI功能的网页：** 为了钱包安全**，必须把 Key 藏在后端**。最简单的办法是让 AI 帮你把代码改成 Next.js 框架，然后再部署。

## 社交分享

觉得这个教程有用吗？分享给更多需要的朋友，或许他们会用AI创造出更有意思的作品，

感谢你看到这里，我是柴翔，一名正在积极探索 AI 赋能的演说教练。

这是我的一堂介绍和名片

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI使用手册](01-AI使用手册.md)

---

<details>
<summary>原文配图上的文字（31 条，图片本身未随文提供）</summary>

**1生成并保存代码**

- 「Save to Hub」 「AI Features」 「Add animations」 「AlphaQubit」 「AI for Quantum Error Correction」 「关键修改：修复入口文件」
- 「Make a new copy」 「Save」 「Name」 「Description」 「Copy of Research Visualization」 「Research paper reimagined as an elegant, interactive narrative site.」 「Cancel」 「关键修改：修复入口文件」
- 「Copy of Research Visualization」 「on main」 「Fill out the information below to create your repo and make your first commit」 「Repository name」 「paper - research」 「Repository description」 「Visibility」 「Private」 「给仓库起个名字（Repository name），点击`Create git repo`」
- 「Create git repo」
- 「Stage and commit all changes」 「关键修改：修复入口文件」

**2关键修改修复入口文件这是很多小白容易卡住的地方**

- 「feat: Initialize project with Vite and React」 「部署无AI功能静态应用」
- 「关键修改：修复入口文件」
- 「module」 「/index.tsx」 「添加一行代码引用React入口文件」 「无AI功能」
- 「Commit changes」

**方案A使用Vercel部署推荐速度快**

- 「Log in to Vercel」 「Email Address」 「Continue with Email」 「Continue with Google」 「Continue with GitHub」 「Last Used」 「Continue with SAML SSO」 「Continue with Passkey」
- 「gemini-balance-lite」 「hot-air-balloon-travel」 「edge-one-code」 「Connect Git Repository」 「Add New...」
- 「Framework Preset」 「Vite」 「Root Directory」 「Build and Output Settings」 「Environment Variables」 「配置环境变量（关键点）」
- 「Environment Variables」 「GEMINI_API_KEY」 「12345」 「方案A：使用Vercel部署」
- 「方案A：使用Vercel部署（推荐，速度快）」 「Settings」 「Action Deployment」 「Repository」 「Build Logs」 「Runtime」

**方案B使用Netlify部署备选**

- 「Push your ideas to the web」 「Ask Netlify」
- 「GEMINI_API_KEY」 「123124」 「Deploy runner-game」

**方案C使用腾讯云EdgeOnePages国内访问**

- 「Tencent EdgeOne」 「Accelerate Globally」 「使用腾讯云EdgeOne Pages部署国内访问最快」 「Learn More」

**方法一使用GoogleCloud部署官方自动保护**

- 「部署应用」
- 「Deploy app on Google Cloud」 「Select a Cloud Project」 「Deploy app」
- 「Deploy app on Google Cloud」 「创建项目」 「FreeProject1」 「GooglePaidProject」
- 「App successfully deployed to Google Cloud」 「This app is using the following API key」

**2本地修复与AI改造**

- 「module」 「/index.tsx」
- 「把这个项目改造成一个Next.js的前后端应用，注意GEMINI_API_KEY要安全的存放在后端，在后端调用AI功能，确保我的API Key不会泄露」 「Auto context」 「AI改造（核心）」
- 「AI改造（核心）」

**3本地测试**

- 「.env.local」 「GEMINI_API_KEY=」
- 「本地测试」
- 「What do you want to create?」 「a futuristic cyberpunk helmet with neon li」 「Generate」 「Retro Goggles」 「Space Rocket」

**4上传并部署**

- 「No local changes」 「Push origin」 「提交代码」
- 「Environment Variables」 「GEMINI_API_KEY」 「yAeTe6XzZXf9ZpvWcFOe8z9qR1LgEnR1oY...」 「方法二：代码改造+Vercel部署」 「Deploy」

**5验证安全**

- 「验证安全」

**社交分享**

- 「一堂 YiTang.top」 「已加入一堂 555天」

</details>
