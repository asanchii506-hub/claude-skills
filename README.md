# Claude Skills

Набор skills для Claude Code: дизайн, motion, AI-агенты, маркетинг, психология продаж, требования РФ к сайтам.

## Как это работает

Skills лежат в `.claude/skills/`. Claude Code подхватывает их автоматически, когда этот репозиторий открыт в сессии.

**На своём компьютере (для всех проектов):** скопируй содержимое `.claude/skills/` в `~/.claude/skills/` (Windows: `C:\Users\<имя>\.claude\skills\`) и перезапусти Claude Code.

**Папка `.claude/tools/`** — справочники по сервисам (Ahrefs, GA4, Semrush и др.), на которые ссылаются маркетинговые skills `link-building` и `reverse-engineer-marketing`. На компьютере скопируй её в `~/.claude/tools/` (Windows: `C:\Users\<имя>\.claude\tools\`). Источник: coreyhaines31/marketingskills, MIT.

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
| Видео | ffmpeg-skill | ruizrica/ffmpeg-skill | MIT |
| Видео | shorts (Claude Shorts) | AgriciDaniel/claude-shorts | MIT; рендер через Remotion |
| Видео | hyperframes, hyperframes-cli, hyperframes-registry, media-use, reverse-any-video, style-sampling | heygen-com/hyperframes | Apache-2.0 |

`ru-website-legal-compliance` — технический чек-лист, а не юридическая консультация.

## Видео

Для всех видео-skills нужен **FFmpeg** (Windows: `winget install Gyan.FFmpeg`).

| Skill | Что делает | Что ещё нужно | Пример промпта |
|---|---|---|---|
| `/ffmpeg-skill` | Монтаж готового видео на компьютере: обрезка, склейка, 9:16 для Reels, субтитры, логотип, музыка с приглушением под голос, удаление пауз, громкость, экспорт под YouTube/TikTok | Python 3.9+ | `Обрежь video.mp4 до 60 секунд, сделай вертикальным 9:16 и добавь субтитры` |
| `/hyperframes` | Видео из HTML-кода: промо продукта, заставки, анимированная инфографика, титры. Можно повторить стиль понравившегося ролика (`/reverse-any-video`) | Node.js 22+ | `Сделай 15-секундное промо-видео для лендинга кофейни в тёплых тонах, 1080×1920` |
| `/shorts` | Из длинного видео (подкаст, интервью, вебинар) находит лучшие моменты и делает вертикальные шортсы с анимированными субтитрами | Python 3.10+, Node.js 18+. **Windows: только через WSL 2**. Один раз запустить `bash ~/.claude/skills/shorts/setup.sh` | `Сделай 3 шортса из podcast.mp4 для Reels, субтитры в стиле Bold` |

**Статистика HyperFrames.** HyperFrames отправляет анонимные счётчики использования (без текстов и имён файлов). Выключить один раз: `npx hyperframes telemetry disable`.

**Не входят в набор:**
- **OpenMontage** (OpenMontageInc/OpenMontage, AGPL-3.0) — не skill, а целая студия видеопроизводства: сценарий, озвучка, музыка, генерация картинок, монтаж. Скачивается отдельной папкой и открывается в Claude Code. Многие функции требуют платных ключей (генерация картинок, голос).
- **Ghost Editor** (kurbaitaev/ghost-editor) — монтаж говорящей головы в рилсы. Работает только на Mac с Apple silicon.
