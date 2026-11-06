---
title: 一页纸模版：Agent从0到实操到工程化落地 副本
node_token: Nbdswocm8iq4uvkHET0cPR89nkf
source: https://www.feishu.cn/wiki/Nbdswocm8iq4uvkHET0cPR89nkf
space: 一堂学习
obj_type: docx
synced: 2026-09-26 06:25
course_line: 深度研修
stage: 私董会
train: 私董会
form: 课程逐字稿
audience: MBA专属
---
# 顶层设计

## 极简定义：快速理解

> *1-3句话，简单说明Agent的目标和价值*

## 内核边界：场景和目标

> *要使用这个工具的场景，以及实现目标的追求，重点分析边界*

**目标：**

**使用场景：**

1. XXXXX
2. XXXXX

**业务目标：**

1. XXXXX
2. XXXXX

**关键边界：**

1. XXXXX
2. XXXXX

# 关键筹备

## 知识：关键方法和知识

> *必备的方法论、分析方法、专家经验和数据*

<table><colgroup><col/><col/></colgroup><thead><tr><th>参考策略</th><th>我可能的知识（待验证假设）</th></tr></thead><tbody><tr><td><ol><li seq="1">专家经验：哪些专家擅长/贡献知识</li><li>工作流程：具体的做事流程/SOP</li><li>方法论模型：哪些方法论和模型</li><li>非结构化知识：知识库和文章库</li><li>结构化数据：标注过的数据</li></ol></td><td></td></tr></tbody></table>

## 评估：合格和优秀

> *至少有评估维度，最好有5-10个测试Case和预期产出；*

<table><colgroup><col/><col/></colgroup><thead><tr><th>参考策略</th><th>我可能的知识（待验证假设）</th></tr></thead><tbody><tr><td rowspan="6"><ol><li seq="1">专家评估：专家定性评估质量</li><li>最佳实践池：和人工案例集对比</li><li>雷达图评估：评估的维度</li><li>测试样本 ：正/负面案例</li><li>严格数据评估（准确率/召回率等）</li></ol></td><td></td></tr><tr><td rowspan="5"></td></tr><tr></tr><tr></tr><tr></tr><tr></tr></tbody></table>

# 基础搭建

## 使用LLM基本验证

> *先用模型初步多轮对话尝试，初步感受一下AI的能力，*
>
> *初步验证一下关键节点、风险和假设，建立一波信心。*

## 使用Coze思路

> *使用的技术、策略和大致的工作流；*
>
> *建议可以用『纸质卡牌』摆一摆然后拍照放这里*

**工作流设计（类比纸牌摆放）：**

## 使用多维表格

> *可以用多维表格作为数据存储和工作流处理*
>
> *如果用到可以写一写基本思路，****当然也可以为空****。*

<sheet sheet-id="GUV9sF" token="DvsasZ4dNhm34otlZTucsOcfnca"></sheet>

## 使用其他工具

> *如果需要使用其他的工具，也可以整理思路在这里*
>
> *比如不同的LLM，Dify，RPA、API、MCP等等。*

# 工程化落地

> *如何提升更好的工程化落地和提升质量*

## 工程化的三大追求

<table><colgroup><col/><col/><col/></colgroup><thead><tr><th><b>三大追求</b></th><th><b>我的设计</b></th><th><b>参考案例</b></th></tr></thead><tbody><tr><td><b>上限稳定</b></td><td><ol><li seq="1"></li></ol></td><td><ol><li seq="1"><em>100 条稳定可筛出 3-5 条可用</em></li><li><em>不同月份数据质量稳定</em></li></ol></td></tr><tr><td><b>下限可控</b></td><td><ol><li seq="1"></li></ol></td><td><ol><li seq="1"><em>必须用原文，不能自己编造</em></li><li><em>不能出现用户真实姓名和手机号</em></li><li><em>不能有竞对名字和评价</em></li><li><em>不能有涉黄/骂人/政治敏感信息</em></li></ol></td></tr><tr><td><b>成本经济</b></td><td><ol><li seq="1"></li></ol></td><td><ol><li seq="1"><em>每月显性成本显著低于班主任成本；</em></li><li><em>每 1000 条成本低于 100 元；</em></li></ol></td></tr></tbody></table>

## 策略1 拆：拆模块化

<table><colgroup><col/><col/></colgroup><thead><tr><th>参考策略</th><th>计划的工作（待验证假设）</th></tr></thead><tbody><tr><td rowspan="6"><ol><li seq="1">基本：按执行 SOP/按动作</li><li>进阶：加评审/提取/校对/XXX</li><li>高阶：ReAct 机制，反思机制</li></ol></td><td>参考：可以把一个“AI 录音转逐字稿”的统一提示词，拆解成【】【】【】【】【】五个节点来分别配置和调试。</td></tr><tr><td rowspan="5"><ol><li seq="1"> </li><li> </li><li> </li></ol></td></tr><tr></tr><tr></tr><tr></tr><tr></tr></tbody></table>

## 策略2 配：配上下文

<table><colgroup><col/><col/></colgroup><thead><tr><th>参考策略</th><th>计划的工作（待验证假设）</th></tr></thead><tbody><tr><td rowspan="6"><ol><li seq="1">优化提示词：<ol><li seq="1">增加角色</li><li>增加参考</li><li>增加说明</li></ol></li><li>增加知识库</li><li>增加数据库/多维表格</li><li>使用插件/工具</li></ol></td><td>参考：给“AI 把录音稿撰写逐字稿”节点增加一个知识库参考：过去历史最佳实践案例清单。</td></tr><tr><td rowspan="5"><ol><li seq="1"> </li><li> </li><li> </li></ol>
 </td></tr><tr></tr><tr></tr><tr></tr><tr></tr></tbody></table>

## 策略3 测：AB 测试

<table><colgroup><col/><col/></colgroup><thead><tr><th>参考策略</th><th>计划的工作（待验证假设）</th></tr></thead><tbody><tr><td rowspan="6"><ol><li seq="1">测不同提示词</li><li>测不同模型<ol><li seq="1">测不同大语言模型</li><li>同一模型不同版本</li><li>同一版本不同参数</li></ol></li><li>测不同节点（多少/配置方式）</li><li>测不同知识/数据库</li><li>测不同插件工具</li></ol></td><td>参考：给 AI 撰写清单体笔记，分别测试【DeepSeekV3】【DeepSeekR1】和【Kimi】的不同交付质量。</td></tr><tr><td rowspan="5"><ol><li seq="1"> </li><li> </li><li> </li></ol>
 </td></tr><tr></tr><tr></tr><tr></tr><tr></tr></tbody></table>

## 策略4 调：调试问题

<table><colgroup><col/><col/></colgroup><thead><tr><th>参考策略</th><th>计划的工作（待验证假设）</th></tr></thead><tbody><tr><td rowspan="6"><ol><li seq="1">看整体输出</li><li>看每一步的输出</li><li>看过程日志</li><li>强制输出中间结果</li><li>用好 COZE 罗盘</li></ol></td><td>参考：在【预处理】【排版】和【初稿】分别打印可视化的日志，存到多维表格。</td></tr><tr><td rowspan="5"><ol><li seq="1"> </li><li> </li><li> </li></ol>
 </td></tr><tr></tr><tr></tr><tr></tr><tr></tr></tbody></table>

---
> [!info]- 🧭 导航
> ⬆️ 上级：[周一晚NPC AI基本功线上内训L1 磨课 副本](02-周一晚NPC%20AI基本功线上内训L1%20磨课%20副本.md)
