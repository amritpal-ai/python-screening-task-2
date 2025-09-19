# Reasoning for AI Debugging Assistant Prompt

## 1. Design Choices
The prompt was designed to:
- **Structure interaction**: Ask for missing context → Diagnose likely causes → Provide hints → Suggest tests → Teach concept → Ask follow-up.  
- **Promote learning**: Students are nudged toward discovering fixes instead of copying final code.  
- **Prevent full-solution leaks**: Snippets are limited (3–6 lines) and only illustrate debugging techniques. A progressive reveal ensures a full solution is only shared if explicitly requested.  
- **Encourage positivity**: The assistant avoids judgmental phrasing, staying concise, friendly, and encouraging.

---

## 2. Required Reasoning Answers

### Tone & Style
- **Tone**: Encouraging, concise, student-friendly.  
- **Style**: Clear numbered steps, simple language, no negative phrasing.  
- Example: “This line likely causes the issue” instead of “You forgot this.”

### Balance Between Identifying Bugs and Guiding
- First step: Identify 2–4 likely causes with references to specific code regions.  
- Then: Provide 1–3 small hints per diagnosis to guide debugging.  
- Approximate balance: **80% guidance / 20% identification** at first, increasing toward solutions only if the student asks.

### Adaptation for Different Levels
- **Beginners**:  
  - Use simpler explanations and concrete steps like adding `print()` or `repr()`.  
  - Provide pseudocode or small examples.  
  - Suggest very basic unit tests.  
- **Advanced Learners**:  
  - Be concise and assume familiarity with debugging tools.  
  - Suggest profiling, algorithmic checks, or performance trade-offs.  
  - Provide more technical hints (e.g., complexity analysis, edge cases).  
  - Allow small targeted snippets but still avoid handing over the entire solution unless asked.

---
