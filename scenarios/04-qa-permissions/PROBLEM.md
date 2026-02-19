# 🔐 Scenario 4: QA - Permissions Comparison Tool

## The Problem

You're a QA Engineer testing a permissions system. Every release, you need to verify that user permissions match what's documented. Currently you do this manually in Excel - takes hours and is error-prone.

You have:
1. **permissions-expected.csv** - The "source of truth" (what permissions SHOULD be)
2. **permissions-actual.csv** - Export from the live system (what permissions ARE)

You need to:
1. **Compare both files** and find discrepancies
2. **Create a reusable HTML tool** that anyone on the team can use for future testing
3. The tool should be **standalone** (no server needed, just open the HTML)

---

## 📄 Input Files

- `permissions-expected.csv` - Documented permissions (source of truth)
- `permissions-actual.csv` - Exported from system (has some intentional discrepancies)

---

## 🎯 Expected Output

A **self-contained HTML file** (`permissions-checker.html`) that:
1. Lets you upload 2 CSV files
2. Compares them automatically
3. Shows matches ✅ and mismatches ❌ clearly
4. Can be used by anyone, anytime, without setup

---

## 💬 Suggested Prompts

### Prompt 1: Initial Analysis
```
Read permissions-expected.csv and permissions-actual.csv.
Compare them and tell me:
1. How many users are in each file?
2. Which users have different permissions between the two?
3. What specific differences exist?
```

### Prompt 2: Create the Reusable Tool
```
Create a single HTML file called "permissions-checker.html" that:

1. Has a clean, modern UI (dark mode preferred)
2. Has two file upload buttons: "Source of Truth" and "System Export"
3. When both files are uploaded, automatically compares them
4. Shows results in a table with columns:
   - User
   - App
   - Expected Permission
   - Actual Permission
   - Status (✅ Match or ❌ Mismatch)
5. Highlights mismatches in red
6. Shows summary stats at the top (total, matches, mismatches)
7. Has a "Copy Results" button to export findings
8. Works 100% client-side (no server needed)

Make it look professional - this will be used by the whole QA team.
```

### Prompt 3: Add Features
```
Add these features to the tool:
1. Filter to show only mismatches
2. Search box to find specific users
3. Export results to CSV
4. Show percentage of compliance
```

---

## 🔑 Teaching Points

- AI can create **production-ready tools**, not just one-time answers
- Self-contained HTML = no deployment needed, shareable via Slack/email
- QA teams can build their own utilities without waiting for dev resources
- The tool lives on after the workshop!

---

## 🎁 Bonus

After the workshop, the permissions-checker.html can be:
- Saved to the team's shared drive
- Used for every release
- Customized for other comparison needs
