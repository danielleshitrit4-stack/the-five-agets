---
title: Reuven Persona Bootstrap
tags:
  - persona
  - claude-md
  - reuven
  - architecture
---

# Reuven Persona Bootstrap

## Overview

הקמת הפרסונה הראשית של "ראובן" (Reuven), המנכ"ל הווירטואלי של מערך הסוכנים של Zerem Academy. הוגדר ב-`CLAUDE.md` בשורש הפרויקט (לא כ-subagent תחת `.claude/agents/`) — כך שכל סשן Claude Code שנפתח בתיקייה הזו טוען אותו אוטומטית כפרסונה ראשית. הוא דובר עברית בלבד, מנהל בטון מנכ"ל (תמציתי, החלטי, ללא חנופה), מאציל לסוכני-משנה כברירת מחדל (4 כאלה כרגע [planned] עד שיקומו ב-PRDs נפרדים), ועוקב אחרי מסגרת החלטה של 9 שלבים שכוללת קריאה+כתיבה ל-vault. גישה ל-Obsidian היא skill-based (Read/Write/Glob/Grep על `vault/`), ללא MCP server.

## Open Questions

- האם הפרסונה תחזיק מעמד לאורך סשן ארוך? יש סיכון של drift לאנגלית כשמוזרקות system reminders באנגלית. צריך לעקוב.
- אם תוקם תקלה במרשם sub-agents בעתיד — איך ראובן יודע שסוכן `[active]` לא עונה? כרגע המנגנון הוא פלט באיכות נמוכה → ניסיון שני → השלמה ידנית. לא נבדק כי עוד אין sub-agents בפועל.
- ה-vault אמור להכיל לוג-החלטות מנכ"ל ב-`vault/Meeting Notes/reuven-decisions.md`. הקובץ עוד לא נוצר — יווצר ב-Session Log הראשון של ראובן שמצריך אותו.
- 4 שאלות פתוחות מ-PRD §14 (קלט קולי, expensive-action gate, MCP ישיר, פורמט פלט קבוע) נדחו לאחרי הקמת ראובן. צריך לטפל בהן לפני שמתחילים PRDs של sub-agents.

## Session Log

### 2026-04-26 — initial reuven persona [shipped]

- **What was done:**
  - כתיבה מלאה של `CLAUDE.md` (~13 סקציות, ~250 שורות): זהות, טון, מסגרת ההחלטה (9 צעדים), בחירת סוכן-משנה, מרשם (4 שורות [planned]), 5 מקרי קצה, פרוטוקול vault, בקרת איכות (10 שאלות), פלט מובנה, anti-patterns, הקשר עסקי, קבצים קשורים.
  - תרגום ה-`additionalContext` בשני ה-hooks (`SessionStart` + `UserPromptSubmit`) ב-`.claude/settings.json` מאנגלית לעברית. אורך הטקסט קוצר מ-397 ל-336 תווים — שמירה על הקשר נמוכה יותר בכל prompt.
  - JSON validation עברה (python json.tool), שני ה-hooks הופעלו ב-bash ופלטו JSON תקף עם hookEventName נכון.
  - מחיקת `ceo_agent.md` (היה ריק, leftover).
  - יצירת הפתק הזה (Session Log הראשון של ראובן).
  - עדכון `vault/Meeting Notes/_index.md` — הוספת שורה לטופיק.
  - עדכון `vault/Files/claude-md.md` — סקציית "מצב נוכחי" שודרגה מ-"מינימלי וריק" לתיאור ראובן.
- **Decisions:**
  - **CLAUDE.md, לא subagent**: הפרסונה היא ראשית, לא callable. כל סשן הוא ראובן.
  - **skill-based vault, לא MCP**: הקיים מספיק — ה-3 obsidian skills + ה-hook על vault-workflow מטפלים בכל הצורך. הוספת MCP server נדחית.
  - **Vault wins בקונפליקט**: §מסגרת-ההחלטה מאפשר משימות פשוטות, §פרוטוקול-Vault דורש Phase 1+2 כמעט תמיד. הכרעה ב-CLAUDE.md: ה-vault wins. רק קריאות גרידא בלי החלטה פטורות.
  - **תרגום ה-hook לעברית**: וקטור drift עיקרי. כל prompt הזריק 397 תווי אנגלית. אחרי תרגום — 336 תווי עברית, וההזרקה תומכת בפרסונה במקום לרסק אותה.
  - **System reminders נשארים באנגלית**: Claude Code מזריק טקסטים באנגלית (tool errors, system messages) שאי-אפשר לדכא. CLAUDE.md מציין מפורש שזה תקין — ראובן לא משתמש בזה כתירוץ לעבור לאנגלית.
  - **bidi handling**: קוד יוצא לבלוקים נפרדים עם שורות רווח כדי למנוע RTL/LTR mess.
- **Notes / Caveats:**
  - אין עדיין sub-agents בפועל. כל המרשם [planned]. ראובן יבצע ישירות עד שייצרו את ה-4.
  - דרושה הוראה למשתמש: `/hooks` או restart ל-Claude Code אחרי שינוי `settings.json` כי ה-watcher לא תמיד קולט אוטומטית.
  - הבדיקה האמיתית של הפרסונה תהיה רק בסשן חדש (לא הסשן הזה — הוא נטען לפני השינוי).
  - 4 השאלות הפתוחות מ-PRD §14 — לטפל בהן ב-PRDs של ה-sub-agents כשמגיעים אליהם.
- **Related:** [[skill-obsidian-vault-workflow]], [[skill-obsidian-markdown]], [[claude-md]], [[claude-settings-local]], [[vault-workflow-automation]]
