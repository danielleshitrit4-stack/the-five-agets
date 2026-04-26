---
title: .claude/skills/obsidian-markdown/SKILL.md
file-path: .claude/skills/obsidian-markdown/SKILL.md
type: skill
belongs-to: claude-code
tags:
  - skill
  - obsidian
  - markdown
  - syntax
---

# .claude/skills/obsidian-markdown/SKILL.md

## תפקיד

Skill שמלמד את Claude את **התחביר המורחב** של Obsidian Flavored Markdown — מעבר ל-CommonMark/GFM הסטנדרטי. זה ה-skill ש**הופעל בפועל** ביצירת קבצי ה-vault הזה.

## מתי לטרוגר את ה-Skill

המשתמש מזכיר:
- wikilinks, callouts, frontmatter, properties, embeds
- עבודה עם קבצי `.md` ב-Obsidian
- תגיות (`#tag`), aliases, block IDs

## מה ה-Skill מכיל

| נושא | מה זה |
|---|---|
| **Wikilinks** | `[[Note Name]]`, `[[Note#Heading]]`, `[[Note\|Display]]` |
| **Embeds** | `![[Note]]`, `![[image.png\|300]]`, `![[doc.pdf#page=3]]` |
| **Callouts** | `> [!note]`, `> [!warning] Title`, foldable עם `-`/`+` |
| **Properties** | YAML frontmatter עם `tags`, `aliases`, `cssclasses` |
| **Tags** | `#tag` inline או ב-frontmatter, תמיכה ב-nested (`#a/b`) |
| **Comments** | `%%hidden%%` |
| **Highlight** | `==text==` |
| **LaTeX** | `$inline$`, `$$block$$` |
| **Mermaid** | בלוקים של ` ```mermaid ` |
| **Footnotes** | `[^1]`, inline `^[...]` |

## איך ה-Skill הזה משפיע על ה-Vault

כל פתק ב-[[Files/_index|Files]] (כולל הפתק הזה עצמו) משתמש בקונבנציות מה-skill:
- frontmatter עם `title`, `tags`, וקסטם properties (`file-path`, `type`, `belongs-to`)
- wikilinks `[[...]]` לקבצים פנימיים, לא markdown links
- Callouts (`> [!info]`, `> [!warning]`) להדגשות

## מי הבעלים

`claude-code` — חלק ממערכת ה-skills של Claude Code עבור הפרויקט.

## קבצים קשורים

- [[skill-obsidian-vault-workflow]] — workflow שמשתמש בתחביר הזה
- [[skill-obsidian-bases]] — בנוי על אותו vault
- [[claude-skills-gitkeep]] — תיקיית האב של ה-skill
