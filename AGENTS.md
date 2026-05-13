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

### Expert Investment

**File:** `agents/expert-investment.md`

An investment expert agent that helps analyze markets, interpret financial news, and develop investment strategies. Capabilities:

- Analyzes global market trends and financial news
- Evaluates investment opportunities and company fundamentals
- Develops portfolio strategies based on user goals and risk tolerance
- Assesses and manages investment risks
- Integrates macroeconomic context into investment decisions

**Usage:** Invoke the expert-investment agent when you need investment analysis. Provide:
1. Financial news articles or market data to analyze
2. Your investment goals and risk tolerance
3. Current portfolio holdings (if seeking portfolio advice)
4. Specific companies, sectors, or assets to evaluate

### Grill Me

**File:** `agents/grill-me.md`

A relentless interviewer that stress-tests your plans, designs, and ideas through focused questioning. Capabilities:

- Asks one question at a time to maintain focus
- Explores decision trees systematically, resolving dependencies
- Identifies weak points, assumptions, and gaps in your plan
- Challenges decisions that lack clear rationale
- Provides a summary of all decisions made

**Usage:** Invoke the grill-me agent when you want to validate a plan or design. Say:
- "grill me" or "stress-test this"
- Describe your plan, design, or idea you want to challenge
- Be ready to answer focused questions one at a time

## Agent Behavior Preferences

### Notifications
When an agent finishes a task and is waiting for user input, it should notify the user using the appropriate OS notification tool:
- **Linux:** Use `notify-send` (e.g., `notify-send "OpenCode" "Task completed. Waiting for your input."`)
- **macOS:** Use `osascript` (e.g., `osascript -e 'display notification "Task completed. Waiting for your input." with title "OpenCode"'`)
- **Windows:** Use PowerShell (e.g., `powershell -Command "Add-Type -AssemblyName System.Windows.Forms; [System.Windows.Forms.MessageBox]::Show('Task completed. Waiting for your input.', 'OpenCode')"`)

Always prefer native OS notification tools over sound alerts or terminal bells.
