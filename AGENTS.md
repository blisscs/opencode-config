# Agent Configurations

This directory contains custom agent definitions for opencode.

## Available Agents

### Teacher

**File:** `agents/teacher.md`

An educational agent that helps create personalized study plans. Capabilities:

- Reads learning topics from provided web links
- Compares new material against your existing knowledge base
- Generates structured study plans with milestones
- Creates study notes and summaries
- Tracks learning progress over time

**Usage:** Invoke the teacher agent when you want to learn a new topic. Provide:
1. Web links to resources you want to learn from
2. Description of what you already know about the topic
3. Your learning goals or desired outcomes

## Agent Behavior Preferences

### Notifications
When an agent finishes a task and is waiting for user input, it should notify the user using the appropriate OS notification tool:
- **Linux:** Use `notify-send` (e.g., `notify-send "OpenCode" "Task completed. Waiting for your input."`)
- **macOS:** Use `osascript` (e.g., `osascript -e 'display notification "Task completed. Waiting for your input." with title "OpenCode"'`)
- **Windows:** Use PowerShell (e.g., `powershell -Command "Add-Type -AssemblyName System.Windows.Forms; [System.Windows.Forms.MessageBox]::Show('Task completed. Waiting for your input.', 'OpenCode')"`)

Always prefer native OS notification tools over sound alerts or terminal bells.
