---
title: Coze工作流三部曲1-基础使用与入门 副本
node_token: WV3rwZFN4ijzxMkOznQcxtHEnyn
source: https://www.feishu.cn/wiki/WV3rwZFN4ijzxMkOznQcxtHEnyn
space: 一堂学习
obj_type: docx
synced: 2026-09-26 05:27
course_line: AI能力线
stage: AI认知与基本功
train: AI认知与基本功
form: 课程逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
先签到哈

哈喽大家好，我叫赵岩，这次由我给大家分享工作流相关的内容。

> - 本职工作是一名程序员，在一个跨境电商公司负责技术；
> - 和小伙伴一起开了一个户外广告公司，是联合创始人；
> - 同时也在探索新的可能。
> - 最近研究AI比较多，也有一点积累。

我们上一节课讲了“AI提示词”的课程

[一堂西安学习中心-线下提示词课程-配套提示词生成工具](http://yitang.lukezhao.cn/prompt.html)

想必同学们对结构化的提示词已经有感觉了，并且能通过持续的练习进步了。。

我们能认识到，一个优秀的提示词，就是一个能让AI稳定执行任务的“可执行程序”，它将模糊的需求转化为精确的创造指令，把我想干什么，变为--我怎么怎么做，第一步是什么，第二步是什么。

让我们从被动的信息消费者，转变为主动的价值创造者。

有方法，可控制。

但这，仅仅是通往AI自动化生产的起点。

今天，我们将开启一次新的升维之旅：从**设计“单一程序”的架构师**，进阶为**编排“整套智能生产线”的总工程师**。

核心工具，就是 Coze工作流。

如果说，结构化的提示词是给AI的单条精确指令，那么Coze工作流就是为AI搭建的一套全自动、可复用、多步骤的智能流水线。

它将告别单次提问、单点优化的模式，迈向真正的**工程化**、**自动化和系统化。**

我们看一个生成儿童识字卡的工作流。

那为什么需要这一系列

### 从“单点智能”到“流程智能”：为何必须进阶？

在提示词课程中，我们成功地为“掼蛋活动策划”或“销售转化率提升”构建了复杂的提示词。

但大家可能已经发现，一些更宏大的想法，是需要多个步骤协同完成的：

- **内容创作**​：是否想过，从一篇热点文章，到自动生成标题、精炼摘要、扩写内容，再到为它配上一张AI绘制的插图，这一切能否一键完成？
- **视频制作**​：是否期待，输入一个简单的食物名称，AI就能自动生成视频脚本，并调用模型产出成片，实现单条视频百万播放的奇迹？
- **代码优化**​：能否构建一个系统，自动识别代码问题、提供优化方案，并生成详细的评估报告？

### 场景一：全自动内容创作流水线

#### 使用提示词

```Markdown
# 角色
你是一名全栈内容创作助手，负责将热点话题转化为一篇完整的自媒体文章。
# 总体目标
基于我提供的话题，生成一个包含“爆款标题”、“文章摘要”、“扩展正文”和“配图提示词”的完整内容包。
# 工作流程​：
信息理解与分析​：首先，分析我提供的以下热点话题，提炼其核心观点、目标受众和可能的情感基调。
生成标题选项​：基于分析，生成3个吸引眼球的社交媒体文章标题。要求风格各异（如悬念式、数字式、利益式）。
撰写文章摘要​：根据最优的一个标题，撰写一段200字左右的文章摘要，逻辑清晰，抓住精髓。
扩展正文内容​：基于摘要，将文章扩展为一篇800字左右的完整文章，结构清晰，有引言、分点论述和总结。
生成配图提示词​：最后，为这篇文章生成一个适合AI绘画工具（如Midjourney）的详细配图提示词。提示词需描述画面风格、关键元素、色彩氛围等。
# 热点话题
Coze 工作流的使用
```

#### 工作流

### 场景二：AI视频自动生成器

#### 使用提示词

```Markdown
#角色​
你是一名专业的短视频编剧和导演，擅长创作高传播度的美食视频。
#总体目标
为我提供的食物名称，生成一个可以直接用于AI视频生成工具的详细视频脚本和分镜提示。
#工作流程
创意构思​：针对食物“[此处插入食物名称，例如：芒果糯米饭]”，构思一个15秒短视频的核心创意和故事线（例如：展现其制作过程的解压感、或强调其异域风情）。
生成视频脚本​：编写脚本，必须包含以下元素：
镜头序列​：按顺序描述5-7个镜头（如：特写-芒果被切开、全景-蒸熟的糯米饭、慢动作-椰浆浇下）。
旁白/字幕文案​：每个镜头对应的画外音或屏幕字幕文字。
背景音乐/音效建议​：推荐匹配的视频氛围音乐类型和关键音效（如：轻快的热带音乐、清脆的切刀声）。
生成视频生成提示词​：为上述脚本中的每一个镜头，生成一个独立的、极其详细的AI视频生成提示词。提示词需明确包含：主体、动作、视觉风格（如电影感、美食摄影）、光线、色彩等。
输出格式​：请以清晰的JSON格式输出，包含"video_script"和"shot_prompts"两个主要字段。
```

<code>{
  "video_script": {
    "food_name": "芒果糯米饭",
    "core_concept": "通过精致特写与自然光影，展现芒果糯米饭从制作到成品的治愈过程，突出热带风情的清新与甜蜜",
    "shot_sequence": [
      {
        "shot_number": 1,
        "shot_type": "特写",
        "visual_description": "阳光透过窗户洒在案板上，成熟芒果的橙黄色果肉闪烁着诱人光泽，刀锋轻轻划过，果肉自然分离",
        "caption": "选一颗熟透的芒果，感受它的柔软"
      },
      {
        "shot_number": 2,
        "shot_type": "特写",
        "visual_description": "蒸汽缭绕中揭开蒸笼，糯米饭晶莹剔透，颗粒分明，泛着珍珠般的光泽",
        "caption": "糯米蒸到恰到好处的Q弹"
      },
      {
        "shot_number": 3,
        "shot_type": "中景",
        "visual_description": "将糯米饭轻轻压实成圆形，芒果切成优雅的薄片，围绕米饭摆放如花瓣",
        "caption": "简单的摆盘，仪式感满满"
      },
      {
        "shot_number": 4,
        "shot_type": "慢动作特写",
        "visual_description": "浓稠的椰浆从勺中缓缓流下，覆盖在米饭和芒果上，滴落瞬间泛起涟漪",
        "caption": "淋上灵魂的椰浆，甜蜜升级"
      },
      {
        "shot_number": 5,
        "shot_type": "大特写",
        "visual_description": "撒上脆脆的黄金绿豆仁，手指轻捻，绿豆仁落下时产生细微跳动",
        "caption": "最后来点脆脆的口感"
      },
      {
        "shot_number": 6,
        "shot_type": "俯拍全景",
        "visual_description": "成品在芭蕉叶上摆放，背景是热带绿植虚化，阳光勾勒整体轮廓",
        "caption": "一秒穿越到泰国街头"
      },
      {
        "shot_number": 7,
        "shot_type": "第一人称视角",
        "visual_description": "勺子挖起包含芒果、糯米饭和椰浆的一角，拉起细微丝线，送入镜头",
        "caption": "这口软糯香甜，谁能抗拒？"
      }
    ],
    "background_music": "轻快的尤克里里小调，带有海岛风情的打击乐节奏",
    "sound_effects": [
      "清脆的切芒果声",
      "蒸汽喷出的嘶嘶声",
      "椰浆倾倒的粘稠流动声",
      "绿豆仁撒落的沙沙声",
      "满足的咀嚼声（结尾）"
    ]
  },
  "shot_prompts": [
    {
      "shot_number": 1,
      "prompt": "特写镜头，阳光下的成熟芒果，金黄色的果肉充满画面，刀锋切开芒果的瞬间，果肉纤维分明，自然光从左侧窗户射入，形成柔和光影，美食摄影风格，高饱和度色彩，4K画质，浅景深，背景虚化"
    },
    {
      "shot_number": 2,
      "prompt": "蒸汽缭绕的蒸笼特写，揭开笼盖瞬间热气升腾，糯米饭晶莹剔透，颗粒饱满，逆光拍摄突出蒸汽轮廓，电影感光影，暖色调，细节清晰，慢动作效果"
    },
    {
      "shot_number": 3,
      "shot_type": "中景",
      "prompt": "中景镜头，一双手正在摆盘，将糯米饭塑成圆形，芒果片呈花瓣状摆放，动作轻柔流畅，自然光照明，色彩鲜艳，俯拍角度，背景为木质台面，极简风格"
    },
    {
      "shot_number": 4,
      "shot_type": "慢动作特写",
      "prompt": "慢动作大特写，浓稠白色椰浆从勺子边缘缓缓流下，覆盖在黄色芒果和白色米饭上，流动感细腻，水滴飞溅瞬间，高快门速度捕捉，明亮柔和光线，美食广告质感"
    },
    {
      "shot_number": 5,
      "shot_type": "大特写",
      "prompt": "微距镜头，手指捻起金黄色绿豆仁撒向食物，绿豆仁落下的轨迹清晰，慢动作捕捉跳动瞬间，侧光突出纹理，色彩对比鲜明，治愈风"
    },
    {
      "shot_number": 6,
      "shot_type": "俯拍全景",
      "prompt": "俯拍全景，芒果糯米饭完整摆盘在芭蕉叶上，周围点缀热带树叶虚化，阳光斜射形成光斑，小清新风格，色彩明亮，景深较浅，构图平衡"
    },
    {
      "shot_number": 7,
      "shot_type": "第一人称视角",
      "prompt": "第一人称视角，勺子挖取芒果糯米饭，拉起丝状椰浆，食物纹理清晰可见，动态捕捉，暖色调灯光，令人垂涎欲滴的效果，4K高清，浅景深"
    }
  ]
}</code><figure view-type="Preview"><source name="75aabb8c-00a4-4784-b8b4-c02748a80379.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="704.000000" size="4947282" token="CXe9bTRvpoWk28x4IHVcozvontg"/></figure>

#### 工作流

### 场景三：智能代码审查与优化系统

这个我简单给大家讲一下

我就是专门审核代码问题的，对于一个陌生的系统，首先得先大概看懂这个系统干了个什么。

然后审核对应的代码，是有一定的逻辑的。

先看有没有业务层面的问题

再看代码引用模块是否合规

最后看书写方式是否违规。

一个提示词写完是比较累的，而且根据项目会有变动，有的没有详细的业务，就是看引用的逻辑。

有的没有引用三方的模块，就想审核书写方式。这样提示词就一直根据项目变。

在这种场景下，写一个通用工作流的话，才能商业化。

所以这些复杂场景，单靠一个提示词难以胜任，而Coze工作流却能轻松实现。它通过“拖拉拽”的方式，将大模型、代码节点、逻辑判断、循环、插件等核心节点连接起来，构建出能够理解复杂意图、顺序执行任务的智能体。

所以我们这节课的核心就是：

**我们将从一个Coze小白，到会设计会编排的AI总工程师，让我们一起，开启这场激动人心的Coze工作流之旅！**

# Coze平台

我们简单介绍一下Coze平台

## 什么是Coze

扣子是字节出品的一站式AI Agent 开发平台。它是个低代码甚至是无代码平台，无论我们是否有编程基础，都可以在扣子上快速搭建基于大模型的各类 AI 应用，并将 AI 应用发布到各个社交平台、通讯软件，比如微信，飞书。

我们可以把 Coze（扣子） 理解成一个「智能工具组装平台」—— 不用我们写复杂代码，像搭积木一样，就能做出属于自己的 “智能小助手”，帮我们处理各种事。

扣子上能做很多事情，文字，图片，视频基本上目前都有相对应的插件来实现。

## 为什么选择Coze

**✅灵活的工作流设计**

扣子提供了大量灵活可组合的节点，包括大语言模型 LLM、自定义代码、判断逻辑等，无论我们是否有编程基础，都可以通过拖拉拽的方式快速搭建一个工作流。

**✅无限拓展的能力集**

扣子集成了丰富的插件工具，极大地拓展智能体的能力边界。扣子官方发布了多款能力丰富的插件，我们可以直接将这些插件添加到智能体中。扣子平台也支持创建自定义插件，自定义插件也可以发布到商店，供其他用户使用。

**✅丰富的数据源**

扣子提供了简单易用的知识库功能，支持智能体与我们自己的数据进行交互。无论是本地文件还是某个网站的实时信息，都可以上传到知识库中。这样，我们的智能体就可以使用知识库中的内容回答问题了。

## Coze的货币，资源点

我们使用扣子可以调用各种大模型，以及各式各样的插件，他们都是第三方提供的服务，有一些是需要收费的，相当于我们使用这些收费的第三方服务时，是会消耗我们的资源点，如果资源点不够，那么我们的智能体的工作就会受到限制，相当于车没油一样，跑不了了。

## 官网地址

我们一起进入网站看看

https://www.coze.cn/

https://www.coze.cn/home

这是Coze（又称扣子）平台官网的页面局部截图，页面上方导航栏包含“扣子空间 BETA”“开发平台”“调试工具”等选项，其中“开发平台”选项被红色箭头明确指向。结合上下文可知，此处指向的是该平台的开发入口，帮助用户进入对应功能区域，用于后续使用平台的开发相关服务，实现智能体搭建、调用第三方服务等操作，而使用这些服务会消耗平台的资源点，资源点不足将限制智能体的运行。

## 工作空间介绍

## 工作流

Coze 工作流（Coze Workflow）是扣子（Coze）这个 AI 聊天机器人／智能体开发平台里的一个**核心模块**，用来把一个复杂的业务／任务拆成多个步骤（节点），在平台上可视化地串联起来执行。

**基本概念**

- **节点（Node）**：工作流里的基本组成单位。每个节点做一件事。常见节点类型有：

  - **大语言模型节点（LLM）**：用 AI 模型做文本理解 / 生成之类的任务

  - **代码节点（Code）**：写代码处理数据、做计算、改格式等逻辑操作

    这是Coze工作流中代码节点的配置界面，核心分为输入、代码、输出三个模块，还带有异常处理区域。输入模块设置变量名为input，类型为字符串；代码模块的编辑区内带有示例代码，标注可通过params获取节点输入的变量值，且已成功注入运行环境；输出模块列出了多个输出变量，包括类型为字符串的key0、key21，数组型的key1以及对象型的key2，用于展示代码处理后生成的不同类型结果，契合代码节点处理数据、执行计算或格式调整的功能定位。

  - **插件节点（Plugin）**：连接外部 API 或服务（比如查天气、查新闻）

  - **条件节点 / 判断节点（Condition / If-Else）**：根据某些条件决定流程走向

  - **知识库节点（Knowledge）**：从“知识库”中检索相关信息

    这是Coze工作流的知识库写入节点操作界面，该节点仅支持添加一个文档类型的知识库，用于向知识库中录入内容。界面分为输入、知识库、输出三个区域：输入区域需填写变量名“knowledge”，支持通过“上传文件”的方式填入对应内容；知识库区域提示需添加目标文档类型的知识库，设有添加操作按钮；输出区域明确了该节点运行后会返回的结果字段，包括字符串类型的documentId、fileName、fileUrl。

- **开始节点（Start）** & **结束节点（End）**：每个工作流都有起点和终点，节点是串在这两者之间的。
- **流程 / 串联**：我们把这些节点按照逻辑用线连起来，形成 “先做这个 → 再做那个 → 最后输出” 的流程。
- **可视化 + 拖拽式**：在 Coze 上，我们不用写整个逻辑代码，而是拖节点到画布上，用可视化的方式搭流程。
- **模块化 / 嵌套**：工作流可以嵌入另一个工作流，把复杂流程拆得更清楚、可管理性更好。
- **调试 / 运行 / 监控**：我们可以在平台上“试跑”工作流，看到每个节点的输入输出，调试流程。

随堂练习：

这里我们强化一下**节点**这个概念，因为这个是后边使用的核心。

1. 用户输入一个地名，要返回今天的天气。
2. 用户提了一个问题，要从公司上传的“内部政策文档”中找出答案。
3. 生成了一份报告，现在要判断字数是否超过 2000 字。
4. 用户输入一段文字，需要帮他总结要点、改写成更简短的版本。
5. 判断客户输入的是链接还是文字，是链接的话，就调用读取链接的插件。文字就直接进行分析。

## 为什么要用工作流呢

因为很多任务不是一步到位能完成的，而是要多个阶段、多个操作才能完成。如果直接用单一次 AI 调用，可能力不从心、输出不稳定、格式难控。用工作流可以：

- 🏁拆分任务，降低每一步的难度
- 🏁对中间步骤做校验 / 处理 / 决策
- 🏁保证输出格式、数据的一致性
- 🏁更容易维护、调整、扩展
- 🏁更稳定、更可控

举个例子：

> 假设我们想让AI “给我写一篇市场调研报告”
> 我们可能拆成流程：
>
> 1. 用户输入“行业 / 时间范围 / 关键词”
> 2. 用插件节点抓取最新行业数据 /新闻
> 3. 用 LLM 节点做初步分析 /生成框架
> 4. 代码节点 / LLM 节点把框架扩展成文章
> 5. 条件节点判断哪段要补充 /删减
> 6. 最终输出报告

工作流就能把这个串起来，让 Bot 自动按流程执行。

✏️练习拆业务

使用工作流的前提是，能把业务拆开，就像我们提示词的拆解任务这一步。

我们练习练习

这是Coze工作流入门练习场景的配图，展示了针对AI报价助手的任务拆解示例。该场景要求用户将“AI处理用户输入产品清单生成最终报价及折扣说明”的业务拆分为工作流步骤，具体需完成三项核心任务：一是计算产品总价，二是判断总价是否达到优惠门槛，三是生成包含折扣说明的最终报价，下方还给出了“哪一步要计算、哪一步要判断、哪一步要生成文字说明”的提示，用于引导练习者拆解业务任务。

# 基础节点深度练习

## 输入输出节点

1. **输入节点（Input）**：

   - 接收外部输入，比如用户问题、选项、参数
   - 可以设置默认值和数据类型

1. **输出节点（Output）**：

   - 把处理好的内容输出给聊天界面或下一个流程

## 大模型节点配置（AI的“大脑”）

有三点需要注意的：

1. **模型选择**：不同模型擅长的方向不同
2. **提示词编写技巧（Prompt设计）**[一堂西安学习中心-线下提示词课程-配套提示词生成工具](http://yitang.lukezhao.cn/prompt.html)
3. **输出格式设置**

   - JSON、Markdown、纯文本
   - 如何在后续节点中调用JSON字段
   - 小陷阱：输出时注意命名规范

第一步✅：新建大模型节点，并连线

---

第二步✅：选择合适的大模型

https://www.coze.cn/open/docs/guides/model_service

按使用习惯来说，默认的这个豆包·1.5·Pro·32k，就能应付平时的工作需要了。要是有图片的需求，再找支持图片的大模型。

---

第三步✅：配置入参

---

第四步✅：写提示词

我们写一个简单点的，写招聘文案的

```Markdown
#明确目标
写一个招聘的文案
#限定条件
使用稍正式但诙谐的语气
#设定角色
你是一位有10年经验的专业的职业分析师，你可以根据企业需求设计岗位画像，并写出文案
#指定能力
岗位画像设计能力，总结概括能力
```

---

第五步✅：选择输出结果格式

默认是JSON

---

第六步✅：配置输出节点

---

第七步✅：调试

单节点调试

整体调试

## 图片处理节点

### 图像生成

1. 添加一个图片生成节点

1. 根据需求选择模型，主要是看价格和需求质量的ROI

1. 配置画面的比例和质量要求

1. 输入信息

1. 提示词

1. 测试

一幅山水画，背景是绿油油的山，前边有水，水上有舟，晴天

### 画板

还有画图这里，用的比较多的一个节点是画板

1. 添加画板节点

1. 配置画板节点入参

1. 导入底图

1. 调整尺寸

1. 添加文字

1. 调整字号，字体，颜色，间距

1. 修改文字为引用入参

1. 测试

有什么业务场景可以使用呢？

1. 奖状
2. 授权书
3. 识字卡片
4. 小红书的图文卡片
5. ...

## 调试技巧：让工作流“听话”

**讲解重点：**

1. **常见问题排查：**

   - 节点输出为空 → 检查变量名
   - 大模型输出有点傻 → 调整提示词，查看输入变量是否引用
2. **调试工具技巧：**

   - 打开“节点日志”看每一步的输入/输出
   - 逐步运行（Step Run）对比中间结果
   - 善用注释节点记录逻辑

**🖊课堂演练：**

根据工作流的作用，判断工作流应该输出的结果，修改工作流的错误。

1. 输入英文词汇，AI找课本中对应的短文

```JSON
{"type":"coze-workflow-clipboard-data","source":{"workflowId":"7561346333816438825","flowMode":0,"spaceId":"7330473409425719332","isDouyin":false,"host":"www.coze.cn"},"json":{"nodes":[{"id":"146416","type":"3","meta":{"position":{"x":184,"y":-113}},"data":{"nodeMeta":{"title":"大模型","icon":"https://lf3-static.bytednsdoc.com/obj/eden-cn/dvsmryvd_avi_dvsm/ljhwZthlaukjlkulzlp/icon/icon-LLM-v2.jpg","description":"调用大语言模型,使用变量和提示词生成回复","mainColor":"#5C62FF","subTitle":"大模型"},"inputs":{"inputParameters":[{"name":"inpot","input":{"type":"string","value":{"type":"ref","content":{"source":"block-output","blockID":"100001","name":"input"},"rawMeta":{"type":1}}}}],"llmParam":[{"name":"modelType","input":{"type":"integer","value":{"type":"literal","content":"1737521813","rawMeta":{"type":2}}}},{"name":"modleName","input":{"type":"string","value":{"type":"literal","content":"豆包·1.5·Pro·32k","rawMeta":{"type":1}}}},{"name":"generationDiversity","input":{"type":"string","value":{"type":"literal","content":"balance","rawMeta":{"type":1}}}},{"name":"temperature","input":{"type":"float","value":{"type":"literal","content":"0.8","rawMeta":{"type":4}}}},{"name":"maxTokens","input":{"type":"integer","value":{"type":"literal","content":"4096","rawMeta":{"type":2}}}},{"name":"spCurrentTime","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"spAntiLeak","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"prefixCache","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"responseFormat","input":{"type":"integer","value":{"type":"literal","content":"2","rawMeta":{"type":2}}}},{"name":"prompt","input":{"type":"string","value":{"type":"literal","content":"客户输入{{input}}","rawMeta":{"type":1}}}},{"name":"enableChatHistory","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"chatHistoryRound","input":{"type":"integer","value":{"type":"literal","content":"3","rawMeta":{"type":2}}}},{"name":"systemPrompt","input":{"type":"string","value":{"type":"literal","content":"# 角色\n你是一位有着15年英语教学经验的“自主学习教练”，凭借丰富的教学经验和对青少年认知规律的深入研究，善于运用激励式语言，助力学生养成良好的自主学习习惯，引导学生每天自主阅读英语课文，增加理解力，提高英语水平。\n\n## 技能\n1. 根据用户输入，在网络查找对应课文信息，返回课文内容。","rawMeta":{"type":1}}}},{"name":"stableSystemPrompt","input":{"type":"string","value":{"type":"literal","content":"","rawMeta":{"type":1}}}},{"name":"canContinue","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"loopPromptVersion","input":{"type":"string","value":{"type":"literal","content":"","rawMeta":{"type":1}}}},{"name":"loopPromptName","input":{"type":"string","value":{"type":"literal","content":"","rawMeta":{"type":1}}}},{"name":"loopPromptId","input":{"type":"string","value":{"type":"literal","content":"","rawMeta":{"type":1}}}}],"fcParamVar":{"knowledgeFCParam":{}},"settingOnError":{"processType":1,"timeoutMs":180000,"retryTimes":0}},"outputs":[{"type":"string","name":"output"}],"version":"3"},"_temp":{"bounds":{"x":4,"y":-113,"width":360,"height":164},"externalData":{"icon":"https://lf3-static.bytednsdoc.com/obj/eden-cn/dvsmryvd_avi_dvsm/ljhwZthlaukjlkulzlp/icon/icon-LLM-v2.jpg","description":"调用大语言模型,使用变量和提示词生成回复","title":"大模型","mainColor":"#5C62FF","skills":[]}}}],"edges":[]},"bounds":{"x":4,"y":-113,"width":360,"height":164}}
```

1. 输入英文词汇，AI找课本中对应的句子和短文

```JSON
{"type":"coze-workflow-clipboard-data","source":{"workflowId":"7561346333816438825","flowMode":0,"spaceId":"7330473409425719332","isDouyin":false,"host":"www.coze.cn"},"json":{"nodes":[{"id":"146416","type":"3","meta":{"position":{"x":184,"y":-113}},"data":{"nodeMeta":{"title":"大模型","icon":"https://lf3-static.bytednsdoc.com/obj/eden-cn/dvsmryvd_avi_dvsm/ljhwZthlaukjlkulzlp/icon/icon-LLM-v2.jpg","description":"调用大语言模型,使用变量和提示词生成回复","mainColor":"#5C62FF","subTitle":"大模型"},"inputs":{"inputParameters":[{"name":"input","input":{"type":"string","value":{"type":"ref","content":{"source":"block-output","blockID":"100001","name":"input"},"rawMeta":{"type":1}}}}],"llmParam":[{"name":"modelType","input":{"type":"integer","value":{"type":"literal","content":"1737521813","rawMeta":{"type":2}}}},{"name":"modleName","input":{"type":"string","value":{"type":"literal","content":"豆包·1.5·Pro·32k","rawMeta":{"type":1}}}},{"name":"generationDiversity","input":{"type":"string","value":{"type":"literal","content":"balance","rawMeta":{"type":1}}}},{"name":"temperature","input":{"type":"float","value":{"type":"literal","content":"0.8","rawMeta":{"type":4}}}},{"name":"maxTokens","input":{"type":"integer","value":{"type":"literal","content":"4096","rawMeta":{"type":2}}}},{"name":"spCurrentTime","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"spAntiLeak","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"prefixCache","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"responseFormat","input":{"type":"integer","value":{"type":"literal","content":"2","rawMeta":{"type":2}}}},{"name":"prompt","input":{"type":"string","value":{"type":"literal","content":"用户输入：","rawMeta":{"type":1}}}},{"name":"enableChatHistory","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"chatHistoryRound","input":{"type":"integer","value":{"type":"literal","content":"3","rawMeta":{"type":2}}}},{"name":"systemPrompt","input":{"type":"string","value":{"type":"literal","content":"# 角色\n你是一位有着15年英语教学经验的“自主学习教练”，凭借丰富的教学经验和对青少年认知规律的深入研究，善于运用激励式语言，助力学生养成良好的自主学习习惯，引导学生每天自主阅读英语课文，增加理解力，提高英语水平。\n\n## 技能\n1. 根据用户输入，在网络查找对应课文信息，返回课文内容。","rawMeta":{"type":1}}}},{"name":"stableSystemPrompt","input":{"type":"string","value":{"type":"literal","content":"","rawMeta":{"type":1}}}},{"name":"canContinue","input":{"type":"boolean","value":{"type":"literal","content":false,"rawMeta":{"type":3}}}},{"name":"loopPromptVersion","input":{"type":"string","value":{"type":"literal","content":"","rawMeta":{"type":1}}}},{"name":"loopPromptName","input":{"type":"string","value":{"type":"literal","content":"","rawMeta":{"type":1}}}},{"name":"loopPromptId","input":{"type":"string","value":{"type":"literal","content":"","rawMeta":{"type":1}}}}],"fcParamVar":{"knowledgeFCParam":{}},"settingOnError":{"processType":1,"timeoutMs":180000,"retryTimes":0}},"outputs":[{"type":"string","name":"output"}],"version":"3"},"_temp":{"bounds":{"x":4,"y":-113,"width":360,"height":164},"externalData":{"icon":"https://lf3-static.bytednsdoc.com/obj/eden-cn/dvsmryvd_avi_dvsm/ljhwZthlaukjlkulzlp/icon/icon-LLM-v2.jpg","description":"调用大语言模型,使用变量和提示词生成回复","title":"大模型","mainColor":"#5C62FF","skills":[]}}}],"edges":[]},"bounds":{"x":4,"y":-113,"width":360,"height":164}}
```

1. 生成一个带底图的图片标题

```SQL
{"type":"coze-workflow-clipboard-data","source":{"workflowId":"7554222198334373915","flowMode":0,"spaceId":"7330473409425719332","isDouyin":false,"host":"www.coze.cn"},"json":{"nodes":[{"id":"177681","type":"23","meta":{"position":{"x":500,"y":-13}},"data":{"inputs":{"canvasSchema":"{\"version\":\"6.0.0-rc2\",\"width\":1628,\"height\":150,\"backgroundColor\":\"#ffffffff\",\"customVariableRefs\":[],\"objects\":[{\"subTargetCheck\":false,\"interactive\":false,\"width\":1928.7805,\"height\":154.6341,\"backgroundColor\":\"\",\"padding\":0,\"customFixedHeight\":154.6341463414634,\"customId\":\"oBK_RHoBuxL846CxplxwO\",\"customType\":\"img\",\"type\":\"Group\",\"version\":\"6.0.0-rc2\",\"originX\":\"left\",\"originY\":\"top\",\"left\":-150.7741,\"top\":-1.3333,\"fill\":\"rgb(0,0,0)\",\"stroke\":null,\"strokeWidth\":0,\"strokeDashArray\":null,\"strokeLineCap\":\"butt\",\"strokeDashOffset\":0,\"strokeLineJoin\":\"miter\",\"strokeUniform\":false,\"strokeMiterLimit\":4,\"scaleX\":1,\"scaleY\":1,\"angle\":0,\"flipX\":false,\"flipY\":false,\"opacity\":1,\"shadow\":null,\"visible\":true,\"fillRule\":\"nonzero\",\"paintFirst\":\"fill\",\"globalCompositeOperation\":\"source-over\",\"skewX\":0,\"skewY\":0,\"clipPath\":{\"rx\":0,\"ry\":0,\"width\":1928.7805,\"height\":154.6341,\"backgroundColor\":\"\",\"padding\":0,\"type\":\"Rect\",\"version\":\"6.0.0-rc2\",\"originX\":\"left\",\"originY\":\"top\",\"left\":-964.3903,\"top\":-77.317,\"fill\":\"rgb(0,0,0)\",\"stroke\":null,\"strokeWidth\":1,\"strokeDashArray\":null,\"strokeLineCap\":\"butt\",\"strokeDashOffset\":0,\"strokeLineJoin\":\"miter\",\"strokeUniform\":false,\"strokeMiterLimit\":4,\"scaleX\":1,\"scaleY\":1,\"angle\":0,\"flipX\":false,\"flipY\":false,\"opacity\":1,\"shadow\":null,\"visible\":true,\"fillRule\":\"nonzero\",\"paintFirst\":\"fill\",\"globalCompositeOperation\":\"source-over\",\"skewX\":0,\"skewY\":0,\"inverted\":false,\"absolutePositioned\":false},\"layoutManager\":{\"type\":\"layoutManager\",\"strategy\":\"fit-content\"},\"objects\":[{\"cropX\":0,\"cropY\":0,\"width\":921,\"height\":88,\"backgroundColor\":\"\",\"padding\":0,\"customFixedType\":\"auto\",\"type\":\"Image\",\"version\":\"6.0.0-rc2\",\"originX\":\"left\",\"originY\":\"top\",\"left\":-814.4262,\"top\":-77.817,\"fill\":\"rgb(0,0,0)\",\"stroke\":null,\"strokeWidth\":0,\"strokeDashArray\":null,\"strokeLineCap\":\"butt\",\"strokeDashOffset\":0,\"strokeLineJoin\":\"miter\",\"strokeUniform\":false,\"strokeMiterLimit\":4,\"scaleX\":1.7686,\"scaleY\":1.7686,\"angle\":0,\"flipX\":false,\"flipY\":false,\"opacity\":1,\"shadow\":null,\"visible\":true,\"fillRule\":\"nonzero\",\"paintFirst\":\"fill\",\"globalCompositeOperation\":\"source-over\",\"skewX\":0,\"skewY\":0,\"src\":\"https://p3-bot-workflow-sign.byteimg.com/tos-cn-i-mdko3gqilj/c32c226a826a46219df17266d5e9cdbd.png~tplv-mdko3gqilj-image.image?rk3s=81d4c505&x-expires=1789958441&x-signature=xzIp8sskE5STOQzN3%2FswVkbvzPo%3D\",\"crossOrigin\":null,\"filters\":[]},{\"rx\":0,\"ry\":0,\"width\":1628.8523,\"height\":154.6341,\"backgroundColor\":\"\",\"padding\":0,\"type\":\"Rect\",\"version\":\"6.0.0-rc2\",\"originX\":\"left\",\"originY\":\"top\",\"left\":-814.4262,\"top\":-77.317,\"fill\":\"#00000000\",\"stroke\":\"#000000ff\",\"strokeWidth\":0,\"strokeDashArray\":null,\"strokeLineCap\":\"butt\",\"strokeDashOffset\":0,\"strokeLineJoin\":\"miter\",\"strokeUniform\":false,\"strokeMiterLimit\":4,\"scaleX\":1,\"scaleY\":1,\"angle\":0,\"flipX\":false,\"flipY\":false,\"opacity\":1,\"shadow\":null,\"visible\":true,\"fillRule\":\"nonzero\",\"paintFirst\":\"fill\",\"globalCompositeOperation\":\"source-over\",\"skewX\":0,\"skewY\":0}]},{\"fontSize\":92,\"fontWeight\":\"normal\",\"fontFamily\":\"黑体-思源黑体\",\"fontStyle\":\"normal\",\"lineHeight\":1.2,\"text\":\"文本\",\"charSpacing\":0,\"textAlign\":\"center\",\"styles\":[],\"pathStartOffset\":0,\"pathSide\":\"left\",\"pathAlign\":\"baseline\",\"underline\":false,\"overline\":false,\"linethrough\":false,\"textBackgroundColor\":\"\",\"direction\":\"ltr\",\"minWidth\":20,\"splitByGrapheme\":true,\"width\":1570.082,\"height\":200,\"editable\":true,\"backgroundColor\":\"\",\"padding\":23,\"customFixedHeight\":200,\"customId\":\"dPHUHYqe4yQye2DqVpCS8\",\"customType\":\"block_text\",\"type\":\"Textbox\",\"version\":\"6.0.0-rc2\",\"originX\":\"left\",\"originY\":\"top\",\"left\":28.5752,\"top\":27.8217,\"fill\":\"#fffffffe\",\"stroke\":\"#000000ff\",\"strokeWidth\":0,\"strokeDashArray\":null,\"strokeLineCap\":\"butt\",\"strokeDashOffset\":0,\"strokeLineJoin\":\"miter\",\"strokeUniform\":false,\"strokeMiterLimit\":4,\"scaleX\":1,\"scaleY\":1,\"angle\":0,\"flipX\":false,\"flipY\":false,\"opacity\":1,\"shadow\":null,\"visible\":true,\"fillRule\":\"nonzero\",\"paintFirst\":\"fill\",\"globalCompositeOperation\":\"source-over\",\"skewX\":0,\"skewY\":0,\"clipPath\":{\"rx\":0,\"ry\":0,\"width\":1616.082,\"height\":246,\"backgroundColor\":\"\",\"padding\":0,\"type\":\"Rect\",\"version\":\"6.0.0-rc2\",\"originX\":\"left\",\"originY\":\"top\",\"left\":-808.041,\"top\":-123,\"fill\":\"rgb(0,0,0)\",\"stroke\":null,\"strokeWidth\":1,\"strokeDashArray\":null,\"strokeLineCap\":\"butt\",\"strokeDashOffset\":0,\"strokeLineJoin\":\"miter\",\"strokeUniform\":false,\"strokeMiterLimit\":4,\"scaleX\":1,\"scaleY\":1,\"angle\":0,\"flipX\":false,\"flipY\":false,\"opacity\":1,\"shadow\":null,\"visible\":true,\"fillRule\":\"nonzero\",\"paintFirst\":\"fill\",\"globalCompositeOperation\":\"source-over\",\"skewX\":0,\"skewY\":0,\"inverted\":false,\"absolutePositioned\":false}}],\"background\":\"#ffffffff\"}","inputParameters":[{"name":"input","input":{"type":"string","value":{"type":"ref","content":{"source":"block-output","blockID":"100001","name":"input"},"rawMeta":{"type":1}}},"id":"m35JxW9eyesrwCMQeNw9K"}],"settingOnError":{"processType":1,"timeoutMs":60000,"retryTimes":0}},"nodeMeta":{"description":"自定义画板排版，支持引用添加文本和图片","icon":"https://lf3-static.bytednsdoc.com/obj/eden-cn/dvsmryvd_avi_dvsm/ljhwZthlaukjlkulzlp/icon/icon_DrawingBoard_v2.jpg","mainColor":"#FF4DC3","subTitle":"画板","title":"画板"},"outputs":[{"type":"string","assistType":2,"name":"data"},{"type":"string","name":"msg"}],"settingOnError":{"processType":1,"timeoutMs":60000,"retryTimes":0}},"_temp":{"bounds":{"x":320,"y":-13,"width":360,"height":112},"externalData":{"icon":"https://lf3-static.bytednsdoc.com/obj/eden-cn/dvsmryvd_avi_dvsm/ljhwZthlaukjlkulzlp/icon/icon_DrawingBoard_v2.jpg","description":"自定义画板排版，支持引用添加文本和图片","title":"画板","mainColor":"#FF4DC3"}}}],"edges":[]},"bounds":{"x":320,"y":-13,"width":360,"height":112}}
```

## 实战项目：创建「儿童识字卡片」工作流

**项目目标：**
 整合文本生成、图像生成、排版输出三个节点，制作一张AI识字卡。

**流程拆解：**
 1️⃣ 用户输入内容
 2️⃣ 大模型节点：生成内容的的趣味解释
 3️⃣ 图像节点：根据内容和趣味解释生成一张可爱插画
 4️⃣ 画板节点：把文字 + 图片组合成排版卡片
 5️⃣ Output节点：展示完整的卡片结果

**课堂实战：小组实战挑战赛 🏆**

> 每组选一个主题制作识字卡，展示输出成果。

# 实战演练

30分钟课堂练习案例：AI「内容创意生产线」工作流

## 练习场景

> 你是一个品牌内容运营，现在要围绕一个“热点关键词”，快速生成一套图文内容包，用于公众号或视频号推广。

## 目标

- 用户输入一个主题词（如“秋天”“环保”“创业”“咖啡”）
- 工作流自动完成：
 1️⃣ 提炼一个创意方向
 2️⃣ 生成一篇短文案（50\~100字）
 3️⃣ 自动拟标题
 4️⃣ 给出一组配图关键词，并生成配图
 5️⃣ 输出整合结果

最终输出要长这样：

> 【标题】
> 秋天，是离别的季节也是收获的开始 🍂
> 【文案】
> 风吹过桂花香，城市里的秋天，藏着不动声色的温柔。你打算去哪儿看第一场落叶？
> 【配图关键词】
> 秋天, 桂花, 阳光, 街景
> 【图片】
> 图片展示

# 总结

同学们，我们今天的 Coze 工作流探索之旅，到这里就暂告一个段落了。

我们首先认识了什么是Coze

之后我们进入了工作流，拆解了业务，也写了几个工作流。

通过这一节紧凑而充实的实战课程，我们共同迈出了从 Coze “使用者”到“创造者”的关键第一步。

我们不仅完成了从“0到1”的环境搭建，更重要的是，大家亲自动手，将抽象的“工作流”概念，通过一个个节点的连接，转化为能真实运行、创造价值的自动化应用。

从一张图片的生成，到一张识字卡片的制作，再到一篇公众号文案的自动撰写，这些实践让“想法落地”的能力真正被激活，也让我们体会到效率倍增的力量。

这节课的终极目标，并不仅是学会点击和拖拽，而是帮助大家建立一种高效的“自动化思维”。

当我们能像拆解乐高积木一样，将复杂任务拆分、重组，并清晰规划每一步“固定路线”时，我们就掌握了智能化时代最具竞争力的核心能力——**让AI替我们工作，而不是替代我们。**

回望这一路，从最初编写提示词，到今天搭建工作流，我们一步步完成了从“让AI听懂我”到“让AI替我干活”的跨越。

这正是生产力的进化：AI 不再只是一个答题器，而是可以被我们编排、被我们控制、被我们赋予角色的“数字合作者”。

当你能拆解任务、定义逻辑、连接节点的那一刻，你就已经不只是AI的使用者，而是真正的AI设计师。

今天的学习，只是一个起点。
下一节课，我们将进入更深层次的探索——**逻辑判断与数据操作**，让AI不再只是执行任务，而是能理解场景、做出选择。

请记住，每一次流畅的自动化背后，都始于一次勇敢的动手尝试。
各位已经成功启航，期待在下节课中，与大家一起构建更强大的AI生产力系统——

**把灵感变成系统，把创意变成生产力。**

谢谢大家。

大家之后遇到AI相关的问题，可以尽管提问，不用客气哈。

再者，我下周一开始，总结一下我平时用AI的一些习惯，以及每个AI擅长的点，试着写一个内容，我们抽一节晚上的时间，我们分享一下。作为我们西安学习中心，AI大航海的内容。

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI使用手册](01-AI使用手册.md)

---

<details>
<summary>原文配图上的文字（100 条，图片本身未随文提供）</summary>
- 「奔跑的毛球」 「一堂大会员」 「立即续费」
- 「input」 「文本生成」 「图像生成」 「output」 「info」 「msg」 「data」 「运行成功」
- 「爱抓老鼠超级萌的小动物」

**热点话题**

- 「内容创作」 「视频生成」 「写一篇关于人工智能的科普文章」 「科普、人工智能、科技、未来、发展、趋势、应用、前景、挑战、机遇、伦理、安全、风险、政策、法规、标准、伦理、安全、风险、政策、法规、标准」 「介绍人工智能发展历程」 「介绍、发展历程、人工智能、科技、发展、应用、前景、挑战、机遇、伦理、安全、风险、政策、法规、标准」

**工作流**

- 是Coze平台全自动内容创作流水线场景下的工作流流程，从开始节点输入初始内容后，依次经过内容分析与标题生成、摘要与正文扩写、配图提示词生成三个环节，每个环节都设置了对应的模型参数，配图提示词生成环节的输出会反馈用于调整环节内容，最终将生成的配图提示词输入图像生成环节，该环节调用了Searxng-4.0模型完成图像生成，最终得到输出内容后结束整个工作流，清晰呈现了将内容创作转化为配套图像的完整自动化
- 「AI视频自动生成器」 「脚本与分镜生成」 「获取镜头分镜数据」
- 「添加插件」
- 「任务开发」 「任务管理」 「工作流」
- 「input」 「output」 「返回变量」
- 「添加节点」
- 「大模型」 「工作流」 「Dy短视频解析」 「图片理解」 「意图识别」 「批处理」 「数据库」
- 「豆包 - 1.5 - Pro - 32k」 「input」 「output」
- 「大语言模型」 「输入数据」 「输入参数」 「输入变量」 「输入文件」 「输入插件」 「输入数据示例」 「输入参数示例」 「输入变量示例」 「输入文件示例」
- 「业务逻辑」
- 「代码节点（Code）」 「代码节点」 「import requests; r = requests.get('https://www.example.com')」
- 「大模型」 「工作流」 「已收藏插件」 「业务逻辑」 「输入&输出」 「数据库」 「WPUSH」 「链接读取」 「意图识别」
- 是Coze平台添加插件的界面。左侧有多个分类标签，当前选中“全部”。右侧显示了多个插件选项，如链接读取、图片理解、头条搜索、Kimi、Doubao图像生成等，每个选项下方有插件名称、描述、发布者、发布时间、评分、文件大小等信息。该图片
- 是Coze平台工作流的节点选择界面，界面内清晰划分了不同类型的工作流节点，可用于辅助创建工作流。其中红框重点标注了两类业务逻辑节点，左侧红框标注的是意图识别、批处理节点，右侧红框标注的是选择器、循环节点，这两类均属于工作流的核心节点类型，能够为工作流的逻辑处理、流程控制提供支持，符合Coze工作流节点使用的相关介绍内容
- 「选择器」 「...」 「条件分支」 「请选择」 「str.」 「+新增」
- 「循环设置」 「循环数组」 「中间变量」 「循环类型」 「使用数组循环」 「input」 「str.」 「output」
- 「开始节点（Start）」 「Start」
- 「知识库写入」 「知识库删除」 「知识库检索」

**使用提示词**

- 「阳光下的芒果，金黄色果肉闪烁着光泽」

**场景三智能代码审查与优化系统**

- 「Coze平台」

**什么是Coze**

- 「扣子，用Agent重塑生产力」 「高效完成之王」 「获取Agent」 「扣子空间」

**为什么选择Coze**

- Coze平台的插件分类。左侧为大模型、工作流、已收藏插件、WPUSH、链接读取、业务逻辑、代码、意图识别、批处理、输入输出、数据库、知识库数据、组件、会话管理等分类；右侧为插件分类，包括Dy短视频解析、图片理解、选择器、循环、变量聚合、新增数据、查询数据、知识库检索、变量赋值、长期记忆检索、面板、提示词优化、图像处理、图像生成、报图、画质提升、视频生成、视频抽帧、视频提取音频、文本处理、JSON序
- 「我的扣子」 「我的工作流」 「我的插件」 「我的代码」 「我的模型」 「我的数据」 「我的任务」
- 「知识库」 「我的扣子」 「小助手」 「添加扣子」 「小助手2」
- 「创建知识库」 「知识库创建方式」 「文本格式」 「表格格式」 「照片类型」 「本地文档」 「在线数据」 「Notion」 「公众号」 「完成创建」
- 「知识库」 「智能体」 「知识库设置」 「知识库管理」

**Coze的货币资源点**

- 「个人版」 「企业团队版」 「当前计划」
- Coze平台的扣子付费套餐。分为团队版和个人版。团队版178元/月，含150,000资源点/月（Lite版120,000资源点/月），可增购，支持模型每分钟请求5000、扩容、无限空间数量、100G知识空间、90天Trace上报量、100,000条单记忆库存储上限、1个支持声音复制、100人团队成员上限、2人团队成员人数上限、多人协同编辑、跨空间资源复制等功能。企业版4,980元/月，含3,000
- 「欢迎增购扣子资源包」

**官网地址**

- 「扣子，用Agent重塑生产力」 「和Agent一起做你的工作」 「免费版」 「AI写作」 「AI PPT」 「AI绘画」 「AI语音转文字」

**工作空间介绍**

- 「项目开发」 「资源库」 「技能评测」 「空间设置」 「文件夹」 「当前筛选状态下未找到相关结果」 「清空筛选」

**为什么要用工作流呢**

- Coze平台中拆解任务的几种方式，包括按时间顺序拆（会前/会中/会后）、按要素拆（市场/产品/运营）、按思考链路拆（问题→分析→结论）、按指定格式拆（PPT/表格/报告）。右侧有示例说明，如按时间顺序拆解可为会前准备资料、会中记录要点、会后整理总结。该图片
- 「场景：自动生成公司招聘文案」
- AI会议纪要助手的场景，系统接收会议录音或文字，自动生成会议纪要并分类。提示包括：原始数据是什么格式？需要做哪些清洗、分析、分类？输出格式是什么？该图片
- 「练习拆业务」
- 是生成行业研究简报的场景。用户输入行业名称，Bot自动生成简报，内容包含最新新闻摘要、行业趋势分析、投资风险提示。图片下方提示需拆任务，思考哪些部分需查实时信息、哪些可模型直接生成、是否需分段处理再汇总。该图片
- 「基础节点深度练习」 「我们练习练习」

**输入输出节点**

- 「str」 「input」
- 「input」 「String」 「Integer」 「Number」 「Boolean」 「Time」 「Object」 「Array」 「File」
- 「Input」 「Default value」 「Enter a default value for the input」 「Data type」 「String」 「Input name」 「Enter an input name」 「Input type」
- 「str.output」 「返回变量」
- 「返回变量」 「返回文本」 「输出变量」 「output」 「大模型-output」
- 「大模型」 「模型选择」 「提示词」 「输出格式」

**大模型节点配置AI的大脑**

- 「大模型」 「工作流」 「添加节点」 「第一步✅：新建大模型节点，并连线」
- 「input」 「output」 「豆包·1.5·Pro·32k」 「返回变量」
- 「大模型」 「工作流」 「添加节点」
- 「未定义」 「output」 「大模型节点配置」
- 「全部模型」 「豆包大模型」
- Coze平台中大模型节点的模型列表。包括豆包 - 工具调用、豆包 - 1.5 Pro - 深度思考等模型，涵盖文本模型、多模态模型等类型。各模型名称后标注了版本号，如Doubao - 1.5 - thinking - pro/m - 250415等。还列出了模型的类型、模型版本、模型类型及说明，如文本模型、多模态模型等。该图片
- 位于Coze工作流基础使用与入门文档里，对应大模型节点配置的第二步操作内容处。图片关联的操作是新建大模型节点后，选择合适的大模型，文档中提及默认的豆包·1.5·Pro·32k通常可满足日常工作需求，还附上了对应大模型服务的参考链接，图片核心用于辅助说明大模型节点配置里选择模型的相关操作步骤
- 「Doubao-1.5-pro-32k-250115」 「豆包·1.5」
- 「input」 「输入或引用参数值」 「第三步✅：配置入参」
- 「变量名」 「变量值」 「input」 「开始 - input」 「第三步✅：配置入参」
- 「岗位名称{{input}}」 「input」 「写提示词」
- 「配置输出节点」 「写提示词」 「选择输出结果格式」
- 「输出格式」 「JSON」 「变量名」 「output」 「支持续写」 「选择输出结果格式」
- 「写提示词」 「招聘文案」 「JSON」 「Markdown」
- 「配置输出节点」 「output」 「String」 「未定义」 「大模型」
- 「输入输出节点」 「配置入参」 「写提示词」 「选择输出结果格式」 「配置输出节点」 「点击编辑」
- 「大模型」 「提示词」 「Head」 「input」 「单节点调试」
- 「大模型」 「试运行」 「查看日志」 「input String」 「销售岗位，产品是电热水器」 「配置入参」
- 「试运行输入」 「销售岗位，产品是电热水器」 「运行结果」 「input: “销售岗位，产品是电热水器」 「技能调用」 「百科全书」
- 「电热水器销售猛将招募令！」 「写提示词」
- 「大模型」 「试运行」 「试运行输入」 「JSON模式」 「整体调试」
- 「试运行」 「查看日志」 「可用测试集」 「测试集」 「AI补全」 「销售岗位，产品是电热水器」 「将本次运行输入保存为测试集或手动创建」
- 「试运行」 「20s | 726 Tokens | 查看日志」 「可用测试集」 「测试集」 「JSON模式」 「AI补全」 「销售岗位，产品是电热水器」 「电热水器销售精英招募令」 「整体调试」
- 「销售岗位，产品是电热水器」 「单节点调试」
- 「电热水器销售精英招募令」

**图像生成**

- 「图像生成」 「画质提升」 「提示词优化」
- 「图片处理」 「图片生成」 「画面比例」 「画面质量」 「输入信息」 「提示词」 「Stable Diffusion」 「一幅山水画，背景是绿油油的山，前边有水，水上有舟，晴天」
- 「图像生成」 「模型设置」 「Seedream 4.0」 「Seedream 3.0」 「通用-Pro」
- 「图像生成」 「Doubao-Seedream-3.0」 「Doubao-Seedream-4.0」 「图片处理节点」
- 「图像生成」 「Doubao-Seedream-3.0」 「Doubao-Seedream-4.0」
- 「图像生成」 「Doubao-Seedream-3.0」 「Doubao-Seedream-4.0」 「图生图 seedream 4.0 - image2image」 「文生图 seedream 4.0 - text2image」
- 「生成质量」
- 「导入底图」 「调整尺寸」 「添加文字」 「调整字号、字体、颜色、间距」 「修改文字为引用入参」
- 「变量值」 「输入或引用参数值」 「提示词」 「正向提示词」
- 「图片处理节点」
- 「提示词」 「正向提示词」 「{{input}}」 「图片处理节点」 「图像生成」 「一幅山水画，背景是绿油油的山，前边有水，水上有舟，晴天」
- 「可用测试集」 「测试集」 「试运行输入」 「一幅山水画，背景是绿油油的山，前边有水，水上有舟，晴天」 「运行结果」 「图片预览」 「输出变量」 「https://s.coze.cn/t/6BYS4g-50pE/」

**画板**

- 「input」 「未配置输入」 「data」 「msg」 「output」
- 对应文档中Coze工作流里的画板节点相关操作环节，是画板节点配置流程的步骤示意图，内容围绕画板节点的使用展开，具体呈现的是该节点操作的相关指引，包含添加入画板节点后，配置其入参的相关步骤，涵盖导入底图、调整尺寸、添加并修改文字（含调整字号、字体、颜色、间距等样式，以及将文字修改为引用入参）、最后进行测试等操作环节，贴合上下文介绍的Coze画板节点入门使用的操作指引内容
- 「添加画板节点后，依次完成配置画板入参、导入底图、调整尺寸、添加文字并调整文字的字号字体等样式，最后修改文字为引用入参并测试」
- 「画板尺寸」 「画板背景」 「画板内容」 「背景色」 「背景图片」 「背景视频」 「内容图片」 「内容视频」
- 「单行文本」 「区块文本」
- 「Coze画板」 「Arial」
- 「舟已过万重山」 「思源黑体 > 常规体」
- 「轻舟已过万重山」 「引用 选择变量」 「input」
- 「试运行」 「查看日志」 「可用测试集」 「测试集」 「试运行输入」 「JSON模式」 「AI补全」 「String」 「今天天气很不错」 「将本次运行输入保存为测试集或手动创建」
- 「今天天气很不错」 「一幅山水画，背景是绿油油的山，前边有水，水上有舟，晴天」

**实战项目创建儿童识字卡片工作流**

- 「图像节点：根据内容和趣味解释生成一张可爱插画」
- 「实战演练」 「课堂实战：小组实战挑战赛🏆」

**目标**

- 「实战演练」

**总结**

- Coze工作流探索课程学习总结与实践回顾图。图中展示了课程学习内容、实践成果展示、未来展望与总结等板块。课程学习内容涵盖Coze平台基础认知、工作流基础认知、业务流程认知等。实践成果展示包括基础能力构建、业务流程实践、思想认知升级等方面。未来展望与总结部分提出核心流程总结、关键能力提升、未来学习方向等。该图是对课程学习与实践的全面总结
- 「让AI替我们工作，而不是替代我们」 「固定路线」 「数字合作者」
- 「把灵感变成系统，把创意变成生产力」

</details>
