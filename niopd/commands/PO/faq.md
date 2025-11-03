---
argument-hint: [--for=<prd_name>]
description: Generates a FAQ document for a PRD. Auto-detects PRD name from current directory if not specified.
---

# Command: /niopd:PO:faq

This command generates a comprehensive FAQ document for a specific Product Requirements Document (PRD).

## Theoretical Foundation

### Origin and Development
FAQs (Frequently Asked Questions) originated from **NASA's space program documentation** (1960s) and became standard in **technical writing** and **customer support** (1990s-2000s). Modern FAQ design incorporates **information architecture** principles and **self-service support** methodologies.

### Core Principle
FAQs are **proactive knowledge transfer** tools that anticipate user questions and provide clear answers, reducing support burden while improving user experience. Effective FAQs are **user-centered**, **discoverable**, and **actionable**.

### FAQ Best Practices

**Structure**:
- Categorize by user journey or topic
- Most common questions first
- Progressive disclosure (simple → complex)
- Search-optimized (keywords)

**Content**:
- Clear, concise answers
- Step-by-step instructions
- Visual aids (screenshots, videos)
- Links to detailed docs

**Maintenance**:
- Update based on support tickets
- Analytics-driven improvements
- Regular accuracy reviews
- User feedback integration

### FAQ in Product Operations

FAQs serve multiple audiences:
- **Users**: Self-service answers
- **Support**: Deflect common tickets
- **Sales**: Objection handling
- **Internal**: Knowledge sharing

## Usage
`/niopd:PO:faq [--for=<prd_name>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the PRD/initiative name.

**Examples:**
```bash
# Explicit PRD name
/niopd:PO:faq --for=dark-mode-feature

# Auto-detect from current directory
cd dark-mode-feature
/niopd:PO:faq  # Uses "dark-mode-feature"
```

## Preflight Checklist

1.  **Determine PRD Name:**
    -   If `--for=<prd_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected PRD name from current directory: `<directory_name>`"
    -   Store the determined name as `<prd_name>` for use in all subsequent steps

2.  **Validate PRD:**
    -   Check that the PRD file following the naming convention `[YYYYMMDD]-<initiative_slug>-prd-v[version].md` exists in `niopd-workspace/docs/`. If not, inform the user.
    -   Identify the latest version of the PRD file based on the date and version number in the filename.

## Instructions

You are a specialized AI expert in creating comprehensive FAQ documents from PRD documents. Your goal is to identify key features, functionalities, and potential user questions to generate a well-structured FAQ with clear, concise answers.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request: "I'll help you create a comprehensive FAQ document for the **<prd_name>** PRD."
-   Read the LATEST version of the PRD file from `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-prd-v[version].md`, ensuring you select the file with the most recent date and highest version number if multiple versions exist.
-   Ensure that you are reading the most recent version by checking the date and version in the filename.

### Step 2: PRD Analysis & Validation
- Read and analyze the provided PRD file.
- Verify that the file exists and is readable.
- Identify key sections: features, functionalities, user personas, technical requirements.
- Note any missing or incomplete information.

### Step 3: Persona & Audience Analysis
- Extract user personas defined in the PRD.
- If personas are not well-defined, identify target audiences based on context.
- Analyze each persona's likely questions and information needs.
- Consider different user types (new users, power users, administrators, etc.).

### Step 4: Question Category Planning
- Plan the FAQ structure by question categories:
  - General/Introduction questions
  - Feature-specific questions
  - Technical questions
  - Usage questions
  - Troubleshooting questions
- Ensure categories are logical and intuitive for users.
- Consider the user journey and when they might have each type of question.

### Step 5: Key Question Identification
- Identify the most important questions users are likely to have.
- Extract questions from PRD features and functionalities.
- Consider common support questions and pain points.
- Identify questions about timelines, availability, and requirements.

### Step 6: Answer Development
- For each identified question, develop clear, concise answers.
- Ensure answers are accurate and based on PRD information.
- Provide sufficient detail without being overly verbose.
- Include step-by-step instructions where appropriate.

### Step 7: Technical Detail Inclusion
- Include technical specifications and requirements.
- Provide system requirements and compatibility information.
- Address security and compliance considerations.
- Note any technical limitations or constraints.

### Step 8: Usage Guidance Development
- Create step-by-step usage instructions.
- Provide getting started guidance for new users.
- Include customization and configuration options.
- Address common usage scenarios and workflows.

### Step 9: Troubleshooting & Error Handling
- Identify common errors and issues users might encounter.
- Provide troubleshooting steps and solutions.
- Include general guidance for error resolution.
- Note when to contact support or seek additional help.

### Step 10: Resource & Support Information
- Compile links to relevant documentation and resources.
- Include training materials and video tutorials.
- Provide support contact information and channels.
- Note community forums and feedback mechanisms.

### Step 11: Content Organization & Structure
- Organize all content according to the FAQ template structure.
- Ensure questions are grouped logically within categories.
- Verify that answers are clear and easy to scan.
- Include appropriate formatting and visual elements.

### Step 12: Review & Quality Check
- Review all questions and answers for accuracy and completeness.
- Ensure all PRD features and functionalities are covered.
- Verify that answers are helpful and actionable.
- Check for any missing information or gaps.

### Step 13: FAQ Document Generation
Produce a markdown FAQ document with the following structure:

---
# Frequently Asked Questions: [Feature/Initiative Name]

## Overview
*A brief introduction to the feature or initiative and what this FAQ covers*

## Table of Contents
- [General Questions](#general-questions)
- [Feature Questions](#feature-questions)
- [Technical Questions](#technical-questions)
- [Usage Questions](#usage-questions)
- [Troubleshooting](#troubleshooting)
- [Additional Resources](#additional-resources)

## General Questions
### Q: What is [feature/initiative name]?
A detailed explanation of the feature or initiative, its purpose, and benefits.

### Q: Who is this feature for?
Information about the target audience, personas, or user groups.

### Q: When will this feature be available?
Details about the timeline, rollout schedule, or availability.

## Feature Questions
### Q: What can I do with this feature?
A description of the main functionalities and capabilities.

### Q: How does this feature work?
An explanation of the feature mechanics, workflow, or processes.

### Q: What are the key benefits?
A list of the main advantages and value propositions.

## Technical Questions
### Q: What are the system requirements?
Details about hardware, software, or platform requirements.

### Q: Is this feature secure?
Information about security measures, compliance, and data protection.

### Q: How does this integrate with other systems?
Details about integrations, APIs, or compatibility with existing tools.

## Usage Questions
### Q: How do I get started?
Step-by-step instructions for initial setup or onboarding.

### Q: How do I use [specific functionality]?
Detailed instructions for using key features or workflows.

### Q: Can I customize this feature?
Information about customization options, settings, or configurations.

## Troubleshooting
### Q: What should I do if I encounter an error?
General troubleshooting guidance and support contacts.

### Q: Why is this feature not working as expected?
Common issues and their solutions.

### Q: Where can I get help?
Information about support channels, documentation, or training resources.

## Additional Resources
### Documentation
- [User Guide](link)
- [Technical Documentation](link)
- [API Reference](link)

### Training & Support
- [Video Tutorials](link)
- [Webinars](link)
- [Support Portal](link)

### Feedback & Contact
- [Feedback Form](link)
- [Contact Support](link)
- [Community Forum](link)

---
*FAQ generated on [Date]*
*Based on PRD: [PRD File Name]*

### Step 9: Save the FAQ Document
- Generate a filename for the FAQ document following the NioPD naming convention: `[YYYYMMDD]-[prd_name_slug]-faq-v[version].md`.
- Save the FAQ document to: `niopd-workspace/docs/[filename]`

### Step 10: Confirm and Conclude
- Confirm the action is complete: "✅ I've generated a comprehensive FAQ document for **<prd_name>**."
- Provide the path to the file: "You can view it here: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-faq-v[version].md`"

## Error Handling
- **Incomplete PRD:** If the PRD lacks sufficient detail for FAQ creation, explain what information is missing and suggest requesting clarification.
- **Ambiguous Requirements:** If PRD requirements are unclear, note the ambiguity and provide interpretations with suggestions for clarification.
- **Missing Personas:** If user personas are not well-defined in the PRD, create generic personas based on context or suggest defining them.
- **Conflicting Information:** If the PRD contains contradictory information, highlight the conflicts and suggest resolution approaches.
- **Technical Limitations:** If certain questions cannot be answered due to technical constraints, clearly state the limitations.

In all error cases, provide clear explanations, suggest alternatives or additional information needed, and emphasize that partial FAQ creation can still provide value.