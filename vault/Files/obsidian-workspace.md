---
title: .obsidian/workspace.json
file-path: .obsidian/workspace.json
type: config
belongs-to: obsidian
tags:
  - obsidian
  - config
  - workspace
  - layout
---

# .obsidian/workspace.json

## תפקיד

מצב **הסידור** של Obsidian: אילו חלונות פתוחים, באילו טאבים, באילו panes (שמאל/ימין/מרכז), מה הקובץ הפעיל, היסטוריית קבצים אחרונים.

## למה זה חשוב

זה הקובץ ש-Obsidian מתעדכן בו **כל הזמן** — בכל פעם שאתה פותח טאב, גורר panel, סוגר חלון. הוא מאפשר ל-Obsidian לחזור בדיוק לאותו מצב בפתיחה הבאה.

## מבנה כללי של הקובץ

- `main` — אזור הטאבים המרכזי
- `left` — sidebar שמאל (file-explorer, search, וכו')
- `right` — sidebar ימין (backlinks, outline, וכו')
- `floating` — חלונות צפים
- `active` — איזה pane מופעל כעת
- `lastOpenFiles` — רשימת ה-recents

## אם נדחף ל-git — נושא לבעיה

כל ה-vault הזה נדחף לרפו. אבל הקובץ הזה משתנה בלי הפסקה כשעובדים. אם דניאל ואתה תעבדו במקביל — תקבלו merge conflicts בכל push. **שיקול לעתיד:** להוסיף `.obsidian/workspace.json` ל-[[gitignore]] כדי שכל אחד יקבל את הסידור שלו.

## מי הבעלים

`obsidian` — נכתב מחדש כל הזמן ע"י Obsidian. אף אחד לא עורך אותו ידנית.

## קבצים קשורים

- [[obsidian-app]] — הגדרות אפליקציה כלליות
- [[obsidian-appearance]] — עיצוב
- [[obsidian-core-plugins]] — אילו plugins דלוקים (משפיע על אילו panes יכולים להיות)
- [[obsidian-graph]] — הגדרות הגרף (workspace שומר אם הגרף פתוח)
- [[gitignore]] — מועמד פוטנציאלי להוספה ל-.gitignore
