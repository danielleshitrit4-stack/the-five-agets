---
title: .claude/agents/.gitkeep
file-path: .claude/agents/.gitkeep
type: placeholder
belongs-to: git
tags:
  - placeholder
  - claude-code
  - agents
---

# .claude/agents/.gitkeep

## תפקיד

קובץ ריק שמטרתו היחידה היא לאלץ את git לשמור את התיקייה `.claude/agents/` ברפו. **git לא עוקב אחרי תיקיות ריקות** — לכן הוספנו קובץ דמה כדי שהתיקייה תישמר.

## על התיקייה עצמה

`.claude/agents/` היא המקום שבו Claude Code מחפש **subagents מותאמים אישית** של הפרויקט. כל קובץ `.md` בתיקייה הזו עם frontmatter מתאים מגדיר agent חדש שאפשר להפעיל מ-Claude Code.

> [!example] דוגמה לקובץ agent
> ```markdown
> ---
> name: code-reviewer
> description: Use this agent when reviewing code...
> tools: All tools
> ---
> # Instructions...
> ```

## מי הבעלים

`git` — הקובץ עצמו הוא קונבנציה של git. **התוכן שיתווסף בעתיד** בתיקייה (קבצי agents בפועל) ישוייך ל-`claude-code`.

## קבצים קשורים

- [[claude-commands-gitkeep]] — אותו רעיון, לתיקיית slash commands
- [[claude-hooks-gitkeep]] — אותו רעיון, לתיקיית hooks
- [[claude-skills-gitkeep]] — אותו רעיון, לתיקיית skills
- [[claude-settings-local]] — הגדרות Claude Code שיכולות להפעיל agents
