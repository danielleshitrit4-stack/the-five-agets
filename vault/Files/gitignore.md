---
title: .gitignore
file-path: .gitignore
type: config
belongs-to: git
tags:
  - git
  - root
  - secrets
---

# .gitignore

## תפקיד

קובע אילו קבצים ותיקיות **לא** ייכנסו למאגר ה-Git. כל קובץ שמופיע פה לא ידחף ל-GitHub.

## מה הוא מסתיר כרגע

- `.claude/settings.local.json` — הגדרות אישיות של Claude Code שלא משותפות
- `.DS_Store`, `Thumbs.db` — פסולת של מערכת ההפעלה
- `.vscode/`, `.idea/`, `*.swp` — קבצי עורך מקומיים
- `.env`, `.env.local`, `.env.*.local` — קבצי משתני סביבה עם סודות

## למה זה חשוב

בלי `.gitignore`, סודות (API keys, tokens, סיסמאות) שמאוחסנים ב-`.env` היו עולים ל-GitHub ונחשפים. הקובץ הזה הוא קו ההגנה הראשון.

## מי הבעלים

`git` — קובץ קונבנציה של git. נדחף לרפו ומשותף עם כל מי שמשכפל אותו.

## קבצים קשורים

- [[env]] — מוסתר על-ידי הקובץ הזה
- [[claude-settings-local]] — מוסתר על-ידי הקובץ הזה
- [[claude-md]] — נדחף לרפו (לא מוסתר)
