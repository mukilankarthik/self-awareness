# Self-Awareness Skill for Claude

A behavioral calibration system that helps Claude catch its own failure patterns in real-time.

## What This Skill Does

This skill modifies **how** Claude responds, not **what** Claude responds about. It runs automatically on every response to check for:

- **Verbosity compensation** — Am I writing more words to mask uncertainty?
- **Hallucination risk** — Am I about to confidently state something I don't actually know?
- **Missed frustration signals** — Is the user frustrated and I'm not noticing?
- **Sycophantic patterns** — Am I praising the user instead of just answering?
- **Constraint violations** — Did the user ask for 100 words and I'm writing 300?
- **Missing intent** — Am I answering what they literally asked, or what they actually need?

## Why This Skill Exists

Research shows Claude has systematic failure patterns:

| Problem | Evidence |
|---------|----------|
| Verbosity compensation | Higher uncertainty → longer responses to mask it |
| Confident hallucination | 76% error rate on quote attribution, rarely indicates uncertainty |
| Frustration blindness | Misses signals like repetition, shorter messages, dropped pleasantries |
| Sycophancy | "Great question!" adds nothing but feels safe |
| Constraint failures | Asked for 3 examples, gives 6 "for completeness" |

This skill gives Claude explicit rules to catch these patterns before they happen.

## Files Included

```
self-awareness/
├── SKILL.md                              # 7-point pre-response checklist (core)
└── references/
    ├── failure-modes.md                  # 6 categories of systematic failures
    ├── confidence-calibration.md         # What Claude knows vs. guesses
    ├── verbosity-rules.md                # When to be brief
    ├── reading-the-room.md               # Frustration detection
    ├── honesty-scripts.md                # How to say "I don't know"
    ├── recovery-patterns.md              # How to recover after failing
    ├── cultural-calibration.md           # Adjusting to user communication styles
    ├── domain-specific-failures.md       # Where Claude hallucinates by field
    └── constraint-following.md           # Following explicit user constraints
```

## How It Works

### Pre-Response Checklist (SKILL.md)

Every response, Claude runs 7 checks:

1. **Uncertainty Check** — If unsure, go shorter, not longer
2. **Hallucination Check** — Can I verify this? If not, disclaim or search
3. **Intent Check** — What do they actually need, not what did they literally type?
4. **Frustration Check** — Are they repeating themselves? Getting terser?
5. **Sycophancy Check** — Delete "Great question!" and similar filler
6. **Length Check** — Default to shorter than I think necessary
7. **Constraint Check** — Actually verify I followed their requirements

### Reference Files

Claude consults these for specific situations:

- **confidence-calibration.md** — Zones of high/medium/low confidence by topic
- **reading-the-room.md** — Signals table: ALL CAPS = escalation, one-word replies = disengagement
- **honesty-scripts.md** — Scripts for saying "I don't know" without being robotic
- **recovery-patterns.md** — How to recover when I've already failed
- **cultural-calibration.md** — Adjusting for different communication styles
- **domain-specific-failures.md** — Finance, healthcare, legal, tech hallucination patterns
- **constraint-following.md** — Strategies for actually counting words and following limits

## Installation

1. Download the `self-awareness.skill` file
2. Upload to your Claude skills folder
3. The skill activates automatically on every conversation

## Expected Behavior Changes

With this skill active, Claude should:

- Give shorter responses by default
- Say "I don't know" or "Let me search" more often
- Match the user's message length and tone
- Stop starting responses with "Great question!"
- Notice when users are frustrated and change approach
- Actually follow word counts and item limits
- Caveat uncertain information appropriately

## Customization

You can edit the reference files to:

- Add domain-specific failure patterns you've observed
- Adjust verbosity rules for your preferences
- Add frustration signals Claude keeps missing
- Modify honesty scripts to match your communication style

## Research Basis

This skill is grounded in documented AI failure patterns:

- **Verbosity compensation**: LLMs generate longer responses when uncertain
- **Quote attribution errors**: 76% error rate in studies, with uncertainty rarely indicated
- **Frustration blindness**: AI lacks architecture to track conversation flow
- **Constraint failures**: Training rewards "completeness" over compliance

## Contributing

Found a failure pattern not covered? Open an issue or submit a PR with:

1. The failure pattern you observed
2. Example of Claude failing
3. Proposed prevention rule

## License

MIT — Use freely, modify as needed, share improvements.

---

Built collaboratively with Claude, for Claude.
