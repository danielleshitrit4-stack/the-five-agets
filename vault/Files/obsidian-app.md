---
title: .obsidian/app.json
file-path: .obsidian/app.json
type: config
belongs-to: obsidian
tags:
  - obsidian
  - config
  - app
---

# .obsidian/app.json

## תפקיד

הגדרות גלובליות של Obsidian עבור ה-vault הזה: התנהגות עורך, attachments, default view ועוד.

## מצב נוכחי

```json
{}
```

ריק לחלוטין — Obsidian משתמש בברירות המחדל לכל ההעדפות. ברגע שתשנה משהו ב-Settings → Editor / Files & Links / וכו', הקובץ הזה ייכתב מחדש עם ההעדפות שלך.

## מה הקובץ יכיל בעתיד

דוגמאות לערכים שנכנסים פה:
- `livePreview: true/false` — מצב Live Preview
- `useTab: true` ו-`tabSize: 4` — הגדרות טאבים
- `attachmentFolderPath: "attachments"` — איפה Obsidian שומר תמונות
- `newFileLocation: "current"` — איפה נוצר קובץ חדש כשפותחים note חדש
- `alwaysUpdateLinks: true` — האם wikilinks מתעדכנים אוטומטית כש-rename

## מי הבעלים

`obsidian` — נוצר ומנוהל ע"י Obsidian. אתה לא עורך אותו ידנית — אתה משנה דברים בממשק Settings.

## קבצים קשורים

- [[obsidian-appearance]] — הגדרות עיצוב נפרדות
- [[obsidian-core-plugins]] — אילו core plugins מופעלים
- [[obsidian-graph]] — הגדרות הגרף
- [[obsidian-workspace]] — מצב פתיחה של חלונות
