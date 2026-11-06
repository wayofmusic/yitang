---
title: 🚀 Google Antigravity + Claude Opus 4.5 零基础实战SOP
node_token: SMuGwFk5wiBE6qkDYtXc0HebnCc
source: https://www.feishu.cn/wiki/SMuGwFk5wiBE6qkDYtXc0HebnCc
space: 一堂学习
obj_type: docx
synced: 2026-09-26 06:21
course_line: AI能力线
stage: AI认知与基本功
train: AI认知与基本功
form: 课程逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
# 🚀 Google Antigravity + Claude Opus 4.5 零基础实战SOP

## 📖 前言：为什么要用这个工具？

- **核心优势：** Google Antigravity 是一款集成AI的开发环境（IDE），最新集成了 **Claude Opus 4.5 (Thinking)** 模型。
- **解决痛点：** 很多用户直接使用Claude官方账号容易被封号，使用Antigravity可以直接调用Opus 4.5，且账号更安全，支持多智能体异步工作（能同时写前端和后端）。
- **适用人群：** 想要快速开发全栈应用、重构代码，但不想手动配置繁琐环境的小白或开发者。

---

## 🛠 第一阶段：准备与安装

### 1. 下载软件

- **动作：** 访问 Google Antigravity 官方下载页面（视频中显示界面）。
- **选择版本：** 根据你的电脑系统选择：

  - macOS (Apple Silicon/Intel)
  - Windows (x64/ARM64)
  - Linux
- **安装：** 下载完成后，按照常规软件安装流程进行安装。

### 2. 账号准备

- **Google账号：** 用于登录Antigravity。
- **Supabase账号（后端必备）：** 访问 `supabase.com` 注册一个账号（用于后续自动生成数据库）。
- **大模型API Key（可选但推荐）：** 如需在项目中调用其他AI（如Mistral），需提前准备好Key。

---

## ⚙️ 第二阶段：核心配置（由AI接管的规矩）

这一步非常关键，相当于告诉AI“我家的装修风格和施工标准”，以后它干活就不会乱来。

### 1. 设置全局规则 (Customizations)

- **路径：** 打开Antigravity -> 点击右上角“三个点” -> 点击 **`Customizations`** -> 在Rules栏下点击 **`+ Global`**。
- **操作：** 会打开一个 `GEMINI.md` 文件，这是给AI看的规则书。
- **填写内容（小白可直接抄作业，视频推荐配置）：**

  - **Python开发规则：**

    - 版本：指定使用 Python 3.11
    - 命令：强制使用 `python3` 而非 `python`
    - 环境：使用 `python3 -m venv venv` 创建虚拟环境
  - **全栈开发规则（Next.js + Supabase）：**

    - 前端框架：Next.js 14 (App Router)
    - 样式：TailwindCSS
    - 后端/数据库：Supabase
    - **强制约束：** 所有数据库表必须启用RLS（安全策略），API Key放入 `.env` 文件等。
- **保存：** 填写完毕后，保存并关闭该文件。

### 2. 配置后端工具 (MCP Server)

- **路径：** 点击右上角“三个点” -> 点击 **`MCP Servers`**。
- **搜索：** 在搜索框输入 `supabase`。
- **安装与配置：**

  1. 点击进入Supabase详情页。
  2. 点击 `Configure`。
  3. **获取Access Token：**

     - 去 Supabase 官网登录 -> 点击头像 -> `Account Settings` -> `Access Tokens` -> `Generate new token`。
     - 取个名字（如 MyProject），过期时间选 Never，生成后**复制Token**。
  4. **填入Antigravity：** 回到软件界面，将Token粘贴到输入框，点击 `Save`。
- **自检：** 在对话框输入“检查Rules和supabse mcp是否设置成功”，AI会自动运行命令检测，看到全绿（Active/Success）即为成功。

---

## 💻 第三阶段：实战演练 A - 代码重构（进阶版）

*场景：你有一段别人的代码（如微软AutoGen写的），想改成谷歌ADK框架写的。*

1. **新建项目：** 打开Antigravity -> `Open Folder` -> 新建一个文件夹并打开。
2. **选择模型：** 在对话框右侧模型列表，务必选择 **`Claude Opus 4.5 (Thinking)`**。
3. **选择模式：** 简单任务选 **`Fast`** 模式。
4. **输入提示词（Prompt）：**

   - 提供官方文档链接（如Google ADK文档）。
   - 明确任务：将 [原框架] 的代码重构为 [新框架] 代码。
   - 提出具体要求：保留原有逻辑，API接口改为 Mistral AI，添加UI界面。
5. **执行过程：**

   - AI会自动阅读文档、创建虚拟环境（点击 `Allow` 允许运行命令）、安装依赖。
   - **人工干预点：** 如果AI提示需要API Key，手动去项目文件夹下的 `.env` 文件里填入你的 Key。
6. **测试运行：**

   - 输入“请为我启动Web UI”。
   - 点击终端生成的 `localhost` 链接，在浏览器中查看重构后的效果。

---

## 🏗 第四阶段：实战演练 B - 从零开发全栈APP（小白重点）

*场景：做一个“宠物领养平台”MVP（最小可行性产品）。*

### 1. 项目初始化

- **新建文件夹：** 比如叫 `MyPets-Platform`，在Antigravity中打开。
- **模型与模式：**

  - 模型：**`Claude Opus 4.5 (Thinking)`**（思考能力最强）。
  - 模式：**`Planning`**（规划模式，适合复杂项目，它会先写计划书）。

### 2. 输入需求（Prompt模板）

复制以下逻辑发送给AI：

> **项目概述：** 开发一个现代化的宠物领养平台MVP。
>
> **技术栈：** 前端 Next.js 14 + TailwindCSS；后端 Supabase。
>
> **核心功能：** 用户注册/登录（Google/Github）、宠物列表展示（带筛选）、宠物详情页、领养申请流程、发布领养信息。
>
> **UI要求：** 响应式设计，黑夜模式，美观大气。

### 3. AI执行流程（看着它干活）

1. **生成计划：** AI会列出 Step 1 到 Step N 的详细计划（数据库设计、认证系统、UI组件等）。
2. **批准执行：** 点击 `Proceed`（继续）。
3. **自动构建：**

   - AI会自动初始化 Next.js 项目。
   - **调用MCP：** AI会自动操作你的 Supabase 账号，在云端创建数据库表、设置SQL规则（这一步以前需要手动做，现在全自动）。
4. **人工辅助（关键点）：**

   - 在构建过程中，AI可能会生成 `.env.example` 文件。
   - 你需要把 `.env.example` 复制一份改名为 `.env.local`。
   - **填空：** 这是一个必须手动的环节。去 Supabase 后台复制 `Project URL` 和 `Anon Key`，填入 `.env.local` 文件中。

### 4. 运行与调试

- **启动项目：** 对话框输入“请为我运行项目”。
- **查看效果：** 浏览器打开 `localhost:3000`。
- **功能测试：**

  - 测试注册/登录（邮件验证码注册通常最稳）。
  - 测试发布功能：上传图片、填写宠物信息。
- **遇到Bug怎么办？（小白必学）：**

  - *案例：* 图片发布后显示不出来。
  - *操作：* 浏览器右键点击坏图 -> `检查(Inspect)` -> 复制那段 HTML 代码。
  - *喂给AI：* 回到Antigravity，粘贴代码并说：“发布宠物时图片不显示，这是元素代码，请修复”。
  - *结果：* AI会分析是权限问题还是代码问题，并自动修改代码修复。

---

## 📝 总结与注意事项

1. **关于模型：** 做复杂项目（尤其是从0到1）一定要用 **Claude Opus 4.5**。虽然是Pro账号功能，但在代码逻辑和一次性成功率上远超其他模型。
2. **关于额度：** 视频实测，Pro账号高强度开发两个完整项目，Opus 4.5的额度依然够用，无需过分担心。
3. **遇到报错不要慌：** 直接把报错信息（红色文字）复制粘贴回对话框，Antigravity 会自动读取并尝试修复，这就是AI IDE的魅力。
4. **MCP是神器：** 务必配置好 Supabase 的 MCP，它能让AI拥有操作数据库的“双手”，否则你需要自己去网页端建表，非常麻烦。

按照这个SOP，即使你不懂具体的代码语法，也能通过指挥AI构建出一个功能完整的Web应用！加油！

---
> [!info]- 🧭 导航
> ⬆️ 上级：[柴翔：🚀 Gemini AI 精准修图/改图保姆级 SOP(aistudio)](45-柴翔：🚀%20Gemini%20AI%20精准修图／改图保姆级%20SOP%28aistudio%29.md)
