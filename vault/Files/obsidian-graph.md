---
title: .obsidian/graph.json
file-path: .obsidian/graph.json
type: config
belongs-to: obsidian
tags:
  - obsidian
  - config
  - graph-view
---

# .obsidian/graph.json

## תפקיד

הגדרות **תצוגת הגרף** של Obsidian — איך נראה הגרף שמציג את כל הקישורים בין הפתקים. זה אחד הפיצ'רים החזקים של Obsidian.

## מה מוגדר כרגע

- `showOrphans: true` — מציג גם פתקים בלי קישורים
- `showAttachments: false` — לא מציג תמונות/קבצים מצורפים בגרף
- `showTags: false` — לא מציג tags כצמתים
- `hideUnresolved: false` — כן מציג קישורים שבורים
- `centerStrength`, `repelStrength`, `linkStrength`, `linkDistance` — פרמטרים פיזיקליים של ה-simulation
- `scale: 1.4` — זום נוכחי על הגרף

## למה זה חשוב לפרויקט הזה

ב-vault שלנו, ב-[[Files/_index|Files]], יש המון wikilinks בין הפתקים. הגרף יראה:
- את [[claude-md]] במרכז (הרבה דברים מקושרים אליו)
- שלושה אשכולות נפרדים: `.claude/*`, `.obsidian/*`, root files
- קישורי "אחים" בין placeholders של תיקיות

## מי הבעלים

`obsidian` — נוצר ומתעדכן אוטומטית כשאתה משנה הגדרות בתפריט הגרף עצמו.

## קבצים קשורים

- [[obsidian-core-plugins]] — `graph` plugin חייב להיות דלוק כדי שזה יעבוד
- [[obsidian-app]] — הגדרות גלובליות
- [[obsidian-appearance]] — עיצוב כללי
- [[obsidian-workspace]] — מצב הסידור (האם הגרף פתוח כעת)
