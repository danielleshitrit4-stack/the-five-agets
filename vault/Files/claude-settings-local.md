---
title: .claude/settings.local.json
file-path: .claude/settings.local.json
type: config
belongs-to: claude-code
tags:
  - claude-code
  - permissions
  - local-only
---

# .claude/settings.local.json

## תפקיד

הגדרות **לוקאליות ואישיות** של Claude Code עבור הפרויקט הזה: הרשאות לכלים, משתני סביבה ב-Claude, ו-hooks אישיים.

## ההבדל מ-settings.json

- `settings.json` — נדחף ל-git, משותף עם כל מי שעובד ברפו (לא קיים בפרויקט הזה כרגע)
- `settings.local.json` — אישי, **gitignored** ב-[[gitignore]], נשאר רק על המחשב שלך

## תוכן כרגע

```json
{
  "permissions": {
    "allow": [],
    "deny": []
  }
}
```

ריק — אין עדיין הרשאות מוגדרות. ככל שתעבוד יותר תוכל להוסיף לכאן הרשאות אוטומטיות לכלים שאתה משתמש בהם הרבה (למשל `Bash(git status:*)`) כדי שלא יבקש אישור בכל פעם.

## מבנה אפשרי

- `permissions.allow` — תבניות שיאושרו אוטומטית
- `permissions.deny` — תבניות שייחסמו תמיד
- `env` — משתני סביבה ש-Claude Code יראה
- `hooks` — סקריפטים שירוצו בנקודות מסוימות (PreToolUse, SessionStart וכו')

## מי הבעלים

`claude-code` — חלק מהאינטגרציה של Claude Code עם הפרויקט. הוא **לא משותף**, ולכן כל מפתח שעובד ברפו יוצר אצלו עותק משלו עם ההעדפות שלו.

## קבצים קשורים

- [[gitignore]] — מסתיר את הקובץ הזה מ-git
- [[claude-md]] — מסמך הנחיה משותף (משלים את הקובץ האישי הזה)
- [[claude-agents-gitkeep]] — תיקיית agents ש-Claude Code משתמש בה
- [[claude-commands-gitkeep]] — תיקיית slash commands
- [[claude-hooks-gitkeep]] — תיקיית hooks
- [[claude-skills-gitkeep]] — תיקיית skills
