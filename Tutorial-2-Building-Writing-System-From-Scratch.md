# Building Writing Practice System from Scratch - Claude Code Rapid Project Startup Hands-on Tutorial

## 🌍 Language / 语言

**🇺🇸 English** (Current) | **[🇨🇳 中文](教程2-从零构建写作练习体系.md)**

---

## 🎯 Tutorial Overview

**Target Audience**: Practitioners who want to learn rapid project startup with agents  
**Core Value**: Master the 0-to-1 complete project construction method through real cases  
**Learning Outcome**: Establish complete writing practice system, prepare for subsequent 3-minute CLI tool build  
**Estimated Duration**: 20-25 minutes

## 📋 Preparation

> 💡 **Important Note**: Before starting this tutorial, please complete [Basic Preparation: Environment Configuration Guide](Environment-Setup-Guide.md) to ensure Claude Code environment is properly configured.

### Final Result Preview
After completing this tutorial, you will have:
```
writing-practice-project/
├── 01-materials/
│   ├── thought-fragments/
│   ├── daily-observations/
│   └── inspiration-collection/
├── 02-practice-records/
│   └── templates/
├── 03-output-results/
├── Practice-Workflow-Guide.md
└── various practice template files
```

## Part 1: Building Writing Practice System from Scratch

### Chapter Goal
Through natural dialogue with Claude Code, design and establish a complete writing practice system from zero.

### Background Description
This is the core part of the entire tutorial. We will demonstrate how to express vague ideas in natural language and let Claude Code help us clarify requirements, design structure, and establish processes. This process perfectly demonstrates the essence of agent collaborative development.

### Actual Operation Demonstration

**⏱️ Stage 1: Requirements Clarification (5 minutes)**

**[00:00] Natural Conversation Initiation**

Open Claude Code and input:
```text
I want to establish a writing practice system to improve my writing ability, but I don't know where to start. Can you help me design it? I hope it's suitable for people with easily distracted attention.
```

**Claude's Guidance (Expected Response)**:
```text
I'd be happy to help you design a writing practice system! Let me first understand some specific situations:

1. What are your writing practice goals? (e.g., improving description skills, logical thinking, creative expression, etc.)
2. How much time can you roughly invest in practice each day?
3. You mentioned "easily distracted attention" - what specific situations does this refer to?
4. Have you tried other writing practice methods before?

Based on this information, I can design a personalized practice system for you.
```

**[02:00] Respond to Claude's Questions**

Based on Claude's guidance, answer:
```text
1. I hope to improve observation skills, logical thinking, and expression abilities, ultimately able to write articles with depth
2. I can roughly invest 10-15 minutes per day, not too long
3. My attention is easily distracted, it's hard to persist in long-term activities
4. I tried journaling before, but always gave up after writing for a few days

I hope this system can help me establish sustainable writing habits.
```

**Claude's Design Suggestions (Expected Response)**:
```text
Based on your situation, I suggest designing an attention-friendly writing practice system:

Core Principles:
- Micro-session design: 5-15 minutes each time, fits attention characteristics
- Low-friction startup: Reduce decision fatigue with clear guidance
- Structured templates: Reduce "don't know what to write" confusion
- Instant positive feedback: Can see progress, maintain motivation

Practice Type Suggestions:
1. Observation Practice: Improve detail perception ability
2. Thinking Practice: Exercise logic and viewpoint expression
3. Structure Practice: Train information organization ability
4. Free Creation: Comprehensive use of various skills

Would you like me to help you design specific file structure and practice processes?
```

**⏱️ Stage 2: Structure Design (3 minutes)**

**[05:00] Discuss File Structure**

Continue dialogue:
```text
This design approach is great! Please help me design specific file structure. I hope to be able to:
1. Conveniently record daily thoughts and inspirations
2. Systematically conduct different types of practice
3. Organize and review previous content
4. Finally output complete articles
```

**Claude's Structure Suggestions (Expected Response)**:
```text
Based on your needs, I suggest this directory structure:

```
writing-practice-project/
├── 01-materials/          # Daily ideas and inspiration collection
│   ├── thought-fragments/   # Random thoughts recorded anytime
│   ├── daily-observations/  # Life observation records
│   └── inspiration-collection/ # Creative ideas and inspirations
├── 02-practice-records/     # Organized practice
│   ├── 2024-12/            # Monthly organization
│   └── templates/          # Practice templates
├── 03-output-results/       # Complete articles
└── practice-workflow-guide.md # Usage guide
```

This structure has several advantages:
1. Material library lets you record ideas anytime, lowering startup threshold
2. Practice records are organized but without pressure
3. Output results give you clear production goals
4. Monthly folders facilitate review and progress statistics

How do you think about this structure? Need any adjustments?
```

**[07:00] Confirm and Optimize Structure**

Reply:
```text
The structure is excellent! I especially like the material library design, so I can record ideas anytime. Can you help me create these directories? Also, what exactly are the practice templates you mentioned?
```

**⏱️ Stage 3: Create Directory Structure (2 minutes)**

**[08:00] Claude Creates Directories**

Claude will use tools to create directory structure:
```text
I'll help you create this directory structure.
```

Then Claude will use corresponding commands to create folders and basic files.

**⏱️ Stage 4: Design Practice Process (5 minutes)**

**[10:00] Discuss Practice Arrangement**

Continue dialogue:
```text
The directory structure is perfect! Can you now help me design specific practice processes? I hope to have clear practice guidance every day, but without feeling pressure.
```

**Claude's Process Design (Expected Response)**:
```text
I'll design a cyclic practice process for you that's both regular and varied:

Weekly Practice Arrangement:
- Mon/Wed/Fri: Observation Practice (improve perception)
- Tue/Thu: Thinking Practice (exercise logic)
- Saturday: Structure Practice (organize summary)
- Sunday: Free Creation (comprehensive application)

Characteristics of each practice:
1. Observation Practice (5-10 minutes)
   - Choose any object around you for deep observation
   - Record visual, tactile, emotional responses
   - Train detail perception ability

2. Thinking Practice (10-15 minutes)
   - Choose a topic for deep thinking
   - Form viewpoints and find supporting evidence
   - Train logical thinking ability

3. Structure Practice (10-15 minutes)
   - Review this week's materials and practice
   - Try to reorganize and framework
   - Train information organization ability

4. Free Creation (15 minutes)
   - Free writing based on this week's materials
   - Comprehensive use of various skills
   - Produce complete short essays

Benefits of this arrangement:
- Clear daily tasks, no need to struggle with what to do
- Short time, fits attention characteristics
- Progressive from observation to creation
- Regular but not monotonous

Would you like me to design specific templates for each practice?
```

**⏱️ Stage 5: Create Practice Templates (3 minutes)**

**[15:00] Request Template Creation**

Reply:
```text
This arrangement is excellent! Please help me create templates for each practice. I hope templates can guide my thinking but won't limit creativity.
```

**Claude Creates Templates**

Claude will create specific template files, for example:

**Observation Practice Template**:
```markdown
# Observation Practice - {Date}

**Theme:** {Specific observation object}
**Goal:** Improve detail perception and description skills

## 🔍 Observation Object
Choose any object in front of you, observe carefully for 30 seconds

**Object:** 

## 📝 Detailed Description (3-5 minutes)
**Visual Details:**

**Texture/Touch:**

**Emotional Response:**

## 💭 Deep Thinking (2 minutes)
What inspiration does this object give you?

## ⭐ Today's Gains
- New Discovery:
- Insight:
- Tomorrow's Expectation:

---
*Completion Time:* ___minutes | *Mood:* ⭐⭐⭐⭐⭐
```

**⏱️ Stage 6: Verification and Optimization (2 minutes)**

**[18:00] Test Run**

```text
The templates look great! I want to try the observation practice now to see if the process flows smoothly.
```

Do a quick observation practice based on the template, verify:
- Whether template guidance is clear
- Whether time arrangement is reasonable
- Whether it's easy to get started

**[20:00] Final Optimization**

Based on trial experience, discuss with Claude and adjust:
- Template improvement suggestions
- Process optimization directions
- Usage considerations

### Checkpoint Items
- [ ] Complete directory structure created
- [ ] Four practice templates generated
- [ ] Practice process documentation complete
- [ ] Completed one template test
- [ ] Confirmed entire system is usable

### Common Questions

**Q: What if Claude's suggestions don't fit my needs?**
A: Express your thoughts directly. For example: "I think 15 minutes is too long, can you design a 5-10 minute version?"

**Q: What if created folder permissions have issues?**
A: Ensure you have write permissions in the project root directory, or manually create directory structure.

**Q: Template too complex, don't know how to fill?**
A: Tell Claude: "This template is too complex for me, can you design a simpler version?"

---

## Part 2: Project Memory Configuration

### Chapter Goal
Let Claude Code deeply understand your project background and personal characteristics, preparing for subsequent development.

### Background Description
By configuring CLAUDE.md file, let Claude Code understand project design philosophy, directory structure, user characteristics, etc., so that in subsequent development, Claude can provide more precise help.

### Specific Operations

**Step 1: Create CLAUDE.md**

Tell Claude:
```text
Now we've established a complete writing practice system. Please help me create a CLAUDE.md file so future Claude instances can understand this project's background and design philosophy.
```

**Step 2: Describe Project Characteristics**

Guide Claude to include in CLAUDE.md:
```text
Please explain in CLAUDE.md:
1. This is a writing practice system designed specifically for users with easily distracted attention
2. Project directory structure and each folder's purpose
3. Practice process design philosophy (micro-sessions, low-friction startup, etc.)
4. Template usage methods
5. My skill preferences (like Python, used to command-line operations)
```

**Expected Generated CLAUDE.md Example**:
```markdown
# CLAUDE.md

This project is a writing practice system designed specifically for users with easily distracted attention.

## Project Overview

This is a writing practice system aimed at helping users with easily distracted attention establish sustainable writing habits.

## Core Design Principles

- **Micro-session Design**: Each practice 5-15 minutes, fits attention characteristics
- **Low-friction Startup**: Clear templates and guidance, reduce decision fatigue
- **Structured Guidance**: Use templates to reduce "don't know what to write" confusion
- **Instant Feedback**: Progress visualization, maintain practice motivation

## Directory Structure

### 01-materials/
- **thought-fragments/**: Record random thoughts and thinking
- **daily-observations/**: Life observations and insights
- **inspiration-collection/**: Creative ideas and writing inspirations

### 02-practice-records/
- Monthly organized practice records
- **templates/**: Structured templates for four practice types

### 03-output-results/
- Storage for complete articles and works

## Practice Types

1. **Observation Practice**: Improve detail perception ability
2. **Thinking Practice**: Exercise logical thinking and viewpoint expression
3. **Structure Practice**: Train information organization and framework building
4. **Free Creation**: Comprehensive use of various writing skills

## User Characteristics

- Easily distracted attention, needs short-term efficient practice methods
- Prefers Python programming and command-line operations
- Needs clear guidance and structured processes
- Suitable for short-term, high-frequency practice modes

## Technical Preferences

- **Language**: Python (most familiar)
- **Interface**: Command-line over GUI
- **Storage**: Local files over cloud services
- **Format**: Markdown documents
```

### Checkpoint Items
- [ ] CLAUDE.md file created
- [ ] Contains complete project background description
- [ ] Explains attention-friendly design features
- [ ] Records user skill preferences
- [ ] Describes directory structure and usage methods

---

## 🎉 Tutorial Completion Check

After completing this tutorial, you should have:

### File Structure Check
```
writing-practice-project/
├── 01-materials/
│   ├── thought-fragments/
│   ├── daily-observations/
│   └── inspiration-collection/
├── 02-practice-records/
│   └── templates/
│       ├── observation-practice-template.md
│       ├── thinking-practice-template.md
│       ├── structure-practice-template.md
│       └── free-creation-template.md
├── 03-output-results/
├── CLAUDE.md
└── Practice-Workflow-Guide.md
```

### Function Verification
- [ ] Successfully completed one observation practice
- [ ] Template filling flows smoothly with clear guidance
- [ ] Claude Code can understand project background
- [ ] Entire practice system logic is complete

### Next Step Preparation
Now you have a complete writing practice system foundation. Next you can:

1. **Experience CLI Tool Rapid Build**: [Tutorial 1: 3-Minute Quick Build](Tutorial-1-3-Minute-Quick-Build.md) - Add automation functions to this system
2. **Learn Agent Integration**: [Tutorial 3: Tool Integration](Tutorial-3-Agent-Tool-Integration.md) - Implement Agent self-bootstrapping workflow
3. **Deep Understanding of Collaboration Principles**: [Supplement: Agent Collaboration Thinking Process](Supplement-Agent-Collaboration-Thinking-Process.md) - Understand underlying thinking methods

---

*Tutorial Duration: ~20 minutes*  
*Recommended Next Step: [3-Minute Quick Build CLI Tool](Tutorial-1-3-Minute-Quick-Build.md)*