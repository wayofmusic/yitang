---
title: AI落地Live79：不要着急让AI干活，AI时代的问题重构
node_token: IB1EwyqY4i8unlkku9VcsmPinke
source: https://www.feishu.cn/wiki/IB1EwyqY4i8unlkku9VcsmPinke
space: 一堂学习
obj_type: docx
synced: 2026-09-25 20:20
course_line: AI能力线
stage: AI行业与前沿
train: AI行业与前沿
form: 直播逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
🎯AI落地Live79：不要着急让AI干活，AI时代的问题重构

Hello，大家好啊，欢迎来到**一堂AI俱乐部**·**落地Live分享**。

我是纪浩。先给新同学画个重点，我就非常简单的讲三点。

1.咱们直播结束之后，回放和文稿都会发给大家的，开放5天时间自由学习。是需要大家提交作业的，快，一定作业\~

2.这周五，一堂最经典的、独树一帜的课题，《清单体笔记》它又来了，周五晚上直播。还没进内测群的，快，扫码进群\~

💥时隔一年半，重讲一堂内部第一基本功「清单体笔记」‼️

很多人都羡慕Truman解题的能力，但是他说，练记笔记其实是这一切的基础。

记笔记，也是一堂内部的第一基本功。所有关键的协同会议纪要、顶层设计的文档、专项调研、专家访谈、方法论萃取，都离不开记笔记。

一堂的清单体笔记，不同于其他笔记，是极高价值的"解决问题的笔记"。很多同学学习之后，都说自己上了那么多年的学，居然在一堂才真正懂得记笔记的意义。

但是，AI时代也带来了新的课题：AI都能记笔记了，人还需要练习吗？如果还要练，到底练的是什么？

本周五，Truman将带你重新理解AI时代，清单体笔记的价值和练习方法，以及清单体笔记和AI数据之间的关系。同时，我们还会尝试交付帮你刻意练习"记笔记"基本功的AI Partner。

如果你想通过记笔记持续提升自己的解题能力，或者是想找到你可以长期刻意练习的题目，这节课一定要来！

**【互动🙋🏻‍♀️】**有多少同学是新加入的呀？可以扣1报到一下。

3.如果你是新同学，还不了解一堂的AI相关内容，请记得回去查看下面的链接↓

> **①新同学看这里，一堂AI体系和相关内容，**你需要知道的内容都在这里！ ☆☆☆☆☆
> https://yitanger.feishu.cn/wiki/JDLqwVHTniV1gJkM9JHcd1Wdnfh
>
> **②一堂AI俱乐部知识库**，1-66期回放在这里**：**☆☆☆☆☆
> https://yai.yitang.top/intro
>  **AI知识库一页纸长期投稿入口，投稿就有3学分，收录最少5学分：** https://yitanger.feishu.cn/share/base/form/shrcnj37Bn9wqHZAZhNVDiAV8Qc
>
> **③《AI俱乐部新人指南》，**想了解AI俱乐部可以看看：☆☆☆
>  （待更新，很多内容被第一篇覆盖了）
>  文稿链接：https://yitanger.feishu.cn/docx/Zz9tds3HtoRGmNx2eoxcL8GbnUt
> 回放链接：https://air.yitang.top/live/w8HDGvkmT6?part=AI%E4%BF%B1%E4%B9%90%E9%83%A8%E5%BF%85%E8%AF%BB%E6%8C%87%E5%8D%97&rs=5431

好，这是我第三次来到 AI 俱乐部分享了，上一次来的时候，Claude 还只出到了 4.6。

三个月过去了，这三个月里面 AI 的变化很多，我自己的认知也有很大的跃迁，也尝试了在底层规律和方法论层面，去思考现在 AI 的一些现象和问题，以及背后的解决思路。

 某位不愿意透露姓名的Sherry同学评价我：“哲学家里面最会写代码的”

我们正式开始。

# 纪浩：在AI任务开始之前

大家好，我是纪浩，是一堂的后端开发工程师，我又又又来了。

感谢于陆老师的邀请，这次是第三次来到AI俱乐部给大家做分享。

这次的主题不再是针对Vibe Coding这个有局限性的场景，而是一个更广泛的场景，我们在与AI协作的过程中，如何不断的自我迭代，无限进步。

上一次关于Vibe Coding的分享，我描绘了一张美好的蓝图，人与AI未来的协作模式会从PDCA的工作流，演化到 Goal -> Run 的自动驾驶模式。

这里有一个容易引起误会的陷阱，就是**高质量的PDCA对人的要求是很高的**，直接从PDCA开始，似乎暗示着人人都是专家。

而在我自己的真实实践中，以及和朋友的交流过程中发现，我的大多数场景下，都是在**用AI做我们能力边界之外的探索和实验**，而在我们不是专家的情况下，往往结果是Plan越多，错的也越多，PDCA循环启动所需要的难度也越大。

这不是说PDCA本身是错的，真实的问题可能在我们开始动手之前就已经发生了。而接下来，我将仔细讨论围绕这个**核心问题**展开的一系列讨论。

实话说，今天的内容有一些抽象，但全是我真金白银烧Token烧出来的，整理出来有点艰难，但是**真的值钱**，希望大家能陪我到最后；希望未来你遇到同样问题的时候，可以想起来之前在AI俱乐部，**有同样的探索者，还有同路人**。

**"翻过一个墙，最好的方式，就是先把自己的鞋子，勇敢扔过去"**

来来来，希望大家一起立一个Flag（承诺），认真听我分享，找到你的切入点。

扣四个字吧：一定坚持

如果你能完整听完本次分享之后，对下面这“**灵魂三问**”，有了一些自己的思考，那我的分享应该就算是成功了。

**问题一** Agent时代，人类学习是否有意义？

**问题二** 当我描述了一个目标，产生了一个好奇心或做事情的冲动，我是不是在解决一个“真问题”？

**问题三** 我和Agent协作的工作流究竟靠谱吗？有没有办法在开工之前发现潜在的问题，并进行一些防御性措施，提升成功率?

那么，我前面提到的这个**核心问题**究竟是什么呢？

在与AI协作的过程中，*我的水平如何？我究竟是新手还是高手？*

## 准备篇

### 最核心的问题： 在与AI协作的过程中，我究竟是高手还是新手？

【互动🙋🏻】帮我热个场，面对这个问题：

认为自己是高手的，可以评论区扣个1

认为自己是新手的，可以评论区扣个2

经常困惑这一点（或者两者横跳）的，可以评论区扣个666

————

首先给一个最简单的判断方式：

•*AI做的足够好吗？*

•*我能看出AI哪些细节和过程处理的不够好吗？*

•*能不能指出AI的问题，补充标准，资料，流程检查点，让AI做的更好？*

•*我自己动手的话，可以比AI做的更好吗？*

如果上面很多答案都是“**否**”，那么毫无疑问，你在这个问题上就是新手。

感谢你的客观务实，是新手也没有关系，大家都是从新手村练出来的。

识别是不是新手的目的，不是为了给自己贴负面标签，不是为了否定自己，而是为了重新唤起自己的**敬畏之心和进取之心**，让自己找到真正的起跑线，无限进步。

刘慈欣在《三体》中有一句名言： “**弱小不是生存的障碍，傲慢才是**”。

在使用AI的过程中，萌新并不可怕，后面我会介绍，萌新在有些情况下反而会成为优势。可怕的是自己明明是萌新，却希望用高手的标准要求自己。

•*“我和张三都用Claude Code，为啥他能做出来，我就做不出来？”*

•*“张三已经开始养马了，我还在养虾，我是不是落后了？”*

•*“张三都已经做出来东西了，我连环境还没装上，我是不是太笨了？”*

心理建设完毕，这里先举一个最近的真实例子。

众所周知，我是一个**后端工程师**，我**不熟悉前端生态，不会产品设计，几乎完全没有UI审美**。

我平时使用AI做的东西，大多都是“看不见的”服务和脚本，或者说，做这些“看不见”的东西，是我的舒适区。

但是，偶尔我也需要做一些简单的 Web UI 页面，因为需求比较简单，我也不想找一些复杂的前端框架，目的是为了避免给项目添加不必要的复杂度。

但结果就是，**我的审美水平 <= GPT的审美水平;**

而众所周知，***GPT没有审美***，于是，我做出来的东西就长成了这样：

（插图）

【互动🙋🏻】你们给这个页面打几分？

（真实客观打分）

————

后来，我和AI进行了激烈的对抗，在多轮讨论之后（具体过程会在后面详细介绍），我终于搞出了一个我自己用着比较舒服的 UI Design Skill ，我的页面终于可以长成了这样。

【互动🙋🏻】你们给这个页面打几分？

（真实客观打分）

————

而这个UI之所以可以被约束住，是因为在UI的背后，有大量的背景，约束，校验条件，让AI把事情作正确。文档大概长这样（不要着急让AI干活 - AI时代的问题重构）：

到这里，我本来应该挺开心的。但是，不要忘了，我在设计领域其实是一个**完完全全的萌新**。

打脸来的特别突然，我的前端同学只是用Grok随便帮他细化了一下Prompt，AI就把UI做成了这样：

【互动🙋🏻】你们给这个页面打几分？

（真实客观打分）

————

对比的结果就是，我用了*极高昂的注意力成本，时间和token成本，做出了一个不如高手随手搞的东西*，虽然现实很残酷，但事实就是，如果萌新不努力，用AI做出来的也就是一坨，但哪怕非常努力，萌新拼尽全力还是不如高手随手搞一下。

不过，这是好事儿，**认清差距才有努力的方向**。

用新手的心态，不给自己增加无谓的包袱，能带来这些好处：

•*对结果的预期低，不会给自己设定一个高到几乎不可能完成的目标*

•*容易把问题想简单，不会给自己脑补各种各样的问题*

•*步骤设计的简单，可以轻装上阵，不至于出现“放弃之前一直在准备”的情况*

•*享受过程，做出来一个“差不多”的东西就会很开心*

•*容错高，遇到了问题时，会把注意力专注在寻找办法上，而不是反复用问题“抽打”自己*

试想，如果我们反过来用很高的标准去要求自己，那么做事情的过程可能就会变得充满压力。

在大模型被广泛应用之前，我绝对不会鼓励别人多去尝试，而是最好“谋定而后动”，尽可能把地图探清楚，把雷排干净。而现在之所以心态发生了巨大的变化，是因为AI极大的降低了试错成本，并且提升了成功率。

所以，后面我们将会用“新手心态”来走完整个旅程。

一般情况下，人的精力是有限的，只在少数领域内能够达到专家水平，大多数别的领域中，其实都是萌新宝宝。

### 开始动手前必须想清楚的第二个问题：你要解决的问题，究竟是problem？还是question？

不知道大家与没遇到过这样的情况，用上Agent之后，每天感觉自己很兴奋，脑子里有无数个点子，Agent烧了无数的token，但是仔细想想，自己除了花时间让Agent烧了很多Token，但好像并没有做出什么有用的东西。

之所以有这个感觉，最大的可能，**就是因为我们要么*只是在提出question*，要么只是在解决伪需求，而没有解决真正的problem。**

在一堂，我们经常使用的一个说法，叫做寻找并解决**“真实问题”**，围绕真实问题进行学习。 而这里的真实问题指的其实就是**“problem”**。

具体来说，这**两个词究竟有什么区别呢**？

•当你提出一个question后，别人给出答案就可以令你满意。你不需要对现实世界做什么，别人也不需要对现实世界做什么，世界的状态不会发生任何的改变，而你**得到的只是一些信息**。

•而当你提出一个problem时，你是真的在现实世界中看到了一些让你不能接受的现象，并**希望这个现象被改变**。

这里举个例子：

•如果你问：为什么下水管道会堵？  这是一个question。

•而如果你发现：我家下水管道堵了，如何解决？ 这就是一个problem。

**回答question满足你的好奇心**，无法解决的question只会让你心痒难耐，但并不会让你损失什么。

**解决problem则是实打实的会改变你的生活状态**，problem被解决的越快越好，越晚解决problem，损失也就越大。

仔细观察就会发现，前Agent时代的网页聊天和知识库应用，这两个应用形态解决的都是question，解决不了problem。

而龙虾也好，CC也好，Hermes也好，Codex也好，这些Agent都是实打实可以解决problem的。而当AI可以解决problem之后，我们一下子就觉得AI好像突然“有用了”。

在动手用AI解决问题之前，我建议**多问几层“为什么”**，因为有些看起来是problem，但实际上是“伪需求”。 而有些伪装成question的，实际上是一个高价值problem。

这里我先列几个problem的关键特征：

1.***BeforeAfter：problem一定有明确的前后状态对比***

2.***真实锚点：problem一定有现实世界的真实锚点***

3.***受益人：problem一定有受益人***

4.***因果链：problem必须相信存在可探索的因果链，且有足够的能力支撑***

我成这几个关键特征为：4要素。

这里以前端小哥哥做的Skill市场为例，不熟悉Skill的就当做一个工具/插件市场来理解，下面我逐条说明为什么这4个要素很重要。

1.**前后状态对比，从根本上决定了需不需为了解决问题而付诸行动**

没有Skill市场时，我们通过微信传zip分享Skill，通过模糊的口述反馈问题，通过文件名区分版本

有Skill市场后，我们就可以对Skill集中管理，集中分发，版本控制

2.**problem一定有现实世界的真实锚点，否则需求一定会被“带飞”到九霄云外**

Skill市场的现实锚点是一堂内部。

这意味着最多50人，不需要考虑并发，要考虑鉴权和内部访问，Skill要面向业务方，不是纯研发同学...

如果没有Skill市场，就很容易做成一个对标github或Skill.sh 的大而全的网站

3.**problem一定有受益人，否则一定没有ROI**

Skill市场一定要为Skill的使用者提供方便

其次是服务Skill的维护者

如果公司没有人开发和使用Skill，那这个市场就没有价值

4.**problem必须相信存在可探索的因果链，且有足够的能力支撑**

试着想一下，分享Skill这个过程中，产生problem的真实场景：

•张三看到我做的东西很好，问我“你是怎么做出来的？”

•我说“我用了xx Skill”

•张三问 “能不能发我一份？”

•我开始找Skill到底放在了哪个文件夹，然后打成zip，微信发送给他。

•后台，我对Skill做了升级，但张三用的还是旧版的Skill

•而张三用Skill的时候，可能会和我说：“我和cc说让他用你的Skill做个xxx，结果做的不行，你能帮我看看为啥没做好么？”，而我没有他实际使用的上下文，我也不知道怎么帮他解决问题

•......

造成Skill难以分发和维护的原因在于：

1) Skill平时保存在设计者的 "\~/.claude/Skills/xx-Skill/.."目录下，不容易找

2) Skill一定会迭代，迭代之后必须证明新版本优于旧版本

3) 用户上报Skill的问题一定要提供具体的上下文

4) Skill的创建，打包，自述，下载安装...最好不要让人来操作，而是agent自己操作，否则结果就是不仅没有解决用户的原始problem，还带来了新的problem。

所以，基于这些真实问题，我们才能把Skill市场的需求分析清楚。

•用市场集中管理版本和分发

•数据库和并发不是瓶颈

•一定要在页面上把Skill的能力，用法，使用场景描述和展示清楚，但不要让人来填表单，而是AI把信息补充完整

•平台一定要给Agent留好接口，不要教用户怎么用这个后台，给用户安装一个专门的Skill，用户有什么需求，让Agent调用这个Skill解决。

•......

案例介绍到这里，希望大家能够感觉到，澄清问题，找到真正要解决的problem是很重要的。

•没有明确的**前后状态变化(BeforeAfter)**，我们就没法定义和验证问题是否被解决。

•没有**真实锚点**，我们的解决方案就会无限发散，进而脱离真实问题。

•没有**受益人**，我们就不知道我们解决问题有没有实际价值，也没办法拿到真实的反馈，最终把解题变成自high

•没有**因果链和能力支撑**，我们就没有办法给问题找到合适的解决方案。

而后面我们将会看到，我们这一步工作将是后面所有工作的起点。

【互动🙋🏻】有没有人有这样的疑问： “如果我们是新手，我们的眼光不如专家毒辣，这一步做不好怎么办？”

————

这里最重要的，不是我们一次性把这4个要素找准找对。

当我们提出了问题，我们就有各种各样的方法去寻找答案：

•提假设

•做调研

•做访谈

•问AI

•做实验

•......

这里最重要的原则是：我们要主动去找这4个要素，只要这4个问题的答案不能让自己满意，就不要轻易下场动手。

做错一件事的损失要远比不做一件事损失高的多。听懂这个里程碑思维的可以扣个1，自己就是这么做的扣个555。

## 起步篇

前面两个大问题搞定之后，我们就要开始真正尝试动手解决问题了。但是，让AI动手解决问题的第一步，不是动手写prompt，而是**搭建Agent执行任务所需要的工作空间**。

### 上手解题的第一个问题：工作空间的准备

【思考🤔】什么是工作空间的准备，或者说为什么要管理好工作空间呢？

用过各种Agent、龙虾、Hermes的同学们是否遇到过这样情况：

在一个用Agent 持续自主迭代的项目中：

1.第一周AI工作质量非常高，产出也非常稳定；

2.随着让AI接手的工作变多，变杂之后，AI开始出现各种混乱的行为，比如理解错误问题，用错误的流程解决问题，工作时开始走神或原地打转，目录也是乱七八糟的；

3.然后我们让AI自己分析问题，AI说的头头是道，给我们重新设计文件目录和工作流，但实际执行的时候，AI反而比以前出现了更多的问题，从此在错误的道路上越走越远……

4.而我们想帮帮AI，也不知道自己能做些什么，只能放弃这个目录，让AI重新投胎，从头再来。

【互动🙋🏻】有没有同学遇到过这样情况？

————

这个问题本质上是因为：**目前的AI只会“模仿”，不会设计结构。**

**现阶段还是需要人来帮助AI做好规划，避免AI长歪了。**

这里，我们先看看“高手”的项目目录会长成什么样子：

•系统结构描述

•领域知识

•ForAgent

◦导诊台

◦Agent工作手册

◦工具集

◦经验与模式库

•任务管理

◦任务定义

◦交付物

◦上下文

◦状态管理与归档

•日志

这里我先不具体解释，而是举两个例子，**一个相对比较复杂，一个则是简化的例子。**

通过这两个例子，来说明为什么需要这样分类，如何让结构自然生长，以及AI会如何使用这些知识。不过不用担心，因为我们是“新手”，我们只要看看就好了，而不是必须把我们的工作目录弄的一模一样。

我们可以结合自己的工作，从熟悉的问题出发，把关注点放在这几个地方：

 1.*这部分知识负责描述和解释什么？*

2.*这部分知识是谁定义的？怎么产生的？*

3.*为什么必须有这些知识？谁在什么情况下使用这些知识？缺失的话会产生什么影响？*

4.*如何在合适的时间找到这些知识？*

这里先介绍一下两个案例的背景：

•一堂Be是一个后端项目，包括公司后台和直播间，选课中心等项目的API；

•SQL-Helper 是一个用户用自然语言向AI提出数据需求，AI根据一堂的线上数据库，写查询SQL，给出分析结果的应用。

有没有被这个表给吓到了？ 不用怕，罗马不是一天建成的。我们作为新手，在起步阶段没必要把问题复杂化。

这里的关键是理解一个复杂项目的知识会包含这样的五层结构：

因此，一个最小实现应包括：

•**ForAgent**

◦**Agent工作手册**

◦**工具箱**

◦**经验与模式库**

•**系统自述和领域知识必须拆开**

•**交付物**

•**对话上下文**

我们需要持续观察Agent的行为，并根据问题，按需增加合适的部分即可。

思考下面这些问题有助于让我们找到我们需要哪些知识

 1.*你希望Agent做什么？这些过程会生产什么？*

2.*AI解决这些问题时，工作流，产出物，用到的知识是否相同？是否需要做区分？*

3.*不同类型任务的流程是怎样的？依赖的知识和能力如何获取？渐进式披露的链路如何构建？*

4.*如何验证关键步骤？如何纠偏或及时中断？ 如何验收结果？*

5.*哪些知识是在描述系统？ 哪些知识是在描述系统所服务的领域？*

6.*习惯一次对话只围绕一个任务目标进行展开，我们是否能在开始对话前，预估需要经过哪几轮对话，可以让AI的任务完成度达到符合我们要求的程度？*

如果我们自己回答不了这些问题，我们可以先让AI把流程跑通，然后反问AI，让AI来回答这些问题。

当我们习惯用工作空间的视角来看人机协作的时候，我们的角色就会慢慢**从Agent的旁观者转变为Agent的管理者**。

### 上手解题的第二个问题：如何从0开始PDCA

不知道大家有没有遇到过这样的情况： **PDCA似乎并没有什么价值？**

•对于**熟悉的任务**，我们不需要PDCA，靠着习惯和本能，也能把工作完成好

•对于**陌生的任务**，我们做了PDCA，结果反而不如不做PLAN，因为实际的任务从来没有按计划的剧本上演过，跑过几轮发现没有用之后，就自然放弃了。

【互动🙋🏻】有没有同学遇到过这样情况？

————

我的观察，新手和高手最大的区别就是：

高手用套路做事可以提升自己的效率和发挥的稳定性；

*而新手用套路反而会降低自己的效率和发挥的稳定性。*

新手必须**对Plan这个行为慎之又慎**，因为：

1.人非生而知之者，高质量的Plan是一个复杂的心理活动，需要大量历史数据的分布，异常期望，兜底策略，资源/流程整合等信息的综合演算做支撑，新手可能连实际的流程都不了解，更不可能做出高质量的Plan

2.高手会把复杂问题拆分成多个互相不依赖，可独立验证的子问题，不仅是执行效率的优化，还包括阶段性验证，可回退，爆炸半径可控等。  而新手的Plan很可能方向错误，或者过于激进，进而导致落地执行过程演化成不可挽回的混乱

3.新手容易无视掉自己不能理解的信息，或者简化问题模型，无知者无畏

【划重点💡】更本质的讲：

不是Plan提升了成功率，不是Plan越多成功率越高，而是**Plan中有效的兜底策略和Check的有效纠偏提升了成功率**。

如果Plan不能提供有效兜底，以及触发及时有效的纠偏，那么Plan越多反而越容易失败。

【思考🤔】既然如此，上面的解释是不是反而证明了对于萌新宝宝来说，PDCA没有用处吗？

之所以有这样的误解，是因为我们**搞错了PDCA的出发点**。

PDCA的核心不是Plan，而是Do.

**Do才是推进“状态变化”的关键动作**，而无论Plan也好，Check也好，都只是Do的双保险。

•对于新手，Plan 的价值不在于预测成功，而在于提前准备失败。

•对于高手，Plan 的价值不在于规定路径，而在于设计纠偏机制。

举一个生活中的例子：假如我希望减重40斤

新手的Plan（by AI）:

但高手在收集这些信息之后，不会直接按计划去落地和要求自己。

因为现实世界中存在着大量的不确定性：

•*连续运动，如何缓解身体疲劳？*

•*下雨天如何坚持运动？*

•*长期固定饮食产生厌食或报复性饮食怎么办？*

•*不同的运动，身体的耐力程度是否不同？*

•*饥饿，运动的时间消耗，疼痛...是否影响工作*

•*...*

在意识到这些不确定性之后，我的解决思路不是纠结于每周必须减多少体重，而是

•*先保证自己的作息：有固定的作息，才能安排足够的运动量*

•*再提升自己的运动量：有了运动习惯之后，不要着急控制饮食，而是先解决包括精力，体能在内的一系列问题*

•*基于作息，运动量，补剂，控制每天和每周的饮食*

•*把运动/饮食/体重数据作为反馈机制的输入，而不是每周必须实现的目标*

而我之所以愿意接受让自己慢下来，用“笨办法”，是因为我重新定义了problem：

1.**减肥这件事本质是：**

a.体重差 = 平均每日热量缺口  \* 总天数

b.热量缺口 = 摄入热量 - 运动消耗 - 基础代谢

2.**运动消耗 和 摄入热量的控制 不是两个数字**，它们在真实世界的锚点是运动，高质量睡眠和一日三餐

3.**减肥的受益人是我自己：**

a.健康的身体

b.充沛的精力

c.体型...

4.**因果链和能力支持** 见上方

所以，好的PDCA不是从Plan开始的，而是从正确定义Problem，以及找到可以落地执行的有效的Do开始的。因为：

1.问题足够小，足够简单，可观测，可理解，可回退

2.Check和Plan本质上是Do的补偿性行为，只有足够简单的循环才能够叠加这些补偿性行为

3.人在Do过程收集信息和建立连接的效率远高于Watch，而有清晰目标的Do则比被动的Do 效率更高。

有了这个视角，再来看之前 UI Design Skill 的例子的完整时间线：

1.感觉UI不重要，让AI随便搞就好，反正不影响使用

2.意识到UI的质量不可接受

3.用各种方式给了例子之后还是做不好的原因是上下文污染

4.用中间产物强约束，增加思考的深度，暴露更多的问题，做更细粒度的决策，把“凭感觉”的问题变成“可验证，可回退”的多个连续子问题

````Markdown
# Daily V1 /focus S1-S5 Frozen Decisions

状态：S1-S5 冻结稿
日期：2026-05-14
范围：冻结 `/focus/[timeNodeId]` 的 S1-S5 产品定位、开放问题结论、IA 和方案方向；不修改页面代码，不变更 DB schema。

## 0. Open Question Check

S1-S5 产品开放问题已关闭，可以进入 S6/S7。

剩余问题属于实现与验证阶段，不阻塞本轮冻结：

- 具体组件拆分。
- projection 字段命名。
- modal 字段细节。
- 移动端折叠方式。
- 日志追踪落点。
- 是否需要在实现中补充 index 或 schema migration。

这些问题进入 S6/S7 处理。

## 1. Frozen Positioning

`/focus/[timeNodeId]` 是现场推进工作台，不是通用项目管理页，也不是聚焦记录展示页。

核心定位冻结为：

```text
当前推进
-> 记录重要信息
-> 处理阻塞
-> 继承、编辑、沉淀、重组持续任务上下文
-> 推进状态或生成后续队列
```

其中，“记录重要信息”替代“记录证据”。证据只是重要信息的一类；现场中同样重要的还有决策、观察、会议结论、阻塞原因、人的状态、探索结果、实验记录和上下文重组。

## 2. S1 Discover / Context

### Project Facts

- `/time` 是时间编排 surface，用户在 `/time` 安排 `TimeBlock`，点击 block 进入 `/focus/[timeNodeId]`。
- 当前 `/focus` 已具备基础投影：`FocusRecord`、焦点对象、事件时间线、开放问题、review candidate、attention index。
- 当前命令可覆盖首版现场记录：`RecordAction`、`RecordObservation`、`RecordHumanState`、`RecordObjectStateChange`、`RaiseQuestion`、`createReview`。
- 当前数据层支持灵活事件：`events.payload_json` 可承载 typed payload。
- 当前已经有可索引的核心列：`subject_id`、`time_node_id`、`kind`、`lens`、`occurred_at`。
- 当前没有面向 payload 内字段的专门索引；高频查询字段必须在 S7 识别。

### Best Practice Inputs

- GTD：未分类输入先进可信 inbox；不要强迫现场立即完整建模。
- Jira：阻塞、状态、下一步和关键记录需要显式，否则任务无法恢复。
- Trello/Kanban：lane 能降低状态切换成本，但 `/focus` 不应膨胀为完整看板。
- Meeting notes：会议需要区分 summary、decision、follow-up、task。
- Research log：探索和实验需要记录假设、尝试、结果、结论、下一步。
- PDCA：没有 Explore / Experiment 支撑，Plan 质量不足。探索和实验在本模型中与 PDCA 节点同等重要。

## 3. S2 Requirements

### Must

- 首屏必须突出当前 `TimeBlock` 的推进目标、焦点对象、active lens、relation 和下一步。
- 允许多个并行推进项；现实执行不是纯线性。
- 必须提供 Capture Mode，作为记录重要信息的输入模式。
- Capture Mode 必须包含 Explore / Experiment；探索和实验是一等模式，不是 observation 的附属。
- 必须有阻塞处理入口，可按需转成 `Question`、`SubProblem`、`State` 或独立 `Problem`。
- 必须支持突发抢占当前推进，但需要二次确认，并提供“进入 inbox”的替代路径。
- 必须支持持续任务上下文继承、查询、编辑、沉淀、重组。
- 上下文编辑的边界是整理任务上下文和背景知识，不是重构任务本身。
- Context 相关内容先放 drawer，不污染主执行区。
- 会议记录必须支持 summary + structured fields，会议主体作为挂载对象，方便追踪。
- `/focus` 记录动作和现场重要信息；`/review` 对结果、流程、知识进行梳理和沉淀。

### Should

- Flow Lanes 需要出现，但默认可折叠。
- 拖动 item 触发状态变化时，应弹出 modal 补充必要信息。
- 状态转变时需要总结和确认。
- 重要信息/证据可以绑定 action，但不强制。
- 最近写入必须可追踪：写入了什么、挂到哪个主体、影响哪个后续入口。

### Could

- 支持 keyboard workflow。
- 支持按 capture mode、主体、状态、时间、lens 过滤。
- 支持用户标记“噪音太多”或“结果太多”，作为索引与交互降噪依据。

### Later

- 外部知识源连接。
- 全文搜索或 FTS。
- 多人协作、assignee、通知和 SLA。
- 重复模式自动生成 PDCA/Card candidate。

## 4. S3 Model / Journey

### Primary Journey

```text
进入 TimeBlock
-> 读取当前推进与并行推进项
-> 查询或整理必要上下文
-> 执行当前 step
-> 通过 Capture Mode 记录重要信息
-> 处理突发、未知或阻塞
-> 状态变化时总结确认
-> 继续推进、进入 inbox、生成后续项、进入 review 或回到 time
```

### Capture Modes

Capture Mode 是必要能力。它是输入控件模式和记录模板，不是默认新增 schema。

首版冻结这些模式：

- `Action`：记录动作、结果、下一步。
- `ImportantInfo`：记录重要信息、观察、判断、链接或片段。
- `HumanSignal`：记录人的状态、能量、阻力、清晰度、体验。
- `Blocker`：记录阻塞，并按需转成 `Question`、`SubProblem`、`State` 或 `Problem`。
- `Interruption`：记录突发；支持二次确认后抢占，或进入 inbox。
- `Meeting`：记录 summary、decision、follow-up、task、meeting subject。
- `Explore`：记录探索目标、线索、发现、开放问题。
- `Experiment`：记录 hypothesis、trial、result、conclusion、next step。
- `StateSummary`：状态转变总结和确认。
- `ContextEdit`：编辑、沉淀、重组任务上下文和背景知识。

### Flow Lanes

Flow Lanes 需要出现，但应是折叠式执行辅助，不是完整项目管理看板。

首版 lane 概念：

- `Active`：当前推进项，可有多个，并允许标记 primary。
- `Inbox`：突发、未分类、暂不打断当前推进的输入。
- `Blocked`：阻塞、未知、依赖、待决策项。
- `Context`：需要整理、沉淀、重组的上下文材料。
- `Logged`：已记录的重要信息。
- `ReviewReady`：需要进入 `/review` 梳理和沉淀的材料。

交互冻结：

- 默认折叠，不压主区。
- 展开后支持拖动 item 改变状态。
- 拖动触发状态变化时，弹出 modal 补充信息。
- 抢占当前推进需要二次确认，并保留“进入 inbox”的推荐选项。

### Context Control

持续任务上下文在 `/focus` 中承担多重角色：

- 继承：进入现场时恢复背景。
- 查询：按主体、历史、mode、状态、lens 查找。
- 编辑：修正上下文摘要、关键假设、约束、背景材料。
- 沉淀：把现场形成的背景理解保存为后续可重入材料。
- 重组：重新组织上下文，不重构任务本身。

承载方式冻结为独立 Context Drawer 或等价独立控件。

## 5. S4 IA / Interaction Strategy

### Surface Model

`/focus/[timeNodeId]` 的 surface 是：

```text
Live Execution Workbench
```

### Information Architecture

```text
FocusExecutionShell
  Header
    TimeBlock / time range / focus object / active lens / relation
    return to /time / open object / review block

  Current Progress
    primary progress item
    parallel progress items
    expected change
    current status

  Capture Dock
    Capture Mode switcher
    mode-specific fields
    subject binding
    optional action binding

  Collapsible Flow Lanes
    Active
    Inbox
    Blocked
    Context
    Logged
    ReviewReady

  Context Drawer
    inherited context summary
    editable background/context notes
    related history
    related Problem / CoreObject / Question
    query/filter by subject, mode, state, lens

  Recent Important Info
    latest writes
    linked subject
    status impact
    review entry
```

### `/focus` And `/review` Boundary

`/focus` 负责：

- 记录动作。
- 记录重要信息。
- 捕获阻塞、突发、会议、探索、实验。
- 编辑和整理现场上下文。
- 状态变化时做现场总结和确认。
- 生成后续项或 review-ready material。

`/review` 负责：

- 对结果进行梳理。
- 对流程进行复盘。
- 对知识进行沉淀。
- 把多条现场记录综合成候选结论、PDCA/Card candidate 或下一轮计划。
- 不从 `/focus` 的单条记录直接推断稳定知识。

## 6. S5 Prototype Direction

首版采用：

```text
Execution Console
+ Capture Dock
+ Context Drawer
+ Collapsible Flow Lanes
+ Recent Important Info
```

不采用完整 Kanban 作为主页面；Flow Lanes 是折叠式辅助。

不采用 Evidence-first Logbook 作为默认页面；日志能力通过 Recent Important Info 和 mode-specific history 承载。

## 7. Logging And Generic Index Plan

### Stage 1: Log Trace First

首版先做日志追踪，不急于新增 schema。

需要追踪：

- 单次加载返回 item 数量。
- 各区块返回 item 数量：progress、lanes、context、recent info。
- 用户展开/折叠 lane 的频率。
- 用户使用的 capture mode。
- 用户使用的过滤条件。
- 拖动 item 的来源 lane、目标 lane 和 modal 补充字段。
- 用户是否标记“噪音太多”或“结果太多”。
- 查询耗时和空结果次数。

这些日志用于判断哪里需要交互降噪，哪里需要索引支持。

### Stage 2: Generic Index Scheme

通用查询维度先按以下字段设计：

- `time_node_id`
- `subject_id`
- `kind`
- `lens`
- `occurred_at`
- `capture_mode`
- `item_status`
- `importance`
- `source_lane`
- `target_lane`
- `linked_action_id`
- `blocker_resolution_type`
- `interrupt_decision`
- `meeting_subject_id`
- `review_readiness`

当前 SQLite 结构天然支持前五类核心列。后续字段如果只用于展示，可留在 `payload_json`；如果用于高频查询、排序、过滤或聚合，应考虑生成列、专表、索引或 schema migration。

### Stage 3: Noise Reduction Policy

当出现以下信号时，再综合考虑交互 + 索引降噪：

- 单次返回数据过多。
- 用户频繁折叠某类信息。
- 用户反馈噪音太多。
- 查询延迟明显。
- 高频过滤条件依赖 payload 字段。
- review-ready material 难以定位。

降噪优先级：

```text
交互过滤 / 默认折叠
-> 更好的排序和分组
-> payload 字段提升为可查询字段
-> index / generated column / 专表
-> FTS 或更复杂搜索
```

## 8. Freeze Result

S1-S5 冻结通过。

冻结结论：

- `/focus` 是 `Live Execution Workbench`。
- 核心定位是当前推进、记录重要信息、处理阻塞。
- Capture Mode 是必要能力。
- Explore / Experiment 是一等 capture mode，与 PDCA 节点同等重要。
- Flow Lanes 需要出现，但默认折叠，作为执行辅助而不是完整看板。
- 支持多个并行推进项。
- 突发可以抢占，但需要二次确认，并提供 inbox 替代路径。
- 阻塞按需转成 `Question`、`SubProblem`、`State` 或 `Problem`。
- 持续任务上下文通过独立控件继承、查询、编辑、沉淀、重组。
- `/focus` 记录动作和现场重要信息；`/review` 梳理和沉淀结果、流程、知识。
- 首版尽量不新增 schema；先做日志追踪和通用索引方案，再根据噪音与查询需求决定是否迁移。

## 9. Knowledge Boundary

本文是 S1-S5 设计冻结 artifact，不是稳定 `.kb` source truth，不执行 Act，不应用 `.kbp`，不做 DB projection 或 schema migration。

如后续要把其中的模式沉淀为长期知识，需要经过 Check 和 Act-governor。
````

````Markdown
# Daily V1 /focus S6-S7 Final Design Handoff

状态：S6/S7 终版设计交接文档
日期：2026-05-14
依据：[Daily V1 /focus S1-S5 Frozen Decisions](./daily-v1-focus-rewrite-s1-s5-decisions.md)
范围：封闭 `/focus/[timeNodeId]` 的 UI 结构、验证脚本、实现切分、projection 需求、命令复用、日志追踪与索引检查；以 [focus-s7-static.html](./prototypes/focus-s7-static.html) 作为 HTML 终版视觉/交互依据；不做浏览器验证。

## 0. Discussion Status

S1-S5 已冻结。S6/S7 已完成终版 HTML 原型并回填到本文档。

本轮终版产物是静态 HTML 视觉/交互模拟，不包含后半部分表单模拟，不执行浏览器验证。

## 0.1 Closed Decisions

以下是本轮已讨论通过并封闭的 S6/S7 决策：

1. 首版实现目标采用：

```text
FocusExecutionScene
  = Current Problem Selector
  + Current Progress Panel
  + Capture Dock
  + Flow Board
  + Material Accordion
  + Context Drawer
  + Recent Important Info
```

2. Capture Mode 作为一等输入控件，不作为默认新增 schema。

3. Capture Dock 只记录现场材料，不承担“推进”动作。
   - `推进` 属于 `CurrentProgressPanel`，直接触发状态变化确认。
   - Capture Dock 默认继承全局选中的 `Problem / ProblemState`。
   - 默认模式建议为 `ImportantInfo`；若 lens 是 `researcher`，优先 `Explore`；若当前现场来自实验/探索，可保持上次模式。

4. Capture Mode 采用“结构化字段 + 自由文本”混合。

5. `Explore` 和 `Experiment` 完全分成两个模式。
   - `Explore` 是外部收集信息、确定问题边界。
   - `Experiment` 是动手拿结论进行剪枝。
   - 二者的思维模式、行为模式和目标不同。
   - 二者都应表现为可重入、可多次编辑的任务对象，而不是一次性长表单。

6. 状态可流转对象使用三栏 `Flow Board`，支持拖动 item 改变状态。

7. 拖动 item 发生状态变化时触发 modal 补充必要信息。

8. Context 相关能力优先放入独立 Context Drawer，不进入主区。

9. 不可流转材料使用 `Material Accordion`。
   - 状态可流转：`Active / Blocked / ReviewReady`。
   - 不可流转材料：`Inbox / Logged / Context`。
   - 不再做六栏对称分栏，也不保留左侧重复状态导航。

10. 拖到 `ReviewReady` 时弹 modal，review scope 默认继承当前 `TimeBlock + focus object`，用户可改。

11. `ContextEdit` 首版写成 event，payload 标记 `captureMode: ContextEdit`。

12. `Meeting` 是轻量会议对象，可补挂多个对象。
    - 不做成临时长表单等待用户一次性填完。
    - 首版可用 event/payload + 关联关系承载，不强制新增 `NodeKind`。

13. `SubProblem` 用 edge 表达。
    - `SubProblem` 的目的主要是在 review 阶段构建跨节点、更抽象/宏观的视角。
    - 子问题可能关联到另一个独立 `CoreObject`，例如 Agent 系统依赖第三方 LLM 接口。
    - 因此首版不新增 `NodeKind`，用 `problem` 节点和 parent/related edge 表达分工、依赖和抽象层级。
    - 增加 edge type：`problem.has_sub_problem.problem`。

14. `State` 转化：
    - 主体是 `problem` 时转为 `ProblemState`。
    - 其它主体先写一般 `StateSummary` event。

15. 日志追踪存文件，优先写 `.data/focus-execution-trace.ndjson`。
    - `.data/` 已被 `.gitignore` 忽略。
    - 日志不写业务 event，避免污染事实流。

16. 首版补低风险基础索引：
    - `events(time_node_id, occurred_at)`
    - `events(subject_id, occurred_at)`
    - `events(kind, occurred_at)`
    - `focus_records(time_node_id)`

17. 移动端降级策略：
    - `Flow Board` 从三栏变为垂直堆叠。
    - `Material Accordion` 保持手风琴。

18. `RecentImportantInfo` 默认显示最近 10 条。

19. S6/S7 封版前不让 AI 做浏览器验证。
    - 本轮已生成 HTML 呈现，但不执行 AI 浏览器验证。
    - 后续若实现成 React 页面，再用人工/协作方式走一轮视觉优化。

20. 首版尽量复用现有 command 与 `events.payload_json`。

21. 日志追踪先于 schema migration；只有出现高频查询、噪音或性能信号时，再考虑索引/生成列/专表/FTS。

22. 如果实现必须新增 indexed/generated fields、专表、FTS 或 DB migration，必须停下进入 schema/data contract gate。

23. `CurrentProgressPanel` 展示密度：
    - 主区显示 primary + 最多 2 个并行 `Active` 摘要。
    - 其余进入三栏 `Flow Board`。

24. 日志文件 schema：
    - `.data/focus-execution-trace.ndjson` 每行最小字段采用：`at`、`timeNodeId`、`event`、`counts`、`queryMs`、`captureMode`、`flowLane`、`materialGroup`、`noiseFeedback`。

25. 会议记录需要支持补挂多个对象。
    - 可关联当前 `Problem / ProblemState / CoreObject / Explore / Experiment` 等对象。
    - 不再把会议强制塞进单个 `ProblemState`。

26. 当前 `Problem / ProblemState` 的选中或切换只在一个全局位置展示。
    - 其它区域只表达“继承全局选择”。
    - 不在每个 box 重复展示当前问题，避免制造多套选择心智。

27. `CurrentProgressPanel` 内的 `推进状态` 是状态变化动作。
    - 它应映射到 `RecordObjectStateChange / CreateProblemState`。
    - 它不是 Capture Dock 里的记录项，也不需要“挂载到行动”。

28. “挂载到行动”不作为主交互。
    - 行动可以作为 event 被记录。
    - 若未来需要追踪某条行动，可作为可选引用字段或 event edge，而不是主路径。

29. 终版 HTML 原型路径：
    - `docs/prototypes/focus-s7-static.html`
    - 该文件是 S7 实现交接的视觉/交互基准。

## 0.2 Closed Open Questions

S6/S7 开放问题本轮已关闭：

- `CurrentProgressPanel` 展示密度：已定。
- 日志文件 schema：已定。
- `SubProblem` edge type：已定，新增 `problem.has_sub_problem.problem`。
- meeting state 区分字段：已定，需要。
- S7 HTML：已完成，作为终版视觉/交互依据。
- 浏览器验证：本轮不做。

后续若进入实现阶段，再另起实现计划与验证计划。

## 0.3 Final HTML Structure

终版 HTML 将 `/focus/[timeNodeId]` 收敛为一个 Problem-centric execution workbench：

```text
Top Bar
  - 时间路径
  - 返回时间页 / 打开对象 / 进入复盘页

Workspace
  - Current Progress Panel
  - Current Problem Selector
  - Capture Dock
  - Flow Board + Material Accordion
  - Recent Important Info
  - Context Drawer
  - State Transition Modal
```

关键布局冻结：

1. 不保留左侧状态 rail。
   - `推进中 / 收件箱 / 阻塞 / 上下文 / 已记录 / 待复盘` 的左侧导航已取消。
   - 状态数量在看板或手风琴内部展示即可。

2. `Current Problem Selector` 是唯一的问题选择/切换位置。
   - 展示当前 `Problem`、当前 `ProblemState`、关联核心对象、子问题数量和状态历史入口。
   - 其它面板只继承它，不重复展示当前问题。

3. `Current Progress Panel` 是推进状态的主入口。
   - 主推进 + 最多 2 个并行摘要。
   - 每个推进卡片提供 `推进状态`。
   - `推进状态` 触发状态变化确认，不进入 Capture Dock。

4. `Capture Dock` 是现场材料记录器。
   - 模式组：`认知` 与 `现场`。
   - `认知`：`ImportantInfo / Explore / Experiment`。
   - `现场`：`Blocker / Inbox / Meeting / HumanSignal / ContextEdit`。
   - 保存动作是“保存材料”，默认继承全局选中的 `Problem / ProblemState`。

5. `Flow Board` 只承载可流转对象。
   - 三栏：`Active / Blocked / ReviewReady`。
   - item 可拖动。
   - 拖动改变状态时打开 `StateTransitionModal`。

6. `Material Accordion` 只承载不可流转材料。
   - 手风琴组：`Inbox / Logged / Context`。
   - 这些材料用于记录、查询、整理，不作为状态卡片拖动。

7. `Context Drawer` 与主区选中项联动。
   - 展示当前选中推进项的关联 `Problem / ProblemState / SubProblem / CoreObject / Meeting / history`。
   - 支持大量关联对象滚动，不假设只有少量上下文。

## 0.4 Confirmation Flow And Control Set

终版 HTML 增补 `确认流程与控件样式` 区域，用于评估 `/focus` 首轮需要的表单负担。该区域是静态表单，不提交，不新增 schema。

表单/控件样式参考 `/time` HTML 的控件实验区：

- `form-card`：分为普通、`lean`、`heavy`。
- `form-fields`：两列字段，移动端降级为单列。
- `stepper`：用于低频确认流程，显示步骤进度。
- `choice-row / choice`：用于可选引用、复盘候选、生成后续项等 checkbox 控件。
- `select / input / textarea`：用于状态、优先级、去向、摘要、总结、验收约束。

本轮 HTML 中先补齐 4 类确认/上下文表单样式：

1. 状态变化确认。
   - 入口：`推进状态` 按钮或 `Flow Board` 拖动。
   - 字段：目标状态。
   - 说明：原状态、主体、时间块、相关引用自动继承，不要求用户补长文本。
   - 写入：`RecordObjectStateChange / CreateProblemState`。

2. 保存现场材料。
   - 入口：`CaptureDock`。
   - 字段：模式、自动关联、摘要、内容。
   - 说明：默认自动关联当前行动；没有行动时关联全局选择，用户只在必要时改关联。
   - 写入：`RecordObservation / RecordHumanState / recordEvent` 等记录类 command。

3. 阻塞转化。
   - 入口：`Blocker` capture 或 `Blocked` lane item。
   - 字段：阻塞描述、转化类型、处理优先级、下一步。
   - 结果：转 `Question`、`SubProblem edge`、`ProblemState` 或独立 `Problem`。

4. 切换全局选择。
   - 入口：`CurrentProblemSelector`。
   - 字段：选择主体、自动结果提示。
   - 说明：选择即自动保存并刷新关联面板，不弹表单确认，不默认写业务 event。

同时新增 `记录工作台模式字段` 区域，补齐 Capture Dock 各模式的差异字段：

1. `ImportantInfo`。
   - 字段：信息类型、重要度、一句话摘要、详细内容、保存去向、引用。
   - 目的：最高频低摩擦记录，进入最近重要信息或已记录材料。

2. `Explore`。
   - 字段：探索任务、阶段、下一次更新、本次更新。
   - 目的：先创建可重入探索任务，后续多次更新线索和边界，不直接形成稳定结论。

3. `Experiment`。
   - 字段：实验任务、实验状态、下一步、本次结果。
   - 目的：先创建可重入实验任务，随着试验过程持续追加结果。

4. `Meeting`。
   - 字段：会议标题、快速摘要、补挂对象。
   - 目的：快速保存轻量会议对象，再按需补挂多个对象。

5. `HumanSignal`。
   - 字段：能量、清晰度、阻力、情绪、备注。
   - 目的：记录人的状态信号，不改变问题状态。

6. `ContextEdit`。
   - 字段：整理对象、整理动作、当前内容、整理结果。
   - 目的：明确整理背景摘要、设计决策、关联对象、查询线索或材料归档，不重构任务本体。

7. 快速收集 `Inbox / Problem`。
   - 字段：内容、创建为、是否影响当前推进。
   - 目的：突发不是独立概念，本质是添加一个 `Inbox` 或 `Problem`，再决定是否影响当前推进。

右下角 `StateTransitionModal` 也升级为三步确认：

```text
拖动 -> 补充 -> 写入
```

它默认继承当前 `TimeBlock + 全局选择`，只允许在确认前调整目标状态。

## 1. S6 Journey Test Script

### Script A: 进入现场并推进多个并行项

目标：验证 `/focus` 不假设纯线性执行。

步骤：

1. 从 `/time` 点击一个 `TimeBlock` 进入 `/focus/[timeNodeId]`。
2. 页面显示 primary progress item。
3. 用户查看 `Flow Board`。
4. 用户看到多个 `Active` item，其中一个标记为 primary。
5. 用户在主推进卡片点击 `推进状态`。
6. 系统打开状态变化确认 modal。
7. 用户确认后写入新的 `ProblemState`。

通过条件：

- 当前推进不被记录表单淹没。
- 多个并行推进项可见但不抢主区。
- 状态变化进入当前问题状态历史。
- Recent Important Info 只更新相关重要材料，不承担推进状态本体。

### Script B: 快速收集到 Inbox / Problem

目标：验证突发事项不会形成独立概念，而是进入 Inbox 或 Problem。

步骤：

1. 用户使用快速收集入口。
2. 用户输入内容。
3. 用户选择创建为 `Inbox` 或 `Problem`。
4. 系统自动保存。
5. 若用户标记影响当前推进，再把它转为阻塞或切换全局选择。

通过条件：

- 突发默认不抢占当前推进。
- 新增对象可追踪、可稍后处理。
- 只有明确影响当前推进时才改变状态或选择。

### Script C: 阻塞转化

目标：验证阻塞能按需转成合适对象。

步骤：

1. 用户使用 Capture Mode `Blocker`。
2. 用户填写阻塞原因和影响。
3. 用户选择转化类型：`Question`、`SubProblem`、`State` 或 `Problem`。
4. 系统弹出对应 modal 补充必要字段。
5. 写入后 item 进入 `Blocked` 或 `ReviewReady`。

通过条件：

- 阻塞不是死文本。
- 转化类型不强迫提前建模。
- 后续对象能从相关工作区或 review 找回。

### Script D: Explore / Experiment 支撑 Plan

目标：验证探索/实验不是 observation 的附属。

步骤：

1. 用户创建或打开一个 `Explore` 任务。
2. 追加本次线索、边界判断或开放问题。
3. 用户创建或打开一个 `Experiment` 任务。
4. 追加本次试验结果或剪枝结论。
5. 用户在后续状态变化确认或 `/review` 中引用这些任务对象。

通过条件：

- Explore / Experiment 是可重入、可多次编辑的任务对象。
- 结果不直接变成稳定知识。
- 它们能支撑后续 Plan 或 review。

### Script E: 会议记录与关联主体

目标：验证会议能形成可追踪材料。

步骤：

1. 用户创建轻量 `Meeting` 对象。
2. 先快速记录标题和摘要。
3. 用户按需补挂多个对象。
4. 写入后可从相关对象、Recent Important Info 或 review 找回。

通过条件：

- 会议不只是长文本。
- 会议对象可补挂多个对象，可追踪。
- follow-up 能进入 `Flow Board`、`Material Accordion` 或 review。

### Script F: Context Drawer 整理上下文

目标：验证持续任务背景能被继承、查询、编辑、沉淀、重组。

步骤：

1. 用户打开 Context Drawer。
2. 查看 inherited context summary。
3. 按 subject、mode、state 或 lens 查询历史材料。
4. 使用 `ContextEdit` 修改背景摘要或重组上下文。
5. 返回主推进区继续执行。

通过条件：

- Context 不污染主区。
- 编辑的是上下文和背景知识，不是重构任务本身。
- 编辑结果后续可重入。

### Script G: 状态转变总结确认

目标：验证状态变更不只是随手覆盖。

步骤：

1. 用户在 `CurrentProgressPanel` 或 `Flow Board` 触发状态变化。
2. 系统展示相关 action / important info 作为可选引用。
3. 用户填写状态转变总结。
4. 用户确认状态转变。

通过条件：

- 状态变化需要总结和确认。
- 证据/action 绑定可选但可见。
- 结果写入 `ProblemState`，并进入状态投影或 review-ready。

## 2. S7 Implementation Target

首版实现目标：

```text
FocusExecutionScene
  = Current Problem Selector
  + Current Progress Panel
  + Capture Dock
  + Flow Board
  + Material Accordion
  + Context Drawer
  + Recent Important Info
```

不要把旧 `/focus` 还原为：

- `SurfaceBrief` 可见说明。
- 多个并列 command form。
- 常驻重型 inspector。
- 关系、timeline、review candidate 平铺。
- 左侧重复状态 rail。
- 六栏等宽分栏式 lanes。

## 3. Component Handoff

建议新增或改造以下组件：

- `FocusExecutionScene`：替代当前 `FocusScene` 的页面编排。
- `CurrentProblemSelector`：唯一展示和切换当前 `Problem / ProblemState` 的位置。
- `CurrentProgressPanel`：显示 primary progress item 和 parallel progress items。
- `CaptureDock`：承载 Capture Mode switcher 与模式字段。
- `FlowBoard`：三栏状态看板，承载可流转对象，支持拖动和状态 modal。
- `MaterialAccordion`：承载不可流转材料，使用手风琴展示 `Inbox / Logged / Context`。
- `FocusContextDrawer`：继承、查询、编辑、沉淀、重组上下文。
- `RecentImportantInfo`：显示最新重要信息和后续入口。
- `StateTransitionModal`：状态总结与确认。
- `QuickCapturePanel`：快速新增 `Inbox` 或 `Problem`。
- `BlockerTransformModal`：阻塞转 `Question` / `SubProblem` / `State` / `Problem`。

可复用现有资源：

- `CommandComposer` 的提交逻辑可被拆给 `CaptureDock`。
- `EventTimeline` 可作为 Recent Important Info 的底层展示资源。
- `RelationSlot` 和 `AttentionIndex` 降级到 Context Drawer 或 supporting panel。
- `buildFocusScene` 继续作为数据入口，但需要扩展 projection。

## 4. Projection Handoff

`FocusSceneProjection` 首版建议扩展为：

```ts
interface FocusExecutionProjection {
  currentProblem: CurrentProblemProjection | null;
  progressItems: FocusProgressItem[];
  primaryProgressItemId: string | null;
  captureModes: CaptureModeProjection[];
  flowBoard: FlowBoardProjection;
  materialAccordion: MaterialAccordionProjection;
  contextSummary: FocusContextSummary;
  contextItems: FocusContextItem[];
  recentImportantInfo: ImportantInfoItem[];
  queryTrace: FocusQueryTrace;
}
```

候选字段：

```ts
type CaptureMode =
  | "ImportantInfo"
  | "HumanSignal"
  | "Blocker"
  | "Inbox"
  | "Meeting"
  | "Explore"
  | "Experiment"
  | "ContextEdit";

type FlowBoardLane =
  | "Active"
  | "Blocked"
  | "ReviewReady";

type MaterialAccordionGroup =
  | "Inbox"
  | "Logged"
  | "Context";
```

状态推进不进入 `CaptureMode`。它由 `CurrentProgressPanel` / `FlowBoard` 触发 `RecordObjectStateChange` 或 `CreateProblemState`。

## 5. Command Handoff

优先复用现有命令：

- `RecordAction`
- `RecordObservation`
- `RecordHumanState`
- `RecordObjectStateChange`
- `RaiseQuestion`
- `createReview`
- `node.create`
- `edge.create`

首版 typed payload 建议：

```json
{
  "captureMode": "Experiment",
  "itemStatus": "Logged",
  "importance": "high",
  "linkedActionEventId": null,
  "sourceGroup": "Inbox",
  "targetGroup": "Logged",
  "reviewReadiness": "candidate"
}
```

说明：

- `linkedActionEventId` 只是可选引用，不是主交互。
- 记录材料默认以当前全局选择的 `Problem / ProblemState` 为主体。
- 状态变化不写 `captureMode: StateSummary`，而是通过 `RecordObjectStateChange / CreateProblemState` 写入 `ProblemState + Event`。

模式特有字段留在 payload：

- `Explore`: `taskTitle`、`stage`、`nextUpdate`、`updateNote`
- `Experiment`: `taskTitle`、`experimentStatus`、`nextStep`、`resultNote`
- `Meeting`: `title`、`quickSummary`、`attachedObjectIds`
- `Blocker`: `reason`、`impact`、`resolutionType`
- `Inbox`: `content`、`createAs`、`impactDecision`
- `ContextEdit`: `contextItemType`、`before`、`after`、`rationale`

状态变化字段进入 `CreateProblemState / RecordObjectStateChange`：

- `fromState`
- `currentState`
- `expectedChange`
- `summary` / `note`
- `steps`
- `acceptanceConstraints`
- `confirmed`

## 6. Logging And Index Check

### Log Trace

实现阶段必须先记录查询和交互日志，用来判断是否需要索引或交互降噪。

日志落点：

```text
.data/focus-execution-trace.ndjson
```

`.data/` 已被 `.gitignore` 忽略。该日志是开发与优化 trace，不写入业务 event，不作为稳定事实。

最低追踪项：

- `at`
- `timeNodeId`
- `event`
- `counts`
- `captureMode`
- `flowLane`
- `materialGroup`
- `queryMs`
- `noiseFeedback`

可选扩展项：

- `filterKeys`
- `dragSourceFlowLane`
- `dragTargetFlowLane`
- `modalType`

### Generic Index Check

实现前检查是否已有索引覆盖：

- `events(time_node_id, occurred_at)`
- `events(subject_id, occurred_at)`
- `events(kind, occurred_at)`
- `events(lens, occurred_at)`
- `focus_records(time_node_id)`
- `edges(time_node_id)`
- `edges(source_kind, source_id)`
- `edges(target_kind, target_id)`

如果没有，不一定立刻迁移；但需要在 S7 risk 中记录。

### Migration Stop Point

若实现发现必须新增 indexed/generated fields、专表、FTS 或 DB migration，必须停下并单独做 schema/data contract gate。

## 7. Validation Commands

实现后至少运行：

```bash
npm run lint
npm run test
npm run build
git diff --check
```

本轮已生成 HTML 终版呈现，不执行 AI 浏览器验证。

若后续进入 React 实现封版，可基于 HTML 终版走人工/协作视觉优化。

检查点：

- 首屏不是信息墙。
- Capture Mode 可见。
- Explore / Experiment 是一等模式。
- 状态可流转对象使用三栏 Flow Board。
- 不可流转材料使用 Material Accordion。
- Context Drawer 不污染主区。
- 状态变化有总结确认入口。
- 突发事项通过快速新增 `Inbox / Problem` 处理，不作为独立概念。
- 左侧不保留重复状态 rail。

## 8. Knowledge Retention Plan

当进入实现阶段并完成一个可验证变更批次后，写 workflow evidence：

- when：完成 `/focus` 页面结构或核心 projection 扩展后。
- do：记录 Do/Check 结果。
- command：`kbl workflow write --json --stage Check --task-id focus-time-e62b5bb845ae4cdd-rewrite --summary "<中文验证摘要>"`
- inputs：S1-S5 冻结稿、S6/S7 封闭文档、实现 diff、验证命令结果。
- evidence：通过/失败命令、未解决 gap。
- write target：`.codex/kbl/workflow/<date>/<id>.kbl`。
- granularity：一个可验证页面重构批次。
- acceptance：验证命令通过，journey scripts 不被破坏，未执行 schema migration 或 stable promotion。
- Act boundary：不执行 Act，不 apply `.kbp`，不修改 stable `.kb`；如需 schema migration 先停下。
````

5.Skill化需要考虑的问题

•*在不同场景下按不同的处理流程完成任务*

◦项目初始化阶段，根据项目功能确定统一的设计风格，样式库，组件库

◦具体页面设计

◦页面重构/调整

•*Skill本身的渐进式披露*

•*结果导向的强流程控制*

•*资源/过程文档管理*

总结一下，对于新手来说，从0开始的PDCA循环演化过程简化之后，大概是这样的：

•**Step1**: Do

•**Step2**: Do -> Check

•**Step3**: Plan -> Do -> Check

•**Step4:** Plan -> Do -> Check -> Action -> ...

## 提升篇

在前面4个环节中，我们一直接受了自己是新手。但是，我们内心深处是不是会有这样一个声音：“我们难道甘愿当一辈子新手吗？”hhh

在PDCA循环中，需要通过Act不断调整循环，而有效的Act一定需要更高的视角，才能从整体对整个PDC过程进行审视和纠偏。那么，“更高的视角”到底是什么？从何而来？

【互动🙋🏻】有同学能回答出这个问题吗？

————

### 更高阶的审美来自于对更底层规律的理解和整合

本来想展开写点什么的，思索了半天之后，还是请出一堂的《全员必修：重新理解科学理念》Y模型吧。

这是一堂Y模型的相关示意图，主题为“科学成事道路”，核心是“我的认知”，标注有“实事求是 解放思想”，认知通过知行合一向下连接“解决真正问题”。认知的来源有两个方向，一是从理论端，通过提炼建模、科学类比形成认知；二是从事实端，通过假设驱动、定性定量形成认知。该图出现在文档介绍《全员必修：重新理解科学理念》Y模型的部分，用于辅助说明AI时代需先理清底层认知规律的相关内容。

这里最需要警惕的，只有一点：

***我让AI总结和整理的认知不是我的认知！***

当我们和AI聊天，很容易产生各家厂商的大模型各个都是人才，说话还好听的错觉。尤其是和GPT聊天的时候，经常能看到GPT用几个自创的词汇和精妙的类比，就把你半天说不清楚的想法表达的特别清楚。

但是我想提醒大家的是，AI根据你提供的素材，尝试理解推演、并帮你理清了想法，**不代表你真的想清楚了**。

AI 在某些方面非常强大，但这个强大是不是属于你，要打个问号。你可能是感觉会了，或者眼睛会了，但手不一定跟上了。

如果再补充一点，前面我们区分了question和problem， 然后后面的章节就一直围绕problem进行展开，而且还反复强调，一定要解决真实的problem。**那么是不是说question不重要呢？**

【🙋🏻‍♀️划重点】优先解决problem是因为，**problem是让你持续掉血的debuff，problem不仅不会自动消失，还有可能不断恶化和扩散。**

当problem被清理的差不多之后，我们就需要重新审视整个问题空间，重新提出problem了。

【🌰举例子】这里我举一个例子，来展示一下question的力量。

我虽然在AI俱乐部做了3次分享，但在我看来，我的分享还是处于“萌新”水平。

现在，我们按之前定义problem的方式，重新描述一遍problem：

**•状态变化**

◦*梳理故事线的速度 ↑， 返工率 ↓*

◦*案例的数量，质量 ↑*

◦*把抽象的概念讲生动 ↑*

◦*情绪调用和表达张力 ↑*

**•真实锚点*：*** *AI俱乐部， 拆书会？ 线下分享？ 自媒体？...？*

**•受益人*：*** *我，于老师，一堂同学   ->  多要反馈*

**•因果链和能力支持*：***

◦*案例来自于平时积累*

◦*情绪调用和表达张力；把概念讲生动可以靠和AI多讨论*

但是，怎么样快速找到一个看起来**靠谱的故事线**？ 怎么样保证抽象的故事线把知识和案例串起来之后一定是顺的？

而且，真实的讲一节课，准备成本和失败的代价都是很高的。

这些problem看起来并不是直观可解的。

•“备课” 这个复杂流程，存不存在一个 “**等效缩放**”？

•我的“备课”过程**本质**是在做什么什么？

•把我自己思考和解决问题的思维模式提炼成**方法论**

•有没有办法通过回答一系列**独立问题**，让方法论更容易被理解，接受和学习？

•如果我想要学会一个**新的技能**，我会关注什么？

**实质问题**：

 1.*如何对问题提纯和聚类   ->  筛选备选案例*

2.*怎么识别这类问题      ->   找可识别的特征*

3.*解决这类问题的通用过程是什么？  ->   提炼方法和工具*

4.*如何泛化这些问题      ->   找问题的应用场景和边界*

5.*怎么提升解题的效率  ->   方法的易错点在哪里？ 如何刻意练习？*

**包装问题**：

 1.*备选案例中，哪几个问题产生的影响最容易引起共鸣？*

2.*如何通过外化解决前后的效果，提升价值感？*

最后，如何对上述问题进行整合？

在这个纯粹的思考过程中，每一次提问，都是在切换看待问题的角色，视角，颗粒度...

而看问题的视角越多，获取的信息就越全面，信息越全面就越容易从中找到问题的模式和结构。

最后，哪怕得到了一个看似“靠谱”的答案，也要回到现实世界中进行验证。

 1.*建池子，并且把流程融入到每日的信息收集和复盘中去*

2.*验证 案例池  ->  方法论 链路是不是能打通*

3.*打磨10-15分钟的案例块*

4.*验证方法论 + 案例块  对打磨故事线确实有正向作用*

5.*找到一个出口，形成稳定的PDCA*

### 学习必须遵守的两个客观规律： i+1 原则  和 必要难度

【思考🤔】AI时代来临后，是不是人就不再需要学习了？

我的观点可能比较悲观，**AI时代反而对学习能力，尤其是自学能力提出了更高的要求。**

AI来临之后，大量替代了新人的工作岗位，新人的学徒晋升路径被AI彻底切断了。而人脑也比想象中更喜欢偷懒。

 《思考，快与慢》中介绍过，**思考过程调用的“系统二”远比自动驾驶的“系统一”更加耗能，**而大脑运作的第一目标就是节约能量

AI目前虽然可以给出“看起来非常正确”的方案，但还做不到独立给出“正确高效”的方案。 人与AI协作的过程中，依旧**需要高水平的人来引导和补充背景信息，审查方案，做高风险决策以及把控方向**。

但是，**人的审美是不可能自然而然提升上去的。必须通过不断学习才能把水平提升上去**。而且，AI进步的速度越快，生成的速度越快，对人的学习速度的要求就越高。

**“i+1 原则”**（又称“可理解性输入”理论）是著名语言学家史蒂芬·克拉申（Stephen Krashen）提出的一种高效学习法。**在该理论中，i 代表你当前的语言水平，+1 代表略高于你现有能力、但通过语境可以理解的新知识，旨在实现“跳一跳能够得着”的黄金学习区。**

**必要难度理论**（Desirable Difficulty）由心理学家 Robert 和 Elizabeth Bjork 提出，**指在学习过程中人为增加适度认知挑战**。这虽会减慢即时学习速度，却能触发深层认知加工，大幅提升长期记忆、知识提取与灵活应用能力。

而这两个理论放在一起正好“夹逼”出了刻意练习中的非舒适区：

我们在三个不同的场景看到了相似的模式：

1.在过去，架构师必须写代码，除非你是“PPT架构师”

2.而最近一个更有意思的新闻是大量顶尖CTO级别的研究院，低薪入职Anthropic做最基础的研发工程师

3.在数学学习中，无法直接学习最上层的抽象概念，跳过中间层，高阶抽象来自于对低阶抽象的熟练掌握

这意味着： 如果我们未来想要持续驾驭AI，我们就不能把所有的工作全部交给AI，而是**必须保持手感，持续脱离舒适区，持续给自己上强度。**

在双三角模型的循环中，有两条线， 我们前面讨论的所有内容，对应的都是人如何调教AI的那条线。

但对于AI辅助人的这条线其实并没有讨论。

我的理解是：**这个循环并不是自然而然能够打通的，**因为两条不同的曲线中，人和AI所扮演的角色是完全不同的**。**

在上面的线中，现实中的大量案例都是，人要提升自己的管理能力，把AI当做员工。

而在下面的曲线中，**AI必须化身最严厉的教练，督促人的不断反思和学习，并给人设计进步的i+1阶梯**。

## **结语： 适可而止**

**之前4个月，我几乎每天都在高强度AI，甚至可以说患上了“*AI综合症*”。**

**结果是每天一有想法就立刻丢给AI，让AI去验证，拿结果。 但**现在回过头去回忆这段时间，感受是只记得自己大概做了什么，思路是什么。但是对于遇到了哪些问题，解决方案是什么，决策点是什么，这些*本应该在大脑中留下最深刻印象的东西没有什么概念*。

而且大脑持续接受强刺激，昼夜颠倒，透支了身体。

**这不太好。**

我的经验数值是，每天用3-4小时AI，身体可以保持比较好的状态。多了就会影响睡眠和思考。 #benchmark

**不是不用AI，不是拒绝AI**，而是**让自己有选择用或者不用的权利**，在不牺牲自己身体的前提下，和AI一起协作，共同解决高价值的问题。

谢谢大家，我是纪浩，感谢大家坚持听到了最后\~

# 作业和Candy

## 本次作业

**初阶题目：什么值得学**

听完这次分享，你觉得在 Agent 时代，哪些能力还必须由人来学、来练、来保持手感？

请结合你自己的一项能力或工作习惯，说说这件事为什么不能完全交给 Agent，你现在和 Agent 的差距在哪里，以及你准备怎么继续练这件事

**进阶题目：问题分辨**

请你描述一个最近被你注意到的目标、冲动或想做的事，结合分享内容，试着判断它更像是 problem 还是 question，并说明理由。

给你一些思路：

•这个问题的前后状态是什么

•现实世界里的真实锚点是什么

•谁是受益人

•你为什么认为它值得现在就开工，或者为什么暂时不值得

**高阶题目：防御性设计**

这是一道选做题。选择一个你打算让 Agent 协作完成的真实任务，写一份「开工前检查清单」。

•请尽量包含：你要让 Agent 做什么，准备提供哪些上下文，会设置哪些检查点

•可以尝试写：哪些结果一旦出现就要暂停或回退，你会怎么降低翻车概率，等等

## 本期Candy

【作业礼包🎁】这节课的课后Candy：

1.纪浩私藏AI能力自查 + 建议的skill

2.纪浩调试skill的聊天过程markdown文件

【Flag🙌】这节课做起来很辛苦，希望大家不要辜负。

来来来，希望大家一起立一个Flog（承诺），认真听课吸收，最后完成这次练习作业。

扣一句话吧：一定作业！！

**看回放/逐字稿的同学**，**也要交作业啊！**你们的反馈真的很重要。

点击作业链接：https://yitang.top/activity/YlQ6a1e9012a62f2/edit

或扫描下方二维码完成作业\~\~

截止时间：**2026年6月9日（周二晚）24:00**

一定挑战，一定作业！\~

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI俱乐部周三LIVE](../01-AI认知与基本功/05-AI俱乐部周三LIVE.md)

---

<details>
<summary>原文配图上的文字（53 条，图片本身未随文提供）</summary>
- 「重讲清单体笔记」 「用最小的笔记训练最大的解题能力」

**纪浩在AI任务开始之前**

- 「一堂YiTang.top AI俱乐部」 「落地Live」 「AI落地Live第57场 一起来用AI啊~」
- 「一堂YiTang.top AI俱乐部」 「AI落地Live」 「AI落地Live第69场 一起来用AI啊~」
- 「AI时代的问题重构」 「AI落地Live」 「AI落地Live第79场 AI时代的问题重构」
- 这张图对应文档中AI落地相关的内容，展示了从Plan-Act-Review循环到Goal-Run的模式，核心是Plan、Act、Review三个环节形成闭环循环：Plan是基于需求收集分析形成执行计划，Act是按计划逐步执行得到结果，Review是对AI产出进行审查确认正确性，三个环节通过箭头形成循环，该图补充说明了文档中提及的AI任务相关的模式，帮助理解相关工作逻辑
- 「翻过一个墙，最好的方式，就是先把自己的鞋子，勇敢扔过去」 「欢迎立Flag：勇敢把自己的鞋子扔过去」 「要拥有敢于尝试、果断行动的勇气」
- 「准备篇」 「在与AI协作的过程中，我的水平如何？我究竟是新手还是高手？」

**最核心的问题在与AI协作的过程中我究竟是高手还是**

- 「在与AI协作的过程中，我究竟是高手还是新手？」
- 「弱小不是生存的障碍，傲慢才是」
- 「本机探针」 「基础入口」 「当前状态」 「公司隧道」 「启动：失败」 「做出来的东西」
- 「最近任务」 「completed」 「第1个高质量程序代码量与LMA相关性指标任务」 「Thread started」
- 「用户反馈」 「最近提交未通过的测试」
- 「发布者」

**开始动手前必须想清楚的第二个问题你要解决的问题究**

- 「你要解决的问题，究竟是problem？还是question？」 「创业课」
- 「NPC」 「用上Agent后，每天感觉自己很兴奋，脑子里有无数个点子，Agent烧了无数的token，但好像并没有做出什么有用的东西」 「problem」 「question」
- 「只是在提出question，没有解决真正的problem」
- 「发布者」 「Unlisted」 「Skill Marketplace Assistant」 「Agent如需搜索、评估、下载、管理及反馈marketplace中的skill」 「最新版本」
- 「管理员」 「用户管理」 「邀请管理」 「标签管理」 「Skill状态」 「Token管理」 「推荐位」 「审计日志」 「skill.upload」

**起步篇**

- 「起步篇」 「纪浩：在AI任务开始之前」

**上手解题的第一个问题工作空间的准备**

- 「工作空间的准备」 「以太旗」 「MVC」 「uble Clas」 「上手解题的第一个问题：工作空间的准备」
- AI落地案例中系统自述、领域知识、ForAgent、导学台、Agent工作手册、工具箱、经验与模式库、任务管理、目标等关注点的表格。表格包含关注点、例子、增长速度、缺失时的影响、一定be等列，如系统自述关注记录系统内容，一定be为项目架构文档；领域知识关注系统所服务的领域相关知识，一定be为项目架构文档等。该表
- 这张图表呈现了复杂项目知识的五层结构，左侧依次为项目、问题域、问题约束/工具/经验、任务状态、日志五个层级；中间列标注各层级对应的边界属性，其中问题约束/工具/经验被高亮标注，其边界为Agent直接关注和使用的知识和工具；右侧列标注各层级与Problem澄清过程的关联关系，分别是项目的关联关系无明确标注、问题域为现实锚点、问题约束/工具/经验为因果链和能力支持、任务状态为前后状态对变化、日志无明确

**上手解题的第二个问题如何从0开始PDCA**

- 「如何从0开始PDCA」 「MVC」 「uble Clas」 「上手解题的第二个问题：如何从0开始PDCA」
- 新手在AI任务开始前减重40斤的Plan，包括每日饮食、运动、睡眠、体重记录等。每日饮食方面，500 kcal、600 kcal、700 kcal对应不同食物摄入量；运动方面，有慢跑、快走、跳绳等不同运动方式及对应时间；睡眠方面，建议7 - 8小时；体重记录方面，每周记录一次。该图片
- 「太丑了！」 「太丑了」
- 「求求你把样式好好搞一下，不是所有的东西都必须用和boder包起来」 「boder」
- 「最近材料」 「切换后关联测试 stable ImportantInfo / observation.recorded」 「1 ImportantInfo / observation.recorded」
- 「推进中」 「待复盘」 「旧页面 -> 新路由并需执行并记录信息的页面」 「优化time - > focus流程，从Active转到Blocked」 「用各种方式给了例子之后还是做不好的原因是上下文污染」
- 「Daily系统 / focus 聚焦重构」 「迭代时间线（以Reonce为例）」 「importantable（左侧测试是enable）」 「切换到测试editstate」
- 「感觉UI不重要，让AI随便搞就好，反正不影响使用」 「这是一条Passionless错误的结论」
- 「PDCA循环+迭代」
- 「我建议不要再去加‘规范’，而是加一个更硬的东西：产品意图优先级约定。它要比代码、Prompt、历史实现都高」
- 「凭感觉」 「可验证、可回退」
- UI Design Skill的完整时间线，分为5 - 10个阶段，包括Discover / Context、Define / Requirements、Design Thinking / MIG、Build / Prototype、Implement / Handoff、Measure / Evaluate等。还列出了关于Pattern / Component、关于UX / UI、关于实现流程、
- AI设计相关资料，包括gpt-pk - design - artifacts.md、gpt-pk - prototype - evaluation.md等文件，以及gpt - pk - design - artifacts. md文件的前10个字符。下方是关于AI设计的讨论，有人提到AI设计的挑战，如AI无法理解上下文、AI设计的原型无法直接用等；也有人分享了AI设计的成果，如AI设计的原型、AI

**8KnowledgeRetentionPlan**

- 「上午聚焦：降低记录与恢复上下文摩擦」 「UI设计」 「交互设计」 「视觉设计」
- 一段关于AI技能化讨论的对话内容。对话中提到在docs目录下设计规范文档和模板，分析能否做成技能，认为可简化成三个阶段：P1 - P4梳理业务流程，P5 - P7具体细节，以及HTML预览和调整。交互风格需在无开放问题时给出冻结稿确认，有开放问题时在对话中输出开放问题并给出建议方案。问题类型分为初始风格定稿、具体页面设计、页面调整/重构三类。最后指出可做成技能，现有文档支撑度高，建议对外简化内保细
- 是与AI相关的Skill落地分析内容，围绕Skill的设计与应用展开。图片中明确给出了Skill应承担的三要件，分别是项目设计阶段管控、文档生命周期管理、新参考知识入口，后续还对Skill相关问题进行梳理判断。内容包含对Skill设计的相关问题设问，如是否Hold住常见用户设计场景和相关问题，还指出可通过中间文档延迟类hint让AI产生幻觉，同时辅助实现过程控制以保证质量稳定，最终对Skill设计
- 是纪浩在AI落地Live79活动中分享的文档内容。文档中详细介绍了UI Design Skill的完整时间线，包括感觉UI不重要、意识到UI质量不可接受、用各种方式给例子但做不好、用中间产物强约束、Skill化需要考虑的问题等环节。还列出了Skill化时需考虑的4个参考维度，如设计流程、设计风格、设计质量、设计结果等。文档还提供了相关代码链接，如`ui_design_skill.py`、`ui_d
- AI设计工作流v2.0的Skill创建界面，包括打开方式、文件路径、文件名等信息。关键内容有：Skill创建时需填写名称、描述、文件路径等；Skill创建后，可进行打开、编辑、删除等操作；Skill内容包括MD文档、参考文档、示例等；还列出了13个文件，如SkillLL.md、artifact-governance.md等。图片
- 「UI Design Workflow」 「AI落地时需先重构问题，而非急于让AI干活」

**提升篇**

- 「提升篇」
- 「一堂AI时代的竞争力·双三角模型」 「更高的视角」

**更高阶的审美来自于对更底层规律的理解和整合**

- 「高阶的审美来自于对更底层规律的理解和整合」 「更高阶的审美来自于对更底层规律的理解和整合」 「不要着急让AI干活，AI时代的问题重构」
- 「和一个人聊天舒服，只能说明对方情商高」

**学习必须遵守的两个客观规律i1原则和必要难度**

- 「提升篇」
- 一个同心圆示意图，从内到外依次为舒适区、学习区、恐慌区。舒适区位于最内层，以黄色标注；学习区位于中间层，以蓝色标注；恐慌区位于最外层，以红色标注。该图
- Andrej Karpathy的社交平台动态截图，内容为他宣布加入Anthropic的个人动态，他表示未来几年是大模型前沿发展的关键阶段，自己很高兴加入团队重返研发一线，同时提及自己仍对教育事业充满热情，计划适当时候恢复相关工作。该动态对应文档中提及的顶尖CTO级研究院低薪入职Anthropic的新闻案例，印证了AI时代需从基础层深耕、维持能力手感的相关观点
- 「一堂AI时代的竞争力·双三角模型」

**结语适可而止**

- 「适可而止」 「结语：适可而止」

**作业和Candy**

- 「作业和Candy奖励」 「作业和Candy」

**本期Candy**

- 「一定挑战！」
- 标准的黑白方格矩阵式二维码，整体呈正方形，由黑色、白色的小方格按规则排布构成，四个角落分别带有用于定位的较大的黑色方形探测图案，符合二维码的典型外观特征。该二维码用于帮助文档中的受众，通过扫描的方式完成对应作业的提交，是文档中提示的完成作业的两种方式之一，另一种方式是点击作业链接，需注意作业提交的截止时间为2026年6月9日（周二晚）24:00

</details>
