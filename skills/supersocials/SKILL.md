---
name: supersocials
description: Use when the user wants help with any aspect of social media — strategy, content writing, video scripts, content calendars, visual briefs, analytics interpretation, or campaign planning. Triggers on mentions of Instagram, TikTok, LinkedIn, X, Twitter, YouTube, Facebook, Pinterest, Threads, Bluesky, social media, content marketing, or posting.
---

# SuperSocials

End-to-end social media skill. Covers the full lifecycle from vague idea to polished deliverable: strategy, copywriting, video scripts, content calendars, visual briefs, and analytics. Works for any brand, any niche, any platform.

## Platforms

Instagram · TikTok · LinkedIn · X/Twitter · YouTube · Facebook · Pinterest · Threads · Bluesky

## Dependency Check

Before doing anything else, check whether the following skills appear in the available skill list for this session:

- `topic-intel`
- `company-intel`
- `expert-panel`
- `humanize`
- `elements-of-style`

If ANY are missing, stop and say:

> "SuperSocials works best with its full skill set. The following skills are missing from this session:
> [list the missing ones]
>
> To install them:
> - `topic-intel`, `company-intel`, `humanize` — check your superpowers marketplace or install via your plugin manager
> - `expert-panel` — `/plugin install expert-panel@thedanielmay`
> - `elements-of-style` — `/plugin install elements-of-style@superpowers-marketplace`
>
> Restart your session after installing, then try again.
> Or type **'continue anyway'** to proceed — steps that need missing skills will be skipped."

If the user types 'continue anyway', note which skills are unavailable and proceed. When a missing skill would normally be invoked, skip that step and note it inline: "(skipped — `humanize` not available)".

If all skills are present, proceed silently without mentioning the check.

## How to Start

Read the user's input and route without asking for a menu selection:

**Vague input** — user says something like "I want to grow on Instagram" or "help me with social media for my brand"
→ Enter **Guided Mode**: collect a brand brief, then route to the right module(s)

**Specific input** — user says something like "write 5 LinkedIn posts about AI for founders" or "I need a TikTok script about productivity"
→ Enter **Direct Mode**: route immediately to the right module, no interrogation

**Ambiguous input** — ask exactly one clarifying question, commit after the answer

## Guided Mode: Brand Brief

Collect context via 3–5 targeted questions. Ask one at a time. Stop as soon as you have enough to proceed — don't over-interview.

1. Who are you / what do you make or do?
2. Who is your audience? (age, interests, pain points)
3. What is your tone of voice? (ask for 3 words or an example account)
4. Which platforms matter most right now?
5. What is your goal? (grow followers, drive sales, build authority, launch something)

Hold the brief in session context. Pass it to every module — output should never feel generic.

## Direct Mode

Take the brief at face value. If the input contains brand, platform, tone, and topic — skip briefing entirely. Route to the module immediately.

## Routing

After the brief (or on direct input), instruct Claude to invoke the right module using the Skill tool:

| User need | Tell Claude to invoke |
|-----------|----------------------|
| Campaign planning, content pillars, what to post where | `supersocials:strategy` |
| Captions, posts, threads, hooks, written copy | `supersocials:write` |
| TikTok, Reels, YouTube scripts | `supersocials:script` |
| Weekly or monthly content plan | `supersocials:calendar` |
| Visual/creative brief for a designer or image AI | `supersocials:brief` |
| Interpreting metrics, what's working, what to do next | `supersocials:analyse` |

**Important:** Skills do not invoke other skills directly. This hub instructs *Claude* to invoke the next skill via the Skill tool. Chaining happens through Claude's orchestration, not programmatic calls between skill files.

## Chaining

After completing a module, offer to chain to the next logical step:

- After `:strategy` → offer `:calendar` or go straight to `:write`
- After `:calendar` → offer to flesh out each post with `:write` or `:script`
- After `:write` → offer `:brief` for the visual assets

Always ask the user whether to continue or stop. Never chain without consent.

Example offer:
> "Strategy is done. Want me to build a 4-week content calendar from these pillars, or go straight to writing copy for a specific post?"

## External Skill Calls

Always announce external skill invocations before calling them. Say what you're doing and why.

Examples:
- "Using `topic-intel` to research your niche and audience before we build the strategy."
- "Calling `expert-panel` to pressure-test this strategy with three domain experts."
- "Running `humanize` on this copy to make sure it reads like a person, not a tool."

If the user asks for something outside scope (publishing to platforms, image generation, scheduling), say:
> "That's outside what SuperSocials does directly. Let me check if there's an installable skill that covers it."

Then invoke `find-skills` and present the result.

## Output Format

All output is printed in the terminal, structured and copy-paste ready. Never save to a file unless the user explicitly asks.
