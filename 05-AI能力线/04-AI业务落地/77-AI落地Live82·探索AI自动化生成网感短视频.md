---
title: AI落地Live82·探索AI自动化生成网感短视频
node_token: VagjwM3sWi7uMhkQPOEcd5AdnMf
source: https://www.feishu.cn/wiki/VagjwM3sWi7uMhkQPOEcd5AdnMf
space: 一堂学习
obj_type: docx
synced: 2026-09-25 20:22
course_line: AI能力线
stage: AI业务落地
train: AI业务落地
form: 直播逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
Hello，大家好啊，欢迎来到 **一堂AI俱乐部** · **落地Live分享** 。

我是大家的AI学习伙伴，Sherry。

1. 曾经的建筑师，在央企做大型公建设计，留学行业创业五年
2. 2023年初加入一堂教研组，负责课程运营业务和内部AI探索
3. 日常协助于陆做一些AI俱乐部的运营工作

**【互动🙋🏻♀️】** 有多少同学是新加入的呀？可以 扣1 报到一下。

> **①新同学看这里 ，一堂AI体系和相关内容，** 你需要知道的内容都在这里！ ☆☆☆☆☆
> https://yitanger.feishu.cn/wiki/JDLqwVHTniV1gJkM9JHcd1Wdnfh
> **②一堂AI俱乐部知识库** ，1-66期回放在这里 **：** ☆☆☆☆☆
> https://yai.yitang.top/intro
> > **AI知识库一页纸长期投稿入口，投稿就有 3学分 ，收录最少 5学分 ：** https://yitanger.feishu.cn/share/base/form/shrcnj37Bn9wqHZAZhNVDiAV8Qc
> **③《AI俱乐部新人指南》，** 想了解AI俱乐部可以看看：☆☆☆
> 文稿链接：https://yitanger.feishu.cn/docx/Zz9tds3HtoRGmNx2eoxcL8GbnUt
> 回放链接：https://air.yitang.top/live/w8HDGvkmT6?part=AI%E4%BF%B1%E4%B9%90%E9%83%A8%E5%BF%85%E8%AF%BB%E6%8C%87%E5%8D%97&rs=5431

## 周五课程预告

<table><colgroup><col/><col/></colgroup><tbody><tr><td>💥高阶建模实操框架篇来啦‼️
如果你也想在自己的行业和领域里，构建一套可复用、有影响力、甚至拥有“江湖地位”的模型，这节课必听。
上节课，我们讲了高阶建模的基本审美，很多同学都意犹未尽。所以这周开始，我们将正式进入「高阶建模」的实操系列。
很多人都对一堂双三角、一堂五步法、MUSE模型、TCP-R很好奇。这节课，我们会还原多个经典一堂模型究竟是如何一步步提炼出来的。
一个好的模型，不仅能够指导行动、提升效率，甚至可以成为一家公司的核心资产和战略资源。
但真正有价值的模型，从来不是靠灵光一现。它的背后是一套完整的生产系统：从洞察分析、框架搭建，到实践验证和持续打磨，每一步都有方法可循。
这节课内容很硬，包含了这些年我们内部沉最有价值的一批工具、方法和策略。请大家提前做好准备，保持最佳脑力状态。
⚠️本课仅限会员，严禁分享。
⏰ 本周五晚9点，不见不散！</td><td></td></tr></tbody></table>

接下来进入今天的分享环节：

AI 能写脚本、剪视频、生成数字人，为什么做出来的内容，总少了一点"网感"？

今晚付则宇同学，将结合 AI 产品「口播王」的完整实践，分享如何从真实需求出发，把一套"网感"经验沉淀成可自动化的 AI 工作流。

下面欢迎付则宇同学\~

# 付则宇：探索AI自动化生成网感短视频

Hello，大家好，我是付则宇。

- 2019年底加入一堂的，好像也是 **第一位一堂十年大会员**
- 2019-2024年在做 3D 交互数字人以及动作生成算法研究
- 23年11月份我写过一份 AI 数字人行业回顾，可能一些同学看过，里面有很多信息和资料
- 2024-2026年主要做语音交互技术解决方案
- 最近两个月，做了一点 AI 生成口播短视频的探索

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td></tr></tbody></table>

2023 年 11 月，我曾经在一堂和徐剑师兄做过一次数字人相关的分享。那次主要聊的是数字人的形态、技术边界和应用场景：

- *数字人能不能替代真人出镜，*
- *能不能进入真实业务，*
- *它真正有价值的地方到底在哪里。*

【互动🙋🏻】 听过我那次分享的同学，可以 扣个666

> 这个资料现在在AI知识库里，估计要更新50%以上的内容，还有一点点参考意义。

————

过去两年多，我从 **数字人交互** 转向做 **更基础的语音交互** 了，重点是 语音交互和可视化呈现的结合 。

为了推广这套语音交互系统，我开始从零开始做短视频。

今年4月，我发了一条口播短视频，播放量只有 1000 多，但带来了 20 多个陌生咨询，还成交了一个海外订单。一条视频，一千播放，二十个咨询。

是不是还不错，对吧，但是为了拍这条视频，我前后花了 **16个小时** 。从写稿到布景，从拍摄到剪辑，52段原始素材， **拍了三天** 。

【思考🤔】 那有没有办法， 用AI把这个时间从16小时压到接近0门槛 ？

这就是今天我想跟大家聊的内容。我会分享三块内容：

1. 我 **为什么会开始做口播王（短视频工具）** ，以及一条口播视频的成本都花在哪里
2. 我怎么从 300 多条参考视频和市场上的各种工具中，逐渐 **判断出80 分口播应该是什么样子**
3. 我怎么借助 AI，把这些判断 **快速做成一个可以使用的产品** ，以及中间踩过的坑和获得的反馈

下面我们正式开始。

# 故事开始

过去两年多，我从 **数字人交互** 转向做 **更基础的语音交互** 了，重点是 语音交互和可视化呈现的结合 。

简单说，就是用户和 AI 对话的过程中，AI 可以同步把相关素材呈现出来。比如自动翻页 PPT、调出图片、展示图表，或者在讲解时实时绘制一些原理动画。

| [🎬 飞书素材2.mp4](https://yitang.top/api/feishu/media/JuzZbitdjockCJxR64Hcknc2n7g) | [🎬 飞书语音交互素材1.mp4](https://yitang.top/api/feishu/media/MmOKbWqLeomJd8xtdjOc8XbOnXc) | [🎬 飞书素材3.mp4](https://yitang.top/api/feishu/media/EayCbnW4ZogX2AxeGL7c6mD4nAg) |
|-|-|-|

今年 4 月，这套语音交互系统做出来之后，我们开始做商业化。为了让别人更快理解我们到底在做什么，我自己录了条口播短视频，讲解我们的产品是什么、能解决什么问题。

这条视频播放量其实不高，就一千多。但它带来了二十来个陌生人主动加好友咨询，并且促成了一单海外项目成交。

**这个反馈让我开始重视口播短视频** 。

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

我自己是短视频门外汉，以前也发过些短视频，但大多是直接展示产品效果，没有我出镜讲解，反馈就比较一般。

我以前看过一堂的短视频课程，但当时没有能对外提供的服务。现在回过头看，我觉得很大程度不是不知道它重要，而是 **启动成本太高** 。因为我那两条视频并不是随手拍出来的，前后花了 3 到 5 天准备。

我自己录了很多遍，剪辑也花了不少时间（尽管剪辑效果一般）。

虽然我对各种剪辑工具并不陌生，但找素材、配字幕、选音乐、剪画面，所有事情加起来还是非常耗精力。

偶尔做两条可以，但如果想每天做，基本不现实。那现在 AI 这么发达，我肯定是希望用 AI 的方式来实现这件事。但这里有一个前提， **我不想要那种一眼就很 AI** 、 **自己都不愿意发的视频** ，它应该有我们平时刷短视频时熟悉的那种节奏和味道。

相关的 AI 生成视频方案其实非常多，我看了大量的市场上已有的商业产品、开源产品：

- 用现有的数字人对口型念稿子 —— 一眼假，不好意思往外发
- PPT+语音播报 —— 没有活人感，发了也白发
- Seedance 制作 —— 成本高，要花精力抽卡
- ...

后面我会详细给大家看这些项目。

一开始，我就是想满足自己的需要： **让我能够 毫不费力地 、 稳定 产出 80 分水平的口播内容** 。

让我愿意发得出去，让观众看得下去。

当然，做着做着，这件事后来不只是我自己的效率问题，也逐渐变成了一个产品判断：

如果一个工具能解决我这种人的问题，那它 **大概率也能解决一批类似创业者的问题。**

> 很多创业者们知道短视频重要，但很难稳定产出高质量的短视频

这就是做这个工具的起点，我们管它叫口播王。

既然是个工具，是个产品，那么还是从需求来看。

# 从需求到审美

这张展示在文档《AI落地Live82·探索AI自动化生成网感短视频》中的图片，核心内容为“从需求到审美”的文字，是文档第一部分的标题，下方搭配带有横线装饰的“敲黑板，说重点”字样，用于点明该部分内容是需要关注的重点，与上文提到的短视频制作卡点相关，呼应了文档围绕短视频制作展开的核心主题，明确了该部分的探讨方向。

去年一堂短视频大航海，很多同学都自己拍过、发过短视频。

【互动🙋♀️】 你在制作短视频的过程中，遇到过哪些卡点？

扣0 ：没拍过短视频

扣1 ： 选题难 ：包括标题方向、开头钩子、正文结构、台词、镜头安排、结尾引导。

扣2 ： 拍摄难 ：包括场景、人物、道具、灯光、收音和画面构图。

扣3 ： 配素材难 ：包括配图、视频等等。

扣4 ： 剪辑难 ：包括粗剪、精剪、字幕、配乐、音效、转场、封面、调色、节奏等。

扣5 ：我都OK，没啥困难

————

## 痛点账单

刚才大家提到的这些问题，最后都可以归到三笔账里，或者说三个ROI问题：

1. **认知账** ，是这件事会不会做，能不能判断什么叫做好。
2. **时间账** ，是即使知道怎么做，真正执行起来还要花多少时间。
3. **经济账** ，是如果不想自己承担前面两项，需要花多少钱购买工具或者找人完成。

我们展开来看：

<table><colgroup><col/><col/><col/><col/><col/></colgroup><tbody><tr><td>环节</td><td>认知账</td><td>时间账</td><td>经济账</td><td></td></tr><tr><td></td><td></td><td></td><td><b>自己做</b></td><td><b>请人做</b></td></tr><tr><td><b>选题</b></td><td>判断选题，组织表达结构、脚本</td><td>调研、构思、写稿</td><td><hr/></td><td>招编导</td></tr><tr><td><b>拍摄</b></td><td>掌握拍摄、布景、灯光和收音</td><td>准备现场、拍摄</td><td>（可能买设备）</td><td>招摄影师</td></tr><tr><td><b>素材</b></td><td>判断如何选择图片/视频</td><td>找素材、筛选和整理素材</td><td><hr/></td><td>招剪辑</td></tr><tr><td><b>剪辑</b></td><td>字幕、节奏、音乐、转场等等</td><td>粗剪、精剪</td><td>（软件月费）</td><td></td></tr></tbody></table>

如果把这些成本大致量化，会更直观一些。我让 AI 按公开价格和常见制作时长估算了一版：

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

我们今天不讨论请人做的情况，因为真的贵。

如果是自己做的话，一条1-3分钟、中等包装的口播视频，如果认真做下来我需要 7 小时左右，时间大致会分布在下面几个环节：

| **环节** | **参考时间及占比** |
|-|-|
| **选题** | 约 2 小时 （28%） |
| **拍摄** | 约 2 小时 （28%） |
| **素材** | 约 1 小时 （14%） |
| **剪辑** | 约 2 小时 （28%） |

实际的时间开销因人而异。

> 熟悉的肯定快\~

我今年自己拍第一条口播时，成片时长大约 6 分钟。

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

为了拍摄这一条视频，我前后拍了三天，一共留下 52 段原始视频，加起来有 1 小时 5 分钟。

> 如果算上布置现场、调整设备、重看素材和中途准备的时间（按照每天第一次和每天最后一次拍摄的时间计算），三个拍摄窗口加起来 **超过 11 个小时**

> 至于选题、素材、剪辑环节，我在能够极其熟练使用电脑操作、剪辑软件、AI工具（写稿、配图、配视频）的情况下，也花了大量时间，我们姑且按 **5个小时** 来算（实际时间花费一定超过了它）

> 总共时间开销， **16个小时** ，换成钱来算：

> 时间成本 = 制作耗时 × 个人每小时的机会成本

> 假设100元/小时，这条视频的成本就是 **1600元**

这个领域我是新人，熟练之后可能会快很多，但哪怕把一条视频的制作时间压缩到 2 小时：

2 小时 × 100 元/小时 = **200 元/条**

如果每天更新一条，一个月的时间成本就是 **6000 元** 。

所以，在这条视频获得了 20+ 客资之后， **我就有了强烈地想要日更** 、 **并且用AI来优化拍视频流程** 的想法。

而且，我相信，这个不光是满足我自己的需求，对于其他跟我类似的创业者，大概率都会有同样的问题：

1. 对于想拍但是还没拍过的人，启动成本极其高昂
2. 对于熟练的人，实际的生产成本也不低

那么，市场上有没有现成的能满足需求的工具呢？我们就要进行调研。

做调研之前，我有一些基础的 know-how 。

> 我知道可以用数字人替代真人出镜，但我为什么不用呢？全程用数字人会比较假，降低信任度

> 我知道有一些自动生成视频的工具，也试着用过它们了，但总感觉出来的效果很low

> ...

所以，有一个关键问题要问自己： **这个调研，我到底是调研什么？**

怎么去判断某个技术/工具到底是不是我需要的，是能直接满足我们的全部需要还是部分需要？

我要做的这个产品目标到底是啥？

...

这些问题都指向了一个前提： **我得先知道** ， **一个 80 分的口播视频需要长成什么样子** 。

所以第一步，要先建立审美。

## 调研建审美

我在视频号里，刷了数千条短视频，从里面挑出了300多条和我们业务有一定相关性的：

<table><colgroup><col/><col/><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

这 300 多条呢：

> 都是带有信息/观点输出的视频，不是搞笑、跳舞、表演、解说类型

> 不能 **完全没有任何制作痕迹** （否则，要么成片质量差，要么卡点都在拍摄上）

> 核心不是看它们的点赞、转发量这些数据指标，这些指标受粉丝数影响很大

> 而我们要解决的是 制作流程 的问题，所以要看的是 成品视频后的视频效果

挑出来之后，我需要方便地观看、做分析，所以我快速用 AI 编程的方式，批量把它们下载下来，并且做了一个方便进行人工预览和分类的本地网站。

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td></tr></tbody></table>

经过人工的挑选，我分成了9类：

| **【人像】** | **【信息流】** |
|-|-|
| 竖屏 | AI生图/视频 |
| 横屏 | 含装饰 |
| 小窗 | 无装饰 |
| 多视角 | 音乐 |
| 板书 |  |

下面逐一展开，快速看一下。

**【人像】竖屏**

人像以 竖屏半身 出镜，中间可能穿插文本/图片/视频等信息

<figure view-type="Preview"><source name="55004c13f07e3a2565a1fda4031c92db.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="4182001" token="NiRebDeUToMH5nxQCOSc4XLfnzg"/></figure>

[🎬 黄执中的一个成交观念，比100句话术有用太多了！#黄执中#销售技巧 #沟通技巧 #销售思维 #职场干货 #成交技巧#高情商沟通#销售话术#表达力提升#干货分享.mp4](https://yitang.top/api/feishu/media/TxC2bc4lUoDvTexEoXTcbawbncb)

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

**【人像】横屏**

人像以 横屏半身 出镜，中间可能穿插文本/图片/视频等信息

<figure view-type="Preview"><source name="d9b56415a9a15a1a99994fe4a6cf5eb9.mp4" mime="video/mp4" origin-height="576.000000" origin-width="1024.000000" size="8528865" token="VKHjbzcWQoG7sQxN3ELcFylOn1f"/></figure>

[🎬 中国版 Spotter 会不会出现？#AI工具#自媒体工具#SpotterStudio#AI辅助#AI选题中台.mp4](https://yitang.top/api/feishu/media/RkF8bnNhmo6LIvxXzcHcl7y5n0f)

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

**【人像】小窗**

人像以 画中画头像 出镜，文本/图片/视频作为主要信息全程出现

<figure view-type="Preview"><source name="baa8de7dbe5d972d5fccfc8bb75ee26f.mp4" mime="video/mp4" origin-height="1440.000000" origin-width="1080.000000" size="5473377" token="FFnnb7kpJoJbbIx702ycgIXdn1g"/></figure>

[🎬 成为一个“从创造里获取多巴胺”的人.mp4](https://yitang.top/api/feishu/media/JMY2bjcPTowwjcx9YNoczG32nIg)

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

**【人像】多视角**

人像以 横竖屏半身 、 画中画头像 、 抠像 等方式混合出现，中间穿插文本/图片/视频等信息

<figure view-type="Preview"><source name="脑子很清楚，但为什么就是说不清楚？#表达#干货#沟通#沟通技巧#社交#人际沟通#说服#社恐#吵架#争吵#观念#个人成长#表达干货#人际交往#黄执中.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="13610308" token="OBMLbqRYSoax4Dx9eBrcogLZnFg"/></figure>

[🎬 脑子很清楚，但为什么就是说不清楚？#表达#干货#沟通#沟通技巧#社交#人际沟通#说服#社恐#吵架#争吵#观念#个人成长#表达干货#人际交往#黄执中.mp4](https://yitang.top/api/feishu/media/UBnmbJNteoZdo9xOSpHcVlsOnKe)

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

**【人像】板书**

人像半身/全身出镜，结合板书进行口播

<figure view-type="Preview"><source name="根式方程的解法。初中数学压轴题，中考易错题，竞赛题，这些题你能做出来吗？#数学思维 #数学压轴题 #数学竞赛题 #初中数学.mp4" mime="video/mp4" origin-height="720.000000" origin-width="1280.000000" size="18138548" token="Zrj6bKVmIoUaMuxtefDcxn6JnzY"/></figure>

[🎬 根式方程的解法。初中数学压轴题，中考易错题，竞赛题，这些题你能做出来吗？#数学思维 #数学压轴题 #数学竞赛题 #初中数学.mp4](https://yitang.top/api/feishu/media/VBWKb324wonTKtxF9YJcfcqwncB)

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

**【信息流】AI 生图/视频**

无人像，有口播语音，素材以 AI 生成图片/视频的方式进行播放

<table><colgroup><col/><col/></colgroup><tbody><tr><td><figure view-type="Preview"><source name="71bfdd38e7e532c4f1794bc7108eeaa1.mp4" mime="video/mp4" origin-height="768.000000" origin-width="576.000000" size="6114756" token="C0vPbq7Xio0MgfxgOnhc9k12nph"/></figure>
<a href="https://yitang.top/api/feishu/media/VwzgbsjoooNHPfxVsHqc2Y43nNf">🎬 一定要大量表达，世界永远属于输出型的人 #个人成长#输出#好习惯#知识#自我提升.mp4</a></td><td><figure view-type="Preview"><source name="482725e572c4022113983ad270469873.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="3573181" token="C2htbTQ9mo72BHxf0Z2c8z4xnke"/></figure>
<a href="https://yitang.top/api/feishu/media/IsPIbNS5hooRZjxzg5YcaZAynCf">🎬 顶级合伙人，就四个字：战略盲从#合伙 #商业思维 #老板思维 #创业 #合伙协议 #股权设计.mp4</a></td></tr></tbody></table>

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

**【信息流】含装饰**

无人像，有口播语音，素材以真实图片/视频的方式进行播放，同时主视觉上方/下方含有装饰文字/图片

<table><colgroup><col/><col/></colgroup><tbody><tr><td><figure view-type="Preview"><source name="56a23052b8766f8aade9a9fa65433a89.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="1230507" token="KPN2bltIIookLjxor52cnGhYnbV"/></figure>
<a href="https://yitang.top/api/feishu/media/GUfybMZkAoFzCHx0yT1cq6w7nLe">🎬 image 2看手相火了，不到一天200万人围观 ，a16z负责人亲测被猜中，背后其实是情绪价值生意 ：拍手掌、讲故事、做订阅.mp4</a></td><td><figure view-type="Preview"><source name="学生爱用AI搜作业跳过思考，直接禁AI为什么没用？这条不讲零散方法，从教育底层逻辑讲透AI与教育，也分享了3个不增加老师工作量的实操小改动。AI再强，也不能代替人去思考。把思考.mp4" mime="video/mp4" origin-height="1560.000000" origin-width="721.000000" size="19253680" token="OCq1bhtKUouqiMxKcYMclpaqnLg"/></figure>
<a href="https://yitang.top/api/feishu/media/HjERbwazio5zftxACf4cwgmqn2f">🎬 学生爱用AI搜作业跳过思考，直接禁AI为什么没用？这条不讲零散方法，从教育底层逻辑讲透AI与教育，也分享了3个不增加老师工作量的实操小改动。AI再强，也不能代替人去思考。把思考的权利还给孩子，这是我们在技术浪潮里最该守住的事。.mp4</a></td></tr></tbody></table>

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

**【信息流】无装饰**

无人像，有口播语音，素材以真实图片/视频的方式进行播放，同时主视觉上方/下方含没有装饰文字/图片

<figure view-type="Preview"><source name="78bee12c466e7f17871e37c3e208aea6.mp4" mime="video/mp4" origin-height="576.000000" origin-width="576.000000" size="1850651" token="D5yWbSxeKoF5vRxZD1ocPXPmnKd"/></figure>

[🎬 AjmndFBgM8.mp4](https://yitang.top/api/feishu/media/NPNNboR6roSl6Mx25wGcyQOwnsf)

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

**【信息流】音乐**

无人像，无口播语音，仅有音乐，素材以真实图片/视频的方式进行播放

<table><colgroup><col/><col/></colgroup><tbody><tr><td><figure view-type="Preview"><source name="32b402b30608441904f4eea9ec5999f6.mp4" mime="video/mp4" origin-height="968.000000" origin-width="720.000000" size="317663" token="Yi7lbBSvco6ZQGxtcypcvLpVnFh"/></figure>
<a href="https://yitang.top/api/feishu/media/UOqcbAU9FoIiWGxXJS6cUgc8nKc">🎬 卡帕西预言成真！Obsidian 版 LLM Wiki 问世，笔记越用越聪明，这才是第二大脑终极形态.mp4</a></td><td><figure view-type="Preview"><source name="274c09b3adba32ff2aab84f3fb9ceb37.mp4" mime="video/mp4" origin-height="968.000000" origin-width="720.000000" size="295194" token="W7mebSwSxork9axcVXFcbgUqnsf"/></figure>
<a href="https://yitang.top/api/feishu/media/SwIZbkFYHoamctxNZcYcgRFWnkH">🎬 Claude Design 刚发布，系统提示词就在 GitHub 上泄露了，笑不活了.mp4</a></td></tr></tbody></table>

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

这些分类好的视频资源我也开放出来了，是这次分享的Candy：

看完这 300 多条视频之后，我的感受是：

我们平时说一条视频有网感，听起来很主观，但真正拆开来看，它没有那么玄学

大家应该都听说过，短视频本身有文本上的结构，比如开场要有钩子之类的，3s 内要留住人。

但是，对于视频画面而言，它的结构应该怎样设计呢？

> 人物应该放在哪里？

> 什么时候切换画面？

> 素材怎么穿插？

> 重点文字什么时候出现？

> 音乐和音效怎么配合？

> ......

哈哈，这个其实都是 **专业剪辑师** 正在做的事情了。

这些视频虽然表面上差异很大， **底层却在反复使用一些相似的表达方式** 。

比如说，对于人物的形象包装，可以归纳出这些：

<table><colgroup><col/><col/><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

而所有的画面元素都可以进行类似的归纳，它们包括这些元素：

- **人物** ：声音、形象
- **素材** ：图片、视频
- **剪辑** ：字体、字幕、文本预设效果、形象包装、素材动画、转场动画、MG动画、空镜、音效、音乐、封面

这意味着， **这件事情是可以去做程序化实现的，而不是完全自由地去凭感觉。**

做到这一步以后，我们再去看市面上的技术/工具，判断标准也变得收敛了：

> 对于实现出80分口播质感，这个技术/工具，能承担多少的剪辑工作？能承担哪部分的剪辑工作

如果某个工具已经可以实现得很好了，那我们没必要再去造轮子；

如果待开发的空间还很大，那我们可以继续来做一做。

# 从工具到方案

看看市面上的工具都能做到什么程度吧。

## 调研看工具

我把市场上的技术/工具分成4类：

1. **剪辑工具** ：剪映、开拍、度加
2. **数字人工具** ：蝉镜、闪剪、万兴播报、讯飞智作；口播智能体
3. **自动化开源项目** ：MoneyPrinterTurbo、ShortGPT 等
4. **Skill / Agent 项目** ：Remotion、HyperFrames

我们来看一看。

**第一类：综合剪辑工具**

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td>工具</td><td>主要受众</td><td>特色 AI 功能</td><td>一键成片效果</td></tr><tr><td><a href="https://www.capcut.cn/?account_id=64915324&amp;ad_platform_id=baidusearch_lead&amp;download_channel=jianying_pc_baidu_sem_winmac_1&amp;ug_attr_appid=3704&amp;utm_medium=baidufengchao&amp;ug_semver=v2.0.0&amp;bd_vid=7999132356036120579"><b>剪映</b></a></td><td>大众创作者、剪辑师、商家与运营团队，覆盖面最广</td><td>AI 字幕、AI 配音、AI 消除、智能抠像、画质修复、降噪、调色，以及丰富的模板、音乐和特效等等</td><td><a href="https://yitang.top/api/feishu/media/ID5Vb6gUCoWdkkxndEkcnlbvnDa">🎬 剪映一键成片.mp4</a></td></tr><tr><td><a href="https://www.updream.cn/?bsource=pc_sem_baidu_updream_rq&amp;bd_vid=11292332087880614714"><b>度加</b></a></td><td></td><td></td><td><a href="https://yitang.top/api/feishu/media/OCqpbev9aoIFwMxiOMScrbiPnEf">🎬 度加一键生成.mp4</a></td></tr><tr><td><a href="https://www.kaipai.com/?channel=bdpz3&amp;clickAppKey=1DCA7E2AA5EEF2C1"><b>开拍</b></a></td><td></td><td></td><td><hr/></td></tr></tbody></table>

这类工具啊，我觉得可能不太需要去专门介绍，大家应该也都很熟。

我们核心去看的是它的这些自动化成片的功能，看看出来的效果怎么样。

**第二类：数字人视频工具**

【✌️互动】 大家现在用过数字人吗？

1. 没用过， 扣1
2. 用过，现在还在用， 扣2
3. 用过，现在没用了， 扣3 （可以评论区说一说原因）

————

下面说说我对这些工具的理解。

**（1）成熟平台**

如果最大的卡点是不想拍、没时间拍，数字人是更直接的一条路线。录一段训练素材，或者上传一张照片，再输入文案，就可以让数字人持续出镜播报。

成熟的商业平台有如下这些：

| 工具 | 主要受众 | 产品特点与我们的观察 |
|-|-|-|
| [**蝉镜**](https://www.chanjing.cc/docs/product-updates/156.html) | 个人创作者、矩阵团队和企业客户 | 支持形象与声音克隆、公共数字人、PPT/PDF 导入以及 1080P/4K 导出。产品能力完整，但主要形态仍然是数字人站着或坐着播报，成片节奏和素材包装很依赖模板。 |
| [**闪剪**](https://www.shanjian.tv/ziyuan/blog/shuziren-16/) |  | 主打数字人定制、声音克隆和智能成片，专业版支持绿幕与换背景。入门价格低，适合先解决“没有人出镜”和批量生产；更丰富的素材关系与剪辑仍要额外处理。 |
| [**万兴播爆**](https://virbo.wondershare.cn/store.html) |  | 除了数字人和声音克隆，还往 IP 定位、选题推荐、脚本和智能混剪延伸。它更像一套营销内容工作台，覆盖范围更完整，但套餐成本和使用复杂度也会随之上升。 |
| [**讯飞智作**](https://peiyin.xunfei.cn/virtual-broadcasting?ppt=1) |  | 优势集中在语音合成、配音音色、数字人播报、PPT 导入和 AI 素材。适合“文稿或课件转讲解视频”，产品定价更偏会员权益与算力组合。 |

这其中，蝉镜有智能成片功能，但效果较为简单：

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td><figure view-type="Preview"><source name="职场晋升靠什么不可替代的专业能力.mp4" mime="video/mp4" origin-height="1920.000000" origin-width="1080.000000" size="37164623" token="LiYRbah4Dot8MrxtXgucOmUTnNf"/></figure>
<a href="https://yitang.top/api/feishu/media/H6LGbTLKMoi8Mdx54pLckk6Bnb3">🎬 职场晋升靠什么不可替代的专业能力.mp4</a></td></tr></tbody></table>

闪剪也有类似的功能，效果不错：

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td><figure view-type="Preview"><source name="b31099a3bfc5ca261a5eea756cf9733d.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="642391" token="BwmvbJ7a6oQbzJxcPq0cWDqRnVf"/></figure>
<a href="https://yitang.top/api/feishu/media/U4x0b1WggoFHw3xR5qycAcaxn5g">🎬 闪剪一键成片.mp4</a></td></tr></tbody></table>

**（2）口播智能体**

在调研的过程中，我发现了一类特殊的项目：口播智能体

<table><colgroup><col/><col/><col/><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

这个类型的项目，在两三年前其实就已经有了。在我2023年的分享中，当时也提过。

因为这类项目有很多是开源的，它们的流程一般是：

1. 爆款仿写改文案
2. 定制语音音色、数字人出镜
3. 配字幕、配封面，搭配一些简单的画中画包装效果

我看了好几场他们卖这个智能体的直播，直播间也一直有互动

坦白地说，我是看了他们之后，我才意识到，哪怕是两三年前的项目，市场上其实还有很多人都需要这些软件：

<table><colgroup><col/><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

**巨大的信息差** 。

**（3）启发**

1. 对于做口播这件事情，它有着巨大的潜在群体——只要想获客，他都希望可以把短视频拍起来。
2. 市场上明明有很多工具，但是为什么大家不用呢？

> 这个问题看起来很傻，但其实背后反映的一个现象，就是这些工具的渗透率和集中度是极其低的。哪怕是 Codex，我们讨论得热火朝天，好像你今天不用、明天就被淘汰了，但依然有海量的人是完全没有接触到这些东西的。

> 对于一般的用户来说，最好就是不需要他有任何认知，让他直接能拿到结果，而不是让他去学一堆复杂的东西，然后才能去使用好这个工具。

对于数字人来说，它最大的问题就是画面非常容易单调，不是靠添加一些简单剪辑效果就能解决的。

但我确实也刷到过一些视频，哪怕是用数字人做的，实际效果上也都不错。我放3个例子上来：

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td><figure view-type="Preview"><source name="揭秘三大新型套路，所有人都要高度警惕！#科普#司马华鹏#硅基动力.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="10665147" token="ZnTLbXHp5oz8TtxdOiycjX49nmc"/></figure>
<a href="https://yitang.top/api/feishu/media/JnwFbEUdxoF3GIxAWLHcB5E3nvb">🎬 揭秘三大新型套路，所有人都要高度警惕！#科普#司马华鹏#硅基动力.mp4</a></td><td><figure view-type="Preview"><source name="四位顶尖人物的重磅预言，背后藏着巨大的财富机遇#财富#认知#趋势#科技#医疗#未来#数字信息#人形机器人#人工智能#技术突破#算力#祖国强大.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="40095669" token="HxHibfnWxorKPMxQVP2cyj9Tnge"/></figure>
<a href="https://yitang.top/api/feishu/media/IVtib16jroZ4X2xvaUHcoG4LnBf">🎬 四位顶尖人物的重磅预言，背后藏着巨大的财富机遇#财富#认知#趋势#科技#医疗#未来#数字信息#人形机器人#人工智能#技术突破#算力#祖国强大.mp4</a></td><td><figure view-type="Preview"><source name="d0d2c8d7854011dfe916ee5d87bfef6a.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="8570563" token="Wmleb3zGtop7oUxjLMXcc9GXnOh"/></figure>
<a href="https://yitang.top/api/feishu/media/QyHBb956gof0CdxbQ2hcnX0vnFh">🎬 阿里良将如云、京东截然相反，核心从不是格局差距，而是两种完全相反的组织哲学。#王耀民三问家居 #阿里巴巴 #京东 #马云 #刘强东 #企业管理 #商业认知 #企业文化 #识人用人.mp4</a></td></tr></tbody></table>

可能会有同学问： **为什么说这些都是数字人呢？**

可以去看这些账号的更新频率，基本上都是一两天就发一条，真人做不到这一点的。

但是， **这些视频都有很显然的人工剪辑痕迹** ，不是自动化实现的。

可能又有同学会问：怎么判定这一定是人工剪辑的？

> 如果全流程都是自动化的，那一天可以发好几条 ...

> 并且，今天这场分享可能也不存在了 ...

至此，我们可以得到一个很清晰的结论：

**第三类：开源的自动化视频项目**

再往下看，就是 GitHub 上的自动化项目。开源项目最有价值的地方，是它把一条视频到底由哪些步骤组成，完整地摊开给我们看。

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td>项目</td><td>主要自动化路线</td><td>我们看到的边界</td><td>效果</td></tr><tr><td><a href="https://github.com/harry0703/MoneyPrinterTurbo"><b>MoneyPrinterTurbo</b></a>
约 9.7 万 Star</td><td>输入主题或关键词，自动完成脚本、TTS、素材检索、字幕、BGM 和 MoviePy 合成；支持 Web 界面、API 和批量生成。</td><td>端到端能力很完整，特别适合快速验证自动化流程。默认成片通常是“旁白 + 素材库画面 + 字幕”，最终效果很依赖素材质量和模板。</td><td><figure view-type="Preview"><source name="817febbdab08cb100f85bd4d49dfdc3d.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="3372866" token="WHMwbFc0noHIg9xguAccidcwnsb"/></figure>
<a href="https://yitang.top/api/feishu/media/VBlqbnCFSoJrCfxr5Ebce2kPnVM">🎬 01-moneyprinterturbo-demo.mp4</a></td></tr><tr><td><a href="https://github.com/FujiwaraChoki/MoneyPrinter"><b>MoneyPrinter</b></a>
约 1.37 万 Star</td><td>偏本地化路线，可结合 Ollama 完成脚本、配音、素材和合成，也可继续接上传流程。</td><td>结构简单，适合看清最小闭环；更接近无真人出镜的 faceless short，对个人 IP 口播的画面包装覆盖较少。</td><td><figure view-type="Preview"><source name="e9bf519e707b4e3d47029a985ce16710.mp4" mime="video/mp4" origin-height="480.000000" origin-width="854.000000" size="8350837" token="A3iJbVKj8oywj0xYTWVcIO2QnKe"/></figure>
<a href="https://yitang.top/api/feishu/media/DSoPb3dEmoaGnbxfCOIcMdK4ngd">🎬 02-moneyprinter-demo.mp4</a></td></tr><tr><td><a href="https://github.com/RayVentura/ShortGPT"><b>ShortGPT</b></a>
约 7700 Star</td><td>用一套编辑标记描述脚本、素材、配音和字幕，面向 YouTube Shorts / TikTok 的自动化生产。</td><td>更像一个实验性框架，思路清楚，适合学习和二次开发；直接拿来做稳定生产，还要自己补工程和视觉模板。</td><td><figure view-type="Preview"><source name="bb68bb342f5300c87c42aa9f3f831b11.mp4" mime="video/mp4" origin-height="720.000000" origin-width="1280.000000" size="3763793" token="McT7bVj8ro3LjxxEfCpcGQdqnUe"/></figure>
<a href="https://yitang.top/api/feishu/media/FpSAbSXAWo5gkDxP078cVtT9nle">🎬 03-shortgpt-demo.mp4</a></td></tr><tr><td><a href="https://github.com/ATH-MaaS/Pixelle-Video"><b>Pixelle-Video</b></a>
阿里国际 AIDC-AI 团队发起 · 约 2.54 万 Star</td><td>输入一个主题，自动完成文案、AI 配图或视频、语音解说、背景音乐和视频合成；也提供数字人口播、图生视频和动作迁移等流水线。</td><td>它更接近“从主题直接生成成片”的完整引擎，适合快速验证端到端流程；但画面主要依赖生成模型和预设模板，想做出稳定的个人 IP 口播质感，仍要继续处理人物表达、素材关系和剪辑节奏。</td><td><figure view-type="Preview"><source name="85d6dd59c8007890962ad03992250ca4.mp4" mime="video/mp4" origin-height="832.000000" origin-width="464.000000" size="5781701" token="S9gObtcvfo3IjTxZQK8cjlu6nad"/></figure>
<a href="https://yitang.top/api/feishu/media/Ce0zbqh6xoy3ehxVHUCc7zkZnLc">🎬 04-pixelle-video-demo.mp4</a></td></tr><tr><td><a href="https://github.com/FireRedTeam/FireRed-OpenStoryline"><b>FireRed-OpenStoryline</b></a>
小红书开源 · 约 3100 Star</td><td>通过自然语言驱动视频 Agent，完成素材搜索与整理、文案、配音、音乐、字体、剪辑和渲染，并能把剪辑方法保存成可复用的 Style Skill。</td><td>它已经很接近“对话式导演”，覆盖范围也比传统自动成片项目更完整；但部署和素材环境较重，最终质量仍依赖人的审美、指令和 Skill。</td><td><figure view-type="Preview"><source name="18a0503658d1be045dbfdf9d708ed421.mp4" mime="video/mp4" origin-height="1278.000000" origin-width="720.000000" size="5444739" token="MelEbUxnhojRQkx6KUrcfkc0nwb"/></figure>
<a href="https://yitang.top/api/feishu/media/JFOtb8YbEo5l3Fx35yLcIycCneX">🎬 05-firered-openstoryline-demo.mp4</a></td></tr></tbody></table>

看完这些项目以后，自动化这件事本身其实已经没有太大疑问：脚本、配音、字幕、素材检索、粗剪和导出，都可以被程序串起来。

但同样的，这里的问题在于这些视频出来的效果，完全没有网感，它们仅仅是流程上的实现。

**第四类：Skill 类项目**

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td>项目</td><td>它怎么做视频</td><td>我们的实际判断</td><td>效果</td></tr><tr><td><a href="https://www.remotion.dev/"><b>Remotion</b></a>
<a href="https://github.com/remotion-dev/remotion">GitHub </a>· <a href="https://github.com/remotion-dev/skills">Agent Skills</a>
约 5.3 万 Star</td><td>用 React 组件描述画面和时间轴，再通过代码完成预览与渲染。参数化、批量化和组件复用都很成熟。</td><td>生态成熟，适合熟悉 React 的团队，也适合做数据视频、产品演示和可复用模板。代价是工程结构更重；Agent 能把代码写出来，但风格、模板和验收标准仍然需要人定义。</td><td><figure view-type="Preview"><source name="599810c885beaba33905ba84d7b83270.mp4" mime="video/mp4" origin-height="540.000000" origin-width="540.000000" size="401859" token="MHISb26g3oyrPdxRWYKcnUBwnxd"/></figure>
<a href="https://yitang.top/api/feishu/media/I5IqbbIkPovsodxNj1KcSJk6n0c">🎬 remotion-what-is-remotion.mp4</a></td></tr><tr><td><a href="https://hyperframes.heygen.com/"><b>HyperFrames</b></a>
<a href="https://github.com/heygen-com/hyperframes">GitHub </a>· <a href="https://hyperframes.heygen.com/showcase">Showcase</a>
约 3.46 万 Star</td><td>直接用 HTML、CSS、JavaScript 和 GSAP/Lottie/Three.js 等网页技术描述画面，再逐帧渲染成 MP4；官方提供可安装到 Codex、Claude Code、Cursor 等工具里的 Skills。</td><td>更接近“为 Agent 设计”的视频框架，搭建和迭代很快，尤其适合网页动效、产品发布和信息流动画。</td><td><figure view-type="Preview"><source name="c9b0e83ed90035ac55906a3e86c74d2d.mp4" mime="video/mp4" origin-height="720.000000" origin-width="1280.000000" size="1416496" token="P2FobRE4moipnHxo24dcoGaXn7d"/></figure>
<a href="https://yitang.top/api/feishu/media/XesAbGq2CoV3hTxA6rIc4ZFAnFc">🎬 hyperframes-launch-preview.mp4</a></td></tr><tr><td><a href="https://chatcut.io/chatgpt-plugin"><b>ChatCut</b></a>
<a href="https://github.com/ChatCut-Inc/agent-plugin">GitHub </a>· <a href="https://chatcut.io/docs">官方文档</a>
ChatGPT / Codex 视频剪辑插件</td><td>安装到 ChatGPT 或 Codex 后，可以在对话中直接调用剪辑时间线，完成口播粗剪、长视频切短、字幕、Motion Graphics、B-roll、配音和视频生成。</td><td>它把“Agent 调用视频工具”做成了更完整的产品形态：用户描述目标，插件调用对应工具，并保留可以继续修改的时间线。它是商业化插件，不是开源框架，但很适合作为 Skill / Agent 路线的最新样本。</td><td><figure view-type="Preview"><source name="Codex + ChatCut = 纯口喷让AI帮你剪视频.mp4" mime="video/mp4" origin-height="720.000000" origin-width="1280.000000" size="15515169" token="JJobb0oOdo5h2axCYfvctdointz"/></figure>
<a href="https://yitang.top/api/feishu/media/XlLPb879AoprD0x569LcTJSKnTf">🎬 Codex + ChatCut = 纯口喷让AI帮你剪视频.mp4</a></td></tr><tr><td><a href="https://github.com/sun-guannan/VectCutAPI"><b>VectCutAPI</b></a>
<a href="https://github.com/sun-guannan/VectCutAPI">GitHub </a>· <a href="https://github.com/sun-guannan/VectCutAPI/tree/main/vectcut-skill">VectCut Skill</a>
流光剪辑接口项目 · 约 2100 Star</td><td>把字幕、配图、画中画、配音、滤镜、关键帧等剪辑能力做成 API、MCP 和 Skill，可接入 Dify、N8N、OpenClaw、Claude Code 等 Agent 环境。</td><td>它的核心形态是“给 Agent 使用的剪辑能力”：Agent 负责理解需求和编排步骤，VectCutAPI 调用流光剪辑完成执行。开源的是调用与接入代码，核心渲染能力仍依赖流光剪辑服务。</td><td><figure view-type="Preview"><source name="8e66008f2ad5857b7d99c6bff636834a.mp4" mime="video/mp4" origin-height="854.000000" origin-width="480.000000" size="2222860" token="Lywib1j03orcXexflAKc4Mvtnsh"/></figure>
<a href="https://yitang.top/api/feishu/media/Xiu6bqwiBo84gOxCpfPccGxKnNb">🎬 06-vectcutapi-demo.mp4</a></td></tr><tr><td><a href="https://github.com/dayuanlog/ppt2video"><b>PPT2Video</b></a>
<a href="https://github.com/dayuanlog/ppt2video/tree/main/ppt2video-sikll">Skill </a>· <a href="https://ppt.neirongpai.com">官网</a>
Skill + Windows 桌面工具</td><td>Skill 先把文章或口播稿整理成页面结构和逐页脚本，再根据主题或自定义风格生成带 HyperFrames、GSAP 动画的 HTML 场景；本地桌面工具负责导入场景、生成 MiniMax 配音，并导出 MP4 或 WebM。</td><td>它比较适合课程、知识讲解和 PPT 型视频，核心是先把内容变成有结构、有动效的页面。GitHub 公开的主体是 Skill 和主题模板，完整桌面工具通过 Releases 分发，因此更像“Skill + 专用渲染工具”，不是完整开源的视频引擎，也不是通用口播剪辑器。</td><td><figure view-type="Preview"><source name="b7a18d0a6cb496da064d85138fbcc548.mp4" mime="video/mp4" origin-height="1920.000000" origin-width="1080.000000" size="3977542" token="BzyKbcvzco48HQxyX1scMk9Enud"/></figure>
<a href="https://yitang.top/api/feishu/media/TJrSbgGl0odbKPxOISacZvYTnHh">🎬 PPT2Video 视频制作：实体店老板，用好免费豆包，就够了。 #PPT2Video #AI视频 #Hyperframes #视频助手.mp4</a></td></tr></tbody></table>

【✌️互动】 大家现在都在用 codex、claude code 或者各种小龙虾吗？

1. 正在用， 扣1
2. 没用过， 扣2

————

这两个月，我基本上天天都在用 Codex，每个月都花大几十亿 Token。

说实话，现在 AI 工具确实非常非常方便，自然而然的我也会关注这方面相关的 skill。

在今年 4、5 月份的时候，由 HeyGen 出品的 HyperFrames 在中文互联网 AI 圈子里引起了非常大的关注。

这里要补 ***一个很重要的踩坑过程给大家*** 。

> 不是工具不好，是使用场景不匹配。

大家知道 **HeyGen** 吗？

HeyGen 是前几年非常非常火的一个由中国人运营的海外数字人产品，年营收已经突破了2亿美元。

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

HyperFrames Skill，基本上是第一批上架到 Codex 的第三方 Skill，很多 AI 博主都在发布各种 **"吹捧"** 。

我这里用 "吹捧" 这个词，可能略微带了一点贬义，但我本意不是指责它。

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

我想说的是，从项目的角度看， **我被这个东西耽误了非常多的时间** 。

虽然今天的分享我是从建审美开始。 **但这是为了给大家分享** ， **我重新加工复盘后的内容** 。

**真实的情况是** ，我基本上一上来，就花了至少 3 周时间，去研究 HyperFrames 到底有如何神奇。他的整个 skill 的设计，我反反复复看了不知道多少遍。

> 我一开始的设计初衷，就想着把 HyperFrames 这种需要通过与 Agent 对话的流程，直接做成一个可以运行的工作流，直接给用户提供服务，而不是在 codex 这类 Agent 的对话窗口里，反复聊天调试。

> 毕竟，现在很多人都没用过 / 用不习惯 codex

从技术发展的角度来说，这种类型的 skill ，包括很多大家可能知道的各种 PPT skill，它们都使用了一套很新的技术理念，就是万物皆可 HTML （当然，这件事过于技术细节，我们不展开讨论）。

从产品的设计角度来看，我当时并没有清晰的理解，所谓网感视频做出来到底是什么样子，而是陷入了这种对新技术的追捧中。

后来，我看了很多其他人通过 HyperFrames 做出来的视频，总觉得哪里都不对劲，我们来看几个：

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td><figure view-type="Preview"><source name="93f1667f5a53d662d017e8cbce59d702.mp4" mime="video/mp4" origin-height="1440.000000" origin-width="1080.000000" size="4484118" token="OYkTbreeooiH3kx4zOjceicbnzh"/></figure>
<a href="https://yitang.top/api/feishu/media/R3zSbCFI8ovYuqxdBDCc5kIcnSd">🎬 居然还能用AGNET卖游泳池？？！！ (2).mp4</a></td><td><figure view-type="Preview"><source name="亲身经历两家创业公司，一家成功上市，另一家从万众瞩目的明星独角兽，硬生生走向落寞落幕😭我陪了它整整 5 年，从几十人小团队做到近千人规模，再到大规模裁员、人心涣散。.mp4" mime="video/mp4" origin-height="1024.000000" origin-width="576.000000" size="15079426" token="Dfc1bLLHbojt5lx0CiwcZlq9nWf"/></figure>
<a href="https://yitang.top/api/feishu/media/ZXoKbrIqBomlaHx5ahOcUw21nrc">🎬 亲身经历两家创业公司，一家成功上市，另一家从万众瞩目的明星独角兽，硬生生走向落寞落幕😭我陪了它整整 5 年，从几十人小团队做到近千人规模，再到大规模裁员、人心涣散。.mp4</a></td><td><figure view-type="Preview"><source name="4aff8282f2b1b1c7611e21f9ad12c340.mp4" mime="video/mp4" origin-height="720.000000" origin-width="1280.000000" size="6224490" token="YiwhbJXOmo9KnBxzHGwcLd1dn5f"/></figure>
<a href="https://yitang.top/api/feishu/media/JEjtbduGmoXsnpx0crbcMp0znUE">🎬 codex自动做视频火了，但要付费、要科学上网。我用免费的TRAE做到了一样的效果——0元、一句话、一键出片。核心是HyperFrames，让AI自己写HTML、自己渲染MP4，不用打开任何剪辑软件。codex能干的TRAE基本都能干，还自.mp4</a><figure view-type="Preview"><source name="fe59fc79566b0b9da6e5b28041572e06.mp4" mime="video/mp4" origin-height="544.000000" origin-width="967.000000" size="47662155" token="RcgybLA2WodEemxqxbicKf0xnnf"/></figure>
<a href="https://yitang.top/api/feishu/media/D6G0brg1YoS4EbxrnChcc6N5ncc">🎬 fe59fc79566b0b9da6e5b28041572e06.mp4</a></td><td><figure view-type="Preview"><source name="e1be945656358bc9714a500d077eab98.mp4" mime="video/mp4" origin-height="1920.000000" origin-width="1080.000000" size="5388894" token="R4ftb5umsoK0zqxz9nBc0YHinpb"/></figure>
<a href="https://yitang.top/api/feishu/media/NmHbb1UyBoY2Ydxl58ycyViKncg">🎬 用AI快速生成视频，再导入剪映修改，是目前多数博主的视频生成方式！.mp4</a></td></tr></tbody></table>

相信大家看过前面我们分析的这些网感模板之后，就会发现，这个 HyperFrames 和网感几乎没有关系。

【❓思考】 这是为什么呢？大家有没有什么思考？可以留在评论区。

————

原因在于，我们所谓的短视频网感和 HyperFrames 背后的 skill 所约束的规则，它用的不是一套东西。

我说的更直白一些，本质上， **网感就是一套特定的最佳实践** ， **就是一套特定的审美模板** 。

它和用什么技术，没有关系。

所以大家能理解，为什么我们拆解了 300 多个视频，去看它们到底是什么样子，对吧？

> 前面我也说了，实际上这件事的顺序，我做反了，我是最近一个月，才梳理的这些网感视频

**调研结论**

至此，我们基本可以得出很明确的结论了：市场上目前还没有一个可以 一键生成 80 分网感口播视频 的工具。

- 产品上

  1. 已有的工具要么解决了一部分的工作，要么产出的视频效果与主流的网感口播相差甚远
  2. 可开发的空间巨大，最缺的是 **自动化剪辑** ——它既涉及 know how，也涉及具体操作，门槛较高
  3. 和 AI 编程类似，用户直接获得结果的价值 **远远大于** 花时间掌握具体技能原理

- 市场上

  1. 集中度较低，即便是已经存在 2-3 年的数字人产品，仍有海量需求
  2. 会用 codex / claude code 等 agent 工具的用户数量非常少，hyperframes 不构成威胁
  3. **市场上始终存在大量信息差与服务窗口**

所以，现在目标非常明确，就是把所有那些能够产出 80 分网感口播视频的各个流程，看看用 AI 怎样去做实现。

我们先做一次简单拆分：

| **环节** | 细分 | **AI 实现路径** |
|-|-|-|
| **选题** | 提纲 | 大语言模型 |
|  | 口播稿 |  |
| **拍摄** | 声音 | 语音合成 |
|  | 形象 | 数字人 |
| **素材** | 现有素材 | OCR / 视觉模型 |
|  | 生成素材 | AI 生成图片 / 生成视频 |
| **剪辑** | **字体** | **网感组件** |
|  | **字幕** |  |
|  | **文本预设效果** |  |
|  | **形象包装** |  |
|  | **素材 / 转场动画** |  |
|  | **MG 动画** |  |
|  | **空镜视频** |  |
|  | **音效** |  |
|  | **音乐** |  |
|  | **封面** |  |

## 网感组件

这里面基本的 agent 工作流或者各种接口的调用，偏技术，我们今天分享不聊这些。（这些其实是开发大头...）

在开发的过程中，我遵循的原则是： **能使用商用 API 的就用商用 API** ， **不要陷入优化细节** ， **自己去做部署** 。

**哪怕有些效果要差些** ，先以能快速跑起来为准，等架构稳定了再做优化。

对于和网感剪辑有关的组件，实现难度上，我们可以划分出3类：

1. **无现成最佳实践，必须依靠人工归纳的** ：

   - 比如，人物的形象包装，刚才我们已经看了。
   - 再比如，素材的处理方式，滚动、高亮、定位等等，这些都可以做程序化实现。

1. **有现成最佳实践，也很容易做出来** ：音效、音乐、字体等等，这些是相对静态的资源，有大量博主分享过：

<table><colgroup><col/><col/><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

这些视频我们只需要人工看一遍，记录好里面对应的资源，把它们下载下来，做好集成就可以了。

1. **有现成最佳实践，但不容易做出来** ：比如文本预设效果、动画等等。

这部分非常有意思， **也是 vibe coding 时代下** ，才可能快速实现的动作：

比如文本预设效果，这是体现网感效果中，非常关键的内容：

[🎬 文本预设效果.mp4](https://yitang.top/api/feishu/media/E5q5bHnb7oquHbxET0fcTVd9nBb)

<figure view-type="Preview"><source name="1f40d2e7c8d2263b7ec5af189c4bdf45.mp4" mime="video/mp4" origin-height="872.000000" origin-width="2136.000000" size="2525323" token="Xz1Mbyn7goAkcPxze1Mcn3yMnXe"/></figure>

我们要怎么做快速的程序化实现呢？

1. 淘宝上可以买到大量的原本服务于人工剪辑流程的预设资源；视频号中也有很多博主售卖：

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

1. Codex 做解析，实现像素级还原

在现在的 AI 工具的加持下，我们可以直接跟 Codex 说，让它去看对应的资源文件，解析为我们自己要实现的程序中可以运行的方式。（ **如果用传统的开发流程来做这件事情，工作量是无法想象的** ）

[🎬 文本预设效果复刻.mp4](https://yitang.top/api/feishu/media/QdX0bPbgsoHE4RxgrKTcChBinEf)

<figure view-type="Preview"><source name="436994753a160cf5aa124b27722eff25.mp4" mime="video/mp4" origin-height="1378.000000" origin-width="2336.000000" size="7151121" token="OxxPbKlRMoyANAxA8Tpc9fm7n4c"/></figure>

类似的方式，我们可以将常见的各类网感动画效果，也做相应的实现。

<table><colgroup><col/><col/></colgroup><tbody><tr><td><figure view-type="Preview"><source name="5b84142c2470848349f14dda12a7a954.mp4" mime="video/mp4" origin-height="1296.000000" origin-width="560.000000" size="4363104" token="Pu86bVgZWoZ0yhxadwhcGgIJnDd"/></figure>
<a href="https://yitang.top/api/feishu/media/DYGSbMgEsorFvVxf7Y8ciFPNnEd">🎬 网感动画.mp4</a></td><td><figure view-type="Preview"><source name="42ae4d05c1a9f2b27304be11dca2c2af.mp4" mime="video/mp4" origin-height="1296.000000" origin-width="560.000000" size="4822319" token="VINjbKNCpoGaptxsOCvcvy4hnPh"/></figure>
<a href="https://yitang.top/api/feishu/media/O9sAbIDtOo5zOLxZJMQc0TUvnyg">🎬 1a6e9753523efce23dbf436611032c6f.mp4</a></td></tr></tbody></table>

所有这些效果组合在一起，最后形成一个完整的自动化工作流，就成为实现网感短视频的基础了。

来看一看我们的 Demo：

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td><figure view-type="Preview"><source name="测试demo.mp4" mime="video/mp4" origin-height="1440.000000" origin-width="1080.000000" size="13051580" token="BnvobAJPVopLbgxqm3IcBz8Unpc"/></figure>
<a href="https://yitang.top/api/feishu/media/S9kZbVshLo8eDCxhXHachlCHnte">🎬 测试demo.mp4</a></td><td><figure view-type="Preview"><source name="测试demo2.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="960.000000" size="13388822" token="PGOnbaykMoJnd5xljJ9cm09Pn5b"/></figure>
<a href="https://yitang.top/api/feishu/media/F5yBbqdLFoh5GXxPFnOcxnvunqg">🎬 测试demo2.mp4</a></td><td><figure view-type="Preview"><source name="d72dc7a4f3b4670ee1e83290830d7dcb.mp4" mime="video/mp4" origin-height="960.000000" origin-width="720.000000" size="4792459" token="NSj7bBlcWoT2m7x27RucXZAlnJb"/></figure>
<a href="https://yitang.top/api/feishu/media/FXbVbvj7povFaTxMMcKcqbeYn1c">🎬 测试Demo3.mp4</a></td></tr></tbody></table>

# 从方案到MVP

## 初步验证

我也在小范围内做了一些测试，收到的反馈都还不错。

有一些朋友他们是直接愿意付费，还有一些朋友是直接想去做这种贴牌的销售。

当然，现在我们还在不断优化过程中， **同时也在进行预售（今日重点）** ，有兴趣体验支持的朋友可以加我。

我们也在找代理商（可OEM）、投资人。

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td></tr></tbody></table>

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

## 快跑 tips

在实现的过程中，还有一些开发上的小技巧，结合 vibe coding，可以临时性规避一些麻烦 / 降低成本：

### 火山引擎，企业认证

在实际的开发过程中，有很多我们需要去调用的 API 接口，各大云厂商本身都会提供一些基础的免费额度。这些免费额度根据业务不同的需要，有的时候测试是够用的，但有的时候其实不太够用。

这个时候，像火山引擎的话，进行企业认证完之后，可以批量去注册 10 个账号。然后结合 vibe coding，让它写一个这种账号池，我们就可以利用好它的免费额度，来进行早期的测试，甚至是早期的小规模验证。

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

举个例子：

> 比如说音色复刻，在火山引擎里面每一个账号都会送 10 个免费的席位。

> 但如果你的席位超出 10 个了，每增加一个席位，就要多花 100+ 块钱，那如果说一个企业认证支持 10 个账号，你就可以直接有 100 个席位，直接节省1万元。

> ...

> 再比如，火山引擎也提供一定量的数字人视频生成服务。在我们的这个流程里面，它可以用来快速帮助用户生成一个用于做训练的数字人预处理视频。这种视频如果使用常规的即梦服务，需要 1 元/秒。但是，每个账号可以有 200 秒的免费额度。我们对于一个用户，只需要使用差不多 20 秒来进行一次处理。

> 按正常使用来看：单次生成这样一个视频的成本，其实需要20元。但如果我们开了 10 个账号（即拥有 2000 秒的免费处理时长），相当于可以满足差不多 100 个用户的训练要求，又能节省2000元。

这种方式以前为什么不好弄？是因为你每做一个接口，你都要去设计这些账号池，在代码里去做这种接入很麻烦。

但是正是因为 vibe coding 可以非常方便地去接入这些接口，那其实就是说一句话的事，AI 就可以帮你配置好。

### 百度秒哒——验证码注册

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td></td><td></td><td></td></tr></tbody></table>

百度的秒搭是一个非常方便的 vibe coding 小工具，对于快速产生一些原型是有帮助的。

我桥接了它的验证码注册功能，因为这个功能在常规情况下接入起来比较麻烦，需要各种认证、配置。对于频繁的测试，成本大概5分钱一条。

画板内容

但如果我们使用百度秒哒绕开常规的接入的话，不仅方便，而且可以近乎免费的使用验证码能力。

唯一的小缺点是无法定制短信签名。

### 廉价中转站（LLM/图片）大量测试11111

很多时候，我们要用到一些比较好的模型来接入到整个 agent 流程中。比如说：用来生成提纲\用来生成口语化的脚本等等，对于一些复杂任务，甚至需要用到一些国外最先进的模型。但如果使用常规的接口调用，它们的成本是非常高的。

使用 opus 级别的模型，单次请求有的时候，我们的提示词可能有大几千甚至上万个 token 作为输入。同时，如果输出的内容也很长的话，可能一次请求就要 1 块钱。

在测试阶段，在频繁请求的情况下，成本还是很高的。如果我们使用一些中转站提供的接入服务来做测试，成本就可以压到非常非常低， **因为有些模型可以按请求次数来算** ，而非按实际输入输出 token 来算。

<table><colgroup><col/><col/></colgroup><tbody><tr><td></td><td></td></tr></tbody></table>

当然，中转商的好处是便宜，缺点就是不稳定，要按情况处理使用：

> 比如可以接入多个中转商，某个任务失败的时候，切换到其他中转商去请求。当然，最后可能需要使用正规的 API 进行兜底。

# 认知复盘

到这里，口播王这件事的探索基本讲完了，整个项目还在继续进行。

回头看，这个项目并不是从“我要做一个 AI 产品”开始的。

1. 最早只是两条视频带来了二十多个陌生咨询，让我第一次认真看见口播视频的获客效果；
2. 接着，我亲自做了一条视频，算清了它的时间账和经济账；
3. 再往后，才有了 300 多条样本、工具调研、模板复刻和自动化系统。

这条路径走完以后，其实和一堂双三角体系是非常吻合的。

大家还记得双三角吗？

我不打算在这里重新讲一遍模型，只说这次项目带给我的几个感受。

## AI 的边界

最开始，我以为难点在能不能生成。只要数字人能说话、字幕能对齐、素材能插进去，流程就算跑通了。

第一批样片出来后，技术上都成立，但画面的味道不对。

它们不是坏掉了，而是没有短视频平台里那种自然的网感节奏。

后来我们花很多时间看 300 多条视频，真正补的不是素材库，而是一套判断标准。

哪句话值得切画面，什么时候人物退到次要位置，字幕、音效和素材怎样一起把重点托起来。

AI 可以快速执行这些动作，但它并不知道什么叫 **刚刚好** 。

## 关于审美

判断标准建立起来以后，下一步不是让 AI 多模仿一点，而是把判断拆成工具能执行的东西。

我们把参考视频归成九类，把反复出现的画面方法拆成组件，把模板、动画、字幕、音效和素材切换变成规则。

以前存在于剪辑师经验里的“这里应该切一下”，逐渐变成系统里一个可选择、可组合、可检验的动作。

这也是我对审美和体系的理解： **审美负责定义结果，体系负责让结果重复发生** 。

> 只有审美，没有体系，做出来的还是一次性作品；

> 只有体系，没有审美，只会稳定地产出味道不对的东西。

这两个月里，我们消耗了非常多 Token。

现在回头看，有些是有效迭代，有些则来自一开始把注意力放错了地方。

> 我们曾经纠结 Remotion、HyperFrames，纠结哪套架构更适合。

> 后来才发现，架构只决定怎么实现，不会告诉我们什么值得实现。

在成片标准不清楚的时候，代码写得越快，越容易把一个不成熟的判断做得很完整。

所以这次我对 AI 开发更深的一层感受，不是开发速度变快了，而是 **验证顺序比以前更重要了** 。

**本质上，仍然是审美，是 Taste**

感谢一堂，今天就分享到这里，最后推荐两个关于 taste 的视频：

<table><colgroup><col/><col/></colgroup><tbody><tr><td><figure view-type="Preview"><source name="中登创业时代已来！YC总裁Garry Tan说；拥有品味和判断力的40岁创始人，才是这个时代的新晋独角兽。.mp4" mime="video/mp4" origin-height="1280.000000" origin-width="720.000000" size="10631607" token="B1vEbNUnJotMLAxdREAcS4Tcn8d"/></figure>
<a href="https://yitang.top/api/feishu/media/CITJbih2FoJKwSxp2Gfc92Tanrf">🎬 中登创业时代已来！YC总裁Garry Tan说；拥有品味和判断力的40岁创始人，才是这个时代的新晋独角兽。.mp4</a></td><td><figure view-type="Preview"><source name="55817ec84ddb233d30f81a0567475c8a.mp4" mime="video/mp4" origin-height="720.000000" origin-width="1280.000000" size="2872045" token="AhJgbi1jIoymzkxw7YKcfpqfnxh"/></figure>
<a href="https://yitang.top/api/feishu/media/D0fMbGjgloijkKxjc27c3mqAn6c">🎬 如何提升自己的taste.mp4</a></td></tr></tbody></table>

我是付则宇，感谢大家的时间，我们下次见\~

# 作业和Candy奖励

**第一个作业，心得理解题**

听完分享，你对AI生产内容有什么新的理解？请尽量结合你自己的业务、内容创作、短视频/小红书/社群运营等，说说这节课的启发。

建议选择一个最触动你的点来写，比如：

- 不是因为 AI 能做视频才开始做口播王，而是因为一条口播视频带来了真实客户咨询；
- 短视频生产背后有认知账、时间账和经济账；
- 做 AI 产品不能先迷恋新技术，而要先知道 80 分结果长什么样；
- 新工具很强，但如果没有审美标准和验证顺序，也可能让人跑偏……

**第二个作业，痛点拆解题**

选一个自己真实想做、正在做，或者观察过的内容场景，尝试像这节课一样，先拆一遍痛点。

这个场景可以是：个人 IP 口播、公司业务获客、小红书种草、课程推广、产品介绍、社群招募，或者你熟悉的任意内容场景。

作业里不用做完整视频，重点写清楚：

- 你想解决的内容/短视频任务是什么
- 这件事的认知账是什么：你现在最不会判断什么
- 时间账是什么：最耗时间的是选题、脚本、拍摄、素材、剪辑，还是发布
- 经济账是什么：如果请人做、买工具、自己做，大概贵在哪里
- 如果 AI 只能先帮你解决其中一环，你最希望它先解决哪一环
- 你会用什么标准判断它有没有做到「80 分可用」

不用追求方案完整，重点是练习：先把真实成本和判断标准拆清楚，再决定让 AI 做什么。

## 本期Candy

【作业礼包🎁】

【Flag🙌】 这节课做起来很辛苦，希望大家不要辜负。

来来来，希望大家一起立一个Flog（承诺），认真听课吸收，最后完成这次练习作业。

扣一句话吧： 一定作业！！

**看回放/逐字稿 的同学** ， **也要交作业啊！** 你们的反馈真的很重要。

点击作业链接：https://yitang.top/activity/\_Xj6a55db2c52d68/edit

或扫描下方二维码完成作业\~\~

截止时间： **2026年7月21日（周二晚）24:00**

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI俱乐部周三LIVE](../01-AI认知与基本功/05-AI俱乐部周三LIVE.md)

---

<details>
<summary>原文配图上的文字（116 条，图片本身未随文提供）</summary>

**周五课程预告**

- 「高阶建模框架篇」

**付则宇探索AI自动化生成网感短视频**

- 「AI落地Live」 「第六场」 「YiTang.top AI俱乐部」 「一堂第一个十年大会员」 「全景图谱：多角度解读AI数字人」 「行业前沿：探索数字人商业落地」 「底层研究：数字人+ AIGC = ?」
- 「AI落地Live6·数字人专场」 「数字人」 「数字人+电商」 「数字人+直播」
- 「事业前兔似锦」 「《羊了个羊》爆火的」 「2035年开始」 「上市大平台紫燕百味鸡来」
- 付则宇在数字人领域的工作历程。2018 - 2020年，他负责AI数字人课件生成平台；2021 - 2024.5年，参与实时语音驱动动作服务，相关荣誉包括创业黑马数字人加速器孵化等；2024.5至今，专注于CYPER实时Agent Engine类人级互动智能体引擎，与Unity、RTE开发者社区、NVIDIA等合作。图片

**故事开始**

- 「故事开始」
- 「面向语音对话的Agent架构」 「动态响应延迟机制」 「遵循人类口语沟通规律」 「语音交互 + 可视化操作」 「当然最重要的是」
- 「数字人格 - 智能沟通解决方案，结合可视化工具」 「PPT互动助手 - 数字化文旅」
- 「我希望毫不费力地、稳定产出80分口播」
- 「口播王」 「如果一个工具能解决我这种人的问题，那它大概率也能解决一批类似创业者的问题」

**痛点账单**

- AI落地Live82·探索AI自动化生成网感短视频文档中关于AI选题、拍摄、素材、剪辑等环节成本估算的公开依据。内容包括3分钟脚本从构思到修改时间，轻量脚本课程时长，高校短视频课程安排，招聘页面中视频编导、摄影摄像薪资，剪辑师岗位薪资，剪映专业版价格，Pexels和包图网使用授权要求，基础口播拍摄和代剪价格等。这些数据
- 「语音对话 竟有这样的神奇体验」 「数字人格·智能沟通解决方案，结合可视化工具...」
- 「52段原始视频」
- 「我需要一款能够一键生成80分口播质感的工具」

**调研建审美**

- 「mike睿」 「零成本做IP爆改配图Skill」 「最顶级的生意都在售卖这个东西」 「反AI狂潮」
- 「他为什么总能赢」 「大宝说创业」 「大司马聊科技」 「AI红发魔女」 「光仔聊AI」
- 「mike睿」 「全球百亿押注的人形机器人被中国这台机器狗玩坏了！」 「旋转动力」 「半年涨粉3万 6大神器全公开」 「Jacky无限生长」 「AI打破信息茧房」 「耳朵房」
- 「mike睿」 「2026年内容型IP最佳时机」 「钱学森弹道来袭」 「让复杂的问题变简单：逻辑树」 「IP口播智能体」
- 「贴图号全量上线」 「奇点更近」 「我死了却活在了抖音」
- 「mike睿」 「本质上都是长期「大量的投入」 「Codex在电商领域怎么落地使用？」 「AI让把一个博主的所有内容变成你的知识库？」
- 「已处理6m 44s」 「ltaoo/wx_channels_download，能帮我部署一下吗」 「已编辑config.yaml」 「已下载好了」 「它能保留原本视频在视频号的标题作为文件名称吗」
- 「显示更多」
- 「视频分析」 「图片分析」 「文本分析」 「高层住宅定时炸弹」
- 「黄执中」 「如果你曾经学过网络上」 「黄执中的一个成交观念 比100句话术有用太多了！」
- 「AI生成」 「从需求到审美」
- 「美国的VC也喜欢投那些不听劝的疯子」
- 「为我所用」 「处处蒸馏了」 「调研建审美」
- 「辅助研究」 「项目规划」
- 「然后开始接受你的解释」
- 「AI时代」 「调研建审美」
- 「那像企业的一二把手他是能学的」
- 「99%老板的朋友圈=3种烂法」 「结果型」 「PUA型」 「那么喜欢在朋友圈天天」 「调研建审美」
- 「从创造里获取多巴胺」 「Sharpen your thinking. The free and flexible app for your private thoughts.」 「Writing is telepathy」
- 与AI生成网感短视频相关的内容，左侧呈现了两个创意插画及对应文字，插画分别是思考场景、拿着提示词的人物，搭配文字说明使用飞书通用页面、飞书MCP及Agent自动给资源配材等内容；右侧排列了大量风格各异的短视频作品缩略图，涵盖不同风格的人像素材、图文排版内容，直观呈现了AI生成网感短视频的多样成果
- 「做视频别乱装skill搞清楚这六个工具的分」 「素材，但场景更通」 「银行视频、Vlog，都可以让它处理」 「Vlog」 「银行视频」 「完整剪辑」 「但是它更通用」
- 「内容实操」 「举例：结果一问，别人花5w就能装修成你15w的样子，真的假的？」 「吸引观众」
- 「那样一起练习」 「人像半身/全身出镜，结合板书进行口播」
- 「不合理对不对？」
- 「四位顶尖人物的重磅预言 背后藏着巨大的财富机遇」 「只有看懂这4位的顶级预言」 「元德坤创始人 冯观趋势 央视财经嘉宾」 「仅代表个人观点 不代表投资意见」
- 「解方程 x = √(6 + √(x + 6))」 「无人像，有口播语音，素材以AI生成图片/视频的方式进行播放」
- 「一人公司」
- 「香火模式」 「3道→1线→工具→口」 「想要的那个结果」
- 「山门殿」
- 「微软苹果奈飞都在用的GTM方法论」 「其实就四个字体验前置」 「认知觉醒 | 突破成长 | 强者思维 | 商业认知」
- 「信息流含装饰」 「分屏分组」 「信息流分组」 「遵循相互独立、完全穷尽的原则拆分分组」 「张猛杰 - 深度 认真负责的沟通有答案 - 腾讯创新」
- 「越早建团队死得越快」 「盲人摸象与金矿陷阱」
- 「的热爱，本质上都是长期大量的，只要自己足够努力，总有一天能把它挖出来」 「SHEN DU JIN HUA LUN」 「强者思维 内核重构」 「认知进化 心智跃迁」 「深度思考 底层逻辑」
- 「育·见未来」 「人工智能+教育」 「‘人工智能+教育’行动计划：每位教师都需要一个‘教·学·评’协同的‘智能体伙伴’」 「政策释放明确信号：教育转向已然到来」
- 「代码剪辑流」 「智能体本来就更懂Web技术栈」
- 「颠覆建筑设计！浏览器就能做全功能3D建模」 「楼层拆解」
- 「龙虾必备Skill（2）批量产出百万爆款的秘诀是AI“互怼」 「#跟傅盛学AI」 「你看不到那些被骂死的版本」
- 「信我，马上爆单」 「Feature Petrova 电商行业创业者」 「调研建审美」
- 「信息流」 「调研建审美」
- 是AI生成短视频的调研建审美过程。左侧为调研文档，包含对AI生成短视频的描述、AI生成短视频的优缺点分析、AI生成短视频的使用场景等。右侧是AI生成短视频的示例，呈现了多帧画面，展示了不同场景和风格的短视频内容。该图片
- 「READM...」 「核心功能」
- 「从需求到审美」 「调研建审美」
- 「Claude Design刚发布，系统提示词就在GitHub上泄露了，笑不活了」 「Introducing Claude Opus 4.7」
- 「涌跃智能」 「1亿美元！中国AI爆款诞生」 「定位AI时代抖音用户无需编程文字输入想法，AI自动生成内容，支持图像、视频、3D全模态交互」
- 「开源HTML Anything 杀疯」
- 「口播参考素材库：331个参考视频」 「AI #CodeX #企业 #应用」
- 「所谓网感，靠的就是画面节奏」 「网感没有那么玄学」
- 「藏得越深 赚得越多」 「搞到大钱的人」
- 「人物的形象包装」
- 「把这个人物出圈的效」 「人物的形象包装」

**从工具到方案**

- 「从工具到方案」 「看看市面上的工具都能做到什么程度吧」

**调研看工具**

- 「视频类型」 「数字人与声音」 「字幕与音乐」 「一键开启智能成片」
- 「选择数字人」 「选择声音」 「定制我的数字人」 「夜视男」 「情感女性」 「职场精英」 「播音男」 「亲切女生」 「播音女」 「输入文字，选模板，即刻出片」
- 「高级感」 「综艺感」 「本地引」 「双行排版标题内容效果展示」 「香港无社保月领4000养老金」 「2025年数码圈压轴榜单」
- 「爽哥口播智能体」 「如何做口播账号」
- 「1. 学习对标」 「2. 改写文案」 「3. 选择声音」 「4. 选择形象」 「提取文案」 「IP大脑」 「营销文案」 「0.76 复制打开抖音，看看【范爸爸】」
- 「IP打造智能体」 「复刻口播智能体」 「视频生成」 「智能播报」 「那个口播数字人的智能体」
- 「两位数一杯咖啡都不到 真人出镜+日更100条+复刻同行爆款」 「自动提取文案 自动修改内容」 「口播智能体」
- 「数字形象克隆」 「巨推管家」 「AI创作」 「我的AI作品」 「自有作品」 「第一个数字人形象克隆」
- 「普通人如何用AI打造百万粉丝IP」 「一个短视频口播的智能体，899一单」
- 「制作文案」 「制作音频」 「制作视频」 「我们在电脑上打开这个口播智能体啊」
- 「复刻口播智能体」 「12号工作流程」 「666」 「云哥AI播...」 「后台发个方式可以」
- 「怎么学」 「值得学习」 「不是老板没有皮源需要学吗」 「两拉就一杯咖啡都不到」 「自动提取文案」 「自动修改内容」 「我看了好几场他们卖这个智能体的直播，直播间也一直有互动」
- 「巨量引擎」 「小猫蝴蝶蝶」 「多少钱」 「几多元」 「健康码可以装出」
- 「短视频口播智能体」
- 「播智能体#引流获客#个人IP」
- 「sip clf」
- 「HeyGen在八个月内将ARR翻倍，得益于身份优先AI视频的崛起」 「HeyGen突破2亿美元年营收」 「HeyGen突破200M ARR」
- 「miguel - heygen」 「Write HTML. Render video. Built for agents.」 「About」
- 「操作方法超简单」 「HyperFrames 7种最火玩法」 「Codex+ Hyperframes从安装到出片全教程」 「AI全自动做视频」 「AI一键成片」
- 「做视频你知道HyperFrames吗？」 「别再手动剪视频了」 「HyperFrames是AI视频生产...」 「HyperFrames最火5种玩法」 「增强版Hyperframes它来了！」 「HyperFrames火了AI视频开始学HTML？」 「HyperFrames正确使用流程」 「HyperFrames用代码开始HTML」

**网感组件**

- 「超实用音效」 「短视频必备40种音效」 「周Sir商业觉醒IP」
- 「10款网感爆🔥音效」 「艾琳Ailin呀」
- 「背景音乐」 「100首谁用谁火的BGM」 「大刘运营别慌张」
- 「网感组件」 「子寒WING美业获客」
- 「高级感口播用什么字体」 「字体设置」 「大刘运营别慌张」
- 「口播视频」 「自带流量常用字体」 「楠西Nancy表现力...」
- 「88套剪映高级感卡片字幕预设」 「88套剪映高级感卡片字幕预设 精致卡片1100款高级动态口播模板预设 [交易快照]」 「不支持7天无理由」 「加入购物车」 「申请售后」
- 「1000款剪映字幕模版高级感口播动态文字排版预设」 「剪映字幕模板」 「1000款」 「持续更新」 「2000+韩味素材/2000+音效素材」 「加入购物车」 「申请售后」

**从方案到MVP**

- 「从方案到MVP」

**初步验证**

- 「今天能把这bug修复一下」 「这是个重要事项」 「我们这两天在加新的模组，还优化了部分功能」 「最近我看到，手搞了个」 「这几天在做更流畅的视频检索」
- 「让AI为你持续产出有质感、有网感的IP口播视频」 「少一点套路，多一点产出，从想找到现，带你实现文案、配音、拍摄、数字人出镜和自动剪辑」
- 「口播王」 「想做一支什么样的短视频？」 「做一段讲解，针对新人，更有创意和时代感」 「分享素材」 「导入企业已有素材」
- 「口播王」 「生成视频」 「互联网搜索补充材料」 「需求理解」 「创意思路」 「最终文案」
- 「口播王」 「生成内容」 「最近入职，做的是什么」 「有年终奖，钱发了吗」 「IPO有啥样的核心担心」
- 「口播王」 「正在进行语音合成」 「确认生成」
- 「生成视频」
- 「一堂 YiTang.top」 「一堂大会员」

**火山引擎企业认证**

- 「已完成企业实名认证」 「变更企业主体」 「变更企业名称」
- 「请选择登录账号」 「Shuzirenge (ID:2101206980)」 「最近登录」 「企业认证」 「Mikeeyfu (ID:2102313658)」 「服务条款」 「隐私政策」
- 「畅享语音模型体验，一键开通」 「计费规则」 「开通即赠免费礼包」
- 「购买音色」 「豆包声音复刻模型2.0 - 声音复刻」 「声音复刻」 「声音复刻 - 大模型精品声音复刻 - 标准版」 「声音复刻 - 大模型精品声音复刻 - 专业版」

**百度秒哒验证码注册**

- 「一句话 做应用」 「说出你的想法...」 「秒哒时间 - 疯狂个饭硬碰硬」 「我是皇帝」 「阿迪达斯官网」 「易图电商快速出图」
- 「验证消息」 「复制验证码」

**廉价中转站LLM图片大量测试11111**

- 「按次计费」 「暂无描述」
- 多种GPT系列AI模型的相关信息，这些模型都支持按批次计费的请求模式，相较于按token计费的方式，更适配大量测试场景以控制成本。图中可见的模型包括gpt-5.4、gpt-5.5、gpt-5.5-pro、gpt-5.6-luna、gpt-5.6-so1、gpt-5.6-terra，以及gpt-image-2，每个模型都标注了对应的版本，且仅列出了请求相关的基础信息，未展示其他详细描述。这些按次计费

**认知复盘**

- 「一堂双三角·AI时代的竞争力模型」 「人类三角×AI三角」 「创造力」 「同样都会用AI，为什么不同人、业务结果相差这么大？」 「同样都是业务高手，AI结果相差这么大？」

**AI的边界**

- 「AI降低的是执行成本，不是判断成本」 「AI的边界」

**关于审美**

- 「审美负责定义结果 体系负责让结果重复发生」
- 「AI让试错变快，也会让错误方向跑得更远」 「审美负责定义结果，体系负责让结果重复发生」

**作业和Candy奖励**

- 「作业和Candy奖励」

**本期Candy**

- 「一定挑战！」 「本期Candy」

</details>
