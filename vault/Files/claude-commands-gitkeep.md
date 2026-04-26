---
title: .claude/commands/.gitkeep
file-path: .claude/commands/.gitkeep
type: placeholder
belongs-to: git
tags:
  - placeholder
  - claude-code
  - commands
---

# .claude/commands/.gitkeep

## תפקיד

קובץ דמה ששומר על קיום התיקייה `.claude/commands/` בתוך git (כי git לא עוקב אחרי תיקיות ריקות).

## על התיקייה עצמה

`.claude/commands/` היא המקום שבו מגדירים **slash commands מותאמים אישית** לפרויקט הזה. כל קובץ `.md` כאן הופך לפקודה שמופעלת ב-`/command-name` מתוך Claude Code.

> [!example] דוגמה
> קובץ `.claude/commands/deploy.md` יוצר את הפקודה `/deploy`. תוכן הקובץ הוא ה-prompt שיישלח ל-Claude כשמפעילים את הפקודה.

## מתי משתמשים בזה

- אוטומציה של זרימות עבודה חוזרות (deploy, test, review)
- קיצורי דרך לפקודות ארוכות
- תבניות לבקשות סטנדרטיות

## מי הבעלים

`git` — הקובץ עצמו הוא placeholder של git. תוכן עתידי בתיקייה ישוייך ל-`claude-code`.

## קבצים קשורים

- [[claude-agents-gitkeep]] — אותו תפקיד placeholder, לתיקיית agents
- [[claude-hooks-gitkeep]] — אותו תפקיד placeholder, לתיקיית hooks
- [[claude-skills-gitkeep]] — אותו תפקיד placeholder, לתיקיית skills
- [[claude-settings-local]] — קונפיגורציה ש-slash commands יכולים להישען עליה
