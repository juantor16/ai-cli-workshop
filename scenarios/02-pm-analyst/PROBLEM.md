# 📊 Scenario 2: PM / Analyst - Sales Data Analysis

## The Problem

You're a Product Manager preparing for the quarterly business review. Finance just sent you a CSV with last quarter's sales data. The CEO wants to know:

1. **What were our top 5 products** by revenue?
2. **Which region is underperforming** and by how much?
3. **A 1-paragraph executive summary** for the board deck

You don't have time to open Excel and create pivot tables. You need answers NOW.

---

## 📄 Input File

`sales-q4-2025.csv` - Sales data from October-December 2025

---

## 🎯 Expected Output

1. Top 5 products ranked by revenue
2. Regional performance comparison
3. Executive summary ready for copy-paste

---

## 💬 Suggested Prompts

### Prompt 1: Quick Analysis
```
Read sales-q4-2025.csv and tell me:
1. Total revenue for the quarter
2. Top 5 products by revenue (with amounts)
3. Revenue breakdown by region
```

### Prompt 2: Find Problems
```
Based on the sales data, identify:
1. Which region is underperforming vs the average?
2. Are there any products with declining sales month-over-month?
3. Any unusual patterns I should be aware of?
```

### Prompt 3: Generate Executive Summary
```
Write a 1-paragraph executive summary of Q4 2025 sales performance 
that I can paste into a board presentation. Include:
- Total revenue
- Top performing product
- Key concern or opportunity
- Recommendation

Keep it under 100 words, professional tone.
```

### Prompt 4: Create Visualization Data
```
Generate the data I need to create a bar chart in Google Sheets showing:
- Monthly revenue trend (Oct, Nov, Dec)
- Format as a simple table I can copy-paste
```

---

## 🔑 Teaching Points

- AI can analyze CSV/Excel data without complex tools
- Natural language queries = no SQL or formulas needed
- Generate presentation-ready content instantly
- Perfect for people who aren't "technical"
