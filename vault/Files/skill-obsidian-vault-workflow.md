---
title: .claude/skills/obsidian-vault-workflow/SKILL.md
file-path: .claude/skills/obsidian-vault-workflow/SKILL.md
type: skill
belongs-to: claude-code
tags:
  - skill
  - obsidian
  - vault
  - workflow
  - session-log
---

# .claude/skills/obsidian-vault-workflow/SKILL.md

## תפקיד

Skill שאוכף **פרוטוקול חובה לקריאה+כתיבה** ב-vault של הפרויקט. הרעיון: ה-vault הוא הזיכרון ארוך-הטווח של Claude Code. לפני כל משימה — קרא את קובץ הנושא הרלוונטי. אחרי כל משימה — הוסף סיכום מתוארך לקובץ.

## מתי לטרוגר את ה-Skill

**כל משימה.** כתיבת קוד, ארכיטקטורה, content, bugfix, review, refactor. רק שאלות read-only שלא נוגעות בקבצים פטורות.

## מבנה הפרוטוקול

| שלב | פעולה |
|---|---|
| **לפני** | זיהוי הנושא → איתור קובץ בנושא ב-`vault/<folder>/<topic>.md` → קריאה מלאה (Overview + Open Questions + Session Log) |
| **קריאה מקבילה** | 2-3 ה-Meeting Notes האחרונות, Content Briefs רלוונטיים, Brand Guidelines אם נוגע |
| **אחרי** | הוספת `### YYYY-MM-DD — <title> [status]` בתחתית ה-Session Log |
| **Verify** | קריאה חוזרת של הקובץ לוודא שהכתיבה הצליחה |

## תיקיות ה-Workflow

| תיקייה | למה |
|---|---|
| `vault/Meeting Notes/` | קוד, ארכיטקטורה, החלטות, session logs |
| `vault/Content Briefs/` | בריפים תוכניים |
| `vault/Publishing Log/` | פרסומים והפקת לקחים |
| `vault/Brand Guidelines/` | קול, ויזואל, טון |

> [!warning] ה-vault הזה (פתק זה כולל) הוא **לא** workflow כזה
> ה-vault שאתה רואה ב-[[Files/_index]] הוא **אינדקס פר-קובץ**, לא session log לפי נושא. הוא שואב מקונבנציות התחביר של [[skill-obsidian-markdown]] ומבנה ה-folders + `_index.md` של ה-skill הזה — אבל המטרה שלו שונה.

## Status tags חובה

`[shipped]`, `[spiked]`, `[wip]`, `[reverted]`, `[planned]`, `[debug]` — כל heading של session חייב להסתיים בתג סוגריים מרובעים.

## Anti-patterns שכדאי להכיר

- ❌ `YYYY-MM-DD <topic>.md` בשם הקובץ (פרוטוקול ישן)
- ❌ קובץ נושא בלי שורה ב-`_index.md`
- ❌ markdown links במקום wikilinks
- ❌ הכרזה על השלמה בלי קריאה חוזרת מאמתת

## מי הבעלים

`claude-code` — חלק ממערכת ה-skills של Claude Code עבור הפרויקט.

## קבצים קשורים

- [[skill-obsidian-markdown]] — תחביר Obsidian (wikilinks, callouts) שה-workflow מסתמך עליו
- [[skill-obsidian-bases]] — skill מקביל שעובד על אותו vault
- [[claude-skills-gitkeep]] — תיקיית האב של ה-skill
- [[claude-md]] — הקובץ הראשי שה-workflow מתעד עבודה סביבו
