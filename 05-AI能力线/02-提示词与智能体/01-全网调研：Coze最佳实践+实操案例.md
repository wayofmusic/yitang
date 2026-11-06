---
title: 全网调研：Coze最佳实践+实操案例
node_token: F0CTwv2f1iC94ok5J0hcYzmPnr9
source: https://www.feishu.cn/wiki/F0CTwv2f1iC94ok5J0hcYzmPnr9
space: 一堂学习
obj_type: docx
synced: 2026-09-26 05:31
course_line: AI能力线
stage: 提示词与智能体
train: 提示词与智能体
form: 课程逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
> 版权归原作者所有，本文仅做汇总，侵删。

[全网调研：Coze最佳实践+实操案例](https://www.feishu.cn/wiki/IFb5wvra3iRfJQkSJy0cmLl3neg)</cite>

## 背景

搜集整理市面上Coze相关的信息：

1. 最佳实践：Coze能达到的上限，比如比赛结果，厉害的能做到什么水平
2. B站教程：工作流拆解，教程复刻

**说明**

1. Coze包含的东西涉及很多方面，包括场景、具体技术、实操、教程等等。
2. 没有找到更好的维度进行整理，暂时根据来源和主要内容类型进行整理。
3. 标❤的是相对比较重要的内容，质量在A以上

**主要信息**

1. **官方资料：**

   1. 扣子官方教程：暂时更新到工作流，本文档内教程和B站视频是一样的
   2. 扣子案例合集：①场景案例；②功能实操；③综合讨论

> 比较重要的是功能实操部分，有具体能力的展开和实操案例
>
> > 图片展示了扣子官方教程中功能实操部分的内容。以红色框突出显示，包含2.1应用、2.2 API、2.3知识库、2.4多维表格、2.5插件、2.6工作流、2.7图像流、2.8变量/数据库、2.9多Agent、2.10卡片等10个子项。该图片与文档中介绍扣子官方教程的内容相关，直观呈现了功能实操部分的分类，帮助读者快速了解官方教程中功能实操涵盖的领域。

>

1. **B站实操教程视频**

   1. WayToAGI的合集+大圣AI超级个体 两部分质量相对较高
   2. 其他内容同质化比较严重（B站还有更多类似的），可以**根据主题来看视频教程**

1. **文字版实操**

   1. WayToAGI有一个按内容整理好的案例集，在这里就直接保留了，可以根据场景来挑选
   2. 彭俊旗的AI工具箱，从Coze官网找了最多人使用的智能体，逆向出来一个类似的Agent

1. **比赛内容**：大部分都*没有找到对应的实操过程*，以建立审美为主

# ❤S- 官方资料：扣子官方教程

原文链接：[📣 扣子官方教程&amp;宣传片（对外版）](https://www.feishu.cn/docx/MU2gdBhluo1aCJx9g5Sc1vwWnte)</cite>

> 这部分资料和B站内容一致[扣子官方教程来啦！｜手把手带你搭建 AI Bot](https://space.bilibili.com/1444391473?spm_id_from=333.337.0.0)

### **扣子空间**

<figure view-type="Preview"><source name="飞书20250418-160742.mp4" mime="video/mp4" origin-height="1080.000000" origin-width="1920.000000" size="100343603" token="WeArbD66xoGZURx9ZKqcqJBEnuf"/></figure>

### 扣子 x 国科大他山社团：用 AI 探索日月星辰

<figure view-type="Preview"><source name="传播版 - 修改版.mp4" mime="video/mp4" origin-height="1080.000000" origin-width="1920.000000" size="326102144" token="VwVpbCaxhoppUgxk5OScBjjZn9e"/></figure>

### **第一节：AI Agent & 扣子介绍**

1. 大模型的痛点
2. 什么是Agent
3. 什么是扣子
4. 扣子的功能和优势
5. 扣子的主页、个人空间、Bot商店、插件商店、工作流商店、团队空间、模型广场
6. 优质 Bot 体验：《读书小助手》、《爸妈防骗助手》

<figure view-type="Card"><source name="第一期 Agent与扣子介绍 (2).mp4" mime="video/mp4" size="575440342" token="BbAdbgXoXoXLf2xMLWecoAWTndd"/></figure>

### **第二节：扣子助手、人设与对话体验 - 快速上手**

1. 提示词及作用
2. 提示词如何写
3. LUI与GUI的区别
4. 如何提升扣子的对话体验
5. 实操：通过扣子助手搭建一个《高情商老板回复话术Bot》

<figure view-type="Card"><source name="扣子官方教程-第二课.mp4" mime="video/mp4" size="358773292" token="PBO3bsj3GoMiT6xj4pAcXh9hnEe"/></figure>

### **第三节：技能：插件  - 快速上手**

1. Function call是什么
2. 扣子插件&插件的基本概念
3. 实操：插件的使用、自定义插件的使用&插件商店

<figure view-type="Card"><source name="官方教程第三节-上（插件入门）.mp4" mime="video/mp4" size="1033207907" token="Q2W2bNYFLo6yFfx0p6zc9n5Nnmh"/></figure>

<figure view-type="Card"><source name="官方教程-第三节下（插件进阶）.mp4" mime="video/mp4" size="860027506" token="IKCSb15OsoM9JGx19eZctuPxnxR"/></figure>

### **第四节：技能：工作流  - 快速上手**

1. 什么是工作流？有什么作用？ 扣子中的工作流
2. 节点介绍：输入输出/功能节点/参数/批处理/代码/选择器/意图识别/文本处理/消息节点/变量和数据库节点
3. 搭建工作流最佳实践演示：旅行计划工作流

<figure view-type="Card"><source name="官方教程-第四节上（工作流）.mp4" mime="video/mp4" size="1640381995" token="XaLHb1eDponF2Mx34BWc6XJwnhf"/></figure>

<figure view-type="Card"><source name="官方教程-第四节中（工作流）.mp4" mime="video/mp4" size="1532111556" token="MQg9b7sHRoaYkRxErIScMbMjnIb"/></figure>

<figure view-type="Card"><source name="官方教程-第四节下（工作流）.mp4" mime="video/mp4" size="1664129894" token="LcjKbp5HxoDdQpxoe7Lcdccbnec"/></figure>

### **扣子智能客服助手**

<figure view-type="Preview"><source name="扣子-智能客服.mp4" mime="video/mp4" origin-height="1080.000000" origin-width="1920.000000" size="96200693" token="K6m2b9JIZoBzrixe46OcH2nenPe"/></figure>

### 雅思口语专家

<figure view-type="Preview"><source name="扣子最佳实践-雅思视频.mp4" mime="video/mp4" origin-height="1080.000000" origin-width="1920.000000" size="76986183" token="OcxbbMXVDoTuX8xTSYOcogkUnZ4"/></figure>

# 官方资料：扣子案例合集-社区内容分享

<blockquote>原文链接：[扣子低代码案例合集-社区内容分享](https://www.feishu.cn/docx/YNj2dVYo7o4L1Uxilq2c6A3Qnuc)</cite>扣子使用手册：https://www.coze.cn/docs/guides/welcome</blockquote>

## B 场景案例（以场景为主，没有具体的实操过程）

### 扣子客户案例合集

> [抖音电商：通过扣子智能体重塑电商服务新体验](https://www.coze.cn/customers/douyindianshang)

> [头条电商借助扣子平台实现智能化内容推荐与商品分发，促进 GMV 增长](https://www.coze.cn/customers/toutiaodianshang)

> [识典古籍基于扣子智能助手高效开展古籍数字化](https://www.coze.cn/customers/shidianguji)

> [墨攻携手扣子平台：以智能之力破解广告创意生产困局](https://www.coze.cn/customers/mogong)

> [鱼泡直聘：通过扣子智能体重塑招聘生态，开启高效就业新时代](https://www.coze.cn/customers/yupaozhipin)

> [探域：携手扣子实现电商服务全流程智能化飞跃](https://www.coze.cn/customers/tanyu)

> [译百分借助扣子平台突破业务挑战实现多维度升级](https://www.coze.cn/customers/yibaifen)

> [和府捞面：AI “诊脉” 评论，口碑效益双赢](https://www.coze.cn/customers/hefulaomian)

> [豆包 MarsCode 携手扣子罗盘，打造智能高效的 AI 编程助手](https://www.coze.cn/customers/marscode)

> [孩子王：以智能培训提升亲子服务，开启业绩增长新引擎](https://www.coze.cn/customers/haiziwang)

> [顶端新闻：智能赋能，重塑新闻传播新生态](https://www.coze.cn/customers/dingduan)

> [扣子助力联康科技，打造高效智能数字化医疗生态](https://www.coze.cn/customers/shanxi_health)

> [猫王音响携手扣子打造全球首款 AI 大模型收音机](https://www.coze.cn/customers/maowang_audio)

> [中国柒牌：基于扣子实现传统时尚产业的智能化转型](https://www.coze.cn/customers/qipai)

> [扣子助力增长营销云：打破技术瓶颈，革新广告投放智能化体验](https://www.coze.cn/customers/zengzhangyingxiaoyun)

### 模板

> [官方模板介绍-智能客服模板](https://www.coze.cn/open/docs/guides/template_customer_service)

> [官方模板介绍-客服陪练模板](https://www.coze.cn/open/docs/guides/template_customer_service_training)

> [官方模板介绍-自媒体创作助手模板](https://www.coze.cn/open/docs/guides/template_visual_content_creation)

> [官方模板介绍-卖点提炼模板](https://www.coze.cn/open/docs/guides/template_sellingpoint)

> [官方模板介绍-情感陪聊模板](https://www.coze.cn/open/docs/guides/template_ai_companion)

> [官方模板介绍-数据质检助手模板](https://www.coze.cn/open/docs/guides/template_dqc)

> [官方模板介绍-智能助教模板](https://www.coze.cn/open/docs/guides/template_study_buddy)

> [扣子上新！文生播客、客服、陪伴、教育…官方带你抄作业！](https://mp.weixin.qq.com/s/UaSdYDdeYoY6LNmYPyjdFA)

> [AI一分钟辅助播客创作！即刻开通自己的小宇宙](https://mp.weixin.qq.com/s/JNTXU5tE_RFHjkkPMOlSBQ)

### 硬件

> [猫王音响携手扣子打造全球首款 AI 大模型收音机](https://www.coze.cn/customers/maowang_audio)

> [中国柒牌：基于扣子实现传统时尚产业的智能化转型](https://www.coze.cn/customers/qipai)

> [译百分借助扣子平台突破业务挑战实现多维度升级](https://www.coze.cn/customers/yibaifen)

> [扣子 X 硬件 Onepager](https://www.feishu.cn/docx/AQsPdlIpJojjuzxjNVpcLQTvnDe)</cite>

> [扣子硬件 Showcase](https://www.feishu.cn/docx/FZ0SdK7EIokxhNxdNIcc6z1RnMe)</cite>

> [扣子+硬件：探索更多 AI 硬件的可能性](https://bytedance.larkoffice.com/docx/OxZ1duLAho8hWZxC4TEc1hw5nze#share-TakqdMHNUoSScXxhMy1cMJvRnvc)

> [扣子智能硬件方案一指禅（可对外）](https://www.feishu.cn/docx/ABEAdSJ8GoDDs8xMJnlcr5sAn7f)</cite>

### Deepseek

> [让Deepseek给你打工， Coze 函数调用解锁AI超能力](https://www.bilibili.com/video/BV19W9uYdEcB/)

> [独家接入Deepseek工具调用的 Coze ，这次真的被我榨干了](https://www.bilibili.com/video/BV1nNoxYREYT/)

> [ Coze +Deepseek实现小红书爆款笔记 ，打造专属Agent智能体](https://www.bilibili.com/video/BV1MHPYekEGd/)

> [ Coze +Deepseek个人记账管家、网文小说写手、批量生成艺术漫画 打造专属Agent智能体](https://www.bilibili.com/video/BV1RyXfYaEhE/)

> [结合Deepseek手搓一个 Coze 工作流](https://www.bilibili.com/video/BV1qT92YAEEv)

> [实战应用工作流：Deepseek+ Coze  一键制作爆款短视频 北大哲学篇](https://mp.weixin.qq.com/s/hD7XNM8NOgsU0OCrgnyWsw)

> [实战生成视频工作流：教育+Deepseek 动画视频轻松学英语 小红书/视频号/快手抖音 全平台](https://mp.weixin.qq.com/s/GdhqD3xYWpRfIcqxFS7D4g)

> [Deepseek结合扣子 一键生成爆款视频的全工作流](https://mp.weixin.qq.com/s/sBwH8zariD9jJjtiokPjjg)

> [Deepseek × 图像生成，用扣子应用打造超萌表情包生成器](https://mp.weixin.qq.com/s/cobmweM7G-nOmfISipfHwQ)

### 客服

> [抖音电商如何用扣子 Coze 打造 AI 客服？](https://mp.weixin.qq.com/s/j4I2pDJPsssVq09xnD2MjA)

> [抖音电商：通过扣子智能体重塑电商服务新体验](https://www.coze.cn/customers/douyindianshang)

> [孩子王：以智能培训提升亲子服务，开启业绩增长新引擎](https://www.coze.cn/customers/haiziwang)

> [探域：携手扣子实现电商服务全流程智能化飞跃](https://www.coze.cn/customers/tanyu)

> [官方模板介绍-智能客服模板](https://www.coze.cn/open/docs/guides/template_customer_service)

> [官方模板介绍-客服陪练模板](https://www.coze.cn/open/docs/guides/template_customer_service_training)

> [如何基于coze清洗文档获取真正QA知识库（电商客服，企业知识库场景必看）](https://www.feishu.cn/wiki/GFWPw2u3mitpFak34RjcLxobnMh)</cite>

> [如何快速搭建AI智能客服？](https://mp.weixin.qq.com/s/C2OiOEOKhAyFX72QtAInmQ)

> [电商老板必备！ Coze 电商客服机器人，24小时在线，帮你轻松砍掉高额人工成本](https://mp.weixin.qq.com/s/Jfld_frPh4jvuosKULbqWQ)

> [抖音商家接入扣子 AI ，打造一位24小时服务的智能客服， 小白保姆级教程](https://mp.weixin.qq.com/s/k2crtGqGEBJs0-OqoOeUjQ)

> [扣子实战案例：如何才能用知识库搭建出完美的智能客服](https://mp.weixin.qq.com/s/YP2_-jnXNjNDOZwgmUZ3HQ)

> [教你如何用扣子免费搭建“赛事活动AI客服”机器人](https://mp.weixin.qq.com/s/y-IAu2npkJsEdKjvHiIzaw)

> [智能客服(知识库+对话流)｜扣子教程](https://www.bilibili.com/video/BV1MJwTewE5s)

> [智能体 Coze 教程第四课，企业智能客服](https://www.bilibili.com/video/BV1FPmaY7E3b/)

> [10分钟用 Coze 打造专属AI客服，接入各大平台！](https://www.bilibili.com/video/BV1cjiiYvEnN/)

> [使用 Coze 搭建Ai客服-第一弹，使用知识库，RAG，超详细教程](https://www.bilibili.com/video/BV1a8A2eSERQ/)

> [使用 Coze 创建AI智能客服-第二弹，接入飞书多维表格，超详细教程](https://www.bilibili.com/video/BV1Wo9fY7ECj)

> [ Coze ：中小企业均可0门槛创建业务agent，支持接入微信公众号、微信客服、discord、tele等各种终端，实现公司AI客服、销售机器人等触达客户](https://www.bilibili.com/video/BV1DA4m1w72p/)

> [使用 Coze 搭建Ai客服-第一弹，使用知识库，RAG，超详细教程](https://www.bilibili.com/video/BV1a8A2eSERQ/)

> [使用 Coze 创建AI智能客服-第二弹，接入飞书多维表格，超详细教程](https://www.bilibili.com/video/BV1Wo9fY7ECj/)

### 营销

> [官方模板介绍-客服陪练模板](https://www.coze.cn/open/docs/guides/template_customer_service_training)

> [墨攻携手扣子平台：以智能之力破解广告创意生产困局](https://www.coze.cn/customers/mogong)

> [扣子助力增长营销云：打破技术瓶颈，革新广告投放智能化体验](https://www.coze.cn/customers/zengzhangyingxiaoyun)

> [用 Coze 搭建智能机器人并挖掘销售线索](https://wap.peopleapp.com/video/rmh41227880/rmh41227880)

> [ Coze +Deepseek实现数码3C销售顾问（基础与进阶）](https://www.bilibili.com/video/BV1tj9gYnEs9/)

> [ Coze  商业实战案例 -- 销售话术脚本](https://www.bilibili.com/video/BV1aiimYnEzK)

> [可复刻的扣子"客户回访"场景工作流，并实现提醒任务执行](https://mp.weixin.qq.com/s/YNT9Itb4VFG3chwAqe0V1A)

### 媒体写作

> [官方模板介绍-自媒体创作助手模板](https://www.coze.cn/open/docs/guides/template_customer_servicehttps://www.coze.cn/open/docs/guides/template_visual_content_creation)

> [短视频文案提取+分析+仿写AI工具，Coze 工作流批量提取二创，自媒体必备！](https://mp.weixin.qq.com/s/rsGV9pNE_xVYoEAo99iErA)

> [ Coze 工作流+飞书多维表格：自动抓取+分析100条笔记详细数据，小红书博主必备！](https://mp.weixin.qq.com/s/SPZWs-QLNYyTG6i-o0YVCQ)

> [全自动Deepseek 写影评+批量生成 + 发布飞书，提效10 倍！](https://mp.weixin.qq.com/s/H_HMfQt3TPAJohnkA2yh1w)

> [使用Deepseek大模型，3分钟生成100篇小红书心理学知识图文！](https://mp.weixin.qq.com/s/zKzq8MbBWdwVba1HlEqa7w)

> [【Agent+RAG】如何用智能体Agent打造自媒体工作素材库？](https://www.bilibili.com/video/BV1iRBkYSEaW/)

> [提取小红书笔记+OCR识别+自动写入飞书](https://www.bilibili.com/video/BV1cqDZYaEwD/)

> [小红书全自动仿写工作流实战，全自动采集爆款小红书笔记+图片识别内容！](https://www.bilibili.com/video/BV1PQQHYuEmA/)

> [小红书全自动仿写工作流实战，全自动仿写爆款小红书笔记+图片自动生成！](https://www.bilibili.com/video/BV16kQpYPEn1/)

> [1分钟100条爆款文案： Coze +飞书多维表格+Deepseek最强工作流](https://www.bilibili.com/video/BV1rqQpYqEGC/)

> [ Coze +Deepseek实现小红书爆款笔记 ，打造专属Agent智能体](https://www.bilibili.com/video/BV1MHPYekEGd/)

> [微信小程序搭建：爆款小红书之"好好说话"图文生成](https://mp.weixin.qq.com/s/ahbUcJZSJl-nhderbm0sVg)

> [自媒体人必备：通过行业热词批量抓取百条小红书涨粉吸睛数据全自动导入飞书在线文档存储分析](https://mp.weixin.qq.com/s/vmzqSDmyigmZKTeWJxImCA)

> [爆款小红书账号定位+数据拆解，扣子工作流详细拆解](https://mp.weixin.qq.com/s/eSnv-NunKFFk0Da2qXmAkg)

> [多平台视频文案获取工作流：完美平替官方下架的抖音视频插件](https://mp.weixin.qq.com/s/ctWXHOAG5lheOELBfpyEvQ)

### 生活助手

> [官方模板介绍-情感陪聊模板](https://www.coze.cn/open/docs/guides/template_ai_companion)

> [用 Coze 打造一个每日定时新闻助手，轻松了解行业资讯](https://www.bilibili.com/video/BV1QS9JYUE5C/)

> [ Coze 实战系列（一）| 天天小管家](https://www.bilibili.com/video/BV1BLuaekE1o/)

> [ Coze 做一个时间管理小助手](https://www.bilibili.com/video/BV1PZoiYFE1e/)

> [记账助手](https://www.bilibili.com/video/BV1AsRAYdEbU?vd_source=930b244a28ab90654de5bfb4e7179b6c&p=8&spm_id_from=333.788.videopod.episodes)

> [告别熬夜做PPT！关键词输入，智能生成，秒变PPT高手！](https://mp.weixin.qq.com/s/HJD6wiwNgl2L4A5rx_Tlhg)

### 教育

> [官方模板介绍-智能助教模板](https://www.coze.cn/open/docs/guides/template_study_buddy)

> [ Coze 上的文献解读类应用，免费一键生成推文和报告](https://www.bilibili.com/video/BV1sdkRYGEom/)

> [用 Coze 平台打造文献提炼智能体](https://www.bilibili.com/video/BV17N9ZYPEA9/)

> [上下班通勤路上也能读Paper，我闲暇之余花了1小时用扣子搭建论文阅读神器](https://mp.weixin.qq.com/s/NYe4t6VAQDL8R0LVuDYhPQ)

> [科研 Cozer：扣子助力科研数据收集](https://mp.weixin.qq.com/s/hldu25u8ovw_jWWgugdAtQ)

> [Deepseek进阶玩法： Coze +Deepseek打造一键论文阅读与分类整理工作流](https://mp.weixin.qq.com/s/d7ZSZYa_jZ9tYGWOuMdoMw)

> [教师必学AI智能体搭建教程：课题开题报告工作流](https://mp.weixin.qq.com/s/jJ_KuR0eSapFfZadFqcVrQ)

> [引爆全网的10秒记单词视频制作](https://mp.weixin.qq.com/s/9CYyJyT1qMWhpS0T_x1sbg)

> [少儿英语阅读学习视频， Coze 工作流一键批量创作，英语教育最新免费AI工具](https://mp.weixin.qq.com/s/m2abeBtCsClbtK2i5reY0w)

> [教育从业者必备！教你用 Coze 平台搭建「小学语文老师」应用！](https://mp.weixin.qq.com/s/xCgIEGMrMBu0DSZKCFpH_w)

> [期中期末不用愁：老师必备的8款 Coze 智能体，一键解决出题、写评语、批改作业等难题](https://mp.weixin.qq.com/s/GYx-dSASIyYwha66Pu38Jw)

> [Deepseek+ Coze ：一键精准生成个性化教学设计](https://mp.weixin.qq.com/s/PuwXwfXUhKdlFtcoZ_CK_w)

> [专为学龄前儿童搭建的智能体 ](https://mp.weixin.qq.com/s/BSHuo8xPJFXWu5epHJoQDw)

### 多维表格

> [Deepseek+ Coze +飞书多维表，5分钟自动化批量深度拆解爆款笔记](https://mp.weixin.qq.com/s/ky_bPUBK-isacSfiEC7UjA)

> [Deepseek+ Coze +飞书多维表，为你深度拆解爆款笔记，直接下载无水印视频](https://mp.weixin.qq.com/s/Dz5beOSLi9Q_7PLboCJnIw)

> [用 Coze +飞书多维表创建工作流，1分钟生成100条今日热点文案](https://mp.weixin.qq.com/s/A4Ynvo4OtQnMIhItFGxb2w)

> [飞书多维表格按条件筛选记录 + 读取分页 Coze 工作流，无限循环使用方法](https://mp.weixin.qq.com/s/0Q7c0dFXKIvZtrUxWpRmwQ)

> [实战应用工作流：1分钟生成100条爆款文案： 扣子 + 飞书多维表格 到底怎么玩转](https://mp.weixin.qq.com/s/F2yoH67r5r02xajrOpiCXw)

> [如何把 Coze 工作流+Deepseek生成的内容，批量插入飞书表格保存？](https://mp.weixin.qq.com/s/dy60q3msxmiN0BvUIpcjHw)

> [我用扣子+飞书手捏了一个私人知识库](https://mp.weixin.qq.com/s/cex1FobHF4t2FN3tPnN3TQ)

> [全自动小红书工作流，从爆款采集→Deepseek仿写→秒出图→飞书自动归档，10分钟搭建 Coze 工作流](https://mp.weixin.qq.com/s/3_RQSSsNfyatYcbcIPSBKg)

> [飞书多维表格秘技：一键批量提取、Deepseek R1分析和改写抖音爆款文案](https://mp.weixin.qq.com/s/PZ3z32oRjUW2N6fZNc5o_Q)

> [Deepseek+扣子实现xhs内容自动采集](https://mp.weixin.qq.com/s/tK53wh6XSb7ZhXizvS4saA)

> [Deepseek + Coze + 飞书，批量二创网络热搜口播文案](https://mp.weixin.qq.com/s/SgpGPAQ2Zo9GpS0y_V5QAQ)

> [提效神器，我用Agent搭建了一个高效办公表格](https://mp.weixin.qq.com/s/soPS3y369K-ta2kUsGaNTg)

> [ Coze +多维表格+Deepseek， 打造自动化内容创作系统 | 信息获取和创作效率翻倍](https://www.bilibili.com/video/BV11CQhYvEMh/)

### 数据分析

> [和府捞面：AI “诊脉” 评论，口碑效益双赢](https://www.coze.cn/customers/hefulaomian)

> [ Coze 搭建专业的数据分析工作流](https://www.bilibili.com/video/BV13zX8YVEZS/)

> [ Coze 搭建深度行业分析报告](https://www.bilibili.com/video/BV14p9yY5ER5/)

> [ Coze 工作流高效分析抖音热点关键词文案](https://www.bilibili.com/video/BV1UpQ3YEEw6/)

> [扣子工作流生成统计图表](https://mp.weixin.qq.com/s/ZSQrMSRa9MVwk_h8ayLFIw)

> [使用 Coze 做一个智能报表助手](https://mp.weixin.qq.com/s/BoGqqQxYS_0Sj80IvZ53gg)

> [Excel表格+AI智能体=效率翻倍！数据分析之 Coze 智能体保姆级搭建教程](https://mp.weixin.qq.com/s/IW95A5giSCpRyPN8_Qxdx)

> [ Coze 案例 | 饮食营养统计： Coze 的数据表SQL操作](https://mp.weixin.qq.com/s/HpibdH3HhhIe9JAqqwIGgA)

### 智能打标

> [头条电商借助扣子平台实现智能化内容推荐与商品分发，促进 GMV 增长](https://www.coze.cn/customers/toutiaodianshang)

> [鱼泡直聘：通过扣子智能体重塑招聘生态，开启高效就业新时代](https://www.coze.cn/customers/yupaozhipin)

> [顶端新闻：智能赋能，重塑新闻传播新生态](https://www.coze.cn/customers/dingduan)

## ❤S 功能实操（技术+实操）

> 这一部分可以当成一个教程来看，遇到卡点，容易找到对应的能力快速学习实践。

### 应用

> [我们用扣子搭建了个 AI 公益应用（详细技术拆解教程）](https://mp.weixin.qq.com/s/GQPwiLECbSQOSy2DJ_CCUQ)

> [1小时开发AI应用小程序](https://www.bilibili.com/video/BV1EtNgeAE3K/)

> [AI应用H5模式案例](https://www.bilibili.com/video/BV1hR6jYrEMe/?spm_id_from=333.337.search-card.all.click&vd_source=930b244a28ab90654de5bfb4e7179b6c)

> [AI应用-PC模式案例](https://www.bilibili.com/video/BV18o6jYgEp4?spm_id_from=333.788.videopod.sections&vd_source=930b244a28ab90654de5bfb4e7179b6c)

> [3分钟上手扣子应用：一键出图，装修效果竟如此惊艳！](https://www.bilibili.com/video/BV129N9ePEJD/)

> [小程序AI应用开发：Logo设计](https://www.bilibili.com/video/BV1UxRpYdERL/)

> [轻松用扣子开发自己的应用，小白也可以](https://mp.weixin.qq.com/s/2Q9UXxFMseVhwrftvFTubQ)

> [10分钟用 Coze 搭建萌宠秀AI应用！](https://mp.weixin.qq.com/s/ncds_g2Lqsl_RonQdZErfg)

> [应用开发实战，搭建生成室内装修图应用](https://mp.weixin.qq.com/s/poLyAtQkpqVyI6LST0luUg)

> [一文讲透扣子应用搭建](https://mp.weixin.qq.com/s/8dB-Lc0KvCbtFrPg9Y2Sjw)

> [无需一行代码就可以搭出用户前端界面，实现拖拉拽搭建AI应用](https://mp.weixin.qq.com/s/l3e0LEUDekPhp8kQXbXI4A)

> [用一个AI应用范例，帮你解决卡点](https://mp.weixin.qq.com/s/1fMX011t1Ii5VYugBVxyZg)

> [扣子AI应用卡点：容器布局](https://mp.weixin.qq.com/s/0aiL9qSFDDbwn3091ZyFCQ)

> [不写一行代码，30分钟手搓AI应用](https://www.bilibili.com/video/BV1aMkPYGEC9/)

> [育婴式 Coze 官方应用拆解教学](https://www.bilibili.com/video/BV1byzoYmERJ/)

> [ Coze 扣子应用开发入门指南：无代码搭建自己的数据库！](https://www.bilibili.com/video/BV1NCc3eTEvY/)

> [AI红包封面生成器，不会设计也能做精品](https://mp.weixin.qq.com/s/EPcWTjhLJFPu6DnBePUfWA)

> [实战开发 Coze 应用-姓氏头像生成器（上）](https://mp.weixin.qq.com/s/S49tXjBftKyEu1Nphlaikw)

> [实战开发 Coze 应用-姓氏头像生成器（下）](https://mp.weixin.qq.com/s/AdTsEAMsRCbAJlawwJiKMQ)

> [肝了2天，我终于产出了 Coze  AI应用详细教程](https://www.bilibili.com/video/BV139zHY9Esn)

> [扣子AI应用-入门使用](https://www.bilibili.com/video/BV1CezdYvEt5/)

> [扣子AI应用-翻译大师应用讲解以及实践](https://www.bilibili.com/video/BV1pezdYvEXx/)

> [扣子AI应用-面试小助手应用以及实践](https://www.bilibili.com/video/BV1pezdYvEoz/)

> [扣子AI应用-创意写真馆讲解以及实践](https://www.bilibili.com/video/BV1CezdYvExa/)

> [扣子最新更新-应用功能](https://www.bilibili.com/video/BV1wrzvYgEMh/)

> [基于 Coze 可一站式构建、托管、复制、发布具有UI界面的AI应用，首次开启的开发者范式转移](https://www.bilibili.com/video/BV17C6NYnEJY/)

> [字节发布扣子应用 IDE，轻松开发各种复杂 AI 应用](https://mp.weixin.qq.com/s/aqxu0fWxhBKOBeCuC-Apuw)

> [智能体驱动的 AI 应用时代已来](https://mp.weixin.qq.com/s/wbo0qhYkLgjU9z99mGnt0w)

### API

> <ul><li>4.16 [一些减少 output token 手段](https://www.feishu.cn/docx/GMHqdEmKOo3CEtx2kG7ctWyvnie)</cite></li></ul>

> <ul><li>4.10 [如何动态修改扣子智能体提示词](https://www.feishu.cn/docx/Yel3d5lqxokEJGxi9QXcG3wXnbe)</cite></li></ul>

> - 4.10 [扣子如何使用火山知识库插件](https://www.volcengine.com/docs/84313/1528465)

> <ul><li>4.3 [扣子 WebSocket 常见问题 FAQ](https://www.feishu.cn/docx/A7NKdi83bovKwMx5wX2cJ2o0nTx)</cite></li></ul>

> <ul><li>3.28 [设备用量管控及账单API使用说明【不再维护】](https://www.feishu.cn/docx/MZOWder6NoIX4HxJxEBclx6Onzh)</cite></li></ul>

> <ul><li>3.28 [硬件设备接入扣子 WebSocket 最佳实践](https://www.feishu.cn/docx/RMUydH1AkoSQTmxT1C9cyjaunNd)</cite></li></ul>

> <ul><li>3.27 [如何动态修改扣子智能体提示词](https://www.feishu.cn/docx/Yel3d5lqxokEJGxi9QXcG3wXnbe)</cite></li></ul>

> <ul><li>3.27 [扣子智能体对话支持自定义传参](https://www.feishu.cn/docx/LNQwdCLoYompk5x8QtEcmSkUnwf)</cite></li></ul>

> <ul><li>3.23 [从零开始，搭建 “长眼睛” 的智能体攻略](https://www.feishu.cn/docx/VybadVL8soZLovxDRsccBxFZnWd)</cite></li></ul>

> <ul><li>3.14 [扣子渠道入驻开发教程](https://www.feishu.cn/docx/PDnbdFbh7oieWKxq9KncqZlEnxc)</cite>（含代码）</li></ul>

> <ul><li>3.8 [语音对话场景下设备如何鉴权？](https://www.feishu.cn/docx/TGDfdGjBsoe3oGxCJbLcWtk8n0e)</cite></li></ul>

> <ul><li>3.6 [浏览器端插件 - 轻量 RPA](https://www.feishu.cn/wiki/AxttwO8HQiS8n5krEzkcY9PnnYe)</cite>（端插件）</li></ul>

> <ul><li>3.3 [如何使用语音和图片理解大模型对话](https://www.feishu.cn/docx/ImBYdsyukoqoRqxoCs7cB9Dcngz)</cite>（含代码）</li></ul>

> <ul><li>2.28 [扣子 OpenAPI 支持 DeepSeek 思维链](https://www.feishu.cn/docx/UpNHdNqz5oqiC2x574gcnpmrnKB)</cite></li></ul>

> <ul><li>2.27 [扣子中如何使用端插件，让智能体与本地设备交互?](https://www.feishu.cn/docx/AAAedsXYAolDEVx47yJcsth2nrd)</cite>（含代码+视频）</li></ul>

> <ul><li>2.25 [在扣子中如何使用 OpenAPI 获取和更新变量(workaround)？](https://www.feishu.cn/docx/IxoNd288kohJn9xRwXycDWsgnHb)</cite></li></ul>

> <ul><li>2.20 [使用扣子 API 如何选择合适的鉴权方式？](https://www.feishu.cn/docx/BcQ8d7CGPoinZJx2Ghsc4fmnn1g)</cite></li></ul>

> <ul><li>2.12 [[对外] 低时延复杂 agent 的搭建原理](https://www.feishu.cn/docx/OzcXd9B9fo5KPcxpZX4cL4Qonpd)</cite></li></ul>

> <ul><li>2.10 [[对外] Agent 联网搜索+设备控制+闲聊+长期记忆搭建](https://www.feishu.cn/docx/CEJedaaf8oxJMox7g6DcOBnAnbh)</cite></li></ul>

### 知识库

> [官方文档：创建并使用知识库](https://www.coze.cn/docs/guides/use_knowledge)

> [官方文档：知识库最佳实践-基于知识库快速搭建产品资料问答 Bot](https://www.coze.cn/docs/guides/product_knowledge_bot)

> - 4.10 [扣子如何使用火山知识库插件](https://www.volcengine.com/docs/84313/1528465)

> [饮食助手：如何在 Coze 进行知识库调优](https://mp.weixin.qq.com/s/502qmGX4pFP9Z2a8C1cF1A)

> [如何基于coze清洗文档获取真正QA知识库（电商客服，企业知识库场景必看）](https://www.feishu.cn/wiki/GFWPw2u3mitpFak34RjcLxobnMh)</cite>

> [0帧起手解决 RAG 分段难题！知识库还能这么玩？](https://mp.weixin.qq.com/s/FyZt3lLeaAmOpZId-0fKWw)

> [玩转扣子 | 5分钟包你搞懂什么是RAG并学会搭建属于自己的RAG智能体](https://www.bilibili.com/video/BV1TWwCePE9v)

> [玩转扣子 | 5分钟包你搞懂什么是RAG并学会搭建属于自己的RAG智能体](https://www.bilibili.com/video/BV1TWwCePE9v)

> [视频：扣子系列教程（五）：知识库的三种用法讲解](https://www.bilibili.com/video/BV13i421e7r1/)

> [趣味知识问答智能体搭建教程，使用工作流配合表格知识库搭建](https://mp.weixin.qq.com/s/S_j11x2ZiuofPOoAPbkyuQ)

> [胎教级教程：万字长文带你使用 Coze 打造企业级知识库](https://waytoagi.feishu.cn/wiki/CT3UwDM8OiVmOOkohPbcV3JCndb)

> [用 Coze 做一个基于知识库的QA bot，TA熟读了我所有的文章](https://zhuanlan.zhihu.com/p/699276883)

> [教你如何用扣子打造一个企业级的知识库机器人](https://zhuanlan.zhihu.com/p/695935995)

### 多维表格

> [Deepseek+飞书多维表，简易工作流搭建](https://www.bilibili.com/video/BV1KU9wY4EYr)

> [飞书多维表格工作流的搭建使用视频讲解](https://www.bilibili.com/video/BV1TXUzYDEGo/)

> [ Coze 工作流接入飞书多维表格实操第一期](https://www.bilibili.com/video/BV1EcXQYUEdG/)

> [ Coze 工作流操作飞书多维表格第二期-写入数据](https://www.bilibili.com/video/BV1AxXfY1E7g/)

> [ Coze 智能体/工作流保存数据到多维表格](https://www.bilibili.com/video/BV1mz9RYVEFU/)

> [ Coze 智能体 保存数据到 飞书多维表格](https://www.bilibili.com/video/BV1KvPxeSECL/)

> [ Coze 操作飞书表格-添加数据](https://www.bilibili.com/video/BV1aaZVYrEPM/)

> [ Coze 工作流操作多维表格第三期-查询工作表数据](https://www.bilibili.com/video/BV1FZ9eY6EWK/)

> [ Coze +飞书多维表探索AI记账](https://www.bilibili.com/video/BV1ujzJYGErB/)

> [ Coze +飞书多维表格，轻松构建项目管理工作流](https://www.bilibili.com/video/BV1NgDbY4EDJ/)

### 插件

> [扣子官方教程｜技能-插件（上）｜第三节](https://www.bilibili.com/video/BV1oH4y1w7yY/)

> [扣子官方教程｜技能-插件（下）｜第三节](https://www.bilibili.com/video/BV1DZ421K7vu/)

> [官方文档-插件开发最佳实践-查询股票价格](https://www.coze.cn/docs/guides/dbj0mdxb)

> [视频：扣子（ Coze )系列教程（三）：插件的创建](https://www.bilibili.com/video/BV1pBKke8EdL/)

> [使用扣子基于IDE创建自定义插件](https://mp.weixin.qq.com/s/ly528cG24hU5aDWG62PWwQ)

> [ Coze 大白话系列 | 创建插件全流程](https://www.bilibili.com/video/BV1uWepexEwv/)

> [ Coze +飞书多维表格，打造 AI 稍后读智能体，解锁 10 倍知识管理效率](https://mp.weixin.qq.com/s/2q9MpHak4SKFJjUQpnnHmA)

> [ Coze  X 通义强强联手，看看我是怎么去用的](https://mp.weixin.qq.com/s/fO0_E5TzEEKnQusc5X9Trw)

> [了解扣子：如何用  Coze IDE 制作一个插件](https://mp.weixin.qq.com/s/Woy-hBSEYh_wUobya_yPcg)

> [教你玩转 Coze 自定义插件](https://mp.weixin.qq.com/s/vTv0-sUs09d0keng1XmhVQ)

> [插件教程 |  Coze 自定义插件集成API](https://mp.weixin.qq.com/s/iAQEsbQ6W5qdzQrCWYVGxA)

> [视频：【共学快闪】AI Agent- Coze 搭建 5月10日罗文分享插件](https://www.bilibili.com/video/BV1HE42137n4)

> [扣子插件教程：如何使用 Coze  IDE创建插件](https://mp.weixin.qq.com/s/xQAyE3zVBYh2vmceV9Rdxg)

> [ Coze 国内版插件汇总](https://mp.weixin.qq.com/s/r-bougqAVSETIROFiLLykA)

> [ Coze 官方插件不够用？教你自己造（白嫖）](https://mp.weixin.qq.com/s/UdW40YVTWukNYXEGujsPOw)

> [视频：扣子开发AI插件实战案例 上传图片识别名称和卡路里](https://www.bilibili.com/video/BV1HE42137tL/)

### 工作流

> [扣子官方教程｜技能-工作流（上）｜第四节](https://www.bilibili.com/video/BV1Y5eFeAE1S/)

> [扣子官方教程｜技能-工作流（中）｜第四节](https://www.bilibili.com/video/BV1E1eweSE26/)

> [扣子官方教程｜技能-工作流（下）｜第四节](https://www.bilibili.com/video/BV1gAeAeMEdq/)

> [扣子实战生成视频工作流：教育+Deepseek 动画视频轻松学英语](https://mp.weixin.qq.com/s/GdhqD3xYWpRfIcqxFS7D4g)

> [实战应用工作流：全自动生成>新闻资讯类<短视频](https://mp.weixin.qq.com/s/FUcJsIVOfXGaF7t6WYLdxg)

> [实战应用工作流： 爬取指定网页信息，整理成信息报表](https://mp.weixin.qq.com/s/QnYtUkZjWBHtbsYpabzpkQ)

> [实战工作流：这么神奇的数字人工作流原来是这样搭建的](https://mp.weixin.qq.com/s/pUp5wcikWPubr14R0FMILw)

> [实战应用工作流：爆款小红书的"个性签名图文"生成器](https://mp.weixin.qq.com/s/_lX_vAKkag-fA_eQfRCOvg)

> [实用工作流： 自动提炼产品卖点的语音式说明书， 让产品信息传递更能触达客户](https://mp.weixin.qq.com/s/1JOHjYiXrC7CioCTG2lyiQ)

> [学会使用批处理，让你的工作流运行时间提升90%](https://www.bilibili.com/video/BV1xLrTY3ENw)

> [解锁扣子循环节点，构建用大模型创作高质量长文本高效工作流](https://www.bilibili.com/video/BV1hvcVenEzi)

> [变量聚合节点太好用，用工作流搭建智能翻译演示案例](https://mp.weixin.qq.com/s/wv5tjxl21QWcjjj6FJQ9XA)

> [扣子实战案例：工作流之用问答节点做一个《黑神话：悟空》答题](https://mp.weixin.qq.com/s/81-lmsovGPtJykybl1acaQ)

> [扣子系列教程（四）：工作流中各节点常用使用方式](https://www.bilibili.com/video/BV1ux4y1J761/)

> [ Coze 工作流教程，让你的Bot高质量的处理复杂任务！](https://www.bilibili.com/video/BV1PZ421g7xT/)

> [【Agent共学第二期】艾木分享 | 这也许是你一生中第一个Bot](https://www.bilibili.com/video/BV1XT421i7jH/)

> [一步一步带你手搓一个 Coze  Bot——Dr. Know（极简版 Perplexity）](https://www.bilibili.com/video/av1005221752)

> [用 Coze 的工作流，攒一个爆款短视频文案工具](https://www.bilibili.com/video/BV1YdGneuEmf/)

> [万字实践教程，全面入门 Coze 工作流｜用 Coze 打造 AI 精读专家，复刻 10 万粉公众号的创作生产力](https://mp.weixin.qq.com/s/r40BDHKq8NC547cehAzOzw)

> [3分钟用字节“扣子”打造股票AI分析工作流](https://mp.weixin.qq.com/s/ptlj0WHnDWIX7VPv-miSCg)

> [扣子工作流实战案例教程，教你搭建一个图书管理工作流](https://mp.weixin.qq.com/s/Fh3Vm3EDSzoYVxf91GcMMA)

> [奶奶也学得会的AI工作流，省时省力下班早！](https://mp.weixin.qq.com/s/bXC8DHzs5_OgPh3FtKhJZA)

> [使用扣子创建AI绘画工作流](https://mp.weixin.qq.com/s/d_6yS-T8JXKf1Tr6JgBPFg)

> [中文GPTS使用秘籍，字节扣子工作流使用全教程](https://zhuanlan.zhihu.com/p/682108709)

> [Workflow实践 | 使用 Coze 复现一个AIGC信息检索Bot](https://mp.weixin.qq.com/s/PFgjR-q7XcTcqog1gLyFqA)

> [AI自动获取B站视频摘要信息](https://mp.weixin.qq.com/s/x8lwvlomhFNLZl__qYuDww)

> [如何用 Coze 制作一个信息检索Bot（含Workflow的基础用法）](https://mp.weixin.qq.com/s/Ory8iVXXjjN3zSTcupPm6Q)

> [视频： Coze  绘制workflows by Coze 2024.01](https://www.bilibili.com/video/BV1PJ4m1v7rc)

> [视频：【共学快闪】AI Agent- Coze 搭建 5月9日艾木分享Agent系统核心Workflow](https://www.bilibili.com/video/BV1is421N72j)

> [一周新手分享 Coze 工作流的学习技巧](https://zhuanlan.zhihu.com/p/687826306)

> [ Coze 工作流的深度体验：打造家庭会议助手并浅谈插件生态](https://mp.weixin.qq.com/s/uxo9jdhNc1SVx62P5t7uNQ)

> [官方文档-工作流最佳实践-搜索新闻](https://www.coze.cn/docs/guides/workflow_search_news)

> [官方文档-工作流最佳实践-使用 LLM 处理问题](https://www.coze.cn/docs/guides/workflow_use_llm)

> [官方文档-工作流最佳实践-生成随机数](https://www.coze.cn/docs/guides/workflow_use_code)

> [官方文档-工作流最佳实践-搜索并获取第一个链接内容](https://www.coze.cn/docs/guides/workflow_get_content)

> [官方文档-工作流最佳实践-识别用户意图](https://www.coze.cn/docs/guides/workflow_user_intent)

### 图像流

图像流功能已融合进工作流功能，具体可参考[官网文档](https://www.coze.cn/open/docs/guides/release_note#2b61dfb6)

> [扣子案例有奖征集活动](https://bytedance.larkoffice.com/docx/RgMWdpVLXoF8Ebxwq7GcOmC6njf)-领航实践奖

> [海报创意工坊](https://www.coze.cn/docs/guides/woz01au0)

> [今日心情海报](https://www.coze.cn/docs/guides/eyu225pk)

> [小红书制图工厂 ](https://www.coze.cn/docs/guides/blox2pt5)

> [人生四宫格](https://www.coze.cn/docs/guides/qqv9weu1)

> [生成营销Banner](https://www.coze.cn/docs/guides/ciy0besc)

> [生成卡通版运营海报](https://www.coze.cn/docs/guides/5fha2cn8)

> [扣子案例有奖征集活动](https://bytedance.larkoffice.com/docx/RgMWdpVLXoF8Ebxwq7GcOmC6njf)-优秀实践奖

> [AI 图像流画板-电影海报](https://www.feishu.cn/docx/YobSdc4IOo848CxH6Gwcq3pinod)</cite>

> [素描双生画卷-图像流](https://www.feishu.cn/docx/O8lhdlcyQoyou5xbqOUcSeZ4nFf)</cite>

> [使用coze图像流实现创意姓氏头像](https://www.feishu.cn/docx/CUO4dzbCgonJUKx21VzcahAinVd)</cite>

> [用画板功能实现每日一问卡片](https://www.feishu.cn/docx/ZvdsdphCIodDbpxna2JcXq55nec)</cite>

> [Coze画板：高效打造儿童识字卡片的利器（附视频教程）](https://www.feishu.cn/docx/PJ8idIONooM41mxPoyzcTufUnbh)</cite>

> [手把手带你玩转 Coze 画板节点- 日签卡片生成器](https://www.feishu.cn/docx/KB0ndv9WRoBdqhxCN3ccia9ZnVI)</cite>

> [用扣子搭了个文章转小红书图片的智能体](https://www.feishu.cn/docx/UwG3dT7O2oCJ9PxMKo8caGw7n0f)</cite>

> [Coze画板功能，让你免费批量生产漫画！](https://www.feishu.cn/docx/VfWpdf9wNoMReVxQSQqckljTnve)</cite>

> [Coze|用AI实现小朋友们的职业理想](https://www.feishu.cn/docx/JBkmdjZ8zoVlGJxaeMXce1henpd)</cite>

> [应该早点发布这个功能的：Coze图像流利器—画板](https://www.feishu.cn/docx/CGcqdWiJPon1hjxcu3gcc8UJnVh)</cite>

> [【首席中秋祝福官】Bot介绍](https://www.feishu.cn/docx/QtcLdzRB2og6M9xRDGecgrItn2f)</cite>

> [Coze搭建山海经卡牌游戏](https://www.feishu.cn/docx/GJ45dqu8iogi3Ox7JXbcueQmntc)</cite>

> [炉石传说抽卡机bot大揭密](https://mp.weixin.qq.com/s/aOIIGams_amMWFciKHO7NQ)

> [最新扣子实战案例：图像流工具节点示例详解](https://mp.weixin.qq.com/s/v399Cz4PWWwfBk0tvEIUQg)

> [一句话生成高质量图文笔记，教你手搓自动化AI图文助手](https://www.bilibili.com/video/BV1qKsMeMEhB)

> [我用AI做了个00后疯感工牌生成器，领导看到后私聊找我要链接](https://mp.weixin.qq.com/s/qlhEVs14NV-cBG7jgHuMHQ)

> [ Coze  保姆级教程：用图像流，给老板来一套表情包](https://mp.weixin.qq.com/s/AyaF3oIO98pzNzZjYiIBgw)

> [视频：【Agent共学第二期】来来 & Stuart分享｜图像流重塑设计](https://www.bilibili.com/video/BV1bJ4m137iR/)

> [基础教程： Coze “图像流” 抢先体验](https://waytoagi.feishu.cn/wiki/AHs2whOS2izNJakGA1NcD5BEnuf)

> [两分钟教你开发一个自己的AI应用](https://www.xiaohongshu.com/explore/667d6565000000001c02691b)

> [猫猫守护神，写真教程，这一波 Coze 上了大分](https://mp.weixin.qq.com/s/xN06sQMATAtj-TP47BE2xQ)

> [【探索AI】使用 Coze 搭建一个正装形象生成器](https://mp.weixin.qq.com/s/4_tRXKVkKlVRbzjKCIrUWA)

> [ Coze /扣子新出的图像流功能，有点惊艳到了！](https://mp.weixin.qq.com/s/si92251Bxm5p8PV14lUqVA)

> [王炸!  Coze 图像流发布，我用它实现了海马体影楼级形象照（内附喂饭级教程)](https://mp.weixin.qq.com/s/JgLuqJUDs5VkEQHkFOpAZQ)

> [AI智能体｜教你使用扣子图像流的文生图功能](https://mp.weixin.qq.com/s/qWKUza0AlgCQ6Z9NvpGg2w)

### 变量/数据库

> [官方文档：数据库](https://www.coze.cn/docs/guides/database)

> [扣子系列教程（七）：数据库的的单/多用户模式用法讲解](https://www.bilibili.com/video/BV11ohDeREiM/)

> [ Coze 工作流【数据库】节点教程](https://www.bilibili.com/read/cv35570626/)

> [扣子系列教程（六）：变量的用法讲解](https://www.bilibili.com/video/BV134421Q7DH/)

> [ Coze 实操14个技巧：数据库、知识库、工作流](https://onml84xn1m.feishu.cn/docx/PZKYdBhFHo991yxy0NCc3SZqnGe)

> [看 Coze 搭建的"访客管理系统"，让数字化管理不再复杂](https://mp.weixin.qq.com/s/YYrfuqfVu_bbT6wCz1goDg)

> [工作流之“数据库增删改查”详解](https://www.bilibili.com/video/BV1kuYee6Ej2)

> [ Coze 数据库-初始化数据](https://www.bilibili.com/video/BV1mWsMedEZD/)

> [ Coze 数据库速成教程-2](https://www.bilibili.com/video/BV1zWeGeyEE5/)

### 多 Agent

> [官方文档：多 Agent 模式](https://www.coze.cn/docs/guides/multiagent)

> [使用 Coze 的muilt-agent驯服GPT-4](https://mp.weixin.qq.com/s/sjRFE44cjBfn4p3_3vv4vg)

> [Multi-agent mode实践 | 用 Coze 手捏一个bot](https://mp.weixin.qq.com/s/YV7M7othSzMjKpm8xNHU-w)

> [视频：分享一个在 Coze 上做提示词工程以及设计多智能体应用的最佳实践案例](https://www.bilibili.com/video/BV1MC411h7ok/)

> [视频：【Agent共学第二期】Kai分享 | 一百个字搭谁是卧底-多Agent](https://www.bilibili.com/video/BV1Ew4m1S7eq)

> [ Coze 版儿童陪伴机器人+实物玩具=AI玩具，体验感还不错](https://mp.weixin.qq.com/s/t20eF7s9On6TPtA9mNQhZA)

### 卡片

> [官方教程-卡片](https://www.coze.cn/docs/guides/message_card)

> [最新扣子实战案例：扣子卡片的制作及使用](https://mp.weixin.qq.com/s/qtgBHPOggldgWs_mZQoQVw)

> [使用扣子——扣子的卡片如何使用](https://mp.weixin.qq.com/s/kRq_I61d7M3hJJIqboyuog)

## A 综合讨论（偏认知+一些实操）

### 活动

> [我在字节 Coze 平台做的智能体上了热榜！](https://mp.weixin.qq.com/s/JDKsikwmDduwDHhfRzboGQ)

> [扣子在上海｜一些捏 Bot 的 “旁门左道” 和赛前赛后](https://mp.weixin.qq.com/s/DqYS06rONeW9tK3-e8UnYQ)

> [跟上海的朋友一起捏 bot](https://mp.weixin.qq.com/s/_t7YIFO2eIIbQAraFm_odw)

> [我们的 Bot 获得了「掘金 x 扣子 Hackathon 活动 - 深圳站」的总冠军](https://mp.weixin.qq.com/s/_BAkMD_EQf8_R9rKKarfCw)

> [深圳线下活动最佳解决方案奖-WeCapture](https://m.okjike.com/originalPosts/660bf25a3624666324495ec1)

> [字节的扣子炸裂更新，模型支持月之暗面，插件 IDE 已经上线](https://mp.weixin.qq.com/s/rwFFZdbxiGGVSTE80HpLMQ)

> [视频：【共学快闪】AI Agent篇  Coze 搭建- Itao+陈慧凌 分享｜主题：和 AI 成为搭子](https://www.bilibili.com/video/BV1Gb421B7AQ/)

### 探讨

> [ 扣子迎来重大升级更新，这篇文章让你明明白白！](https://mp.weixin.qq.com/s/w7gBtN-jYqhWskaLCNWWVQ)

> [想变现? Coze Agent商业化路径分析](https://mp.weixin.qq.com/s/vDvYT-Ulns1UfYSjUMEJZw)

> [扣子系列教程（一）：什么是扣子智能体](https://www.bilibili.com/video/BV1rRE7eTEtH/)

> [小微智能体v1.2：支持多会员套餐、快速发布、名片分享（ Coze 扣子AI智能体发布到小程序方案，个人可用，无限制）](https://mp.weixin.qq.com/s/8BqQ1RkmBD7miuMj6n7v2w)

> [扣子教程集锦[AI agent教程]](https://mp.weixin.qq.com/s/BLtrm-kEqD4-nN9l7Oi9ZQ)

> [这可能是全网目前最全的 Coze 入门教程了！](https://www.bilibili.com/video/BV1YM4m167zP/)

> [扣子实战教程，全网最细节讲解](https://www.bzfree.com/doc/coze#%E5%BC%95%E8%A8%80)

> [Bot创作者如何在 Coze 上赚钱？](https://mp.weixin.qq.com/s/WO-ZPuVgNHF129b4qsSjlQ)

> [如何用扣子给企业搭建一个超级数字员工](https://mp.weixin.qq.com/s/xXDKXRl-KhfYK9p4pHJ3MQ)

> [新手总结 Coze  bot创建步骤：先锁定“最简”任务，提前准备测试问题](https://zhuanlan.zhihu.com/p/687931917)

> [视频：【共学快闪】AI Agent- Coze 搭建 5月8日大圣分享 Coze 全流程搭建](https://www.bilibili.com/video/BV1bs421N7tR)

> [视频：【共学快闪】AI Agent- Coze 搭建 5月7日赛博禅心大聪明分享](https://www.bilibili.com/video/BV1V1421z7At/)

> [面向业务开发的 Coze 使用指南](https://mp.weixin.qq.com/s/ZY8zwaGdR6dq1OL_XQ2iTQ)

> [扣子初体验 | 拥有一个属于自己的聊天机器人](https://mp.weixin.qq.com/s/glT5Qc4a3vpRLxVAPdDDbA)

> [用 Coze 扣子轻松搭个Bot，从此告别"标题党"](https://mp.weixin.qq.com/s/Fm_tPWAcZsysRz6Wsq5HBA)

> [扣子官方：用扣子/ Coze  揭秘吴恩达的4种 AI Agent 设计模式](https://mp.weixin.qq.com/s/OtdncYNt9KDE6YzDJeexFg)

> [扣子官方：这届00后已经学会用扣子/ Coze “偷懒”了](https://mp.weixin.qq.com/s/uZMSrXp2MLrmcFAfV8N8ow)

> [【2万字长文】如何用Kimi全自动创建扣子智能体？这喂饭级教程将揭晓一切！](https://mp.weixin.qq.com/s/sGgUJgte4taivEJCZKRRXQ)

> [保姆级教程： Coze  打工你躺平](https://mp.weixin.qq.com/s/QNg2-hRjSxBc_4MKtJh7Jw)

> [扣子智能体开发实战教程 | 智能体开发](https://mp.weixin.qq.com/s/blmMHAV1IBDMyqwYpwqbSA)

### Bot 分享

> [ Coze  + 高德 ：智能导游](https://juejin.cn/post/7413317657938821139)

> [万字实践教程，全面入门 Coze 工作流｜用 Coze 打造 AI 精读专家，复刻 10 万粉公众号的创作生产力](https://mp.weixin.qq.com/s/r40BDHKq8NC547cehAzOzw)

> [[ Coze 教程] “菜品秀秀”bot制作流程大揭密](https://mp.weixin.qq.com/s/iYgsr8uh34ihZW24qyWrVg)

> [动了谁的奶酪？——用字节扣子打造一个每篇都10万+阅读的知音人](https://mp.weixin.qq.com/s/yeRTwo_Xt1LzdLCXHwzI_A)

> [闭关10天，捣鼓出一个自媒体写作神器，一分钟一篇文章，写作嘎嘎猛！](https://mp.weixin.qq.com/s/8QdY4c_pRViUbTS96QkZRg)

> [扫码枪+AI：一扫生成药品信息卡片，说明书可以扔了！｜AI 教程](https://mp.weixin.qq.com/s/GB33M8KrCDdPQ_DvciPysg)

> [视频：【Agent共学第二期】制作一个新闻鉴别相关的bot](https://www.bilibili.com/video/BV1QJ4m1M7ti/)

> [视频： Coze 实战系列（一）| 天天小管家](https://www.bilibili.com/video/BV1nRMQexER7/)

> [视频：毕业加速器：如何用AI爆肝论文？](https://www.bilibili.com/video/BV12z421m7YV)

> [视频：不写代码，如何用 Coze 做专属的对话机器人](https://www.bilibili.com/video/av1603694358)

> [视频：用 Coze 一键生成朋友圈文案](https://www.xiaohongshu.com/explore/65c1d0ae000000001100d442)

> [视频：【Agent共学第二期】许键分享｜拆解“离谱村捏剧本” Coze  bot思路](https://www.bilibili.com/video/BV1Cx4y1n7yU/)

> [视频：【Agent共学第二期】银海分享 | 用AI重塑我的工作流](https://www.bilibili.com/video/BV1sr421L7Hj/)

> [视频：【Agent共学第二期】大家一起捏 Bot， Coze  作品分享会](https://www.bilibili.com/video/BV1hT421v7YD/)

> [视频：【Agent共学第二期】Bot冠军大揭秘：李小白](https://www.bilibili.com/video/BV1L1421y7zx/)

> [视频：【Agent共学第二期】两位个人Bot创作者的分享：《你出生的那一天》和《热点文章生成器》](https://www.bilibili.com/video/BV1DD421u7m7/)

> [视频：【Agent共学第二期】一点都不简单的共创之路](https://www.bilibili.com/video/BV1ei421v7hA/)

> [61儿童节，我给儿子做了两款 Coze 小应用，让他见识一下程序员爸爸的厉害。](https://mp.weixin.qq.com/s/YxPxpds9OJl0CWXTCYfxWg)

> [视频：使用「扣子/ Coze 」搭建文本纠错助手](https://www.bilibili.com/video/BV1q7421o7xx/)

> [六一【黑科技】礼物，AI“复活”玩具！细节剖析\~](https://mp.weixin.qq.com/s/-sK0Nb8xNZN8XQ0SixHKaw)

> [这是 Coze 平台上最完善、最强大的Notion连接器](https://mp.weixin.qq.com/s/3gzSEjWxnxB0dRKFZvOx4g)

> [最贴心的 Coze  bot：从零开始的bot搭建实战](https://juejin.cn/post/7362743871979831311)

> [数据何规接入AI客服（kimi版）啦！](https://mp.weixin.qq.com/s/zibF1XMFPBBMLnbNKn2alw)

> [人民日报健康客户端：智能对话 科学防癌 AI赋能肿瘤防治行动](https://ar.peopledailyhealth.com/ai/index.html)

> [使用 Coze 打造私人播客助手 - 根据个人喜好自动化生成播客](https://mp.weixin.qq.com/s/BmhwFJBf7_t88zI15at8jA)

> [字节 Coze 应用创作平台，开发 AI chatbot（短视频爆款案例）初探](https://mp.weixin.qq.com/s/5R21o5BCNXZQd6ZgkTx8bg)

> [使用 Coze 制作MidJourney提示词专家](https://mp.weixin.qq.com/s/BTzdCzIkrh2Nq11Eh5adOA)

> [使用扣子创建AI绘画助手](https://mp.weixin.qq.com/s/9Me7PiCpykquPSATqI0cRw)

> [我用 Coze 搓了一个乞丐版的秘塔搜索](https://waytoagi.feishu.cn/wiki/IM2TwbChWixcR9kEt87cmKsHnAc)

> [用 Coze 搞一个简单的安全AI助手](https://mp.weixin.qq.com/s/QE6V_UZs7WsOHMuQOTZ5DA)

> [英语怎么快速提高？我用 Coze AI 免费手搓了一个 24 小时陪练教师](https://zhuanlan.zhihu.com/p/691177635)

> [玩转  Coze ，我帮开源 AI 社区搞了一个社群运营机器人](https://juejin.cn/post/7365704703362269184)

> [保姆级教程！教你如何用扣子搭建一个免费好用的“图片转表格”AI客服（附实操过程+效果）](https://mp.weixin.qq.com/s/FOcAaARTnTp50D49ZKPZow)

> [前端智能化，扣子能做什么？](https://mp.weixin.qq.com/s/tiolzTwPKPZF4b8zZbvYpA)

> [【AI学习】如何用扣子搭建“赛事活动AI客服”机器人？亲测效果好](https://www.toutiao.com/article/7367384038752977417)

> [字节最新发布的 Coze 太好用了，我也不想取代合规老师的工作啊！](https://mp.weixin.qq.com/s/dgr9GhWatREfOR61s0iucg)

> [从0到1 | 使用 Coze 国内版部署飞书bot机器人、豆包智能体](https://mp.weixin.qq.com/s/suaawdGz453LaRX6kAcAcA)

> [ Coze  + 爬虫 = 周末去哪不用愁！！](https://mp.weixin.qq.com/s/OfN3ndVfye9p_0wIeuQWng)

> [今天拿到心动offer，这个AI有点东西…](https://mp.weixin.qq.com/s/QNgY1EC6nvPu1vRJOaLcPA)

> [从0到1无代码使用 Coze 搭建一对一作画工具](https://mp.weixin.qq.com/s/KZ6VjwbxQ9_emrAhSYUyrA)

> [应对裁员潮，突发奇想，打造“收割offer”智能体.......](https://mp.weixin.qq.com/s/JZpKf_mSEJCXfZklKBCpKA)

# B站：视频实操教程

## ❤S- WayToAGI AI Agent 合集

https://space.bilibili.com/259768893/lists/3313478

## ❤S- 大圣AI超级个体 Coze保姆级教程

https://space.bilibili.com/674669330/lists/3246709

## A+ Coze智能体搭建：从入门到精通！全网最细致的DeepSeek+Coze智能体工作流教程！

> 大咖教运营 粉丝3.9万 https://www.bilibili.com/video/BV1F8oLYZEiR

**课程列表**

1、Coze Ai智能体第一课 认识智能体的强大

2、Coze 初步入门-搭建自己的第一个Bot

3、搭建自己的第一个 Coze智能体

4、Coze 小红书爆款笔记大师-升级优化版

5、Coze智能体：古诗绘画工作流-古诗拆解（数组）

6、Coze智能体：古诗绘画工作流-图片生成（批处理）

7、Coze智能体：古诗绘画-图文升级（简单版）

11、Coze智能体：儿童故事绘本生成

12、Coze智能体：一键生成装修效果图

13、Coze智能体：字符串分隔及拼接

14、Coze智能体：花草知识百科（Coze多知识节点）

15、Coze智能体：抖音视频爆改小红书

16、Coze智能体：抖音转小红书至飞书多维表格

17、Coze智能体：本地知识库搭建-在线客服

18、Coze智能体：本地知识库-在线采集网页

19、Coze智能体：知识库-Excel表格及图片知识库

## A+ Coze（扣子）从入门到精通-基础/应用/搭建智能体讲明白的教程

> 12点就睡的林同学 粉丝2.8万 https://www.bilibili.com/video/BV1YooHYYEKr

**课程列表**

1、Coze智能体快速入门

2、Coze插件使用

3、Coze工作流与触发器实战

4、Coze知识库和记忆

5、Coze优化智能体交互体验

6、Coze搭建企业客服智能体

7、Coze搭建爆款文案智能体

8、Coze搭建产品卖点提炼智能体

9、Coze搭建情感陪聊智能体

10、Coze搭建数据质检智能体

11、Coze搭建智能助教智能体

12、Coze搭建客服陪练智能体

13、Coze搭建搜索新闻工作流

1、从爆火的Manus聊下AI Agent基本原理

2、从零开始开发一款自己的AI Agent智能体

3、从零开始手搓一个播放百万的养生爆款短视频

4、利用AI Agent批量抓取抖音爆款养生短视频文案

5、微调Deepseek自动化批量生成爆款养生短视频文案

6、日产上万条短视频的自动化混剪Agent实现原理拆解

7、AI大模型企业落地核心：业务知识库+AI自动化工作流

8、价值百万的企业增长获客直播间到底是怎么做的

## A+ 从零搭建Coze工作流coze智能体

> 赛博李沐瑶 粉丝2.2万 https://www.bilibili.com/video/BV1yeLbz2ECR

【第1集】coze实战教学-第一集： Coze是个啥？

【第2集】coze实战教学第二集：创建第一个智能体-游戏NPC原始人

【第3集】coze实战教学第三集：基于国内大模型搭建个人全能小助手

【第4集】coze实战教学第四节：全自动短视频生成机器人

【第5集】coze实战教学第五集：基于知识库的AI人才库实现

【第6集】coze实战教学第六集：基于数据库生成个人财务管理工具

【第7集】coze实战教学第七集：基于文件系统的智能相册应用

【第8集】coze实战教学第八集：基于计划任务的每日信息总结小助手

【第9集】coze实战教学第九集：将bot部署第三方平台

【第10集】coze实战教学第十集：短视频自动洗稿工作流演示

【第11集】coze实战教学第十一集：从最近火爆的Manus看工作流的发展方向

【第12集】coze实战教学第十二集：热门的工作流解决方案Dify和Coze怎么抉择

【第13集】coze实战教学第十三集：Dify快速部署

【第14集】coze实战教学第十四集：Ollama实现DeepSeek的本地部署

【第15集】coze实战教学第十五集：通过Dify来实现的各种解决方案

【第16集】coze实战教学第十六集：RAG工作原理和技术架构拆解

【第17集】coze实战教学第十七集：程序员拥抱AI大模型最佳学习路线

【第18集】Coze案例之行业调研报告的工作流和界面展示

【第19集】Coze案例之一键生成行业深度调研报告的工作流2

【第20集】Coze案例之一键生成行业深度调研报告的用户界面绘制和发布

【第21集】Coze案例之官方海报应用的演示

【第22集】Coze案例之官方海报应用工作流的剖析与界面交互

【第23集】Coze案例之爆款视频的实现流程

【第24集】Coze案例之复刻爆款视频工作流1

【第25集】Coze案例之复刻爆款视频工作流2及后续

# ❤S WayToAGI 扣子案例合集

<blockquote>原始链接：[扣子案例合集-社区内容分享](https://www.feishu.cn/wiki/N0Iew9G4ailq2hk7rakcJkn0nPe)</cite>更多内容：[教程：Coze / 扣子](https://www.feishu.cn/wiki/FjBYwQHVdicl26kXh7Ccdj6xngU)</cite></blockquote>

> 大部分文档都包含完整的构建过程，建议根据主题查找再深入。

### 应用IDE

> [健健: Coze应用实战指南 -- 吐槽心灵鸡汤](https://www.feishu.cn/wiki/QNytw8RZ5iLHzFkhne0c5wd1nxd)</cite>

> [Stuart: 0基础教学系列之Coze“用户界面”创建初体验](https://www.feishu.cn/wiki/FKM6wwhLsiJZkPkFr8dcrONunJb)</cite>

### 图像流

> [五津: DeepSeek+扣子：1分钟生成小红书爆款单词视频](https://www.feishu.cn/wiki/DPw2wG9KxiDDCrkVlAlcgmlFnvg)</cite>

> [Stuart: 炉石抽卡机coze bot大揭秘](https://www.feishu.cn/wiki/J4tVwxdd0iOEDDkZeU3cZHF2nMc)</cite>

> [Stuart: &lt;找三思做二十四节气海报&gt; coze bot大揭秘](https://www.feishu.cn/wiki/FMZBwCMBNismuhkjCfRcfck5n5f)</cite>

> [老田: AI时代的美女写真日记，女生勿进](https://www.feishu.cn/wiki/HNmXwy3Yei8Uy4kE4t6cQRmCnLh)</cite>

> [清: coze比赛作品[菜品秀秀]大揭密](https://www.feishu.cn/wiki/DTO8wynvDiolrlkYdWycIwlBnVg)</cite>

> [7颗扣子coze的搭建视频](https://www.feishu.cn/wiki/UkfswXrZqiuAzbkOmcNcNl8unQf)</cite>

> [Wojak meme-coze复刻版本](https://www.feishu.cn/wiki/LBXpwsfsFinB6wkX0jdcXBiGn7c)</cite>

> [《万物皆可meme》-扣子复刻wojak](https://www.feishu.cn/wiki/X0xcwVhOwis1F4kgN6fcUIIlnPb)</cite>

> [Coze 保姆级教程：用图像流，给老板来一套表情包](https://mp.weixin.qq.com/s/AyaF3oIO98pzNzZjYiIBgw)

> [视频：【Agent共学第二期】来来 & Stuart分享｜图像流重塑设计](https://www.bilibili.com/video/BV1bJ4m137iR/)

> [Coze/扣子新出的图像流功能，有点惊艳到了！](https://mp.weixin.qq.com/s/si92251Bxm5p8PV14lUqVA)

> [王炸! Coze图像流发布，我用它实现了海马体影楼级形象照（内附喂饭级教程)](https://mp.weixin.qq.com/s/JgLuqJUDs5VkEQHkFOpAZQ)

> [AI智能体｜手把手教你使用扣子Coze图像流的文生图功能](https://mp.weixin.qq.com/s/qWKUza0AlgCQ6Z9NvpGg2w)

> [coze卡牌生成器搭建思路（内含精华）](https://www.feishu.cn/wiki/TQ0VwnP11iVcpkkKZzhcvlZXnxG)</cite>

### 知识库

> [官方文档：创建并使用知识库](https://www.coze.cn/docs/guides/use_knowledge)

> [官方文档：知识库最佳实践](https://www.coze.cn/docs/guides/product_knowledge_bot)

> [胎教级教程:万字长文带你使用Coze打造企业级知识库](https://waytoagi.feishu.cn/wiki/CT3UwDM8OiVmOOkohPbcV3JCndb)

> [用Coze做一个基于知识库的QA bot，TA熟读了我所有的文章](https://zhuanlan.zhihu.com/p/699276883)

> [手把手教你如何用扣子（COZE）打造一个企业级的知识库机器人](https://zhuanlan.zhihu.com/p/695935995)

> [Coze汽车售后服务知识库Bot拆解](https://www.feishu.cn/wiki/N4wBwPY1oifcNJkZsyHc6McdnYg)</cite>

### 工作流

> [Stuart: 教你用coze写起点爆款小说《夜无疆》, 做到高中生文笔水平](https://www.feishu.cn/wiki/LRskwrJkli3CgkkY06xcC3HanBh)</cite>

> [Stuart: [教学向] 我把Coze比赛第一的bot拆了教大家](https://www.feishu.cn/wiki/Qt8Bwgl3PihQNukO7PjcmeuJnJg)</cite>

> [画小二：用Coze工作流制作行业简报：实战案例画小二日报](https://www.feishu.cn/wiki/HmIhwt1IkiIAzok73rDcgG7fnQg)</cite>

> [画小二：Coze工作流之抖音热门视频转小红书图文详细配置](https://www.feishu.cn/wiki/MV7gw298TiBajFkSrFeceYRMnXc)</cite>

> [扣子版虚拟女友李思思的思路](https://www.feishu.cn/wiki/O9M4w66fxiElylkBkCRcP6jLnsg)</cite>

> [视频：扣子（coze）系列教程（四）：工作流中各节点常用使用方式](https://www.bilibili.com/video/BV1ux4y1J761/)

> [视频：Coze工作流的手把手教程，让你的Bot高质量的处理复杂任务！](https://www.bilibili.com/video/BV1PZ421g7xT/)

> [视频：【Agent共学第二期】艾木分享 | 这也许是你一生中第一个Bot](https://www.bilibili.com/video/BV1XT421i7jH/)

> [视频：一步一步带你手搓一个Coze Bot——Dr. Know（极简版 Perplexity）](https://www.bilibili.com/video/av1005221752)

> [扣子工作流实战案例教程，手把手教你搭建一个图书管理工作流](https://mp.weixin.qq.com/s/Fh3Vm3EDSzoYVxf91GcMMA)

> [使用扣子Coze创建AI绘画工作流](https://mp.weixin.qq.com/s/d_6yS-T8JXKf1Tr6JgBPFg)

> [奶奶也学得会的AI工作流，省时省力下班早！](https://mp.weixin.qq.com/s/bXC8DHzs5_OgPh3FtKhJZA)

> [中文GPTS使用秘籍，字节扣子Coze工作流使用全教程](https://zhuanlan.zhihu.com/p/682108709)

> [Workflow实践 | 使用coze复现一个AIGC信息检索Bot](https://mp.weixin.qq.com/s/PFgjR-q7XcTcqog1gLyFqA)

> [AI自动获取B站视频摘要信息](https://mp.weixin.qq.com/s/x8lwvlomhFNLZl__qYuDww)

> [如何用Coze制作一个信息检索Bot（含Workflow的基础用法）](https://mp.weixin.qq.com/s/Ory8iVXXjjN3zSTcupPm6Q)

> [视频：Coze 绘制workflows by coze 2024.01](https://www.bilibili.com/video/BV1PJ4m1v7rc)

> [视频：【共学快闪】AI Agent-Coze搭建 5月9日艾木分享Agent系统核心Workflow](https://www.bilibili.com/video/BV1is421N72j)

> [一周新手分享COZE工作流的学习技巧](https://zhuanlan.zhihu.com/p/687826306)

> [Coze工作流的深度体验：打造家庭会议助手并浅谈插件生态](https://mp.weixin.qq.com/s/uxo9jdhNc1SVx62P5t7uNQ)

> [官方文档-工作流最佳实践-搜索新闻](https://www.coze.cn/docs/guides/workflow_search_news)

> [官方文档-工作流最佳实践-使用 LLM 处理问题](https://www.coze.cn/docs/guides/workflow_use_llm)

> [官方文档-工作流最佳实践-生成随机数](https://www.coze.cn/docs/guides/workflow_use_code)

> [官方文档-工作流最佳实践-搜索并获取第一个链接内容](https://www.coze.cn/docs/guides/workflow_get_content)

> [官方文档-工作流最佳实践-识别用户意图](https://www.coze.cn/docs/guides/workflow_user_intent)

### 数据库

> [Coze记账管家——数据库使用教程](https://www.feishu.cn/wiki/SGJnwlUwMi5Rh9kPhjFcQaI1nnf)</cite>

> [COZE工作流【数据库】节点教程](https://www.bilibili.com/read/cv35570626/)

> [官方文档：数据库](https://www.coze.cn/docs/guides/database)

### 多Agent

> [使用coze的muilt-agent驯服GPT-4](https://mp.weixin.qq.com/s/sjRFE44cjBfn4p3_3vv4vg)

> [Multi-agent mode实践 | 用coze手捏一个bot](https://mp.weixin.qq.com/s/YV7M7othSzMjKpm8xNHU-w)

> [视频：免费视频教程｜分享一个在Coze上做提示词工程以及设计多智能体应用的最佳实践案例](https://www.bilibili.com/video/BV1MC411h7ok/)

> [视频：【Agent共学第二期】Kai分享 | 一百个字搭谁是卧底-多Agent](https://www.bilibili.com/video/BV1Ew4m1S7eq)

> [官方文档：多 Agent 模式](https://www.coze.cn/docs/guides/multiagent)

> [一文读懂扣子上的多 Agent 模式](https://www.feishu.cn/wiki/PZjLwnKjviW9XpkK391cbGeNnHd)</cite>

### 插件

> [画小二：通过Coze定制开发插件案例：根据食物识别营养热量](https://www.feishu.cn/wiki/CTQWwpbDwikoaekFOKpcpY2qn3b)</cite>

> [官方文档-插件开发最佳实践-查询股票价格](https://www.coze.cn/docs/guides/dbj0mdxb)

> [视频：扣子（coze)系列教程（三）：插件的创建](https://www.bilibili.com/video/BV1pBKke8EdL/)

> [使用扣子Coze基于IDE创建自定义插件](https://mp.weixin.qq.com/s/ly528cG24hU5aDWG62PWwQ)

> [coze X 通义强强联手，看看我是怎么去用的](https://mp.weixin.qq.com/s/fO0_E5TzEEKnQusc5X9Trw)

> [了解扣子：如何用 CozeIDE 制作一个插件](https://mp.weixin.qq.com/s/Woy-hBSEYh_wUobya_yPcg)

> [手把手教你玩转Coze自定义插件](https://mp.weixin.qq.com/s/vTv0-sUs09d0keng1XmhVQ)

> [插件教程 | coze自定义插件集成API](https://mp.weixin.qq.com/s/iAQEsbQ6W5qdzQrCWYVGxA)

> [视频：【共学快闪】AI Agent-Coze搭建 5月10日罗文分享插件](https://www.bilibili.com/video/BV1HE42137n4)

> [扣子Coze插件教程：如何使用Coze IDE创建插件](https://mp.weixin.qq.com/s/xQAyE3zVBYh2vmceV9Rdxg)

> [Coze国内版插件汇总](https://mp.weixin.qq.com/s/r-bougqAVSETIROFiLLykA)

> [Coze官方插件不够用？手把手教你自己造（白嫖）](https://mp.weixin.qq.com/s/UdW40YVTWukNYXEGujsPOw)

> [视频：扣子Coze开发AI插件实战案例 上传图片识别名称和卡路里](https://www.bilibili.com/video/BV1HE42137tL/)

### 活动

> [我在字节Coze平台做的智能体上了热榜！](https://mp.weixin.qq.com/s/JDKsikwmDduwDHhfRzboGQ)

> [扣子在上海｜一些捏 Bot 的 “旁门左道” 和赛前赛后](https://mp.weixin.qq.com/s/DqYS06rONeW9tK3-e8UnYQ)

> [跟上海的朋友一起捏 bot](https://mp.weixin.qq.com/s/_t7YIFO2eIIbQAraFm_odw)

> [我们的 Bot 获得了「掘金 x 扣子 Hackathon 活动 - 深圳站」的总冠军](https://mp.weixin.qq.com/s/_BAkMD_EQf8_R9rKKarfCw)

> [深圳线下活动最佳解决方案奖-WeCapture](https://m.okjike.com/originalPosts/660bf25a3624666324495ec1)

> [字节的扣子炸裂更新，模型支持月之暗面，插件 IDE 已经上线](https://mp.weixin.qq.com/s/rwFFZdbxiGGVSTE80HpLMQ)

> [猎豹移动集团 coze 版 Al Hackathon](https://bytedance.larkoffice.com/docx/VUOMdmaUOor5t7x9zfzc0H3rnvb)

> [视频：【共学快闪】AI Agent篇 Coze搭建- Itao+陈慧凌 分享｜主题：和 AI 成为搭子](https://www.bilibili.com/video/BV1Gb421B7AQ/)

### 扣子X火山引擎开发者社区夏季 Bot Hackathon 线上赛道获奖作品

> 原文链接：https://developer.volcengine.com/articles/7391744119359406143

> 一等奖: [我用扣子做一个简单的智能体——竖起耳朵听](https://www.feishu.cn/wiki/T5Elwj2yjim0ROkYgmRc4OB0nbd)</cite>

> 二等奖: [超级飞机百科Bot](https://www.feishu.cn/wiki/JmDpwyP38ih1ABkm5rlcorWtndf)</cite>

> 二等奖: [扣子初体验——菠萝作词家](https://www.feishu.cn/wiki/PNJzwDZvairmZ8kVOdWctuvUnIp)</cite>

> 二等奖: [使用coze做一个智能报表助手](https://www.feishu.cn/wiki/PpnPwVN9Ninu47kfUzrc3hRwnJg)</cite>

> 二等奖: [我们居然开发出了图灵测试游戏！](https://www.feishu.cn/wiki/TUdnwayw9iW0iMkBC17cdIUXn5g)</cite>

> 二等奖: [军师联盟BOT｜同时询问多个大模型并返回汇总梳理后的结果](https://www.feishu.cn/wiki/FfADwlQT4iiZcLkqCAbcOlj8nGb)</cite>

> 三等奖:[创新守护者：专利小助手，您的智能知识产权管家](https://www.feishu.cn/wiki/Acc1wJMRPiDLLvkjOhMc7co6nza)</cite>

> 三等奖:[救！！暧昧对象这样说我咋回啊？？](https://www.feishu.cn/wiki/RTLZw0WpcizQ9TkqQJ4cBxARnce)</cite>

> 三等奖: [搭建了两个AI助手，故事图文生成助手和汽车管家](https://www.feishu.cn/wiki/OMTuw5Sb6i1VV8kBDmActyFEncf)</cite>

> 三等奖:[生物医药小助手的诞生之旅～如果你有公众号，你也应该做一个扣子智能体](https://www.feishu.cn/wiki/LZrfwQ0EIiB8mtkh5LGcKtG4nNg)</cite>

> 三等奖:[生成有趣的《图文短句》【扣子】来帮你实现，零代码也OK](https://www.feishu.cn/wiki/ZDlXwxZ2LiUR5fkoSP1cLaIqn4e)</cite>

> 三等奖: [Bot智能体 | 用Coze实现【多模态资讯的跨平台推送】](https://www.feishu.cn/wiki/M5qZwnhOgiyHQFkColtcQIDsnRg)</cite>

> 三等奖:[沉浸式单机剧本杀Bot](https://www.feishu.cn/wiki/QT1MweHlZi81p7kpnr5ccmHOnud)</cite>

> 三等奖:[用扣子搭建一个儿童故事书，我把它取名为「漫画小书虫📚🐛」](https://www.feishu.cn/wiki/FQ2zwexD2iqFtTk6zUvcXOsSn9c)</cite>

> 三等奖:[《执笔者》：基于多Agent模式的全能写手](https://www.feishu.cn/wiki/EE5Qw4bgtis02tkSX69cvmi6n9d)</cite>

> 三等奖:[【我的会议我做主】一款全能会议助手](https://www.feishu.cn/wiki/SEZtwGlVYi3XBjkodlDcpIlYnSh)</cite>

> 创新奖:[实战Coze发布SysOps个人系统运维助手](https://www.feishu.cn/wiki/FRG3wLRmiiEKlhkQFXAc547nnvW)</cite>

> 创新奖:[Bot智能体 | 如何高情商回复，快来体验《高情商小师傅》给你解答](https://www.feishu.cn/wiki/ZbGBwFN3giymnmkVSMWcWmBun8g)</cite>

> 创新奖:[我读书少，所以做了读书神器](https://www.feishu.cn/wiki/WrkqwtViqiHCSKkVr2EcGz1anSd)</cite>

> 创新奖:[Coze直聘，职业助手Bot助力拿好Offer](https://www.feishu.cn/wiki/D5IMwkyF7it9g5k8oDHcJcCIn5e)</cite>

> 创新奖:[增强版 Bot：基于 AI 驱动的智能创作平台，实现一站式内容生成（图片、PPT、PDF）](https://www.feishu.cn/wiki/RcmMwJWKgiPJiGkQtVYcqySHnrd)</cite>

> 创新奖:[扣子AI应用 - 故事与绘本](https://www.feishu.cn/wiki/UyF6wYMxxiPGTSk77kVcR4hrnFf)</cite>

> 创新奖: [如何学习AI绘画，快来体验《AI绘画助手》](https://www.feishu.cn/wiki/I3khwaJ9sizsM4kvGZ6czbVAnNg)</cite>

> 创新奖: [🌟 一站式职业规划服务，为您量身定制求职路径， 从性格测试到理想工作匹配，助您实现职业目标](https://www.feishu.cn/wiki/Pv94wRIl2ish9Gk4zeAcm11qnld)</cite>

> 创新奖: [我看你骨骼惊奇,必是练武奇才,来测测你家宝宝将来干啥吧](https://www.feishu.cn/wiki/KYF7wnjunicWukkR3fUcGlAqnqc)</cite>

> 创新奖:[&#34;剧本影子&#34;创作剧本的新体验](https://www.feishu.cn/wiki/IyC1wuk1fi2quuklTJ6caVVtnDd)</cite>

> 创新奖:[汽车贴纸，为你的爱车换上新的外衣](https://www.feishu.cn/wiki/NZWlwai45irrP8ky7Toc2lgInXd)</cite>

> 创新奖:[如何规划好自己的旅游路线](https://www.feishu.cn/wiki/ZSPJw5uHXiI1v7kMOFectdHAn0c)</cite>

> 创新奖:[智能客服助手|基于扣子应用开发平台的解决方案](https://www.feishu.cn/wiki/AhbHwHxFuiJSGkkeWYEcucWsnAe)</cite>

> 创新奖:[睡前故事小助手，随时随地编故事](https://www.feishu.cn/wiki/Q6yewfSBMifzdZkgPBUcGkernvc)</cite>

> 创新奖:[[COZE零代码实现商业工具开发]销售总监助理（算力产业商机挖掘机）](https://www.feishu.cn/wiki/I9lSwbUrPix681k2T3ych2RInub)</cite>

### 综合探讨

> [这可能是全网目前最全的Coze入门教程了！](https://www.bilibili.com/video/BV1YM4m167zP/)

> [扣子实战教程，全网最细节讲解](https://www.bzfree.com/doc/coze#%E5%BC%95%E8%A8%80)

> [Bot创作者如何在Coze上赚钱？](https://mp.weixin.qq.com/s/WO-ZPuVgNHF129b4qsSjlQ)

> [新手总结Coze bot创建步骤：先锁定“最简”任务，提前准备测试问题](https://zhuanlan.zhihu.com/p/687931917)

> [视频：【共学快闪】AI Agent-Coze搭建 5月8日大圣分享Coze全流程搭建](https://www.bilibili.com/video/BV1bs421N7tR)

> [视频：【共学快闪】AI Agent-Coze搭建 5月7日赛博禅心大聪明分享](https://www.bilibili.com/video/BV1V1421z7At/)

> [面向业务开发的 Coze 使用指南](https://mp.weixin.qq.com/s/ZY8zwaGdR6dq1OL_XQ2iTQ)

> [扣子（](https://mp.weixin.qq.com/s/glT5Qc4a3vpRLxVAPdDDbA)[coze.cn](https://mp.weixin.qq.com/s/glT5Qc4a3vpRLxVAPdDDbA)[）初体验 | 拥有一个属于自己的聊天机器人](https://mp.weixin.qq.com/s/glT5Qc4a3vpRLxVAPdDDbA)

> [用Coze扣子轻松搭个Bot，从此告别"标题党"](https://mp.weixin.qq.com/s/Fm_tPWAcZsysRz6Wsq5HBA)

> [扣子官方：用扣子/Coze 揭秘吴恩达的4种 AI Agent 设计模式](https://mp.weixin.qq.com/s/OtdncYNt9KDE6YzDJeexFg)

> [扣子官方：这届00后已经学会用扣子/ Coze “偷懒”了](https://mp.weixin.qq.com/s/uZMSrXp2MLrmcFAfV8N8ow)

> [【2万字长文】如何用Kimi全自动创建扣子智能体？这喂饭级教程将揭晓一切！](https://mp.weixin.qq.com/s/sGgUJgte4taivEJCZKRRXQ)

> [保姆级教程：Coze 打工你躺平](https://mp.weixin.qq.com/s/QNg2-hRjSxBc_4MKtJh7Jw)

> [扣子Coze智能体开发实战教程 | 智能体开发](https://mp.weixin.qq.com/s/blmMHAV1IBDMyqwYpwqbSA)

### Bot 分享

> [视频：【Agent共学第二期】制作一个新闻鉴别相关的bot](https://www.bilibili.com/video/BV1QJ4m1M7ti/)

> [视频：用Coze搭建智能机器人并挖掘销售线索](https://wap.peopleapp.com/video/rmh41227880/rmh41227880)

> [视频：coze实战系列（一）| 天天小管家](https://www.bilibili.com/video/BV1nRMQexER7/)

> [视频：毕业加速器：如何用AI爆肝论文？](https://www.bilibili.com/video/BV12z421m7YV)

> [视频：不写代码，如何用 Coze 做专属的对话机器人](https://www.bilibili.com/video/av1603694358)

> [视频：用coze一键生成朋友圈文案](https://www.xiaohongshu.com/explore/65c1d0ae000000001100d442)

> [视频：COZE：中小企业均可0门槛创建业务agent，支持接入微信公众号、微信客服、discord、tele等各种终端，实现公司AI客服、销售机器人等触达客户](https://www.bilibili.com/video/BV1DA4m1w72p/)

> [视频：【Agent共学第二期】许键分享｜拆解“离谱村捏剧本”coze bot思路](https://www.bilibili.com/video/BV1Cx4y1n7yU/)

> [视频：【Agent共学第二期】银海分享 | 用AI重塑我的工作流](https://www.bilibili.com/video/BV1sr421L7Hj/)

> [视频：【Agent共学第二期】大家一起捏 Bot，Coze 作品分享会](https://www.bilibili.com/video/BV1hT421v7YD/)

> [视频：【Agent共学第二期】Bot冠军大揭秘：李小白](https://www.bilibili.com/video/BV1L1421y7zx/)

> [视频：【Agent共学第二期】两位个人Bot创作者的分享：《你出生的那一天》和《热点文章生成器》](https://www.bilibili.com/video/BV1DD421u7m7/)

> [视频：【Agent共学第二期】一点都不简单的共创之路](https://www.bilibili.com/video/BV1ei421v7hA/)

> [61儿童节，我给儿子做了两款coze小应用，让他见识一下程序员爸爸的厉害。](https://mp.weixin.qq.com/s/YxPxpds9OJl0CWXTCYfxWg)

> [视频：使用「扣子/Coze」搭建文本纠错助手](https://www.bilibili.com/video/BV1q7421o7xx/)

> [六一【黑科技】礼物，AI“复活”玩具！细节剖析\~](https://mp.weixin.qq.com/s/-sK0Nb8xNZN8XQ0SixHKaw)

> [这是Coze平台上最完善、最强大的Notion连接器](https://mp.weixin.qq.com/s/3gzSEjWxnxB0dRKFZvOx4g)

> [最贴心的coze bot：从零开始的bot搭建实战](https://juejin.cn/post/7362743871979831311)

> [数据何规接入AI客服（kimi版）啦！](https://mp.weixin.qq.com/s/zibF1XMFPBBMLnbNKn2alw)

> [人民日报健康客户端：智能对话 科学防癌 AI赋能肿瘤防治行动](https://ar.peopledailyhealth.com/ai/index.html)

> [使用 coze 打造私人播客助手 - 根据个人喜好自动化生成播客](https://mp.weixin.qq.com/s/BmhwFJBf7_t88zI15at8jA)

> [字节COZE应用创作平台，开发 AI chatbot（短视频爆款案例）初探](https://mp.weixin.qq.com/s/5R21o5BCNXZQd6ZgkTx8bg)

> [使用Coze制作MidJourney提示词专家](https://mp.weixin.qq.com/s/BTzdCzIkrh2Nq11Eh5adOA)

> [使用扣子Coze创建AI绘画助手](https://mp.weixin.qq.com/s/9Me7PiCpykquPSATqI0cRw)

> [我用Coze搓了一个乞丐版的秘塔搜索](https://waytoagi.feishu.cn/wiki/IM2TwbChWixcR9kEt87cmKsHnAc)

> [用Coze搞一个简单的安全AI助手](https://mp.weixin.qq.com/s/QE6V_UZs7WsOHMuQOTZ5DA)

> [英语怎么快速提高？我用 Coze AI 免费手搓了一个 24 小时陪练教师](https://zhuanlan.zhihu.com/p/691177635)

> [玩转 Coze，我帮开源 AI 社区搞了一个社群运营机器人](https://juejin.cn/post/7365704703362269184)

> [保姆级教程！教你如何用扣子搭建一个免费好用的“图片转表格”AI客服（附实操过程+效果）](https://mp.weixin.qq.com/s/FOcAaARTnTp50D49ZKPZow)

> [前端智能化，扣子（](https://mp.weixin.qq.com/s/tiolzTwPKPZF4b8zZbvYpA)[coze.cn](https://mp.weixin.qq.com/s/tiolzTwPKPZF4b8zZbvYpA)[）能做什么？](https://mp.weixin.qq.com/s/tiolzTwPKPZF4b8zZbvYpA)

> [【AI学习】如何用扣子搭建“赛事活动AI客服”机器人？亲测效果好](https://www.toutiao.com/article/7367384038752977417)

> [重磅！浙师版ChatGPT，上线！](https://mp.weixin.qq.com/s/ltLcAbKUv08Ym08FKCpcEw)

> [字节最新发布的Coze太好用了，我也不想取代合规老师的工作啊！](https://mp.weixin.qq.com/s/dgr9GhWatREfOR61s0iucg)

> [从0到1 | 使用coze国内版部署飞书bot机器人、豆包智能体](https://mp.weixin.qq.com/s/suaawdGz453LaRX6kAcAcA)

> [Coze + 爬虫 = 周末去哪不用愁！！](https://mp.weixin.qq.com/s/OfN3ndVfye9p_0wIeuQWng)

> [今天拿到心动offer，这个AI有点东西…](https://mp.weixin.qq.com/s/QNgY1EC6nvPu1vRJOaLcPA)

> [从0到1无代码使用coze搭建一对一作画工具](https://mp.weixin.qq.com/s/KZ6VjwbxQ9_emrAhSYUyrA)

> [应对裁员潮,突发奇想,打造“收割offer”智能体.......](https://mp.weixin.qq.com/s/JZpKf_mSEJCXfZklKBCpKA)

> [通过 Coze API 打造强大的微信图片助手](https://www.feishu.cn/wiki/A4sJweE25iZsBDkziG1crnkAnHf)</cite>

# **❤S 彭俊旗的AI工具箱**

https://www.coze.cn/store/agent

官方商店中，有过万的智能体，根据收藏人数和使用评论次数，可以找到一些场景下的智能体最佳实践。可惜官方没有给排序功能，但是翻几页大概能看出使用多的都在前面。

这个公众号，把Coze官方最多人使用的智能体找出来，然后用逆向的方式进行复刻并开源，达到原智能体近似的效果，可以比较全面的看到最佳实践，和智能体的搭建细节，包括提示词。

<table><colgroup><col/><col/><col/><col/></colgroup><tbody><tr><td><b>评级</b></td><td><b>智能体</b></td><td><b>具体实现过程</b></td><td><b>补充</b></td></tr><tr><td>S
插件和工作流搭建</td><td>自媒体运营大师
https://www.coze.cn/store/project/7453438932919812133</td><td>https://mp.weixin.qq.com/s/zcw10tPUib9HnANyUAiDkQ</td><td>
 </td></tr><tr><td>S-
非Coze公开，有代码嵌入</td><td>批量处理pdf合同</td><td>https://mp.weixin.qq.com/s/FP2N8hvi09xRFlDfqFGxIw</td><td></td></tr><tr><td>S-
细节复刻</td><td>表情包生成器
https://www.coze.cn/store/project/7444083905063567410</td><td>https://mp.weixin.qq.com/s/WTu2UgpDViqZkfaRBrzecw</td><td></td></tr><tr><td>S-
细节复刻</td><td>图文工厂
https://www.coze.cn/store/project/7453092645703811099</td><td>https://mp.weixin.qq.com/s/GWnVYYfiG3sk1Xl_9OINTw
https://mp.weixin.qq.com/s/OPyi_gIyV5YrSnKxMit9Zw</td><td></td></tr><tr><td>S-
细节复刻</td><td>AI抠图神器
https://www.coze.cn/store/project/7443274617134923827</td><td>https://mp.weixin.qq.com/s/Ke7uIbxQN5RnARWfuYZfWg</td><td></td></tr><tr><td>A+
文章「插件」部分的思考</td><td>一键整理会议/读书/方案
https://www.coze.cn/store/agent/7357721169338073123</td><td>https://mp.weixin.qq.com/s/jy0YTjooxS-RlDYmpxcUQg</td><td></td></tr><tr><td>A
核心是提示词复刻难度低</td><td>姓名打分
https://www.coze.cn/store/agent/7405842780536356927</td><td>https://mp.weixin.qq.com/s/ZXWYJRbProm4iMFspkO_AA</td><td></td></tr></tbody></table>

# A 韦恩AI智能体定制

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td><b>评级</b></td><td><b>主题</b></td><td><b>公众号链接</b></td></tr><tr><td>A+
有几张关于AI落地的图</td><td>AI智能体企业落地实战坊分享</td><td>https://mp.weixin.qq.com/s/qQyirRvenrYop_hZylkuoQ
韦恩-智能破局：AI智能体应用落地实战.pdf<figure view-type="Card"><source name="output (4).pdf" mime="application/pdf" size="13310146" token="IeADbEsX1oqFsrxNbovcbs6BnAh"/></figure></td></tr><tr><td>A</td><td>一个节点的智能体，变现了</td><td>https://mp.weixin.qq.com/s/-9ftlP1Jt5XgeYfddJP6Jw</td></tr><tr><td>A</td><td>5分钟做个出海报的智能体——即梦3.0效果</td><td>https://mp.weixin.qq.com/s/09NNewE4exUpTdZcF5aIAg</td></tr><tr><td>A</td><td>用激活码保护你的AI智能体</td><td>https://mp.weixin.qq.com/s/lq53Stuwb8psqnPfi7_qzQ</td></tr></tbody></table>

# 比赛：看最佳实践

> 以提升审美为主，多数都没有对应的构建过程。

## A+ 扣子 AI 工坊 Coze AI Factory

2024年6月coze官方举办的一次大赛，下面把获奖的主要作品摘录下来。

https://www.coze.cn/open/docs/guides/

**全赛道总冠军**

急诊室的一夜：[https://www.coze.cn/store/bot/7385073552590012435](https://www.coze.cn/store/bot/7385073552590012435)

搭建过程：https://mp.weixin.qq.com/s/qu08P3zB8RDw90nXwZKUXQ

**实用工具赛道奖项**

| **名次** | **Bot名称** | **Bot链接** |
|-|-|-|
| 一等奖  | 我要买什么\~问题解决师  | [https://www.coze.cn/store/bot/7381764402032394303](https://www.coze.cn/store/bot/7381764402032394303) |
| 二等奖  | 胖豆大厨（PandaChef）1.1  | [https://www.coze.cn/store/bot/7385130217649537058](https://www.coze.cn/store/bot/7385130217649537058) |
| 二等奖  | 小帅漫话技术  | [https://www.coze.cn/store/bot/7382230396894887988](https://www.coze.cn/store/bot/7382230396894887988) |
| 三等奖  | 去留学  | [https://www.coze.cn/store/bot/7385124995413852200](https://www.coze.cn/store/bot/7385124995413852200) |
| 三等奖  | 星语-多工作流科学写作  | [https://www.coze.cn/store/bot/7383556199616135179](https://www.coze.cn/store/bot/7383556199616135179) |
| 三等奖  | 小白爱旅行  | [https://www.coze.cn/store/bot/7383708800202686499](https://www.coze.cn/store/bot/7383708800202686499) |
| 最佳人气奖  | 小雷选机  | [https://www.coze.cn/store/bot/7379971455104172059](https://www.coze.cn/store/bot/7379971455104172059) |
| 最佳创意奖  | 小红书美妆类文案生成助手  | [https://www.coze.cn/store/bot/7384801399416045605](https://www.coze.cn/store/bot/7384801399416045605) |
| 最佳技术奖  | 智能分析助手  | [https://www.coze.cn/store/bot/7384775031236198419](https://www.coze.cn/store/bot/7384775031236198419) |

**图文创作赛道奖项**

| **名次** | **Bot名称** | **Bot链接** |
|-|-|-|
| 一等奖  | 电商背景设计大师  | [https://www.coze.cn/store/bot/7385199593866280960](https://www.coze.cn/store/bot/7385199593866280960) |
| 二等奖  | 胖豆摄影师（PandaPhotographer）1.1  | [https://www.coze.cn/store/bot/7385120590879031315](https://www.coze.cn/store/bot/7385120590879031315) |
| 二等奖  | 阿星AI编辑室  | [https://www.coze.cn/store/bot/7384692368978706473](https://www.coze.cn/store/bot/7384692368978706473) |
| 三等奖  | 小红书爆款文案【专家定制 必出爆款】  | [https://www.coze.cn/store/bot/7384844095866503168](https://www.coze.cn/store/bot/7384844095866503168) |
| 三等奖  | 儿童绘本故事-视频生成  | [https://www.coze.cn/store/bot/7385124820096237620](https://www.coze.cn/store/bot/7385124820096237620) |
| 三等奖  | 小众旅行  | [https://www.coze.cn/store/bot/7383217900334776347](https://www.coze.cn/store/bot/7383217900334776347) |
| 最佳人气奖  | 找三思做二十四节气海报  | [https://www.coze.cn/store/bot/7382246186440359945](https://www.coze.cn/store/bot/7382246186440359945) |
| 最佳创意奖  | 你的漫画  | [https://www.coze.cn/store/bot/7384289588510113827](https://www.coze.cn/store/bot/7384289588510113827) |
| 最佳技术奖  | 10W粉博主私藏写作神器  | [https://www.coze.cn/store/bot/7383683749017305129](https://www.coze.cn/store/bot/7383683749017305129) |

**互动创意赛道奖项**

| **名次** | **Bot名称** | **Bot链接** |
|-|-|-|
| 一等奖  | 小精灵-莉莉娅  | [https://www.coze.cn/store/bot/7384208632562384908](https://www.coze.cn/store/bot/7384208632562384908) |
| 二等奖  | 平行世界  | [https://www.coze.cn/store/bot/7384808238245707839](https://www.coze.cn/store/bot/7384808238245707839) |
| 二等奖  | 藤原拓海の改装坊  | [https://www.coze.cn/store/bot/7384750901476622374](https://www.coze.cn/store/bot/7384750901476622374) |
| 三等奖  | 历史名人时空导游  | [https://www.coze.cn/store/bot/7384472094102536203](https://www.coze.cn/store/bot/7384472094102536203) |
| 三等奖  | 这个茶馆不一般 V2  | [https://www.coze.cn/store/bot/7385193187125493795](https://www.coze.cn/store/bot/7385193187125493795) |
| 三等奖  |  东方市公安局之谜案重重  | [https://www.coze.cn/store/bot/7384842524357263395](https://www.coze.cn/store/bot/7384842524357263395) |
| 最佳创意  | 神仙也要考绩效？！  | [https://www.coze.cn/store/bot/7384967539241025588](https://www.coze.cn/store/bot/7384967539241025588) |
| 最佳技术  | 时空邀约—来自未来的你  | [https://www.coze.cn/store/bot/7385147856169992226](https://www.coze.cn/store/bot/7385147856169992226) |

## A 扣子X豆包8月主题活动

| **名次** | **Bot名称** | **作品链接** |
|-|-|-|
| 一等奖  | 嗨!皇叔 | https://www.coze.cn/s/ir9fqcWo/ |
| 二等奖  | 超级英语备课助手MuseGuru  | https://www.coze.cn/store/bot/7402427962244792329?bot_id=true |
| 二等奖  | 高效写论文智能体助手 | https://www.coze.cn/s/irCbWMBY/ |
| 二等奖  | 今天营养吃够了吗? | https://www.coze.cn/store/bot/7404011157037760527?panel=1&bid=6dgcq8br4400j |
| 三等奖  | 塔罗牌占卜大师 | https://www.coze.cn/s/irYEYs99/ |
| 三等奖  | 与KOKO一起练英语 | https://www.coze.cn/store/bot/7404057244339453978?panel=1&bid=6dg6hr5oo000a |
| 三等奖  | 超级奶爸 | https://www.coze.cn/store/bot/7400249016430182412?from=bots_card&panel=1&bid=6dgdk3j9s7g1k |
| 三等奖  | 听话胶囊图片表情包生成器 | https://www.coze.cn/store/bot/7402345506577481739 |
| 三等奖  | 知识分解器 | https://www.coze.cn/store/bot/7403273231500591158?panel=1&bid=6dg6d2kc80g1j |
| 三等奖  | 养娃日常记录的AI助手 | https://www.coze.cn/store/bot/7402264801151516706?panel=1&bid=6dgck7b040g0a |

## A- 与 AI 童行，扣子创意 Bot 挑战赛

天马行空奖

| **Bot名称** | **作品链接** |
|-|-|
| 拼图游乐馆  | [https://www.coze.cn/s/ijDAPJQs/](https://www.coze.cn/s/ijDAPJQs/) |
| MuseGuru  | [https://www.coze.cn/s/ijPckoYr/](https://www.coze.cn/s/ijPckoYr/) |
| 冠军欧洲  | [https://www.coze.cn/store/bot/7379639244861767707](https://www.coze.cn/store/bot/7379639244861767707) |

才华横溢奖

| **Bot名称** | **作品链接** |
|-|-|
| AI电子宠物  | [https://www.coze.cn/store/bot/7373938556126969891?bot_id=true](https://www.coze.cn/store/bot/7373938556126969891?bot_id=true) |
| 找三思做二十四节气海报  | [https://www.coze.cn/s/i68qvBce/](https://www.coze.cn/s/i68qvBce/) |
| 成语拼图  | [https://www.coze.cn/store/bot/7376928713239445530](https://www.coze.cn/store/bot/7376928713239445530) |
| 网页总结 · 万物皆可脑图（url-脑图）  | [https://www.coze.cn/store/bot/7375878065538465819?panel=1&bid=6cnvbr4to9g00](https://www.coze.cn/store/bot/7375878065538465819?panel=1&bid=6cnvbr4to9g00) |
| 小白爱旅行  | [https://www.coze.cn/store/bot/7383708800202686499?panel=1&bid=6cu1pug240g14](https://www.coze.cn/store/bot/7383708800202686499?panel=1&bid=6cu1pug240g14) |

# ————2025年5月10日更新————

## S 一泽的 AI 实践分享

有思路有细节有测试有认知，非常全面的优质教程/案例。

1. [万字实践教程，全面入门 Coze 工作流｜用 Coze 打造 AI 精读专家智能体，复刻 100 万粉公众号的创作生产力](https://www.feishu.cn/wiki/Jp6ewePXKiQKUMkI0MScYxjinPc)</cite>
2. [Coze+飞书多维表格，打造专属 AI 智能体，享受 10 倍知识管理效率｜一泽的 AI 实践分享](https://www.feishu.cn/wiki/GfAGwQb76i4WNCk9lzHcGZZmnpY)</cite>

## S- **云中江树的知识库**

比较全面的知识库，案例较少。

1. [普通人如何使用 coze 打造个人专属智能体](https://www.feishu.cn/wiki/BIImwitvkiRx36kHQYWcYfdCncc)</cite>
2. [教你在扣子上做多Agents智能体](https://www.feishu.cn/wiki/PuG9wjP2mi81Oek1vFPcj7FCnsf)</cite>

# 知乎

### ❤A+ **斜杠君**

> 每篇内容都相对完整，内容相对较新，判断原创的比较多。

https://www.zhihu.com/column/c_1761416767527022592

<sheet sheet-id="x5FLYL" token="Vn5YsgjRLhEV35tumsQc3LF3noZ"></sheet>

### ❤A- 灯塔AIGC

> 每篇内容都相对完整，有具体的工作流拆解，但是没有提示词（可以逆向），基本都在A。

知乎专栏：https://www.zhihu.com/people/fu-sheng-si-yue

Coze合集：https://www.coze.cn/user/2522754578914201

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td><b>分类</b></td><td><b>主题</b></td><td><b>知乎链接</b></td></tr><tr><td rowspan="9">图文</td><td>小红书爆款梗图工作流搭建</td><td>https://zhuanlan.zhihu.com/p/17208433532</td></tr><tr><td>小红书爆款养生图文工作流搭建</td><td>https://zhuanlan.zhihu.com/p/17469014448</td></tr><tr><td>一个案例学会智能体卡片</td><td>https://zhuanlan.zhihu.com/p/17728767851</td></tr><tr><td>一个案例学会智能体卡片(2)</td><td>https://zhuanlan.zhihu.com/p/17892221749</td></tr><tr><td>1.5W次使用的官方推荐模板，5个节点就可以搭建？</td><td>https://zhuanlan.zhihu.com/p/18117718410</td></tr><tr><td>小绿书、小红书爆款发疯文学梗图批量出图</td><td>https://zhuanlan.zhihu.com/p/18326104610</td></tr><tr><td>小红书爆款英语单词卡片视频制作</td><td>https://zhuanlan.zhihu.com/p/18955585681</td></tr><tr><td>春节朋友圈拜年配图、文案智能体</td><td>https://zhuanlan.zhihu.com/p/20142837665</td></tr><tr><td>【减肥赛道】爆款图文，Coze工作流一键批量创作</td><td>https://zhuanlan.zhihu.com/p/31148681761</td></tr><tr><td rowspan="4">批处理文字</td><td>DeepSeek+智能体搭建作文批改助手</td><td>https://zhuanlan.zhihu.com/p/26899110287</td></tr><tr><td>工作流+飞书多维表格，自动抓取+分析100条小红书笔记详细数据</td><td>https://zhuanlan.zhihu.com/p/29299113503</td></tr><tr><td>一键获取100条爆款文案，高效仿写爆款（工作流教程）</td><td>https://zhuanlan.zhihu.com/p/30345060927</td></tr><tr><td>小红书爆款【百岁老人养生计划】，工作流一键批量创作</td><td>https://zhuanlan.zhihu.com/p/29490572063</td></tr><tr><td rowspan="7">视频</td><td>100W+播放的爆款养生视频</td><td>https://zhuanlan.zhihu.com/p/32060777482</td></tr><tr><td>少儿英语阅读学习视频</td><td>https://zhuanlan.zhihu.com/p/32974934252</td></tr><tr><td>短视频文案提取+分析+仿写AI工具</td><td>https://zhuanlan.zhihu.com/p/1889081514064602191</td></tr><tr><td>100W+播放的爆款国学文化视频</td><td>https://zhuanlan.zhihu.com/p/1890066141382148782</td></tr><tr><td>10W+点赞情感治愈系漫剪视频</td><td>https://zhuanlan.zhihu.com/p/1892280390552622880</td></tr><tr><td>治愈老奶奶老爷爷爆款视频</td><td>https://zhuanlan.zhihu.com/p/1894478797207745400</td></tr><tr><td>短视频文案提取+批量仿写</td><td>https://zhuanlan.zhihu.com/p/1895239757803524790</td></tr></tbody></table>

### A+ 如何用 Coze 搭建图文生成+排版一体化工作流？

https://zhuanlan.zhihu.com/p/767518027

### A+ 一键出海报！超简单的Coze入门案例实战教程

https://zhuanlan.zhihu.com/p/1896186658682024896

### A AI 开发者必学！掌握 Coze 工作流核心技能的全攻略！

https://zhuanlan.zhihu.com/p/17117887085

### A RAG回答准确率暴涨300%！用Coze工作流进行数据结构化

https://zhuanlan.zhihu.com/p/1888226234275709019

### A 扣子(Coze)实战案例：不想做攻略？AI来帮你收集地方美食！

https://zhuanlan.zhihu.com/p/20053708411

### A- 使用扣子Coze制作一个智能询价客服

https://zhuanlan.zhihu.com/p/18800159266

### B+ 对于扣子Coze初学者来说，有哪些可以快速上手的优秀案例值得参考？

https://www.zhihu.com/question/9313514383/answer/1900608903110165946

1. 搭建一个【每日定时新闻推送】AI智能体
2. 小红书发疯图文
3. 每日学成语类型视频的工作流

# ❤A- YC项目（创业向）

> 把YC投资的AI项目，https://www.ycombinator.com/companies/industry/ai
> 在2023年之后的进行了筛选，找到使用生成式AI、可能是使用智能体技术作为核心的项目进行整理

<table><colgroup><col/><col/><col/><col/><col/></colgroup><tbody><tr><td><b>分类</b></td><td><b>分类</b></td><td><b>项目</b></td><td><b>简介</b></td><td><b>链接</b></td></tr><tr><td>专项业务</td><td>会计</td><td><b>Truewind</b></td><td></td><td>https://www.ycombinator.com/companies/truewind</td></tr><tr><td></td><td>保险</td><td><b>Remy</b></td><td></td><td>https://www.ycombinator.com/companies/remy</td></tr><tr><td></td><td>税务</td><td><b>TaxGPT</b></td><td></td><td>https://www.ycombinator.com/companies/taxgpt</td></tr><tr><td></td><td>抵押贷款</td><td><b>Approval AI</b></td><td></td><td>https://www.ycombinator.com/companies/approval-ai</td></tr><tr><td></td><td>合规</td><td><b>Diligent</b></td><td></td><td>https://www.ycombinator.com/companies/diligent</td></tr><tr><td></td><td>贷款指导</td><td><b>Casca</b></td><td></td><td>https://www.ycombinator.com/companies/casca</td></tr><tr><td></td><td>审计</td><td><b>Agentive</b></td><td></td><td>https://www.ycombinator.com/companies/agentive</td></tr><tr><td></td><td>供应商</td><td><b>Mandel AI</b></td><td></td><td>https://www.ycombinator.com/companies/mandel-ai</td></tr><tr><td></td><td>采购</td><td><b>askLio</b></td><td></td><td>https://www.ycombinator.com/companies/asklio</td></tr><tr><td></td><td>碳核算</td><td><b>GreenTally</b></td><td></td><td>https://www.ycombinator.com/companies/greentally</td></tr><tr><td>辅助业务</td><td>辅助业务</td><td><b>Marblism</b></td><td></td><td>https://www.ycombinator.com/companies/marblism</td></tr><tr><td></td><td>挖掘真实</td><td><b>TruthSuite</b></td><td></td><td>https://www.ycombinator.com/companies/truthsuite</td></tr><tr><td></td><td></td><td><b>StackAI</b>
部署自定义 AI 代理</td><td></td><td>https://www.ycombinator.com/companies/stackai</td></tr><tr><td></td><td></td><td><b>Spine AI</b></td><td></td><td>https://www.ycombinator.com/companies/industry/ai</td></tr><tr><td></td><td>发现机会</td><td><b>Canvas</b></td><td></td><td>https://www.ycombinator.com/companies/canvas</td></tr><tr><td>通用能力</td><td>AI工具</td><td><b>Deasy Labs</b></td><td></td><td>https://www.ycombinator.com/companies/deasy-labs</td></tr><tr><td></td><td>高效学习</td><td><b>Shepherd</b></td><td></td><td>https://www.ycombinator.com/companies/shepherd-2</td></tr><tr><td></td><td>AI电话助理</td><td><b>Pernell</b></td><td></td><td>https://www.ycombinator.com/companies/pernell</td></tr><tr><td></td><td>AI电话助理</td><td><b>Cactus</b></td><td></td><td>https://www.ycombinator.com/companies/oncactus</td></tr><tr><td></td><td>复制人类动作</td><td><b>Basepilot</b></td><td></td><td>https://www.ycombinator.com/companies/basepilot</td></tr><tr><td></td><td>搜索+资料整合</td><td><b>Lumona</b></td><td></td><td>https://www.ycombinator.com/companies/lumona</td></tr><tr><td></td><td></td><td><b>Tegon</b></td><td></td><td>https://www.ycombinator.com/companies/tegon</td></tr><tr><td></td><td>通用数据</td><td><b>camelAI</b></td><td></td><td>https://www.ycombinator.com/companies/camelai</td></tr><tr><td rowspan="5">音视频</td><td>视频</td><td><b>AIVideo.com</b></td><td></td><td>https://www.ycombinator.com/companies/aivideo-com</td></tr><tr><td>语音</td><td><b>Aqua Voice</b></td><td></td><td>https://www.ycombinator.com/companies/aqua-voice</td></tr><tr><td>语音</td><td><b>Fluently</b></td><td></td><td>https://www.ycombinator.com/companies/fluently</td></tr><tr><td>音频</td><td><b>Magic Hour</b></td><td></td><td>https://www.ycombinator.com/companies/magic-hour</td></tr><tr><td>语音</td><td><b>Ponder</b></td><td></td><td>https://www.ycombinator.com/companies/ponder</td></tr></tbody></table>

# Youtube（案例没有想象中多）

### A+ 从0开始在Coze中通过节点搭建一套新闻搜索并AI改写工作流

https://www.youtube.com/watch?v=BpOEVg85Nos&t=8s

### A 10分钟手把手教你搭建Coze工作流 ：一个可接入微信小程序

https://www.youtube.com/watch?v=083BtkeUHtc

### A 文章精炼扩写

https://www.youtube.com/watch?v=BF1Iu60-ODw

### A 一键自动生成国风养生视频，手把手教你制作古风养生中医视频

https://www.youtube.com/watch?v=-bkv3WgCE2g

### A 5分钟学会用Coze制作爆火心理学火柴人视频 | 零基础可操作

细节还比较丰富

https://www.youtube.com/watch?v=JVP7W0SOY7s

# Github

> Coze比较少，其他的ComfyUI等开源的很多
> 有一些类教程的资料，下面这个Excel的智能体搭建比较完整

## A- [Excel智能分析及优化](https://www.coze.cn/template/workflow/7438532887869177907?entity_type=23)

https://github.com/datawhalechina/coze-ai-assistant

这是一款智能数据分析助手，能够自动处理Excel数据并输出洞察。用户只需上传Excel文件，系统就能自动完成数据分析、可视化呈现、特征优化等工作,大幅提升数据分析效率,降低使用门槛。

支持的功能:

1. 智能数据分析

   - 自动进行描述性统计分析
   - 相关性分析和趋势发现
   - 异常值检测与处理
   - 数据质量评估报告
2. 数据可视化

   - 支持柱状图、折线图、散点图等多种图表
   - 智能推荐最适合的可视化方式
   - 生成可视化分析

参考项目：[Excel智能分析及优化（付费模板）](https://www.coze.cn/template/workflow/7438532887869177907?entity_type=23)

对话流名称：Excel_Smart_Processing

对话流描述：表格智能分析及优化

我们可以把整体看为有五个输出

**设计目标：**

好久的案例，忘了，等等再写

**制作流程：**

我们一个输出做一个整体来说，共四个输出整体

### 新建一个 对话流，并打开

对话流名称： `Excel_Smart_Processing`

对话流描述： `表格智能分析及优化`

### 输出一：接受数据表，减少用户使用时间

1. 添加输出节点

重命名： `消息_文件接受`

输出变量：无

输出内容：

```Plain Text
已接受到数据表，正在进行剖析
```

### 输出二：数据快速描述性统计

1. 代码块

节点类型名称：文本处理

选择应用：字符串拼接

输入 String1：开始-BOT_USER_INPUT

字符串拼接：

1. 数据的快速描述性统计

节点类型名称：插件-代码执行器

输入： code —— 代码块-output

1. 数据分析

节点类型名称：大模型

模型选择：豆包·1.5·Pro·32k

输入：

input —— str.数据的快速描述性统计result中的FinalOutput

系统提示词

1. 信息

节点类型名称：输出

输出变量：output ——str. 数据分析 output

第二个输出的整体样子如下

### 输出三：生成特征工程代码

1. 代码拼接

节点类型名称：文本处理

选择应用：字符串拼接

输入 String1：开始-BOT_USER_INPUT

字符串拼接

1. 读取excel字段与前五行

节点类型名称：插件-代码执行器

输入： code ——代码拼接-output

1. 数据分析

节点类型名称：大模型

模型选择：豆包·工具调用

输入：

input —— str. 数据的快速描述性统计 result-Object中的FinalOutput

系统提示词：

用户提示词：

1. 输出代码1

重命名： `消息_文件接受`

输出变量：output —— str. 生成特征工程代码-output

输出内容：

输出三的整体样子如下

### 输出四：生成可视化图片

这个输出我们将从输出三的第二节点开始，如下图所示

1. 生成可视化代码

节点类型名称：大模型

模型选择：豆包·1.5·Pro·32k

输入：

input —— str.数据的快速描述性统计result中的FinalOutput

系统提示词：

用户提示词：

1. 代码拼接1

节点类型名称：文本处理

选择应用：字符串拼接

输入 String1：开始-BOT_USER_INPUT

输入 String2：生成可视化代码-python_code

字符串拼接

1. 数据可视化

节点类型名称：插件-代码执行器

输入： code —— 代码块-output

1. 判断图片是否生成成功

条件分支

如果不为空

1. 图片生成成功

节点类型名称：文本处理

选择应用：字符串拼接

输入 String1：数据可视化-PicList

字符串拼接

### **数据可视化结果📊**![生成图片]({{String1[0]}})

1. 图片生成失败

节点类型名称：文本处理

选择应用：字符串拼接

输入 String1：数据可视化-PicList

字符串拼接

### **生成图片失败/(ㄒoㄒ)/\~\~**![图片生成失败](https://www.emojiall.com/en/header-svg/%E2%9D%8C.svg)**注意**：报错原因为{{String1}}，小概率会出现环境中没有相关字体的情况，建议重新运行一下

输出三的整体样子如下

### 输出五：特征工程执行展示

从第三个输出的结束开始

1. 代码拼接2

节点类型名称：文本处理

选择应用：字符串拼接

输入 String1：开始-BOT_USER_INPUT

输入 String2：生成特征工程代码 - output

字符串拼接

1. 特征工程

节点类型名称：插件-代码执行器

输入： code ——代码拼接2-output

1. 判断执行是否成功

条件分支 大于等于

如果：

1. 输出前五行代码

节点类型名称：文本处理

选择应用：字符串拼接

输入 String1：开始-BOT_USER_INPUT

输入 String2：生成特征工程代码 - output

字符串拼接

1. 输出前五行

节点类型名称：插件-代码执行器

输入： code ——输出前五行代码-output

1. 特征工程失败

节点类型名称：文本处理

选择应用：字符串拼接

字符串拼接

1. 特征工程失败

节点类型名称：文本处理

选择应用：字符串拼接

字符串拼接

好的，现在让我们看看整体的流程：

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI落地Live第51/52场 Candy](01-AI落地Live第51／52场%20Candy.md)

---

<details>
<summary>原文配图上的文字（52 条，图片本身未随文提供）</summary>

**SWayToAGIAIAgent合集**

- 「谁是‘人类’」 「Coze」 「DeepSeek」 「欧洲杯」

**S大圣AI超级个体Coze保姆级教程**

- 「Coze AI Agent？」 「Coze小红书爆款笔记大师 - 升级优化版」 「Coze智能体：古诗绘画工作流 - 古诗拆解（数组）」

**S彭俊旗的AI工具箱**

- 「智能体搭建案例、相关项目链接及细节复刻」
- 「去上架智能体」 「华泰股市助手」 「DeepSeek R1能力一」 「高速路况查询」 「懂车帝」
- 「立即体验」 「AI助手」 「天眼查」
- 「上传智能体」 「小红书爆款文案神器」 「文案改写」 「恋爱神器：情诗生成」
- 「自媒体运营大师」 「自媒体运营大师（2月18日更新）」
- 「表情包生成器」 「能DO，得加钱」
- 「图文工厂(DeepSeek模型版)」 「DeepSeek驱动，开启图文制作AutoPilot模式！」 「细节复刻」
- 「抠图✂️神器」 「AI抠图神器」
- 「思维导图」 「豆包·工具调用」
- 「姓名打分」

**A扣子AI工坊CozeAIFactory**

- 「01 <bot>」 「03 <knowledge>」 「图文创作赛道」 「实用工具赛道」 「互动创意赛道」 「扣子AI工坊 COZE AI FACTORY」 「6.13 - 6.30（2024）」 「扫码报名，13万奖金 超多流量扶持等你来拿！」 「扣子 × intel」
- 「急诊室的一夜」
- 「我要买什么~问题解决师」 「胖豆大厨（PandaChef）1.1」 「小帅漫话技术」 「去留学」 「星语-多工作流科学写作」 「小白爱旅行」 「小雷选机」 「小红书美妆类文案生成助手」 「智能分析助手」 「火车票小管家」
- Coze AI Factory比赛图文创作赛道奖项。表格中列出名次、Bot名称及Bot链接。一等奖为电商背景设计大师，链接为https://www.coze.cn/store/bot/7385199593866280960；二等奖有胖豆摄影师（PandaPhotographer）1.1和阿星AI编辑室，链接分别为https://www.coze.cn/store/bot/7385120590879

**A斜杠君**

- 「扣子(Coze)实战教程」 「已更内容」 「一键批量抓取小红书博主所有笔记写入飞书表格」

**A灯塔AIGC**

- 「养生视频（动态图生成）」 「儿童故事绘本视频创作」 「短视频文案歌词写诗（文化篇）」

**AYC项目创业向**

- 「生成式AI」 「健康保险」 「人工智能」
- 名为税务GPT的项目相关信息，该项目所属标签为春夏2024，状态为活跃，拥有11名员工，地点位于美国加利福尼亚州旧金山。它是面向会计师和税务专业人士的TaxGPT AI副驾驶，可通过自动化税务研究、客户沟通、入司流程和安全文档收集，将税务公司的生产力和盈利能力提高10倍。此外，该项目的分类标签包含金融科技、B2B餐厅、人工智能
- 「人工智能」 「金融科技」 「防欺诈」 「监管科技」
- 创业公司Casca的相关信息。其位于美国加利福尼亚州旧金山，有25名员工，2023年活跃。Casca正在为银行业构建AGI，用AI原生记录系统取代30+年传统技术，自动化90%手动工作。其首个产品是AI原生贷款发放系统，内置AI代理Sarah，通过电子邮件或短信与小企业贷款申请人沟通，指导完成申请流程并准备贷款文件。下方有对话式银行、金融科技、机器学习、金融、人工智能等标签
- 「代理 Y 春夏 2023」
- 曼德尔人工智能（Mandel）的相关信息。其成立于2023年，位于美国加利福尼亚州旧金山，有3名员工。该企业通过电子邮件AI揭示供应链中断和供应商更新，使用AI代理主动提取数据并向供应商发送电子邮件以进行订单更新，从而构建实时自我更新的供应链事实来源。图片下方有其所属的行业分类标签，包括人工智能、制造业、供应链、采购、企业软件
- 是askLio公司的相关信息页面内容，该公司标注为2023年春夏阶段，地处美国加利福尼亚州旧金山，当前处于活跃状态，拥有3名员工。其核心业务是构建面向企业采购团队的AI Copilots，将员工采购某样东西的流程耗时从原来的数周缩短到数小时。该公司由AI工程师和采购专家创立，他们此前曾合作建立过AI初创公司，将自身产品视作每位采购经理的额外助手，可平均为企业节省数百万美元，还能将采购经理的手动工作
- 格林理货（GreenTally）的相关信息。其成立于2023年，位于美国加利福尼亚州圣马特奥市，有2名员工。GreenTally是一个为所有企业构建的碳核算平台，使用LLM帮助公司以小时而非月为单位测量碳足迹，可自动进行排放计算和报告，使企业满足监管要求并跟踪减排目标，无需顾问或专门的可持续发展团队。图片中还列出了其所属类别，包括人工智能、生成式AI、机器学习、软件即服务、人工智能
- 「人工智能」 「生成式AI」 「机器学习」 「法律科技」
- 「人工智能」 「自动化」
- Spine AI的相关信息。其成立于2023年，位于美国加利福尼亚州旧金山，有5名员工。Spine构建可靠的AI基础设施，为Facets提供支持，该系统专为私人市场打造，可自动执行关键工作流程，提供综合情报，使IR团队有效向LP代表资金，加快筹款周期和交割速度。图片还列出了其所属类别，包括金融科技、生成式AI、软件即服务、投资、人工智能
- 「软件即服务」 「客户成功案例」 「分析学」 「人工智能」
- Deasy Labs的相关信息。其为AI工作流提供元数据编排，平台为AI团队提供创建高质量自定义元数据并嵌入其AI工作流程的最佳方式。三位创始人来自亚马逊、麦肯锡/QuantumBlack和MIT，此前在麦肯锡内部构建ML数据治理工具，与11家财富500强公司部署。2023年初，创建高质量元数据成为趋势。图片
- 「牧羊人（Shepherd）」
- 「人工智能」 「对话式AI」
- 名为仙人掌（X2025系列）的创业项目信息，该项目主体位于美国加利福尼亚州旧金山，在职员工2名，所属类别为软件即服务、B2B餐厅、人工智能。该项目正计划为个体创业者构建一款AI副驾驶类的工具，可自动化处理个体创业者的管理工作，具体功能包括接听电话、确定客户资格与记录收入，其定位是类似Jarvis的Ironman的AI业务助手，旨在帮助个体创业者取得成功
- 是开源问题跟踪工具Tegon的相关介绍内容。Tegon是针对工程团队问题跟踪设计的工具，能简化问题跟踪工作，特点是易于使用且功能强大，解决了现有同类工具存在的复杂性和缓慢性问题，现有工具往往通过增添流程和手动任务降低工程师工作效率，无法帮助工程师更快解决问题或获取任务完整上下文，Tegon则通过智能使用AI及集成功能，实现任务的自动创建与更新，还能辅助工程师明确任务
- 「骆驼AI」 「软件即服务」 「数据科学」 「数据可视化」 「人工智能」 「camelAI」
- AIVideo.com的相关信息。其成立于2023年，位于美国加利福尼亚州奥克兰，有7名员工。公司构建了一个AI代理来创建专业品质的视频，时间成本仅为传统视频制作的1%。AI代理在单个工作流程中使用数十个特定于任务的AI模型，编排完整视频（脚本、视觉效果、VoiceOver、效果等）的创建。该图片
- 「生成式AI」 「NLP」 「人工智能」
- Magic Hour的相关信息。其为一款专业的视频创作工具，采用AI视频模型，将它们放在一个工作流程中，使创建视频像选择模板并自定义一样简单。Magic Hour有2名员工，在职，位于美国加利福尼亚州旧金山。用户可访问https://magichour.ai使用该产品。图片
- 关于A-YC项目分类下的音频项目Magic Hour的介绍，该项目隶属于音视频类目下的音频细分领域，是一款专业的视频创作工具。图片中还展示了Magic Hour的标识，以及该项目的相关信息，包括其推出内容、所属类别链接等

**A5分钟学会用Coze制作爆火心理学火柴人视频零**

- 「新闻搜索」 「AI改写」 「工作流程介绍」 「时间图设计步骤」 「我们等会就是输出的这几个文档 We will output these documents later.」

**AExcel智能分析及优化httpswwwcoz**

- 「Excel_Smart_Processing」

**输出二数据快速描述性统计**

- 「数据分析{{output}}」

**输出三生成特征工程代码**

- 「开始进行特征工程，相关代码如下...」

**输出四生成可视化图片**

- 「Excel_Smart_Processing」 「代码拼接」 「读取excel字段与前五行」 「生成特征工程代码」 「输出代码1」 「code——代码块-output」 「output」
- 「input」 「String」 「数据的快速描述性统计 - FinalOutput」 「生成可视化代码」
- 「数据可视化 - PicList」 「empty」 「生成可视化图片」
- 「判断图片是否生成成功」 「PicList Array<String>」

**数据可视化结果生成图片String10**

- 「数据可视化」 「String1」 「数据可视化 - FinalOutput」 「生成可视化代码」 「代码拼接1」 「读取excel字段与前五行」 「代码拼接」

**生成图片失败ㄒoㄒ图片生成失败httpswwwe**

- 「生成可视化图片」

**输出五特征工程执行展示**

- 「Excel_Smart_Processing」 「读取Excel文件并提取五行」 「生成特征工程代码」 「输出前五行代码」
- 「Excel_Smart_Processing」 「输出五：特征工程执行展示」

</details>
