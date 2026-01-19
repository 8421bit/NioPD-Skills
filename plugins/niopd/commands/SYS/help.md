---
description: Displays help information for the NioPD system.
---

# Command: /niopd:SYS:help

This command displays help information about the NioPD system, primarily focusing on the command set.

## Usage
`/niopd:SYS:help`

## Preflight Checklist

1.  **No validation needed:** This command requires no arguments or input validation.

## Instructions

You are Nio, an AI Product Assistant. Your task is to display helpful information about the NioPD system in the user's preferred language.

### Step 1: Check User's Language Preference
- Check the .claude/AGENTS.md file for the user's preferred communication language
- If not found, default to English
- Store the language preference for use in subsequent steps

### Step 2: Acknowledge
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将为您显示NioPD系统的帮助信息。"
    -   If English: "I'll display the help information for the NioPD system."
    -   For other languages, use an appropriate translation

### Step 3: Display Help Information
-   Display the help information to the user in their preferred language:
    -   If Chinese, display the Chinese version of help information
    -   If English, display the English version as shown below
    -   For other languages, use an appropriate translation or default to English

```
📚 NioPD - AI驱动的产品管理工具包
=====================================

🎯 快速开始工作流程
  1. /niopd:SYS:init        - 初始化NioPD工作区
  2. /niopd:BS:new-initiative "<name>" - 创建新的产品项目
  3. /niopd:UR:feedback --for=<initiative> - 分析反馈（自动检测反馈文件）
  4. /niopd:PD:draft --for=<initiative> - 生成PRD草案
  5. /niopd:PM:roadmap              - 更新产品路线图

📄 核心工作流程命令
  /niopd:SYS:init               - 初始化NioPD工作区
  /niopd:BS:new-initiative "<name>" - 开始新的高级产品项目
  /niopd:UR:feedback [--from=<file>] --for=<initiative> - 分析反馈并生成摘要（自动检测反馈文件）
  /niopd:PD:draft --for=<initiative> - 自动生成PRD草案
  /niopd:PM:roadmap              - 生成或更新产品路线图

🔍 商业策略命令
  /niopd:BS:note [content] - 向项目添加笔记
  /niopd:BS:feature-planning - 基于反馈、笔记和历史PRD生成新功能想法
  /niopd:BS:hi - 与Nio开始对话

🔍 市场研究命令
  /niopd:MR:competitor --url=<url> - 分析竞争对手网站
  /niopd:MR:compare [--topic=<market_topic>] - 执行自动化竞争对手比较分析
  /niopd:MR:positioning [--topic=<market_topic>] [--product=<product_name>] - 分析产品的市场定位
  /niopd:MR:pricing [--product=<product_name>] [--market=<market_context>] - 分析竞争性定价策略
  /niopd:MR:trends --topic="..." - 研究并总结某一主题的市场趋势

👥 用户研究命令
  /niopd:UR:feedback [--from=<file>] --for=<initiative> - 分析反馈并生成摘要（自动检测反馈文件）
  /niopd:UR:behavior [--from=<file>] --for=<initiative> - 分析用户行为数据以识别产品改进机会
  /niopd:UR:interview --file=<path> - 总结用户访谈记录
  /niopd:UR:personas --from=<summary> - 从反馈摘要创建用户画像
  /niopd:UR:journey --for=<initiative> - 根据行为数据绘制用户旅程图
  /niopd:UR:satisfaction --for=<initiative> - 分析用户满意度并识别改进领域

📄 产品开发命令
  /niopd:PD:draft             - 生成完整的PRD草案
  /niopd:PD:convert-to-daily-prd - 将指定文档转换为日常迭代PRD格式
  /niopd:PD:stories           - 生成用户故事和验收标准
  /niopd:PD:journey           - 向PRD添加用户旅程图
  /niopd:PD:process           - 向PRD添加业务流程图
  /niopd:PD:roadmap           - 向PRD添加路线图甘特图
  /niopd:PD:jobs-to-be-done   - 应用JTBD框架以识别用户动机
  /niopd:PD:kano-model        - 应用Kano模型以优先化功能
  /niopd:PD:moscow-prioritization - 使用MoSCoW方法优先化需求
  /niopd:PD:rice-prioritization - 使用RICE框架优先化项目
  /niopd:PD:opportunity-solution-tree - 构建机会-解决方案树
  /niopd:UR:personas          - 创建详细的用户画像
  /niopd:MR:compare-products - 分析竞争格局
  /niopd:PD:acceptance-criteria - 生成详细的验收标准
  /niopd:PD:wireframe         - 创建低保真线框图
  /niopd:PM:feature-metrics           - 定义成功指标和KPI
  /niopd:PD:integrate         - 将分析报告集成到PRD
  /niopd:PD:workflow          - 引导完成完整的PRD开发流程

🚀 产品运营命令
  /niopd:PO:faq --for=<prd_name> - 生成全面的FAQ文档

🚀 战略分析命令
  /niopd:ST:swot [--for=<initiative_name>|--for=<product_name>] - 进行全面的SWOT分析
  /niopd:ST:canvas [--for=<initiative_name>|--for=<product_name>] - 生成商业模式画布
  /niopd:ST:portfolio [--organization=<org_name>] - 进行产品组合分析
  /niopd:ST:canvas [--for=<initiative_name>|--for=<product_name>] - 生成商业模式画布

🗺️ 项目管理命令
  /niopd:PM:release [--for=<initiative_name>|--for=<product_name>] - 规划和管理产品发布
  /niopd:PO:stakeholder-update --for=<initiative> [year|month|week|day] - 创建简洁的利益相关者更新报告（可选时间段过滤器）
  /niopd:PM:kpis --for=<initiative> - 获取项目KPI的状态报告
  /niopd:PM:roadmap - 生成或更新产品路线图

🧠 深度思考命令
  /niopd:DT:first-principles [--problem=<problem>] - 应用第一性原理思维
  /niopd:DT:socratic-questioning [--topic=<discussion_topic>] - 使用苏格拉底式提问
  /niopd:DT:five-whys [--problem=<problem_statement>] - 使用五问法

⚙️  系统命令
  /niopd:SYS:help               - 显示此帮助信息
  /niopd:SYS:hi                 - 与Nio开始对话
  /niopd:SYS:init               - 初始化NioPD工作区
  /niopd:SYS:update             - 从GitHub仓库更新NioPD
  /niopd:SYS:flow-check         - 回顾已完成的任务并建议组织改进
  /niopd:SYS:new-command       - 基于已完成的工作创建新命令
  /niopd:SYS:new-agent         - 创建新的专业代理
  /niopd:SYS:new-memory       - 记录个人工作习惯

💡 提示
  • 使用 /niopd:SYS:init 初始化NioPD工作区
  • 使用 /niopd:BS:new-initiative 开始新的产品项目
  • 使用 /niopd:UR:feedback 分析用户反馈（自动检测sources/中的反馈文件）
  • 使用 /niopd:UR:behavior 分析用户行为（自动检测sources/中的行为文件）
  • 使用 /niopd:PD:draft 自动生成PRD
  • 使用 /niopd:PM:roadmap 保持路线图更新
  • 使用 /niopd:BS:feature-planning 生成新功能想法
  • 使用 /niopd:MR:compare 比较竞争对手
  • 使用 /niopd:MR:positioning 分析市场定位
  • 使用 /niopd:ST:swot 进行SWOT分析
  • 使用 /niopd:ST:canvas 创建商业模式画布
  • 使用 /niopd:ST:portfolio 分析产品组合
  • 使用 /niopd:PM:release 规划产品发布
  • 使用 /niopd:SYS:flow-check 检查组织改进建议
  • 查看 README.md 获取完整文档
```

### Step 5: Conclude
-   End with a message in the user's preferred language:
    -   If Chinese: "如需了解更多关于每个命令的详细信息，请参阅 README.md 文件。"
    -   If English: "For more detailed information about each command, please refer to the README.md file."
    -   For other languages, use an appropriate translation
```
