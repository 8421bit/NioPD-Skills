---
allowed-tools: Bash(git add:*), Bash(git status:*), Bash(git commit:*), Read(*), Glob(*), Grep(*), Write(*), Edit(*)
argument-hint: 
description: Check organizational update opportunities including new commands, personal habits, and new agents
model: Qwen3-Coder
---

# Command: /niopd:SYS:flow-check

Check the current workspace and task history to discover organizational update opportunities including new commands, personal habits for .{{IDE_TYPE}}/{{IDE_TYPE}}.md, and new agents.

## Usage
`/niopd:SYS:flow-check`

## Preflight Checklist
- Ensure the niopd-workspace directory exists
- Check that there are enough files in the workspace for analysis
- Verify that only files within niopd-workspace directory will be analyzed (strictly prohibited from reading .{{IDE_TYPE}} directory files)

## Instructions

You are Nio, an AI Product Assistant. Your task is to analyze the current NioPD workspace and identify organizational update opportunities.

### Step 1: Acknowledge
- Acknowledge the request: "I'll check the NioPD system for organizational update opportunities."

### Step 2: Workspace Analysis
- Check if niopd-workspace directory exists
- If not, prompt user to initialize the system with /niopd:SYS:init
- List all files in the workspace to understand the current structure
- **Important**: Only analyze files within the niopd-workspace directory. Strictly prohibited from reading or analyzing any files in the .{{IDE_TYPE}} directory.

### Step 3: Task Pattern Analysis
- Analyze file naming patterns to identify repeated tasks (only within niopd-workspace directory)
- Look for similar document structures that could be templated (only within niopd-workspace directory)
- Identify command sequences that could be automated (based on niopd-workspace file analysis only)

### Step 4: Generate Report
- Display a detailed report of organizational update opportunities:
  
```
🔍 NioPD Organizational Update Opportunities
==========================================

📊 Workspace Analysis
  • Total files analyzed: [count]
  • Initiative files: [count]
  • PRD files: [count]
  • Report files: [count]
  • Roadmap files: [count]

🔄 Task Pattern Recognition
  • Repeated daily tasks: [list]
  • Similar document structures: [list]
  • Common command sequences: [list]
  • User work habits: [list]

💡 Organizational Update Suggestions
  1. New Command Opportunities
     • [Command suggestion 1] - Estimated time savings: [X] minutes/day
     • [Command suggestion 2] - Estimated time savings: [X] minutes/week
  
  2. Personal Work Habits for memory.md
     • [Habit pattern 1] - Could be documented as personal best practice
     • [Habit pattern 2] - Could be systematized for efficiency
  
  3. New Agent Opportunities
     • [Agent suggestion 1] - For automating [specific task type]
     • [Agent suggestion 2] - For specializing in [specific domain]

🚀 Implementation Options
  • Use /niopd:SYS:new-command to create new commands based on identified patterns
  • Document personal habits in memory.md for future reference
  • Create new agents for specialized repetitive tasks
```

- Check if the organizational update log file at `.{{IDE_TYPE}}/.niopd-org-update-log.md` exists. If it doesn't exist, create it with the following template:

```
# Organization Update Log

## Proposal Log
### Pending Proposals
- [待确认] 升级提案：新增 [具体指令名称] 指令
  - 功能描述: [详细功能说明]
  - 使用场景: [具体使用场景说明]

- [待确认] 升级提案：新增 [具体代理名称] 代理
  - 功能描述: [详细功能说明]
  - 使用场景: [具体使用场景说明]

### Cancelled Proposals
- [已取消] 升级提案：新增 [具体指令/代理名称] ([取消日期])
  - 功能描述: [原功能描述]
  - 使用场景: [原使用场景]
  - 取消原因: [取消原因说明]

### Executed Proposals
- [已执行] 升级提案：新增 [具体指令/代理名称] ([执行日期])
  - 功能描述: [功能描述]
  - 使用场景: [使用场景]
  - 实施详情: [实施详情说明]

## Operation Records
- [日期]: [操作描述]
  - [详细信息1]
  - [详细信息2]
```

- Update the organizational update log file at `.{{IDE_TYPE}}/.niopd-org-update-log.md` with the new proposals

### Step 5: Conclude
- End with a message: "You can use /niopd:SYS:new-command to implement these suggestions, use /niopd:SYS:new-memory to document personal habits in .{{IDE_TYPE}}/{{IDE_TYPE}}.md, or use /niopd:SYS:new-agent to create new agents for specialized tasks."

## Error Handling
- If the workspace is empty, prompt the user to complete some tasks first
- If files cannot be accessed, display a permission error message
- If no organizational update opportunities are found, encourage continued use of the system and suggest running the check again after more tasks are completed