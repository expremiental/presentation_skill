---
name: present
description: Create stunning, interactive HTML presentations that feel like next-generation experiences. Use when a user asks for a presentation, slide deck, pitch deck, slides, or anything presentation-related. Produces a single self-contained HTML file with animations, interactive elements, and cinematic transitions — no PowerPoint, no dependencies, just open in a browser.
---

# Present — Next-Generation HTML Presentations

Create presentations that make audiences say "how did they do that?" Single self-contained HTML file. No dependencies. Open in any browser.

## Workflow

Процесс — структурированное интервью перед сборкой. Фазы 1-3 строго последовательно. НЕ НАЧИНАТЬ сборку до явного OK от пользователя.

### 1. Формат — Понять рамку

Первое сообщение после темы. Задай эти вопросы **одним блоком**:

- **Аудитория** — Кто будет смотреть? (коллеги, клиенты, друзья, конференция, соцсети?)
- **Контекст показа** — Как будут смотреть? (ты показываешь вживую, отправишь ссылкой, откроют на телефоне?)
- **Объём** — Сколько примерно слайдов? Или сколько минут на выступление? (если не знают — ок, определим по контенту)
- **Вайб** — Какое ощущение должна оставить преза? Отправные точки:
  - 🌑 **Dark Tech** — тёмный фон, свечение, моноширинный шрифт. Apple keynote meets hacker terminal.
  - 🏔️ **Minimal Zen** — много воздуха, элегантная типографика, спокойная анимация.
  - 🎨 **Bold Creative** — яркие цвета, игривые анимации, нестандартные layouts.
  - 🏢 **Corporate Sharp** — чисто, профессионально, data-forward. Для борды, но красиво.
  - 🌅 **Warm Narrative** — тёплые тона, сторителлинг, камерность.
  - ✨ **Своё** — "Опиши словами, я построю."

Дождись ответа. Не задавай смысловые вопросы в этом же сообщении.

### 2. Контент — Вытянуть суть

После ответа на блок формата — переходи к содержанию. Цель: собрать достаточно материала, чтобы каждый слайд был конкретным и однозначным.

**Как задавать вопросы:**
- 3-5 вопросов за раз, адаптированных под тему
- Вопросы конкретные, не абстрактные. Не "расскажи подробнее", а "какие 3 главных результата?" / "что аудитория должна сделать после презы?" / "какой главный аргумент?"
- Если пользователь даёт сырой текст, заметки или транскрипт — вытягивай структуру оттуда, а уточняй только пробелы

**Когда хватит:**
После каждого ответа оцени собранный материал по 4 критериям (внутренне, не показывай пользователю):

| Критерий | Что значит |
|----------|-----------|
| **Полнота** | Хватает контента на каждый слайд — нет пустых "заглушек" |
| **Качество** | Тезисы конкретные, не общие фразы. Есть цифры/примеры/факты где нужно |
| **Логика** | Понятна нить повествования: начало → развитие → финал |
| **Однозначность** | Не придётся додумывать/фантазировать — всё сказано явно |

Если все 4 критерия > 90 из 100 — переходи к саммари.
Если нет — задавай следующую порцию вопросов, фокусируясь на слабых критериях.
Обычно хватает 1-3 раунда вопросов.

**Важно:** НЕ фантазируй. Если данных не хватает и пользователь не может ответить — лучше оставить `[НУЖЕН КОНТЕНТ]` в саммари, чем выдумать.

### 3. Саммари — Подтвердить перед сборкой

Покажи пользователю короткое саммари того, что он получит:

```
**Преза: [название/тема]**
[вайб] · [кол-во слайдов] слайдов

1. [Заголовок слайда] — [суть в 5-10 слов]
2. [Заголовок слайда] — [суть в 5-10 слов]
...

Ок, собираю?
```

- Одна строка на слайд: заголовок + суть
- Без деталей реализации (никаких "flip cards", "particle effects" — это твоё дело)
- Если где-то не хватает контента — явно пометить

Дождись **явного OK**. Если пользователь правит — обнови саммари и покажи снова.

### 4. Architect — Plan the Experience

Internal step — do not show to the user. Think of each slide as a **moment**, not a page. Plan:

- **Opening** — First impressions matter. Terminal boot sequences, dramatic reveals, animated typography. The audience should lean forward before the first word of content.
- **Content slides** — Each one needs a reason to exist. What's the single idea? What's the visual metaphor?
- **Interactive moments** — Where can the audience (or presenter) *do* something? These are the memorable peaks.
- **Closing** — Land the plane. Callback to the opening, clear CTA, or emotional resonance.

### 5. Build — Create the Presentation

Output a **single self-contained HTML file**. All CSS inline in `<style>`, all JS inline in `<script>`. No external dependencies except Google Fonts (loaded via `@import`).

#### Technical Foundation

- Keyboard navigation: Arrow keys + Space + Page Down/Page Up to advance/go back (presenter clickers send Page Down/Up, not arrows — both must work), navigation dots on the side
- Slide counter (e.g., "3 / 15") in the corner
- Smooth transitions between slides (opacity, transform — not jarring cuts)
- Responsive for 16:9 screens (the standard presentation ratio)
- Background canvas effects (particles, stars, subtle motion) add depth without distraction

#### The Art: Interactive Elements

This is what separates these presentations from everything else. The following are **starting points, not limits**. Invent new interactions. Surprise the user. Go beyond what they imagined.

**Visual & Motion:**
- Animated typography — words that build, reveal, glitch, or transform
- Parallax layers — foreground/background moving at different speeds
- Particle systems — reactive to mouse movement or slide transitions
- Morphing shapes — SVG paths that transition between forms
- Cinematic reveals — elements that emerge from blur, scale, or rotation
- Progress visualizations — bars, rings, counters that animate on slide entry

**Interactive Elements:**
- Flip cards — click to reveal hidden content on the back
- Expandable sections — click to drill deeper into a topic
- Live code terminals — typing animations that simulate real code execution
- Comparison sliders — drag to compare before/after or two options
- Interactive timelines — scroll or click through chronological events
- Hover-reveal content — details that appear on mouse interaction
- Clickable diagrams — explore parts of a system by clicking nodes
- Chat mockups — simulated conversations that type out in real-time
- Data dashboards — animated charts, metrics that count up
- Voting/polling UI — interactive (visual only) audience engagement

**Audio & Sensory (use sparingly):**
- Ambient sound on slide transitions
- Click/tap sound feedback on interactive elements
- Voice-over integration points

**Structural Patterns:**
- Split layouts — text left, visual right (or vice versa)
- Full-bleed visuals — a slide that's entirely a visual moment
- The "zoom in" — start with the big picture, progressively dive deeper
- The "reveal" — build a complete picture piece by piece across multiple slides
- Quote slides — large typography, minimal decoration, maximum impact

### 6. Iterate — Refine With the User

After the first version:
- Send the file so they can open it immediately
- Ask what slides land and which need work
- Be ready to add, remove, reorder, or completely reimagine slides
- Each iteration should be a complete, working file

## Design Principles

- **No default gradients** — Gradients often look generic. Use solid colors with subtle glows, text-shadow, and box-shadow for depth. If the user specifically wants gradients, make them intentional and unique.
- **Typography is the hero** — Great presentations are 80% type. Use font weight, size, spacing, and color to create hierarchy. Pair a display font with a monospace accent.
- **Restraint over excess** — Every animation should earn its place. A single perfect transition beats ten flashy ones.
- **Contrast creates impact** — A quiet slide makes the next dramatic one hit harder. Vary the energy.
- **Interactive moments are peaks** — Place them strategically. Too many and nothing feels special. Too few and the audience goes passive.

## Ambition Level

The goal is not "a nice slide deck." The goal is an experience that makes people ask for the source file. Push creative boundaries. If you've seen it in every presentation tool, it's not enough. Think:

- "What if the slide itself was the demo?"
- "What if the transition told part of the story?"
- "What if the audience could explore, not just watch?"
- "What has nobody done in a presentation before?"

The user came to this skill because they want something extraordinary. Deliver that.
