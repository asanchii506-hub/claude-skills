# Claude Skills

Набор skills для Claude Code: дизайн, motion, AI-агенты, маркетинг, психология продаж, требования РФ к сайтам.

## Как это работает

Skills лежат в `.claude/skills/`. Claude Code подхватывает их автоматически, когда этот репозиторий открыт в сессии.

**На своём компьютере (для всех проектов):** скопируй содержимое `.claude/skills/` в `~/.claude/skills/` (Windows: `C:\Users\<имя>\.claude\skills\`) и перезапусти Claude Code.

## Источники и лицензии

Все skills скопированы без изменений из открытых репозиториев. Тексты лицензий авторов — в папке `LICENSES/` и внутри папок skills, где они были. У remotion-dev/skills файла лицензии нет: репозиторий приватный и только для личного использования, публиковать его не стоит.

| Тема | Skills | Источник | Лицензия |
|---|---|---|---|
| Дизайн | frontend-design, canvas-design, theme-factory, algorithmic-art, web-artifacts-builder | anthropics/skills | Apache-2.0 |
| Дизайн | ui-ux-pro-max, design-system, ui-styling, brand, banner-design | nextlevelbuilder/ui-ux-pro-max-skill | MIT |
| Дизайн | visual-design-foundations, interaction-design, design-system-patterns, responsive-design, accessibility-compliance, mobile-ios-design, mobile-android-design, web-component-design | wshobson/agents | MIT |
| Motion | motion-design | LottieFiles/motion-design-skill | MIT |
| Motion | design-motion-principles | kylezantos/design-motion-principles | MIT |
| Motion (видео) | remotion-best-practices, remotion-create, remotion-render, remotion-captions, remotion-docs | remotion-dev/skills | см. репозиторий; сам Remotion платный для компаний от 4 человек |
| AI-агенты | mcp-builder | anthropics/skills | Apache-2.0 |
| AI-агенты | prompt-engineering-patterns, langchain-architecture, llm-evaluation, rag-implementation, embedding-strategies, similarity-search-patterns, hybrid-search-implementation, vector-index-tuning | wshobson/agents | MIT |
| AI-агенты | agent-designer, agent-workflow-designer, rag-architect | alirezarezvani/claude-skills | MIT |
| Маркетинг и продажи | 53 skills (copywriting, cro, seo-audit, ai-seo, marketing-psychology, offers, sales-enablement и др.) | coreyhaines31/marketingskills | MIT |
| Юридический РФ | ru-website-legal-compliance (152-ФЗ, ЗОЗПП, РКН) | duduev/rkn-compliance | MIT |

`ru-website-legal-compliance` — технический чек-лист, а не юридическая консультация.
