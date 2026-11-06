---
title: AI落地Live1：生成海报和两段代码
node_token: Lzs7wqEeqiNbkNklxNHcKURinIb
source: https://www.feishu.cn/wiki/Lzs7wqEeqiNbkNklxNHcKURinIb
space: 一堂学习
obj_type: docx
synced: 2026-09-25 18:57
course_line: AI能力线
stage: AI设计
train: AI设计
form: 直播逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
AI落地Live1：生成海报和两段代码

分享的内容

生成一张海报用图

任务场景

解决思路

实现步骤

实际演示

小结

工具和基础

处理一个Excel的程序

任务场景

解决思路

实现步骤

实际演示

小结

工具和基础

完成一个稍复杂的程序

任务场景

解决思路

实现步骤

拆解工作流

任务：完成数据接口访问拿到数据

任务：用链接抓取文章保存本地

任务：完成正则表达分析微信链接

任务：完成文章内容分析并打分

综合结果

小结

工具和基础

回顾和小结

作业

AI落地Live1：生成海报和两段代码

哈喽哈喽，大家好\~

我是于陆，先快速自我介绍一下吧。

 1.曾经是少校，在部队内做技术研究；

2.两次创业，烧了大几百万，一个是搞砸之夜，一个倒在单元模型没跑通；

3.2021年认识一堂，2022年加入一堂做课程产品经理，做过N节小案例课（搞砸之夜、落地之夜、其他案例课等）；

4.**负责AI俱乐部的运营。**

**一堂AI落地Live**

在一堂内部，其实已经在很多场景，用AI能力去提高效率了。

为了和大家一起加速学习和使用AI，我们决定**把一堂使用AI的真实场景，给大家分享出来**。给大家看看我们是怎么用的，给一个参考借鉴的例子，所以就有了**一堂AI落地Live。**

这件事暂定计划是执行一个月，每周用30分钟时间，来分享3-5个真实能力，如果反馈不错，再扩大内容，让有意愿分享的同学也加入进来。

说几个特点：

•**真实性**：颗粒度有大有小，但都是真实场景，真实落地；

•**易用性**：从入门、到进阶和高阶，都尽量体现，覆盖各个层面的同学；

•**开放性**：你有什么想学的能力，抛出来，我们一起学；我们讲的不好的，你来纠正。

**AI落地Live规则**

1.不是课程是分享：和大家一样，都是在探索AI落地；如果有更简单，更好的解决方案，欢迎你在评论区反馈，或者写作业。

2.评论区积极优化：请勿讨论与本场话题无关的内容，尊重其他同学，尊重分享人；有什么没说清楚的概念，评论区帮忙解答一下。

# 分享的内容

为了方便学习，说一下今天分享的三个内容：

1.**生成海报：**GPT4 + DALL-E3，5分钟生成一张海报用图。

2.**生成代码：**GPT3.5/4，生成一段处理Excel的Python代码。

3.**生成代码：**GPT3.5/4，生成一个复杂的Python代码。

## 生成一张海报用图

 *GPT4+DALL·E 3 Prompt：生成个一张图片，借助GPT文生图，目标高大上，比例16:9*

用5分钟，给Prompt大赛做了一张海报。

### **任务场景**

在进行大赛宣传时，需要制作一张海报。但团队只有一位兼职设计师，如果不想占用设计师资源，如何快速制作一个及格的海报？

### **解决思路**

1.用文生图工具生成一张背景图片

2.找海报模板，填充内容

### **实现步骤**

**第一步：**试生成，看效果。

使用**GPT4+DALL·E 3。**

选用这个方案的原因是：

•简单：小白友好，提示词简单，不用复杂设计；

•快速：基本不用等待，半分钟出图；

•质量：可以接受。

虽然 Stable Diffusion 和 Mid Journey 具有更好的可控性和细节质量，但*需要更详细的提示词设计和反复调试，使用门槛较高*，因此在这个场景中不使用它们。

  Stable Diffusion 和 Mid Journey 是另外两个著名的文生图工具。

还使用**豆包的AI漫画生成，和星火大模型**尝试过，因为风格较少，没有选用。

这是一组赛博朋克风格的人物海报，对应生成海报的相关实验内容。海报围绕“多人华山论剑”的主题，以霓虹闪烁的未来都市为背景，呈现了多组身着融合传统与赛博朋克元素服饰的武侠风格人物，部分人物配备刀剑类武器。海报的视觉设计呼应了该场景中文生图工具的风格选择方向，是使用指定类AI工具生成创意海报的成果展示，直观呈现了赛博风武侠主题的创作效果。

【Prompt🤖】：生成一张图片，使用提示词比拼的华山论剑。

看看生成的效果。

**第二步：**选定风格，匹配需求，生成图片。

一步一步调整提示词，匹配需求。

1.决定选择**黑白/水墨风格**，因为它可能更符合「华山论剑」这个主题的特点；

2.**上一步的提示词，加上**背景空旷一些，给文字留出空间；

3.**上一步的提示词，加上**比例9:16的要求。

**第三步**：寻找模板，完成设计。

不展开说了，这一步是找一个做海报的网站，选一个参考的海报，填充信息。

### 实际演示

内部测试的时候，大家反馈光看可能体感不够，那我们**实际来看看**。

【交互🙋♂️】你们来描述一个场景，现场看看AIGC能够做到什么程度。

**小结**

这个案例说了一件事：无需专家资源占用，快速拿到及格产品。从原来需要占用专家1-2小时的80分+设计，变成了可以快速生成的60分流程。

**工具和基础**

1.**工具环境：**

a.推荐：GPT4+DALL·E 3

b.备选：豆包，SD，MJ，LiblibAI

2.**使用基础**：少量提示词知识

第一个分享说完了，比较简单。能够这么容易的做这件事，还是因为GPT的能力升级，把这件事所需的能力，**从进阶降低到了入门的「简单聊天」**。原先需要在GPT里面帮助你设计一组提示词（反向提示词），然后拿到更专业的工具中，才能得到最终结果，现在一个工具内部就能完成。

这一波GPT引入DALL-E3，带来的变化比想象中还要多。不展开了，这里有一篇文章，除了类似上面写的文生图的案例，还描述了一个更开阔的使用场景，我有些感同身受，你逐字稿拿到之后，可以阅读一下。从DALL-E 3接入ChatGPT说起

在开始下面的分享之前，我想问个问题。

【交互🙋♂️】整个这一系列的分享，如果有一些自动化的处理的部分，大概率会用到Python，先了解一下大家的开发能力。会Python的扣1；会用其他语言的扣2；不会写任何程序的扣3。

作为一个非典型Python开发者，推荐大家尝试一下用GPT写程序。因为**大语言模型加持下，写程序的壁垒已破，几乎可以无基础的去写程序。**

写程序、写代码，咱不提什么 程序 = 数据结构 + 算法 这种黑话，用大白话说，将具体需求转换成程序语言，并执行完成一定的功能。个人观点，很多人的工作是在用“非典型的程序语言”在写程序。

•**Before**：用户需求-产品经理挖掘解释-程序员写程序-机器执行

•**After**：用户需求-GPT写程序-机器执行

即便你是零基础，现在完全可以**解放思想**学一下怎么写程序，有问题可以直接问GPT，比如说一下我想学习写程序，比如我想搭建一个可以跑Python程序的环境，我该怎么做。如果需要帮助，可以扣一下“我要写代码”，下次分享场，考虑用两分钟介绍一下。

处理一个Excel的程序

 *GPT4+DALL·E 3 Prompt：生成个一张图片，借助GPT分析Excel，目标高大上，比例16:9*

**任务场景**

今年年初，Truman提了一个叫做GONGJIAN的计划，邀请大家一起GONGJIAN课程，用这个方式，今天和同学们攻克了很多很难的课题。所以每次共建课程最后，会附上一个共建名单，来感谢大家陪我们一起做课。

在导出共建名单，生成图片的过程，有一个比较麻烦的工作，就是**对共建名单进行去重和整理，最后再排成7列**。

可以看出来，原始数据有一些问题：

1.重复出现：比如王震南同学，范同学，都出现了很多次。

2.姓名错误：比如姓名处是“一堂创业者”，这是因为同学没有在绑定过程，没有写真实姓名。这时候就需要用微信昵称替代姓名。

有些共建，不只是从一个渠道获得数据，比如作业一部分、晚餐会一部分、以及其他共建，所以纯粹的SQL不容易直接写出来。

还有一些场景下，共建的名单列表里面，会有一些班班、助理等一堂工作人员的名字进入，还需要手工把这些家伙挑出来。

除了解决这两个问题，还需要排成7列，为此雨安（一堂产品经理），还专门录了个视频教大家怎么处理。

原来整个流程，从下载数据，到最后排成7列，熟练之后，10-15分钟可以搞定。但是经常需要返工：

1.漏了“一堂创业者”或者忘了删除工作人员，一个“一堂创业者”可能代表着几位同学；

2.名单发生变动，为了保证所有共建同学都能出现在列表中，课程的共建列表至少生成两次，一次是课程当天下午，一次是课程开始之前。

每次返工就要重新导出、筛选、排序、分列，是一个费眼、费心、费力的小工作。这里欢迎大家报名一堂的课程共建活动，我们真的会非常认真的对待每一位同学的名字，让他们出现在课程和"小黄书"上面。

【思考💡】因为我更熟悉Python，所以我请GPT帮我生成的是程序，理论上这个需求完全可以只用Excel去实现，这个就交给你们去尝试了。

共建名单试手版.xlsx

视频仅支持MP4格式

**解决思路**

所以当教研助理Sherry找到我的时候，我们讨论了一下。写个程序来完成。回顾一下需求：

1.分析Excel中的内容

2.去除重复的同学

3.排除官方人员

4.尽量用姓名，姓名不准确再用昵称

5.排成7列

6.使用图形界面，便于使用 #追加

 **名词解释：图形界面**

实现步骤

大概用了十来分钟，写了一个Prompt，完成了一段小小的代码，来解决这个问题。

【Prompt🤖】：

你是一个强大的的程序员，请帮我生成一个MAC系统下处理Excel的图形python程序。你只需要完成代码，要求如下：

1. 界面大小是600x400，并在屏幕中央，有一个按钮[读取]，点击之后，可以选择系统中的一个Excel文件，后缀xlsx，并进行处理

2. 需要解析的Excel分成三列，第一列是ssoid，第二列是姓名，第三列是微信昵称

3. 输出结果是一个不重复的人名列表

4. 遍历所有行，根据id的唯一性，进行去重

5. 排除掉id在一个数组内的的行（排除官方人员）

6. 如果一行之内姓名为空，或者姓名是“一堂创业者”，则输出人名使用昵称

7. 将获得的列表，分成7列，输出到原Excel目录，文件名后缀增加“\_去重”

8. 给出的代码合并到一个文件

格式不重要，文字内容混成一块也是一样效果。

 你是一个强大的的程序员，请帮我生成一个MAC系统下处理Excel的图形python程序。你只需要完成代码，要求如下：界面大小是600x400，并在屏幕中央，有一个按钮[读取]，点击之后，可以选择系统中的一个Excel文件，后缀xlsx，并进行处理；需要解析的Excel分成三列，第一列是ssoid，第二列是姓名，第三列是微信昵称；输出结果是一个不重复的人名列表；遍历所有行，根据id的唯一性，进行去重；排除掉id在一个数组内的的行（排除官方人员）；如果一行之内姓名为空，或者姓名是“一堂创业者”，则输出人名使用昵称；将获得的列表，分成7列，输出到原Excel目录，文件名后缀增加“\_去重”；输出的代码合并到一个文件。

这个需求比较简单，没有刻意套用提示词框架，但是下面几个要素是必备的

1.**背景角色**

a.给GPT一个人设：你是一个强大的的程序员

b.需要解析的Excel分成三列，第一列是ssoid，第二列是姓名，第三列是微信昵称

2.**需求细节**，3-7

3.**解决方案**

a.MAC系统下处理Excel的图形python程序

b.你只需要完成代码

c.给出的代码合并到一个文件

 **名词解释：遍历**

Prompt吐给GPT4，一次性生成程序，完成了这个小需求。

 实测效果 GPT4 ≥ GPT3.5 ≥ 其他模型

 代码如下：

import tkinter as tk

from tkinter import filedialog

import pandas as pd

import os

def center_window(window, width=600, height=400):

    *# 获取屏幕 宽、高*

    ws = window.winfo_screenwidth()

    hs = window.winfo_screenheight()

    *# 计算 x, y 位置*

    x = (ws / 2) - (width / 2)

    y = (hs / 2) - (height / 2)

    window.geometry('%dx%d+%d+%d' % (width, height, x, y))

def read_and_process_excel():

    file_path = filedialog.askopenfilename(filetypes=[("Excel files", "\*.xlsx")])

    if not file_path:  *# 如果没有选择文件，则返回*

        return

    df = pd.read_excel(file_path)

    *# 假定的官方人员ID列表*

    official_ids = ['id1', 'id2']  *# 请根据实际情况替换这些占位符*

    *# 移除官方人员条目*

    df = df[\~df['ssoid'].isin(official_ids)]

    *# 去重并处理姓名和昵称*

    unique_entries = {}

    for \_, row in df.iterrows():

        ssoid = row['ssoid']

        if ssoid not in unique_entries:

            name = row['姓名'] if row['姓名'] and row['姓名'] != '一堂创业者' else row['微信昵称']

            unique_entries[ssoid] = name

    *# 转换为DataFrame*

    final_df = pd.DataFrame(list(unique_entries.items()), columns=['ssoid', '姓名'])

    *# 分成7列*

    reshaped = pd.DataFrame(final_df['姓名'].values.reshape(-1, 7))

    *# 保存到新的Excel文件*

    new_file_path = os.path.splitext(file_path)[0] + '\_去重.xlsx'

    reshaped.to_excel(new_file_path, index=False)

    label_output.config(text=f"处理完成，文件已保存为： {new_file_path}")

*# 创建TKinter窗口*

root = tk.Tk()

root.title("Excel Processor")

center_window(root)

*# 添加读取文件按钮*

button_load = tk.Button(root, text="读取", command=read_and_process_excel)

button_load.pack(expand=True)

*# 添加输出标签*

label_output = tk.Label(root, text="")

label_output.pack(expand=True)

*# 运行TKinter主循环*

root.mainloop()

**解决错误**

因为大语言模型的特性，不一定每次都能生成完美的程序，只需要把程序执行出现的问题告诉GPT，让它重新生成即可。

【Prompt🤖】：刚刚执行的时候出现了xx问题，请帮我重新生成一下所有的代码，合并到一个代码文件中。

**迭代问题**

【Prompt🤖】：增加一个要求：如果姓名为空或者姓名是"一堂创业者"，同时微信昵称也是空，那么最后结果中，可以删除这一条记录，然后给我一个完整的代码吧

实际演示

再看一下实际的操作。

hhh，电脑被我搞死机了，不如直接把文件给你们，你们自己试一下。

共建名单试手版.xlsx

视频仅支持MP4格式

**小结**

这个案例说了一件事：怎么用自然语言，写一段简单的程序。从原来10-30分钟的容易出错的一个流程，变成了可以用程序1秒钟解决的工具。

**工具和基础**

1.**工具环境：**

a.推荐：Visual Studio CODE

b.备选：Cursor、命令行

2.**使用基础**：写程序的少量基础知识

Candy：

给一个亲测好用的分析Excel提示词框架：

 你是一个强大的的程序员，请帮我生成一个MAC系统下处理Excel的图形程序。你只需要完成代码，要求如下：

1. 界面大小是600x400，并在屏幕中央，有一个按钮[读取]，点击之后，可以选择系统中的一个Excel文件

2. 需要解析的Excel分成N列，第一列是xx，第二列是xx，第三列是xx……

3. 点击[处理]按钮，进行处理，输出结果是

4. 遍历所有行……

5. ……

6. ……

7. 将获得的列表，输出到原Excel目录，文件名后缀增加“\_去重”

8.给出的代码合并到一个文件

完成一个稍复杂的程序

 *GPT4+DALL·E 3 Prompt：生成个一张图片，借助GPT写一个复杂的程序，目标高大上，比例16:9*

这个例子，属于**高阶里面的最简单应用，**但是还是比较偏写程序，我尽量聚焦在把事情说清楚上，少讲专业的部分。

**任务场景**

AI俱乐部有十几个群，每天同学们会发一些有价值的链接到群里，我需要每天整理信息，沉淀到知识库。

AI俱乐部·共建资讯信息

每天手动进行，容易忘记，能不能提炼摘要，能不能自动进行，并判断分类？

解决思路

**尝试用工具做摘要分析**

首先看看，能不能直接用工具完成。

**测试方法**

1.使用最简单的Prompt，在各个LLM网页对话中收集反馈

a.【Prompt🤖】帮我分析一下文章内容

https://mp.weixin.qq.com/s?\_\_biz=MjM5MTk3NTYyMA==&mid=2651272287&idx=1&sn=9e5c0c2c4a871e5a8fe9694663d891a6

2.原始链接：生成式人工智能：发展演进及产业机遇｜GGView

**测试结果**

<table><colgroup><col/><col/><col/></colgroup><tbody><tr><td><b>LLM</b>  </td><td><b>是否可用</b>  </td><td><b>测试结果</b>  </td></tr><tr><td>讯飞星火
https://xinghuo.xfyun.cn/desk  </td><td>不可用  </td><td></td></tr><tr><td>智谱清言
https://chatglm.cn/detail  </td><td>不可用  </td><td></td></tr><tr><td>百川大模型
https://www.baichuan-ai.com/chat  </td><td>不可用  </td><td></td></tr><tr><td>豆包
https://www.doubao.com/chat/  </td><td>不可用  </td><td></td></tr><tr><td>文心一言
 </td><td>不可用  </td><td>-  </td></tr><tr><td>文心一言
助手  </td><td>不可用  </td><td></td></tr></tbody></table>

 结论：截止止2023年09月07日，测试的大模型没有达到可用的结果。

收到俱乐部专家Edward的启发，能不能用Make.com完成？

**测试结果：**如果方案是配合Notion和GPT，可以选择。不提风险，小规模+接飞书，不太适用。

还是写程序吧，哈哈哈。

实现步骤

拆解工作流

1.调用metabase API，获取待处理数据

2.循环处理列表

a.从中间找到微信链接

b.将微信链接通过抓取，保存文章到本地

c.利用星火模型的接口，调用分析能力

d.记录保存的结果

3.调用飞书接口，将处理结果保存到多维表格

4.多维表格发送消息提示进行内容更新

5.串联整个逻辑

拆解工作流，是宜骄（AI俱乐部主理人）一直在提倡的一个动作，可以说是使用AI降本增效的一个基础。

怎么拆解？我个人的理解和动作：记录-提炼-归纳-迭代。

📌

GPT完成代码，部分使用ChatGPT3.5，部分使用豆包、星火等模型。

任务：完成数据接口访问拿到数据

完全没有用过metabase，怎么从它那里拿到数据？

【Prompt🤖】帮我写一个python程序，可以调用metabase API获取数据

def login_to_metabase(username, password):

    """

    登录metabase

    """

    login_url = f"{METABASE_URL}/api/session"

    response = requests.post(

        login_url, json={"username": username, "password": password}, verify=False)

    print("Login response status code:", response.status_code)

    print("Login response content:", response.content)

    if response.status_code == 200:

        token = response.json()['id']

        return token

    else:

        print(response)

        raise Exception("登录到Metabase失败")

def execute_metabase_query(token, query_id):

    """

    查询metabase

    """

    query_url = f"{METABASE_URL}/api/card/{query_id}/query"

    headers = {"X-Metabase-Session": token}

    response = requests.post(query_url, headers=headers)

    print("Query url:", query_url)

    print("Query response status code:", response.status_code)

    print("Query response content:", response.content)

    decoded_text = response.content.decode('utf-8')

    print("Query decoded_text content:", decoded_text)

    save_to_file(get_date(query_id), decoded_text)

    if response.status_code == 202:

        return decoded_text

    else:

        raise Exception("查询Metabase失败")

任务：用链接抓取文章保存本地

import re

import requests

import csv

import os

def extract_http_links(text):

    *# 使用正则表达式提取http链接*

    return re.findall(r'http[s]?://(?:[a-zA-Z]|[0-9]|[\$-\_@.&+]|[!\*\\\\(\\\\),]|(?:%[0-9a-fA-F][0-9a-fA-F]))+', text)

def fetch_web_content(url):

    response = requests.get(url)

    response.raise_for_status()  *# 如果请求失败，这将引发HTTPError异常*

    return response.text

def call_api(content):

    *# 这里是一个示例，你需要根据实际API进行调整*

    *# response = requests.post('YOUR_API_ENDPOINT', data={'content': content})*

    *# return response.json()*

    return {"result": "processed content"}  *# 示例返回*

def save_to_csv(data, filename):

    with open(filename, 'w', newline='') as csvfile:

        writer = csv.writer(csvfile)

        writer.writerow(['URL', 'Processed Content'])

        for row in data:

            writer.writerow(row)

def main():

    items = ["Here is a link: http://example.com", "No link here", "Another link: https://openai.com"]

    processed_data = []

    for item in items:

        links = extract_http_links(item)

        for link in links:

            content_filename = f"content\_{hash(link)}.txt"

            api_result_filename = f"api_result\_{hash(link)}.txt"

            *# 如果本地已有内容，则不再进行网络请求*

            if os.path.exists(content_filename):

                with open(content_filename, 'r') as f:

                    content = f.read()

            else:

                content = fetch_web_content(link)

                with open(content_filename, 'w') as f:

                    f.write(content)

            *# 如果本地已有API结果，则不再调用API*

            if os.path.exists(api_result_filename):

                with open(api_result_filename, 'r') as f:

                    api_result = f.read()

            else:

                api_result = call_api(content)

                with open(api_result_filename, 'w') as f:

                    f.write(str(api_result))

            processed_data.append((link, api_result['result']))

    save_to_csv(processed_data, 'results.csv')

if \_\_name\_\_ == "\_\_main\_\_":

    main()

注意：

1.你需要安装requests库来运行上述代码。

2.这只是一个基础示例，你可能需要根据实际情况进行调整，例如处理网络请求的异常、调整API调用等。

3.为了简化示例，我使用了hash()函数来为每个链接生成一个唯一的文件名。在实际应用中，你可能需要使用更稳定和可靠的方法。

 备注：hash()函数是动态的，后面改成了MD5。

任务：完成正则表达分析微信链接

【Prompt🤖】帮我写一个正则匹配，要求给一个url字符串

要求1：必须包含mp.weixin.qq.com

要求2：删除"&chksm"和其后的所有字符

请用"https://mp.weixin.qq.com/s?\_\_biz=MjM5MDAyMzQyMQ==&mid=2650871639&idx=1&sn=77de9f9ff0aa5efdac2f8794beec17dd&chksm=bdbe9cc58ac915d30c3c14d07bf496a2f6c3dfa5e9be6929960af2f4942a4977022c5d86e217&mpshare=1&scene=1&srcid=0902U6Eea1jBBW3mu3jKisDR&sharer_shareinfo=93fbf720b998cd6d3716542394c5ac3a&sharer_shareinfo_first=2d4b0706872310622b6364c7480e98e5#rd"举例子来说明正则的有效

import re

url = "https://mp.weixin.qq.com/s?\_\_biz=MjM5MDAyMzQyMQ==&mid=2650871639&idx=1&sn=77de9f9ff0aa5efdac2f8794beec17dd&chksm=bdbe9cc58ac915d30c3c14d07bf496a2f6c3dfa5e9be6929960af2f4942a4977022c5d86e217&mpshare=1&scene=1&srcid=0902U6Eea1jBBW3mu3jKisDR&sharer_shareinfo=93fbf720b998cd6d3716542394c5ac3a&sharer_shareinfo_first=2d4b0706872310622b6364c7480e98e5#rd"

*# 匹配包含"mp.weixin.qq.com"的 URL*

match = re.search(r'mp.weixin.qq.com', url)

*# 如果匹配成功，删除"&chksm"和其后的所有字符*

if match:

    cleaned_url = re.sub(r'&chksm.\*', '', url)

else:

    cleaned_url = url

print(cleaned_url)

运行上述代码，输出结果为：

https://mp.weixin.qq.com/s?\_\_biz=MjM5MDAyMzQyMQ==&mid=2650871639&idx=1&sn=77de9f9ff0aa5efdac2f8794beec17dd

可以看到，正则表达式成功地删除了"&chksm

任务：完成文章内容分析并打分

【Prompt🤖】你是人工智能领域的专家，并且非常熟悉创业和商业领域，现在请你帮我阅读一些文章进行分析。下面是我的需求：

1.阅读文章内容，总结输出文章摘要

2.阅读文章内容，分析主要内容属于哪种，并按照下面分层标准打标签，必须放到下面四个之一

    第一个是宏观层，可以是说行业的发展趋势

    第二个是使用层，比如文章主要内容说的是AI能力的具体应用，这一层需要多打一个具体应用方向的标签

    第三个是创业层，讲的是最新的创业动向，新兴企业

    第四个是技术层，内容是技术的变化，或者是和AI相关的技术变化

3.根据你的判断，给文章内容打个分数，最低5分，最高10分，按照以下标准

    1）最前沿的信息，加分

    2）最影响产业的信息，或者对产业带来重大变动，加分

    3）内容受众面窄，减分

    4）太专业的内容适当减分，减分

    5）时效性低，减分

    6）打分是整数，分数标准可以严格一些，大部分文章可以给8分

文章摘要：英特尔在9月19日的技术创新大会上推出了首款基于Intel4制程工艺打造的MeteorLake处理器平台。MeteorLake有5大技术亮点，包括采用最新的Intel4制程工艺和全新的微架构、分离式模块化设计、采用3D封装技术Foveros、首次将人工智能加速引擎NPU集成到CPU处理器上以及Arc独显技术回馈到集成显卡，提升了Meteor Lake的图形引擎的性能。

主要内容分析：这篇文章主要介绍了英特尔推出的新款处理器MeteorLake的技术特点和优势，属于使用层，具体应用方向是AI能力的具体应用。

评分：

最前沿的信息：8分，文章介绍了英特尔的最新处理器技术和产品。

最影响产业的信息：7分，文章介绍了英特尔在处理器技术上的创新，可能对整个行业产生影响。

内容受众面窄：6分，文章主要面向科技领域的专业人士和对AI技术感兴趣的读者。

太专业的内容：7分，文章详细介绍了MeteorLake的技术特点和优势，对于普通读者来说可能较难理解。

时效性低：7分，虽然文章没有提到具体的发布时间，但作为英特尔最新推出的产品，具有一定的时效性。

综合结果

没有完美达到预期，*星火1.5分析结果还不够好，2.0没能调通*。

算一下ROI，完全调通的价值<现在半手动完成的价值。

自动化节约的时间<每篇文章阅读、打分给我带来信息的价值。

小结

整个过程中，混用了ChatGPT3.5/4，和其他的一些语言模型，综合下来GPT3.5/4在开发上的表现不错。提升了80%+的效率。跳过了很多外部能力的学习过程，比如什么metabase、beautifulSoup等。没听过，对吧，我也只是听过，没有用过。

每天节约的时间，原来是10分钟，现在两分钟，接通星火2.0之后，有希望达到全自动。

**工具和基础**

1.**工具环境：**

a.推荐：Visual Studio CODE

b.备选：Cursor、命令行

2.**使用基础**：

a.写程序的一定知识

b.需要串联调试的能力

回顾和小结

1.使用门槛在逐渐降低，百花齐放+多模态聚合

a.各个模态的复合能力值得期待

b.未来一定是没有Prompt的，而是自然语言交流

2.突破了领域边界

a.绘画领域

i.不需要会画画，不需要会摄影，需要审美、需要工具使用

b.在开发领域

i.大语言模型极大降低了写程序门槛

ii.大语言模型极大提高了写程序效率

多说几句关于俱乐部运营。

•群里面的信息很有用，谢谢你们，请继续抛信息；

•开了几次AI私董会，分析了一些项目，还会持续，未来扩大到所有俱乐部同学；

•有合作的需求么？找合伙人，搭建团队？

作业

虽说叫作业，但更像线索收集。

**第一个题目：案例心得题**

今天讲了3个小案例，听完了之后，你有哪些新的收获？说说你的心得体会和思考，个人、业务层面的思考都可以聊聊。

**第二个题目：我的案例题**

看了一堂的实践，有没有你可以在自己的业务中借鉴的地方，可以尝试之后反馈一下。更好的情况是，你已经在用各种AI能力，并且真实在业务中体现价值，只是一个Prompt都可以写一写。如果你愿意，下次可以讲你的案例或者你来分享。

**第三个题目：许愿题**

你有什么想学想了解的内容，比如我想用GPT帮我写订阅号文章，比如我想用AIGC生成一个头像，等等需求，你都可以提出来，我们来学/找高手分享。

**课程建议：**

这个部分欢迎大家吐槽，分享形式、内容，有什么不足的，请多反馈给我，这个系列能不能持续下去就看这些反馈了。

🎁 作业奖励Candy：这次分享，我们希望能准备出一个特别的案例集《我用AI做XXX》落地集，这应该是一个非常有趣的案例合集，你可以来看看身边同学的学习段位、知行合一，欢迎相互抄抄彼此的作业。

【Flag🙋】

来来来，希望大家一起立一个Flag（承诺），认真吸收，最后完成这次训练作业。

扣一句话吧：一定作业！！

截止时间：22日周日晚12:00

好啦，这次分享就到这里，期待未来，再次相见\~\~\~

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI俱乐部周三LIVE](../01-AI认知与基本功/05-AI俱乐部周三LIVE.md)

---

<details>
<summary>原文配图上的文字（49 条，图片本身未随文提供）</summary>
- 「一堂AI落地Live」 「在一堂内部，其实已经在很多场景，用AI能力去提高效率了」
- 「一堂·生成式AI使用段位图」 「GPT多数场景可以替换成其他语言模型」 「一堂·坚持只做必修课」

**生成一张海报用图**

- 「一堂·生成式AI使用段位图」
- 是一个Prompt大赛的相关活动信息页面，涵盖大赛的核心规则与相关示例。页面包含参赛方式说明，参赛者可在指定大语言模型中二选一参与，需提交符合要求的短视频主题或职位主题的Prompt；同时标注了大赛截止时间为10月28日24:00，获奖名单将于11月1日公布。页面还列出了提交要求、评比标准、比赛奖励等内容，奖励为两个主题综合排名前三的参赛者可从十幅书法作品中任选一件，图中还配有相关书法作品及展示服

**实现步骤**

- 「试生成，看效果」
- ChatGPT中模型选择界面。上方有GPT-3.5和GPT-4两个选项，GPT-4被选中。GPT-4介绍为最强大的模型，适合需要创造力和高级推理的任务，仅对Plus用户开放，每3小时有25条消息限制。下方有Default、Advanced Data Analysis、Plugins、DALL-E 3四个选项，其中DALL-E 3被勾选，表明当前使用的是DALL-E 3模型。该图片
- 「讯飞星火SparkDesk」 「主题是华山论剑」 「退出助手」
- 「豆包 - 你的AI朋友」 「创建新对话」 「要升级tinker库，可以使用pip ...」
- 「比拼的华山论剑」
- 「赛博朋克，华山之巅，人物分列画面左右，剑拔弩张对抗」 「豆包AI生成」
- 「华山论剑」 「选定风格，匹配需求，生成图片」 「一步一步调整提示词，匹配需求」
- 「华山论剑」
- 「第二步：选定风格，匹配需求，生成图片」 「生成一张海报用图」 「实现步骤」
- 「华山论剑」 「寻找模板，完成设计」
- 「华山论剑」 「生成一张海报用图」 「决定选择黑白/水墨风格」 「上一步的提示词，加上背景空旷一些，给文字留出空间」 「上一步的提示词，加上比例9:16的要求」
- 「第三步：寻找模板，完成设计」
- 「第0届「华山论剑」 「能力竞赛」

**实际演示**

- 「一堂·生成式AI使用段位图」 「简单聊天」 「生成一张海报用图」
- 「设计一个聊天软件的UI，运行在iOS上」
- 四种不同风格的iOS聊天软件UI设计，由DALL - E 3生成。每种设计对应一个手机界面，包括蓝色、白色、黑色和白色背景的聊天界面，界面中有头像、消息输入框、表情符号等元素。图片下方文字说明可根据需求和喜好选择其中一个或提供反馈，还提示若有其他要求或建议可告知。该图片
- 用于创建iOS聊天界面的SwiftUI代码示例，内容包含SwiftUI的基础结构定义ChatView视图，声明了保存消息文本的状态变量messageText。代码通过VStack布局，在顶部放置包含头像（设置了裁剪为圆形、指定宽高尺寸）和联系人姓名的HStack，还在下方添加了视频相关的图标，该代码是为了实现类似首图展示的iOS聊天界面，属于结合GPT工具生成的相关代码演示内容
- 「100%」 「生成一张海报用图」
- 「一堂·生成式AI使用段位图」 「简单聊天」
- 「一堂课程GONGJIAN计划」 「感谢参与一堂课程GONGJIAN计划」 「共建课程《一堂五步法：企业服务篇》」
- 「一堂课程GONGJIAN特别共建荣誉」 「排名按拼音顺序排列」
- 「感谢参与一堂课程 GONGJIAN计划」 「排名按拼音顺序排列」
- 「一堂课程GONGJIAN计划」 「感谢所有共建者，没有你们的热情参与就没有这门课程的诞生」 「排名按拼音顺序排列」
- 「感谢参与一堂课程GONGJIAN计划」 「共建课程：《科学开会必修课》」
- 「GONGJIAN计划」 「感谢参与一堂课程 GONGJIAN计划」 「感谢所有共建者，没有你们的热情参与就没有这门课程的诞生」 「感谢磨课专家」 「感谢贡献案例」 「感谢共建课程」 「排名按拼音顺序排列」
- 「感谢参与一堂课程GONGJIAN计划」
- 「ssoid」 「微信昵称」 「一堂创业者」
- 「如何快速横排名单」 「排成7列」
- 「遍历（Traversal）」
- 「处理完成，文件已保存」
- 「Excel处理工具」
- 「迭代问题」
- 「一堂创业者」
- 「一堂·生成式AI使用段位图」 「API调用」 「生成一张图片，借助GPT写一个复杂的程序，目标高大上，比例16:9」
- 「AI俱乐部·共建资讯信息」
- 「生成式人工智能：发展演进及产业机遇」 「GGV有话说」
- 「帮我分析一下这篇文章内容」 「生成一张海报用图」 「实际演示」
- 「科技每日推送」
- 「区块链」
- 「生成一张海报用图」
- 「图的描绘」 「自定义标题」 「输入文章」 「背景音乐」 「生成海报」 「测试助理」 「测试助理测试」 「测试结果」
- 名为Rss-DiscordBot的工作流界面，用于实现从RSS到Discord的内容流转。界面呈现了两条并行的自动化流程，每条流程都从RSS源（RSS）或Notion数据库作为起点，经过集成OpenAI（ChatGPT、Whisper、DALL-E）进行内容处理，期间配置了JSON、Router等组件，还加入了多个用于忽略内容的节点（Ignore），最终将处理后的内容同步到Notion或Disco
- AI落地Live分享内容里的任务相关演示图，呈现了一个任务要求及说明：任务是通过链接抓取文章并保存到本地，为实现该任务，给出了5个具体步骤，分别为循环读取列表、找到列表项中包含http链接的内容、访问链接并保存页面内容、调用接口处理页面内容、将结果输出到csv。图片还补充说明，为避免网络访问和接口调用出现故障，每一步的结果都会本地保存，再次运行无需重复访问网络与接口，进一步明确了任务的落地逻辑，搭
- 一个包含用户名称、使用层、网址、文章内容和时间的表格类内容，展示了不同用户分享的相关信息，其中用户包括张国强、lightsilver、城东一君（Lee）、不二幻觉，部分用户的内容涉及美国区Apple ID注册、美国地址生成器等工具使用，还有内容涉及人工智能发展趋势的讨论，时间范围覆盖2023年9月25日至21日，各条目关联的网址均来自mp.veixin.qx.com相关链接。这些内容和AI落地相关
- 是Cursor网站的定价页面。页面左侧是免费版，包括50次慢速GPT - 4使用、200次GPT - 3.5使用、AI驱动代码编辑器、私有数据控制等。中间是Pro版，每月20美元，包含免费版所有内容，500次快速GPT - 4使用、无限慢速GPT - 4使用、无限GPT - 3.5使用。右侧是Business版，每月40美元，包含Pro版所有内容，集中计费、本地模式强制、OpenAI零数据保留等。

</details>
