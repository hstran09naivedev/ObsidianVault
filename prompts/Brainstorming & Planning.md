## Template

I'm developing a VoiceChat project and need assistance with [describe problem/feature].

**Project Context:** 
- **What it is:** [brief description of what VoiceChat does]
- **Current features:** [what's already built]
- **Architecture:** [frontend/backend/database structure]
- **Scale:** [user expectations/performance needs]

**Problem to solve:** [detailed problem description]
**Current tech stack:** [specific technologies/frameworks/libraries]

**Important:** If you're unclear about any aspect of my project or requirements, please ask clarifying questions first. I prefer discussion over assumptions.

Please provide 2-3 different solution approaches, each including:
- Main concept
- Pros/cons  
- Implementation complexity

Then ask me which approach I'd like to discuss in more detail.

## VoiceChat Project Template

I'm developing a VoiceChat project and need assistance with [describe problem/feature].

**Project Context:**

- **What it is:** Extensible real-time AI voice assistant framework built on LiveKit, designed for domain-specific knowledge interactions through pluggable RAG systems
- **Current features:**
    - Domain-agnostic voice assistant framework with function-based tool system
    - Pluggable knowledge domain architecture (healthcare and tax as reference implementations)
    - Voice-optimized conversational responses with 15-20 second target duration
    - Session management with user preferences and conversation context tracking
    - Real-time metrics and telemetry with Prometheus/Grafana monitoring
    - Modular RAG system using sentence transformers and FAISS vector search
    - Component caching system for performance optimization
- **Architecture:**
    - **Frontend:** React 19 + Next.js 15.4 client with LiveKit components for real-time audio/video streaming
    - **Backend:** Python LiveKit agent server with modular domain system architecture
    - **Database:** Redis for caching, sessions, and metrics storage
    - **Knowledge Layer:** Domain-specific RAG systems with vector embeddings
    - **Infrastructure:** Docker containerized services with monitoring stack
- **Scale:** Development framework targeting real-time voice interactions with sub-second response times, designed for production deployment with comprehensive monitoring

**Problem to solve:** [detailed problem description]

**Current tech stack:**

- **Backend:** Python 3.12+, LiveKit Agents SDK 1.0, PyTorch 2.7, OpenTelemetry, aiohttp, Redis, Pydantic, Sentence Transformers, FAISS
- **Frontend:** React 19, Next.js 15.4, TypeScript 5, LiveKit Client SDK 2.13, Tailwind CSS 4, Radix UI, Framer Motion
- **Infrastructure:** Docker Compose, Redis 7, Prometheus, Grafana, LiveKit Cloud
- **AI/ML:** OpenAI integration, Deepgram STT, customizable TTS providers, vector search capabilities

**Important:** If you're unclear about any aspect of my project or requirements, please ask clarifying questions first. I prefer discussion over assumptions.

Please provide 2-3 different solution approaches, each including:

- Main concept
- Pros/cons
- Implementation complexity

Then ask me which approach I'd like to discuss in more detail.