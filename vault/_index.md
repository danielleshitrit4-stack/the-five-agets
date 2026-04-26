---
title: Vault — Master Index
tags:
  - index
  - vault
---

# Vault — Master Index

ה-vault הזה הוא הזיכרון ארוך-הטווח של הפרויקט. הוא מתעד **מה כל קובץ בפרויקט עושה ולמי הוא משויך**.

> [!info] איך לקרוא את זה
> כל קובץ בפרויקט מקבל פתק MD משלו ב-[[Files/_index|Files]]. לכל פתק יש frontmatter עם `file-path`, `type` ו-`belongs-to`, ובגוף — תיאור התפקיד וקישורי `[[wikilinks]]` לקבצים קשורים.

## תתי-תיקיות

- [[Files/_index|Files]] — אינדקס פר-קובץ של כל הפרויקט

## קונבנציות

- **שמות קבצים** — אותיות קטנות עם מקפים, ללא תאריך. דוגמה: `claude-md.md`.
- **קישורים פנימיים** — תמיד `[[wikilinks]]`, אף פעם לא `[text](file.md)`.
- **Frontmatter** — כל פתק מתחיל ב-YAML עם `file-path`, `type`, `belongs-to`, `tags`.

## Types שנהוגים בפרויקט

| Type | משמעות |
|---|---|
| `doc` | מסמך טקסטואלי (כמו CLAUDE.md) |
| `config` | קובץ הגדרות (JSON, ENV, gitignore) |
| `skill` | קובץ SKILL.md של סקיל קוד |
| `placeholder` | קובץ ריק לשמירת תיקייה ב-git (.gitkeep) |
| `secret` | קובץ עם ערכים סודיים (לא נדחף ל-git) |

## Belongs-to (למי הקובץ משויך)

| Owner | משמעות |
|---|---|
| `claude-code` | חלק מהאינטגרציה עם Claude Code (תחת `.claude/`) |
| `obsidian` | חלק מקונפיגורציית Obsidian (תחת `.obsidian/`) |
| `git` | קובץ של Git (`.gitignore`, `.gitkeep`) |
| `project` | קובץ ברמת הפרויקט (CLAUDE.md, .env) |
| `user` | קובץ אישי שלא משותף |
