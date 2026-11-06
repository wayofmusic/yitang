---
title: 🚀 【小白必看】打造顶级博主 AI 第二大脑 SOP
node_token: R60Rw2azjiujZWk2ZMpcxCOknzf
source: https://www.feishu.cn/wiki/R60Rw2azjiujZWk2ZMpcxCOknzf
space: 一堂学习
obj_type: docx
synced: 2026-09-26 06:20
course_line: AI能力线
stage: AI认知与基本功
train: AI认知与基本功
form: 课程逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
# 🚀 【小白必看】打造顶级博主 AI 第二大脑 SOP

## 🛠️ 核心逻辑

1. **抓取**：把博主所有视频的字幕（文案）下载下来。
2. **加工**：用 AI 把乱糟糟的字幕翻译、润色成可读性强的文章（Markdown格式）。
3. **克隆**：把整理好的文章喂给 NotebookLM，生成 AI 顾问。
4. **内化**：导入 Obsidian 建立知识库，深度学习。

---

## 📦 第一阶段：环境与工具准备 (一次性工作)

在开始之前，我们需要安装几个免费工具。不要怕，按步骤点点点就行。

### 1. 安装 Python (运行脚本的基础)

- **下载**：去 Python 官网下载最新版安装包。
- **安装（⚠️关键一步）**：运行安装包时，**务必勾选底部的 `Add Python to PATH`**，然后一直点 "Next" 直到完成。

### 2. 安装 yt-dlp (下载视频字幕的神器)

- **操作**：

  1. 在电脑桌面新建一个文件夹（例如叫 `AI_Learning`）。
  2. 进入文件夹，在空白处按住 `Shift` 键 + 点击鼠标**右键**，选择“**在此处打开 Powershell 窗口**”或“**在终端中打开**”。
  3. 在黑框框里输入以下命令并回车：

     ```Bash
     pip install yt-dlp
     ```
  4. 等待跑完代码，显示安装成功。

### 3. 安装浏览器插件 (为了伪装成真人)

- **工具名**：`Get cookies.txt LOCALLY`
- **操作**：

  1. 打开 Chrome 或 Edge 浏览器的扩展商店。
  2. 搜索并安装 `Get cookies.txt LOCALLY`。
  3. **获取 Cookie**：

     - 用浏览器登录你的 YouTube 账号。
     - 点击浏览器右上角的这个插件图标。
     - 点击 **`Export`** 按钮，你会得到一个 `.txt` 文件。
     - 把这个文件改名为 `www.youtube.com_cookies.txt`，放到刚才新建的 `AI_Learning` 文件夹里。

### 4. 安装 LM Studio (本地 AI 大模型运行器)

- **下载**：去 LM Studio 官网下载并安装。
- **下载模型**：

  1. 打开 LM Studio，点击左侧放大镜图标（搜索）。
  2. 搜索 `qwen-3-8b-instruct` (通义千问，翻译效果好且速度快)。
  3. 在右侧选择一个版本下载（推荐 `Q4_K_M` 或 `Q5_K_M` 版本）。
- **开启服务**：

  1. 点击左侧“开发者/Local Server”图标（像个 `At` 符号的）。
  2. 顶部选择刚才下载的模型。
  3. 点击 **`Start Server`** 按钮。
  4. **⚠️关键设置**：点击旁边的 Settings，确保 **`Enable CORS`** 选项是**打开**的（绿色）。

---

## 📥 第二阶段：批量获取数据 (自动下载字幕)

我们要把博主的几百个视频字幕一次性抓下来。

### 1. 准备脚本

- *注：视频作者提供了现成的 Python 脚本（*`run_channel_downloader.py`），你需要去他的主页或视频简介获取。假设你已经把脚本放到了 *`AI_Learning` 文件夹。*

### 2. 修改脚本配置

1. 右键点击 `run_channel_downloader.py`，选择用记事本打开（或者用 VS Code）。
2. 找到代码开头的配置区，修改两处：

   - `CHANNEL_URL = "这里填你想抓取的博主主页链接"` (例如 Dan Koe 的主页)。
   - `COOKIE_FILE = "www.youtube.com_cookies.txt"` (确保文件名和你下载的一致)。
3. 保存并关闭。

### 3. 运行脚本

1. 回到 `AI_Learning` 文件夹，打开终端（右键+终端）。
2. 输入命令：

   ```Bash
   python run_channel_downloader.py
   ```
3. **结果**：程序会自动运行，把该博主所有视频的字幕文件（`.vtt` 格式）下载到你的文件夹里。可能需要几分钟到十几分钟。

---

## 🧠 第三阶段：数据清洗与翻译 (AI 批量润色)

原始字幕有很多时间轴和乱码，我们需要用本地 AI 把它变成漂亮的文章。

### 1. 准备清洗脚本

- *注：同样使用作者提供的脚本（*`translate_vtt_to_md.py`），放入 *`AI_Learning` 文件夹。*

### 2. 修改脚本配置

1. 用记事本打开 `translate_vtt_to_md.py`。
2. 修改配置：

   - `VTT_FOLDER_PATH`: 指向刚才下载字幕的文件夹路径。
   - `OUTPUT_FOLDER_PATH`: 设置一个你想保存处理后文件的路径。
   - `API_URL`: 默认通常是 `http://127.0.0.1:1234/v1/chat/completions` (这是 LM Studio 的默认地址，不用改)。
   - `MAX_TOKENS_PER_CHUNK`: 根据你电脑性能设置，一般 `2500` 左右比较稳。
3. 保存。

### 4. 运行清洗

1. **确保 LM Studio 的 Server 正在运行（第一阶段第4步）。**
2. 在终端输入命令：

   ```Bash
   python translate_vtt_to_md.py
   ```
3. **结果**：你会看到黑框里一行行代码跳动，AI 正在逐个阅读字幕、翻译成中文、去掉时间轴、整理成 Markdown 笔记。
4. 去喝杯咖啡，这步比较耗时（处理一个视频约3-5分钟）。

---

## 🤖 第四阶段：构建 AI 私人顾问 (最后一步)

现在你手里已经有几百篇高质量的 Markdown 笔记了，我们来“复活”博主。

### 使用 Google NotebookLM

1. 访问 **Google NotebookLM** 官网。
2. 点击“新建笔记本”，起个名字叫“Dan Koe AI 顾问”。
3. 点击 **`上传来源`** -> 选择 **`Markdown`** (或者把所有笔记文件拖进去)。

   - *注意：如果 NotebookLM 不支持直接传大量 Markdown，可以先转成 PDF 或者直接复制粘贴关键内容，或者利用脚本把所有 MD 合并成一个大文件上传。*
4. **见证奇迹**：

   - 上传完成后，你可以直接在对话框问它：“Dan Koe 关于如何实现财务自由的核心观点是什么？”
   - 它会基于这几百个视频的内容，给你精准的回答，并标注出处！
   - 你还可以点击 **`Audio Overview`**，让 AI 生成一段两个主持人讨论这些知识的播客（英文）。

---

## 📚 第五阶段：深度学习 (Obsidian 知识库)

把这些处理好的 Markdown 文件导入 **Obsidian**。

1. 打开 Obsidian，将存放 Markdown 文件的文件夹作为“仓库”打开。
2. 现在你拥有了该博主的完整知识库。
3. **怎么学？**

   - 搜索关键词。
   - 利用双向链接建立知识关联。
   - 在 NotebookLM 聊出灵感后，回到 Obsidian 做深度笔记。

---

## 💡 备选方案 (如果你觉得 Python 太难)

如果你实在搞不定代码和脚本，可以用 **Notion 方案**：

1. 下载字幕文件后。
2. 使用 **Notion** 的导入功能。
3. 使用 **Notion AI** 的“自定义自动填充”功能，设置 Prompt（提示词）：

\> "将原文翻译成流畅的中文，去除时间轴，提取核心观点。"

1. 这需要购买 Notion AI 会员，但省去了配置本地代码的麻烦。

---

## 📝 总结：你得到了什么？

通过这套流程，你没有花一分钱（除了电费），就完成了：

1. **全自动下载** 100+ 小时的顶级视频内容。
2. **全自动翻译/润色** 成几百万字的中文高质量文稿。
3. **拥有了一个 24 小时在线的 AI 导师**，他拥有该博主的所有智慧。

现在，去行动吧！先从下载 Python 开始！

---
> [!info]- 🧭 导航
> ⬆️ 上级：[柴翔：🚀 Gemini AI 精准修图/改图保姆级 SOP(aistudio)](45-柴翔：🚀%20Gemini%20AI%20精准修图／改图保姆级%20SOP%28aistudio%29.md)
