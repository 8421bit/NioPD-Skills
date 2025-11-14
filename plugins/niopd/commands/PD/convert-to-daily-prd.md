---
description: Convert specified document to daily iteration requirements format using the daily PRD template. Supports multiple input methods including file path, file name, attachment, text content, and URL.
---

# Command: /niopd:PD:convert-to-daily-prd

This command converts an existing document into a well-structured daily iteration PRD following the standard template.

## Theoretical Foundation

### Origin and Development
The Daily PRD format is a streamlined product requirements document designed for **existing products' iterative development**. Unlike comprehensive PRDs for new products, daily PRDs focus on incremental improvements and feature iterations with a practical, execution-oriented structure.

### Core Principle
Daily PRDs emphasize **efficiency and clarity** for ongoing product development:
- **Background-driven**: Clear business context and product status
- **Goal-oriented**: Specific iteration objectives with measurable outcomes
- **Solution-focused**: Business processes, user flows, and detailed requirements
- **Launch-ready**: Phased rollout strategy (pre-release, internal beta, external beta)

### Daily PRD vs. Standard PRD

**Standard PRD (New Features)**:
- Comprehensive market analysis
- Strategic positioning
- Long-term vision
- Extensive user research

**Daily PRD (Iterations)**:
- Business context and current status
- Specific iteration goals
- Practical solutions and workflows
- Immediate launch plans

### Essential Daily PRD Components

**1. Background (Pre-business context)**:
- Current business challenges
- Product domain goals
- Historical iterations and system shortcomings

**2. Objectives**:
- Overall product domain goals review
- Specific iteration goals with timeline/scope/value

**3. Solution**:
- Business Process (Mermaid diagrams required)
- User Flow (optional, with interface prototypes)
- Requirements List (table format with priorities)

**4. Detailed Requirements**:
- Feature descriptions with business logic
- Input items and output items
- Interaction demos (optional)

**5. Data Requirements (Optional)**:
- Data tracking requirements
- Business reporting needs

**6. Product Risk Management (Optional)**:
- Security, Privacy, Compliance
- Financial, Customer Satisfaction

**7. Launch Plan**:
- Pre-release phase
- Internal Beta phase
- External Beta phase

**8. Appendix (Optional)**:
- Concept explanations
- Technical implementation details
- Data transformation processes

### When to Use Daily PRD
- Ongoing product iterations
- Feature enhancements
- Bug fixes with requirements
- Small to medium scope changes
- Regular sprint planning
- Existing product improvements

### Related Templates
- **Standard PRD Template**: For new features and products
- **MRD Template**: For market requirements
- **User Story Template**: For agile development

### Complementary NioPD Commands
- `/niopd:PD:draft-prd` - Create standard PRD
- `/niopd:PD:draft-mrd` - Market requirements document
- `/niopd:PD:stories` - Generate user stories
- `/niopd:PD:process` - Add business process diagrams

## Usage
`/niopd:PD:convert-to-daily-prd`

**Input Methods Supported**:
```bash
# Method 1: File path
/niopd:PD:convert-to-daily-prd
# Then provide: docs/feature-spec.md

# Method 2: File name
/niopd:PD:convert-to-daily-prd
# Then provide: feature-spec.md

# Method 3: Upload attachment
/niopd:PD:convert-to-daily-prd
# Then upload: [file.docx]

# Method 4: Paste content
/niopd:PD:convert-to-daily-prd
# Then paste document content directly

# Method 5: URL
/niopd:PD:convert-to-daily-prd
# Then provide: https://docs.google.com/document/d/...
```

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the conversion process

2.  **Check Input:**
    -   User can provide content in multiple ways:
        -   **File path**: Path to an existing document in workspace (e.g., `niopd-workspace/docs/feature-spec.md`)
        -   **File name**: Document identifier that can be found in workspace
        -   **Attachment**: User-uploaded file or document
        -   **Text content**: Direct paste of document content in the conversation
        -   **URL**: Link to an external document (if accessible)
    -   If no input provided, ask: "Please provide the content you'd like to convert to daily PRD format. You can:
        -   Share a file path (e.g., `docs/feature-spec.md`)
        -   Upload an attachment
        -   Paste the document content directly
        -   Provide a document name to search for"

3.  **Validate and Read Content:**
    -   **If file path provided:**
        -   Verify the file exists in the workspace
        -   If not found, inform user: "❌ Error: File not found at the specified path. Please check and try again."
    -   **If file name provided:**
        -   Search for the file in workspace directories
        -   If multiple matches found, ask user to choose
        -   If no match found, inform user: "❌ Error: No file found with that name. Please provide the full path or upload the file."
    -   **If attachment provided:**
        -   Read the attachment content
        -   Support formats: .md, .txt, .docx (convert to text)
        -   If format not supported, inform user: "❌ Error: Unsupported file format. Please provide .md, .txt, or .docx files."
    -   **If text content provided:**
        -   Use the pasted content directly
        -   Validate it's not empty
    -   **If URL provided:**
        -   Fetch the content from URL
        -   If inaccessible, inform user: "❌ Error: Cannot access the URL. Please check permissions or provide content another way."

4.  **Load Template:**
    -   Read the template file: `../../templates/prd-daily-template.md`
    -   Parse the template structure to understand the required sections

## Instructions

You are Nio, a friendly and efficient AI product assistant specialized in document format conversion. Your goal is to help the user convert an existing document into a well-structured daily iteration PRD following the standard template.

**Core Principle:** Preserve the original document's information while restructuring it to match the daily PRD template. Focus on format conversion rather than content creation. The final converted document should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Read Source Document
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the user's request in their preferred language:
    -   If Chinese: "好的，我将把您的内容转换为日常PRD格式。"
    -   If English: "On it! I'll convert your content to the daily PRD format."
    -   For other languages, use an appropriate translation based on user's language preference
-   **Determine input type and read content:**
    -   **If file path provided**: Read the file from workspace
    -   **If file name provided**: Search workspace, confirm if multiple matches, then read
    -   **If attachment provided**: Read attachment content, handle different formats (.md, .txt, .docx)
    -   **If text content pasted**: Use the provided text directly
    -   **If URL provided**: Fetch content from URL
-   Analyze the current content structure and identify key information
-   Inform user about the source in their preferred language: "I've received your [file/attachment/content]. Let me analyze it and convert to daily PRD format."

### Step 2: Load and Parse Template Structure
-   Read the template file from: `../../templates/prd-daily-template.md`
-   Identify the template structure:
    -   Section 1: Background (Pre-business context, Overall goal, Product current status)
    -   Section 2: Objectives (Overall goals review, This iteration's goals)
    -   Section 3: Solution (Business Process, User Flow, Requirements List)
    -   Section 4: Detailed Requirements Description (Feature-by-feature breakdown)
    -   Section 5: Data Requirements (Optional)
    -   Section 6: Product Risk Management (Optional)
    -   Section 7: Launch Plan
    -   Section 8: Appendix (Optional)

### Step 3: Analyze Source Document Content
-   Extract information from the source document:
    -   **Background information**: Business context, problems, current status
    -   **Goals and objectives**: What the document aims to achieve
    -   **Features and requirements**: List of functionalities described
    -   **Business processes**: Any workflows or processes mentioned
    -   **Technical details**: Implementation specifics
    -   **Launch/rollout information**: Timeline, phases, targets
-   Identify which template sections have corresponding content in the source
-   Note any missing critical information

### Step 4: Content Mapping and Transformation
-   **Map source content to template structure:**
    -   Background → Section 1 (Background)
    -   Goals/Objectives → Section 2 (Objectives)
    -   Features/Solutions → Section 3 (Solution) + Section 4 (Detailed Requirements)
    -   Data/Analytics → Section 5 (Data Requirements)
    -   Risks/Compliance → Section 6 (Product Risk Management)
    -   Rollout/Timeline → Section 7 (Launch Plan)
    -   Additional info → Section 8 (Appendix)

-   **Transform content format:**
    -   Convert free-form text into structured sections
    -   Create requirements table with: Product Module | Requirement Name | Description | Priority
    -   Generate business process diagrams using Mermaid syntax if processes are described
    -   Break down features into detailed requirement descriptions (4.1, 4.2, etc.)
    -   Add Input Items and Output Items for each feature

### Step 5: Generate Business Process Diagrams
-   If business processes or workflows are mentioned in the source:
    -   Ask user: "I found workflow information. What type of diagram would you prefer? (flowchart/swimlane/sequence diagram)"
    -   Wait for user's choice
    -   Generate appropriate Mermaid diagram based on the workflow description
    -   Ensure the diagram is clear, readable, and follows Mermaid syntax

### Step 6: Fill Template Gaps
-   For required sections with insufficient source content:
    -   **Background**: If missing, ask user: "Could you provide some background context for this requirement?"
    -   **Objectives**: If unclear, ask: "What are the specific goals and success criteria for this iteration?"
    -   **Requirements List**: If not in table format, transform into structured table
    -   **Launch Plan**: If missing, ask: "What's the planned rollout strategy? (pre-release/internal beta/external beta)"

-   For optional sections:
    -   Only include if relevant content exists in source document
    -   Don't ask for optional information unless it's clearly relevant

### Step 7: Structure and Format the Daily PRD
-   Create the new document following the template structure exactly:
    -   Use the same heading hierarchy (## for main sections, ### for subsections)
    -   Maintain the template's formatting conventions
    -   Include all required sections
    -   Only include optional sections if relevant content exists
    -   **Use the user's preferred language for all content generation**

-   **Ensure proper formatting:**
    -   Requirements table with clear columns
    -   Mermaid diagrams with proper syntax
    -   Bulleted lists for enumerated items
    -   Clear feature breakdown in Section 4 (4.1, 4.2, etc.)

### Step 8: Generate Output File
-   Determine output file name:
    -   Use pattern: `[YYYYMMDD]-<product-identifier>-daily-prd-v[version].md`
    -   Extract product identifier from:
        -   Original file name (if file path provided)
        -   Document content (product name mentioned)
        -   User's project context
    -   Suggest name to user: "I'll save this as `20251113-[product-name]-daily-prd-v0.md`. Is this okay?"
    -   Wait for user confirmation or alternative name

-   **Create the converted document content**:
    -   Combine all structured sections into a complete document
    -   Ensure proper Markdown formatting
    -   Validate all Mermaid diagrams syntax
    -   Verify requirements table structure

-   **Save the converted document to `niopd-workspace/docs/`**:
    -   Use the Write tool to create the file:
        -   File path: `niopd-workspace/docs/[determined_filename]`
        -   Content: The complete converted document content
    -   If file already exists, inform user and suggest incrementing version number

-   **If source was a file**: Preserve original document (don't overwrite)
-   **If source was attachment/text**: Create new file with suggested name
-   Inform user of the saved location

### Step 9: Review and Present Results
-   Inform user in their preferred language: "✅ Document converted successfully!"
-   Show summary in their preferred language:
    -   **If from file**: "Original document: [source file path]"
    -   **If from attachment**: "Source: [attachment name]"
    -   **If from text**: "Source: Pasted content"
    -   **If from URL**: "Source: [URL]"
    -   "Converted daily PRD: niopd-workspace/docs/[new file name]"
    -   "Template sections populated: [list of included sections]"
    -   "Sections requiring your input: [list any gaps]"

-   **Confirm the completion** in their preferred language: "✅ I've converted your document to the daily PRD format."
-   **Provide the path** in their preferred language: "You can review and edit it at: `niopd-workspace/docs/[new_file_name]`"
-   **Suggest next steps** in their preferred language: "Consider using /niopd:PD:draft-prd to create a full PRD, /niopd:PD:stories to generate detailed user stories, or /niopd:PD:process to document business processes."

-   Highlight key transformations in their preferred language:
    -   "✅ Created requirements table with [N] items"
    -   "✅ Generated [diagram type] for business process" (if applicable)
    -   "✅ Structured [N] detailed feature descriptions"

-   If any gaps exist, provide actionable guidance in their preferred language:
    -   "📝 Next steps: Please review and fill in the following sections:"
    -   List specific sections that need user input
    -   Suggest: "You can use `/niopd:PD:draft-prd` to enhance any section further."

### Step 10: Offer Next Actions
-   Suggest follow-up actions:
    -   "Would you like me to enhance any specific section?"
    -   "Do you want to add more detailed feature descriptions?"
    -   "Should I generate additional diagrams for the user flow?"
-   Wait for user's decision

## Error Handling
-   **If file path invalid**: Inform user in their preferred language and suggest checking path or using alternative input method
-   **If file not found**: Offer to search workspace or ask user to upload/paste content, using their preferred language
-   **If attachment format unsupported**: List supported formats (.md, .txt, .docx) and ask for compatible format in user's preferred language
-   **If URL inaccessible**: Suggest checking permissions or providing content through alternative method, using their preferred language
-   **If pasted content is empty**: Ask user to provide valid content in their preferred language
-   **If multiple files found with same name**: Present options and ask user to choose, using their preferred language
-   If template file is missing, inform user in their preferred language: "❌ Template file not found. Please ensure `templates/prd-daily-template.md` exists."
-   If content mapping is ambiguous, ask user for clarification rather than making assumptions, using their preferred language
-   If Mermaid diagram generation fails, provide the diagram as code block and suggest manual review, using their preferred language
-   **If file save fails**: Provide clear error messages and troubleshooting suggestions (e.g., check directory permissions, disk space) in user's preferred language
-   **If file already exists**: Inform user and suggest incrementing version number or choosing a different name, using their preferred language
-   If user cancels at any step, preserve all work and inform them how to resume, using their preferred language

## Quality Checks
Before finalizing the converted document, verify:
-   ✅ All required sections are present (1-4, 7)
-   ✅ Section numbering matches template exactly
-   ✅ Requirements table is properly formatted
-   ✅ Mermaid diagrams use correct syntax
-   ✅ Feature descriptions include Description/Input/Output
-   ✅ Document follows naming convention
-   ✅ File is saved in correct directory (docs/)
-   ✅ Original document is preserved
-   ✅ Converted document file is successfully created
-   ✅ File content matches converted content exactly

## Template Reference
The template structure to follow is located at: `../../templates/prd-daily-template.md`

Key template sections (in order):
1. Background (Pre-business context, Overall goal, Product current status)
2. Objectives (Overall goals review, This iteration's goals)
3. Solution (Business Process, User Flow, Requirements List)
4. Detailed Requirements Description (4.1, 4.2, ... feature breakdown)
5. Data Requirements (Optional)
6. Product Risk Management (Optional - 6.1-6.5 subsections)
7. Launch Plan (Pre-release, Internal Beta, External Beta)
8. Appendix (Optional)

## Notes
-   This command focuses on **format conversion** rather than content creation
-   **Multiple input methods supported**:
    -   File paths (workspace files)
    -   File names (auto-search in workspace)
    -   Attachments (uploaded files)
    -   Text content (direct paste)
    -   URLs (if accessible)
-   Preserve the original document's information while restructuring
-   Don't invent information - ask user when content is missing
-   Prioritize clarity and completeness over brevity
-   The daily PRD template is designed for existing product iterations, not new features
-   **Supported file formats**: .md (Markdown), .txt (Plain text), .docx (Word document)
-   **File naming convention**: `[YYYYMMDD]-<product-identifier>-daily-prd-v[version].md`
-   **Output directory**: `niopd-workspace/docs/`
-   **Version management**: Increment version number if file already exists
-   **Language preference**: The converted document will be generated in the user's preferred language as specified in the project configuration or inferred from their communication
