# 🏢 Scenario 5: Cross-File Company Analysis

## The Problem

You're a consultant who just got access to TechFlow Solutions' internal documents. The CEO wants answers FAST:

1. **"How is the company doing financially?"**
2. **"Which projects are at risk?"**
3. **"Who are our top performers?"**
4. **"What's our customer churn situation?"**

The data is scattered across multiple folders and file types. Normally this would take hours of digging.

---

## 📁 Company Structure

```
company-data/
├── finance/
│   ├── q4-2025-budget.csv
│   ├── expenses-december.csv
│   └── revenue-forecast.md
├── hr/
│   ├── employees.csv
│   ├── performance-reviews.md
│   └── hiring-plan-2026.md
├── projects/
│   ├── active-projects.csv
│   ├── project-alpha-status.md
│   └── project-beta-status.md
├── customers/
│   ├── customer-list.csv
│   ├── churn-risk.csv
│   └── nps-survey-results.md
└── reports/
    └── (empty - AI will generate reports here)
```

---

## 🎯 What This Demonstrates

1. **Multi-file navigation** - AI reads across directories
2. **Cross-referencing data** - Connects info from different sources
3. **Different output formats** - Not just HTML:
   - Markdown reports
   - CSV summaries
   - Plain text analysis
   - Actionable recommendations
4. **Real business questions** - Not just coding tasks

---

## 💬 Suggested Prompts

### Prompt 1: Explore the Data
```
List all files in this directory recursively.
Then give me a 1-sentence summary of what each file contains.
```

### Prompt 2: Financial Overview
```
Read the files in the finance/ folder.
Give me a brief financial health summary:
- Total budget vs projected revenue
- Major expense categories
- Any red flags?
```

### Prompt 3: Cross-Reference Analysis
```
Compare employees.csv with active-projects.csv.
- Which employees are on multiple projects?
- Any projects that seem understaffed?
- Who are the project leads and how are their performance reviews?
```

### Prompt 4: Risk Assessment
```
Analyze all available data and identify the top 3 business risks.
Cross-reference:
- Project delays (from project status files)
- Employee performance issues (from HR)
- Customer churn risk (from customers/)
Write a 1-page executive risk briefing.
```

### Prompt 5: Generate Dashboard Data (NOT HTML)
```
Create a data summary file (dashboard-data.md) that includes:
- Key metrics from all departments
- Traffic light status (🟢🟡🔴) for each area
- Top 3 actions needed

Format as clean markdown, not HTML.
```

### Prompt 6: Custom Report
```
The CEO is meeting investors tomorrow.
Create a 1-page company overview that highlights:
- Revenue growth
- Team strength
- Key projects
- Customer satisfaction

Make it optimistic but honest. Save as investor-brief.md
```

---

## 🔑 Teaching Points

- AI CLI tools excel at **navigating file systems**
- Can **cross-reference** data that would take humans hours
- Output can be **any format** - not just code or HTML
- Perfect for **business analysis**, not just development
- Shows value for **non-technical roles** (consultants, analysts, executives)
