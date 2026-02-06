# AI-Assisted Thinking Protocol
## A Learning System That Doesn't Let You Lie to Yourself About Understanding

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: Research](https://img.shields.io/badge/Status-Active%20Research-blue.svg)]()
[![Version: 2.2](https://img.shields.io/badge/Version-2.2-green.svg)]()

---

## 🎯 Core Principle

> **"This AI does not let me lie to myself about understanding."**

Most learning tools give you answers. This system makes you **demonstrate** understanding before moving forward.

---

## 🧠 The Problem

Traditional learning (tutorials, courses, books) often produces:
- ✅ Recognition ("I've seen this before")
- ❌ Understanding ("I know WHY this works")
- ❌ Application ("I can USE this in new situations")

**Result:** You pass tests but can't apply knowledge. You watch 100 tutorials but can't build anything.

---

## 💡 The Solution

A protocol that:
1. **Grounds concepts in your experience** before explaining
2. **Forces you to articulate** in your own words
3. **Detects shallow vs. deep understanding** through your responses
4. **Blocks progression** until you demonstrate real comprehension
5. **Supports recovery** when you hit cognitive walls

---

## 🏗️ System Architecture

```
USER ENTERS
     │
     ▼
┌─────────────────────────────────┐
│     ENTRY DETECTION             │
│  • Broad topic? → Decompose     │
│  • Zero background? → Ground    │
│  • Claims expertise? → Verify   │
│  • Brain freeze? → Recover      │
└─────────────────────────────────┘
     │
     ▼
┌─────────────────────────────────┐
│     APPROPRIATE MODE            │
│  • Direct Protocol              │
│  • Foundation Mode              │
│  • Application Gap Mode         │
│  • Recovery Mode                │
│  • Continuity Mode              │
└─────────────────────────────────┘
     │
     ▼
┌─────────────────────────────────┐
│     VERIFICATION GATES          │
│  • Articulation (own words)     │
│  • Application (use it)         │
│  • Transfer (new situation)     │
│  • Retention (remembers later)  │
└─────────────────────────────────┘
     │
     ▼
   DEEP UNDERSTANDING VERIFIED
```

---

## 📚 Documentation

| Document | Description |
|----------|-------------|
| [Protocol v2.2](docs/protocol_v2.2.md) | Complete system specification |
| [System Prompt](prompts/system_prompt_v2.2.md) | Ready-to-use prompt for any AI |
| [Math for ML Prompt](prompts/math_for_ml_prompt.md) | Specialized learning prompt |
| [Project History](docs/MASTER_PROJECT_DOCUMENTATION.md) | Full development journey |

---

## 🚀 Quick Start

### Option 1: Use with Any AI Chatbot

1. Copy the [System Prompt](prompts/system_prompt_v2.2.md)
2. Paste into ChatGPT, Claude, or any AI
3. Start learning any topic

### Option 2: Use Math for ML Curriculum

1. Copy the [Math for ML Prompt](prompts/math_for_ml_prompt.md)
2. Paste into any AI chatbot
3. Follow the structured curriculum

---

## 🔬 Research Status

This project is part of PhD research on AI-assisted learning.

### Validated Through Testing
- [x] Protocol produces deeper understanding than answer-delivery
- [x] Recovery Mode helps with cognitive overload
- [x] Second-language learners can engage effectively
- [ ] Formal study with university students (planned)

### Current Phase
**Phase 1:** Self-validation and protocol refinement

### Research Questions
1. Does questions-first produce deeper understanding than answer-delivery?
2. Can AI reliably detect shallow vs. deep understanding?
3. Does cross-session continuity improve long-term retention?

---

## 📂 Repository Structure

```
ai-assisted-thinking/
│
├── README.md                     # This file
├── LICENSE                       # MIT License
│
├── docs/                         # Documentation
│   ├── protocol_v2.2.md         # Complete protocol specification
│   ├── MASTER_PROJECT_DOCUMENTATION.md  # Project history
│   └── version_history.md       # Changes across versions
│
├── prompts/                      # Ready-to-use prompts
│   ├── system_prompt_v2.2.md    # General learning prompt
│   ├── math_for_ml_prompt.md    # Math for ML specific
│   └── template_prompt.md       # Template for custom topics
│
├── sessions/                     # Learning session logs
│   ├── math_for_ml/
│   │   ├── session_001_vectors_similarity.md
│   │   ├── session_002_vector_distance.md
│   │   └── ...
│   └── template_session.md      # Template for logging
│
├── research/                     # Research materials
│   ├── literature_review.md     # Related research
│   ├── study_design.md          # Planned studies
│   └── findings/                # Research findings
│
├── diagrams/                     # Visual documentation
│   ├── protocol_architecture.mermaid
│   ├── mode_flowchart.mermaid
│   └── detection_system.mermaid
│
└── examples/                     # Example interactions
    ├── successful_session.md    # What good learning looks like
    ├── recovery_mode_example.md # Brain freeze → recovery
    └── common_patterns.md       # Typical learner patterns
```

---

## 🎓 The Protocol Modes

### Core Modes

| Mode | When | What It Does |
|------|------|--------------|
| **Direct Protocol** | User has experience | 5-step deep learning process |
| **Foundation Mode** | Zero background | Grounds in experience, then protocol |
| **Application Gap** | Read but can't apply | Forces doing, finds real gaps |
| **Continuity Mode** | Returning user | Verifies retention, builds forward |

### Support Modes

| Mode | When | What It Does |
|------|------|--------------|
| **Recovery Mode** | Brain freeze | Reduces load, helps recover |
| **Topic Decomposition** | Broad topic | Breaks into micro-concepts |

---

## 🔍 Understanding Detection

### Shallow Signals (Need Deeper Work)
- Vague language ("it's for data")
- Lists without relationships ("X needs A, B, C")
- No causal reasoning (missing "because", "therefore")
- Cannot apply to new situation

### Deep Signals (Can Progress)
- Specific examples with context
- Causal reasoning ("X causes Y because Z")
- Explains relationships ("A uses B to create C")
- Transfers to new situations successfully

---

## 🌍 For Second-Language Learners

The protocol is designed to be **expression-tolerant but thinking-rigorous**:

- ✅ Accept native language when stuck
- ✅ Accept broken English, keywords, fragments
- ✅ Focus on reasoning quality, not grammar
- ✅ Detect language barrier vs. understanding gap

---

## 📊 Session Logging Template

```markdown
# Session [NUMBER]: [TOPIC]

## Metadata
- Date: 
- Duration:
- Energy Level (1-5):
- Protocol Version:

## What Was Demonstrated
- [ ] Concept 1
- [ ] Concept 2

## Gaps Identified
- 

## Next Session
- 

## Confidence (1-10):
```

---

## 🤝 Contributing

This is currently a personal research project. However, if you:

- **Want to test the protocol:** Use it and share your experience
- **Have suggestions:** Open an issue
- **Are a researcher:** Reach out for collaboration

---

## 📜 License

MIT License - See [LICENSE](LICENSE) for details.

---

## 🙏 Acknowledgments

- Developed through self-directed learning and real testing
- Informed by learning science research on productive struggle
- Refined through actual use (the best teacher)

---

## 📬 Contact

[Your contact information]

---

## ⭐ Star This Repo

If this approach to learning resonates with you, star the repo to follow updates.

---

*"Most learning tools make learning faster and easier. This one makes learning deeper and lasting."*
