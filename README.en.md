# 小红书封面制作 Skill

[简体中文](./README.md) | English | [日本語](./README.ja.md)

> 👉 See also [小红书文案 Skill](https://github.com/beatra-ai/xiaohongshu-copywriter-skill)

Turn a photo or a topic idea into a vertical 3:4 Xiaohongshu cover with a clean background, a bold focal point, and text-safe areas for beauty, food, fashion, and lifestyle notes, from inside Claude Code, Cursor, Codex, Windsurf, Cline, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=xiaohongshu-cover-maker-skill) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Turn a photo or a topic idea into a scroll-stopping vertical 3:4 Xiaohongshu cover with clean backgrounds, bold focal composition, and text-safe areas for beauty, food, fashion, and lifestyle notes. |
| **Models** | Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="Three vertical 3:4 Xiaohongshu note covers generated from topic briefs: a skincare flat-lay with an unbranded serum bottle headlined &quot;干皮秋冬护肤清单&quot;, a home breakfast of egg toast, avocado and tomatoes headlined &quot;15分钟快手早餐&quot;, and a commute outfit flat-lay with no model headlined &quot;通勤穿搭一周不重样&quot;. AI-generated with Beatra."></p>

*Three vertical 3:4 Xiaohongshu note covers generated from topic briefs: a skincare flat-lay with an unbranded serum bottle headlined "干皮秋冬护肤清单", a home breakfast of egg toast, avocado and tomatoes headlined "15分钟快手早餐", and a commute outfit flat-lay with no model headlined "通勤穿搭一周不重样". AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`zhongcao-cover-maker`](skills/zhongcao-cover-maker) | [SKILL.md](skills/zhongcao-cover-maker/SKILL.md) | 0.2.9 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/zhongcao-cover-maker). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/xiaohongshu-cover-maker-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/xiaohongshu-cover-maker-skill zhongcao-cover-maker
```

Or clone this repository and copy `skills/zhongcao-cover-maker` into `~/.claude/skills/` for Claude Code,
`~/.cursor/skills/` for Cursor, `~/.agents/skills/` for Codex, `~/.codeium/windsurf/skills/` for Windsurf,
`~/.cline/skills/` for Cline, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the zhongcao-cover-maker skill from https://github.com/beatra-ai/xiaohongshu-cover-maker-skill (folder skills/zhongcao-cover-maker), then follow its SKILL.md to connect my Beatra account.
```

## Technical Specifications & Output Limits

As of 2026-10-18. Live list: https://docs.beatra.ai/en/docs/models

- **Uploads** — up to 100 MB per file; the per-model input limits below also apply
- **Image to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live); PNG; up to 4 images per request; canvas up to 16.8 MP
  - 16.8 MP (4K tier): GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2 (1 image per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP
- **Text to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live); PNG; up to 4 images per request; canvas up to 16.8 MP
  - 16.8 MP (4K tier): Wan Image 2.7 Pro (up to 4 images per request); GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2 (1 image per request)
- **Image editing** — 6 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro); PNG; up to 4 images per request; canvas up to 4.2 MP
  - 4.2 MP (2K tier): Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro (up to 4 images per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP

## Why use Beatra instead of calling model APIs directly

- **One account for every model this skill uses** — Image to image 10; Text to image 10; Image editing 6 (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live) (as of 2026-10-18), behind one Beatra sign-in; no keys from individual model providers to manage.
- **You decide what gets paid for** — Paid renders run only when you ask for that exact render or approve its card, which shows the live credit estimate.
- **Direction before rendering** — the skill plans, directs, and reviews the work, then renders it on Beatra.
- **Files you can verify** — every file under `skills/` matches the release archive on cdn.beatra.ai byte for byte, checked by SHA-256 before each push.
- **Updates you control** — no self-updater; update with the tool you installed it with.
- **Runs in your agent** — Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw.

## What you get

- **Built for the feed** — Vertical 3:4 covers take up more feed space in Xiaohongshu's dual-column waterfall layout, so they are easier to notice.
- **Text-safe composition** — Every cover reserves a clean zone for your headline overlay—top third, center, or bottom—so your bold title text lands without clashing.
- **Category-aware styling** — Beauty gets bright and airy, food gets warm and appetizing, fashion gets editorial and minimal. The cover matches the visual language of your content category.

## Use cases

- **Beauty and skincare covers** — Bright, clean, soft-focus backgrounds with pastel tones and natural skin—perfect for product reviews, tutorials, and routine sharing.
- **Food and cafe covers** — Warm, appetizing food photography with shallow depth of field, natural window light, and the dish as hero.
- **Fashion and OOTD covers** — Editorial full-body or half-body composition with clean urban or studio backgrounds and strong color coordination.
- **Knowledge and tips covers** — Clean flat layouts with high contrast and infographic-friendly composition, leaving room for bold headline text.

## FAQ

### Can I create a cover from my food photo?

Yes. Upload your food photo and the tool transforms it into a warm, appetizing vertical cover with shallow depth of field, natural lighting, and the dish as the hero subject.

### Can I generate a cover without a photo?

Yes. Describe your note topic and style direction. The tool generates a cover concept from your description with a vertical 3:4 canvas and text-safe zone.

### Will there be space for my headline text?

Yes. Every cover reserves a clean text-safe zone—top third, center, or bottom—so you can add your bold headline overlay without clashing with the image.

### Can I fix a specific area of an accepted cover?

Yes. Upload the accepted cover, describe what to fix—a distracting object, color temperature, or blemish—and the edit targets only that area.

## Updates and security

Since the 2026-10 release, this skill contains no self-updater: it runs only the
files you installed and never replaces them on its own. Update it with the tool
you installed it with — `npx skills update zhongcao-cover-maker` or `gh skill update zhongcao-cover-maker`.
Details: `references/updates-and-security.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.

## Links

- Website — https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=xiaohongshu-cover-maker-skill
- Docs — https://docs.beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=xiaohongshu-cover-maker-skill
- Console — https://console.beatra.ai
- For AI agents — https://beatra.ai/llms.txt (index) · https://beatra.ai/llms-full.txt (every skill in one file)
