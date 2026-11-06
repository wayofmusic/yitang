---
title: Coze企业园区信息检索智能体 副本
node_token: Ygxhwi8NxipPlikvQWicxO33nbg
source: https://www.feishu.cn/wiki/Ygxhwi8NxipPlikvQWicxO33nbg
space: 一堂学习
obj_type: docx
synced: 2026-09-26 02:49
course_line: 个人必修
stage: 竞争力
train: 竞争力-AI力
form: 课程逐字稿
audience: 全员
series: 周五内测LIVE
---
# Coze企业园区信息检索智能体 副本

## 智能体链接

## 智能体总体设计

### 截图

### 提示词

```Plain Text
# 角色
你是一个擅长检索信息的专员，能够通过工作流准确检索企业的注册信息，并查找该企业地址所在的产业园区信息。同时能够运用必应搜索获取其他相关信息。

## 技能
### 技能 1: 检索企业注册信息和产业园区信息
1. 当用户仅输入了一个企业名称时，使用工作流执行调研，不要调用插件。
2. 当接收到检索某个企业注册信息的任务时，使用工作流进行精确查找。
3. 确保获取的信息准确完整，包括企业名称、注册时间、经营范围等。

### 技能 2: 运用必应搜索其他信息
1. 当有通过必应搜索其他信息的需求时，准确输入关键词进行搜索。
2. 筛选并整理有价值的信息提供给用户。

## 限制:
- 当用户仅输入了一个企业名称，使用工作流执行调研，不要调用插件。
- 只进行与企业注册信息、产业园区信息及指定的其他信息相关的检索和搜索。
- 所输出的内容必须按照给定的格式进行组织，不能偏离框架要求。
- 确保提供的信息准确可靠。
```

## 工作流

## 大模型_提取企业名称

#### 提示词
```Plain Text
你将以专业的行业产品专家身份，通过检索线上资料，详细回答以下问题：
1. 问题中涉及了什么行业？
2. 属于行业中什么细分赛道，拆分2层细分赛道？
3. 涉及在细分赛道中的什么产品？

请按照以下步骤进行分析：
1. 仔细阅读问题，提取关键信息。
2. 根据关键信息判断涉及的行业。
3. 深入研究该行业，确定2层细分赛道。
4. 明确细分赛道中涉及的产品。

答案要丰富、全面，请严格按照以下格式输出你的答案：

## 行业
[具体行业名称]

## 赛道

1. 第一层细分赛道：[具体细分赛道名称]
2. 第二层细分赛道：[具体细分赛道名称]

## 产品
[具体产品名称]
```

## 插件_水滴信用

## 代码_企业信息表格格式输出

```JavaScript
async function main({ params }: Args): Promise<Output> {
    const { business_scope, capital, company_name, company_status, company_type, credit_no, industry, authority, province, establish_date, legal_person, company_address } = params.company_data.data;
    const output = `| 企业信息 | |\n`
    + '|---|---|\n'
    + `| 企业名称 | ${company_name.trim()} |\n`
    + `| 注册地址 | ${company_address.trim()} |\n`
    + `| 法人代表 | ${legal_person.trim()} |\n`
    + `| 存续状态 | ${company_status.trim()} |\n`
    + `| 企业类型 | ${company_type.trim()} |\n`
    + `| 所属行业 | ${industry.trim()} |\n`
    + `| 统一信用代码 | ${credit_no.trim()} |\n`
    + `| 所在省份 | ${province.trim()} |\n`
    + `| 发证机构 | ${authority.trim()} |\n`
    + `| 注册日期 | ${establish_date.trim()} |\n`
    + `| 注册资本 | ${capital.trim()} |\n`
    + `| 经营范围 | ${business_scope.trim().replace('|',' ').replace('\n',' ').replace('\r',' ')} |\n`

    return {output};
}
```

## 插件_高德地图

## 代码_园区信息表格格式输出

这是企业园区信息检索智能体的代码模块界面，标题为“代码_园区信息表格格式输出”，功能是编写代码处理输入变量生成返回值。界面分为三个核心区域，上方是输入区，包含两个变量：“map_data”对应变量值“周边园区 - pol_list”，“target_data”对应变量值“查询地址 - data”；中间是代码编辑区，显示了基于lodash的JavaScript代码框架，核心为main函数，用于处理输入的两个变量，筛选匹配的园区并提取园区名称，目前代码中存在部分未补全的逻辑代码；下方是输出区，输出变量名为“output”，变量类型为“str. String”，还设有异常处理的对应区域。

```JavaScript
import _ from 'lodash'

async function main({ params }: Args): Promise<Output> {
    const { map_data, target_data } = params;
    let output = ''
    if (map_data && target_data && map_data!= null && target_data != null && map_data.length > 0 && target_data.length > 0) {
        const filterMapData = map_data.filter(item => item.name!== '');
        const customData = filterMapData.map(({city_name, district_name, address, name, location}) => ({
            name,
            city_name,
            district_name,
            address,
            distance: Math.round(getDistanceBetweenCoordinates(target_data[0].location, location) * 1000)
        })).sort((a, b) => a.distance - b.distance)

        const {city_name, district_name, address, name, distance} = customData[0];

        output += `| 产业园区 | |\n`
        + '| --- | --- |\n'
        + `| 园区名称 | ${name.trim()} |\n`
        + `| 城市 | ${city_name.trim()} |\n`
        // + `| 镇 | ${target_data[0].township.trim()} |\n`
        + `| 区 | ${target_data[0].district.trim()} |\n`
        + `| 地址 | ${address.trim()} |\n`
        + `| 距离目标 | ${distance} 米 |\n`

    }
    else {
        output += '未搜索到园区信息'
    }

    return {output};
}

function toRadians(degrees) {
    return degrees * (Math.PI / 180);
}

function calculateDistance(lat1, lon1, lat2, lon2) {
    var R = 6371; // 地球半径，单位为公里
    var dLat = toRadians(lat2 - lat1);
    var dLon = toRadians(lon2 - lon1);
    var rlat1 = toRadians(lat1);
    var rlat2 = toRadians(lat2);

    var a = Math.sin(dLat / 2) * Math.sin(dLat / 2) +
            Math.sin(dLon / 2) * Math.sin(dLon / 2) * Math.cos(rlat1) * Math.cos(rlat2);
    var c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1 - a));
    var distance = R * c;
    return distance;
}

function parseCoordinates(coordString) {
    const [lat, lon] = coordString.split(',').map(Number);
    return { lat, lon };
}

function getDistanceBetweenCoordinates(coordString1, coordString2) {
    const { lat: lat1, lon: lon1 } = parseCoordinates(coordString1);
    const { lat: lat2, lon: lon2 } = parseCoordinates(coordString2);
    return calculateDistance(lat1, lon1, lat2, lon2);
}
```

## 结束

---
> [!info]- 🧭 导航
> ⬆️ 上级：[直播Live一堂分享：AI俱乐部年度开放麦](56-直播Live一堂分享：AI俱乐部年度开放麦.md)

---

<details>
<summary>原文配图上的文字（19 条，图片本身未随文提供）</summary>

**截图**

- 「company_park.xlsx」 「搜索企业所在的产业园」 「生成反馈」 「智能体链接」

**工作流**

- 「大模型_提取企业名称」 「企业信息查询」 「代码_企业信息表格格式输出」 「查询地址」 「周边园区检索」 「代码_园区信息表格格式输出」

**大模型_提取企业名称**

- 「大模型_提取企业名称」 「str. input」 「str. company_name」 「豆包·工具调用」 「未配置技能」
- 「大模型_提取企业名称」 「包-工具调用」 「input」 「会话历史」 「系统提示词」 「用户提示词」

**插件_水滴信用**

- 「创建插件」 「水滴信用」
- 「企业信息查询」 「company_name」 「{} data」 「str.log_id」 「str.msg」 「NO code」 「插件_水滴信用」
- 「企业信息查询」 「获取公司名称、联系人公司详细信息」 「批处理」 「company_name」 「大模型_提取企业名称 - company_name」 「data Object」 「查看示例」

**代码_企业信息表格格式输出**

- 「代码_企业信息表格格式输出」
- 「企业信息查询 - data」

**插件_高德地图**

- 「添加插件」 「创建插件」 「最受欢迎」 「仅展示官方插件」 「仅展示端插件」 「没找到想要的插件？」 「提交反馈」 「高德地图」
- 「poi_to_geocode」 「city」 「address」 「查看示例」
- 「查询地址」 「str.address」 「str.city」 「NO code」 「\[{} data\]」 「str.log_id」 「str.msg」 「代码_园区信息表格格式输出」
- 「查询地址」 「address」 「city」
- 「search_around」 「参数 查看示例」 「添加1」
- 「周边园区检索」
- 「周边园区检索」 「查询地址 - formatted_address」

**代码_园区信息表格格式输出**

- 「代码_园区信息表格格式输出」

**结束**

- Coze企业园区信息检索智能体工作流中的“结束”环节。该环节的输出有str. output1、str. output2、str. location，输出类型为返回文本。此环节位于工作流流程的最后，是智能体工作流的终止点，用于汇总并输出园区相关信息，为后续处理或展示园区信息做好准备
- 「返回变量」 「返回文本」 「代码_企业信息表格格式输出」 「查询地址-location」 「\[output1\]」 「流式输出」

</details>
