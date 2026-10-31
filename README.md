# FYP Skills

A pack of AI agent skills for short-form content creators, written by a working creator who shoots, edits, and publishes product and entertainment videos every day across TikTok, Instagram, Facebook, YouTube, and Shopee.

Each skill is a field manual: it teaches an AI agent (Claude Code, Cursor, Codex, and other agents that support the SKILL.md format) one creator job, the way an experienced creator actually does it. No generic AI advice, no motivational filler. Concrete rules, platform-specific details, and output formats that are ready to paste.

## Skills in this pack

| Skill | What it does |
| --- | --- |
| [video-hook](skills/video-hook/SKILL.md) | Researches and writes scroll-stopping hooks for short videos, ranked by pattern family (result first, mistake callout, curiosity gap, contrast, challenge, numbered promise). |
| [multi-platform-caption](skills/multi-platform-caption/SKILL.md) | Turns one video into five different paste-ready captions: TikTok, Instagram Reels, Facebook Reels, YouTube Shorts, and Shopee Video, each in that platform's own style. |
| [short-drama-script](skills/short-drama-script/SKILL.md) | Writes 60-90 second vertical drama episodes: hook in the first 3 seconds, one conflict, cliffhanger ending, character cards that stay consistent across episodes, plus per-scene image prompts for AI production. |
| [content-calendar](skills/content-calendar/SKILL.md) | Builds a realistic posting calendar from an existing stock of finished videos, with rotation rules, anchor posting times, and honest stock-out dates. |

## Who this is for

- Solo creators and small teams publishing on multiple platforms from the same video stock
- Affiliate and TikTok Shop / Shopee sellers who need product-accurate captions at volume
- AI short-drama producers who need episode structure and character consistency
- Anyone whose AI assistant writes captions that sound like a brochure

## Install

These skills follow the open SKILL.md format used by Anthropic's skills repository.

Clone the repository and copy the skill folders into your agent's skills directory:

```bash
git clone https://github.com/xsrazy/fyp-skills.git
```

- Claude Code: copy `skills/<skill-name>` into `~/.claude/skills/` or your project's `.claude/skills/`, or install this repository as a plugin marketplace using the included `.claude-plugin/marketplace.json`.
- Other agents: point your agent at the `SKILL.md` file of the skill you want, or copy the folder into the skills location your agent documents.

Then just ask in plain language: "write hooks for a video about a phone holder for motorbikes" or "make captions for this product video for all five platforms". The agent picks the matching skill from its description and follows it.

## Language

The skills are written in English so agents apply them reliably, and they are built for Indonesian-market creators: platform rules include Shopee Video, defaults are Bahasa Indonesia output and WIB posting times, and every skill can switch output language on request.

## Contributing

New skills are welcome if they come from real production work: a clear trigger description, a concrete workflow, platform-specific rules, and a fixed output format. Generic prompt collections will not be merged.

## License

MIT. See [LICENSE](LICENSE).
