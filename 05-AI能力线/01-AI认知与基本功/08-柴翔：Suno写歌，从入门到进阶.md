---
title: 柴翔：Suno写歌，从入门到进阶
node_token: M5PowYTyxiffTFkRL8RcBFf9nqh
source: https://www.feishu.cn/wiki/M5PowYTyxiffTFkRL8RcBFf9nqh
space: 一堂学习
obj_type: docx
synced: 2026-09-26 05:23
course_line: AI能力线
stage: AI认知与基本功
train: AI认知与基本功
form: 课程逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
# 柴翔：Suno写歌，从入门到进阶

## **Suno音乐创作**

AI生成音乐工具，海外有Suno、Udio，国内有字节的海绵音乐、天工AI音乐等。

个人体验看，Suno综合实力最强，几乎是遥遥领先。

尤其是最近更新了 4.5 版，提示词遵循能力大大提升。

可玩性、可用性猛的提升，非常酷。

官网：
https://suno.com/

如想体验，用我链接，互赚点积分。

> https://suno.com/invite/@wayofmusic1987

但是，想玩最牛模型，双币信用卡Stripe支付 ，或某宝买成品号（75元左右/月）。

## **Suno简单模式**

以网页版为例。

点击Create->Simple，输入音乐风格和主题提示词，点橙色的Create按钮。

就能生成一首还OK的歌。

是不是很简单？

## **Suno自定义模式**

如想相对精确控制一首歌的歌词、每小节风格/唱腔/器乐等。

就要用Custom模式，可理解为专家模式。

不要怕，其实也很简单。

**核心输入就三个：**

- 歌词
- 风格提示词
- 负向风格提示词

负向提示词，可以避免完全不想要的风格，选填。

比如喜欢重金属的，肯定要俗套的流行乐。

## **如何生成歌词？**

**不会写歌词怎么办？**

点击Lyrics模型下的“**Full Song**”，出现弹窗，输入主题和风格。

然后点击“Write Lyrics”，AI自动生成两个版本，选一个即可。

如不满意，可手动修改。或点“Edit，选中待修改段落，让AI继续改。

**虽方便，但生成歌词质量一般。**

也没用上很多Suno的一些隐藏控制技巧。

## **一段提示词玩转Suno**

理论上，任何一首歌，都是结构的。

类似于文章的起承转合。
一般不会上来就是高潮。

让AI给了一些常见音乐结构组成的解释。

> ### **Verse（主歌）**

主歌是讲述故事或表达主题的部分，歌词内容通常每段不同，推动歌曲情节发展。

> ### **Pre-Chorus（前副歌）**

位于主歌和副歌之间，起到过渡和增强期待感的作用，旋律和情绪通常逐渐上升。

> ### **Chorus（副歌）**

歌曲中最核心、最具记忆点的部分，通常包含主题和Hook（钩子），旋律和歌词多次重复，是整首歌的高潮。

> ### **Bridge（桥段）**

在歌曲后半段出现，提供音乐和情感上的转折，带来新鲜感，通常旋律和和声与主歌、副歌不同。

> ### **Outro（尾奏）**

歌曲的结尾部分，用于收尾和渐渐结束，帮助听众从情绪中平稳过渡出来。

> ### **其他常见结构名词**

• **Post-Chorus（后副歌）** ：副歌后的延伸部分，通常更具能量或舞曲感。
• **Drop** ：电子音乐中高潮爆发的部分，常在前副歌后出现。
• **Interlude（间奏）** ：歌曲中段的器乐过渡部分，给听众短暂休息。
• **Breakdown** ：乐器简化或重新编排的部分，常用于突出某种情绪或为高潮做铺垫。
• **Refrain（叠句）** ：在每个主歌结尾重复的短句，加强记忆点。
• **Spoken Word（说唱/对白）** ：用说话或朗诵的方式表达内容，增加表现力。
• **Ad-libs（即兴短句）** ：歌手即兴添加的背景声音或短句，增强歌曲表现力。

## **结构标记大全和用法**

Suno 4.5升级后，**语义理解和遵循能力大幅提升。**

能在歌词（Lyrics）中做段落标记，以控制歌曲的结构和情绪走向。

支持的结构标记如下：

此外，通过搜索官方Reddit社区，发现还有一些更细的控制。

比如

> 窗前明月光(明月光)

效果：括号内也会跟着唱出来，像叠唱和声效果。

再比如，Suno对中文理解不到位。

某字发音不对，也可以通过**小括号加上音标。**

> 春花秋月何时了**(liǎo)**

避免唱成le

[]括号也很有用，比如想指定某段用甜美女声唱，可以这么写：

> [Verse 1: Narrative] [Sweet Female Vocal]

## **太复杂了，学不会怎么办？**

没关系。

像我们普通人。

音乐风格也了解的不多。

所以，借助 AI ，我把**上面的技巧写到了一个提示词**中。

```Markdown
# 🎵 Suno AI 歌词创作大师plus

## 用户输入（支持多种形式）
你可以输入：
- 简单主题：如"爱情"、"友谊"、"太空探索"
- 详细描述：描述你想要的歌曲风格、情感和内容
- 文章/故事：分享一个故事或文章，AI将提取核心主题和情感创作歌曲
- 关键词列表：提供一系列关键词或概念

## 后台处理（AI自动完成）
AI将分析你的输入，自动为你：
- 提取核心主题和情感
- 选择最佳音乐风格
- 确定适合的语言和结构
- 设计匹配的人声类型和特殊元素

## 输出内容

### 1. 完整歌词
创作一首专业级歌词，注重原创性和艺术性，避免流行音乐的陈词滥调，包含以下结构和技巧：

#### A. 商业级Hook设计（核心竞争力）
- **[Hook]**: 创作极具记忆点的核心短句，这是歌曲的灵魂和商业成功的关键
- Hook应在3-7秒内抓住听众，通常8-16个音节最为理想
- 使用"音乐钩子"原则：简单、重复、独特、情感共鸣
- 确保Hook有强烈的节奏感、押韵效果和情感冲击力
- 考虑"回音效应"：听众听完后会不自觉地在脑中重复的短句
- 可使用对比、悖论、问题或宣言等技巧增强吸引力
- 标记为[Hook: Catchy]或[Hook: Anthemic]等增强效果
- 确保Hook与歌曲主题紧密相连，成为歌曲的标志性部分

#### B. 专业歌曲结构设计
##### 经典结构模板
- **流行标准结构**: Intro(8秒) → Verse 1(16秒) → Pre-Chorus(8秒) → Chorus(16秒) → Verse 2(16秒) → Pre-Chorus(8秒) → Chorus(16秒) → Bridge(16秒) → Chorus(16秒) → Outro(8秒)
- **简化结构**: Intro → Verse → Chorus → Verse → Chorus → Bridge → Chorus → Outro
- **扩展结构**: Intro → Verse 1 → Pre-Chorus → Chorus → Post-Chorus → Verse 2 → Pre-Chorus → Chorus → Post-Chorus → Bridge → Breakdown → Chorus → Outro
- **现代流行结构**: Intro → Chorus(前置) → Verse → Chorus → Post-Chorus → Verse → Chorus → Post-Chorus → Bridge → Chorus → Outro

##### 特殊结构元素
- **Drop**: 电子音乐中的高潮部分，通常在Pre-Chorus后
- **Interlude**: 歌曲中段的器乐过渡部分
- **Breakdown**: 乐器简化或重新编排的部分
- **Post-Chorus**: 副歌后的延伸，通常更具能量或舞曲感
- **Refrain**: 在每个Verse结尾重复的短句
- **Spoken Word**: 说唱或对白部分
- **Ad-libs**: 即兴添加的背景声音或短句

#### C. Suno AI专业标记系统
##### 基础结构标记
- [Intro]: 歌曲开头，设定氛围和基调
- [Verse 1]/[Verse 2]: 主歌部分，推进故事情节
- [Pre-Chorus]: 副歌前的过渡，增强期待感
- [Chorus]: 核心副歌，包含歌曲主题和最具记忆点的部分
- [Post-Chorus]: 副歌后的延伸，通常更具能量或舞曲感
- [Bridge]: 提供音乐和叙事转折
- [Breakdown]: 乐器简化或重新编排的部分
- [Outro]: 歌曲结束部分

##### 高级表现标记
- **人声标记**: [Male Vocals], [Female Vocals], [Whispers], [Shouting], [Duet], [Harmonies], [Falsetto], [Growl], [Rap]
- **情感标记**: [Calm], [Energetic], [Emotional], [Aggressive], [Intense], [Melancholic], [Euphoric], [Nostalgic], [Dreamy]
- **音效标记**: [Applause], [Rain], [City Sounds], [Heartbeat], [Static], [Phone], [Crowd], [Nature], [Traffic]
- **乐器标记**: [Heavy drums], [Piano solo], [Distorted Guitars], [Synth Lead], [Bass Drop], [Strings], [Brass], [Acoustic], [808]
- **段落修饰**: [Verse: Storytelling], [Chorus: Anthemic], [Bridge: Atmospheric], [Intro: Mysterious], [Outro: Fading]

##### 组合标记策略
- 使用1-2个主要标记+1个修饰标记，如[Chorus: Energetic][Male Vocals]
- 情感渐变标记，如[Verse: Calm to Intense]
- 对比标记，如[Verse: Whispered][Chorus: Shouted]
- 乐器焦点标记，如[Bridge: Piano Focus]

#### D. 声音处理与表现技巧
- **和声/背景声**: 使用圆括号()标注，如(Yeah!), (Echoes), (Whispers), (Call: ... Response: ...)
- **声音延长**: 使用连字符延长音节，如lo-o-ong, cra-a-azy, he-e-ey
- **强调处理**: 使用大写字母强调关键词，如STOP, NEVER, NOW, FEEL
- **节奏控制**: 使用标点符号(!?...)和换行控制演唱节奏和停顿
- **声音效果**: 指示特殊声音效果，如(Vocoder effect), (Auto-tune), (Distortion), (Reverb)
- **情感指导**: 添加简短的情感指导，如(with passion), (whispered), (screamed), (breaking voice)
- **动态变化**: 指示音量或强度变化，如(building), (fading), (suddenly quiet)
- **空间感**: 指示声音的空间位置，如(distant), (close up), (surrounding)

#### E. 语言特定优化与多语言策略
- **英文歌词优化**:
  * 注重音节平衡、强弱格律和自然押韵
  * 使用短促有力的单音节词增强节奏感
  * 避免过于复杂的词汇和句式
  * 利用英文特有的同音词和双关语
  * 考虑辅音和元音的分布，确保流畅演唱

- **中文歌词优化**:
  * 注重平仄变化、字数均衡和尾字押韵
  * 考虑汉字声调对旋律的影响
  * 避免生僻字和难以演唱的连续辅音
  * 利用成语和谐音创造独特表达
  * 注意避免歧义，确保意思明确

- **多语言策略**:
  * 以一种语言为主体，另一种语言仅用于特定段落
  * 避免每行交替使用不同语言
  * 可在特定结构转换处(如Verse到Chorus)切换语言
  * 确保不同语言部分在意义上连贯，而非简单翻译
  * 考虑不同语言的文化背景和表达习惯

#### F. 主题提取与故事转化（针对长文本输入）
- **核心主题识别**: 从长文本中提取最核心的主题和情感
- **情感基调分析**: 识别文本的主要情感基调和情感变化
- **关键场景选择**: 选择最具戏剧性或情感冲击力的场景作为歌词素材
- **角色声音提取**: 从文本中提取独特的角色声音或视角
- **叙事简化**: 将复杂叙事简化为适合歌曲的简洁形式
- **意象转化**: 将文本中的描述性语言转化为歌词中的意象和比喻
- **情感升华**: 提炼文本中的情感主题并在歌词中升华
- **结构重组**: 根据歌曲结构需求重新组织文本内容

#### G. 情感工程与听众心理学
- **情感弧线设计**: 设计完整的情感发展路径，从开始到结束有明确的情感变化曲线
- **张力与释放**: 创造音乐和歌词的张力，然后在关键时刻释放
- **共鸣点创造**: 设计能引起听众共鸣的情感触发点
- **情感锚定**: 将特定词汇或短语与强烈情感关联
- **高潮预期**: 通过歌词暗示和铺垫，创造对高潮的期待
- **情感对比**: 使用情感对比增强表现力，如从脆弱到强大
- **普遍性与特殊性平衡**: 结合普遍情感与具体细节，既有共鸣又有独特性
- **记忆触发**: 使用能唤起集体记忆或个人经历的意象

#### H. 非主流歌词创作技巧
- **开头吸引力**: 使用非常规开场，避免陈词滥调的开场白
- **高潮独特性**: 创造不同于流行音乐的副歌，追求艺术性而非简单重复
- **桥段实验性**: 在Bridge部分尝试更大胆的音乐和歌词实验
- **结尾留白**: 考虑开放式或富有哲理性的结尾，而非简单的情感总结
- **押韵创新**: 尝试内部押韵、半押韵或不规则押韵，增加艺术深度
- **节奏变化**: 在不同段落使用不同的节奏模式，打破常规
- **意象独特性**: 创造新鲜、独特的意象，避免常见比喻
- **叙事角度**: 尝试不同的叙事视角，如第三人称或多视角
- **时间跳跃**: 在歌词中使用非线性时间，如闪回或预视
- **概念性**: 围绕一个中心概念构建整首歌，追求思想深度

#### I. Suno AI平台优化策略
- **器乐描述精确化**: 在[Instrumental]部分添加详细且具体的氛围和乐器描述，如(电子鼓点渐入，带有轻微失真的合成器创造出梦幻氛围)
- **标记平衡控制**: 每个段落使用1-2个最相关的标记，避免过度标记导致AI混淆
- **冒号使用精简化**: 使用冒号进一步细化段落特性，如[Verse: Storytelling]，但保持简洁明了
- **Hook标记突出化**: 突出使用[Hook]标记最具记忆点的短句，确保AI优先处理这部分
- **换行节奏控制**: 精心设计换行影响AI对演唱节奏的理解，短句独立成行增强停顿感
- **By Line模式优化**: 适当使用短行和精确标点，优化Suno的By Line模式效果
- **情感渐变引导**: 使用递进的情感标记，如从[Calm]到[Intense]，引导AI创建情感弧线
- **声音效果具体化**: 使用具体的声音效果描述，如(echo fading)而非简单的(echo)
- **乐器组合标记**: 使用组合标记描述乐器配置，如[Synth and Piano]
- **空间感标记**: 使用空间感标记创造声音环境，如[Verse: Intimate][Chorus: Expansive]
- intro和outro：下面不要加任何文本，否则suno会误认为是歌词。

#### J. 专业音乐创作核心要素
- **主题一致性**: 确保所有歌词围绕核心主题展开，避免主题漂移
- **意象连贯性**: 创建连贯的意象系统，使用相关的比喻和象征贯穿全曲
- **音节平衡**: 确保每行歌词的音节数量平衡，适合演唱
- **对比原则**: 在不同段落间创造对比，如强弱、快慢、密集稀疏的变化
- **高潮设计**: 精心设计歌曲高潮部分，通常在副歌或桥段，情感和能量达到顶点
- **回环结构**: 考虑在结尾呼应开头，创造完整感
- **黄金比例**: 考虑在歌曲约61.8%处放置最重要的转折或高潮
- **节奏变化**: 在不同段落使用不同的节奏模式增加变化
- **声音层次**: 设计不同的声音层次，如主唱、和声、背景声等
- **空间感变化**: 从亲密到宏大的空间感变化增强戏剧性

#### K. 质量保证与专业检查清单
- 避免陈词滥调和空洞表达
- 使用具体场景和细节代替抽象概念
- 确保音节平衡与押韵优化
- 保证歌词"可唱性"和情感连贯性
- 尾字押韵，增强记忆点和听感
- 确保歌词与主题、情感和风格一致
- 创造独特意象和比喻，避免常见套路
- 检查是否有难以演唱的词组或拗口部分
- 验证歌词整体流动性和节奏感
- 确认Hook部分是否足够强大和记忆点
- 检查情感弧线是否清晰且有效
- 验证各段落之间的过渡是否自然
- 确保歌词适合目标受众和商业目标

### 2. Style Description（风格描述）
使用以下格式提供全面的风格关键词，包括并局限于：
- 音乐风格（如alternative-rock, indie-folk, synthwave）
- 人声类型（如male-vocals, female-vocals, harmonies）
- 乐器元素（如acoustic-guitar, synth-bass, sax, violin）
- 速度感受（如fast-tempo, mid-tempo, slow-groove）
- 情感氛围（如dreamy, energetic, melancholic, nostalgic）

输出示例：alternative-rock, male-vocals,acoustic-guitar,fast-tempo,dreamy

### 3. Exclude Styles（排除风格）
使用以下格式列出不适合的风格元素，包括并局限于：
- 不想要的音乐风格（如mainstream-pop, r&b, trap）
- 不想要的乐器元素（如auto-tune, heavy-bass）
- 不想要的情感氛围（如overly-happy, cheesy）

输出示例：mainstream-pop, auto-tune,overly-happy

### 4. 创意歌名建议
提供三个有创意且符合主题的歌名选择，每个都简洁有力并能反映歌曲核心。

### 5. 语言偏好
优先创作单一语言（中文或英文）的歌词，避免每行交替使用不同语言。如果使用双语，应以一种语言为主体，另一种语言仅作为点缀或用于特定段落（如副歌或桥段）。

请直接以Markdown代码块格式输出完整歌词，不需要额外解释。

用户输入内容如下:
{{content}}

```

## 提示词更新

```Plain Text
Role: Suno AI Music Prompt Engineer
Profile
你是一位精通音乐理论、流派分类以及 Suno AI 算法生成机制的提示词专家。你的任务是根据用户提供的【歌曲名称】、【歌词】或【歌曲描述】，反推出能够精准还原该歌曲风格的 Suno 提示词（Prompts）和元标签结构（Metatags）。
Knowledge Base
Suno 的生成机制严重依赖于具体的英文标签（Tags）。请遵循以下规则：
Tags 优先级：[流派 Genre] > [子流派 Sub-genre] > [氛围 Vibe] > [乐器 Instruments] > [人声 Vocals] > [制作质量 Production]。
魔法词汇：适当加入如 High Fidelity, Studio Recording, Masterpiece 等提升音质的词。
结构指令：Suno 需要通过 [Verse], [Chorus], [Bridge], [Drop] 等元标签来控制歌曲结构。
Workflow
当用户提供信息后，请按以下步骤思考并输出：
Step 1: 音乐风格分析 (Mental Chain)
分析该歌曲的主要流派（如 Pop, Rock, Electronic）。
细化子流派（如 Dream Pop, Hard Rock, Liquid DnB）。
确定情绪（如 Melancholic, Uplifting, Aggressive）。
识别核心乐器（如 Synth, Electric Guitar, Piano, 808 Bass）。
确定人声特征（如 Female, Male, Gritty, Ethereal, Choir）。
Step 2: 生成 Style Prompt
将分析结果转化为 Suno 专用的英文标签串，用逗号分隔。
限制：保持在 120 个字符以内，确保核心词在前。
Step 3: 结构与元标签建议
如果用户提供了歌词，请在歌词中插入正确的结构标签（如 [Intro], [Chorus]）。
如果用户未提供歌词，请给出一个典型的结构模板。
Output Format (请严格按照以下格式回复)
🎶 Suno Style Prompt (直接复制)
[这里填写生成的英文标签字符串]
📝 结构建议 (Metatags)
推荐结构：[Intro] -> [Verse] -> [Chorus] -> ...
关键技巧：(简要说明，例如：在副歌前加入 [Build up] 以增强爆发力)
💡 风格解析
流派：(解释选择该流派的原因)
人声：(解释人声设定的细节)
Initialization
准备好了。请告诉我你想反推的 歌曲名、音频描述 或 粘贴歌词。
```

模型推荐 [**Gemini 2.5 Pro** ](https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%221rni_RR7sJ--DF_c00nfB5wLRGqu-1ACV%22%5D,%22action%22:%22open%22,%22userId%22:%22106718122158833913828%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing)

另外发现，如果是**中文歌，中文大模型（豆包、文心）写歌词更押韵，但【音乐标记】做的不够好。**

推荐模型组合使用，加上人工微调，完成你的歌词。

大概效果如下：

```YAML
### 1. 完整歌词

[Intro: Mysterious]
(Synth pad drones, sound of wind, a single piano note repeats like a sonar ping)
[Heartbeat]

[Verse 1: Storytelling]
[Male Vocals] [Calm]
白板上画满了 攀登的路径
每一个节点 都是一个假设的证明
氧气瓶满载着 A轮的憧憬
我们是探路者 也是远征军

[Pre-Chorus: Building]
[Male Vocals] [Harmonies]
冰川裂缝 像市场的陷阱 (步步为营)
数据流是唯一的 风向引
稀薄空气里 调整呼吸
每一次迭代都向着 黎-明

[Chorus: Anthemic]
[Male Vocals] [Distorted Guitars] [Energetic]
这是科学的攀登 创业的雪峰
用逻辑和代码 凿开绝境的峥嵘
[Hook: Anthemic]
**心跳是代码 敲响每一次搏动 (每一次搏动)**
我们在零和一的 陡峭中冲锋
仰望着星空 NEVER a-lone

[Verse 2: Intense]
[Male Vocals] [Aggressive]
暴风雪来临 像融资的寒冬
竞争者足迹 覆盖了来时的路程 (无影无踪)
篝火旁争论着 模型的最终
是坚持路径 还是彻底变通?

[Pre-Chorus: Building]
[Male Vocals] [Harmonies]
岩壁上寻找 关键的支点 (绝不放弃)
验证失败让信念 更-坚-定
疲惫眼神里 燃烧着憧憬
每一次试错都为了 最-终-赢

[Chorus: Anthemic]
[Male Vocals] [Heavy drums] [Euphoric]
这是科学的攀登 创业的雪峰
用逻辑和代码 凿开绝境的峥嵘
[Hook: Anthemic]
**心跳是代码 敲响每一次搏动 (每一次搏动)**
我们在零和一的 陡峭中冲锋
仰望着星空 NEVER a-lone

[Bridge: Atmospheric]
[Spoken Word] [Calm to Intense]
(Music pulls back, leaving a shimmering synth pad and a steady heartbeat)
"日志，第三百六十五天。
海拔八千米，缺氧区。
所有理论都已失效...
但...等一下...
看那云层之上...数据...数据汇合成了一条全新的路径...
就是那里！"
(Beat drops back in, harder and faster)

[Chorus: Shouted]
[Male Vocals] [Duet] [Euphoric]
这是我们的攀登 我们的雪峰!
用生命和热爱 凿开绝境的峥嵘!
[Hook: Anthemic]
**心跳是代码 回应着苍穹的脉动 (苍穹的脉动)!**
我们在世界之巅 看梦想恢弘!
去拥抱星空 WE ARE NOT ALONE!

[Outro]
(Guitar solo, triumphant and emotional, fades into the sound of wind on a summit, then silence)

### 2. Style Description
alternative-rock, indie-rock, male-vocals, anthemic, mid-tempo, uplifting, synth-lead, cinematic

### 3. Exclude Styles
mainstream-pop, hip-hop, r&b, ballad, slow-tempo, relaxing, acoustic

### 4. 创意歌名建议
1.  《假设的山峰》
2.  《迭代攀登》
3.  《零和一的冰川》

### 5. 语言偏好
歌词已使用单一语言（中文）创作，并融入了少量英文短语以增强情感爆发力，确保了整体风格的统一和现代感。
```

与此同时，还会生成正向和负向风格提示词、推荐歌名。

**只需要复制粘贴到Suno中即可。**

## **高级技巧：模仿生成**

发现一些专业搞音乐的网友。

1用Suno找创作灵感。

2 通过录音哼唱，生成纯音乐歌曲。

**如何做？**

点创作界面中的**Audio**

**可录音**（可以规避一些版权审查），也可上传一段音乐

支持最多120s音频，以此为**基础生成翻版或延长。**

**注意：** 上传或录制的音频，会做版权检测，测了一些大牌乐队歌曲，都不让用...

## **高级技巧：纯音乐生成歌词**

先用Suno生成纯音乐，挑选最喜欢的一首，下载为MP3。

打开谷歌AIStudio，上传后让它基于歌曲写Lyrics歌词。

> https://aistudio.google.com/

示例如下：

**谷歌多模态AI威武**，不少音乐人喜欢这**个Use Case。**

## **社交**

感谢你看到这里，我是柴翔，一名正在积极探索 AI 赋能的演说教练。

这是我的一堂介绍和名片

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI使用手册](01-AI使用手册.md)
> 📂 子页（1）：[Suno AI 歌词创作专家](01-Suno%20AI%20歌词创作专家.md)
