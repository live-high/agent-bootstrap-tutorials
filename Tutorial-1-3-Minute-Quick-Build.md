# Tutorial 1: 3-Minute CLI Tool Build - An Impressive Agent Bootstrap Opening

## 🌍 Language / 语言

**🇺🇸 English** (Current) | **[🇨🇳 中文](教程1-3分钟快速构建.md)**

---

## 🚀 Impressive Opening

**Question**: How long does it take to build a complete CLI tool from scratch using Agent?

**Answer**: **3 minutes**

This isn't a theoretical estimate, but a real construction record. Next, you'll see the complete 3-minute build process, specific operations at each time point, and the final feature-rich CLI tool.

## 📋 Pre-Build Preparation

> 💡 **Important Note**: Before starting this tutorial, please complete [Basic Preparation: Environment Configuration Guide](Environment-Setup-Guide.md) to ensure Claude Code environment is properly configured.

### Technical Requirements
- ✅ Python 3 environment
- ✅ Basic command-line operation skills

### ⚡ Basic Environment Check

Before starting the 3-minute build, confirm your working directory contains the following structure:
```
current-directory/
├── 01-materials/
│   ├── thought-fragments/
│   ├── daily-observations/
│   └── inspiration-collection/
│       └── quick-notes.md
├── 02-practice-records/
│   ├── templates/ (contains 4 practice template files)
│   └── 2024-12/
├── 03-output-results/
└── Practice-Workflow-Guide.md
```

> 💡 **Tip**: If your directory doesn't have these files, check [Writing Practice Directory Configuration Tutorial.md](Writing-Practice-Directory-Setup-Tutorial.md) to learn how to quickly set up.

### Expected Final Results

After completing the 3-minute build, you will have:
- 📄 **writing_cli.py** - Complete CLI tool (~600 lines of code)
- 🔧 **Quick Script** - Shell script for simplified calls
- ⚡ **15+ Core Functions** - Covering practice, material management, output creation
- 🎯 **Ready to Use** - Can start using immediately

## ⚡ 3-Minute Build Process

> **Important Note**: The following timeline is based on real build logs, each time point represents actual operations.

### 🕐 Minute 1 (00:00-01:00): Requirements Analysis & Architecture Design

**[00:00] 📝 Initiate Build Request**

Input in Claude Code:
```text
I need a command-line tool to manage writing practice workflows, including practice recording, material collection, output creation, and other functions. Can you help me build it?
```

> **💡 Note**: This uses natural expression, directly stating functional requirements.

**[00:04] 🔍 Agent Begins Analysis**

Agent's response:
```text
I'll help you create a writing practice management CLI tool. Let me first understand your specific needs, then design a feature-complete command-line tool.
```

Agent automatically analyzes requirements, identifying these core functions:
- Practice management (start practice, view status)
- Material collection (thought fragments, daily observations, inspiration collection)
- Content search and organization
- Output creation management

**[00:22] 🏗️ Design CLI Command Architecture**

Agent proposes command structure design:
```bash
# Basic practice commands
writing init              # Initialize environment
writing practice          # Start practice
writing status            # View status
writing random            # Random prompts

# Material management commands
writing fragment "content"    # Add thought fragment
writing observation "content" # Add observation record
writing inspiration "content" # Add inspiration
writing note "content"        # Quick note

# View and search
writing list [type]        # List materials
writing search "keyword"   # Search content

# Output creation
writing create "title"     # Create work
writing works             # List works
writing export "keyword" "title" # Export materials to work
```

**[00:38] 📋 Auto-Generate Development Plan**

Agent creates development plan:
```text
1. ✅ Analyze writing tool requirements and functional architecture
2. 🔄 Design CLI tool structure and command system  
3. ⏳ Implement core classes and configuration management
4. ⏳ Implement practice workflow management functions
5. ⏳ Implement material collection and management functions
6. ⏳ Implement search and output creation functions
7. ⏳ Complete command-line interface and error handling
```

**[01:00] ✅ Minute 1 Summary**
- Requirements understanding complete
- Complete architecture design confirmed
- 15+ function commands planned

---

### 🕑 Minute 2 (01:00-02:00): Core Code Implementation

**[01:00] 💻 Start Writing Python Core Classes**

Agent begins generating core code framework:
```python
#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Writing Practice Command Line Tool
Friendly design adapted for effort-saving needs
"""

import os
import sys
import json
import datetime
import argparse
import random
from pathlib import Path

class WritingPracticeCLI:
    def __init__(self):
        self.project_root = Path(__file__).parent
        self.config_file = self.project_root / '.writing_config.json'
        self.progress_file = self.project_root / '.writing_progress.json'
        self.load_config()
```

**[01:15] ⚙️ Implement Configuration and Progress Management**

```python
def load_config(self):
    """Load configuration"""
    default_config = {
        "user_name": "",
        "start_date": str(datetime.date.today()),
        "practice_time": "09:00",
        "reminder_enabled": True,
        "auto_backup": True
    }
    
    if self.config_file.exists():
        with open(self.config_file, 'r', encoding='utf-8') as f:
            self.config = {**default_config, **json.load(f)}
    else:
        self.config = default_config

def load_progress(self):
    """Load progress data"""
    if self.progress_file.exists():
        with open(self.progress_file, 'r', encoding='utf-8') as f:
            return json.load(f)
    return {"total_days": 0, "streak": 0, "last_practice": "", "skills": {}}
```

**[01:30] 📅 Implement Practice Types and Template System**

```python
def get_today_practice_type(self):
    """Determine practice type based on day of week"""
    weekday = datetime.date.today().weekday()
    practice_types = {
        0: ("Observation Practice", "Monday: Daily Object Observation"),
        1: ("Thinking Practice", "Tuesday: Facial Expression Capture"), 
        2: ("Observation Practice", "Wednesday: Sound Texture Description"),
        3: ("Thinking Practice", "Thursday: Emotional State Analysis"),
        4: ("Observation Practice", "Friday: Viewpoint Collision Debate"),
        5: ("Structure Practice", "Saturday: Experience Reconstruction Narrative"),
        6: ("Free Creation", "Sunday: Free Creative Flight")
    }
    return practice_types[weekday]

def create_practice_file(self, file_path, practice_type, theme, date_str):
    """Create structured practice file"""
    templates = {
        "Observation Practice": f"""# Observation Practice - {date_str}

**Theme:** {theme}
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
""",
        # Other templates...
    }
    
    content = templates.get(practice_type, templates["Observation Practice"])
    with open(file_path, 'w', encoding='utf-8') as f:
        f.write(content)
```

**[02:00] ✅ Minute 2 Summary**
- Core classes and configuration system complete
- Practice management and template system implemented
- Basic file operation functions complete

---

### 🕒 Minute 3 (02:00-03:00): Function Enhancement & Command Interface

**[02:00] 📝 Implement Material Management Functions**

```python
def add_fragment(self, content, tag=None):
    """Add thought fragment"""
    timestamp = datetime.datetime.now().strftime("%Y-%m-%d %H:%M")
    fragment_dir = self.project_root / "01-materials" / "thought-fragments"
    fragment_dir.mkdir(parents=True, exist_ok=True)
    
    filename = f"{datetime.date.today().strftime('%Y-%m-%d')}-fragments.md"
    file_path = fragment_dir / filename
    
    tag_str = f" #{tag}" if tag else ""
    entry = f"## {timestamp}{tag_str}\n{content}\n\n"
    
    with open(file_path, 'a', encoding='utf-8') as f:
        f.write(entry)
    
    print(f"💭 Thought fragment added to: {file_path}")

def search_materials(self, keyword):
    """Search material library"""
    results = []
    materials_dir = self.project_root / "01-materials"
    
    for subdir in materials_dir.iterdir():
        if subdir.is_dir():
            for file_path in subdir.glob("*.md"):
                try:
                    with open(file_path, 'r', encoding='utf-8') as f:
                        content = f.read()
                        if keyword.lower() in content.lower():
                            results.append((str(file_path), subdir.name))
                except:
                    continue
    
    if results:
        print(f"🔍 Found {len(results)} related results:")
        for file_path, category in results:
            print(f"  📁 {category}: {Path(file_path).name}")
    else:
        print(f"❌ No content found containing '{keyword}'")
    
    return results
```

**[02:15] 🎯 Implement Output Creation Management**

```python
def create_work(self, title, work_type="Article"):
    """Create new work"""
    works_dir = self.project_root / "03-output-results"
    works_dir.mkdir(parents=True, exist_ok=True)
    
    timestamp = datetime.date.today().strftime("%Y-%m-%d")
    filename = f"{timestamp}-{title}.md"
    file_path = works_dir / filename
    
    template = f"""# {title}

**Type:** {work_type}
**Created:** {timestamp}
**Status:** Draft

## 📝 Content

## 📚 Reference Materials

## 💭 Writing Ideas

## ✏️ Revision Log

---
*Created on {timestamp}*
"""
    
    with open(file_path, 'w', encoding='utf-8') as f:
        f.write(template)
    
    # Open with system default editor
    os.system(f"open '{file_path}'")
    print(f"📄 Work created: {file_path}")

def export_materials_to_work(self, keyword, work_title):
    """Export materials to new work based on keyword"""
    # First search related materials
    results = self.search_materials(keyword)
    
    if not results:
        print(f"❌ No related materials found, cannot create work")
        return
    
    # Create work file
    works_dir = self.project_root / "03-output-results"
    works_dir.mkdir(parents=True, exist_ok=True)
    
    timestamp = datetime.date.today().strftime("%Y-%m-%d")
    filename = f"{timestamp}-{work_title}.md"
    file_path = works_dir / filename
    
    # Collect material content
    materials_content = []
    for file_path_str, category in results:
        try:
            with open(file_path_str, 'r', encoding='utf-8') as f:
                content = f.read()
                materials_content.append(f"### {category} - {Path(file_path_str).name}\n{content}\n")
        except:
            continue
    
    # Generate work file
    work_content = f"""# {work_title}

**Based on keyword:** {keyword}
**Created:** {timestamp}
**Material sources:** {len(results)} files

## 📝 Main Content

## 📚 Related Materials

{''.join(materials_content)}

---
*Auto-generated based on keyword "{keyword}" on {timestamp}*
"""
    
    with open(file_path, 'w', encoding='utf-8') as f:
        f.write(work_content)
    
    os.system(f"open '{file_path}'")
    print(f"🎉 Work '{work_title}' created with {len(results)} related materials")
```

**[02:45] 🔧 Complete Command Line Interface**

```python
def main():
    cli = WritingPracticeCLI()
    
    parser = argparse.ArgumentParser(description='Writing Practice Command Line Tool')
    subparsers = parser.add_subparsers(dest='command', help='Available commands')
    
    # Basic commands
    subparsers.add_parser('init', help='Initialize practice environment')
    subparsers.add_parser('practice', help='Start today\'s practice')
    subparsers.add_parser('status', help='Check practice status')
    subparsers.add_parser('random', help='Random practice prompt')
    
    # Material management
    fragment_parser = subparsers.add_parser('fragment', help='Add thought fragment')
    fragment_parser.add_argument('content', help='Content')
    fragment_parser.add_argument('--tag', help='Tag')
    
    note_parser = subparsers.add_parser('note', help='Quick note')
    note_parser.add_argument('content', help='Content')
    
    # Search and export
    search_parser = subparsers.add_parser('search', help='Search materials')
    search_parser.add_argument('keyword', help='Keyword')
    
    export_parser = subparsers.add_parser('export', help='Export materials to work')
    export_parser.add_argument('keyword', help='Keyword')
    export_parser.add_argument('title', help='Work title')
    
    args = parser.parse_args()
    
    # Command dispatch
    try:
        if args.command == 'init':
            cli.init_environment()
        elif args.command == 'practice':
            cli.start_practice()
        elif args.command == 'fragment':
            cli.add_fragment(args.content, args.tag)
        elif args.command == 'search':
            cli.search_materials(args.keyword)
        elif args.command == 'export':
            cli.export_materials_to_work(args.keyword, args.title)
        # ... other commands
        else:
            parser.print_help()
    except KeyboardInterrupt:
        print("\n👋 Goodbye! Remember to keep practicing~")
    except Exception as e:
        print(f"❌ Error occurred: {e}")
```

**[02:58] 🔧 Create Quick Script and Agent Integration**

```bash
#!/bin/bash
# w quick script
python3 writing_cli.py "$@"
```

**Agent Project Memory Configuration (`/init` command)**:
Agent automatically executes equivalent to `/init` operation, creating CLAUDE.md file:

```markdown
# Project Memory Configuration

This is a writing practice management system with complete CLI tools.

## Tool Functions
- Practice management: init, practice, status, random
- Material collection: fragment, observation, inspiration, note  
- Search organization: list, search
- Output creation: create, works, export

## Usage
All operations executed through `./w [command]`, Agent can actively call these tools to help users manage writing workflows.
```

**[03:00] ✅ Build Complete!**

---

## 🎯 Result Verification

### Complete Function Demonstration

**Basic practice commands**:
```bash
./w init                    # Initialize environment
./w practice               # Start today's practice
./w status                 # Check practice status
./w random                 # Get random prompts
```

**Material management commands**:
```bash
./w fragment "thought content" --tag "tag"     # Add thought fragment
./w observation "observation content" --location "place" # Add observation record
./w inspiration "inspiration content" --source "source"   # Add inspiration
./w note "quick idea"                        # Quick note
```

**Search and organization**:
```bash
./w list                   # List all materials
./w list thought-fragments # List specific type
./w search "keyword"       # Search content
```

**Output creation**:
```bash
./w create "article title"                    # Create new work
./w works                              # List all works
./w export "keyword" "Thoughts on XX"        # Export materials to work
```

**Expected output example**:
```text
$ ./w status
👋 Hello! Today is a good day for writing practice

📅 Today's recommendation: Thinking Practice
🎯 Practice theme: Tuesday: Facial Expression Capture
⏰ Suggested time: 10-15 minutes

📊 Practice statistics:
🔥 Consecutive practice: 5 days
📈 Total practice days: 23 days
💪 Skill distribution: Observation Practice(8) Thinking Practice(7) Structure Practice(5) Free Creation(3)

💡 Today's status: Ready to start practice
```

### Code Statistics
- **Total lines**: ~600 lines
- **Core classes**: 1 main class + 15+ methods
- **Command support**: 15+ main commands
- **Function modules**: Configuration management, practice workflow, material collection, search organization, output creation

### Function Completeness Check
- [x] ✅ Initialization function (`./w init`)
- [x] ✅ Practice management (`./w practice`, `./w status`, `./w random`)
- [x] ✅ Material collection (`./w fragment`, `./w observation`, `./w inspiration`, `./w note`)
- [x] ✅ Content search (`./w list`, `./w search`)
- [x] ✅ Output creation (`./w create`, `./w works`, `./w export`)
- [x] ✅ Progress tracking (consecutive days, skill statistics)
- [x] ✅ Template-based file generation
- [x] ✅ Agent integration support (auto project memory)

---

## 🔍 Why Can Such a Complex Tool Be Built in 3 Minutes?

### 1. Agent Natural Language Understanding Capability
- Directly infer 15+ specific functions from vague requirements
- Automatically design reasonable command structure and parameters
- Intelligently generate user interface that fits usage habits

### 2. Pattern Recognition and Code Generation
- Recognize common patterns of CLI tools
- Automatically choose appropriate Python libraries and architecture
- Generate structured, extensible code framework

### 3. Complete Function Inference
- Infer complete function ecosystem from "writing practice management"
- Automatically supplement functions users might need but didn't explicitly mention
- Design complete data flow from input to output

### 4. Effort-Saving Design Philosophy
- Minimum commands for maximum functionality
- Smart defaults and automated processing
- Instant feedback and friendly error handling

---

## 🚀 Start Using Immediately

### Environment Verification

If your directory lacks basic files, check [Writing Practice Directory Configuration Tutorial.md](Writing-Practice-Directory-Setup-Tutorial.md) to learn how to quickly set up a complete environment.

### First Use
```bash
# Set executable permissions
chmod +x w

# Initialize environment
./w init

# Check today's suggestions
./w status

# Start first practice
./w practice
```

### Agent Self-Bootstrapping Verification

Now the most exciting part: **Let Agent use the just-built tool**!

Tell Agent:
```text
We just completed the CLI tool build. Please help me use this tool to record this construction experience.
```

Agent should automatically use:
```bash
./w note "Completed 3-minute CLI tool build, functions richer than expected, includes complete material management and output creation functions. Agent's natural language understanding capability is amazing."
```

This is the perfect demonstration of **Agent Self-Bootstrapping**!

---

## 🎊 Summary

**Build Statistics**:
- Build time: 3 minutes
- Function count: 15+ commands
- Code lines: ~600 lines
- Ready to use: ✅

**Core Value**:
- Experienced complete power of Agent collaborative development
- Obtained feature-rich practical tool
- Established foundation for Agent self-bootstrapping workflow
- Mastered minimal Bootstrap methodology

**Next Steps**:
Enter [Tutorial 2: Building Writing Practice System from Scratch](Tutorial-2-Building-Writing-System-From-Scratch.md) to experience the complete 0-to-1 construction process.

**Extended Reading**:
[Supplement: Agent Collaboration Thinking Process](Supplement-Agent-Collaboration-Thinking-Process.md) - Deep understanding of design thinking behind rapid construction.

---

*Build time: 3 minutes*  
*Next tutorial: [Deep Understanding of System Design](Tutorial-2-Deep-Understanding-System-Design.md)*  
*Complete series: [Agent Bootstrap Tutorials](README_EN.md)*