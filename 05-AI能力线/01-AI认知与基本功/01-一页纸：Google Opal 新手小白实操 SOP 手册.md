---
title: 一页纸：Google Opal 新手小白实操 SOP 手册
node_token: KkNowR5kzi77jokv4nfcpVrJnTe
source: https://www.feishu.cn/wiki/KkNowR5kzi77jokv4nfcpVrJnTe
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
# 一页纸：Google Opal 新手小白实操 SOP 手册

本手册旨在帮助没有任何编程基础的新手，通过 Google Opal 快速搭建自动化工作流。

## 一、 准备工作

1. **账号准备**：

   - 需要一个 Google 账号。
   - 访问地址：[opal.google](https://opal.google) （注意：可能需要特定的网络环境或访问权限，部分功能归属于 Google Labs）。
   - 建议开通 Gemini Advanced（部分高级模型如 Gemini 1.5 Pro/Ultra 可能需要，但 Opal 目前很多基础模型有免费额度）。
2. **核心概念理解（仅 4 个节点）**：

   - **User Input (用户输入)**：用来接收你输入的信息（如文字主题、上传图片）。
   - **Generate (生成)**：工作流的大脑。调用 AI 模型（写文章、画图、做视频、配音）。
   - **Output (输出)**：展示最终结果（网页形式、保存到文档等）。
   - **Add Assets (添加素材)**：导入外部文件（如本地图片、YouTube 视频链接）。

---

## 二、 实操案例 1：全自动 UGC 广告生成器 (0 代码/AI 对话建流)

**目标**：输入产品和模特图，自动生成广告图、视频、配音和音乐。

### 步骤 1：创建项目

1. 登录 Opal 首页。

   - 点击右上角或中心的 **"Create New" (新建)**。
2. 此时你会看到一个对话框 "Describe what you want to build" (描述你想构建什么)。

### 步骤 2：通过对话生成工作流

1. 在对话框中输入以下提示词（Prompt）：

\> “我要做一个UGC广告生成器。用户输入：产品名称、产品图片、模特图片、广告创意描述、广告语、背景音乐风格。

\> 请根据这些信息：

\> 1. 生成高质量的UGC广告图片。

\> 2. 根据广告语生成语音配音。

\> 3. 根据风格生成背景音乐。

\> 4. 生成一段UGC风格的广告视频。

\> 最后在一个页面展示所有结果。”

1. 点击发送，等待 AI 自动构建节点连线。

### 步骤 3：关键模型调整 (小白必看！)

AI 自动生成的配置大部分可用，但 **画图模型** 需要手动优化以获得最佳人像效果。

1. 在画布中找到 **"Generate Image" (生成图片)** 的节点。
2. 点击该节点，在右侧设置面板中找到 Model (模型) 选项。
3. **修改模型**：默认可能是 `Gemini 2.5 Flash Image`，请手动点击下拉菜单，更改为 **`Gemini 3 Pro Image`** (部分版本显示为 Nano Banana Pro)。

   - *原因：Pro 模型对人脸和细节的还原度远高于 Flash 模型，避免模特脸部崩坏。*

### 步骤 4：运行与测试

1. 点击右上角的 **Start** 按钮。
2. **Product Name**：输入产品名（如：小黑瓶精华）。
3. **Product Image**：上传一张白底或干净背景的产品图。
4. **Model Image**：上传一张真人模特图。
5. **Creative Description**：描述画面（如：模特在浴室，手持产品微笑，光线柔和）。
6. **Ad Slogan**：输入广告语（如： 空格   焕发青春光彩  空格  ）。

   - *技巧：前后加空格可防止配音吞字或不一致。*
7. **Music Style**：输入风格（如：轻快、高级感、钢琴曲）。
8. 点击执行，等待 1-2 分钟。

### 步骤 5：保存与导出

1. 在右侧预览区查看生成的 4 个素材（图、视频、音频、音乐）。
2. 满意后，可以单独下载这些素材，放入**剪映等软件**进行合成。

---

## 三、 实操案例 2：手动搭建“爆款文章写手” (进阶理解)

**目标**：输入主题，AI 自动联网搜索研究，并生成图文并茂的文章保存到 Google Doc。

### 步骤 1：搭建输入与研究

1. 点击画布空白处，添加 **User Input** 节点 -> 命名为“文章主题”。
2. 添加 **Generate** 节点，连接到输入节点。

   - 模型选择：`Plan and Execute` (适合复杂任务)。
   - 开启工具：点击 Tools，勾选 `Search Web` (联网搜索) 和 `Get Webpage`。
   - 提示词：`针对[文章主题]进行深度研究，生成一份包含历史背景、核心观点和未来趋势的研究报告。`

### 步骤 2：生成大纲与正文

1. 添加 **Generate** 节点（大纲），连接上一步。

   - 模型：Gemini 1.5 Pro 或 2.5。
   - 提示词：`根据研究报告，生成一个详细的文章大纲。`
2. 添加 **Generate** 节点（正文），连接大纲节点。

   - 提示词：`根据大纲和研究报告，撰写一篇深度的博客文章，使用Markdown格式。`

### 步骤 3：生成配图

1. 添加 **Generate** 节点，连接到正文节点。

   - 模型：**Gemini 3 Pro Image**。
   - 提示词：`根据文章内容，设计一张极简科技风格的Banner头图，不要有文字。`

### 步骤 4：输出与保存

1. 添加 **Output** 节点。
2. 在 Output 设置中，选择 **"Save to Google Docs"**。
3. 运行工作流，输入主题（如“什么是 SORA”），AI 将自动写好文章并存入你的网盘。

---

## 四、 实用技巧与避坑指南

1. **Remix (混音/复用) 大法**：

   - 在 Opal 的 Gallery (画廊) 中有很多别人做好的 App（如菜谱生成器）。
   - 不要从头做，直接点进去按 **Remix**，这会复制一份给你。

   - 修改其中的 Prompt (提示词)，例如把“Generate in English”改为“请用中文输出”，即可快速通过本土化获得一个新工具。

2. **图片一致性**：

   - 如果发现生成的广告图里模特换了张脸，记得在提示词里强调：“Keep the model's face consistent with the uploaded image” (保持模特面部与上传图片一致)。
3. **Add Assets 的妙用**：

   - 想做视频总结？不用手动复制文字。直接拖入一个 `Add Assets` 节点，选择 YouTube，粘贴链接，然后连一个 Generate 节点写总结即可。
4. **备份**：

   - 不用担心数据丢失，Opal 生成的所有工作流文件会自动保存在你的 Google Drive 的 `Opal` 文件夹中。

社交：

---
> [!info]- 🧭 导航
> ⬆️ 上级：[Google Opal 新手小白实操 SOP 手册](60-Google%20Opal%20新手小白实操%20SOP%20手册.md)

---

<details>
<summary>原文配图上的文字（3 条，图片本身未随文提供）</summary>

**四实用技巧与避坑指南**

- 「Get topic」 「Do Research」 「Write Outline」 「Write Post」 「Create Banner Image」 「Display Blog Post」 「Blog Post Writer」 「Start」
- 「Search Web」 「Get Webpage」 「Get topic」
- 「血条上的生死线」 「它是精准的数学模型，更是惊心动魄的心理博弈。揭秘游戏世界中最令肾上腺素飙升的临界点」

</details>
