# SuperSocials

End-to-end social media skill for [Claude Code](https://claude.ai/code). Covers the full lifecycle from vague idea to polished deliverable: strategy, copywriting, video scripts, content calendars, visual briefs, and analytics. Works for any brand, any niche, any platform.

## Platforms

Instagram · TikTok · LinkedIn · X/Twitter · YouTube · Facebook · Pinterest · Threads · Bluesky

## Skills

| Skill | What it does |
|-------|-------------|
| `supersocials` | Hub — intent detection, brand briefing, routing, chaining |
| `supersocials:strategy` | Campaign briefs, content pillars, platform mix, posting cadence |
| `supersocials:write` | Captions, threads, hooks, CTAs, all written copy |
| `supersocials:script` | TikTok, Reels, YouTube long-form + Shorts scripts |
| `supersocials:calendar` | Weekly/monthly content plans |
| `supersocials:brief` | Visual/creative briefs for designers and image AI tools |
| `supersocials:analyse` | Analytics interpretation → strategic next actions |

## Install

```
/plugin install supersocials@thedanielmay
```

## Usage

**Vague input** → guided mode (brand brief → strategy → content):
```
I want to grow my Instagram for my coffee brand
```

**Specific input** → direct execution:
```
/supersocials write 5 LinkedIn posts about AI for founders, tone: authoritative but approachable
```

**Invoke a module directly:**
```
/supersocials:strategy
/supersocials:write
/supersocials:script
/supersocials:calendar
/supersocials:brief
/supersocials:analyse
```

## Chaining

SuperSocials can chain modules end-to-end:

**Strategy → Calendar → Copy → Visual Brief**

After each module completes, it offers to continue to the next step. You control depth.

## External Skills Used

SuperSocials transparently invokes these skills when relevant (announced before each call):

- `topic-intel` — audience and niche research
- `company-intel` — competitor positioning
- `expert-panel` — strategy pressure-testing and analytics interpretation
- `humanize` — making copy and scripts feel genuinely human
- `elements-of-style` — sharpness and precision for written copy
- `find-skills` — surfaces installable skills when a request is out of scope

## Author

Daniel May — [daniel@thedanielmay.com](mailto:daniel@thedanielmay.com)
