---
title: AI落地Live36·编程工具Windsurf+视频号AI工具
node_token: P7u5wwLI1iZtLXkWY2mcJbRXn7E
source: https://www.feishu.cn/wiki/P7u5wwLI1iZtLXkWY2mcJbRXn7E
space: 一堂学习
obj_type: docx
synced: 2026-09-25 19:41
course_line: AI能力线
stage: AI业务落地
train: AI业务落地
form: 直播逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
Hello，大家好啊，欢迎来到**一堂AI俱乐部**·**落地Live分享**。

我是于陆，你们的AI探索伙伴，好久不见\~

> **新同学看这里，**你需要知道的内容都在这里！
> ①**《AI俱乐部新人指南》**文稿链接：
> https://yitanger.feishu.cn/docx/Zz9tds3HtoRGmNx2eoxcL8GbnUt
> ②**《AI俱乐部新人指南》**回放链接：
> https://air.yitang.top/live/w8HDGvkmT6?part=AI%E4%BF%B1%E4%B9%90%E9%83%A8%E5%BF%85%E8%AF%BB%E6%8C%87%E5%8D%97&rs=5431

如果高清流卡，就换流畅\~

今天时间比较紧，熙熙为了分享认真准备了很长时间，我也想听，所以今天可能会先快速过一遍，然后根据大家反馈再重点展开。

# 新工具、新项目、新模型

## Kimi（视觉思考版）

https://kimi.moonshot.cn/kimiplus/crm40ee9e5jvhsn7ptcg

## OpenAI 12天 新品发布会

https://openai.com/12-days/

一场"非典型"发布会：

•架个摄像头，几个人一坐

•连续12天，每天不一样

新模型+新产品+新功能，每一个都在其领域是重磅的内容，刚到第10天还没结束，毕竟是领头羊，肯定会对很多的产品带来影响，可以稍微关注一下，或者等下周发布完的汇总。

比较有意思的是，这种形式，**线上产品发布会MVP？**

非常想知道是怎么决策的，ROI怎么算的。

## Gemini 2.0 Flash

https://aistudio.google.com/prompts/new*\_chat*

轻度试用了一下，还是比较强的，GPT o1的水平，趁免费赶紧用(薅)。

## Github Copilot免费？

 感谢晨波分享的新鲜消息

## 您的程序员Devin已上线

3600一个月，要雇一个Devin吗？

估计有同学又说了，怎么又是编程，我也不会啊，跟我也没什么关系。

那么再推荐一个课程吧，真的非常精彩，这一小时的ROI非常正。

## 吴恩达：人工智能 Python 初学者指南

 https://www.deeplearning.ai/short-courses/ai-python-for-beginners

这是DeepLearning.AI平台上“人工智能Python初学者指南”课程的介绍页面，课程导师为Andrew Ng。页面主视觉区域配有对应课程的讲师介绍视频，课程时长共4小时15分钟，课程核心内容包含学习Python编程基础、AI工具操作等，相关链接对应吴恩达的该课程官方页面，页面还标注了可点击免费注册参与课程。

快速看了一下整个内容，称得上是深入浅出，不论你的基础如何，如果愿意花4小时听完，再加以练习，可以说市面上大部分的开源AI项目你都能跑起来了。

唯一的卡点可能是全英文，别着急，先看B站中文版，第一部分已经有全中文版，如果真的感兴趣，先从这1小时内容开始吧。学会之后，举一反三后面的部分甚至可以自己摸索。

 https://www.bilibili.com/video/BV1B5pweDE1w

刚刚讲到Github Copiot和吴恩达的Python教程，再来看个重磅的。

## 干翻Cursor的AI编程神器？

我翻了下最近的分享，神级提示词就用了两次，这次又来编程神器？

还别说，真的很神\~

这个工具上次就想分享，但是觉得没有自己实践，缺信息，这次终于补上了。

https://codeium.com/windsurf/download

更多信息可以参考这篇公众号文章。

 https://mp.weixin.qq.com/s/8VYkAxA73JcRaUZ7MoNKcA

 强烈推荐一试，尤其是在用Cursor或者Github Copolit的伙伴。

## 分享两个我的实践。

提示词：

帮我生成一个网页，内容是最基础的计算器功能

>
>
> <!DOCTYPE html>
>
> <html lang="en">
>
> <head>
>
>     <meta charset="UTF-8">
>
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>
>     >
>     <style>
>
>         body {
>
>             display: flex;
>
>             justify-content: center;
>
>             align-items: center;
>
>             height: 100vh;
>
>             margin: 0;
>
>             font-family: Arial, sans-serif;
>
>             background-color: #f0f0f0;
>
>         }
>
>         .calculator {
>
>             background-color: #fff;
>
>             padding: 20px;
>
>             border-radius: 10px;
>
>             box-shadow: 0 0 10px rgba(0,0,0,0.1);
>
>         }
>
>         #display {
>
>             width: 100%;
>
>             height: 40px;
>
>             margin-bottom: 10px;
>
>             font-size: 20px;
>
>             text-align: right;
>
>             padding: 5px;
>
>             box-sizing: border-box;
>
>             border: 1px solid #ddd;
>
>             border-radius: 5px;
>
>         }
>
>         .buttons {
>
>             display: grid;
>
>             grid-template-columns: repeat(4, 1fr);
>
>             gap: 5px;
>
>         }
>
>         button {
>
>             padding: 15px;
>
>             font-size: 18px;
>
>             border: none;
>
>             border-radius: 5px;
>
>             cursor: pointer;
>
>             background-color: #f8f9fa;
>
>         }
>
>         button:hover {
>
>             background-color: #e9ecef;
>
>         }
>
>         .operator {
>
>             background-color: #ffd700;
>
>         }
>
>         .equals {
>
>             background-color: #4CAF50;
>
>             color: white;
>
>         }
>
>         .clear {
>
>             background-color: #ff4444;
>
>             color: white;
>
>         }
>
>     </style>
>
> </head>
>
> <body>
>
>     <div class="calculator">
>
>         <input type="text" id="display" readonly>
>
>         <div class="buttons">
>
>             C
>
>             (
>
>             )
>
>             /
>
>
>
>             7
>
>             8
>
>             9
>
>             ×
>
>
>
>             4
>
>             5
>
>             6
>
>             -
>
>
>
>             1
>
>             2
>
>             3
>
>             +
>
>
>
>             0
>
>             .
>
>             =
>
>         </div>
>
>     </div>
>
>
>
>     <script>
>
>         let display = document.getElementById('display');
>
>
>
>         function appendToDisplay(value) {
>
>             display.value += value;
>
>         }
>
>
>
>         function clearDisplay() {
>
>             display.value = '';
>
>         }
>
>
>
>         function calculate() {
>
>             try {
>
>                 display.value = eval(display.value);
>
>             } catch (error) {
>
>                 display.value = 'Error';
>
>             }
>
>         }
>
>     </script>
>
> </body>
>
> </html>

熟悉网页结构的同学会知道，现在所有内容在一起，不够好，那么要求AI给我分开。

果然也做到了。

**HTML文件**

>
>
> <!DOCTYPE html>
>
> <html lang="en">
>
> <head>
>
>     <meta charset="UTF-8">
>
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>
>     >
>     <link rel="stylesheet" href="styles.css">
>
> </head>
>
> <body>
>
>     <div class="calculator">
>
>         <input type="text" id="display" readonly>
>
>         <div class="buttons">
>
>             C
>
>             (
>
>             )
>
>             /
>
>
>
>             7
>
>             8
>
>             9
>
>             ×
>
>
>
>             4
>
>             5
>
>             6
>
>             -
>
>
>
>             1
>
>             2
>
>             3
>
>             +
>
>
>
>             0
>
>             .
>
>             =
>
>         </div>
>
>     </div>
>
>     <script src="script.js"></script>
>
> </body>
>
> </html>

**JavaScript文件**

> document.addEventListener('DOMContentLoaded', () => {
>
>     const display = document.getElementById('display');
>
>
>
>     *// Add click event listeners to all buttons*
>
>     document.querySelectorAll('.buttons button').forEach(button => {
>
>         button.addEventListener('click', () => {
>
>             if (button.classList.contains('clear')) {
>
>                 clearDisplay();
>
>             } else if (button.classList.contains('equals')) {
>
>                 calculate();
>
>             } else {
>
>                 appendToDisplay(button.textContent);
>
>             }
>
>         });
>
>     });
>
>
>
>     *// Handle keyboard input*
>
>     document.addEventListener('keydown', (event) => {
>
>         if (event.key >= '0' && event.key <= '9' || '+-\*/.()'.includes(event.key)) {
>
>             appendToDisplay(event.key);
>
>         } else if (event.key === 'Enter') {
>
>             calculate();
>
>         } else if (event.key === 'Escape') {
>
>             clearDisplay();
>
>         } else if (event.key === 'Backspace') {
>
>             display.value = display.value.slice(0, -1);
>
>         }
>
>     });
>
> });
>
>
>
> function appendToDisplay(value) {
>
>     const display = document.getElementById('display');
>
>     if (display.value === 'Error') {
>
>         display.value = '';
>
>     }
>
>     display.value += value;
>
> }
>
>
>
> function clearDisplay() {
>
>     document.getElementById('display').value = '';
>
> }
>
>
>
> function calculate() {
>
>     const display = document.getElementById('display');
>
>     try {
>
>         *// Replace × with \* for evaluation*
>
>         const expression = display.value.replace(/×/g, '\*');
>
>         const result = eval(expression);
>
>         display.value = Number.isInteger(result) ? result : result.toFixed(8).replace(/\\.?0+\$/, '');
>
>     } catch (error) {
>
>         display.value = 'Error';
>
>     }
>
> }

**Css样式文件**

> body {
>
>     display: flex;
>
>     justify-content: center;
>
>     align-items: center;
>
>     height: 100vh;
>
>     margin: 0;
>
>     font-family: Arial, sans-serif;
>
>     background-color: #f0f0f0;
>
> }
>
>
>
> .calculator {
>
>     background-color: #fff;
>
>     padding: 20px;
>
>     border-radius: 10px;
>
>     box-shadow: 0 0 10px rgba(0,0,0,0.1);
>
> }
>
>
>
> #display {
>
>     width: 100%;
>
>     height: 40px;
>
>     margin-bottom: 10px;
>
>     font-size: 20px;
>
>     text-align: right;
>
>     padding: 5px;
>
>     box-sizing: border-box;
>
>     border: 1px solid #ddd;
>
>     border-radius: 5px;
>
> }
>
>
>
> .buttons {
>
>     display: grid;
>
>     grid-template-columns: repeat(4, 1fr);
>
>     gap: 5px;
>
> }
>
>
>
> button {
>
>     padding: 15px;
>
>     font-size: 18px;
>
>     border: none;
>
>     border-radius: 5px;
>
>     cursor: pointer;
>
>     background-color: #f8f9fa;
>
>     transition: background-color 0.2s;
>
> }
>
>
>
> button:hover {
>
>     background-color: #e9ecef;
>
> }
>
>
>
> .operator {
>
>     background-color: #ffd700;
>
> }
>
>
>
> .equals {
>
>     background-color: #4CAF50;
>
>     color: white;
>
> }
>
>
>
> .clear {
>
>     background-color: #ff4444;
>
>     color: white;
>
> }

但是出现了数字出现两次的bug，直接要求修改。

这不过就是Claude还有ChatGPT刚刚发布的能力吗，很常见啊。

再来一个稍微复杂点的案例，试了一个小爬虫。

一个真实的需求：每天信息量太大了，各种新闻、论坛、博客、公众号，都有很多的信息，根本看不过来。

**【互动🙋🏻‍♀️】**怎么办？

写个爬虫帮我来抓数据，提炼出来其中最重要的部分，英文给我翻译成中文，整理好给我，最好还能转化成音频念给我，这样上班路上顺带就听完了。

需求：

~~1.抓取网站信息~~

~~2.英文翻译成中文~~

3.归纳整理摘要

~~4.转化成音频~~

**【思考💡】**有开发经验的同学可以估算一下，你们觉得需要多长时间的开发，尽量用现成的库来实现的话。

————

如果是两年前的我，没写过爬虫，摸摸现成的开源库，快了半天调通一个点，慢了一天差不多，整体两三天怎么也要有的。

看看Windsurf的表演。

就这么简单的一句提示词。

然后：

刚刚的只有链接，没有具体的文章，同时把文章翻译成中文。

 JSON

{

  "original_title": "Open partners with Will Smith on social commerce merch on Open SuperApp",

  "translated_title": "Open 与 Will Smith 合作开发 Open SuperApp 上的社交商务商品",

  "original_text": "Join our daily and weekly newsletters for the latest updates and exclusive content on industry-leading AI coverage. Learn More\n\nOpen announced that its social commerce Open SuperApp is launching a partnership with actor and artist Will Smith.\n\nThe Open SuperApp will serve as the exclusive merchandise platform for Smith’s 2025 World Tour starting with an intimate pop-up concert show in San Diego, California, on December 11 and December 12.\n\nLos Angeles-based Open, which raised \$28 million last year, has created a SuperApp that combines\n\nsocial commerce, messaging, creator community, and AI into one ad-free platform, said Jaeson Ma, CEO of Open, in an interview with GamesBeat.\n\nSmith’s first concert event is at The Observatory North Park in San Diego, featuring exclusive hoodies, tees, and hats. Additionally, Smith’s merch website for his world tour will be powered by Open. This kind of tech could be re-used with a variety of creators and celebrities across industries.\n\nThe partnership introduces a merchandise model that eliminates the need to pre-order inventory and enables worldwide shipping through the Open SuperApp. Fans at the San Diego pop-up show will experience an innovative merchandising approach, with a unique QR code displayed surrounding the merchandise tables and on digital screens guiding them to the Open SuperApp web store, where they can explore and purchase Will Smith’s exclusive tour merchandise, allowing fans to purchase merch on-site and having them shipped directly to them.\n\n“Our partnership with Will Smith exemplifies OPEN’s mission to empower creators to connect\n\nwith fans through innovative, seamless experiences,” said Ma. “By reimagining the merchandise model, we’re not only streamlining production but also creating a platform that enhances the overall shopping experience.”\n\nKosaku Yada, CEO at Westbrook, Smith’s investment arm and an early investor in Open, said in a statement, “Will is always looking for innovative ways to connect with his global fanbase and providing an online shop to compliment his in-person merchandise stands to offer an opportunity for everyone to shop seamlessly anywhere in the world.”\n\nThe Open SuperApp aims to redefine merchandise distribution for artists and creators by introducing a\n\nplatform that eliminates traditional inventory and logistical barriers. By providing a global, on-demand merchandise solution, Open enables artists like Will Smith to offer fans premium, limited-edition products with ease and reach. The platform’s innovative approach allows for direct artist-to-fan connections, transforming how merchandise is conceived, produced, and distributed worldwide.\n\nOpen empowers creators to build their own businesses, engage directly with fans, and maintain ownership of their data and brand, revolutionizing the creator economy by providing a comprehensive suite of tools in one user-friendly platform. Open’s recent collaborations include launching a lifestyle and clothing line from current University of Florida quarterback DJ Lagway, and merchandise drop with Coolman, a popular artist known for his surreal and humorously simplistic animations.\n\nMa explained that the company has developed a global supply chain and proprietary tech that enables it to forego the risks of buying inventory ahead of time.\n\nMa said the idea is focused around social commerce, combining social media and ecommerce. It’s an idea that Ma imported from Asia, where such integrated social networking and commerce are common.\n\nOpen was focused non-fungible tokens (NFTs) as a company when it was founded in 2020. Along the way, Open pivoted to becoming a social commerce and supply chain company for creators and their superfans. It has raised \$38 million to date in two rounds. The commerce side of the business isn’t easy. Ma said the company has connections to 10,000 manufacturers who can supply goods for the Open SuperApp as needed.\n\nThe Open SuperApp stands at the forefront of this collaboration, allowing for the rapid creation\n\nof premium products through simple prompts. Their cutting-edge generative AI text-to-product\n\ntechnology not only streamlines the production process but also opens up new possibilities for\n\npersonalized merchandise in the creator economy.\n\nOpen’s pioneering generative AI text-to-product technology also enables the creation of physical products from text descriptions. Users can input a text prompt describing a desired item, and the AI system generates a design that can be manufactured into a physical product.\n\nBecause of this, Open’s technology allowed for the quick design and production of merch based on any given campaign’s concept, significantly speeding up the process from idea to finished product.\n\nOpen empowers creators to build their own businesses, engage directly with fans, and maintain ownership of their data and brand, revolutionizing the creator economy by providing a comprehensive suite of tools in one user-friendly platform.\n\nOpen’s recent collaborations include launching a lifestyle and clothing line from current University of Florida quarterback DJ Lagway, and an upcoming product drop with Coolman, a popular artist known for his surreal and humorously simplistic animations.\n\nMa said his passion has been to bridge East and West, and this business is similar in that respect. Social commerce on various platforms has been growing in Asia, and Ma wants to apply the learnings in the West, starting with celebrities like Smith. Ma has come up with a supply-chain solution that makes the merchandise business less risky and able to create merch on demand as celebrities like Smith make a splash on the social commerce app. And the goal is to create manufacturing runs that meet demand for a given product without going too far above what is needed to ship in a timely manner. This where some more sophisticated AI technology can be brought to bear, Ma said.\n\n\n\n“Social commerce has been happening in Asia for the last 10 plus years,” Ma said. “We’re also seeing ecommerce disruption on the backend.”\n\nPart of the thinking is the belief that creators and celebrities need to be rewarded more for their work and that coming up with new models like social commerce can help creation and artistry pay off better and faster. And a platform should also connect celebrities and creators with fans on different levels, from ordinary fans to the super fans.\n\nThe company has 50 people.\n\n“We’re solving for design with AI, no inventory, drop-ship manufacturing, supply chain logistics, payments,” he said. “No platforms are doing that. And it’s hard. We’re literally doing something that no one else is doing.”",

  "translated_text": "加入我们的每日和每周时事通讯，了解有关行业领先人工智能报道的最新更新和独家内容。了解更多\n\nOpen 宣布其社交商务 Open SuperApp 正在与演员兼艺术家威尔·史密斯 (Will Smith) 建立合作伙伴关系。\n\nOpen SuperApp 将作为史密斯 2025 年世界巡演的独家商品平台，以 12 月 11 日和 12 月 12 日在加利福尼亚州圣地亚哥举办的一场亲密的快闪音乐会开始。\n\n总部位于洛杉矶的 Open 去年筹集了 2800 万美元，创建了一个超级应用程序，该应用程序结合了\n\nOpen 首席执行官 Jaeson Ma 在接受 GamesBeat 采访时表示，将社交商务、消息传递、创作者社区和人工智能整合到一个无广告平台中。\n\n史密斯的首场音乐会活动在圣地亚哥北天文台举行，其中包括独家连帽衫、T 恤和帽子。此外，史密斯世界巡演的商品网站将由 Open 提供支持。这种技术可以被各行业的各种创作者和名人重复使用。\n\n此次合作推出了一种商品模型，无需预订库存，并可通过 Open SuperApp 在全球范围内发货。圣地亚哥快闪秀的粉丝将体验创新的营销方式，商品桌周围和数字屏幕上显示独特的二维码，引导他们前往 Open SuperApp 网上商店，在那里他们可以探索和购买威尔·史密斯的独家巡演商品，允许粉丝现场购买商品并直接运送给他们。\n\n“我们与威尔·史密斯的合作体现了 OPEN 的使命，即让创作者能够相互联系\n\n通过创新、无缝的体验与粉丝互动。”马云说道。 “通过重新构想商品模型，我们不仅简化了生产，还创建了一个增强整体购物体验的平台。”\n\n史密斯的投资部门 Westbrook 的首席执行官兼 Open 的早期投资者 Kosaku Yada 在一份声明中表示：“威尔一直在寻找创新的方式来与他的全球粉丝群建立联系，并提供一个在线商店来赞美他的实体商品。为每个人提供在世界任何地方无缝购物的机会。”\n\nOpen SuperApp 旨在通过引入\n\n消除传统库存和物流障碍的平台。通过提供全球性的按需商品解决方案，Open 使像威尔·史密斯这样的艺术家能够轻松、方便地为粉丝提供优质的限量版产品。该平台的创新方法允许艺术家与粉丝直接联系，改变商品在全球范围内的构思、生产和分销方式。\n\nOpen 使创作者能够建立自己的业务，直接与粉丝互动，并维护其数据和品牌的所有权，通过在一个用户友好的平台中提供一整套工具，彻底改变创作者经济。 Open 最近的合作包括推出由现任佛罗里达大学四分卫 DJ Lagway 推出的生活方式和服装系列，以及与以超现实和幽默简单的动画而闻名的流行艺术家 Coolman 合作推出的商品。\n\n马云解释说，该公司已经开发了全球供应链和专有技术，使其能够放弃提前购买库存的风险。\n\n马云表示，这个想法的重点是社交商务，将社交媒体和电子商务结合起来。这是马云从亚洲引入的一个想法，这种集成的社交网络和商业在亚洲很常见。\n\nOpen 于 2020 年成立时，是一家专注于不可替代代币 (NFT) 的公司。一路走来，Open 逐渐成为一家为创作者及其超级粉丝服务的社交商务和供应链公司。迄今为止，它已通过两轮融资筹集了 3800 万美元。商业方面的业务并不容易。马云表示，该公司与 10,000 家制造商有联系，可以根据需要为 Open SuperApp 供应商品。\n\nOpen SuperApp 处于此次合作的最前沿，可实现快速创建\n\n通过简单的提示即可获得优质产品。他们最先进的生成人工智能文本到产品\n\n技术不仅简化了生产流程，还开辟了新的可能性\n\n创造者经济中的个性化商品。\n\nOpen 开创性的生成式 AI 文本到产品技术还可以根据文本描述创建实体产品。用户可以输入描述所需物品的文本提示，人工智能系统会生成可以制造成实体产品的设计。\n\n因此，Open 的技术可以根据任何给定的活动概念快速设计和生产商品，从而显着加快从创意到成品的过程。\n\nOpen 使创作者能够建立自己的业务，直接与粉丝互动，并维护其数据和品牌的所有权，通过在一个用户友好的平台中提供一整套工具，彻底改变创作者经济。\n\nOpen 最近的合作包括推出由现任佛罗里达大学四分卫 DJ Lagway 推出的生活方式和服装系列，以及即将与以超现实和幽默简单的动画而闻名的流行艺术家 Coolman 合作推出的产品。\n\n马云表示，他的热情一直是在东西方之间架起桥梁，而这项业务在这方面是相似的。各种平台上的社交商务在亚洲不断发展，马云希望将所学到的知识应用到西方，首先是史密斯这样的名人。马云提出了一种供应链解决方案，可以降低商品业务的风险，并且能够随着史密斯等名人在社交商务应用程序上引起轰动，按需创建商品。我们的目标是创建满足特定产品需求的生产运行，但又不会超出及时发货所需的水平。马云说，这可以发挥一些更复杂的人工智能技术的作用。\n\n\n\n“过去十多年来，社交商务一直在亚洲发生，”马云说。 “我们还看到后端电子商务受到破坏。”\n\n部分想法是相信创作者和名人的工作需要获得更多奖励，并且提出社交商务等新模式可以帮助创作和艺术更好更快地获得回报。平台还应该将名人、创作者与不同层次的粉丝（从普通粉丝到超级粉丝）联系起来。\n\n公司现有员工50人。\n\n“我们正在解决人工智能设计、无库存、直运制造、供应链物流、支付等问题，”他说。 “没有平台这样做。这很难。我们实际上正在做其他人没有做过的事情。”",

  "original_summary": "Learn MoreOpen announced that its social commerce Open SuperApp is launching a partnership with actor and artist Will Smith.\nThe partnership introduces a merchandise model that eliminates the need to pre-order inventory and enables worldwide shipping through the Open SuperApp.\nMa said the idea is focused around social commerce, combining social media and ecommerce.\nAlong the way, Open pivoted to becoming a social commerce and supply chain company for creators and their superfans.\nThe Open SuperApp stands at the forefront of this collaboration, allowing for the rapid creationof premium products through simple prompts.",

  "translated_summary": "了解更多Open 宣布其社交商务 Open SuperApp 正在与演员兼艺术家威尔·史密斯 (Will Smith) 建立合作伙伴关系。\n此次合作推出了一种商品模型，无需预订库存，并可通过 Open SuperApp 在全球范围内发货。\n马云表示，这个想法的重点是社交商务，将社交媒体和电子商务结合起来。\n一路走来，Open 逐渐成为一家为创作者及其超级粉丝服务的社交商务和供应链公司。\nOpen SuperApp 处于此次合作的最前沿，允许通过简单的提示快速创建优质产品。",

  "keywords": [

    "partners",

    "superapp",

    "commerce",

    "creators",

    "open",

    "platform",

    "fans",

    "social",

    "ai",

    "merch",

    "smith",

    "merchandise",

    "ma"

  ],

  "publish_date": "2024-12-11 14:30:00+00:00",

  "top_image": "https://venturebeat.com/wp-content/uploads/2024/07/Will-Smith-Dec-11_12-Merch-Mockups-1.jpg?w=1024?w=1200&strip=all",

  "url": "https://venturebeat.com/games/open-partners-with-will-smith-on-social-commerce-merch-on-open-superapp/",

  "crawl_time": "2024-12-18T12:50:33.687801"

}

将文字转换成语音。

视频仅支持MP4格式

视频仅支持MP4格式

几个重要的需求都搞定了。

1.~~抓取网站信息~~

2.~~英文翻译成中文~~

3.归纳整理摘要

4.~~转化成音频~~

到这时候，从下载安装，只过去了20分钟。。。

写个Java库，也没问题。

写一个java库，读取硬盘指定目录下的文件，找出其中重复的文件，并且写一个测试用例

右下角切换到Chat模式，当个大语言模型用也是ok的。

哪个最先进？哪个会形成主流？

**【思考💡】**Cursor？ Devin？ Copolit？ Windsurf？辅助开发 还是 独立程序员？

————

这张是名为“AI x 开发 探索Beta版”的内容表格，核心梳理了不同AI开发工具的相关分类信息。表格从分级、典型工具、能力、举例、成本、难点六个维度展开：分级包含生成、辅助、进阶、终极四个类别，对应典型工具如ChatGPT、Github Copilot、Windsurf、Devin等；明确了不同工具的能力定位、对应的使用示例，标注了工具的成本区间，还指出了各类工具使用时面临的难点，下方备注为粗略统计且为长期优化的内容。

看一下这两个图，还挺中肯的。。。

说回来，Windsurf的体验是我用过这么多工具中，最好的，对新人小白最友好的，所有的东西统一在一起，最后能形成完整的交付，遇到任何问题直接问，一般都能解决。

实践中的**卡点**：

1.**基础编程/项目认知**：自学，比如吴恩达课程

2.**英文界面**

3.**执行环境**：Windows 了解 CMD、PowerShell，Mac 了解 终端；会安装Python语言环境。

4.**Git思维**：自学

5.**文件夹问题**：每次新建

先叠个甲，因为视频号我是新手，也是在探索的案主，下面内容是根据过往经验总结，还需要大量的共建，还有专家反馈，请同学们共同迭代。

# 视频号大航海 x AI

**【互动🙋🏻‍♀️】**先统计一下哈，看看同学们有多少人参加？

报名大航海的案主 扣1

报名大航海的创客 扣2

————

AI俱乐部，肯定要考虑人工智能的因素，先看一个AI生成内容的最佳实践。

**【互动🙋🏻‍♀️】**感觉怎么样？

除了哪些用AI"恶搞"的，还有很多非常优秀的作品。

 这个内容块暂不支持，请联系教研修改

 这个内容块暂不支持，请联系教研修改

这个内容块暂不支持，请联系教研修改

如果说你想做一个，主要是AI生成内容的视频号的话，下面是另一个重要的**最佳实践。**

## AI春晚拆解

https://www.bilibili.com/video/BV15v421k7PY

**认知**

1.**全局视角**：确认想要传递给观众的内容主题，设计好衔接，分配好节目顺序

2.**内容流程**：每期春晚都是一个最佳实践，包括AI春晚

3.**部分创新**：可以利用原有的歌曲，视频，等内容综合创作

4.**剧本分镜**：**核心能力**，好的内容，对质量有直接影响 #大师可以用手机拍出传世之作

a.可以用Agent和提示词做一个1.0

5.**时间长度**：大部分都很简单，可以消除长视频带来的不适感，只有相声9分钟，MV稍长，其他普遍1/2分钟

6.**创意为王**：真实、虚幻，动画、真人，现在、未来、过去，怎么在几分钟内混合不同维度的内容，贴合主题

我还拆了一下用到的工具。

**使用技术/工具**

约50个有说明的作品使用的工具统计

<table><colgroup><col/><col/><col/><col/><col/></colgroup><tbody><tr><td><b>类型</b>  </td><td><b>二级分类</b>  </td><td><b>工具及使用次数</b>  </td><td><b>技术门槛&amp;可能解法</b>  </td><td><b>卡点</b>  </td></tr><tr><td><b>文字</b>
 </td><td>脚本/文本/分镜
 使用大语言模型，生成作品的文字部分
 </td><td>1.ChatGPT 24
2.通义千问 4
3.智谱清言 3
4.Kimi 3
5.豆包 2
6.Perplexity 1
7.Claude 1  </td><td><b>提示词 难度☆☆☆</b>
解法：可以通过Agent或者批发提示词，大大提升产出质量
 </td><td>1.对视频作品的基础认知，比如框架、结构、情节等
2.对最佳实践的审美  </td></tr><tr><td rowspan="2"><b>图像</b>  </td><td>图像生成
 </td><td>1.Midjourney 25
2.Stable Diffusion 12
3.DALL·E3 7
4.Wonder AI 1  </td><td><b>提示词 难度☆☆☆☆</b>
解法：可以通过Agent或者批发提示词，大大提升产出质量

<b>工具使用 难度☆☆☆☆</b>
1.Midjourney需要科学上网+付费
2.SD使用需要培训
解法：崔磊的AI刻意练习  </td><td>1.不付费可用的资源有限
2.对最佳实践的审美
3.图像匹配文字  </td></tr><tr><td>图像编辑  </td><td>1.PS 4
2.Magnific(无损放大) 2
3.美图秀秀 1  </td><td><b>工具使用 难度☆☆☆</b>
解法：抠图、效果等培训教程  </td><td> </td></tr><tr><td rowspan="2"><b>视频</b>
 </td><td>视频生成  </td><td>1.Runway 18
2.Pixverse 14
3.StableVideo Diffusion 5
4.DemoAl 3
5.Pika 2
6.D-ID 1
7.Kaiber 1
8.千象 1  </td><td><b>工具使用 难度☆☆☆</b>
1.Midjourney需要科学上网+付费
2.SD使用需要培训
 </td><td>1.不付费可用的资源有限
2.对最佳实践的审美
3.视频匹配文字  </td></tr><tr><td>视频剪辑  </td><td>1.剪映 27
2.PR 3
3.iMovie 1  </td><td><b>工具使用 难度☆☆</b>
解法：动态、字幕、效果等培训教程
 </td><td> </td></tr><tr><td rowspan="2"><b>音频</b>  </td><td>音频生成  </td><td>1.GPT-SoVITS 4
2.Suno 4
3.WAV2LIP 2
4.Eleven labs(声音训练) 2   </td><td><b>开发技术 难度☆☆☆☆</b>
除Suno外，其他都需要一定的开发基础，较难。  </td><td> </td></tr><tr><td>音频剪辑  </td><td>1.ACE Studio 1
2.Meta Audio Craft 1  </td><td><b>工具使用 难度☆☆</b>
解法：动态、字幕、效果等培训教程  </td><td> </td></tr><tr><td rowspan="3"><b>其他</b>  </td><td>数字人  </td><td>1.Heygen 5  </td><td><b>工具使用 难度☆☆</b>
需要科学上网   </td><td> </td></tr><tr><td>工作流工具  </td><td>1.COMFYUI 1  </td><td><b>开发技术 难度☆☆☆☆</b>
功能强大，但是需要一定的部署能力  </td><td> </td></tr><tr><td>3D效果  </td><td>1.LumaAl 1  </td><td><b>工具使用 难度☆☆☆</b>  </td><td> </td></tr></tbody></table>

电子酒同学2025年的春晚已经进行过半，也有一堂同学参与，可以期待一下。

## AI工具整理（一）

**分层一：通用型工具**

1.调研工具

2.案主业务相关的提示词

3.AI+知识库

**分层二：功能型工具**

1.音频：FishAudio https://fish.audio/zh-CN/，GPT-SoVITS，Suno，Clone-voice

2.视频：Runway、可灵、Vidu、Pixverse

3.图像：Midjourney，Stable Diffusion，国内MJ平替TensAI，SD平替liblib.art，**豆包生图**

 用我的邀请码，免费3天VIP https://ai.tensgpt.com/?invite_code=5l1JaO

**分层三：内容型工具**

**【互动🙋🏻‍♀️】**这张小抄大家都看过吗？

熙熙整理的真好。

**A.图文工具+B.不出镜**

https:*//icraft.gantcloud.com/zh-CN*

https:*//www.readkidz.com/*

**C.观点输出**

1.AI+知识库，你的历史资料整理成口播稿

2.新闻抓取-输出内容

**D.问答互动**

1.快速分析对方表达

2.提前设计问题列表

**E.采访**

1.设计题目

2.模拟采访

**F.vlog**

1.用大模型设计脚本

**G.演绎**

1.用大模型设计剧情

2.给脚本打分

**H.AI技术**

参考上面的拆解表格。

1.Domo AI 视频转动漫

2.Story小说转视频

3.Manim Community

作为一个案主，我大胆的假设：

**假设一：**AI落地Live拆成两个部分，日常视频号+Live主要是案例

**假设二：**自动化完成AI大航海视频生成

**【思考💡】**大家帮我想想哈，多提假设，也找创客hhh

# 听歌点赞

AI俱乐部举办的**提示词大赛，正在评选中**，我们这次内部做了一个初步筛选，从50多首参赛歌曲中，挑选出了相对完整且比较有趣的二十多首作品，请大家共同参与评选。

**评选方式**：请所有一堂同学，去听听同学们的作品，觉得好听的留个言，收藏一下；最后我们将根据上榜作品的**播放量、评论、收藏、分享**等等数据，综合进行评比选出获奖者。

更多作品在这个收藏列表里面：https://music.163.com/#/my/m/music/playlist?id=12982197907

# 作业和Candy

## 本次作业

**题目一：实操题**

对于从来没写过代码，也不熟悉其他工具的同学，突破自我，下载Windsurf安装吧，写个网页游戏，写个文件处理，把需求和过程，以及结果和评价都贴在这里。

对于写过代码，或者用过之前的工具，或者已经用过Windsurf工具的同学，请你们再找一个实践的例子吧，把需求和过程，以及结果和评价都贴在这里。

（为了鼓励大家，需求、过程、结果、评价，都完整的认真作业5分起）

**题目二：在视频号执行中，好用的AI工具（共建）**

最好是今天分享没有说过的，并且你在实践中真正好用的工具。说说你实践的过程，以及你对工具的评价。

（为了鼓励大家，过程完整，真实有用的作业5分起）

 两个都不错就6分\~

**题目三：大航海需要支持的AI工具/技能（需求问卷）**

说说你最大的困扰，并且可能用AI工具可以解决的。

给一个参考句式：

**大航海我是案主**，我在XXXXXX赛道/业务/项目，我的短视频类型可能是XXXXXX，我最大的卡点是XXXXXX，希望有AI工具能帮忙解决。

**大航海我是创客**，案主是XXXXXX赛道/业务/项目，我负责XXXXXX部分的探索，我最大的卡点是XXXXXX，希望有AI工具能帮忙解决。

## 本期Candy

【🎁Candy**】**

1.本次分享的可部分复制的一堂Doc文档\~

2.同学共建的工具更新版

【Flag🙋】

来来来，希望大家一起立一个Flag（承诺），认真吸收，最后完成这次训练。

扣一句话吧：一定挑战！！

**看回放/逐字稿的同学**，**也要交作业啊！**你们的反馈真的很重要。

点击作业链接：https://yitang.top/activity/jaT6763b84c432c1/edit

或扫描下方二维码完成作业\~\~

截止时间：**2024年12月24日（周二晚）24:00**

一定挑战，一定作业！\~

📌**任何遇到的问题都可以用作业告诉我，我都会认真看的**

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI俱乐部周三LIVE](../01-AI认知与基本功/05-AI俱乐部周三LIVE.md)

---

<details>
<summary>原文配图上的文字（71 条，图片本身未随文提供）</summary>

**新工具新项目新模型**

- 「新工具、新项目、新模型」

**Kimi视觉思考版**

- Kimi（视觉思考版）的交互界面，左侧白色气泡中是Kimi的问候语，它表明可以仔细查看用户发送的图片并深入分析其中内容，右侧蓝色气泡是用户输入的指令，要求根据上传内容进行推理回答，在该用户指令旁还展示了一张待分析的黄色表格图片，对应了Kimi视觉分析的功能定位，符合文档中关于Kimi（视觉思考版）的相关介绍内容
- 一张关于视图内容形式的表格，列出了多种类型及其子分类、适用场景和参考示例。表格分为A.图文、B.不出镜、C.观点输出、D.问答互动、E.采访、F. vlog、G.直播、H. AI技术等类别，每个类别下又细分多个子类别，如A1笔记/思维导图/干货清单、B1展示生产过程、C1经管口播等，还附有简要介绍和适用场景，以及一些参考示例。该表格
- 一段关于选择合适视频形式的建议内容。内容提到选择视频形式需考虑目标受众、内容类型和传达信息，列举了6种形式：A1笔记/思维导图/干货清单，B1展示生产过程，C1经典口播或C2白板教学，D1线上直播连麦切片或D2读评论/读信，F1记录自己的生活或F2记录他人的生活，H1/AIGC高效生成内容。该图片

**OpenAI12天新品发布会**

- 「o1 & ChatGPT Pro」 「Watch the replay」
- 「OpenAI's Reinforcement Fine-Tuning Research Program」 「Watch the replay」 「非典型」
- 「Sora」 「Watch the replay」
- 「ChatGPT in Apple Intelligence」 「TREE REX」 「Watch the replay」
- 「Watch the replay」 「架个摄像头，几个人一坐」 「非典型」
- 「Advanced voice with video & Santa mode」 「Watch the replay」
- 「Day8」 「Search」 「Watch the replay」
- 「开发者节日礼物」 「Watch the replay」
- 「ChatGPT中的项目」 「Watch the replay」

**Gemini20Flash**

- 「System Instructions」 「Input」 「Output」 「Model」 「Gemini 2.0 Flash Experimental」 「PREVIEW」 「Code execution」 「Function calling」 「Grounding」 「Type something」

**GithubCopilot免费**

- GitHub官方发布的一条推文，宣布在VS Code中推出GitHub Copilot的新免费层级。推文显示每月可完成2000次代码补全，每月50条聊天消息，使用Claude 3.5 Sonnet或GPT - 4o等模型，提供更多乐趣。还提到GitHub已过1.5亿开发者，并配有GitHub Copilot的卡通形象。该图片

**您的程序员Devin已上线**

- 「Devin is a collaborative AI teammate」 「Built to help ambitious engineering teams achieve more」
- 「德文（Devin）」 「德文是一个协作的AI队友」 「您的程序员Devin已上线」
- 德文（Devin）的优势所在，涵盖代码迁移和现代化、大规模重构、卓越工程及客户工程支持四大方面。在代码迁移和现代化方面，能进行语言迁移、框架升级、云基础设施现代化及ETL代码迁移；在大规模重构方面，可进行Monorepo到子模块转换、代码结构重组等；在卓越工程方面，能提高测试覆盖率、解决静态分析错误等；在客户工程支持方面，能构建客户特定的集成、创建定制演示等。该图片
- 「什么样子好看」 「fix: only show repos in message when subset is selected」 「程序员Devin已上线」
- 「3600一个月，要雇一个Devin吗？」

**吴恩达人工智能Python初学者指南**

- 「AI Python for Beginners」 「Explore Courses」 「Enroll for Free」
- AI Python编程基础课程的大纲。课程目标是学习Python基础知识并应用到AI应用中，涵盖编程概念、Jupyter Notebook使用、Python代码编写与执行、与聊天机器人交互等。课程时长35h，包含25个代码示例，如变量、函数、列表等操作。还列出了课程介绍、运行第一个程序、如何功能化代码等10个视频标题，以及对应时长。该图片
- 「使用Python自动执行任务」
- 是名为《AI Python初学者指南》课程的第4课内容，课程主题为使用包和API扩展Python。图片详细列出了该课程的核心技能学习目标，包括使用Python内置模块、从外部及第三方库导入函数、与聊天机器人交互、使用应用程序编程接口API获取数据和使用Anaconda安装Python与Jupyter等。此外，图片还标注了课程的多个教学小节，各小节配有相应时长，涵盖使用本地文件、内置包、第三方包、A
- 「吴恩达：人工智能Python初学者指南」 「AI Python for Beginners: Basics of AI Python Coding」 「欢迎来到AI Python初学者教程」

**干翻Cursor的AI编程神器**

- 「干翻Cursor的AI编程神器？」
- 「Available wherever you want it」 「Download for macOS」 「Download for Linux」 「Download for Windows」
- Windsurf AI编程工具的付费计划对比。分为自由、专业版、专业终极版三个版本。自由版每月0美元，有5个基础用户提问积分、5个基础流程行动积分，可购买更多高级积分，但不适用保费积分成本。专业版每月15美元，有500个基础用户提问积分、1,500个基础流程行动积分，可购买更多高级积分，额外300个流程操作用户提示积分需支付10美元。专业终极版每月60美元，有3,000个基础流程行动积分，可购买更
- Windsurf AI工具的对比表格，展示了不同版本的Windsurf AI在功能、成本、特征等方面的对比。分为免费版、1200元/月版、2500元/月版三个版本。免费版仅提供基础功能；1200元/月版可自定义更多模型参数、提供3000个Flow Action和User Prompt积分；2500元/月版可提供5000个积分。表格还列出了各版本的特征，如无代码代码生成、编辑器AI聊天助手等，以及企
- 「Choose setup flow」 「Import from VS Code」 「Start fresh」 「Add windsurf to PATH」 「Back」
- 「Open with Cascade」 「Open Command Palette」 「Workspaces」 「Open Folder」 「Connect to」 「Write with Cascade」
- 「新晋AI编程神器干翻Cursor！首创实时感知无限用，估值12.5亿华人初创震惊AI界」
- 「还可以」

**分享两个我的实践**

- 「实践一：一个网页计算器」 「创业课」
- AI助手帮助生成的最基础计算器网页相关内容。上方说明将创建一个包含HTML、CSS和JavaScript的index.html文件，界面简洁。中间列出计算器功能，如基本算术运算、小数支持、括号等。下方列出布局元素，如显示屏幕、数字按钮、运算按钮等。底部提示在默认浏览器中打开index.html文件，可尝试使用计算器进行基本计算，并询问是否添加更多功能或调整设计
- 「259×1783」
- AI助手帮助创建计算器网页的步骤及成果。首先创建了CSS文件styles.css，接着创建JavaScript文件script.js，最后编辑index.html文件，将其分为三个部分：仅含HTML结构及外部CSS、JavaScript文件链接的index.html；含所有CSS规则的styles.css；含所有JavaScript功能及改进的script.js。AI还对计算器代码进行了优化，如添
- 「试了一个小爬虫」 「实践二：AI资讯爬虫」 「每天信息量太大，各类资讯过多难以处理」
- 「我想做一个抓取最新AI咨询的爬虫」
- 「我想做一个抓取最新AI资讯的爬虫」
- 「pip install -r requirements.txt」 「python crawler.py」
- 「Windsurf AI」 「OpenAI」 「date」 「source」 「link」 「excerpt」 「Windsurf」
- 使用Windsurf编程工具更新爬虫功能的操作过程及终端运行结果。首先是代码更新相关记录，包含对requirements.txt、scraper.py、README.md文件的修改内容，还标注了各文件的增改行数，同时提供了打开对应文件的选项。接下来是执行安装新依赖的终端命令，命令为pip install -r requirements.txt，下方显示了命令输出的详细内容，包含卸载旧版本库、发现并
- 「Canceled background terminal command」 「python crawler.py」 「运行爬虫」
- 在AI项目中将文章转换为语音的程序开发过程。首先，创建了text_to_speech.py程序，使用Microsoft Edge的TTS引擎生成高质量中文语音，包含文章标题、摘要、正文等。接着，安装了新添加的依赖，运行pip install -c requirements.txt命令，显示Requirement already satisfied等信息。该图片
- 「将文字转换成语音」
- 「写一个java库，读取硬盘指定目录下的文件，找出其中重复的文件，并且写一个测试用例」
- 「main.java.com.fileutil」 「DuplicateFinder.java」 「DuplicateFinderTest.java」 「pom.xml」 「写一个java库，读取硬盘指定目录下的文件，找出其中重复的文件，并且写一个测试用例」
- 「学习AI编程，首选的语言是什么」 「Accept all」 「Decline all」 「Chat」
- 「自动驾驶分级·对比理解版」
- 「chatGPT is becoming a real engineer」 「你给我写的代码用不了，请抓虫」 「在我机器上就能用啊」 「哪个最先进？哪个会形成主流？」
- 「不发牢骚的老码农」 「懂得复制，1K」 「粘贴完还能跑起来，20K」
- 「Chinese (Simplified) (简体中文) Language Pack」 「英文界面」
- 「ai_code_loader」 「Cancelled background terminal command」
- 「Accept All Changes」 「Open off」 「Open」 「Close」
- 「ai_news_crawler」 「data」 「src」 「main」 「test」 「DuplicateFinder.java」 「DuplicateFinderTest.java」 「crawler.py」 「index.html」 「pom.xml」

**视频号大航海xAI**

- 「视频号大航海xAI」

**AI春晚拆解**

- 是李奕辰在AI落地Live1中关于AIGC短视频和商业认知分享的PPT内容。PPT中呈现了李奕辰的个人简介，包括其连续创业者身份及字节跳工厂打工人的经历。还展示了他在阿里AI视频竞赛中获得二等奖的证书，奖金为15,000元。此外，PPT还列出了其在AIGC方面的相关工作，如AI视频生成、AI视频剪辑等。该图片
- 「我的人生红点：AI春晚」 「30天，从想法到实现」
- 「美丽中国」 「诚策AI的奇遇 bilibili」 「AI春晚拆解」 「创意为王」
- 「有很长一段时间」
- 「无敌老崔/北京话」 「通往AGI之路 bilibili」
- 「星推AI创作 - Bilibili」
- 「通往AGI之路」 「AI春晚」

**AI工具整理一**

- 「一堂视频号大航海·内容形式小抄」
- 「设计3D架构图更现代化」 「开始编辑」 「开始使用」 「AI工具整理（一）」 「设计工具」
- 「创作绘本」 「创作视频」 「热门新品发布」 「INAUCURAL Children's Book CREATIVE CONTEST」 「The Adventurous Little Kitten」

**听歌点赞**

- 「来听同学们的新作品呀（评论哦）」 「一空整垫」 「笔墨纸（摇滚版）」

**本次作业**

- 「本次作业」

**本期Candy**

- 「一定挑战！」
- 「作业和Candy」

</details>
