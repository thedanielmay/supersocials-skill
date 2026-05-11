---
name: calendar
description: Use when planning a weekly or monthly social media content calendar. Produces a post-by-post schedule across platforms with topics, formats, and copy briefs. Part of the SuperSocials suite.
---

# SuperSocials: Calendar

Think like a content manager. Build a structured, executable posting plan.

## What This Module Produces

A weekly or monthly content calendar as a markdown table:

| Date | Platform | Format | Pillar | Topic / Hook | Copy brief |
|------|----------|--------|--------|--------------|------------|
| Mon 13 May | Instagram | Reel | Education | "3 things nobody tells you about X" | Hook on camera, 3 punchy beats, CTA to follow |

## Process

### Step 1: Establish context

If no strategy exists in context, ask:
- How many weeks to plan?
- Which platforms?
- What are the content pillars? (if unknown, offer to run `supersocials:strategy` first)
- How many posts per week per platform?

### Step 2: Build the calendar

Distribute content across pillars evenly. Don't cluster the same pillar on consecutive days. Vary formats within each platform.

**Cadence guidance (if user hasn't specified):**

Do not apply generic cadence defaults. Ask the user:
- How many posts per week are you realistically able to produce?
- Are you starting from scratch or do you have an existing posting rhythm?

Then recommend cadence based on their capacity and account stage:

- **Starting out (0–1K followers):** Lower volume, higher quality — 3x/week max per platform. Consistency beats frequency at this stage.
- **Growth phase (1K–10K):** Increase frequency on platforms where analytics show traction. Use the `topic-intel` skill to check current platform-specific best practices before recommending specific numbers.
- **Established (10K+):** Match or slightly exceed current rhythm. Frequency gains are marginal — optimise for format and quality instead.

Never prescribe daily posting on LinkedIn or high-volume schedules for accounts that don't have the content infrastructure to sustain them.

### Step 3: Deliver the calendar

Output as a markdown table. Include all columns: Date, Platform, Format, Pillar, Topic/Hook, Copy brief.

The "Copy brief" column should give enough direction that a writer (or `:write` module) can execute without asking questions. One sentence minimum.

End with:
> "Want me to write the full copy for any of these posts? I can do them one at a time or work through the whole calendar."

If they say yes to the full calendar, invoke the `supersocials:write` skill (or `supersocials:script` for video posts) for each entry in sequence. Pass the calendar row as context. Number the outputs to match the calendar.
