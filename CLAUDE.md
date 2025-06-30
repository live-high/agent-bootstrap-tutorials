# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an Agent Bootstrap Tutorials repository that teaches users how to rapidly start projects using Claude Code agent collaboration. The repository contains a complete tutorial series demonstrating how to build functional tools from ideas to working products using natural language interaction with Claude Code.

**Available in multiple languages:**
- 🇺🇸 English (Default): `README.md` and files starting with English names  
- 🇨🇳 Chinese: `README_CN.md` and files with Chinese names

## Project Structure

### Tutorial Files

**Chinese Tutorials:**
- `教程1-3分钟快速构建.md` - Demonstrates building a complete CLI tool in 3 minutes
- `教程2-从零构建写作练习体系.md` - Shows complete 0-1 project construction process
- `教程3-工具集成.md` - Agent tool integration and automation workflows
- `教程4-总结和扩展.md` - Methodology summary and extension patterns

**English Tutorials:**
- `Tutorial-1-3-Minute-Quick-Build.md` - 3-minute CLI tool construction
- `Tutorial-2-Building-Writing-System-From-Scratch.md` - Complete system building process
- `Tutorial-3-Agent-Tool-Integration.md` - Agent and tool collaboration workflows
- `Tutorial-4-Methodology-Summary-Extension.md` - Methodology extraction and extension

### Supporting Files

**Chinese Documentation:**
- `基础准备-环境配置指南.md` - Environment setup guide
- `写作练习目录配置教程.md` - Directory structure tutorial
- `练习流程说明.md` - Practice workflow instructions
- `补充-Agent协作的思维过程.md` - Deep dive into agent collaboration thinking

**English Documentation:**
- `Environment-Setup-Guide.md` - Environment configuration guide
- `Practice-Workflow-Guide.md` - Practice workflow instructions
- `Supplement-Agent-Collaboration-Thinking-Process.md` - Agent collaboration thinking deep dive

### Directory Structure
The tutorials create this structure:
```
01-materials/              # Material collection
  ├── thought-fragments/   # Thought fragments
  ├── daily-observations/  # Daily observations  
  └── inspiration-collection/ # Inspiration collection
      └── quick-notes.md   # Quick recording file
02-practice-records/       # Practice records
  └── templates/           # Practice templates
      ├── observation-practice-template.md
      ├── thinking-practice-template.md
      ├── structure-practice-template.md
      └── free-creation-template.md
03-output-results/         # Output results
```

## Core Methodology

### Agent Bootstrap Philosophy
- **Natural Expression**: Describe needs in plain language, let Claude infer technical details
- **Progressive Clarification**: Refine ideas through conversation
- **Rapid Validation**: Small steps, quick feedback loops
- **Self-Bootstrapping**: Use agent-built tools with the agent itself

### Key Principles
- **Minimal Friction**: Reduce decision fatigue with clear guidance
- **Attention-Friendly**: Short sessions (5-15 minutes) for focus-challenged users
- **Structured Templates**: Provide frameworks while preserving creativity
- **Immediate Feedback**: Visible progress and instant validation

## Technology Preferences

Based on tutorial content, the system prefers:
- **Language**: Python for CLI tools and automation
- **Interface**: Command-line over GUI
- **Storage**: Local files in Markdown format
- **Architecture**: Simple, extensible structures

## Common Development Patterns

### CLI Tool Development
- Use argparse for command-line interfaces
- Implement configuration management with JSON files
- Create template-based file generation
- Support both direct execution and wrapper scripts

### File Organization
- Use numbered prefixes (01-, 02-, 03-) for logical ordering
- Employ descriptive Chinese filenames for user-facing content
- Create template directories for reusable structures
- Maintain clear separation between input, process, and output

## Agent Integration Guidelines

When working with this codebase:
- Focus on building tools that the agent itself can use
- Prioritize natural language interfaces over complex configurations
- Create self-documenting code with clear help messages
- Enable rapid prototyping and iteration cycles

## Common Tasks

### Building CLI Tools
- Start with core functionality identification
- Design command structure before implementation
- Include help systems and error handling
- Test with real usage scenarios

### Creating Templates
- Structure templates to guide thinking without limiting creativity
- Include time estimates and completion indicators
- Provide multiple template types for different needs
- Make templates easily discoverable and reusable

## Support and Documentation

The repository includes comprehensive tutorials that demonstrate:
- Complete project construction from scratch
- Natural language interaction patterns
- Agent collaboration best practices
- Tool integration and automation workflows

Users should start with the README.md overview and follow the numbered tutorial sequence for optimal learning experience.