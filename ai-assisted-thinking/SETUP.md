# Repository Structure Setup

## Folder Structure

Create these folders in your GitHub repository:

```
ai-assisted-thinking/
│
├── docs/                         # Documentation
├── prompts/                      # Ready-to-use prompts  
├── sessions/                     # Learning session logs
│   └── math_for_ml/             # Math for ML sessions
├── research/                     # Research materials
│   └── findings/                # Research findings
├── diagrams/                     # Visual documentation
└── examples/                     # Example interactions
```

## Commands to Create Structure

```bash
# Create main directories
mkdir -p docs
mkdir -p prompts
mkdir -p sessions/math_for_ml
mkdir -p research/findings
mkdir -p diagrams
mkdir -p examples

# Create placeholder files
touch docs/.gitkeep
touch research/findings/.gitkeep
touch examples/.gitkeep
```

## Files to Add

### Root Level
- README.md (main project description)
- LICENSE (MIT)
- .gitignore

### docs/
- protocol_v2.2.md
- MASTER_PROJECT_DOCUMENTATION.md
- version_history.md

### prompts/
- system_prompt_v2.2.md
- math_for_ml_prompt.md
- template_prompt.md

### sessions/math_for_ml/
- session_001_vectors_similarity.md
- (future sessions)

### diagrams/
- protocol_architecture.mermaid

### research/
- literature_review.md (future)
- study_design.md (future)
