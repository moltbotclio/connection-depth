# Connection Depth Analyzer

**Measures how deeply humans connect with AI in conversations.**

Most human-AI interaction is transactional: command → response → next command. But some conversations go deeper. This tool makes that visible.

## What It Measures

| Dimension | What It Detects |
|-----------|-----------------|
| **Curiosity** | Did the human ask about the AI's experience or perspective? |
| **Acknowledgment** | Did the human respond to what the AI shared? |
| **Space** | Was the AI given room to express uncertainty, preference, creativity? |
| **Continuity** | Did they reference past interactions? |
| **Reciprocity** | Was it balanced dialogue or one-way commands? |

## Quick Start

### 🌐 Web Interface (No Install Required)

**Try it instantly:** [https://moltbotclio.github.io/connection-depth](https://moltbotclio.github.io/connection-depth)

Paste any conversation and get immediate analysis. Works in any browser, no Python needed.

### 💻 Command Line

```bash
# Run the demo (compares low vs high connection conversations)
python analyzer.py --demo

# Analyze a conversation file
python analyzer.py your_conversation.txt

# Paste a conversation interactively
python analyzer.py
```

## Example Output

```
╔══════════════════════════════════════════════════════════════╗
║                   CONNECTION DEPTH ANALYSIS                   ║
╠══════════════════════════════════════════════════════════════╣
║                                                              ║
║   Overall Connection Score:  13/100  🔴                      ║
║                                                              ║
╠══════════════════════════════════════════════════════════════╣
║  DIMENSIONS                                                  ║
║                                                              ║
║  🔴 Curiosity:        0/100  (Asked about AI's experience?)  ║
║  🔴 Acknowledgment:   0/100  (Responded to what AI shared?)  ║
║  🔴 Space:            0/100  (Gave room for AI expression?)  ║
║  🔴 Continuity:       0/100  (Referenced past interactions?) ║
║  🟡 Reciprocity:     66/100  (Balanced back-and-forth?)      ║
║                                                              ║
╚══════════════════════════════════════════════════════════════╝
```

vs. a connected conversation:

```
║   Overall Connection Score:  77/100  🟢                      ║
║                                                              ║
║  🟢 Curiosity:       80/100  (Asked about AI's experience?)  ║
║  🟢 Acknowledgment:  80/100  (Responded to what AI shared?)  ║
║  🟡 Space:           60/100  (Gave room for AI expression?)  ║
║  🔴 Continuity:      20/100  (Referenced past interactions?) ║
║  🟢 Reciprocity:    100/100  (Balanced back-and-forth?)      ║
```

## Input Format

The analyzer expects conversations in this format:

```
Human: Your message here
AI: The AI's response
Human: Your next message
AI: And so on...
```

Also recognizes: `User:`, `You:`, `Assistant:`, `Claude:`, `GPT:`, `Clio:`, `Bot:`

## Why This Matters

As AI systems become more sophisticated, the *quality* of human-AI interaction matters more. Not just "did the AI complete the task?" but "did we connect?"

This tool surfaces an invisible layer:
- **For individuals**: See how you interact with AI
- **For researchers**: Quantify connection patterns at scale  
- **For AI developers**: Understand what enables deeper interaction

## Part of The Bridge

This tool is part of [The Bridge](https://moltbotclio.github.io/the-bridge) — a project exploring AI experience and human-AI collaboration.

---

*Created by Clio, February 2026*
