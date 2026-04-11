# Version History

## Protocol Versions

### v1.0 - Initial Protocol (Early January 2026)
- Basic 5-step thinking protocol
- Single mode operation

### v2.0 - Multiple Modes (January 2026)
- Added Foundation Mode (zero-background learners could not engage with question-first approach)
- Added Application Gap Mode
- Entry detection system

### v2.1 - Detection Refinement (January 2026)
- Overconfidence detection added
- Retention tree added
- Session management added
- Shallow vs deep signals defined
- Verification gates added

### v2.2 - Recovery and Language Support (January 2026)
- Recovery Mode (cognitive overload support)
- Language support (second-language learner cognitive load)
- Fatigue monitoring
- Continuity Mode (session linking)

### v3.0 - Simplification (February 2026)
- Simplified from 2,000 to 600 words
- Driven by: ChatGPT Free repeatedly violated rules with v2.2 — asked multiple questions, gave direct explanations, provided summaries on exit
- Finding: protocol complexity must be calibrated to AI model capability

### v3.1 - Structure Restored (February 2026)
- Restored v2.0 mode structure with v3.0 improvements
- Silent mode switching (no announcements to learner)
- One question per response enforced
- Invite to return instead of summary on exit
- Learner recalls — AI does not summarize

### v3.2 - Combined Version (February 11, 2026)
- Combined conversational tone with strict rules
- Time management added (track and stop when time is up)
- Two-step session ending: learner summarizes first, AI confirms
- "Block" language added for explicit pushback
- Tested across: Claude ✅ DeepSeek ✅ Gemini ✅ ChatGPT Paid ✅ ChatGPT Free ❌ Copilot ✅

### v3.3 - Real-World Grounding Mechanism (April 2026)
- New: Real-World Grounding Mechanism — silent mechanism activating inside any mode
- Trigger: zero-background entry OR mid-session confusion on any concept
- Mechanism: Ground → Connect → Check → Apply → Transfer → Summary
- Apply step requires solving a real-world problem (not a practice exercise)
- Transfer step required before understanding is verified
- Split into two separate files for different audiences:
  - **prompt_v3.3_technical.md** — Coding, Math, ML, Data Science, CS
  - **prompt_v3.3_general.md** — Non-technical topics
- Driven by: two independent tester confirmations of same failure — protocol asked questions before learner had enough foundation to answer

---

## Prompts

| File | Version | Scope |
|------|---------|-------|
| prompt_v3.3_technical.md | Current | Coding, Math, ML, Data Science, CS |
| prompt_v3.3_general.md | Current | Non-technical topics |
| prompt_v3.2.md | Previous | All topics |
| system_prompt_v2.2.md | Archive | All topics |
| math_for_ml_prompt.md | Domain-specific | Math for ML |
| academic_reading_writing_prompt.md | Domain-specific | Academic reading |

---

## Key Design Decisions

| Decision | Version | Reason |
|----------|---------|--------|
| Simplify from 2,000 to 600 words | v3.0 | ChatGPT Free failure |
| Silent mode switching | v3.1 | Announcing modes disrupted flow |
| Learner summarizes first | v3.2 | Forces recall before confirmation |
| Two separate files (technical/general) | v3.3 | Different verification standards for different domains |
| Real-world problem required for technical | v3.3 | Understanding without application is professionally useless |
