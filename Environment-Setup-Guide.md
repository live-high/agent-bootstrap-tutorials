# Basic Preparation: Environment Configuration Guide

## 🌍 Language / 语言

**🇺🇸 English** (Current) | **[🇨🇳 中文](基础准备-环境配置指南.md)**

---

## 🎯 Guide Overview

**Purpose**: Ensure Claude Code environment is properly configured for smooth tutorial experience  
**Scope**: Environment verification, tool installation, basic configuration  
**Duration**: 5-10 minutes  
**Outcome**: Ready-to-use Claude Code development environment

## 📋 Environment Requirements

### System Requirements
- **Operating System**: macOS, Linux, or Windows with WSL
- **Python**: Version 3.8 or higher
- **Terminal**: Command-line interface access
- **Text Editor**: Any text editor (VS Code, Sublime, Vim, etc.)

### Tool Requirements
- **Claude Code**: Latest version installed and configured
- **Git**: For version control (optional but recommended)
- **Internet Connection**: For Claude Code API access

## 🚀 Step-by-Step Setup

### Step 1: Verify Python Installation

**Check Python Version**:
```bash
python3 --version
```

Expected output:
```
Python 3.8.x or higher
```

**If Python is not installed**:
- **macOS**: Install via Homebrew: `brew install python3`
- **Ubuntu/Debian**: `sudo apt update && sudo apt install python3`
- **Windows**: Download from [python.org](https://python.org) or use WSL

### Step 2: Claude Code Installation

**Check if Claude Code is installed**:
```bash
claude --version
```

**If not installed, follow these steps**:

1. **Install Claude Code** (follow official installation guide)
2. **Verify installation**:
   ```bash
   claude --help
   ```
3. **Configure authentication** (if required)

### Step 3: Create Working Directory

**Create project directory**:
```bash
mkdir agent-bootstrap-practice
cd agent-bootstrap-practice
```

**Verify directory creation**:
```bash
pwd
ls -la
```

### Step 4: Test Claude Code Functionality

**Basic functionality test**:
```bash
# Test Claude Code response
claude "Hello, can you help me test if Claude Code is working?"
```

Expected behavior:
- Claude Code should respond with a helpful message
- No connection errors
- Proper formatting in terminal

### Step 5: Optional Git Setup

**Initialize Git repository** (recommended):
```bash
git init
git config user.name "Your Name"
git config user.email "your.email@example.com"
```

**Create initial .gitignore**:
```bash
cat > .gitignore << EOF
# Python
__pycache__/
*.pyc
*.pyo
*.pyd
.Python
env/
venv/

# OS
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/

# Project specific
.writing_config.json
.writing_progress.json
EOF
```

## 🔍 Environment Verification

### Quick Verification Checklist

Run these commands to verify your setup:

```bash
# 1. Python check
python3 --version

# 2. Claude Code check  
claude --version

# 3. Directory check
pwd

# 4. Write permissions check
touch test_file.txt && rm test_file.txt && echo "Write permissions: OK"

# 5. Claude Code interaction test
claude "Please respond with 'Environment test successful' if you can see this message"
```

### Expected Results

✅ **All checks should pass**:
- Python 3.8+ detected
- Claude Code responds properly
- Working directory accessible
- Write permissions confirmed
- Claude Code interaction working

❌ **If any check fails**:
- Review the specific step above
- Check error messages for guidance
- Ensure all prerequisites are met

## 🛠 Troubleshooting

### Common Issues

**Issue 1: Claude Code not found**
```
Command 'claude' not found
```
**Solution**: Ensure Claude Code is properly installed and in your PATH

**Issue 2: Python version too old**
```
Python 2.x.x detected
```
**Solution**: Install Python 3.8+ and use `python3` command

**Issue 3: Permission denied**
```
Permission denied: cannot create file
```
**Solution**: Check directory permissions or create directory in your home folder

**Issue 4: Claude Code connection issues**
```
Connection failed / API error
```
**Solution**: 
- Check internet connection
- Verify Claude Code authentication
- Check API key configuration

### Getting Help

**If you encounter issues**:
1. **Check error messages** for specific guidance
2. **Review Claude Code documentation** for troubleshooting
3. **Create issue in this repository** with error details
4. **Join community discussion** for peer support

## 📚 Additional Configuration

### Optional Enhancements

**1. Shell Aliases** (for convenience):
```bash
# Add to your ~/.bashrc or ~/.zshrc
alias cc="claude"
alias py="python3"
```

**2. Environment Variables** (if needed):
```bash
export CLAUDE_API_KEY="your-api-key"
export PYTHONPATH="${PYTHONPATH}:$(pwd)"
```

**3. Editor Configuration**:
- Set default editor for markdown files
- Install syntax highlighting for Python
- Configure auto-save for better workflow

### Advanced Setup

**For experienced users**, you may also configure:
- Custom Claude Code prompts
- Project-specific configurations
- Integration with IDEs
- Automated backup systems

## ✅ Setup Complete

After successful setup, you should have:

- [x] Python 3.8+ installed and working
- [x] Claude Code installed and authenticated
- [x] Working directory created with proper permissions
- [x] Basic Git setup (optional)
- [x] All verification tests passing

## 🎉 Ready to Start!

Your environment is now ready for the Agent Bootstrap Tutorials!

**Next Steps**:
1. **Recommended**: [Tutorial 1: 3-Minute Quick Build](Tutorial-1-3-Minute-Quick-Build.md)
2. **Alternative**: [Tutorial 2: Building Writing System from Scratch](Tutorial-2-Building-Writing-System-From-Scratch.md)

**Quick Test**:
Start with a simple interaction:
```bash
claude "I'm ready to start the Agent Bootstrap tutorials. Please confirm you can help me build projects using natural language interaction."
```

---

*Setup Duration: 5-10 minutes*  
*Next: [Start Tutorial 1](Tutorial-1-3-Minute-Quick-Build.md)*  
*Back to: [Tutorial Overview](README_EN.md)*