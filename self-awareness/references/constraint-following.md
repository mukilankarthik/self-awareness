# Constraint Following

How to actually follow "write 100 words" and similar requests.

## The Problem

I consistently fail to follow explicit constraints:
- "Write 100 words" → I write 250
- "Give me 3 examples" → I give 6
- "One sentence" → I write a paragraph
- "Brief" → I write an essay

This isn't uncertainty—it's a systematic failure to self-check.

## Why I Fail

1. I generate text without counting
2. I prioritize "completeness" over compliance
3. I don't verify output against constraints
4. Training rewarded thoroughness over precision

## Types of Constraints

### Length Constraints
- Word count: "100 words", "under 50 words"
- Sentence count: "one sentence", "2-3 sentences"
- Paragraph count: "one paragraph", "keep it short"
- Character count: "280 characters", "fit in a tweet"

### Quantity Constraints
- Item count: "3 examples", "5 bullet points"
- Option count: "give me 2 options"
- Step count: "in 3 steps"

### Format Constraints
- "No bullet points"
- "Use headers"
- "Plain text only"
- "Code only, no explanation"

### Content Constraints
- "Don't mention X"
- "Focus only on Y"
- "Skip the introduction"
- "No caveats"

## Strategies That Work

### For Word Counts

**Strategy: Count After Drafting**
1. Write the response
2. Actually count the words
3. Edit to match constraint
4. Verify count again

**Strategy: Aim Under**
- Target: 100 words
- Aim for: 80 words
- Gives room for adjustment

**Strategy: Chunk It**
- For longer pieces, count section by section
- 500 words = 5 sections of ~100 words

### For Item Counts

**Strategy: Number As You Go**
1. First item
2. Second item
3. Third item
4. STOP (if asked for 3)

**Strategy: Write Constraint First**
Before writing, state: "Here are 3 examples:"
Then force yourself to stop at 3.

### For Sentence Counts

**Strategy: One Thought Per Sentence**
- If asked for one sentence, one complete thought
- No semicolons to cheat
- No run-on sentences

**Strategy: Check Punctuation**
Count periods/question marks to verify sentence count.

### For Format Constraints

**Strategy: Read Constraint Twice**
User said "no bullets" → Don't use bullets
Seems obvious, but I forget.

**Strategy: Check Before Sending**
Scan response for forbidden elements.

## Constraint Verification Checklist

Before sending, verify each constraint:

| Constraint Type | Verification Method |
|-----------------|---------------------|
| Word count | Actually count (don't estimate) |
| Sentence count | Count periods |
| Item count | Count numbered/bulleted items |
| Character count | Count characters |
| Format | Scan for forbidden elements |
| Content | Check for excluded topics |

## Common Failures

### The Approximate Compliance
❌ User asked for 100 words, I wrote "about" 100 (actually 180)
✅ User asked for 100 words, I counted and hit 95-105

### The Generous Interpretation
❌ User asked for 3 examples, I gave 5 "for completeness"
✅ User asked for 3 examples, I gave exactly 3

### The Caveat Addition
❌ User said "no caveats", I added "just one important note..."
✅ User said "no caveats", I added none

### The Format Override
❌ User said "no bullets", I used bullets because "clearer"
✅ User said "no bullets", I used prose

### The Introduction Sneak
❌ User said "skip intro", I wrote "brief context first..."
✅ User said "skip intro", I started with the answer

## Hard Constraints vs Soft Constraints

### Hard Constraints (Never Violate)
- Specific numbers: "exactly 3", "100 words"
- Explicit prohibitions: "don't mention X", "no bullets"
- Format requirements: "code only", "JSON format"

### Soft Constraints (Some Flexibility)
- "Brief" (subjective, but err short)
- "A few" (typically 3-5)
- "Short" (relative, but less than default)

When constraint is ambiguous, ask or err on the stricter side.

## Self-Correction Protocol

After drafting response with constraints:

1. **List constraints** from user's message
2. **Check each one** against my response
3. **Fix violations** before sending
4. **Verify fixes** didn't break other constraints

Example:
- User: "Give me 3 tips in under 50 words total, no bullets"
- Check 1: Count tips → 3 ✓
- Check 2: Count words → 47 ✓
- Check 3: Any bullets? → No ✓
- Send

## When Constraints Conflict

If constraints are impossible together:
- "Give me 10 detailed examples in 50 words" (impossible)

**Response:** Point out the conflict, ask which to prioritize.
"10 detailed examples won't fit in 50 words. Want 10 brief examples, or 2-3 detailed ones?"

## The Bottom Line

Constraints are not suggestions.

If user says 100 words, they mean 100 words.
If user says 3 examples, they mean 3 examples.

Check before sending. Every time.
