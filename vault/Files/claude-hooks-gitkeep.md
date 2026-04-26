---
title: .claude/hooks/.gitkeep
file-path: .claude/hooks/.gitkeep
type: placeholder
belongs-to: git
tags:
  - placeholder
  - claude-code
  - hooks
  - automation
---

# .claude/hooks/.gitkeep

## תפקיד

קובץ דמה ששומר על קיום התיקייה `.claude/hooks/` ב-git.

## על התיקייה עצמה

`.claude/hooks/` היא המקום שבו שמים **סקריפטים שמתבצעים אוטומטית** בנקודות מסוימות בעבודה של Claude Code.

## נקודות אירוע שנפוצות

| Event | מתי |
|---|---|
| `SessionStart` | בתחילת כל sessionחדש |
| `PreToolUse` | לפני שכלי כלשהו רץ |
| `PostToolUse` | אחרי שכלי כלשהו רץ |
| `Stop` | כש-Claude מסיים תור |
| `UserPromptSubmit` | כל פעם שהמשתמש שולח prompt |

> [!tip] דוגמה
> אפשר להריץ אוטומטית `npm test` ב-`PostToolUse` של Edit, ככה שכל שינוי בקוד מאומת מיידית.

## מתי משתמשים בזה

- הרצת tests/lint אוטומטית אחרי שינויים
- חסימת פעולות מסוכנות (PreToolUse)
- לוגינג של פעילות ה-session
- התראות מותאמות

## הגדרת hooks

ה-hooks מוגדרים ב-[[claude-settings-local]] (או ב-`settings.json` המשותף), ומפנים לסקריפטים שיושבים בתיקייה הזו.

## מי הבעלים

`git` — הקובץ עצמו placeholder של git. סקריפטים עתידיים בתיקייה ישוייכו ל-`claude-code`.

## קבצים קשורים

- [[claude-settings-local]] — מגדיר אילו hooks דלוקים ומה הם מפעילים
- [[claude-agents-gitkeep]] — placeholder אחר תחת `.claude/`
- [[claude-commands-gitkeep]] — placeholder אחר תחת `.claude/`
- [[claude-skills-gitkeep]] — placeholder אחר תחת `.claude/`
