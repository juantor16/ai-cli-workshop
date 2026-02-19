# 👥 Scenario 3: HR / Marketing - Candidate Feedback & Content

## The Problem

You're in HR/Talent Acquisition. You just finished interviewing 8 candidates for a Senior Developer position. You have raw interview notes from multiple interviewers and need to:

1. **Summarize each candidate** in 2-3 sentences
2. **Rank them** based on the feedback
3. **Draft a rejection email** for candidates who didn't make it
4. **Create a LinkedIn post** announcing you're hiring (for future roles)

You have 30 minutes before the hiring committee meeting.

---

## 📄 Input File

`interview-notes.md` - Raw notes from 4 interviewers about 8 candidates

---

## 🎯 Expected Output

1. Candidate summary table
2. Ranked recommendation
3. Professional rejection email template
4. LinkedIn hiring post

---

## 💬 Suggested Prompts

### Prompt 1: Summarize Candidates
```
Read interview-notes.md and create a summary table with:
| Candidate | Strengths | Concerns | Overall Impression |

Keep each cell to 1-2 sentences max.
```

### Prompt 2: Rank and Recommend
```
Based on the interview feedback, rank the candidates from strongest to weakest.
For the top 3, explain why they should move forward.
For the bottom 3, explain the main concerns.
```

### Prompt 3: Draft Rejection Email
```
Write a professional but warm rejection email for candidates who didn't make it.
- Thank them for their time
- Be encouraging but clear
- Mention we'll keep their info on file
- Keep it under 150 words
```

### Prompt 4: Create Reusable Interview Scoring Tool
```
Create a single HTML file called "interview-scorer.html" that:

1. Has a professional UI
2. Lets me paste interview notes (free text)
3. Uses a form to input:
   - Candidate name
   - Position
   - Interviewer scores (1-5) for: Technical, Communication, Culture Fit
4. Calculates weighted average score
5. Generates a summary paragraph
6. Stores all candidates in a table (localStorage)
7. Exports final ranking to CSV
8. Has templates for rejection/offer emails

This tool should work for any hiring process, not just this one.
```

### Prompt 5: Add Comparison View
```
Add a feature that shows all candidates side-by-side with:
- Radar chart comparing their scores
- Color coding (green=proceed, yellow=maybe, red=pass)
- One-click email generation for each candidate
```

---

## 🔑 Teaching Points

- AI excels at summarizing unstructured text
- **Build tools that become part of your workflow**
- HR can create their own utilities
- Templates save time on repetitive communications

## 🎁 End Result

An `interview-scorer.html` that HR uses for every hiring round - consistent process, faster decisions.
