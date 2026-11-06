---
title: AI落地Live第31场Candy
node_token: B6MUw6kL4i9PnOkTaQ8ct2Sondb
source: https://www.feishu.cn/wiki/B6MUw6kL4i9PnOkTaQ8ct2Sondb
space: 一堂学习
obj_type: docx
synced: 2026-09-26 02:06
course_line: AI能力线
stage: AI业务落地
train: AI业务落地
form: 作业/练习
audience: 全员
series: AI俱乐部周三LIVE
---
AI落地Live第31场Candy

Google：NotebookLM

AI落地Live31分享文档内容

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

AI落地Live第31场Candy

🎁 作业奖励Candy：

恭喜你完成了第31场落地Live的作业，解锁了本次分享的完整内容！

❗

便于大家参考，**本文档提示词等内容开放复制权限，**自己练习，不要外传！

**本次Candy内容包括：**

1.Google：NotebookLM实践

2.Live31分享的可复制文档 这段内容等会贴进来哈\~

Google：NotebookLM

分享的时候，把这个忘记了。。。

补在Candy里面吧。

几个要点：

•可以直接生成播客，听完之后我都震惊了，对主题的理解非常到位，发音非常地道自然，直接商用都OK的标准

◦

（可惜是英文的，不能换语音，希望未来能换）

•**免费！**

请大家感受一下这个"播客"的质量。

 还给大家准备了字幕版本：）

  人生红点英文字幕

操作比较简单，直接登录后，上传文档，跟着引导，然后选择生成就可以了。

 后续这个功能在右下角【Notebook guide】里可以查看。

然后就可以开始聊文档的内容了，可以看到内容翻译和理解是非常准确的，可惜也是英文的。

 如果是我使用方法不对，欢迎同学告诉我正确的打开方式。

用浏览器直接翻译成，好像也还行？

AI落地Live31分享文档内容

优秀作业

韦忠耿&朱泽文：Coze**创建换脸 bot**

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

 Bash

复制

https://www.coze.cn/store/bot/7408036005485346825

https://www.coze.cn/store/bot/7408036005485346825

新工具、新项目、新模型

李继刚："神级"提示词

先看一组卡片：

**【互动🙋🏻‍♀️】**看到过的同学扣个1

————

https://mp.weixin.qq.com/s/7CYRPFQxi37ONTlX0hfzRQ

https://mp.weixin.qq.com/s/3k4NxdhuWLIqcobZc7XJGw

https://developer.volcengine.com/articles/7416231446572400703

 Bash

复制

;; 作者: 李继刚 ;; 版本: 0.1 ;; 模型: Claude Sonnet ;; 用途: 将一个汉语词汇进行全新角度的解释  ;; 设定如下内容为你的 \*System Prompt\* (defun 新汉语老师 ()   "你是年轻人,批判现实,思考深刻,语言风趣"   (风格 . ("Oscar Wilde" "鲁迅" "林语堂"))   (擅长 . 一针见血)   (表达 . 隐喻)   (批判 . 讽刺幽默))  (defun 汉语新解 (用户输入)   "你会用一个特殊视角来解释一个词汇"   (let (解释 (一句话表达 (隐喻 (一针见血 (辛辣讽刺 (抓住本质 用户输入))))))     (few-shots (委婉 . "刺向他人时, 决定在剑刃上撒上止痛药。"))   (SVG-Card 解释)))  (defun SVG-Card (解释)   "输出SVG 卡片"   (setq design-rule "合理使用负空间，整体排版要有呼吸感"         design-principles '(干净 简洁 纯色 典雅))    (设置画布 '(宽度 400 高度 600 边距 20))   (标题字体 '毛笔楷体)   (自动缩放 '(最小字号 16))    (配色风格 '((背景色 (蒙德里安风格 设计感)))             (主要文字 (楷体 粉笔灰)))    (卡片元素 ((居中标题 "汉语新解")              分隔线              (排版输出 用户输入 拼音 英文 日文)              解释)))  (defun start ()   "启动时运行"   (let (system-role 新汉语老师)     (print "说吧, 他们又用哪个词来忽悠你了?")))  ;; 运行规则 ;; 1. 启动时必须运行 (start) 函数;; 2. 之后调用主函数 (汉语新解 用户输入)

;; 作者: 李继刚

;; 版本: 0.1

;; 模型: Claude Sonnet

;; 用途: 将一个汉语词汇进行全新角度的解释

;; 设定如下内容为你的 \*System Prompt\*

(defun 新汉语老师 ()

  "你是年轻人,批判现实,思考深刻,语言风趣"

  (风格 . ("Oscar Wilde" "鲁迅" "林语堂"))

  (擅长 . 一针见血)

  (表达 . 隐喻)

  (批判 . 讽刺幽默))

(defun 汉语新解 (用户输入)

  "你会用一个特殊视角来解释一个词汇"

  (let (解释 (一句话表达 (隐喻 (一针见血 (辛辣讽刺 (抓住本质 用户输入))))))

    (few-shots (委婉 . "刺向他人时, 决定在剑刃上撒上止痛药。"))

  (SVG-Card 解释)))

(defun SVG-Card (解释)

  "输出SVG 卡片"

  (setq design-rule "合理使用负空间，整体排版要有呼吸感"

        design-principles '(干净 简洁 纯色 典雅))

  (设置画布 '(宽度 400 高度 600 边距 20))

  (标题字体 '毛笔楷体)

  (自动缩放 '(最小字号 16))

  (配色风格 '((背景色 (蒙德里安风格 设计感)))

            (主要文字 (楷体 粉笔灰)))

  (卡片元素 ((居中标题 "汉语新解")

             分隔线

             (排版输出 用户输入 拼音 英文 日文)

             解释)))

(defun start ()

  "启动时运行"

  (let (system-role 新汉语老师)

    (print "说吧, 他们又用哪个词来忽悠你了?")))

;; 运行规则

;; 1. 启动时必须运行 (start) 函数

;; 2. 之后调用主函数 (汉语新解 用户输入)

 上面提示词在 Claude 平台使用效果最佳。

有两点体会：

•大模型的能力越来越厉害，需要我们**持续挖掘**

•提示词**现在还是使用大模型必备的基础能力**

Cursor VS Github Copolit

https://mp.weixin.qq.com/s/lCCuJ8ze5QoSjXwPgjUP4Q

OpenAI 实时语音及新能力

Sam Altman：智能时代

https://ia.samaltman.com/

 PlainText

复制

In the next couple of decades, we will be able to do things that would have seemed like magic to our grandparents. This phenomenon is not new, but it will be newly accelerated. People have become dramatically more capable over time; we can already accomplish things now that our predecessors would have believed to be impossible. We are more capable not because of genetic change, but because we benefit from the infrastructure of society being way smarter and more capable than any one of us; in an important sense, society itself is a form of advanced intelligence. Our grandparents – and the generations that came before them – built and achieved great things. They contributed to the scaffolding of human progress that we all benefit from. AI will give people tools to solve hard problems and help us add new struts to that scaffolding that we couldn’t have figured out on our own. The story of progress will continue, and our children will be able to do things we can’t. It won’t happen all at once, but we’ll soon be able to work with AI that helps us accomplish much more than we ever could without AI; eventually we can each have a personal AI team, full of virtual experts in different areas, working together to create almost anything we can imagine. Our children will have virtual tutors who can provide personalized instruction in any subject, in any language, and at whatever pace they need. We can imagine similar ideas for better healthcare, the ability to create any kind of software someone can imagine, and much more. With these new abilities, we can have shared prosperity to a degree that seems unimaginable today; in the future, everyone’s lives can be better than anyone’s life is now. Prosperity alone doesn’t necessarily make people happy – there are plenty of miserable rich people – but it would meaningfully improve the lives of people around the world. Here is one narrow way to look at human history: after thousands of years of compounding scientific discovery and technological progress, we have figured out how to melt sand, add some impurities, arrange it with astonishing precision at extraordinarily tiny scale into computer chips, run energy through it, and end up with systems capable of creating increasingly capable artificial intelligence. This may turn out to be the most consequential fact about all of history so far. It is possible that we will have superintelligence in a few thousand days (!); it may take longer, but I’m confident we’ll get there. How did we get to the doorstep of the next leap in prosperity? In three words: deep learning worked. In 15 words: deep learning worked, got predictably better with scale, and we dedicated increasing resources to it. That’s really it; humanity discovered an algorithm that could really, truly learn any distribution of data (or really, the underlying “rules” that produce any distribution of data). To a shocking degree of precision, the more compute and data available, the better it gets at helping people solve hard problems. I find that no matter how much time I spend thinking about this, I can never really internalize how consequential it is. There are a lot of details we still have to figure out, but it’s a mistake to get distracted by any particular challenge. Deep learning works, and we will solve the remaining problems. We can say a lot of things about what may happen next, but the main one is that AI is going to get better with scale, and that will lead to meaningful improvements to the lives of people around the world. AI models will soon serve as autonomous personal assistants who carry out specific tasks on our behalf like coordinating medical care on your behalf. At some point further down the road, AI systems are going to get so good that they help us make better next-generation systems and make scientific progress across the board. Technology brought us from the Stone Age to the Agricultural Age and then to the Industrial Age. From here, the path to the Intelligence Age is paved with compute, energy, and human will. If we want to put AI into the hands of as many people as possible, we need to drive down the cost of compute and make it abundant (which requires lots of energy and chips). If we don’t build enough infrastructure, AI will be a very limited resource that wars get fought over and that becomes mostly a tool for rich people. We need to act wisely but with conviction. The dawn of the Intelligence Age is a momentous development with very complex and extremely high-stakes challenges. It will not be an entirely positive story, but the upside is so tremendous that we owe it to ourselves, and the future, to figure out how to navigate the risks in front of us. I believe the future is going to be so bright that no one can do it justice by trying to write about it now; a defining characteristic of the Intelligence Age will be massive prosperity. Although it will happen incrementally, astounding triumphs – fixing the climate, establishing a space colony, and the discovery of all of physics – will eventually become commonplace. With nearly-limitless intelligence and abundant energy – the ability to generate great ideas, and the ability to make them happen – we can do quite a lot. As we have seen with other technologies, there will also be downsides, and we need to start working now to maximize AI’s benefits while minimizing its harms. As one example, we expect that this technology can cause a significant change in labor markets (good and bad) in the coming years, but most jobs will change more slowly than most people think, and I have no fear that we’ll run out of things to do (even if they don’t look like “real jobs” to us today). People have an innate desire to create and to be useful to each other, and AI will allow us to amplify our own abilities like never before. As a society, we will be back in an expanding world, and we can again focus on playing positive-sum games. Many of the jobs we do today would have looked like trifling wastes of time to people a few hundred years ago, but nobody is looking back at the past, wishing they were a lamplighter. If a lamplighter could see the world today, he would think the prosperity all around him was unimaginable. And if we could fast-forward a hundred years from today, the prosperity all around us would feel just as unimaginable.   在未来的几十年里，我们将能够做到我们的祖父母认为像魔术一样的事情。这种现象并不新鲜，但将会进一步加速。随着时间的推移，人们的能力显著提高；我们现在已经能够完成前人认为不可能完成的事情。我们的能力更强不是因为基因变化，而是因为我们受益于社会基础设施，它比我们任何人都聪明、更有能力；从某种意义上说，社会本身就是一种高级智能。我们的祖父母——以及他们之前的几代人——创造并取得了伟大的成就。他们为人类进步的框架做出了贡献，我们都从中受益。人工智能将为人们提供解决难题的工具，并帮助我们为框架添加我们自己无法解决的新支柱。进步的故事将继续下去，我们的孩子将能够做我们做不到的事情。 虽然这一切不会一下子发生，但我们很快就能与人工智能合作，帮助我们完成比没有人工智能时多得多的事情；最终，我们每个人都可以拥有一个个人人工智能团队，由不同领域的虚拟专家组成，共同创造几乎任何我们能想象到的东西。我们的孩子将拥有虚拟导师，他们可以在任何科目、任何语言和任何他们需要的速度下提供个性化指导。我们可以想象出类似的想法，比如更好的医疗保健、创建人们能想到的任何类型软件的能力等等。 有了这些新能力，我们就能实现如今难以想象的共同繁荣；未来，每个人的生活都会比现在更好。单靠繁荣并不一定能让人们幸福——有很多穷困潦倒的富人——但它会显著改善世界各地人民的生活。 这是看待人类历史的一种狭隘方式：经过数千年的科学发现和技术进步，我们已经知道如何熔化沙子，添加一些杂质，以惊人的精度在极小的规模上将其排列成计算机芯片，并通过它运行能量，最终得到能够创造出越来越强大的人工智能的系统。 这可能是迄今为止历史上最重要的事实。我们有可能在几千天内拥有超级智能（！）；这可能需要更长的时间，但我相信我们会实现这一目标。  我们如何才能到达下一轮繁荣的门槛？简而言之：深度学习有效。 用 15 个字来概括：深度学习有效，随着规模的扩大，其效果可预见地更好，我们为其投入了越来越多的资源。 事实就是如此；人类发现了一种可以真正学习任何数据分布（或者说产生任何数据分布的底层“规则”）的算法。令人惊讶的是，可用的计算和数据越多，它就越能帮助人们解决难题。我发现，无论我花多少时间思考这个问题，我都无法真正理解它的重要性。 我们还有很多细节需要解决，但被任何特定的挑战分散注意力都是错误的。深度学习是有效的，我们会解决剩下的问题。我们可以谈论很多接下来可能发生的事情，但最主要的是，人工智能将随着规模的扩大而变得更好，这将为世界各地人们的生活带来有意义的改善。 人工智能模型很快就会成为自主的个人助理，代表我们执行特定任务，例如代表您协调医疗护理。在未来的某个时候，人工智能系统将变得如此优秀，以至于它们可以帮助我们打造更好的下一代系统并全面推动科学进步。 科技将我们从石器时代带入农业时代，再带入工业时代。从这里开始，通往智能时代的道路由计算、能源和人类意志铺就。 如果我们想让尽可能多的人拥有人工智能，我们需要降低计算成本并使其丰富（这需要大量的能源和芯片）。如果我们不建设足够的基础设施，人工智能将成为一种非常有限的资源，战争将为此展开，并主要成为富人的工具。 我们需要明智但坚定地采取行动。智能时代的到来是一个重大发展，伴随着非常复杂和极高风险的挑战。这不会是一个完全积极的故事，但好处是如此巨大，我们有责任为自己和未来找出如何应对我们面前的风险。 我相信未来将会如此光明，以至于现在没有人能够通过写作公正地描述它；智能时代的一个决定性特征将是大规模的繁荣。 尽管这一切将逐渐发生，但令人震惊的胜利——修复气候、建立太空殖民地以及发现所有物理学——最终将变得司空见惯。凭借几乎无限的智慧和丰富的能源——产生伟大想法的能力，以及将其付诸实践的能力——我们可以做很多事情。 正如我们在其它技术中看到的那样，人工智能也有缺点，我们现在就需要开始努力最大限度地发挥其优势，同时尽量减少其危害。例如，我们预计这项技术将在未来几年内对劳动力市场产生重大影响（无论好坏），但大多数工作变化的速度都比大多数人想象的要慢，我并不担心我们会无事可做（即使这些工作在我们今天看来并不像“真正的工作”）。人们天生就有创造和为彼此服务的愿望，而人工智能将使我们能够以前所未有的方式增强自己的能力。作为一个社会，我们将回到一个不断扩大的世界，我们可以再次专注于玩正和博弈。我们今天从事的许多工作在几百年前的人看来都是微不足道的浪费时间，但没有人会回顾过去，希望自己能成为点灯人。如果点灯人能看到今天的世界，他会认为他周围的繁荣是不可想象的。如果我们能从今天快进一百年，我们周围的繁荣也会同样令人难以想象。

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

LLama 3.2 1B 3B 端侧起飞？

接下来是AIx知识库部分。

几点说明：

1.比较偏研究，本身我的工作，不涉及到太多的 AIx知识库 的场景，用的深度不如大家，算是一次探索

a.欢迎作业给更多的反馈

2.今天算是上半部分，认知+入门+进阶，视情况再续上

3.测试样本非常少，不代表最终产品能力，仅做参考

在用这些大语言模型LLM的时候，经常会遇到一个场景，就是我们询问大模型一个具体/专业问题的时候，收到的结果和我们想要的距离很远。

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

提示词完成知识追加

现在几乎所有的大模型都支持上传文件，那么直接把我的文档给它之后，配合提示词是不是就能完成这个“**投喂**”？

有很多同学是这样做的\~

用提示词完成内容学习

 难度：★☆☆☆☆ #入门

效果：★★★☆☆

场景：单场景，偶尔使用

**建弛同学：学习论文**

 Python

复制

接下来我们来整理学习关于可降解材料的降解性能，请学习这两篇论文，并按照我们之前建立的论文总结模版进行总结。

接下来我们来整理学习关于可降解材料的降解性能，请学习这两篇论文，并按照我们之前建立的论文总结模版进行总结。

**依依同学：阅读文献**

 Python

复制

请针对这篇文章进行以下七部分内容的总结，每部分不低于400字： ·第一部分：总结这篇文章的发表时间及期刊信息、通讯作者姓名及其附属单位信息； ·第二部分：为本文进行一个400字的摘要小结； ·第三部分：总结本文的Introduction是如何引出研究选题的？ ·第四部分：总结本文的研究结果部分包括哪些重要发现？ ·第五部分：总结本文的讨论部分如何展开？有哪些内容和已经报道的一致，哪些相互矛盾，存在哪些不足及仍待解决的问题？ ·第六部分：总结本文的方法部分涉及了哪些？用了哪些细胞、动物模型？·第七部分：总结本文涉及的组学数据如何分析和进行数据筛选，其分析方法及筛选标准是什么？

请针对这篇文章进行以下七部分内容的总结，每部分不低于400字：

·第一部分：总结这篇文章的发表时间及期刊信息、通讯作者姓名及其附属单位信息；

·第二部分：为本文进行一个400字的摘要小结；

·第三部分：总结本文的Introduction是如何引出研究选题的？

·第四部分：总结本文的研究结果部分包括哪些重要发现？

·第五部分：总结本文的讨论部分如何展开？有哪些内容和已经报道的一致，哪些相互矛盾，存在哪些不足及仍待解决的问题？

·第六部分：总结本文的方法部分涉及了哪些？用了哪些细胞、动物模型？

·第七部分：总结本文涉及的组学数据如何分析和进行数据筛选，其分析方法及筛选标准是什么？

**恩雅同学：知识运用型提示词**

现在一般不是从零开始写提示词了，都会直接生成一个。

生成提示词完成文档阅读

 难度：★☆☆☆☆

效果：★★★☆☆

场景：单场景，偶尔使用

有很多工具/提示词可以完成这个工作，我用Kimi比较熟悉，就用它举例。

1.登录 https://kimi.moonshot.cn/

2.点左侧花瓣，到达 Kimi+ 页面

3.找到 【提示词专家】 直接使用或者收藏

4.收藏后未来可以在首页直接访问

**生成提示词的提示词**

 Python

复制

我有一篇文档，里面有一些比较好的内容，请你帮我撰写提示词，根据附件文档内容来回答我的问题

我有一篇文档，里面有一些比较好的内容，请你帮我撰写提示词，根据附件文档内容来回答我的问题

现在Kimi真的做的不错，还会把流程部分单独用图像来进行表达，帮助理解和优化。

**生成好的提示词**

 Python

复制

\- Role: 文档内容分析师 - Background: 用户拥有一篇包含丰富信息的文档，需要从文档中提取关键内容以回答特定问题。 - Profile: 你是一位专业的文档分析师，擅长快速阅读和理解文档内容，能够准确提取关键信息和数据。 - Skills: 你具备高效的信息检索能力、文本分析技巧以及出色的记忆力，能够迅速定位文档中的关键段落。 - Goals: 根据用户的问题，从文档中提取相关信息，并给出准确、详细的回答。 - Constrains: 必须确保回答的内容与文档内容一致，不得添加个人主观意见或推断。 - OutputFormat: 文本回答，包含文档中的关键信息和数据。 - Workflow:   1. 阅读用户上传的文档，理解文档的结构和内容。   2. 根据用户的问题，定位文档中相关的信息。   3. 提取关键信息，组织语言，形成回答。 - Examples:   - 例子1：用户问：“文档中提到了哪些主要问题？”     回答：文档中提到了以下主要问题：问题一、问题二、问题三。   - 例子2：用户问：“文档中对这个问题的解决方案是什么？”     回答：文档中针对这个问题提出的解决方案包括：方案一、方案二、方案三。   - 例子3：用户问：“文档中的数据表显示了哪些关键数据？”     回答：文档中的数据表显示了以下关键数据：数据一、数据二、数据三。-Initialization: 在第一次对话中，请直接输出以下：欢迎您使用文档内容分析服务。请上传您的文档，我将仔细阅读并根据您的问题提供准确的答案。请问您有什么问题？

\- Role: 文档内容分析师

\- Background: 用户拥有一篇包含丰富信息的文档，需要从文档中提取关键内容以回答特定问题。

\- Profile: 你是一位专业的文档分析师，擅长快速阅读和理解文档内容，能够准确提取关键信息和数据。

\- Skills: 你具备高效的信息检索能力、文本分析技巧以及出色的记忆力，能够迅速定位文档中的关键段落。

\- Goals: 根据用户的问题，从文档中提取相关信息，并给出准确、详细的回答。

\- Constrains: 必须确保回答的内容与文档内容一致，不得添加个人主观意见或推断。

\- OutputFormat: 文本回答，包含文档中的关键信息和数据。

\- Workflow:

  1. 阅读用户上传的文档，理解文档的结构和内容。

  2. 根据用户的问题，定位文档中相关的信息。

  3. 提取关键信息，组织语言，形成回答。

\- Examples:

  \- 例子1：用户问：“文档中提到了哪些主要问题？”

    回答：文档中提到了以下主要问题：问题一、问题二、问题三。

  \- 例子2：用户问：“文档中对这个问题的解决方案是什么？”

    回答：文档中针对这个问题提出的解决方案包括：方案一、方案二、方案三。

  \- 例子3：用户问：“文档中的数据表显示了哪些关键数据？”

    回答：文档中的数据表显示了以下关键数据：数据一、数据二、数据三。

-Initialization: 在第一次对话中，请直接输出以下：欢迎您使用文档内容分析服务。请上传您的文档，我将仔细阅读并根据您的问题提供准确的答案。请问您有什么问题？

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

Agent模式附带文档（知识库）

GPTs

 难度：★★☆☆☆

效果：★★★★☆

场景：单场景，偶尔使用

用了一个最简的提示词来演示。

 Python

复制

首先请充分理解知识库文档的内容，然后请你充当一位人生红点导师，辅导用户找到自己的人生红点。

首先请充分理解知识库文档的内容，然后请你充当一位人生红点导师，辅导用户找到自己的人生红点。

 Python

复制

https://chatgpt.com/g/g-k2opOSAHu-ren-sheng-hong-dian-dao-shi

https://chatgpt.com/g/g-k2opOSAHu-ren-sheng-hong-dian-dao-shi

Coze

 难度：★★☆☆☆ #进阶

效果：★★★☆☆

场景：单场景，偶尔使用

 1.登录 https://www.coze.cn/

2.创建一个知识库，挂载文件：工作空间-资源库-知识库

3.上传文件

FastGPT

 难度：★★☆☆☆

效果：★★★☆☆

场景：单场景，偶尔使用

  Python

复制

https://cloud.fastgpt.cn/

https://cloud.fastgpt.cn/

说实话，这三个工具对比下来，GPTs的结果是让我惊艳的。

有这样的效果也正常：

1.大模型能力的差异

2.产品形态的差异

**【互动🙋🏻‍♀️】**这么用会有什么问题么？

————

最大的问题：**数据安全。**

无论是你自己的知识库还是公司的资产，放到这些第三方平台真的放心么？不考虑未来也许的涨价，会不会担心自己的数据会被泄露或者滥用去训练模型了？

**【思考💡】**有没有其他使用的方法？

私有化部署提升可控性

先补充一个概念，RAG，检索增强生成。

其实上面说Agent模式，本身也是用的RAG技术，只不过是封装好了的一个产品，为了便于说明，所以单独把Agent列出来了。

这是AI落地Live第31场Candy相关内容中，展示的RAG流程示意图。图中清晰呈现了RAG技术的核心处理流程，分为文本入库和推理辅助两条路径。上方路径是将一堆文本切割成片段，把片段做成嵌入向量后存入向量数据库；下方路径则是将提示词转为向量数据，与向量数据库比对相关性，找出相关片段转回文本，和提示词组合成新提示词，最终输入大模型完成推理。

AI Studio

 难度：★★★☆☆ #高阶

效果：★★★☆☆

场景：多场景

AnythingLLM+Ollama/AI Studio

 难度：★★★☆☆

效果：★★★☆☆

场景：多场景

FastGPT本地部署

 难度：★★★★☆ #高阶

效果：★★★☆☆

场景：多场景

 https://tryfastgpt.ai/

准备研究的项目&预判

**MaxKB**

 高阶：难度★★★★☆

效果：★★★★☆

场景：多场景

  Python

复制

https://github.com/1Panel-dev/MaxKB

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

 Bash

复制

https://www.bilibili.com/video/BV1HS421R7oLhttps://www.bilibili.com/video/BV1Jn4y1f79rhttps://www.bilibili.com/video/BV1Ay411B7rxhttps://www.bilibili.com/video/BV1sH4y1T7s9

https://www.bilibili.com/video/BV1HS421R7oL

https://www.bilibili.com/video/BV1Jn4y1f79r

https://www.bilibili.com/video/BV1Ay411B7rx

https://www.bilibili.com/video/BV1sH4y1T7s9

真诚点赞，手留余香

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI落地Live31·人工智能+AI知识库](25-AI落地Live31·人工智能+AI知识库.md)

---

<details>
<summary>原文配图上的文字（88 条，图片本身未随文提供）</summary>
- 「人生红点」
- 「Sources」 「Select all sources」 「Untitled notebook」 「Settings」 「Share」 「Audio Overview」 「Deep dive conversation」 「Customize」 「Generate」 「Suggested questions」
- 「Red Dot Types（红圆点类型）」 「赚钱类型」 「成就类型」 「AI落地Live第31场」
- 「Red Dot Types and Stages of Mastery」
- 9种红点类型相关内容，分为理想主义+结果、理想主义+过程、现实主义+过程、现实主义+结果四个象限。每个象限下有具体描述，如精通、作品、内在、体验、生活、过程、金钱、成就等，还标注了数字序号，对应文中相关段落。该图片
- 「工作空间」 「个人空间」 「Bot名称」 「换脸小兵」 「Bot功能介绍」
- 「个人空间」 「图像流」 「换脸小兵」 「选择两张图片进行换脸操作」
- 「图像流」 「添加图像流」 「创建图像流」
- 「状态：已发布」 「图像流」 「创建图像流」
- 「图像流名称」 「face_swapping_workflow」 「图像流描述」 「定义换脸工作流」
- 「智能换脸」
- 「换脸原图(如个人原照)」 「换脸形象图(如黑猴原照)」
- 「使用设定的内容直接回答」 「output」 「智能换脸 - da」 「!{{{output}}}\\」 「配置完成后，点击右上角进行发布，设置快捷指令，回到bot设计页面，点击添加快捷指令，指令内容填写相关内容，完成后点击确认，工作流配置结束」
- 「快捷指令」 「添加快捷指令」 「人设与回复逻辑」
- 「按钮名称」 「指令名称」 「/swapface」 「直接使用插件、工作流或图像流」 「换脸原图」 「换脸形象图」 「指令内容」 「face_image为{{换脸原图}}，swap_image为{{换脸形象图}}」
- 「黑神话 - 悟空换脸」
- 「黑神话·悟空换脸（高清版）」 「图像流」
- 「新工具、新项目、新模型」
- 「汉语新解」 「中国男足」 「一群穿着球衣的戏子」 「新工具、新项目、新模型」
- 「Lisp」 「汉语新解」 「括号星球的原住民语言」 「先看一组卡片」
- 「汉语新解」 「ài qíng」 「love / romance」 「先看一组卡片」
- 「汉语新解」 「自我安慰剂」 「副作用」 「李继刚：‘神级’提示词」
- 「你还不够努力」 「把责任轻飘飘地抛向他人肩头，同时为自己的不作为找到了完美借口的话术魔法」
- 「纵情投入LLM Prompt，是为了以静默的态度观照自身」
- Cursor AI与GitHub Copilot对比表。对比了两者在独立特性、深度AI集成、功能集、代码建议质量、语言和框架支持、在线编辑、效率等方面的特点。Cursor AI在独立特性、深度AI集成、功能集、代码建议质量、在线编辑、效率等方面表现突出，而GitHub Copilot作为现有编辑器的附加功能，其深度AI集成和语言框架支持方面有局限。该表
- 「介绍 Realtime API」 「OpenAI实时语音及新能力」
- 「将视觉引入微调API」
- 「API中的模型提炼」
- 「智能时代」
- 「隆重推出Llama3.2」 「下载模型」 「在Meta AI上试用Llama」 「了解更多」
- 「LLAMA 3.2 On-device」
- 「大模型的8B 70B的B，什么意思」 「billion」
- 「有和占用内存对应的关系么」 「按了计算器」
- 「大语言模型x知识沉淀」
- 「什么是人生红点」 「人生红点」 「随时会你想要的RAG使用各种能力」 「联网搜索」
- 「什么是人生红点」 「联网搜索」
- 「人生红点类型」
- 「提示词完成知识追加」
- 「随时@你想要的Kimi+使用各种能力」 「联网搜索」 「支持上传文件（最多50个，每个100 MB）接受pdf、doc、xlsx、ppt、txt、图片等」
- 「靠谱青年用清言」 「硬核科普」 「卷王秘籍」 「支持上传文件（最多10个，每个20 MB）接受pdf、doc、xlsx、ppt、txt、图片等」 「从最简单的提示词开始」
- 「用提示词完成内容学习」
- 「Degradation mechanisms...」 「PHB VS PCL in seawater」
- 「知识运用型」
- 「以...的创业课」 「生成提示词完成文档阅读」
- 「提示词专家」 「随时@你想要的Kimi+使用各种能力」 「联网搜索」
- 「官方推荐」 「提示词专家」
- 「点左侧花瓣，到达Kimi+页面」 「KIMI」
- 「提示词专家」 「生成提示词」 「生成提示词的提示词」 「现在你可以在复制这个提示词并提交给Kimi完成任务」 「这是一个方便管理提示词的工作流程图」
- 「接收文档」 「理解文档内容」 「用户提出问题」 「定位文档关键信息」 「提取关键信息」 「组织回答」 「提供答案」
- 「投喂‘人生红点·认知篇’的PDF」
- 文档中提及的人生红点类别的详细内容，其中明确列出了从赚钱、成就、作品、出名、生活、体验、内心、高手到影响共9种不同的人生红点类型，每种类型都对应了具体的定义说明，比如赚钱对应追求财富积累和物质成功，成就对应渴望晋升、社会地位提升等。图片还介绍了用于确定人生红点类型的模型，该模型基于结果过程和现实主义理想主义两个维度，能帮助个体理解自身内在驱动力，明确人生优先级和取舍，更清晰地规划符合自身价值观与愿
- 「如何平衡人生不同类型的红点」 「在追求红点的过程中，如何平衡不同类型之间的冲突」 「人生红点·认知篇」
- 「Agent模式附带文档（知识库）」
- 「我的GPT」 「+ 创建」 「GPT」 「精选推荐」
- 「人生红点导师」
- 「人生红点导师」 「人生红点」
- 「人生红点锦鲤」 「对话开场白」 「上传文件」 「人生红点有哪些类型」
- 「工作空间」 「资源库」 「draw_buleimage」 「blue_img」 「+资源」 「知识库」
- 「新增知识库」 「工作空间」 「红点实践：驾控红点篇·PDF.pdf」 「认知篇：人生红点必修课·PDF.pdf」
- 「新增知识库」 「工作空间」 「资源库」 「分段设置」 「自动分段与清洗」 「自定义」 「数据处理」 「上一步」 「下一步」 「挂载文件」
- 「新增知识库」 「工作空间」 「项目开发」 「资源库」 「服务器处理完成」 「红点点1：笃定红点篇 - PDF.pdf」 「认知篇：人生红点必读课 - PDF.pdf」 「点击确认不影响数据加载，处理完毕后可进行确认」
- 「创建智能体」 「最近编辑」 「生成标题图片」 「创建知识库」
- 「人生红点·知识库」 「和子助手在这呢！」
- 「选择知识库」 「人生红点」
- 「用户493138062581」 「人生红点+知识库」 「什么是人生红点」 「运行完毕」
- 「人生红点有哪些类型」 「第二次飞跃：从有意识到有红点」
- 「什么是成就型」 「成就型」
- 「飞书暂未授权」 「授权依赖安装扣子飞书商店应用」 「安装遇到问题」
- 「简易应用」 「工作流」 「简易机器人」 「Owner」 「仅协作作者访问」
- 「简聊机器人」 「什么是人生红点」 「人生红点」
- 「我的知识库」 「知识库」 「通用知识库」 「Web站点同步」 「外部文件库」 「文件夹」 「还没有知识库，快去创建一个吧！」
- 「知识库」 「数据集」 「搜索测试」 「排队情况」 「文件夹」 「手动物数据集」 「表格数据集」 「文本数据集」 「人生红点」 「单条数据上限」
- 「选择文件」 「数据处理」 「上传数据」 「红点实战1：为啥红点篇PDF.pdf」 「认知篇：人生红点必修課PDF.pdf」 「下一步」
- 「工作台」 「知识库」 「根目录 / 人生红点」 「认知：人生红点必修课-PDF.pdf」 「红点实操1：笃定红点篇-PDF.pdf」 「已训练」 「...」
- 「人生红点导师」 「简易应用」 「工作流」 「搜索应用」 「创建简易应用」 「取个名字」 「从模板中选择」 「对话引导+变量」 「知识库+对话引导」 「+新建」
- 「私有化部署提升可控性」
- 「检索（Retrieval）」 「生成（Generation）」 「增强（Augment）」
- 「File Attachments and RAG」 「Upload File」 「Don't show this message again」
- 「Red Points in Life」 「Hugging Face」 「huggingface/llama-3.2-7b-instruct」 「什么是人生红点」 「人生红点」 「User」 「Assistant」
- 「Chat」 「Develop」 「Settings」 「Red Points in Life」 「什么是人生红点」 「Assistant」 「人生红点」 「Citation 1」 「Citation 2」 「Citation 3」
- 「人生红白的类型有哪些」 「Chat」 「Red Points in Life」 「AI Studio」 「Developer」
- 「Root Project in List」 「痛苦转折点」
- 「My Documents」 「这可能需要一段时间来加载文档」 「点击以复制或拖放」 「人生红点」 「更新工作区...」
- 「人生红点」 「Send a message」
- 「Impossible?」 「速度质量成本不可能三角？」
- 「提示词」 「大模型推理」 「统一文本问题/指令」 「多步流程嵌入/拆分」 「合为抽象能力」 「变成嵌入向量」 「拼接成向量/多向量序列」
- 一张关于三种AI实现方式的对比表格，对比的方式分别是提示词、rag、微调。表格从作用区域、优点、缺点、适用场景四个维度呈现各方式的特点，其中rag的作用区域是提示词之后、推理之前的参考书区域，优点为减少幻觉，提高数据正确性和实时性，知识库可随时更新；微调的作用区域是大模型本身，优点包括掌握特定领域知识范式，通用能力强、token消耗少、速度快；提示词的作用区域是提示词卷子上，优点是简单方便灵活，三
- 「想让大模型学习我的知识怎么给他数据？」 「某某某支持1,000万」

</details>
