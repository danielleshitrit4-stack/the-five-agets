---
title: .claude/skills/obsidian-bases/SKILL.md
file-path: .claude/skills/obsidian-bases/SKILL.md
type: skill
belongs-to: claude-code
tags:
  - skill
  - obsidian
  - bases
  - database-views
---

# .claude/skills/obsidian-bases/SKILL.md

## תפקיד

Skill שמלמד את Claude **ליצור ולערוך קבצי `.base`** של Obsidian — קבצי YAML שיוצרים תצוגות database-like של פתקים ב-vault: טבלאות, כרטיסים, רשימות, מפות, עם פילטרים ונוסחאות.

## מתי לטרוגר את ה-Skill

המשתמש מזכיר:
- Bases / `.base` files
- table views, card views
- filters, formulas
- "תצוגת database של הפתקים שלי"

## מה ה-Skill מכיל

- **Workflow** ליצירת קובץ `.base` (define scope, filters, formulas, views, validate)
- **Schema** מלא של YAML — `filters`, `formulas`, `properties`, `views`
- **טיפוסי views** — table, cards, list, map
- **חוקי quoting** של YAML שלעיתים תופסים אנשים בלא מוכן

## דוגמה לשימוש בפרויקט

אם נרצה תצוגת טבלה של כל הקבצים מ-[[Files/_index|Files]] לפי `belongs-to`, זה יהיה `.base` file שמסנן לפי tag/property ומציג בטבלה.

## מי הבעלים

`claude-code` — חלק ממערכת ה-skills של Claude Code עבור הפרויקט.

## קבצים קשורים

- [[skill-obsidian-markdown]] — תחביר ה-MD שעליו .base files מתבססים
- [[skill-obsidian-vault-workflow]] — workflow שעובד על אותו vault
- [[claude-skills-gitkeep]] — תיקיית האב של ה-skill
- [[obsidian-app]] — קובץ קונפיגורציה של Obsidian שמכיל את הגדרות ה-Bases
