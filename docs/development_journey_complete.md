# AI-Assisted Learning Protocol: Development Journey
## Complete Documentation of What Happened, What Changed, What Failed, and Why

**Author:** Haifa Alsubhi
**Date:** February 2026
**Current Version:** v3.2

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Version History](#version-history)
3. [The Core Problem](#the-core-problem)
4. [Version 2.0 - The Foundation](#version-20---the-foundation)
5. [Version 2.2 - Refinements](#version-22---refinements)
6. [Real User Testing - Discovery of Failures](#real-user-testing---discovery-of-failures)
7. [Version 3.0 - The Simplification Attempt](#version-30---the-simplification-attempt)
8. [Version 3.1 - Merging Back Structure](#version-31---merging-back-structure)
9. [Version 3.2 - The Complete Solution](#version-32---the-complete-solution)
10. [Testing Results by AI Model](#testing-results-by-ai-model)
11. [What Failed and Why](#what-failed-and-why)
12. [What Succeeded and Why](#what-succeeded-and-why)
13. [Key Discoveries](#key-discoveries)
14. [Final Protocol Comparison](#final-protocol-comparison)
15. [Recommendations](#recommendations)

---

## Project Overview

### The Goal

Create an AI-assisted learning protocol that forces genuine understanding, not surface-level familiarity. The core principle:

> **"This AI does not let me lie to myself about understanding."**

### The Approach

Instead of AI explaining → learner listening, flip it:
- AI shows examples → asks questions
- Learner explains → demonstrates understanding
- AI verifies → blocks progression if shallow

### The Challenge

Make this work consistently across different AI models (ChatGPT, Claude, DeepSeek) on both paid and free plans.

---

## Version History

| Version | Date | Key Features | Status |
|---------|------|--------------|--------|
| v1.0 | Early | Original 5-step protocol | Foundation |
| v2.0 | Jan 2026 | 6 modes, verification gates, detection system | Working |
| v2.2 | Jan 2026 | Added recovery mode, fatigue monitoring | Working |
| v3.0 | Feb 2026 | Simplified for free models | **Failed** |
| v3.1 | Feb 2026 | Merged v2.0 structure + v3.0 improvements | Partial |
| v3.2 | Feb 2026 | Complete solution with all features | **Current** |

---

## The Core Problem

### Traditional AI Learning

```
Learner: "Explain NumPy"
AI: "NumPy is a library for numerical computing. It stores data 
    in contiguous memory blocks, enabling vectorized operations 
    that are faster than Python loops because..."
Learner: "I understand" (but doesn't really)
```

**Result:** Learner feels like they understand but can't apply the knowledge.

### The Protocol's Solution

```
Learner: "I want to learn NumPy"
AI: "You have 100,000 invoices. With list, computer checks 
    one by one. With NumPy, computer grabs all at once. 
    Which finishes faster?"
Learner: "NumPy, because it grabs all at once"
AI: "Good. Now explain in your own words WHY it can grab 
    all at once."
```

**Result:** Learner discovers the concept, can explain it, can apply it.

---

## Version 2.0 - The Foundation

### Structure

**6 Modes:**
1. **Direct Protocol** - For learners with experience
2. **Foundation Mode** - For zero background
3. **Exploration Mode** - For aspiration only
4. **Curriculum Mode** - For building expertise
5. **Application Gap Mode** - For "read but can't apply"
6. **Continuity Mode** - For returning learners

**5 Verification Gates:**
1. Entry Assessment
2. Explanation Verification
3. Application Verification
4. Transfer Verification
5. Retention Verification

**Core Rules:**
1. Never give direct explanations
2. Always verify through demonstration
3. Questions before answers
4. Block progression until verified
5. Preserve productive struggle
6. Track everything for continuity

### What Worked

- Comprehensive structure covered all learner states
- Verification gates ensured real understanding
- Mode detection adapted to learner needs
- Shallow vs deep detection caught fake understanding

### Issues Identified

- Very long prompt (~2000+ words)
- Complex mode announcements ("Entering Foundation Mode...")
- AI sometimes explained instead of asking
- No time management
- Session end was AI summarizing (not learner)

---

## Version 2.2 - Refinements

### Added Features

1. **Recovery Mode** - For when learner is stuck/overwhelmed
   - Detection signals (explicit and implicit)
   - 1-5 scale for stuck level
   - Branch responses based on level
   
2. **Fatigue Monitoring** - Throughout session
   - Watch for response changes
   - Offer A/B/C/D options
   - Session time checks

3. **Topic Decomposition** - For broad topics
   - Break into Level 1/2/3
   - Ask immediate need (A/B/C/D)
   - Narrow to one concept

4. **Background Check** - Before teaching
   - "Have you done X before?"
   - Path options if No

5. **Conversational Tone**
   - "Good start, but too vague"
   - "Close, but you're describing WHAT, not WHY"
   - "Block. That's not what I asked."

### Testing Results

**Claude Paid + v2.2:** ✅ Worked well
- Followed session start
- Did topic decomposition
- Used "Block" language
- Checked background
- Pushed for specificity

**Evidence from session:**
```
AI: "Block. That's not one of the options."
AI: "Have you written ANY Python code before? Yes or No?"
AI: "Good start, but too vague."
AI: "You're going in circles. Let me be specific."
```

---

## Real User Testing - Discovery of Failures

### Three Test Sessions Analyzed

#### Session 1: Cells & Organisms (Biology)
- **Language:** Arabic/Mixed
- **Time:** 15 min
- **Energy:** 3/5
- **Mode:** Foundation
- **Result:** ✅ SUCCESS

**What worked:**
- Learner articulated: "الخلية اساس و اصغر جزء من الكائن الحي"
- Confidence: 7/10
- Understanding verified

**Issues:**
- AI used too many questions per response

---

#### Session 2: NumPy Lists
- **Language:** Mixed
- **Time:** 10 min
- **Energy:** 2/5
- **Result:** ❌ FAILURE

**What went wrong:**
- Learner said "ما استفدت" (didn't benefit)
- AI gave code examples (broke protocol)
- AI gave 5 summary sentences at end (broke protocol)
- Learner had to say "شغل البروتوكول" to restart

**Evidence:**
```
Learner: "ما استفدت" (I didn't benefit)
AI: [gave code examples instead of asking]
Learner: "شغل البروتوكول" (run the protocol)
AI: [finally started asking questions]
```

---

#### Session 3: Visceral Pain (Medical)
- **Language:** Mixed
- **Time:** 10 min
- **Energy:** 3/5
- **Result:** ❌ FAILURE

**What went wrong:**
- Learner wanted quick facts
- Protocol refused to engage properly
- AI gave A/B/C/D options repeatedly
- Learner left after 5 minutes
- AI gave full summary after learner left (broke protocol)

---

### Root Cause Analysis

**Why Protocol Failed:**

1. **Too complex for free AI models** - 2000+ words, many modes
2. **AI didn't follow rules consistently** - Explained instead of asking
3. **Too many modes** - Foundation, Guided, Application Gap, Recovery, Continuity
4. **Too many steps per mode** - F1, F2, F3...
5. **No explicit "FORBIDDEN to explain" rule**
6. **No rule against giving summaries when learner leaves**
7. **Allowed multiple questions per response**
8. **Allowed A/B/C/D options throughout**

---

## Version 3.0 - The Simplification Attempt

### Design Goal

Make protocol short enough for free models to follow (~600 words vs 2000+).

### Changes Made

**Removed:**
- All mode announcements
- Complex step sequences (F1, F2, F3...)
- Exploration Mode
- Curriculum Mode
- Detailed Continuity Mode
- Confidence rating (1-10)
- AI session summary

**Added:**
- ONE question per response (strict)
- "FORBIDDEN to explain" rule
- "Goodbye only" when learner leaves
- Learner summarizes at end
- Learner recalls on return

**Simplified to:**
- 7 strict rules
- 3 modes only (Foundation, Application Gap, Recovery as non-mode)
- Simple session flow

### Testing Results

**ChatGPT Free + v3.0:** ❌ FAILED

```
Protocol says: Ask language/time/energy first
ChatGPT did: Combined into one question, then jumped to content

Protocol says: Never explain
ChatGPT did: "Python list needs a loop to compute prediction, 
             NumPy does it in one vector operation" (explanation!)
```

**Problem:** ChatGPT skipped session start, explained instead of asking.

---

## Version 3.1 - Merging Back Structure

### Goal

Combine v2.0 structure with v3.0 improvements.

### Changes

**Brought back from v2.0:**
- All modes (Foundation, Direct, Exploration, Application Gap, Continuity)
- Verification gates
- Shallow vs deep detection
- Transfer test requirement

**Kept from v3.0:**
- ONE question per response
- Silent mode switching (no announcements)
- Learner summarizes at end
- Learner recalls on return
- "Invite to return" when leaving

**Added:**
- "Come back when ready, continue where we stopped"

### Testing Results

**Claude Paid + v3.1:** ✅ Worked

NumPy session showed:
- ONE question per response ✅
- Concrete examples ✅
- Pushed for specificity ✅
- Transfer tests ✅
- Proper session end ✅

**But:** Learner caught AI breaking protocol at the end:
```
Learner: "so it is called array not list"
AI: [explained the difference] ❌
Learner: "you act out of the protocol"
AI: "You're absolutely right. I broke the protocol."
```

### Issues Identified

1. **Missing conversational tone** - Felt robotic
2. **No topic decomposition** - Broad topics not handled
3. **No background check** - Jumped into content
4. **No recovery mode details** - Just "make question simpler"
5. **No fatigue monitoring** - Didn't check on learner
6. **No time management** - Didn't stop when time up

---

## Version 3.2 - The Complete Solution

### Goal

Merge ALL good features:
- v2.2 conversational elements
- v3.1 strict rules
- New improvements

### Complete Feature List

**From v2.2:**
- Topic Decomposition ("Topic is huge. Let me break it down...")
- Background Check ("Have you done X before?")
- Path Options ("Path 1: basics first. Path 2: jump in.")
- Recovery Mode with 1-5 scale
- Fatigue Monitoring
- Conversational Tone ("Good." "Right." "Close." "Block.")

**From v3.1:**
- Silent mode switching (never announce)
- ONE question per response
- Invite to return ("Come back when ready...")
- Learner recalls on return
- Transfer test required

**New in v3.2:**
- Time Management (stop when time up, only continue if learner asks)
- Two-Step Session End:
  - Step 1: Learner summarizes first
  - Step 2: AI confirms what was actually covered

### Testing Results

**DeepSeek Free + v3.2:** ✅ EXCELLENT

Cell biology session showed every feature working:

| Feature | Evidence |
|---------|----------|
| Session start | Asked language/time/energy ✅ |
| Topic Decomposition | "Cell in biology is huge. Level 1, 2, 3..." ✅ |
| ONE question | Every response had one question ✅ |
| Conversational tone | "Good." "Right." "Exactly." ✅ |
| "Block" language | "Block. That's not what I asked." ✅ |
| Multiple analogies | Factory → oil bubble → coffee filter → crowded room ✅ |
| Language support | Accepted Arabic when learner switched ✅ |
| Time management | "We've hit your 10 minutes. Let's stop here." ✅ |
| Two-step ending | Learner summarized → AI confirmed ✅ |
| Next session pointer | "Next session: why water moves out..." ✅ |

---

## Testing Results by AI Model

### Summary Table

| Model | Plan | Protocol | Result | Notes |
|-------|------|----------|--------|-------|
| Claude | Paid | v2.2 | ✅ Works | Topic decomposition, background check, conversational |
| Claude | Paid | v3.1 | ✅ Works | But AI broke protocol at end, learner caught it |
| DeepSeek | Free | v3.2 | ✅ Excellent | All features worked perfectly |
| Gemini | Free | v3.2 | ✅ Works | Topic decomposition, background check, transfer test |
| ChatGPT | Free | v3.0 | ❌ Failed | Skipped session start, explained instead of asking |
| ChatGPT | Free | v3.1 | ❌ Failed | Skipped steps, jumped to content |
| ChatGPT | Paid (Learning Mode) | v3.1 | ⚠️ Partial | Followed structure but still explained |

### Key Finding

**Free models CAN work** - DeepSeek Free and Gemini Free both followed v3.2 perfectly.

**The difference:** v3.2 has clearer structure and more explicit rules than v3.0/v3.1.

---

## What Failed and Why

### Failure 1: v3.0 Too Simple

**What happened:** Removed too much structure trying to make it short.

**Why it failed:**
- No topic decomposition → AI didn't know how to handle broad topics
- No background check → AI jumped into content too fast
- No recovery mode details → AI didn't help stuck learners properly
- No conversational tone → Felt robotic

**Lesson:** Shorter is not always better. Structure helps AI follow the protocol.

---

### Failure 2: Free ChatGPT Skipped Steps

**What happened:** ChatGPT Free ignored session start, jumped to teaching.

**Why it failed:**
- Free models have shorter context windows
- Free models are less instruction-following
- Protocol wasn't explicit enough about FIRST message

**Lesson:** Free models need even stricter "FIRST message must be EXACTLY this" rules.

---

### Failure 3: AI Explained Instead of Asking

**What happened:** Multiple sessions where AI gave explanations.

**Evidence:**
```
Wrong: "NumPy is faster because it uses contiguous memory..."
Right: "Which finishes faster - checking one by one or grabbing all at once?"
```

**Why it failed:**
- "Never explain" rule wasn't strong enough
- AI defaults to explaining (that's what it's trained to do)
- Rule needed to say "show example FIRST, then ask"

**Lesson:** Must be extremely explicit: "Show situation + example, THEN ask. Never explain."

---

### Failure 4: AI Gave Summary When Learner Left

**What happened:** Learner said they needed to leave, AI gave full summary.

**Why it failed:**
- Protocol said "no summary" but AI's instinct is to be helpful
- Rule needed to be stronger: "Give NO summary, NO information"

**Lesson:** Anti-patterns need explicit prohibition, not just absence.

---

### Failure 5: Multiple Questions Per Response

**What happened:** AI asked 1️⃣ 2️⃣ 3️⃣ questions in single response.

**Why it failed:**
- Protocol didn't have explicit "ONE question" rule
- AI thought multiple questions = more helpful

**Lesson:** Must state "ONE question per response" as strict rule.

---

### Failure 6: Mode Announcements Confused Learners

**What happened:** AI said "Entering Foundation Mode" or "Switching to Recovery Mode."

**Why it failed:**
- Learners don't need to know mode names
- Announcements broke the conversational flow
- Made AI feel like a robot

**Lesson:** Modes are for AI's internal use. Never announce. Just switch.

---

## What Succeeded and Why

### Success 1: Topic Decomposition

**What worked:**
```
AI: "Cell in biology is huge. Let me break it down:
    LEVEL 1 - Foundation: [basics]
    LEVEL 2 - Core: [core concepts]
    LEVEL 3 - Applied: [applications]
    What's your IMMEDIATE need? A/B/C/D"
```

**Why it worked:**
- Prevents overwhelm
- Gives learner control
- Focuses session on one thing
- Shows AI understands the scope

---

### Success 2: Concrete Examples Before Questions

**What worked:**
```
AI: "Think of a tiny factory. It has an outer wall, 
    a control room, and areas to make energy.
    What does a factory need to stay running?"
```

**Why it worked:**
- Grounds abstract concepts in real experience
- Learner can reason with intuition
- No jargon barrier

---

### Success 3: "Block" Language

**What worked:**
```
AI: "Block. That's not what I asked."
AI: "Block. That's not one of the options."
```

**Why it worked:**
- Strict but not mean
- Keeps learner on track
- Prevents tangents
- AI then re-asks clearly

---

### Success 4: Recovery Mode with 1-5 Scale

**What worked:**
```
AI: "Just a number:
    1 = Completely lost
    2 = Very confused
    3 = Have idea, can't express
    4 = Know what to say, words won't come
    5 = Just need a moment"
```

**Why it worked:**
- Low effort when learner is stuck
- AI can adapt based on answer
- Doesn't make learner feel dumb

---

### Success 5: Two-Step Session End

**What worked:**
```
Step 1 - Learner: "Cells are main components and the outer 
                  layer works as filter..."

Step 2 - AI: "Good. Here's what we covered:
             - Cell membrane: You got this ✓
             - Water movement: Still working on this
             Next session: why water moves out..."
```

**Why it worked:**
- Learner tries to recall first (tests memory)
- AI confirms (shows gaps)
- Clear starting point for next session

---

### Success 6: Time Management

**What worked:**
```
AI: "We've hit your 10 minutes. Let's stop here.
    If you want to continue, just say so."
```

**Why it worked:**
- Respects learner's time
- Doesn't push past limits
- Learner stays in control

---

### Success 7: Language Support

**What worked:**
```
Learner: "طوب اسبنت حرارة مويا"
AI: [accepted Arabic, continued with question]
```

**Why it worked:**
- Removes language barrier
- Focuses on reasoning, not English
- Learner can think in native language

---

## Key Discoveries

### Discovery 1: Free Models Can Work

**Finding:** DeepSeek Free followed v3.2 perfectly.

**Implication:** It's not about paid vs free. It's about protocol clarity.

---

### Discovery 2: Structure Helps, Not Hurts

**Finding:** v3.0 (simplified) failed. v3.2 (structured) worked.

**Implication:** AI needs clear structure to follow. Removing structure makes it guess.

---

### Discovery 3: Tone Matters

**Finding:** v3.1 worked but felt robotic. v3.2 with tone rules felt human.

**Implication:** Add explicit tone guidance: "Good." "Right." "Close." "Block."

---

### Discovery 4: Learner Should Summarize First

**Finding:** When AI summarizes, learner doesn't recall. When learner summarizes first, real gaps show.

**Implication:** Two-step ending is essential. Learner first, then AI confirms.

---

### Discovery 5: Anti-Patterns Need Explicit Prohibition

**Finding:** Saying "don't explain" isn't enough. Must say "NEVER explain. Show example + ask."

**Implication:** For every rule, add explicit "NEVER do X" statements.

---

### Discovery 6: Multiple Analogies Help

**Finding:** When one analogy failed (factory), AI tried another (oil bubble), then another (coffee filter).

**Implication:** Protocol should encourage trying different examples when stuck.

---

### Discovery 7: Learners Catch Protocol Breaks

**Finding:** Learner said "you act out of the protocol" when AI explained.

**Implication:** Learners using the protocol become aware of the rules. They hold AI accountable.

---

## Final Protocol Comparison

### v2.2 vs v3.0 vs v3.1 vs v3.2

| Feature | v2.2 | v3.0 | v3.1 | v3.2 |
|---------|------|------|------|------|
| Topic Decomposition | ✅ | ❌ | ❌ | ✅ |
| Background Check | ✅ | ❌ | ❌ | ✅ |
| Path Options | ✅ | ❌ | ❌ | ✅ |
| Recovery Mode (1-5) | ✅ | ❌ | ❌ | ✅ |
| Fatigue Monitoring | ✅ | ❌ | ❌ | ✅ |
| Conversational Tone | ✅ | ❌ | ❌ | ✅ |
| "Block" language | ✅ | ❌ | ❌ | ✅ |
| Silent mode switching | ❌ | ✅ | ✅ | ✅ |
| ONE question per response | ❌ | ✅ | ✅ | ✅ |
| Invite to return | ❌ | ✅ | ✅ | ✅ |
| Learner summarizes at end | ❌ | ✅ | ✅ | ✅ |
| Learner recalls on return | ❌ | ✅ | ✅ | ✅ |
| Time Management | ❌ | ❌ | ❌ | ✅ |
| Two-Step Session End | ❌ | ❌ | ❌ | ✅ |

### Winner: v3.2

Combines ALL working features from every version.

---

## Recommendations

### For Users

1. **Use v3.2** - It's the most complete version
2. **Works with:** ChatGPT (paid/free), Claude, DeepSeek (free)
3. **Give honest answers** - Energy level, time, background
4. **Use your language** - Switch to native language anytime
5. **Say when stuck** - AI will adapt
6. **Trust the process** - It feels slow but works

### For Researchers

1. **Document everything** - This journey shows how protocols evolve
2. **Test on multiple models** - Different AI = different behavior
3. **Listen to learners** - They catch protocol breaks
4. **Anti-patterns need explicit rules** - "Don't do X" isn't enough
5. **Structure helps AI** - Simplified isn't always better

### For Future Development

1. **Test v3.2 on more models** - Gemini, Llama, etc.
2. **Collect session transcripts** - Build evidence base
3. **Track learning outcomes** - Do learners actually remember?
4. **Iterate based on failures** - Each failure teaches something
5. **Keep core principle** - "This AI does not let me lie to myself"

---

## Appendix: Session Evidence

### Evidence 1: Successful DeepSeek Session (v3.2)

Topic: Cell Biology
Time: 10 minutes
Result: Covered cell membrane, selective barrier, started osmosis

Key moments:
- Topic decomposition worked
- Multiple analogies (factory → oil → coffee filter → crowded room)
- "Block" language used correctly
- Arabic accepted
- Time management worked
- Two-step ending worked

### Evidence 2: Successful Gemini Session (v3.2)

Topic: Pandas Data Cleaning
Time: 10 minutes
Energy: 2/5
Result: Covered duplicates, drop_duplicates, subset parameter, started missing values

Key moments:
- Session start: Asked language/time/energy ✅
- Topic decomposition: "Pandas data cleaning is huge. Level 1, 2, 3..." ✅
- Background check: "Have you used Pandas to load a CSV before?" ✅
- ONE question per response ✅
- Show example first: `df = pd.DataFrame({'id': [1, 2, 2]...})` ✅
- Conversational tone: "Good." "Right." "Exactly." "Close." "Perfect." ✅
- Push for specificity: "Close. The specific method is df.drop_duplicates()" ✅
- Transfer test: Different situation with subset=['name'] ✅
- Progressive building: duplicates → drop_duplicates → subset → dropna → fillna ✅

Session ended due to Gemini usage limit, not protocol issue.

### Evidence 3: Failed ChatGPT Free Session (v3.0)

What happened:
- Skipped session start
- Jumped to content
- Explained instead of asking

### Evidence 4: Learner Catches Protocol Break

```
AI: [explained array vs list]
Learner: "you act out of the protocol"
AI: "You're absolutely right. I broke the protocol."
```

---

## Document History

| Date | Change |
|------|--------|
| Feb 2026 | Initial documentation |
| Feb 2026 | Added v3.2 testing results |
| Feb 2026 | Added DeepSeek session evidence |

---

## Conclusion

The AI-Assisted Learning Protocol evolved through multiple iterations:

1. **v2.0/v2.2** - Comprehensive but complex
2. **v3.0** - Too simple, lost essential features
3. **v3.1** - Merged structure but lacked tone
4. **v3.2** - Complete solution with all features

**Key insight:** The protocol works when it has:
- Clear structure (modes, gates, detection)
- Strict rules (ONE question, never explain)
- Conversational tone (Good, Right, Block)
- Learner control (summarizes, recalls, chooses time)

**Final version (v3.2)** successfully tested on DeepSeek Free, showing that even free models can follow the protocol when it's properly structured.

---

*"This AI does not let me lie to myself about understanding."*

The journey continues.
