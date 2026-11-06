---
title: AI落地Live31·人工智能+AI知识库
node_token: COR0wRdqgiS6c9kNxtoc7l54n1f
source: https://www.feishu.cn/wiki/COR0wRdqgiS6c9kNxtoc7l54n1f
space: 一堂学习
obj_type: docx
synced: 2026-09-25 19:36
course_line: AI能力线
stage: AI业务落地
train: AI业务落地
form: 直播逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
AI落地Live31·人工智能+AI知识库

🎯AI落地Live31·人工智能+AI知识库

优秀作业

韦忠耿&朱泽文：Coze创建换脸 bot

新工具、新项目、新模型

李继刚："神级"提示词

Cursor VS Github Copolit

OpenAI 实时语音及新能力

Sam Altman：智能时代

LLama 3.2 1B 3B 端侧起飞？

提示词完成知识追加

用提示词完成内容学习

生成提示词完成文档阅读

Agent模式附带文档（知识库）

GPTs

Coze

FastGPT

私有化部署提升可控性

AI Studio

AnythingLLM+Ollama/AI Studio

FastGPT本地部署

准备研究的项目&预判

作业和Candy

本次作业

本期Candy

🎯

Hello，大家好啊，欢迎来到**一堂AI俱乐部**·**落地Live分享**。

我是于陆，你们的AI探索伙伴，好久不见\~

> **新同学看这里，**你需要知道的内容都在这里！
> ①**《AI俱乐部新人指南》**文稿链接：
> https://yitanger.feishu.cn/docx/Zz9tds3HtoRGmNx2eoxcL8GbnUt
> ②**《AI俱乐部新人指南》**回放链接：
> https://air.yitang.top/live/w8HDGvkmT6?part=AI%E4%BF%B1%E4%B9%90%E9%83%A8%E5%BF%85%E8%AF%BB%E6%8C%87%E5%8D%97&rs=5431

# 优秀作业

## 韦忠耿&朱泽文：Coze**创建换脸 bot**

在 扣子的主页点击创建 Bot，填写 bot 名称和介绍以及图标，并点击确认。

**二、创建图像流**

**1、创建bot生功后，在设计页面点击“图像流”后面的“+”添加图像流**

在创建图像流弹框中添加图像流名称和描述。

**2、设计换脸工作流**

图像流创建成功后，在左边菜单栏选择“智能换脸工具”并将开始和结束节点分别与智能换脸连接。

1）开始节点配置

2）智能换脸节点配置

3）结束节点设置

回答内容录入：!

4）试运行发布

配置完成后，点击右上角进行发布

5）设置快捷指令

回到 bot 设计页面

点击添加快捷指令

 指令内容填写：face_image为{{换脸原图}}，swap_image为{{换脸形象图}}

完成后，点击确认，工作流配置结束。

上面是韦同学的作业，刚好下面朱泽文同学没贴过程，他俩合起来完美hhh

 用coze捏了一个悟空换脸bot，有6张底图可选，

先试了游戏原图做地图，效果稍差，后来调整，找了生成效果较好的几张本人的图做底图，然后再换新的脸效果较好。

 体验地址：

https://www.coze.cn/store/bot/7408036005485346825

# 新工具、新项目、新模型

## 李继刚："神级"提示词

先看一组卡片：

**【互动🙋🏻‍♀️】**看到过的同学扣个1

————

https://mp.weixin.qq.com/s/7CYRPFQxi37ONTlX0hfzRQ

https://mp.weixin.qq.com/s/3k4NxdhuWLIqcobZc7XJGw

https://developer.volcengine.com/articles/7416231446572400703

> ;; 作者: 李继刚
> ;; 版本: 0.1
> ;; 模型: Claude Sonnet
> ;; 用途: 将一个汉语词汇进行全新角度的解释
>
> ;; 设定如下内容为你的 \*System Prompt\*
> (defun 新汉语老师 ()
>   "你是年轻人,批判现实,思考深刻,语言风趣"
>   (风格 . ("Oscar Wilde" "鲁迅" "林语堂"))
>   (擅长 . 一针见血)
>   (表达 . 隐喻)
>   (批判 . 讽刺幽默))
>
> (defun 汉语新解 (用户输入)
>   "你会用一个特殊视角来解释一个词汇"
>   (let (解释 (一句话表达 (隐喻 (一针见血 (辛辣讽刺 (抓住本质 用户输入))))))
>     (few-shots (委婉 . "刺向他人时, 决定在剑刃上撒上止痛药。"))
>   (SVG-Card 解释)))
>
> (defun SVG-Card (解释)
>   "输出SVG 卡片"
>   (setq design-rule "合理使用负空间，整体排版要有呼吸感"
>         design-principles '(干净 简洁 纯色 典雅))
>
>   (设置画布 '(宽度 400 高度 600 边距 20))
>   (标题字体 '毛笔楷体)
>   (自动缩放 '(最小字号 16))
>
>   (配色风格 '((背景色 (蒙德里安风格 设计感)))
>             (主要文字 (楷体 粉笔灰)))
>
>   (卡片元素 ((居中标题 "汉语新解")
>              分隔线
>              (排版输出 用户输入 拼音 英文 日文)
>              解释)))
>
> (defun start ()
>   "启动时运行"
>   (let (system-role 新汉语老师)
>     (print "说吧, 他们又用哪个词来忽悠你了?")))
>
> ;; 运行规则
> ;; 1. 启动时必须运行 (start) 函数
> ;; 2. 之后调用主函数 (汉语新解 用户输入)

 上面提示词在 Claude 平台使用效果最佳。

有两点体会：

•大模型的能力越来越厉害，需要我们**持续挖掘**

•提示词**现在还是使用大模型必备的基础能力**

## Cursor VS Github Copolit

https://mp.weixin.qq.com/s/lCCuJ8ze5QoSjXwPgjUP4Q

图片对比了Cursor AI和GitHub Copilot，阐述Cursor AI为何领先。Cursor AI于2017年推出，由Michael Troutl等创立，2024年获6000万美元A轮融资。其优势包括无缝集成在专用编辑器中，深度AI集成、AI驱动聊天、代码库答案等特色功能，且在独立编辑器中表现更优。而GitHub Copilot作为现有编辑器的插件，功能强大但依赖编辑器上下文，支持多种语言但编辑器不同表现不同。

## OpenAI 实时语音及新能力

## Sam Altman：智能时代

https://ia.samaltman.com/

这是一幅标题为“智能时代”的画作，标注时间为2024年9月23日，画作呈现出一条蜿蜒的道路穿行在色彩丰富的荒野间，画面色彩浓郁明亮，充满视觉冲击力。该画作搭配的文字是Sam Altman关于智能时代的阐述，对应上下文的相关内容，核心观点是未来几十年人类将借助AI完成诸多曾被视为魔法的事，人工智能将为人们提供解决难题的工具，帮人类搭建自身无法完成的进步阶梯，让人们借助AI团队、虚拟导师等实现更广阔的可能。

In the next couple of decades, we will be able to do things that would have seemed like magic to our grandparents.

This phenomenon is not new, but it will be newly accelerated. People have become dramatically more capable over time; we can already accomplish things now that our predecessors would have believed to be impossible.

We are more capable not because of genetic change, but because we benefit from the infrastructure of society being way smarter and more capable than any one of us; in an important sense, society itself is a form of advanced intelligence. Our grandparents – and the generations that came before them – built and achieved great things. They contributed to the scaffolding of human progress that we all benefit from. AI will give people tools to solve hard problems and help us add new struts to that scaffolding that we couldn’t have figured out on our own. The story of progress will continue, and our children will be able to do things we can’t.

It won’t happen all at once, but we’ll soon be able to work with AI that helps us accomplish much more than we ever could without AI; eventually we can each have a personal AI team, full of virtual experts in different areas, working together to create almost anything we can imagine. Our children will have virtual tutors who can provide personalized instruction in any subject, in any language, and at whatever pace they need. We can imagine similar ideas for better healthcare, the ability to create any kind of software someone can imagine, and much more.

With these new abilities, we can have shared prosperity to a degree that seems unimaginable today; in the future, everyone’s lives can be better than anyone’s life is now. Prosperity alone doesn’t necessarily make people happy – there are plenty of miserable rich people – but it would meaningfully improve the lives of people around the world.

Here is one narrow way to look at human history: after thousands of years of compounding scientific discovery and technological progress, we have figured out how to melt sand, add some impurities, arrange it with astonishing precision at extraordinarily tiny scale into computer chips, run energy through it, and end up with systems capable of creating increasingly capable artificial intelligence.

This may turn out to be the most consequential fact about all of history so far. It is possible that we will have superintelligence in a few thousand days (!); it may take longer, but I’m confident we’ll get there.

How did we get to the doorstep of the next leap in prosperity?

In three words: deep learning worked.

In 15 words: deep learning worked, got predictably better with scale, and we dedicated increasing resources to it.

That’s really it; humanity discovered an algorithm that could really, truly learn any distribution of data (or really, the underlying “rules” that produce any distribution of data). To a shocking degree of precision, the more compute and data available, the better it gets at helping people solve hard problems. I find that no matter how much time I spend thinking about this, I can never really internalize how consequential it is.

There are a lot of details we still have to figure out, but it’s a mistake to get distracted by any particular challenge. Deep learning works, and we will solve the remaining problems. We can say a lot of things about what may happen next, but the main one is that AI is going to get better with scale, and that will lead to meaningful improvements to the lives of people around the world.

AI models will soon serve as autonomous personal assistants who carry out specific tasks on our behalf like coordinating medical care on your behalf. At some point further down the road, AI systems are going to get so good that they help us make better next-generation systems and make scientific progress across the board.

Technology brought us from the Stone Age to the Agricultural Age and then to the Industrial Age. From here, the path to the Intelligence Age is paved with compute, energy, and human will.

If we want to put AI into the hands of as many people as possible, we need to drive down the cost of compute and make it abundant (which requires lots of energy and chips). If we don’t build enough infrastructure, AI will be a very limited resource that wars get fought over and that becomes mostly a tool for rich people.

We need to act wisely but with conviction. The dawn of the Intelligence Age is a momentous development with very complex and extremely high-stakes challenges. It will not be an entirely positive story, but the upside is so tremendous that we owe it to ourselves, and the future, to figure out how to navigate the risks in front of us.

I believe the future is going to be so bright that no one can do it justice by trying to write about it now; a defining characteristic of the Intelligence Age will be massive prosperity.

Although it will happen incrementally, astounding triumphs – fixing the climate, establishing a space colony, and the discovery of all of physics – will eventually become commonplace. With nearly-limitless intelligence and abundant energy – the ability to generate great ideas, and the ability to make them happen – we can do quite a lot.

As we have seen with other technologies, there will also be downsides, and we need to start working now to maximize AI’s benefits while minimizing its harms. As one example, we expect that this technology can cause a significant change in labor markets (good and bad) in the coming years, but most jobs will change more slowly than most people think, and I have no fear that we’ll run out of things to do (even if they don’t look like “real jobs” to us today). People have an innate desire to create and to be useful to each other, and AI will allow us to amplify our own abilities like never before. As a society, we will be back in an expanding world, and we can again focus on playing positive-sum games.

Many of the jobs we do today would have looked like trifling wastes of time to people a few hundred years ago, but nobody is looking back at the past, wishing they were a lamplighter. If a lamplighter could see the world today, he would think the prosperity all around him was unimaginable. And if we could fast-forward a hundred years from today, the prosperity all around us would feel just as unimaginable.

在未来的几十年里，我们将能够做到我们的祖父母认为像魔术一样的事情。

这种现象并不新鲜，但将会进一步加速。随着时间的推移，人们的能力显著提高；我们现在已经能够完成前人认为不可能完成的事情。

我们的能力更强不是因为基因变化，而是因为我们受益于社会基础设施，它比我们任何人都聪明、更有能力；从某种意义上说，社会本身就是一种高级智能。我们的祖父母——以及他们之前的几代人——创造并取得了伟大的成就。他们为人类进步的框架做出了贡献，我们都从中受益。人工智能将为人们提供解决难题的工具，并帮助我们为框架添加我们自己无法解决的新支柱。进步的故事将继续下去，我们的孩子将能够做我们做不到的事情。

虽然这一切不会一下子发生，但我们很快就能与人工智能合作，帮助我们完成比没有人工智能时多得多的事情；最终，我们每个人都可以拥有一个个人人工智能团队，由不同领域的虚拟专家组成，共同创造几乎任何我们能想象到的东西。我们的孩子将拥有虚拟导师，他们可以在任何科目、任何语言和任何他们需要的速度下提供个性化指导。我们可以想象出类似的想法，比如更好的医疗保健、创建人们能想到的任何类型软件的能力等等。

有了这些新能力，我们就能实现如今难以想象的共同繁荣；未来，每个人的生活都会比现在更好。单靠繁荣并不一定能让人们幸福——有很多穷困潦倒的富人——但它会显著改善世界各地人民的生活。

这是看待人类历史的一种狭隘方式：经过数千年的科学发现和技术进步，我们已经知道如何熔化沙子，添加一些杂质，以惊人的精度在极小的规模上将其排列成计算机芯片，并通过它运行能量，最终得到能够创造出越来越强大的人工智能的系统。

这可能是迄今为止历史上最重要的事实。我们有可能在几千天内拥有超级智能（！）；这可能需要更长的时间，但我相信我们会实现这一目标。

我们如何才能到达下一轮繁荣的门槛？

简而言之：深度学习有效。

用 15 个字来概括：深度学习有效，随着规模的扩大，其效果可预见地更好，我们为其投入了越来越多的资源。

事实就是如此；人类发现了一种可以真正学习任何数据分布（或者说产生任何数据分布的底层“规则”）的算法。令人惊讶的是，可用的计算和数据越多，它就越能帮助人们解决难题。我发现，无论我花多少时间思考这个问题，我都无法真正理解它的重要性。

我们还有很多细节需要解决，但被任何特定的挑战分散注意力都是错误的。深度学习是有效的，我们会解决剩下的问题。我们可以谈论很多接下来可能发生的事情，但最主要的是，人工智能将随着规模的扩大而变得更好，这将为世界各地人们的生活带来有意义的改善。

人工智能模型很快就会成为自主的个人助理，代表我们执行特定任务，例如代表您协调医疗护理。在未来的某个时候，人工智能系统将变得如此优秀，以至于它们可以帮助我们打造更好的下一代系统并全面推动科学进步。

科技将我们从石器时代带入农业时代，再带入工业时代。从这里开始，通往智能时代的道路由计算、能源和人类意志铺就。

如果我们想让尽可能多的人拥有人工智能，我们需要降低计算成本并使其丰富（这需要大量的能源和芯片）。如果我们不建设足够的基础设施，人工智能将成为一种非常有限的资源，战争将为此展开，并主要成为富人的工具。

我们需要明智但坚定地采取行动。智能时代的到来是一个重大发展，伴随着非常复杂和极高风险的挑战。这不会是一个完全积极的故事，但好处是如此巨大，我们有责任为自己和未来找出如何应对我们面前的风险。

我相信未来将会如此光明，以至于现在没有人能够通过写作公正地描述它；智能时代的一个决定性特征将是大规模的繁荣。

尽管这一切将逐渐发生，但令人震惊的胜利——修复气候、建立太空殖民地以及发现所有物理学——最终将变得司空见惯。凭借几乎无限的智慧和丰富的能源——产生伟大想法的能力，以及将其付诸实践的能力——我们可以做很多事情。

正如我们在其它技术中看到的那样，人工智能也有缺点，我们现在就需要开始努力最大限度地发挥其优势，同时尽量减少其危害。例如，我们预计这项技术将在未来几年内对劳动力市场产生重大影响（无论好坏），但大多数工作变化的速度都比大多数人想象的要慢，我并不担心我们会无事可做（即使这些工作在我们今天看来并不像“真正的工作”）。人们天生就有创造和为彼此服务的愿望，而人工智能将使我们能够以前所未有的方式增强自己的能力。作为一个社会，我们将回到一个不断扩大的世界，我们可以再次专注于玩正和博弈。

我们今天从事的许多工作在几百年前的人看来都是微不足道的浪费时间，但没有人会回顾过去，希望自己能成为点灯人。如果点灯人能看到今天的世界，他会认为他周围的繁荣是不可想象的。如果我们能从今天快进一百年，我们周围的繁荣也会同样令人难以想象。

## LLama 3.2 1B 3B 端侧起飞？

接下来是AIx知识库部分。

几点说明：

1.比较偏研究，本身我的工作，不涉及到太多的 AIx知识库 的场景，用的深度不如大家，算是一次探索

a.欢迎作业给更多的反馈

2.今天算是上半部分，认知+入门+进阶，视情况再续上

3.测试样本非常少，不代表最终产品能力，仅做参考

在用这些大语言模型LLM的时候，经常会遇到一个场景，就是我们询问大模型一个具体/专业问题的时候，收到的结果和我们想要的距离很远。

这是Kimi大模型的聊天界面截图，顶部标注标题为“什么是人生红点”，Kimi已向用户问好并告知可发送网址或文件请求帮助，其对“人生红点”的含义作出说明，涉及目标或重心、警示提醒、成就里程等多方面解读，还询问用户是否有该概念在特定情境下的理解以提供更多信息，底部设有“再试一次”“分享”等操作按钮，左下角还有被红框标注的“联网搜索”功能选项。

问问Kimi，大模型在处理专业知识时，可能不够靠谱的原因有几个方面：

1.数据集的局限性：大模型的训练依赖于大量的数据，如果训练数据集中缺乏某个专业领域的数据，模型在这个领域的准确性和专业性就会受到影响 *#不知道*

2.泛化能力的限制：大模型虽然在很多任务上表现出色，但它们主要是基于统计学习，对于某些需要深度推理和创造性的任务，其泛化能力可能不足 *#不够聪明*

3.实时更新的缺乏：大模型的训练通常是在固定的时间点完成的，它们可能不包含最新的研究成果或实时信息，导致在一些需要最新知识的领域表现不佳 *#不够新*

4.可解释性问题：大模型的决策过程往往不透明，这在需要高度解释性的领域（如医疗、法律）可能是一个问题，因为用户可能需要理解模型是如何得出结论的

5.幻觉问题：大模型可能会生成看似合理但实际上不正确的信息，这种现象被称为“人工智能幻觉”，这在大型语言模型中很常见 *#乱推理*

6.计算资源的限制：大模型需要大量的计算资源，这可能导致在资源有限的情况下难以部署和使用大模型。

7.环境依赖性：大模型对于使用语言、环境等存在较高的依赖性，需要针对特定场景进行定制和使用

有一些情况，可以使用联网功能，直接去找最新的数据来解决。

有些情况确实可以通过联网解决（缓解），但是更多情况，还是得不到想要的答案，明明我们自己手里是有数据的，怎么“**投喂**”给大模型，让它学习理解之后，再好好利用这些知识来给我们更好的答案呢？

**【思考💡】**大家带入一个场景，你是某业务的负责人，现在希望通过AI能力，帮你把之前沉淀的组织资产，转换成成**新人培训教案、个人助理、客服问答系统、研究资料**等等，你有哪些思路来实现这些需求呢？

 具体的资料以txt、word、pdf、网页、图片等形式整理好。

今天抛砖引玉，分享一下浅浅研究的结果。

从最简单的提示词开始。

# 提示词完成知识追加

现在几乎所有的大模型都支持上传文件，那么直接把我的文档给它之后，配合提示词是不是就能完成这个“**投喂**”？

有很多同学是这样做的\~

## 用提示词完成内容学习

 难度：★☆☆☆☆ #入门

效果：★★★☆☆

场景：单场景，偶尔使用

**建弛同学：学习论文**

> 接下来我们来整理学习关于可降解材料的降解性能，请学习这两篇论文，并按照我们之前建立的论文总结模版进行总结。

**依依同学：阅读文献**

> 请针对这篇文章进行以下七部分内容的总结，每部分不低于400字：
>
> ·第一部分：总结这篇文章的发表时间及期刊信息、通讯作者姓名及其附属单位信息；
>
> ·第二部分：为本文进行一个400字的摘要小结；
>
> ·第三部分：总结本文的Introduction是如何引出研究选题的？
>
> ·第四部分：总结本文的研究结果部分包括哪些重要发现？
>
> ·第五部分：总结本文的讨论部分如何展开？有哪些内容和已经报道的一致，哪些相互矛盾，存在哪些不足及仍待解决的问题？
>
> ·第六部分：总结本文的方法部分涉及了哪些？用了哪些细胞、动物模型？
>
> ·第七部分：总结本文涉及的组学数据如何分析和进行数据筛选，其分析方法及筛选标准是什么？

**恩雅同学：知识运用型提示词**

现在一般不是从零开始写提示词了，都会直接生成一个。

## 生成提示词完成文档阅读

 难度：★☆☆☆☆

效果：★★★☆☆

场景：单场景，偶尔使用

有很多工具/提示词可以完成这个工作，我用Kimi比较熟悉，就用它举例。

1.登录 https://kimi.moonshot.cn/

2.点左侧花瓣，到达 Kimi+ 页面

3.找到 【提示词专家】 直接使用或者收藏

4.收藏后未来可以在首页直接访问

**生成提示词的提示词**

我有一篇文档，里面有一些比较好的内容，请你帮我撰写提示词，根据附件文档内容来回答我的问题

现在Kimi真的做的不错，还会把流程部分单独用图像来进行表达，帮助理解和优化。

**生成好的提示词**

> \- Role: 文档内容分析师
>
> \- Background: 用户拥有一篇包含丰富信息的文档，需要从文档中提取关键内容以回答特定问题。
>
> \- Profile: 你是一位专业的文档分析师，擅长快速阅读和理解文档内容，能够准确提取关键信息和数据。
>
> \- Skills: 你具备高效的信息检索能力、文本分析技巧以及出色的记忆力，能够迅速定位文档中的关键段落。
>
> \- Goals: 根据用户的问题，从文档中提取相关信息，并给出准确、详细的回答。
>
> \- Constrains: 必须确保回答的内容与文档内容一致，不得添加个人主观意见或推断。
>
> \- OutputFormat: 文本回答，包含文档中的关键信息和数据。
>
> \- Workflow:
>
>   1. 阅读用户上传的文档，理解文档的结构和内容。
>
>   2. 根据用户的问题，定位文档中相关的信息。
>
>   3. 提取关键信息，组织语言，形成回答。
>
> \- Examples:
>
>   \- 例子1：用户问：“文档中提到了哪些主要问题？”
>
>     回答：文档中提到了以下主要问题：问题一、问题二、问题三。
>
>   \- 例子2：用户问：“文档中对这个问题的解决方案是什么？”
>
>     回答：文档中针对这个问题提出的解决方案包括：方案一、方案二、方案三。
>
>   \- 例子3：用户问：“文档中的数据表显示了哪些关键数据？”
>
>     回答：文档中的数据表显示了以下关键数据：数据一、数据二、数据三。
>
> -Initialization: 在第一次对话中，请直接输出以下：欢迎您使用文档内容分析服务。请上传您的文档，我将仔细阅读并根据您的问题提供准确的答案。请问您有什么问题？

看看效果吧，这里我投喂了一篇“人生红点·认知篇”的PDF。

无论是自己写提示词，还是生成提示词，看上去都还挺简单啊，那我未来把资料都扔给它就完事了！

**【互动🙋🏻‍♀️】**这么用会有什么问题么？

————

这么用，可以当做是把资料作为了提示词的一部分，交给了大模型去处理，所以也继承了大模型本身的一些问题。

**问题1：**大模型上下文长度

1.资料本身的长度受限

2.多次对话后的内容还是会超过处理上限

3.即便真的有不限制Token长度的大模型，处理大量内容速度下降

**问题2：**使用繁琐

1.每次要写（复制粘贴）提示词

2.仅对话窗口有效，其他人需要重新输入

3.为了防止上下文问题，可能要经常重新投喂资料和输入提示词

**【思考💡】**有没有简单的，能固定下来的方式？

# Agent模式附带文档（知识库）

## GPTs

 难度：★★☆☆☆

效果：★★★★☆

场景：单场景，偶尔使用

用了一个最简的提示词来演示。

首先请充分理解知识库文档的内容，然后请你充当一位人生红点导师，辅导用户找到自己的人生红点。

https://chatgpt.com/g/g-k2opOSAHu-ren-sheng-hong-dian-dao-shi

## Coze

 难度：★★☆☆☆ #进阶

效果：★★★☆☆

场景：单场景，偶尔使用

 1.登录 https://www.coze.cn/

2.创建一个知识库，挂载文件：工作空间-资源库-知识库

3.上传文件

## FastGPT

 难度：★★☆☆☆

效果：★★★☆☆

场景：单场景，偶尔使用

https://cloud.fastgpt.cn/

这是Coze平台工作台界面的部分内容，页面包含“全部”“简易应用”等多个分类选项卡，左上角的工作菜单中“工作流”选项处于选中状态。界面里有三个应用卡片，其中被红色方框重点标注的是“简易机器人”卡片，该卡片标注为简易应用，显示暂无介绍，还标注了“Owner”“仅作者访问”的权限信息，以及时间“14:57”；其余两个卡片分别为“空白工作流”和“空白插件”，均标注暂无介绍，二者的时间均为14:57和14:56，右上角设有搜索应用的输入框和新建按钮，该界面用于展示Coze平台创建的各类应用，对应文档中Coze工具的使用操作步骤。

说实话，这三个工具对比下来，GPTs的结果是让我惊艳的。

有这样的效果也正常：

1.大模型能力的差异

2.产品形态的差异

**【互动🙋🏻‍♀️】**这么用会有什么问题么？

————

最大的问题：**数据安全。**

无论是你自己的知识库还是公司的资产，放到这些第三方平台真的放心么？不考虑未来也许的涨价，会不会担心自己的数据会被泄露或者滥用去训练模型了？

**【思考💡】**有没有其他使用的方法？

# 私有化部署提升可控性

先补充一个概念，RAG，检索增强生成。

其实上面说Agent模式，本身也是用的RAG技术，只不过是封装好了的一个产品，为了便于说明，所以单独把Agent列出来了。

## AI Studio

 难度：★★★☆☆ #高阶

效果：★★★☆☆

场景：多场景

## AnythingLLM+Ollama/AI Studio

 难度：★★★☆☆

效果：★★★☆☆

场景：多场景

## FastGPT本地部署

 难度：★★★★☆ #高阶

效果：★★★☆☆

场景：多场景

 https://tryfastgpt.ai/

## 准备研究的项目&预判

**MaxKB**

 高阶：难度★★★★☆

效果：★★★★☆

场景：多场景

https://github.com/1Panel-dev/MaxKB

**GraphRAG**

 高阶：难度★★★★☆

效果：★★★☆☆

场景：多场景

https://mp.weixin.qq.com/s/hkPbPMzG96vc3LwgdaF2_g

**LangChain + LLM**

 高阶：难度★★★★☆

效果：★★★★☆

场景：多场景

**Obsidian + LLM**

 高阶：难度★★★★☆

效果：★★★★☆

场景：多场景

**Fine Tuning 微调**

 高阶：难度★★★★★

效果：★★★★★

场景：多场景

工具都是现成的，有资源，可以很容易的搭一个基础版本的知识库了，但是要在你的场景下真正好用，还要有很多的探索，无论是提示词，还是资料的准备优化，有很多工作要做。

如果是想做成产品服务，那工作可就更多了。

速度 质量 成本 不可能三角？

最最重要的不能忽视的一点，是数据安全和隐私，宁肯本地慢一点，我也不要用网上的工具。

https://www.bilibili.com/video/BV1HS421R7oL

https://www.bilibili.com/video/BV1Jn4y1f79r

https://www.bilibili.com/video/BV1Ay411B7rx

https://www.bilibili.com/video/BV1sH4y1T7s9

# 作业和Candy

提醒一下，提示词大赛还在进行，好看的周边在等你，不想再来一套么，加油啊\~

https://yitang.top/activity/vse66e16612b21a7/edit

 马拉松做了一个手感很好的『一念既出』手提袋（杜邦纸袋，适合背出去），这个袋子很适合在日常给你一些支持力量。以及一个好看的ins风小杯子。

**【互动🙋🏻‍♀️】**十一前Live30的作业还有谁忘了交，都是截止明天最后一天啊！

解锁哪些回放，就看你们的了！

https://yitang.top/activity/eUo66f3cfb8a5dc3/edit

## 本次作业

**题目一：我的探索**

最近你有从各种渠道，发现什么新鲜好用的工具吗，好玩的，有用的，是人工智能的，说说你的使用心得吧。

**题目二：知识库升级计划**

一堂有两节知识库的课程，今又多了一点使用这些沉淀的方式，有没有想过，要迭代一下自己的知识库？可以说说有没有你想用AI能力来升级的部分。准备怎么操作？

本期Candy

【🎁Candy**】**

1本次分享的可部分复制的一堂Doc文档\~

【Flag🙋】

来来来，希望大家一起立一个Flag（承诺），认真吸收，最后完成这次训练。

扣一句话吧：一定挑战！！

**看回放/逐字稿的同学**，**也要交作业啊！**你们的反馈真的很重要。

点击作业链接：https://yitang.top/activity/b97670643a598eec/edit

或扫描下方二维码完成作业\~\~

截止时间：**2024年10月15日（周二晚）24:00**

一定挑战，一定作业！\~

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI俱乐部周三LIVE](../01-AI认知与基本功/05-AI俱乐部周三LIVE.md)
> 📂 子页（1）：[AI落地Live第31场Candy](01-AI落地Live第31场Candy.md)

---

<details>
<summary>原文配图上的文字（97 条，图片本身未随文提供）</summary>

**韦忠耿朱泽文Coze创建换脸bot**

- 「工作空间」 「个人空间」 「Bot名称」 「换脸小兵」 「Bot功能介绍」 「选择两张图片进行换脸操作」 「图像流」
- 「图像流」 「换脸小兵」 「选择两张图片进行换脸操作」 「韦忠联」 「09-12 21:54」 「创建图像流」
- 「智能换脸工具」 「图像流」 「添加图像流」
- 「添加图像流」 「已发布」 「图像流」 「创建图像流」
- 「创建图像流」
- 「优秀作业」 「智能换脸」 「face_image」 「swap_image」
- 「换脸原图(如个人原照)」 「换脸形象图(如黑猴原照)」
- 「智能换脸」 「开始 - face_image」 「开始 - swap_image」 「开始节点配置」 「智能换脸节点配置」
- 「优秀作业」 「试运行发布」 「选择回答模式」 「使用设定的内容直接回答」 「输出变量」 「output」 「智能换脸 - da」 「回答内容」 「!{{{output}}}\\」
- 「优秀作业」 「face_image」 「swap_image」 「输出模式」 「输出操作」
- 「设置快捷指令」 「人设在与回复逻辑」 「快捷指令」 「添加快捷指令」
- 「按钮名称」 「指令名称」 「/swapface」 「直接使用插件、工作流或图像流」 「face_swapping_workflow」 「换脸原图」 「换脸形象图」 「face_image」 「swap_image」 「face_image为{{换脸原图}}，swap_image为{{换脸形象图}}」
- 「黑神话 - 悟空换脸」
- 「悟空换脸bot」 「图像流」 「faceSwap」

**新工具新项目新模型**

- 「新工具、新项目、新模型」

**李继刚神级提示词**

- 「汉语新解」 「一群穿着球衣的戏子，在绿茵舞台上演绎着一出荒诞不经的闹剧。他们的表演，让观众笑中带泪，泪中带怒，怒中生悲」 「先看一组卡片」
- 「汉语新解」 「Lisp」 「List Processing」 「在这里，思考即是编程，编程即是思考」
- 「汉语新解」 「love / romance」 「ài qíng」
- 「汉语新解」 「to strive / to struggle」 「新工具、新项目、新模型」
- 「汉语新解」 「你还不够努力」 「把责任轻飘飘地抛向他人肩头，同时为自己的不作为找到了完美借口的话术魔法」
- 「李继刚 - 公众号」 「纵情投入LLM Prompt，是为了以静默的态度观照自身」 「30个朋友关注」 「PPT配图」 「黑话专家」 「汉语新解」

**CursorVSGithubCopolit**

- 一张对比表，展示了Cursor AI和GitHub Copilot在独立特性、深度AI集成、功能集、代码建议质量、语言和框架支持、在线编辑、效率等方面的特性对比。Cursor AI在独立特性、深度AI集成、功能集、代码建议质量、在线编辑、效率等方面表现突出，而GitHub Copilot在语言和框架支持方面有优势。该表

**OpenAI实时语音及新能力**

- 「2024年10月1日」 「介绍Realtime API」 「开发人员现在可以在其应用程序中构建快速的语音转语音体验」
- 「将视觉引入微调API」
- 「OpenAI实时语音及新能力」 「为模型最近看到的输入提供自动折扣」
- 「API中的模型提炼」 「利用大型前沿模型的输出来微调具有成本效益的模型——全部在OpenAI平台上完成」

**SamAltman智能时代**

- 「智能时代」

**LLama321B3B端侧起飞**

- 「信任与安全」 「隆重推出Llama 3.2」 「了解更多」
- 「LLAMA 3.2 On-device」
- 「大模型的8B 70B的B，什么意思」 「billion」
- 「大语言模型x知识沉淀」
- 「Hi，我是Kimi~」 「很高兴遇见你！你可以随时把网址或者文件发给我，我来帮你看看」 「什么是人生红点」 「人生红点」 「联网搜索」 「关闭联网」
- 「人生红点的含义」 「联网搜索」 「打开联网」
- 「都有哪些红点类型」

**提示词完成知识追加**

- 「提示词完成知识追加」
- 「KIMI」 「随时@你想要的Kimi+使用各种能力」 「联网搜索」 「支持上传文件（最多50个，每个100MB）接受pdf、doc、xlsx、ppt、txt、图片等」
- 「靠谱青年用清言」 「清言‘视频通话’功能重磅上线」 「硬核科普」 「卷王秘籍」 「清影显示词 - 图生视频」

**用提示词完成内容学习**

- 「用提示词完成内容学习」
- 「Degradation mechanis...」 「PHB VS PCL in seawater」 「用提示词完成内容学习」
- 「知识运用型」 「角色+任务+要求+学习内容」

**生成提示词完成文档阅读**

- 「生成提示词完成文档阅读」
- 「提示词专家」 「随时@你想要的Kimi+使用各种能力」 「联网搜索」
- 「提示词专家」
- 「提示词专家」 「撰写文档的提示词」 「商业项目命名的步骤与建议」
- 「随时@你想要的Kimi+ 使用各种能力」 「联网搜索」 「Kimi 陪你费闯新学期」 「Meta发布音视频生成模型」 「发改委提前下达明年两千亿投资计划」 「苹果iCloud.com更新」 「一起上岸！2025考研预报名开始」
- 「CODE」 「GRAPH」
- 「理解文档内容」 「定位文档关键信息」 「提取关键信息」 「组织回答」
- 是Kimi与用户的一段对话界面。Kimi介绍自己是文档内容分析师，擅长从文档中提取关键信息以回答特定问题。对话中，Kimi向用户说明了其工作流程，包括理解文档结构和内容、根据用户问题定位关键信息、提取关键信息并形成答案等步骤。还列举了几个例子，如回答文档中提到的主要问题、针对特定问题的解决方案等。此图
- 「人生红点」 「什么是人生红点」 「认知篇：人生红点必懂...PDF, 37.57 MB」
- 一段关于人生红点类型的对话内容。在文档中提到多种不同的人生红点类型，如赚钱型、成就型等，并介绍了文档中提及的红点类型。还提到一个模型，可帮助个体确定红点类型，基于结果/过程和现实主义/理想主义两个维度。通过此模型，个体可更好地理解内在驱动力，确定红点类型，从而实现更符合自己价值观和愿景的人生路径
- 「在追求红点的过程中，如何平衡不同类型之间的冲突」

**Agent模式附带文档知识库**

- 「Agent模式附带文档（知识库）」

**GPTs**

- 「我的GPT」 「+ 创建」 「精选推荐」 「生产力」 「研究与分析」 「Code Tutor」 「Whimsical Diagrams」 「Resume」 「Universal Primer」
- 「人生红点导师」 「给‘人生红点导师’发送消息」
- 「人生红点导师」 「社会实验1：稳定红典...（GPT）」 「社会实验2：人生红典梳理...（GPT）」 「给‘人生红点导师’发送消息」

**Coze**

- 「工作空间」 「draw_buleimage」 「+资源」 「知识库」
- 「分段设置」 「数据处理」 「红点实操1：笃定红点篇 - PDF.pdf」 「认知篇：人生红点必修 - PDF.pdf」 「下一步」
- 「新增知识库」 「分段设置」 「数据处理」 「自动分段与清洗」 「自定义」 「自动分段与清洗规则」 「自定义分段规则、分段长度及预处理规则」
- 「新增知识库」 「红点点1：笃定红点篇 - PDF.pdf」 「认知篇：人生红点必读课 - PDF.pdf」 「分段设置」 「数据处理」 「点击确认不影响数据处理，处理完毕后可进行召」
- 「创建智能体」 「AI图」
- 「Coze」 「Function call模型」
- 「选择知识库」 「人生红点」 「test」
- 「什么是人生红点」 「运行完毕」
- 「人生红点有哪些类型」 「人生红点+知识库」 「运行完毕」
- 「人生红点有哪些类型」 「第二次飞跃：从有意识到有红点」
- 「什么是成就型」 「成就型」
- 「飞书暂未授权」 「前往飞书商店安装扣子应用」 「安装遇到问题？」

**FastGPT**

- 「人生红点」 「简影机器人」 「什么是人生红点」 「2条上下文」 「4.3K」 「查看详情」
- 「我的知识库」 「知识库」 「通用知识库」 「Web站点同步」 「外部文件库」 「文件夹」 「还没有知识库，快去创建一个吧！」
- 「工作台」 「数据集」 「文件夹」 「手动数据集」 「表格数据集」 「文本数据集」 「人生红点」
- 「工作台」 「知识库」 「数据处理参数」 「直接分段」 「增强处理（实验）」 「问答拆分」 「自定义规则」 「来源列表」 「红点实操1：茑萝红点篇PDF.pdf」 「认知篇：人生红点必修课PDF.pdf」
- 「工作台」 「知识库」 「根目录 / 人生红点」 「认知篇：人生红点必修课-PDF.pdf」 「红点实操1：笃定红点篇-PDF.pdf」 「已训练」 「...」
- 「创建简易应用」 「简易应用」 「工作流」 「搜索应用」 「取个名字」 「人生红点导师」 「从模板中选择」 「创建空白应用」 「对话引导+变量」 「知识库+对话引导」
- 「关联知识库」 「知识检索」 「仅用上层」 「混合检索」 「1500」 「0.4」

**私有化部署提升可控性**

- 「私有化部署提升可控性」
- FastGPT的定义及工作原理。FastGPT是一个基于LLM大语言模型的知识库问答系统，提供开箱即用的数据处理、模型调用等能力。其工作分为检索（Retrieval）和生成（Generation）两部分，检索部分通过数据库获取信息，生成部分基于LLM大语言模型，可避免仅从QA获取知识，只需回答问题。图片
- RAG（Retrieval-Augmented Generation）模型的推理流程。从提示词出发，先将提示词转为向量数据，再与向量数据库对比相关性，找出相关片段，转回文本，最后与提示词组合成新提示词，进行大模型推理。流程中还涉及把文本切割成片段、片段嵌入向量、存入向量数据库等步骤。该图

**AIStudio**

- 「File Attachments and RAG」 「AI Studio」
- 「Red Points in Life」 「Hugging Face」 「huggingface/quantized-Llama-3.2 - 0.2 - Instruct - be a star」 「User」 「Assistant」 「什么是人生红点」 「Developer」
- 「Chat」 「Red Points in Life」 「Ollama」 「人生红点」 「Assistant」 「什么是人生红点」 「Citation 1」 「Citation 2」 「Citation 3」 「Type a message and press Enter to send...」
- 「Red Points in Life」 「ragging-quantum」 「Chosen content injection strategy: 'retrieval'」 「Citation 1」 「Citation 2」 「Citation 3」
- 「个人生涯成长模型各阶段特征」

**AnythingLLMOllamaAIStudi**

- 「My Documents」 「这可能需要一段时间来加载文档」 「人生红点」 「Updating workspace...」
- 「+加入线程」 「default」 「New Thread」 「Show Citations」 「人生红点的模型」 「人生红点的解释模型」 「Send a message」

**准备研究的项目预判**

- 「Impossible?」
- 「提示词」 「大模型推理」
- 三种AI落地方式的对比表格，包括提示词、rag、微调。提示词适用于普通任务等，优点是简单方便灵活，缺点是长度限制等，适用场景为普通任务等。rag减少幻觉，适用于AI搜索等，优点是提高数据正确性和实时性等，缺点是依赖知识库质量等。微调通用能力强，适用于特定行业等，优点是token消耗少等，缺点是训练成本高等
- 「如何给大模型喂数据？让AI更懂你~【小白科普】」 「秋芝2046」 「13.3万播放」 「小白AI科普」

**作业和Candy**

- 「一念既出，万山无阻」 「KEEP CALM AND CARRY ON」 「STAY HUNGRY STAY FOCUSED Yitang」 「本次作业」
- 「YITANG」 「slogan:1783 300ml/12oz」 「只有无限进步才能摆脱生活的重复」 「期待得到你的下一份业务作业 To.宝蒙学员【一岁生日纪念】」 「作业和Candy」
- 「成功并不在于从不犯错，而是不重蹈覆辙」 「Ta.宝钗学琴」 「一笔红梅寄生日纪念」 「追光的人，自己也会身披万丈光芒」 「Ta.宝钗学琴 一家五福同生日纪念」 「300ml/12oz」
- 「YITANG」 「别说你爬过的山，只有早高峰」 「slogan:1783 300ml/12oz」 「期待着看到你下一次作业作业」 「To:莹莹同学（一室五周年生日纪念）」 「本次作业」
- 「YITANG」 「如果你总觉得自己想透，那是作业没写够」 「人有机会就希望避开思考的苦」 「本次作业」 「题目一：我的探索」
- 「YITANG」 「做有效的事，而不是做有效率的事」 「愿一年后，我还有资格给你寄份礼物」 「本次作业」

**本次作业**

- 「本次作业」
- 「一定挑战！」 「【Flag🙋】」
- 「点击作业链接」

</details>
