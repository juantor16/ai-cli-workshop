# 🔧 Scenario 1: Developer - Log Analysis

## The Problem

You're a developer on the Platform team. The ops team just sent you a server log file from last night's incident. They need you to:

1. **Find all ERROR entries** and categorize them
2. **Identify the most frequent error** type
3. **Create a simple script** that can monitor for these errors in real-time

You have 10 minutes before the incident review meeting.

---

## 📄 Input File

`server-logs.txt` - 500 lines of server logs from the incident

---

## 🎯 Expected Output

1. A summary of errors by type
2. A timeline of when errors occurred
3. A simple monitoring script

---

## 💬 Suggested Prompts

### Prompt 1: Initial Analysis
```
Read the file server-logs.txt and give me:
1. Total number of ERROR entries
2. Group them by error type
3. Show me the timeline (when did each type first appear?)
```

### Prompt 2: Deep Dive
```
For the most frequent error type, show me:
1. The full error messages
2. Any patterns in the data (user IDs, endpoints, etc.)
3. Possible root cause based on the context
```

### Prompt 3: Create Monitoring Script
```
Create a bash script called monitor.sh that:
1. Tails a log file passed as argument
2. Highlights ERROR lines in red
3. Counts errors per minute
4. Alerts if more than 5 errors occur in 1 minute
```

---

## 🔑 Teaching Points

- AI can process large files instantly
- Pattern recognition across hundreds of lines
- Code generation from natural language requirements
- Iterative refinement ("make it also count warnings")
