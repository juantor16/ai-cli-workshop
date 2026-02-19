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

### Prompt 4: LinkedIn Hiring Post
```
Write a LinkedIn post announcing we're hiring Senior Developers.
Make it:
- Engaging, not corporate-boring
- Mention what makes our team special
- Include a call to action
- Add relevant hashtags
- Keep it under 200 words
```

---

## 🔑 Teaching Points

- AI excels at summarizing unstructured text
- Generate multiple content variations quickly
- Maintain consistent professional tone
- HR/Marketing can use AI without writing code
