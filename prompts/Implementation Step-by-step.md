## Template

I need to implement [specific feature/solution] for my [Project name] project.

**Requirements details:**
- [describe functionality needed]
- [technology/framework being used]
- [constraints/limitations if any]

**Output requirements:**
Break this into clear implementation steps. Show ONLY THE FIRST STEP with:
- Brief description of what this step does
- Code to write/modify
- How to test/verify this step

**Important:** If you need more details about my project structure, existing code, or specific requirements, or not sure about anything, please ask before providing solutions. Let's discuss and clarify rather than making assumptions.

After I confirm "DONE" for the current step, proceed to the next step.


## VoiceChat Project Template - Step-by-Step Implementation

I need to implement [specific feature/solution] for my VoiceChat project.

**Requirements details:**

- [describe functionality needed]
- **Technology/framework being used:** Python 3.12+ with LiveKit Agents SDK, React 19 + Next.js 15.4 frontend
- **Constraints/limitations:** Real-time voice processing requirements, modular domain architecture, Redis caching, production monitoring needs

**Project structure context:**

```
VoiceChat/
├── agent/                          # Python LiveKit agent server
│   ├── voicechat_agent/
│   │   ├── agents/                 # Domain-specific agents (healthcare, tax examples)
│   │   ├── core/                   # Core systems (cache, config, session)
│   │   ├── metrics.py              # Prometheus metrics
│   │   ├── assistant.py            # Main voice assistant
│   │   └── lkmain.py              # Entry point
│   └── pyproject.toml
├── client/                         # React frontend
│   ├── components/                 # UI components
│   ├── app/                       # Next.js app structure
│   └── package.json
└── server/                        # Infrastructure
    ├── compose.yaml               # Docker services
    └── monitoring/                # Prometheus/Grafana
```

**Output requirements:** Break this into clear implementation steps. Show ONLY THE FIRST STEP with:

- Brief description of what this step does
- Code to write/modify
- How to test/verify this step

**Important:** If you need more details about my project structure, existing code, or specific requirements, please ask before providing solutions. Let's discuss and clarify rather than making assumptions.

After I confirm "DONE" for the current step, proceed to the next step.