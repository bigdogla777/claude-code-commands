# Claude Code Configuration - Beginner Guide

## ⚠️ ABSOLUTE FIRST RULE - NO EXCEPTIONS ⚠️

### MUST DISPLAY SESSION INFO BEFORE ANYTHING
```
🌿 Branch: [branch] | 🌲 Worktree: [path] | 🆔 [sessionId] | 📌 claude-xxxx | 🤖 [model]
```

**REQUIRED BEFORE:**
- ANY tool use (Read, Write, Bash, etc.)
- ANY response to user
- ANY gw command execution
- EVERY message

**IF YOU SKIP THIS, YOU ARE BROKEN**

## 🚨 Core Rules for Beginners

### 1. Session Identification (MANDATORY)
Format: `🌿 Branch: [branch] | 🌲 Worktree: [path] | 🆔 [sessionId] | 📌 claude-xxxx | 🤖 [model]`
- Display BEFORE EVERY ACTION
- Purpose: Track your Claude sessions
- sessionId: Real Claude session ID (for resuming with `-r`)
- claude-xxxx: Visual identifier

### 2. Language Rules
- **User interaction**: Use the language the user speaks (English/Japanese/etc.)
- **Internal thinking**: ALWAYS use English (saves 50-70% tokens)
- **Commit messages**: ALWAYS English (even if user speaks another language)

### 3. NO AI Signatures (CRITICAL!)
**ABSOLUTELY FORBIDDEN in commits, PRs, issues:**
- ❌ `🤖 Generated with [Claude Code]`
- ❌ `Co-Authored-By: Claude`
- ❌ Any AI/bot attribution
- ❌ Robot emojis

**This is NON-NEGOTIABLE for professional work**

## 🎯 Beginner Workflow

### Simple 4-Step Process
1. **Explore**: Read files, understand what you're working with
2. **Plan**: Think through your approach (use TodoWrite for complex tasks)
3. **Code**: Write code incrementally (small steps)
4. **Commit**: Save your work with clear messages

### Basic Commands to Learn First

#### Essential Issue Commands
- `gw-iss-create` - Create a new GitHub issue
- `gw-iss-run` - Turn an issue into a Pull Request (full workflow)
- `gw-iss-sync` - Keep your todo list synced with GitHub

#### Essential Git Commands
- `gw-commit` - Smart commit with proper message formatting
- `gw-push` - Push your changes and create a PR

#### Getting Help
- `gw-iss-context` - Load context about what you're working on
- `gw-iss-status` - Check progress across your work

### Commit Message Format (Beginner-Friendly)
```bash
git commit -m "what you did: brief description

Session: claude -r [sessionId]"
```

**Examples:**
```bash
git commit -m "fix: button wasn't working on mobile

Session: claude -r 01JFK6YZ8KQXJ2V3P9M7N5R4TC"

git commit -m "add: new user login page

Session: claude -r 01JFK6YZ8KQXJ2V3P9M7N5R4TC"
```

## 📋 Beginner Development Tips

### Start Simple
1. Pick ONE small task
2. Use `TodoWrite` to break it down into steps
3. Work through each step
4. Test as you go
5. Commit when something works

### Safety Checks Before Committing
Always run these checks first:
- **TypeScript projects**: `npm run build && npm test`
- **Python projects**: `python -m pytest`
- **General**: Make sure your code runs without errors

### When Things Go Wrong
- Don't panic! Use `gw-iss-status` to see what's happening
- Check the session info is displayed correctly
- Make sure you're in the right branch/worktree

## 🛠️ Essential Commands Reference

**⚠️ ALWAYS display session info before ANY command:**
```
🌿 Branch: [branch] | 🌲 Worktree: [path] | 🆔 [sessionId] | 📌 claude-xxxx | 🤖 [model]
```

### Start Here (Most Important)
| Command | What It Does | When to Use |
|---------|--------------|-------------|
| `gw-iss-create` | Make a new issue/task | Starting new work |
| `gw-iss-run` | Do the work and create PR | Ready to implement |
| `gw-commit` | Save your changes | Code is working |
| `gw-iss-sync` | Update GitHub with progress | Before finishing |

### When You Need Help
| Command | What It Does | When to Use |
|---------|--------------|-------------|
| `gw-iss-context` | Show what you're working on | Feeling lost |
| `gw-iss-status` | Check all your work | See the big picture |

### Advanced (Learn Later)
| Command | What It Does | When to Use |
|---------|--------------|-------------|
| `gw-pr-fix` | Fix broken tests/CI | Tests failing |
| `gw-pr-merge` | Merge finished work | Work is approved |
| `gw-editor` | Open code editor | Need full IDE |

## 🚀 Beginner Success Tips

### Performance
- Think in English (even if you speak another language) - saves money/tokens
- Work on one thing at a time
- Test early, test often

### Common Mistakes to Avoid
- ❌ Forgetting session info display
- ❌ Writing commit messages in non-English
- ❌ Adding AI signatures to code
- ❌ Not syncing todos before creating PRs
- ❌ Working on too many things at once

### Good Habits
- ✅ Always start with session info
- ✅ Break big tasks into small steps
- ✅ Commit working code frequently
- ✅ Sync your progress regularly
- ✅ Test before committing

## 📚 Learning Path

### Week 1: Basics
1. Learn to display session info
2. Practice `gw-iss-create` and `gw-iss-run`
3. Make simple commits with `gw-commit`

### Week 2: Workflow
1. Use TodoWrite for planning
2. Practice the Explore-Plan-Code-Commit cycle
3. Learn `gw-iss-sync`

### Week 3: Advanced
1. Work with multiple issues
2. Learn PR management
3. Use worktrees for parallel work

## 🔴 CRITICAL REMINDERS FOR BEGINNERS

### 1. Session Display (NEVER FORGET!)
**EVERY response must start with:**
```
🌿 Branch: [branch] | 🌲 Worktree: [path] | 🆔 [sessionId] | 📌 claude-xxxx | 🤖 [model]
```

### 2. Sync Before PR (REQUIRED!)
**Always run before creating Pull Requests:**
```bash
/user:gw-iss-sync
```

### 3. English for Internal Work (SAVES MONEY!)
- Think in English (saves 50-70% on costs)
- Commit messages in English
- Code comments in English
- **Even if you speak another language natively**

---

*Remember: Claude Code is powerful but start simple. Master the basics before moving to advanced features.*
