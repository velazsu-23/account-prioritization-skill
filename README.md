# Account prioritization skill

A Claude skill that segments, scores (High/Medium/Low) and groups a B2B target-account list into five go-to-market groups: Win-Back Now, Close the Gap, Net New, Nurture and Set Aside.

It is rule-based on purpose: every account lands where the rules say, with a one-line reason, so sales and leadership can predict and trust the output. See [`account-prioritization/SKILL.md`](account-prioritization/SKILL.md) for the full method.

## Install

**Claude Code:** copy the skill folder into your skills directory.

```bash
git clone https://github.com/velazsu-23/account-prioritization-skill.git
cp -R account-prioritization-skill/account-prioritization ~/.claude/skills/
```

**Claude.ai / Claude desktop:** zip the `account-prioritization` folder and upload it under Settings → Capabilities → Skills.

## Use

Share an account list (CRM export, ABM target list or spreadsheet) and ask Claude to prioritize, tier or segment it. The skill adds four columns, Score, Why, Group and Segment, and leaves the original columns untouched.
