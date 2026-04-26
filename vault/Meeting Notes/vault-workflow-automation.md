---
title: Vault Workflow Automation
tags:
  - vault
  - hooks
  - automation
  - claude-code
---

# Vault Workflow Automation

## Overview

הגדרה אוטומטית של פרוטוקול ה-Obsidian Vault Workflow דרך Claude Code hooks. ב-`.claude/settings.json` הוגדרו שני hooks ברמת הפרויקט (משותפים עם כל מי שמשכפל את הרפו): `SessionStart` ו-`UserPromptSubmit`. כל אחד מזריק `additionalContext` שמזכיר ל-Claude לקרוא את [[skill-obsidian-vault-workflow]] ולעקוב אחרי שני השלבים שלו (Phase 1 לפני, Phase 2 אחרי). המטרה: שכל סשן ופקודה ייאלצו את ה-vault הזה לתפקד כזיכרון ארוך-טווח של הפרויקט, בלי שהמשתמש יצטרך לבקש את זה ידנית בכל פעם.

## Open Questions

- האם ה-additionalContext ב-397 תווים הוא הגודל הנכון? קצר מדי ייתן ל-Claude מעט מדי הקשר; ארוך מדי ישרוף הקשר בכל prompt.
- האם להוסיף גם `Stop` hook שיזכיר Phase 2 לפני שה-session מסתיים? כרגע מסתמכים על Phase 1 כדי שכל פקודה תזכיר את שני השלבים — אבל אם משתמש סוגר באמצע, אין אכיפה.
- ה-watcher של Claude Code לא בהכרח קולט אוטומטית את `.claude/settings.json` חדש. צריך `/hooks` או הפעלה מחדש של ה-CLI כדי לוודא שזה פעיל.

## Session Log

### 2026-04-26 — initial hook setup [shipped]

- **What was done:**
  - יצרתי `.claude/settings.json` ברמת הפרויקט (לא local — רוצים שזה יידחף לרפו וישותף עם דניאל וכל מי שיוריד).
  - הוגדרו שני hooks: `SessionStart` ו-`UserPromptSubmit`. שניהם משתמשים ב-`shell: "bash"` ו-`echo` של JSON עם `hookSpecificOutput.additionalContext`.
  - הטקסט ב-additionalContext מצביע על `.claude/skills/obsidian-vault-workflow/SKILL.md` ומפרט קצרות את שתי הפאזות.
  - יצרתי תיקיית `vault/Meeting Notes/` עם `_index.md` (לא היו עד כה — ה-vault הקיים הכיל רק את `vault/Files/`).
  - הפתק הזה הוא ה-Session Log הראשון.
- **Decisions:**
  - **רמת הפרויקט (`settings.json`), לא local** — כי המשתמש ביקש שכל מי שעובד ברפו יקבל את ההתנהגות. `settings.local.json` היה משאיר את זה אישי בלבד.
  - **`shell: "bash"` מפורש** — Windows לפעמים מפנה ל-PowerShell כברירת מחדל; ה-escape של ה-JSON ב-`echo '...'` יציב יותר ב-bash.
  - **טקסט קצר ב-additionalContext (397 תווים)** — UserPromptSubmit פולט אותו בכל prompt; כל תו מצטבר. הצבעה לקובץ ה-SKILL במקום שכפול תוכן מלאה.
  - **ללא `matcher`** — SessionStart ו-UserPromptSubmit אינם events של כלי ספציפי. ה-schema מאפשר להשמיט.
- **Notes / Caveats:**
  - `jq` לא מותקן על המחשב הזה — אומתה תקינות JSON עם `python -m json.tool` במקום.
  - ה-pipe-test עבר; פלט ה-bash תוקף JSON שמכיל את `hookEventName` הנכון לכל event ו-`additionalContext` באורך 397.
  - **Phase 6 דולגנו** (proof firing) — SessionStart ו-UserPromptSubmit פולטים מחוץ לתור הנוכחי. לא ניתן לוודא בזמן אמת שהם פועלים בלי `/hooks` או restart.
  - **פעולה למשתמש:** לפתוח `/hooks` פעם אחת או לעשות restart ל-Claude Code כדי שה-watcher יקלוט את הקובץ החדש.
- **Related:** [[skill-obsidian-vault-workflow]], [[skill-obsidian-markdown]], [[claude-settings-local]], [[claude-md]]
