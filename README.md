# FYP Skills

A pack of AI agent skills for short-form content creators, written by a working creator who shoots, edits, and publishes product and entertainment videos every day across TikTok, Instagram, Facebook, YouTube, and Shopee.

Each skill is a field manual: it teaches an AI agent (Claude Code, Cursor, Codex, and other agents that support the SKILL.md format) one creator job, the way an experienced creator actually does it. No generic AI advice, no motivational filler. Concrete rules, platform-specific details, and output formats that are ready to paste.

## Skills in this pack

Six skills, one for each job in the short-form production chain:

| Skill | What it does |
| --- | --- |
| [video-hook](skills/video-hook/SKILL.md) | Researches and writes scroll-stopping hooks for short videos, ranked by pattern family (result first, mistake callout, curiosity gap, contrast, challenge, numbered promise). |
| [multi-platform-caption](skills/multi-platform-caption/SKILL.md) | Turns one video into five different paste-ready captions: TikTok, Instagram Reels, Facebook Reels, YouTube Shorts, and Shopee Video, each in that platform's own style. |
| [short-drama-script](skills/short-drama-script/SKILL.md) | Writes 60-90 second vertical drama episodes: hook in the first 3 seconds, one conflict, cliffhanger ending, character cards that stay consistent across episodes, plus per-scene image prompts for AI production. |
| [content-calendar](skills/content-calendar/SKILL.md) | Builds a realistic posting calendar from an existing stock of finished videos, with rotation rules, anchor posting times, and honest stock-out dates. |
| [thumbnail-brief](skills/thumbnail-brief/SKILL.md) | Writes a production-ready thumbnail or cover brief: big text of 3 to 4 words max, product close up, contrast plan, per platform sizes and safe zones, a face or faceless option, and A/B test variants, delivered as a designer brief plus an AI image prompt. |
| [affiliate-product-match](skills/affiliate-product-match/SKILL.md) | Matches a video to the exact affiliate listing it should link to, at variant level: color, size, and model must match exactly or the result is HOLD. Scores commission, sales, rating, and shop trust, avoids ambiguous multi brand listings, and outputs a ranked match table plus HOLD and REJECT cases. |

## Who this is for

- Solo creators and small teams publishing on multiple platforms from the same video stock
- Affiliate and TikTok Shop / Shopee sellers who need product-accurate captions at volume
- AI short-drama producers who need episode structure and character consistency
- Anyone whose AI assistant writes captions that sound like a brochure

## How to use

You do not need to be a developer to use this pack. There are three ways, from easiest to most complete:

### 1. Paste into any AI chat (no install)

Open the SKILL.md file of the skill you want, for example `skills/video-hook/SKILL.md`, copy the whole content, and paste it as the first message in ChatGPT, Claude, Gemini, or any other AI chat. Then just tell the AI what you are working on, for example "make hooks for a video reviewing a phone holder". The AI follows the skill's rules for the rest of that chat.

### 2. Put it in a Claude Project

If you use Claude, create a Project for your content work and paste the skill's content into the project instructions, or upload the SKILL.md file there. Every new chat inside that project then follows the skill automatically, so you never have to paste it again. This works well if you publish every day and always use the same one or two skills.

### 3. Install it in your agent (Claude Code, Cursor, and others)

Follow the Install section below. This is the full setup: the agent picks the right skill by itself whenever your request matches it, with no pasting at all.

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
