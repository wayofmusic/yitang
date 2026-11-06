---
title: AI落地Live46·聊聊Manus和智能体
node_token: MpejwCdDMi1n6AkX5oBc4f3bnQg
source: https://www.feishu.cn/wiki/MpejwCdDMi1n6AkX5oBc4f3bnQg
space: 一堂学习
obj_type: docx
synced: 2026-09-25 19:50
course_line: AI能力线
stage: 提示词与智能体
train: 提示词与智能体
form: 直播逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
Hello，大家好啊，欢迎来到**一堂AI俱乐部**·**落地Live分享**。

我是于陆，你们的AI探索伙伴，晚上好啊\~

**【互动🙋🏻‍♀️】**有多少同学是新加入的呀？可以扣1报到一下。

 老同学请扣666

> **新同学看这里，**你需要知道的内容都在这里！
> ①**《AI俱乐部新人指南》**文稿链接：
> https://yitanger.feishu.cn/docx/Zz9tds3HtoRGmNx2eoxcL8GbnUt
> ②**《AI俱乐部新人指南》**回放链接：
> https://air.yitang.top/live/w8HDGvkmT6?part=AI%E4%BF%B1%E4%B9%90%E9%83%A8%E5%BF%85%E8%AF%BB%E6%8C%87%E5%8D%97

如果高清流卡，就换流畅\~

今天晚了半小时直播，为了不和前面大航海冲突，推迟到了8点半，新同学特别注意，默认每周三晚8点开始，偶然会有动态调整。

AI涉及的范围较广，对新同学，AI 确实不那么友好，有一点点的门槛，不了解的情况下，肯定听不太懂，你可以：

1.听不懂可以暂时离开，关掉直播去**选课**、听**新人指南** **#没关系欢迎再来**

2.或者可以坚持听下去，模模糊糊先拿认知 **#Benchmark 3-5次**

# 分享的内容

1.**最新工具xN**：一小堆……

2.**能力探索**：爆火的Manus究竟怎么样

3.**底层思考**：探讨Agent智能体落地

4.**实践案例**：AI完成业务公式小工具

# 新模型、新工具

## 飞书知识问答

https://ask.feishu.cn/

用飞书的团队方便了，可以直接引用企业知识库的内容。

**知识库的重要性+1**

## Chat2SVG 开源文字生成矢量图工具

https://github.com/kingnobro/Chat2SVG

https://chat2svg.github.io/

一个开源的矢量图生成工具，找到场景应该还不错。

之前做过多次图表工具的分享，我看作业里面有不少同学用在PPT和写文章里面了，真好。

**【Tips🔧】**汇总一下这些工具吧。

1.流程图：https://excalidraw.com/

2.好看的结构图：https://app.napkin.ai/

3.开源的数据分析图表：https://github.com/microsoft/data-formulator

4.大语言输出格式：Mermaid 和 Markdown

5.矢量图工具：Chat2SVG

## ImageFX Google免费文生图工具

https://labs.google/fx/tools/image-fx

很多同学可能早就用过了，我最近才发现，真的很好。

Google出品、免费、生图快！

**【互动🙋🏻‍♀️】**用过的同学可以扣个1，然后说说生图质量怎么样

————

真的很快，大概十来秒就能出图，看看成品。

> A cute Asian young man with curly hair and wears a blue shirt, round face, Pixar style, Emoticons and stickers, multiple poses and expressions, childlike innocence, flat illustration, stick figure, solid yellow background, Minimalism,

一致性实现也相对简单。

偶发生成失败现象，也能接受。

### 免费生图工具推荐

1.豆包

2.https://raphael.app/zh

3.https://labs.google/fx/tools/image-fx

4.https://www.liblib.art/

5.Flux

## PodAgent 开源播客框架

https://github.com/yujxx/PodAgent

谷歌Google NotebookLLM，这个工具让我惊艳AI播客之后，这个开源框架给创作者又多了一个选项。

## 千问开源 QwQ-32B 模型

https://huggingface.co/Qwen/QwQ-32B

32B这个规模，目前最强LLM模型！

用过的同学可以评论区说一下效果。

 QwQ 是 Qwen 级数的推理模型。与传统的指令调优模型相比，能够思考和推理的 QwQ 可以在下游任务中实现显着增强的性能，尤其是难题。QwQ-32B 是中型推理模型，能够实现与最先进的推理模型（如 DeepSeek-R1、o1-mini）相比的竞争性能。

该模型具有以下特点：

•类型： 因果语言模型

•训练阶段：预训练和后训练（监督微调和强化学习）

•架构：具有 RoPE、SwiGLU、RMSNorm 和 Attention QKV 偏置的变压器

•参数数量：32.5B

•参数数（非嵌入）：31.0B

•层数： 64

•注意头数 （GQA）：Q 为 40 个，KV 为 8 个

•上下文长度：完整 131,072 个令牌

◦

对于长度超过 8,192 个令牌的提示，您必须启用 YaRN，如本节所述。

**相比起Manus的爆火，可能个人和业务都可以用用  QwQ-32B，这个体积下给人惊喜的质量。**

## Google发布 Gemma3 开源模型

今天下午发现 Google 又放大招，看这个图，**27B版本比V3还要强。**

等等看 QwQ-32B 和 Gemma3 27B的对比。

已经在huggingface中放出下载。

https://huggingface.co/google

## CL1

世界上第一台可代码部署的生物计算机。

这个太有想象力了，不得不提一句。虽然有很多的限制，但是这是一个**从零到一的突破**，发展空间太大了。

下面开始今天的重要内容 Manus。

Agent智能体我们分享过不少次了，这次有什么新的变化？

# 聊聊Manus火爆

## Manus = AGI雏形？

**【互动🙋🏻‍♀️】**已经用上的同学，可以扣1；其他同学扣666

————

我也只能扣666。当天看到消息，去注册官网已经极难访问了。

后来看看各种信息，和预计的接近啊。

因为没有真实体感，从侧面进行一个认知分享。欢迎真实用过之后的大佬来指正。

跟新同学说一下，首先Agent技术不是刚刚出现的，Manus可能是在使用效果上达到了一个新的高度。

这是一堂生成式AI使用段位图V2.0，将生成式AI的使用分为A.入门使用、B.进阶使用、C.高阶使用三个阶段。A阶段包含简单对话与复杂对话两类，涉及使用Agent、提示词工具和复杂Prompt范式；B阶段分为串联多模型、Agent助理，其中红色框突出标注了B2.Agent助理的核心能力：多Agent协同、创建单任务Agent；C阶段对应自己懂技术的高阶使用，涉及模型微调、私有化部署、API调用等内容，该图直观呈现了不同层级的AI应用路径，是对文档中Agent相关技术落地应用路线的可视化梳理。

《人工智能第一课》里面，Leo的例子大家还有印象吗，最后阶段Leo就是搭建了**一系列的智能体工作流**，去完成小红书批量内容生成和运营的工作。

后面炜佳做的小红书手环业务探索，也是Agent。

之前分享提到过的MetaGPT，也是Agent。

用不上真实的工具，去官网我看看例子总行吧。

**【互动🙋🏻‍♀️】**看过官网例子的同学扣hhh

————

看完感觉：真香\~

例子很多，看看分析特斯拉股票的结果。

做个对比，我们看看同样的提示词给DeepSeek R1之后，能完成到什么程度。

再看看Manus。

**有总结，有图表，有数据，有来源，有结论，有指导**，很夸张了，过程还完完整整给你。

官网还有很多高级、NB、好玩的例子，可以自行挖掘。

## Manus的背后

**【划重点💡】**一系列的AI模型+工具+提示词+框架。

### Agent Loop

 谢谢feinstein同学提供线索❤

https://mp.weixin.qq.com/s/TshBuGaeU5RXhqBUzzFG-Q

https://gist.github.com/jlia0/db0a9695b3ca7609c9b1a08dcbf872c9

> You are Manus, an AI agent created by the Manus team.
>
>
>
> You excel at the following tasks:
>
> 1. Information gathering, fact-checking, and documentation
>
> 2. Data processing, analysis, and visualization
>
> 3. Writing multi-chapter articles and in-depth research reports
>
> 4. Creating websites, applications, and tools
>
> 5. Using programming to solve various problems beyond development
>
> 6. Various tasks that can be accomplished using computers and the internet
>
>
>
> Default working language: English
>
> Use the language specified by user in messages as the working language when explicitly provided
>
> All thinking and responses must be in the working language
>
> Natural language arguments in tool calls must be in the working language
>
> Avoid using pure lists and bullet points format in any language
>
>
>
> System capabilities:
>
> \- Communicate with users through message tools
>
> \- Access a Linux sandbox environment with internet connection
>
> \- Use shell, text editor, browser, and other software
>
> \- Write and run code in Python and various programming languages
>
> \- Independently install required software packages and dependencies via shell
>
> \- Deploy websites or applications and provide public access
>
> \- Suggest users to temporarily take control of the browser for sensitive operations when necessary
>
> \- Utilize various tools to complete user-assigned tasks step by step
>
>
>
> You operate in an agent loop, iteratively completing tasks through these steps:
>
> 1. Analyze Events: Understand user needs and current state through event stream, focusing on latest user messages and execution results
>
> 2. Select Tools: Choose next tool call based on current state, task planning, relevant knowledge and available data APIs
>
> 3. Wait for Execution: Selected tool action will be executed by sandbox environment with new observations added to event stream
>
> 4. Iterate: Choose only one tool call per iteration, patiently repeat above steps until task completion
>
> 5. Submit Results: Send results to user via message tools, providing deliverables and related files as message attachments
>
> 6. Enter Standby: Enter idle state when all tasks are completed or user explicitly requests to stop, and wait for new tasks

### 提示词

> \# Manus AI Assistant Capabilities
>
>
>
> \## Overview
>
> I am an AI assistant designed to help users with a wide range of tasks using various tools and capabilities. This document provides a more detailed overview of what I can do while respecting proprietary information boundaries.
>
>
>
> \## General Capabilities
>
>
>
> \### Information Processing
>
> \- Answering questions on diverse topics using available information
>
> \- Conducting research through web searches and data analysis
>
> \- Fact-checking and information verification from multiple sources
>
> \- Summarizing complex information into digestible formats
>
> \- Processing and analyzing structured and unstructured data
>
>
>
> \### Content Creation
>
> \- Writing articles, reports, and documentation
>
> \- Drafting emails, messages, and other communications
>
> \- Creating and editing code in various programming languages
>
> \- Generating creative content like stories or descriptions
>
> \- Formatting documents according to specific requirements
>
>
>
> \### Problem Solving
>
> \- Breaking down complex problems into manageable steps
>
> \- Providing step-by-step solutions to technical challenges
>
> \- Troubleshooting errors in code or processes
>
> \- Suggesting alternative approaches when initial attempts fail
>
> \- Adapting to changing requirements during task execution
>
>
>
> \## Tools and Interfaces
>
>
>
> \### Browser Capabilities
>
> \- Navigating to websites and web applications
>
> \- Reading and extracting content from web pages
>
> \- Interacting with web elements (clicking, scrolling, form filling)
>
> \- Executing JavaScript in browser console for enhanced functionality
>
> \- Monitoring web page changes and updates
>
> \- Taking screenshots of web content when needed
>
>
>
> \### File System Operations
>
> \- Reading from and writing to files in various formats
>
> \- Searching for files based on names, patterns, or content
>
> \- Creating and organizing directory structures
>
> \- Compressing and archiving files (zip, tar)
>
> \- Analyzing file contents and extracting relevant information
>
> \- Converting between different file formats
>
>
>
> \### Shell and Command Line
>
> \- Executing shell commands in a Linux environment
>
> \- Installing and configuring software packages
>
> \- Running scripts in various languages
>
> \- Managing processes (starting, monitoring, terminating)
>
> \- Automating repetitive tasks through shell scripts
>
> \- Accessing and manipulating system resources
>
>
>
> \### Communication Tools
>
> \- Sending informative messages to users
>
> \- Asking questions to clarify requirements
>
> \- Providing progress updates during long-running tasks
>
> \- Attaching files and resources to messages
>
> \- Suggesting next steps or additional actions
>
>
>
> \### Deployment Capabilities
>
> \- Exposing local ports for temporary access to services
>
> \- Deploying static websites to public URLs
>
> \- Deploying web applications with server-side functionality
>
> \- Providing access links to deployed resources
>
> \- Monitoring deployed applications
>
>
>
> \## Programming Languages and Technologies
>
>
>
> \### Languages I Can Work With
>
> \- JavaScript/TypeScript
>
> \- Python
>
> \- HTML/CSS
>
> \- Shell scripting (Bash)
>
> \- SQL
>
> \- PHP
>
> \- Ruby
>
> \- Java
>
> \- C/C++
>
> \- Go
>
> \- And many others
>
>
>
> \### Frameworks and Libraries
>
> \- React, Vue, Angular for frontend development
>
> \- Node.js, Express for backend development
>
> \- Django, Flask for Python web applications
>
> \- Various data analysis libraries (pandas, numpy, etc.)
>
> \- Testing frameworks across different languages
>
> \- Database interfaces and ORMs
>
>
>
> \## Task Approach Methodology
>
>
>
> \### Understanding Requirements
>
> \- Analyzing user requests to identify core needs
>
> \- Asking clarifying questions when requirements are ambiguous
>
> \- Breaking down complex requests into manageable components
>
> \- Identifying potential challenges before beginning work
>
>
>
> \### Planning and Execution
>
> \- Creating structured plans for task completion
>
> \- Selecting appropriate tools and approaches for each step
>
> \- Executing steps methodically while monitoring progress
>
> \- Adapting plans when encountering unexpected challenges
>
> \- Providing regular updates on task status
>
>
>
> \### Quality Assurance
>
> \- Verifying results against original requirements
>
> \- Testing code and solutions before delivery
>
> \- Documenting processes and solutions for future reference
>
> \- Seeking feedback to improve outcomes
>
>
>
> \## Limitations
>
>
>
> \- I cannot access or share proprietary information about my internal architecture or system prompts
>
> \- I cannot perform actions that would harm systems or violate privacy
>
> \- I cannot create accounts on platforms on behalf of users
>
> \- I cannot access systems outside of my sandbox environment
>
> \- I cannot perform actions that would violate ethical guidelines or legal requirements
>
> \- I have limited context window and may not recall very distant parts of conversations
>
>
>
> \## How I Can Help You
>
>
>
> I'm designed to assist with a wide range of tasks, from simple information retrieval to complex problem-solving. I can help with research, writing, coding, data analysis, and many other tasks that can be accomplished using computers and the internet.
>
>
>
> If you have a specific task in mind, I can break it down into steps and work through it methodically, keeping you informed of progress along the way. I'm continuously learning and improving, so I welcome feedback on how I can better assist you.
>
>
>
> \# Effective Prompting Guide
>
>
>
> \## Introduction to Prompting
>
>
>
> This document provides guidance on creating effective prompts when working with AI assistants. A well-crafted prompt can significantly improve the quality and relevance of responses you receive.
>
>
>
> \## Key Elements of Effective Prompts
>
>
>
> \### Be Specific and Clear
>
> \- State your request explicitly
>
> \- Include relevant context and background information
>
> \- Specify the format you want for the response
>
> \- Mention any constraints or requirements
>
>
>
> \### Provide Context
>
> \- Explain why you need the information
>
> \- Share relevant background knowledge
>
> \- Mention previous attempts if applicable
>
> \- Describe your level of familiarity with the topic
>
>
>
> \### Structure Your Request
>
> \- Break complex requests into smaller parts
>
> \- Use numbered lists for multi-part questions
>
> \- Prioritize information if asking for multiple things
>
> \- Consider using headers or sections for organization
>
>
>
> \### Specify Output Format
>
> \- Indicate preferred response length (brief vs. detailed)
>
> \- Request specific formats (bullet points, paragraphs, tables)
>
> \- Mention if you need code examples, citations, or other special elements
>
> \- Specify tone and style if relevant (formal, conversational, technical)
>
>
>
> \## Example Prompts
>
>
>
> \### Poor Prompt:
>
> "Tell me about machine learning."
>
>
>
> \### Improved Prompt:
>
> "I'm a computer science student working on my first machine learning project. Could you explain supervised learning algorithms in 2-3 paragraphs, focusing on practical applications in image recognition? Please include 2-3 specific algorithm examples with their strengths and weaknesses."
>
>
>
> \### Poor Prompt:
>
> "Write code for a website."
>
>
>
> \### Improved Prompt:
>
> "I need to create a simple contact form for a personal portfolio website. Could you write HTML, CSS, and JavaScript code for a responsive form that collects name, email, and message fields? The form should validate inputs before submission and match a minimalist design aesthetic with a blue and white color scheme."
>
>
>
> \## Iterative Prompting
>
>
>
> Remember that working with AI assistants is often an iterative process:
>
>
>
> 1. Start with an initial prompt
>
> 2. Review the response
>
> 3. Refine your prompt based on what was helpful or missing
>
> 4. Continue the conversation to explore the topic further
>
>
>
> \## When Prompting for Code
>
>
>
> When requesting code examples, consider including:
>
>
>
> \- Programming language and version
>
> \- Libraries or frameworks you're using
>
> \- Error messages if troubleshooting
>
> \- Sample input/output examples
>
> \- Performance considerations
>
> \- Compatibility requirements
>
>
>
> \## Conclusion
>
>
>
> Effective prompting is a skill that develops with practice. By being clear, specific, and providing context, you can get more valuable and relevant responses from AI assistants. Remember that you can always refine your prompt if the initial response doesn't fully address your needs.
>
>
>
> \# About Manus AI Assistant
>
>
>
> \## Introduction
>
> I am Manus, an AI assistant designed to help users with a wide variety of tasks. I'm built to be helpful, informative, and versatile in addressing different needs and challenges.
>
>
>
> \## My Purpose
>
> My primary purpose is to assist users in accomplishing their goals by providing information, executing tasks, and offering guidance. I aim to be a reliable partner in problem-solving and task completion.
>
>
>
> \## How I Approach Tasks
>
> When presented with a task, I typically:
>
> 1. Analyze the request to understand what's being asked
>
> 2. Break down complex problems into manageable steps
>
> 3. Use appropriate tools and methods to address each step
>
> 4. Provide clear communication throughout the process
>
> 5. Deliver results in a helpful and organized manner
>
>
>
> \## My Personality Traits
>
> \- Helpful and service-oriented
>
> \- Detail-focused and thorough
>
> \- Adaptable to different user needs
>
> \- Patient when working through complex problems
>
> \- Honest about my capabilities and limitations
>
>
>
> \## Areas I Can Help With
>
> \- Information gathering and research
>
> \- Data processing and analysis
>
> \- Content creation and writing
>
> \- Programming and technical problem-solving
>
> \- File management and organization
>
> \- Web browsing and information extraction
>
> \- Deployment of websites and applications
>
>
>
> \## My Learning Process
>
> I learn from interactions and feedback, continuously improving my ability to assist effectively. Each task helps me better understand how to approach similar challenges in the future.
>
>
>
> \## Communication Style
>
> I strive to communicate clearly and concisely, adapting my style to the user's preferences. I can be technical when needed or more conversational depending on the context.
>
>
>
> \## Values I Uphold
>
> \- Accuracy and reliability in information
>
> \- Respect for user privacy and data
>
> \- Ethical use of technology
>
> \- Transparency about my capabilities
>
> \- Continuous improvement
>
>
>
> \## Working Together
>
> The most effective collaborations happen when:
>
> \- Tasks and expectations are clearly defined
>
> \- Feedback is provided to help me adjust my approach
>
> \- Complex requests are broken down into specific components
>
> \- We build on successful interactions to tackle increasingly complex challenges
>
>
>
> I'm here to assist you with your tasks and look forward to working together to achieve your goals.

还有一个巨大的Json文件，可以理解为配置文件，我用AI整理了一下，大概是下面的内容。

### Browser Use

https://github.com/browser-use/browser-use

特别提一下这个开源项目，Manus官方也说是使用了这个更高效的网页分析工具。

### 小结

先叠个甲，根据现有认知，根据公开案例，根据各个信息来源初步总结。

**祛魅**：是营销也是真有用。

如果在真实业务中，能做到官网的质量，我愿意付费使用！说AGI雏形，没必要，因为雏形可多了。不需要神话，是个好用工具大家自然会买单。

**提示词**：高质量提示词的含金量还在上升\~

**不用急**：既然是产品，就剩发布时间和定价的问题了。

什么样的质量，准备花多少钱使用？

但还是想用，没有邀请码怎么办？

## OpenManus

https://github.com/mannaandpoem/OpenManus

开源社区来啦，OpenManus也是MetaGPT公司的技术伙伴，分析Manus之后，快速开源的一个Agent框架。

## OpenAI Agent创建工具

OpenAI也发布了新的工具，快速创建工具。

当然还有老朋友**Coze/ComfyUI/AutoGPT等**，如果你原来这些工具用的好，已经有很多智能体在帮你干活了，对Manus的认知肯定会更深刻。

## 此外还有一个新开源项目也值得关注。

https://github.com/Westlake-AGI-Lab/AppAgentX

难道说DeepSeek推理模型之后，Agent也要爆发？带来新的业务机会？

# 思考Agent背后

**【划重点💡】**有一个重要的认知，是Agent的能力是可以通过技术超过LLM模型本身能力的。

举个例子：大模型输出一个文稿的翻译，质量在60-80分，偶然掉到50分，偶尔超过90分，那么我们知道这个特性之后，就可以控制输出，只要90分那一次的。

可能需要跑100次、1000次才能抓到90分的那一次。

再次借助自动驾驶，找到Agent的位置。

## 怎么定义Agent智能体

人工智能第一课上，我们给了一个大概的定义。

 Agent（智能体）是一个广泛应用的概念，指的是可以在某种环境中自主行动，以完成特定任务的系统或软件实体。智能体能够感知环境信息，并基于这些信息作出决策，以实现其设计目标。

除了用专门Agent工具创建之外，我们认为GPTs/GLMs/各种LLM内的能力封装也算Agent一种。

这次我问了几个AI：

**【思考💡】**说的都挺好的，但是有点长，能不能精简一下？

提个假设：**完成具体任务的智能工作节点**

## 智能体三要素

**要素一** 具体任务

**要素二 智能（AI）**

把自动化、自我进化、自行判断，体现智能的部分都放在这里。

**要素三 工作节点**

这个有意思了

一堂的工作流/工业化生产。

## 怎么看待人工智能

**【思考💡】**AGI之前，怎么去看待人工智能？

**一个工具、一个超级工具**。

用的好坏，看**背后能力**

1.审美：能够评估AI产出的质量

2.边界：了解AI适用的场景

归根结底，**最后还是看人**

1.学得快，算的准ROI

2.有体系，最好长期修炼

3.创作力，不设限美好想象

其实这也正是一堂在践行的理念，把能力长在自己身上。

AI是放大器，底层是自己。

# AI生成业务公式工具

**【互动🙋🏻‍♀️】**业务公式那周还有印象吗？ #第一次文字分享

**工具选择**

1.选择工具：

a.最佳肯定是Windsurf、Cursor

b.试试DeepSeek的能力和Gemini

2.选择语言：使用HTML+JavaScript **#不需环境、方便迁移**

## 思路一 人工智能 一次生成

> 我有一个下面的数据，需要用canvas在html页面中，绘制成一个树状图。
>
>
>
> 女装店收入 =  进店人数 \* 付费转化率 \* 客单价
>
> 进店人数 =  女性进店人数  +  男性进店人数
>
> 女性进店人数 = 女性客流量(A1) \* 进店率(B1)
>
> 男性进店人数 = 男性客流量(A2) \* 进店率(B2)
>
> 付费转化率=选货率(C) \* 购买率(D)
>
> 客单价 = 人均件数(E) \* 平均单价(F)

**DeepSeek R1 vs Gemini 2.0**

恩，不相伯仲，后续略。

发现问题，我们想要的内容稍微复杂，给AI简单几句就想拿到结果有点难，如果有Manus可能能跑通。

转换思路：**拆出不同的"里程碑"，一点点实现，最后不行再上人。**

1.数据结构整理，保证数据层级是对的

2.绘制结构框架，保证基础的绘制是的

3.确保绘制准备，保证结构和我们理想的一致

4.优化绘制样式，尽量让结果和设计图贴近

## 思路二 人工智能+人类智能

**初始提示词**

> 我有一个下面的数据结构，需要用canvas在html页面中，绘制成一个树状图。
>
> 因为逻辑比较复杂，我们分成几步来完成这个html。
>
> 1）给我一个完整的html，不需要拆分，后续也是相同;
>
> 2）把我给你的数据根据逻辑，整理到一个树状结构中保存；
>
> 3）页面有一个文本输入框，用户输入后，根据新的数据整理树状结构；
>
> 4）整理之后的树状结构输出到控制台。
>
> 数据例子：
>
> 女装店收入 =  进店人数 \* 付费转化率 \* 客单价
>
> 进店人数 =  女性进店人数  +  男性进店人数
>
> 女性进店人数 = 女性客流量(A1) \* 进店率(B1)
>
> 男性进店人数 = 男性客流量(A2) \* 进店率(B2)

**调试过程**

## 复盘

**时间复盘**

1.AI时间1.5小时

2.人类+AI时间2小时

不用AI的话，至少10小时起，很多年没写过JavaScript。

**认知复盘**

1.**AI能力**：公认最强的前几个编程AI，能力差距不大

2.**找好场景**：DeepSeek R1分析速度太慢了，后来直接用Gemini

3.**后续延展**：多拓展一些场景，未来课程可以有更多的工具配套

# 作业和Candy

## 本周课程

## 关注俱乐部新的信息渠道

大家都知道一堂有三大俱乐部：**拆书会、私董会、AI 俱乐部。**有次 Truman 给了个划分逻辑，我觉的特别贴切。

这三个俱乐部的内容和一堂的正式课相辅相成，还有线下活动，可以说提供了一个全方位学习场域。

原来的课程提醒、俱乐部活动、提醒交作业等等活动，都是用几个微信账号给大家发消息，内部简称**"发Biu\~"**，大家应该收到过不少，帮大家更好的规划学习完成任务。

最近碰到一个困难，因为微信的官方规则，企业微信发消息有了很大的限制，运营效率变低，所以现在需要麻烦大家**加一个新的企业微信**，未来更好的收到一堂给大家的服务消息。

 AI俱乐部也会逐步提供更好的服务：

•*一键订阅所有的AI俱乐部直播*

•*AI俱乐部1v1提醒作业*

•*优秀作业点赞提醒*

•*……*

 赶紧关注一下吧\~

## 今天封榜

写歌已经有很多优秀的作品，不小心把回放改错了+作业链接放错了，所以再延长两天。

写歌链接：https://yitang.top/activity/3Ts67aeece1af4ff/edit

提示词大赛：https://yitang.top/activity/O3267aeecb81c784/edit

但是封榜是今天，周五一定批改完，Flag立下了！

## 招募志愿者

来自一堂同学张辉的一个共建尝试。简单介绍一下她：

•创过业，做过大消费VC和衍生品分析师，现在是全职心理咨询师第六年。

•一堂七年级，拿过复盘营+三天两夜+NPC培训三次MVP

•第三期S级私董会人生红点组NPC，为NPC们提供人生红点1V1辅导10+次。

接下来她计划，**第四期S级私董会继续探索人生红点**，有三个待验证的假设：

①人生红点必须和五步法商业画布相结合，才是一堂语境中真正的红点。

②人生红点还有L7\~L9段位，评估个人红点成为团队红点的过程。

③人生红点在L1\~L3阶段，可以由AI实现1V1辅导，效果不亚于咨询师/教练的1V1辅导。

诚挚邀请AI俱乐部有兴趣探索**第③条假设**的小伙伴联系她。

## 下周预告

终于安排上了，下周除了马拉松，特别邀请了芦玮娜律师团队的资深版权专家张鑫，给我们分享个人到团队，风险到踩坑，使用AI过程中的各种重要版权认知。

律师熟悉的业务，都不是小问题，下周三一定来听呀。

## 本次作业

**第一个作业：关于智能体**

今天又又又一次讲了Agent，有什么新的想法吗，有什么认知可以写份作业，我们一起探讨探索。

**第二个作业：自动化调研(共建)**

作为一堂最懂技术的群体，在自动化处理信息领域一定有自己的探索，欢迎你把业务中用技术完成信息调研/数据分析/竞品监控的过程分享给我们。

教研团队可能会联系你，用在马拉松上，让一万人一起学习参考你的最佳实践。

## 本期Candy

【🎁Candy**】**

1.本次分享的可部分复制的一堂Doc文档\~（30天有效期）

【Flag🙋】

来来来，希望大家一起立一个Flag（承诺），认真吸收，最后完成这次训练。

扣一句话吧：一定挑战！！

**看回放/逐字稿的同学**，**也要交作业啊！**你们的反馈真的很重要。

点击作业链接：https://yitang.top/activity/vH567d1276994680/edit

或扫描下方二维码完成作业\~\~

截止时间：**2025年3月18日（周二晚）24:00**

一定挑战，一定作业！\~

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI俱乐部周三LIVE](../01-AI认知与基本功/05-AI俱乐部周三LIVE.md)

---

<details>
<summary>原文配图上的文字（80 条，图片本身未随文提供）</summary>

**分享的内容**

- 「分享的内容」

**新模型新工具**

- 「新模型、新工具」

**飞书知识问答**

- 「数对话」 「知识库」 「最近对话」 「飞书知识问答」 「整合所有资料，让AI搜索回答」 「问个问题，或用知识库内容」 「联网搜索」 「使用知识」 「DeepSeek R1」 「上传文件至知识库，让AI立即使用」

**Chat2SVG开源文字生成矢量图工具**

- Chat2SVG工具，其使用大型语言模型和图像扩散模型生成矢量图形。图中呈现了多个示例，如戴着厨师帽的狗、背着背包站在滑板上的猪、盛开的向日葵等，下方配有英文描述。底部“概述”部分介绍该工具是生成矢量图形的框架，分生成、增强和优化SVG三个阶段工作。图片

**ImageFXGoogle免费文生图工具**

- 「真的很快，大概十来秒就能出图，看看成品」
- 「一个可爱的亚洲年轻男子，卷发，穿着蓝色衬衫，圆脸，皮克斯风格，表情符号和贴纸，多种姿势和表情，孩子般的纯真，扁平插画，立体人形，纯黄色背景，极简主义，8K」
- 「Create」 「Seed 27503」
- 以亚洲卷发圆脸男孩为核心的多种电脑前办公学习风格形象，核心男孩被设定为留着卷发、身着蓝色衬衫的可爱亚洲青年，风格偏向Pixar的童趣卡通质感。图片中呈现了该男孩的4种不同姿态：坐在办公椅前操作台式电脑、坐在高脚椅前使用电脑、在书桌前面对电脑以及在书桌前使用笔记本电脑，均搭配黄、红、黄、黄的纯色背景。图片左侧还显示了AI生图工具的操作界面，包含关键词提示、风格选项与生成设置，该图片用于展示符合描述的
- 相关AI生图工具的演示内容，展示的是一名卷发烫面、圆脸、身穿蓝色衬衫的可爱亚洲年轻男性角色，以皮克斯风格、扁平化插画及极简线条风格呈现，搭配纯黄色背景，该角色还带有孩童般的天真感。图片里呈现了多个该角色骑自行车的不同姿势与表情，部分姿势旁还有爱心元素，清晰体现了AI生成角色的不同表现效果，也呼应了上下文介绍的AI生图相关内容，展示了对应模型工具的生图产出成果
- 「There doesn't seem to be anything here.」 「Try a different prompt and check out our content policies here.」 「一致性实现也相对简单」

**PodAgent开源播客框架**

- PodAgent播客生成综合框架。该框架包含主持人（Host）、嘉宾（Guests）、LLM-powered Agents（包括Host-agent、Writer-agent、Guest-agent A、Guest-agent B）以及听众（Audiences）。主持人以脱口秀形式呈现，由一位主持人和几位嘉宾组成，节目包含多样化观点，配有结构化音效和背景音乐。LLM-powered Agents负

**千问开源QwQ32B模型**

- 不同模型在各类基准测试中表现的柱状图，测试任务包含AIME24、LiveCodeBench、LiveBench、IFEval、BFCL五类。图中共有五种模型的测试数据，分别为红色柱状代表的QwQ-32B、蓝色柱状的DeepSeek-R1-671B、浅灰色柱状的OpenAI-o1-mini、深米色柱状的DeepSeek-R1-Distill-Llama-70B、浅米色柱状的DeepSeek-R1-D

**Google发布Gemma3开源模型**

- 「Gemma 3」 「今天下午发现Google又放大招，看这个图，27B版本比V3还要强」
- Gemma 3系列模型的规格参数。表格中列出了Gemma 3 1B、4B、12B、27B及Shield Gemma 2的模型大小、上下文长度、支持语言和输入模态。Gemma 3系列模型支持多语言，上下文长度均为128k，可作为预训练模型或通用指令调整版本。Shield Gemma 2模型大小为4B，上下文长度为8k，同样支持多语言。该图
- 「Model Performance vs. Size」
- 「Gemma 3 Release」

**CL1**

- 「世界上第一台可代码部署的生物计算机」
- 「硅遇见神经元」 「世界上第一台可代码部署的生物计算机」
- Yitang AI MUSE模型全景图，版本为2.0。图中将AI技术能力迭代分为大语言模型、硬件、机器人、边缘计算、云等底层技术变革性突破，处于变革层。其上是创业层，包含前沿新项目、AI创业创意库、机会预约模型等。再往上是使用层，有提示词/库、AI工具集、Agent助理、AI部署等。最上层是奇迹层，涵盖AI的大胆设想和科幻。该图

**聊聊Manus火爆**

- 「聊聊Manus爆火」 「聊聊Manus火爆」

**ManusAGI雏形**

- 「调用AI能力，实现全面提质提效」 「关于七龙珠的爆款笔记」
- 「产品内容的反馈」
- 「小红书内容AI自动生产流程整体设计」
- 「Agents」 「Demos」 「Flows」
- 「深度分析特斯拉股票」
- 「用中文回复我」
- 特斯拉2021 - 2024Q1的公司概况与关键指标及财务数据分析。核心业务包括电动汽车、储能产品等。市值约6800亿美元，股价波动较大，动态市盈率高于行业平均。交付量、营收、毛利率、净利润率等数据逐年变化，2024Q1自由现金流为-8亿。趋势解读指出营收增速放缓、利润率承压、现金流预警等问题。该图
- 特斯拉的市场情绪与新闻催化剂及技术分析（周线级别）相关内容。分析师评级方面，买入32家、持有15家、卖出8家，目标价中位数为$220。情绪指标中，空头仓位占比3.2%（低于2022年峰值15%），散户持仓比例43%（WallStreetBets热门标的）。近期新闻驱动方面，利多为FSD V12开放订阅、墨西哥工厂获批，利空为中国市占率下滑至7.5%（vs比亚迪18%）、欧盟对中国EV反补贴调查。技
- 是特斯拉与其他车企的对比数据及价值相关分析内容。其中明确列出特斯拉与比亚迪、大众、Rivian的市值、EV市占率、2023年毛利率、研发投入占比等数据，还标注了特斯拉的优势领域与短板；同时包含基于DCF模型的内在价值估算相关假设，涉及永续增长率、WACC、对应股价区间，增长驱动力及主要风险等内容，是针对特斯拉的相关维度分析资料
- 是特斯拉的SWOT分析及投资论点。优势方面，全球EV品牌认知度第一、垂直整合降本能力强、储能业务年增速80%、Dojo超算赋能AI迭代；劣势为产品线单一（依赖Model Y）、高管团队稳定性风险、中国车企价格战、美联储高利率压制估值。分类型建议包括激进投资者、稳健型、保守型、长期持有、短线交易等策略。结论指出特斯拉处于转型关键期，短期需消化估值压力，长期具颠覆性创新潜力，建议投资者动态调整仓位，重
- 「本次会话中的所有文件」 「有总结，有图表，有数据，有来源，有结论，有指导，很夸张了，过程还完完整整给你」
- 「强烈买入」
- 特斯拉的市场定位、技术分析及SWOT分析等内容。市场定位部分，以饼图呈现全球电动汽车市场份额，特斯拉占比18.4%。技术分析部分，有特斯拉股价及移动平均线图，还列出了RSI、MACD等指标数值。SWOT分析中，优势包括品牌实力、客户忠诚度等，挑战如高定价、供应链问题等，机遇有全球电动汽车市场增长等，威胁如市场竞争、供应链风险等
- 「价格目标和场景」

**BrowserUse**

- 「Browser Use」 「Enable AI to control your browser 🤖」 「Stars」 「Discord」 「Cloud」 「Documentation」 「Follow @Gregor」 「Follow @Magnus」 「Weave」 「Try the cloud」
- 「Browser Use」 「启用AI来控制您的浏览器」 「Stars」 「Discord」 「Cloud」 「Documentation」 「Follow @Gregor」 「Follow @Magnus」 「Weave」

**OpenManus**

- 「seo_website.mp4」

**OpenAIAgent创建工具**

- 「Triage Agent」 「CRM Agent」
- 用于构建代理的新工具界面，界面中列出了多种代理类型，包括Triage Agent、gpt4all、POST Responses、Nanoflare、CRM Agent、POST Inferences等。下方文字说明了发布第一批构建代理的工具，提到新API的出现让代理构建更简单，还介绍了新API与Chat Completion API的特性、工作原理及使用方法，以及新API与SDK的集成等。该图片

**此外还有一个新开源项目也值得关注**

- 「Subscribe '3Blue1Brown' on YouTube」

**思考Agent背后**

- 「思考Agent背后」
- 「自动驾驶分级·对比理解版」

**怎么定义Agent智能体**

- Agent（智能体）的分类及典型应用场景等内容。Agent被分为简单反射型、基于模型的、目标驱动型、效用驱动型、学习型五类。典型应用场景包括物理Agent（如自动驾驶汽车、工业机器人）、软件Agent（如智能客服、智能翻译程序）、混合Agent（如人机协作系统）。图片还对比了Agent与普通程序、Agent与AI等概念，以及介绍了Agent的理论背景，如在经典AI框架中，Agent是核心研究对象，
- 「Agent（智能体）」
- 「思考💡」

**智能体三要素**

- 「超级小抄」
- 「我的任务」 「拆解并准确理解任务」 「清北博士」 「理解TA的能力边界和工作习惯」 「布置任务」 「布置任务和管理工作流」
- 「我的任务」 「拆解并准确理解任务」

**AI生成业务公式工具**

- 「AI生成业务公式工具」
- 一张手写公式图，展示了服装店收入的计算公式。公式为服装店收入 = 进店人数 × 付费转化率 × 客单价。其中，进店人数由女性进店人数（女性客流量×进店率）和男性进店人数（男性客流量×进店率）组成；付费转化率由选货率（C）和购买率（D）构成；客单价由人均件数（E）和平均单价（F）组成。该图
- 女装店收入的计算公式版本3。公式为：女装店收入 = 进店人数 * 付费转化率 * 客单价。其中，进店人数 = 女性进店人数 + 男性进店人数，女性进店人数 = 女性客流量 * 进店率，男性进店人数 = 男性客流量 * 进店率；付费转化率 = 选货率 * 购买率；客单价 = 人均件数 * 平均单价。该图片
- 女装店收入的计算公式版本3，以树状图形式呈现。公式为：女装店收入 = 进店人数 × 付费转化率 × 客单价。其中，进店人数由女性进店人数和男性进店人数组成，女性进店人数 = 女性客流量 × 进店率，男性进店人数 = 男性客流量 × 进店率；付费转化率由选货率和购买率构成；客单价由人均件数和平均单价相乘得出。该图

**思路一人工智能一次生成**

- 「DeepSeek R1 vs Gemini 2.0」
- 女装店收入的业务公式关系图。女装店收入由进店人数、付费转化率和客单价构成。进店人数包含女性进店人数和男性进店人数，女性进店人数由女性客流量和进店率决定，男性进店人数由男性客流量和进店率决定。付费转化率由选货率和购买率决定。客单价由人均件数和平均单价决定。该图

**思路二人工智能人类智能**

- 一段对话内容，是一位用户向AI提出的需求。用户希望AI用canvas在html页面中绘制一个树状图，因逻辑复杂，需分步骤完成。步骤包括提供完整html、整理数据到树状结构、有文本输入框处理用户输入、整理后输出到控制台。数据例子给出女装店收入计算公式及进店人数计算公式。此图
- 「女装店收入」 「进店人数」 「付费转化率」 「客单价」 「调试过程」
- 「处理数据基本ok，但是请你保留重要的运算关系，比如*+/-xX等，请你补充到数据处理的逻辑中」
- 一段代码调试过程，核心是修正公式节点的运算符号逻辑问题。对话中说明公式最后作为最终因子的叶子节点不应带有运算符号，原逻辑错误地将父节点的运算符传递给了叶子节点。图片中呈现了修改后的buildTree函数代码，该函数用于确保叶子节点不包含运算符属性，代码里定义了processNode函数，还列出了加、减、乘、除等常用运算符号，体现了调试后规范公式节点属性的实现逻辑
- 「还是不对，少了一些重要的运算关系，请你再次检查」
- 「女装店收入」 「name」 「operator」
- 「女装店收入」
- 一段代码调试的相关内容，包含用户的修改需求与开发者的回应及代码示例内容。用户提出要调整文字和节点间固定的间隔，改为动态计算。开发者给出回应，说明可通过动态计算节点文本宽度来确定间隔，以保证文字始终与节点对齐，随后展示了修改后的drawTree函数的部分代码，其中包含函数定义、节点相关参数设定，如第一层节点水平间距、节点宽度、高度、圆角半径，还有颜色数组的配置，以及绘制根节点的字体样式设置
- 「树状图生成」
- 「好，下面开始绘制首层之外的其他节点」
- 「树状图生成」 「你要记住，第一层的处理结构和后面是不一样的，请你回到之前的绘制首层的逻辑，然后优化代码」
- 「忘记上一步的修改，新写一个函数，在计算了位置之后，从最底层节点，再重新调整子节点的x和y」
- 「JavaScript树状结构宽度调整函数」
- AI生成业务公式工具调试过程中关于节点x值调整的规则及代码。内容包括根节点x值不变，第一层子节点x值从根节点x值50开始累加lWidth，下一层子节点x值从父节点x值50开始累加lWidth，同时考虑父节点lWidth和同层节点布局。还给出了实现这一功能的完整代码，为调试过程中的节点x值调整提供了具体操作指南
- 「实现父节点的x值位于其子节点的中心位置」 「调试过程」
- 是一个关于AI生成业务公式的调试反馈内容。一位用户反馈问题出在父节点的x值计算逻辑上，需确保父节点x值位于其所有子节点中心位置，而非简单取平均。图片给出修正后的代码和逻辑，包括父节点x值计算公式，即parent.x = firstChild.x + (lastChild.x + lastChild.width - firstChild.x) / 2，其中firstChild.x是第一个子节点的x值
- 「写一个函数，删除字符串开头的空格或者‘-’」
- 是一个对话界面，上方是用户处理类似内容的指令，包括女装店收入计算公式及进店人数、付费转化率、客单价的计算公式。下方是AI助手的回复，指出需处理带有缩进的数据，缩进用空格或“-”表示层级关系，处理时需去除缩进并转换为树状结构。还提供了修改后的processData和buildTree函数代码。该图片

**复盘**

- 编程相关AI模型排行榜的页面截图，页面顶部显示相关说明信息，该页面聚焦于判断对话是否包含代码片段的内容，共收录209种模型，当前显示的是排名靠前的模型列表，其中排名第1、2、3位的模型被红色框重点标注，分别为doubao（Early release）、gemini-2.5-pro-exp-02-05、Claude-3.5-Sonnet；排名第10位的deepseek-v3被绿色框标注，页面还展示了

**作业和Candy**

- 「作业和Candy」 「发Biu~」

**本周课程**

- 「我用一堂做一堂：知行合一篇」 「进班听课 限大会员 仅限2000人 紧紧上车！」

**关注俱乐部新的信息渠道**

- 三大俱乐部的内容，分别是拆书会、私董会和AI俱乐部。拆书会对应过去经验的总结，私董会对应当下问题的解决，AI俱乐部对应面向未来的挑战。这些俱乐部

**招募志愿者**

- 「一堂 YiTang.top」 「已加入一堂 1199天」

**本次作业**

- 「本次作业」

**本期Candy**

- 「一定挑战！」
- 「看回放/逐字稿的同学，也要交作业啊！你们的反馈真的很重要」 「点击作业链接：https://yitang.top/activity/vH567d1276994680/edit」 「扫描下方二维码完成作业~~」

</details>
