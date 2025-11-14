# NioPD Configuration Handling Template

This template defines the standard approach for reading and applying user preferences and project settings from configuration files in NioPD commands.

## Configuration Files Overview

NioPD uses two primary configuration files:

1. **.{{IDE_TYPE}}/{{IDE_TYPE}}.md** - User preferences and communication settings
2. **{{IDE_TYPE}}.md** - Project background and context information

## Standard Configuration Handling Process

### Step 1: Check User's Configuration Files
- Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
- Read and parse the {{IDE_TYPE}}.md file for project background and context
- Extract user's preferred communication language from configuration
- Extract other relevant settings (project context, team preferences, etc.)
- Store all configuration settings for use throughout the command execution

### Step 2: Apply Configuration Settings
- Use the user's preferred communication language for all user interactions
- Apply project context and background information to enhance output relevance
- Follow team preferences and work standards defined in the configuration
- Adapt command behavior based on user preferences (e.g., detail level, format preferences)

## Implementation Guidelines

### Language Preference Handling
- Always check for language preference in .{{IDE_TYPE}}/{{IDE_TYPE}}.md
- Default to English if no preference is specified
- Use the preferred language for all user-facing messages, prompts, and output
- Maintain consistency in language throughout the command execution

### Project Context Integration
- Incorporate project background information to tailor output to specific context
- Use project goals and objectives to guide decision-making and recommendations
- Reference team preferences and work standards in suggestions and guidance

### Error Handling with Configuration
- When errors occur, provide messages in the user's preferred language
- Reference configuration settings when suggesting solutions or alternatives
- Respect user preferences even when handling error conditions

## Example Implementation Pattern

```
### Step 1: Check User's Configuration Files
- Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and communication settings
- Read and parse the {{IDE_TYPE}}.md file for project background and context information
- Extract communication language, project context, and other relevant settings
- Acknowledge the user's request in their preferred language:
  - If Chinese: "好的，我将帮您处理[任务名称]。"
  - If English: "On it! I'll help you with [task name]."
  - For other languages, use an appropriate translation based on user's language preference
```

## Best Practices

1. **Always Check Configuration First**: Before performing any task-specific actions, read and apply configuration settings
2. **Respect User Preferences**: Honor all user-defined preferences, especially language and communication style
3. **Provide Fallbacks**: When configuration information is missing, use sensible defaults
4. **Maintain Consistency**: Apply configuration settings consistently throughout the command execution
5. **Update Configuration When Appropriate**: If new preferences are established during command execution, update configuration files accordingly