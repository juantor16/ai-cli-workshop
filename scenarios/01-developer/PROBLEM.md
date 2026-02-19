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

### Prompt 3: Create Reusable Log Analyzer Tool
```
Create a single HTML file called "log-analyzer.html" that:

1. Has a modern dark UI
2. Lets me paste or upload log files
3. Automatically detects and highlights:
   - ERROR (red)
   - WARN (yellow) 
   - INFO (gray)
4. Shows a summary: total lines, errors, warnings
5. Filters to show only errors/warnings
6. Timeline chart showing errors over time
7. Search functionality
8. Works 100% in the browser (no server)

This tool should be reusable for any future incident analysis.
```

### Prompt 4: Add Export Feature
```
Add a "Generate Incident Report" button that creates a 
markdown summary I can paste into Slack/Jira with:
- Incident timeline
- Error counts by type
- Affected services
- Suggested root cause
```

---

## 🔑 Teaching Points

- AI can process large files instantly
- Pattern recognition across hundreds of lines
- **Create reusable tools, not just one-time answers**
- The HTML tool can be used for every future incident

## 🎁 End Result

A `log-analyzer.html` file that the whole team can use for incident analysis - no setup required, just open in browser.
