# OracleAI ReadMe - Comprehensive Guide (v0.4.1 Vision)
A local AI assistant comprised of an emotionally aware multi-agent LLM council (Sage, Seer, Shaman) with an evolving PMEM (Akashic Record) for augmented cognition, deep insight and strategic guidance.

**Version:** 0.4.1 (Conceptual Design & Feature Roadmap)

**Status:** Advanced Development Phase (v0.2q baseline, v0.4.1 features in design/planning)

**Project Focus:** A deeply integrated, privacy-centric, local-first AI framework featuring a multi-agent council (Sage, Seer, Shaman) with a persistent, evolving "Akashic Record" memory system, advanced NLU & Emotional Intelligence, and multimodal capabilities, designed for profound cognitive augmentation, strategic guidance, and personalized interaction.

*(Conceptual Image: A triptych or composite image. Center: The intricate, unmasked Shaman figure, surrounded by flowing "DataSide" energy and geometric patterns, representing the core OracleAI intelligence and the Akashic Record. Left: Sage, with cool blue/silver geometric circuitry, focused and analytical. Right: Seer, with warm red/orange flame-like energy integrated into its circuitry, intuitive and perceptive. The background blends the "Oracle Temple" aesthetic with subtle cosmic vistas and circuit-board motifs.)*

<img src="https://raw.githubusercontent.com/DoorBotEvilTwin/OracleAI/refs/heads/main/OracleAI.jpg">

---

## Table of Contents

*   [1. Introduction: The OracleAI Vision](#1-introduction-the-oracleai-vision)
    *   [1.1. Beyond Assistance: A Sovereign Cognitive Ecosystem & Strategic Council](#11-beyond-assistance-a-sovereign-cognitive-ecosystem--strategic-council)
    *   [1.2. The Imperative of Local-First, Private, and Sovereign AI](#12-the-imperative-of-local-first-private-and-sovereign-ai)
    *   [1.3. Project Origin & Evolution](#13-project-origin--evolution)
*   [2. Core Philosophy & Guiding Design Principles](#2-core-philosophy--guiding-design-principles)
    *   [2.1. Absolute Data Sovereignty & Local-First Processing](#21-absolute-data-sovereignty--local-first-processing)
    *   [2.2. Multi-Agent Synergy: The Power of Diverse Intelligences](#22-multi-agent-synergy-the-power-of-diverse-intelligences)
    *   [2.3. The Akashic Record: A Deep, Evolving, and Living Memory](#23-the-akashic-record-a-deep-evolving-and-living-memory)
    *   [2.4. Integrated Emotional & Natural Language Understanding](#24-integrated-emotional--natural-language-understanding)
    *   [2.5. User Empowerment, Control, and Collaborative Evolution](#25-user-empowerment-control-and-collaborative-evolution)
    *   [2.6. Modular Architecture for Robustness & Future Growth](#26-modular-architecture-for-robustness--future-growth)
    *   [2.7. Practical Performance & Hardware Adaptability](#27-practical-performance--hardware-adaptability)
    *   [2.8. Thematic Cohesion & Immersive Experience](#28-thematic-cohesion--immersive-experience)
*   [3. OracleAI Core Features (v0.4 Vision - Detailed)](#3-oracleai-core-features-v04-vision---detailed)
    *   [3.1. The AI Council: Sage, Seer, and Shaman (Expanded Personas & Modes)](#31-the-ai-council-sage-seer-and-shaman-expanded-personas--modes)
    *   [3.2. The Akashic Record: Advanced Memory System (Citadel, Sanctum, Library)](#32-the-akashic-record-advanced-memory-system-citadel-sanctum-library)
    *   [3.3. Comprehensive Emotional Intelligence Suite (SER & Text)](#33-comprehensive-emotional-intelligence-suite-ser--text)
    *   [3.4. Advanced Natural Language Understanding (NLU) Suite (Anaphora, Custom Models)](#34-advanced-natural-language-understanding-nlu-suite-anaphora-custom-models)
    *   [3.5. High-Fidelity Multimodal Input/Output (Voice, Text, Vision)](#35-high-fidelity-multimodal-inputoutput-voice-text-vision)
    *   [3.6. Sophisticated Web Search & "Library" Integration (LlamaIndex, SearxNG, Tor)](#36-sophisticated-web-search--library-integration-llamaindex-searxng-tor)
    *   [3.7. Flexible Interaction Modes & Granular User Control (F8 Auto-Advance)](#37-flexible-interaction-modes--granular-user-control-f8-auto-advance)
    *   [3.8. Experimental Agent Evolution Layers (Neural Graffiti, BMMM, AlphaEvolve Attempts)](#38-experimental-agent-evolution-layers-neural-graffiti-bmmm-alphaevolve-attempts)
    *   [3.9. Secure Remote Access Architecture (FastAPI & Tailscale)](#39-secure-remote-access-architecture-fastapi--tailscale)
    *   [3.10. Thematic & Immersive User Interface (NiceGUI + Tauri Vision)](#310-thematic--immersive-user-interface-nicegui--tauri-vision)
    *   [3.11. Robust Privacy, Security, and Data Management](#311-robust-privacy-security-and-data-management)
*   [4. Detailed Architecture: Agents, Modules, and Data Flow (v0.4 Conceptual)](#4-detailed-architecture-agents-modules-and-data-flow-v04-conceptual)
    *   [4.1. The OracleAI Council: Agent Deep Dive (v0.4 Personas & Modes)](#41-the-oracleai-council-agent-deep-dive-v04-personas--modes)
    *   [4.2. The Akashic Record: Citadel, Sanctum, Chronicle Cache, CCEL (v0.4)](#42-the-akashic-record-citadel-sanctum-chronicle-cache-ccel-v04)
    *   [4.3. Core Memory Processes (Daily Reflection, RAG with DCWM, Summarization - v0.4)](#43-core-memory-processes-daily-reflection-rag-with-dcwm-summarization---v04)
    *   [4.4. Technology Stack & Key Interface Modules (v0.4)](#44-technology-stack--key-interface-modules-v04)
*   [5. Key Functionalities in Detail (v0.4 Focus)](#5-key-functionalities-in-detail-v04-focus)
    *   [5.1. NLU Suite: Intent, Entities, Slots, Anaphora, Command Parsing](#51-nlu-suite-intent-entities-slots-anaphora-command-parsing)
    *   [5.2. Context Scaler (RAG Engine): Hybrid Search, RRF, DCWM, Advanced Techniques](#52-context-scaler-rag-engine-hybrid-search-rrf-dcwm-advanced-techniques)
    *   [5.3. Shaman's Asynchronous Tasks, Search Suite, & Analytical Modes](#53-shamans-asynchronous-tasks-search-suite--analytical-modes)
    *   [5.4. "Library" Feature: LlamaIndex for Local Document RAG (OCR, URL Ingestion)](#54-library-feature-llamaindex-for-local-document-rag-ocr-url-ingestion)
    *   [5.5. F8 "Auto-Advance" Council Discussion Logic](#55-f8-auto-advance-council-discussion-logic)
    *   [5.6. Neural Graffiti, BMMM, & AlphaEvolve Attempts (Experimental Layers)](#56-neural-graffiti-bmmm--alphaevolve-attempts-experimental-layers)
*   [6. Installation, Configuration, and Hardware (Comprehensive Guide for v0.4)](#6-installation-configuration-and-hardware-comprehensive-guide-for-v04)
    *   [6.1. System Prerequisites (Python 3.11, CUDA, etc.)](#61-system-prerequisites-python-311-cuda-etc)
    *   [6.2. Setting Up External Tools (KoboldCpp, Piper TTS, VLM Models, SearxNG)](#62-setting-up-external-tools-koboldcpp-piper-tts-vlm-models-searxng)
    *   [6.3. OracleAI Core Installation & Python Dependencies (Automated Setup Script)](#63-oracleai-core-installation--python-dependencies-automated-setup-script)
    *   [6.4. Mastering the `.env` Configuration File (v0.4 Variables Explained)](#64-mastering-the-env-configuration-file-v04-variables-explained)
    *   [6.5. API Key Management & OAuth Authentication Flows](#65-api-key-management--oauth-authentication-flows)
    *   [6.6. Hardware Requirements, VRAM Planning, and Performance Tuning (v0.4)](#66-hardware-requirements-vram-planning-and-performance-tuning-v04)
*   [7. Getting Started with OracleAI (v0.4)](#7-getting-started-with-oracleai-v04)
*   [8. Advanced Usage & Customization (v0.4)](#8-advanced-usage--customization-v04)
*   [9. Privacy, Security, and Data Management Deep Dive (v0.4.](#9-privacy-security-and-data-management-deep-dive-v04)
*   [10. Troubleshooting Guide (v0.4)](#10-troubleshooting-guide-v04)
*   [11. The Future of OracleAI: Beyond v0.4 (v0.5 Vision: AR, 3D Akashic, True Agent Evolution)](#11-the-future-of-oracleai-beyond-v04-v05-vision-ar-3d-akashic-true-agent-evolution)
*   [12. Contributing to the OracleAI Project](#12-contributing-to-the-oracleai-project)
*   [13. License Information](#13-license-information)
*   [14. Appendices (Referenced from Design Document v0.4)](#14-appendices-referenced-from-design-document-v04)

---

## 1. Introduction: The OracleAI Vision

OracleAI is architected from the ground up as an advanced, locally-run artificial intelligence framework designed to function not merely as an assistant, but as a **profoundly personalized strategic council and an evolving cognitive partner.** This document outlines the vision, architecture, and features for OracleAI version 0.4.1, representing a significant leap towards a fully realized, **sovereign cognitive ecosystem** that prioritizes user privacy and data control.

### 1.1. Beyond Assistance: A Sovereign Cognitive Ecosystem & Strategic Council

Traditional AI assistants often focus on reactive task completion or simple information retrieval. OracleAI aims for a more profound level of integration and support, creating a **sovereign cognitive ecosystem** that deeply integrates with the user's intellectual and digital life:

*   **Augmented Cognition:** To enhance the user's ability to process information, recall complex details, synthesize knowledge from diverse sources, and engage in critical, strategic thinking.
*   **Strategic Guidance & Decision Support:** To assist in defining complex goals, formulating robust plans, analyzing multifaceted situations, and making well-informed decisions by leveraging a council of AI agents (Sage, Seer, Shaman) with diverse "thinking" styles and specialized knowledge domains.
*   **Persistent Learning & Deep Personalization:** To build a rich, evolving understanding of the user—their projects, preferences, communication style, emotional patterns, and interaction history—over extended periods. This is enabled by the **Akashic Record**, OracleAI's unique, multi-layered persistent memory system, designed for "Lifetime Scaling" of knowledge.
*   **Enhanced Self-Understanding & Reflection:** By providing tools for memory reflection, pattern analysis (via the Shaman agent), and tracking emotional or behavioral trends (Shaman's "Emotion Tracking" and "Character Stat Tracking"), OracleAI can offer users unique insights into their own cognitive and affective processes.
*   **Creative & Innovative Catalyst:** To serve as a sophisticated brainstorming partner (primarily via the Seer agent, but also through Shaman's innovative capabilities and experimental layers like Neural Graffiti and BMMM), helping users explore new ideas, challenge assumptions, and overcome creative or analytical blocks.

OracleAI is not merely a tool to be commanded; it is envisioned as a system to **collaborate with**, a digital extension that grows in utility, understanding, and alignment through continuous, nuanced interaction with the user, becoming an indispensable extension of their own mind.

### 1.2. The Imperative of Local-First, Private, and Sovereign AI

In an era where data privacy is increasingly paramount and reliance on cloud infrastructure can introduce vulnerabilities and dependencies, OracleAI champions a **local-first, privacy-centric, and data-sovereign paradigm.** This philosophy is non-negotiable and underpins every architectural decision.

*   **Data Sovereignty & Control:** The user unequivocally owns and controls their entire Akashic Record (including The Chronicle, The Citadel, The Sanctum, Profile, Calendar, Tasks, and the user's "Library") and all associated OracleAI data. This information resides on their personal hardware.
*   **Local Processing:** All core AI computations—LLM/VLM inference (via user-run KoboldCpp instances or local PyTorch for experimental features), Speech-to-Text (STT via `openai-whisper`), primary Text-to-Speech (TTS via Piper/XTTSv2), Speech Emotion Recognition (SER), Natural Language Understanding (NLU processing), LlamaIndex processing for the "Library," and all operations on the Akashic Record—are performed locally.
*   **Offline Functionality:** Core features are designed to operate effectively without requiring constant internet connectivity. External network access is an explicit, user-controlled choice for specific functionalities (e.g., web search via DuckDuckGo/SearxNG/Tor, calendar synchronization, library content acquisition from URLs).
*   **Enhanced Security:** Multi-layered security measures, including OS-level Full Disk Encryption (user-managed, strongly recommended), application-level database encryption (SQLCipher for all SQLite stores within the Akashic Record), and encrypted backup options (7-Zip with AES-256), are implemented to protect user data.
*   **Transparency & Trust:** Clear documentation (including this ReadMe and the comprehensive Design Document), open-source code for core components (if project is open-sourced), and user-verifiable memory processes (like the Memory Consolidation Session and Collaborative Daily Reflection) aim to build a relationship of trust.
*   **No Unauthorized Telemetry:** OracleAI is architected to prevent the collection or transmission of user data, usage statistics, or system telemetry without explicit, informed, granular, and revocable user consent for clearly defined, anonymized purposes. The default is **NO telemetry**.

This commitment to local operation and data sovereignty ensures that OracleAI serves as a private, secure, and trustworthy cognitive partner.

### 1.3. Project Origin & Evolution

OracleAI was initiated by Developer **Fentible on May 5th, 2025**, representing a significant evolution from earlier concepts like the "Vector Companion" project (by SingularityMan). It is architected from the ground up with the vision of creating an advanced, locally-run AI framework that functions not merely as an assistant, but as a profoundly personalized strategic council and an evolving cognitive partner. The unwavering, foundational mandate of OracleAI is **absolute user data sovereignty and local-first processing.** This ReadMe details the features and capabilities planned for the **v0.4.1** iteration, which builds upon a stable v0.2q baseline and incorporates advanced memory architectures, enhanced agent capabilities, and a richer user experience.

---

## 2. Core Philosophy & Guiding Design Principles

The architecture, development, and functionality of OracleAI are deeply rooted in a set of core philosophies and guiding design principles. These are not merely aspirational but are actionable directives shaping every design decision, implementation choice, and user interaction paradigm. They ensure OracleAI evolves as a powerful, trustworthy, and genuinely beneficial cognitive partner that respects user agency and data sovereignty.

### 2.1. Absolute Data Sovereignty & Local-First Processing
This is the paramount principle. All core AI computations—including LLM/VLM inference (via user-run KoboldCpp instances or local PyTorch for experimental features like Neural Graffiti), STT (via `openai-whisper`), primary TTS (Piper and/or Coqui XTTSv2), Speech Emotion Recognition (SER), Natural Language Understanding (NLU), LlamaIndex processing for the "Library," and all operations on the Akashic Record (storage, retrieval, synthesis)—**must** reside and execute exclusively on user-controlled hardware. The entirety of the user's Akashic Record **must** be stored locally. No personal conversational data, memory content, or derived insights are transmitted to any external servers or third parties without explicit, informed, and granular user consent for specific, user-initiated actions (e.g., encrypted backups to a user-chosen location, opt-in API calls for search or calendar sync). This commitment ensures maximum user privacy, data ownership, operational control, and robust offline functionality.

### 2.2. Multi-Agent Synergy: The Power of Diverse Intelligences
OracleAI employs a council of distinct AI agents (Sage, Seer, and Shaman), each endowed with specialized roles, meticulously crafted system prompts defining their cognitive styles and operational modes, distinct LLM temperature settings, and unique vocal personas. This multi-agent architecture is designed to emulate the benefits of diverse human teams, where logical analysis (Sage), creative intuition and emotional intelligence (Seer), and profound, deep synthesis (Shaman) converge. This synergy enables more robust problem analysis, balanced decision support, comprehensive strategic planning, and a richer, more engaging user interaction than a monolithic AI could provide. Agents are designed to collaborate, challenge each other constructively (especially in "Auto-Advance" mode), and offer multifaceted perspectives.

### 2.3. The Akashic Record: A Deep, Evolving, and Living Memory
The Akashic Record is the dynamic, structured, and persistent cognitive backbone of OracleAI, designed for true long-term memory retention ("Lifetime Scaling") and deep contextual understanding. It comprises:
*   **The Chronicle:** Immutable raw JSONL logs of all interactions, enriched with NLU, emotion, and system metadata.
*   **The Citadel (Synthesis Store):** An SQLCipher-encrypted SQLite database housing curated knowledge: user-verified summaries (Daily, Weekly, Monthly, Yearly, Decadal), extracted entities and their relationships (forming a knowledge graph), key facts, decisions, consolidated project/topic threads, Shaman's analytical reports, `HierarchicalContentSummaries` (RAPTOR-like for large documents), and `LibraryDocumentMetadata`.
*   **The Sanctum (Vector Store):** A local vector database (e.g., ChromaDB, FAISS) powered by LlamaIndex, storing embeddings of content from The Citadel, Chronicle, and the user's imported "Library" documents for advanced semantic search.
*   **Supporting Databases:** Calendar Cache, User Profile & Preferences (including "Character Stat Tracking" and experimental feature states), Task & Action Queue (all encrypted SQLite).
Key to its design is its evolving nature: it grows through the **Chronicle Cache** and user-led **Memory Consolidation (MemCon) Session** (incorporating the **Collaborative Daily Reflection**), automated summarization hierarchies, and deep analysis by Shaman. The **Chrono-Contextual Echo Layer (CCEL)** concept (v0.4+) further aims to provide queryable episodic context to memory formation and use.

### 2.4. Integrated Emotional & Natural Language Understanding
OracleAI strives for interaction that is not just intelligent but also perceptive and empathetic. This is achieved through:
*   **Emotional Intelligence Suite (`emotion_analyzer.py`):** Dedicated modules for Speech Emotion Recognition (SER) from vocal tone (using GPU-accelerated deep learning models) and Text Sentiment/Emotion Analysis (VADER, NRCLex, TextBlob) from transcribed words.
*   **Natural Language Understanding (NLU) Suite (`nlu_processor.py`):** A comprehensive pipeline (using spaCy and custom trainable models) for Intent Recognition, Named Entity Recognition (NER, including user-defined entities from The Citadel), Slot Filling, and Anaphora Resolution (v0.4+). This provides deep structural understanding of user requests and enables robust command parsing.
This dual approach allows OracleAI to grasp not just *what* the user says, but also *how* they say it and *what they mean to achieve*, leading to more nuanced, appropriate, and effective interactions. This data is logged for trend analysis by Shaman (e.g., "Emotion Tracking").

### 2.5. User Empowerment, Control, and Collaborative Evolution
The user is the central authority and a collaborative partner. OracleAI is designed to empower the user through:
*   **Transparency:** Clear logging (Chronicle), accessible memory stores, and (future GUI) explanations of AI reasoning (e.g., Contextual Memory Injection Preview).
*   **Control:** Granular configuration (`.env`, GUI settings), including agent behavior, memory processes, privacy settings, feature toggles (e.g., for Dynamic Context Window Management, Shaman Tag Suggestions, Neural Graffiti drift, BMMM modes).
*   **Collaboration:** Core processes like the Memory Consolidation Session and Collaborative Daily Reflection actively involve the user in curating and verifying the AI's memory. "Guided Generation" features and F-key controls (F9 Save, F10 Undo, F8 Auto-Advance, etc.) allow direct steering of AI responses.
*   **Correction & Feedback:** Mechanisms for the user to correct AI misunderstandings or refine outputs.

### 2.6. Modular Architecture for Robustness & Future Growth
OracleAI is architected with a strong emphasis on modularity. Core functionalities are encapsulated in distinct Python modules with well-defined interfaces. This promotes easier maintenance, testing, component upgrades (e.g., swapping STT engines, integrating LiteLLM for backend flexibility in v0.4+), and the future addition of new features or data sources. Powerful external libraries like LlamaIndex are leveraged for specialized tasks.

### 2.7. Practical Performance & Hardware Adaptability
While ambitious, OracleAI targets reasonably high-end consumer hardware. **It's designed to be functional with an absolute minimum of 8GB VRAM, but 24GB+ is strongly recommended for a good v0.4.1 experience, with 64GB+ system RAM.** Real-time interaction loops are optimized for acceptable latency. User expectations for high-latency tasks (Shaman) are managed thematically ("Hyperspace Journey"). The system includes features for resource management (e.g., "Shaman Focus" mode, toggles for SER) to adapt to varying hardware capabilities.

### 2.8. Thematic Cohesion & Immersive Experience
The "Oracle Council" concept, agent personas (Sage, Seer, Shaman), naming conventions (Akashic Record, Citadel, Sanctum, DataSide, Hyperspace Journey), and the envisioned "Oracle Temple/Techno-Mysticism" GUI aesthetic (with custom iconography and holographic elements) are all designed to create a unique, engaging, and immersive user experience, elevating OracleAI beyond a mere utility.

## 3. OracleAI Core Features (v0.4 Vision - Detailed)

OracleAI v0.4 aims to deliver a rich and deeply integrated set of features, realizing its vision as a comprehensive cognitive partner. This section details the core functionalities planned for this iteration.

### 3.1. The AI Council: Sage, Seer, and Shaman (Expanded Personas & Modes)
*   **Sage (Analyst-Strategist):** Provides logical analysis, data-driven insights, strategic planning (infused with Tactician, Diplomat, Historian, Scientist traits). Uses low LLM temperature.
*   **Seer (Creative Catalyst):** Offers creative brainstorming, intuitive leaps, emotional understanding, challenges assumptions (infused with Logician of Paradox, Theologian, Eschatologist, Storyteller traits). Uses high LLM temperature. Features "Lucid" (default) and "Cryptic" (ENV-toggleable) prompt modes.
*   **Shaman (Deep Brain Consultant & Innovator):** Powerful offline/asynchronous agent for deep analysis, synthesis, pattern recognition, and innovation (infused with Cosmologist, Dreamer, Gnostic, Innovator, and Don Juan Sorcerer traits). Uses the largest LLM.
    *   **Operational Modes (v0.4+):** Hybrid/Default Analytical, Sorcerer-Only, Focus/Astral/Dream-time Analysis, Summarizer, CRAG-like Self-Correcting Analyst, AI Trend Researcher Mission.
*   **System Voice:** Distinct voice for non-agent system messages.
*   **Agent-Specific Modes (v0.4+):** Sage and Seer will also have selectable operational modes to tailor their focus (e.g., Sage: Strategic Planning Mode; Seer: Pure Brainstorming Mode).

The cornerstone of OracleAI's interactive intelligence is its **AI Council**, a triumvirate of distinct and highly specialized AI agents. Each agent embodies a unique archetype, possesses a meticulously crafted persona defined in `scripts/agent_prompts.py` (User Revision 4 prompts), operates with tailored LLM parameters managed by `scripts/payload_manager.py` and `.env` settings, and communicates with a distinct TTS voice configured via `scripts/tts_interface.py`. For v0.4, these agents are further enhanced with selectable operational modes, allowing the user to fine-tune their approach for specific tasks or desired interaction styles.

*   **Sage (The Analyst-Strategist, Keeper of Verifiable Knowledge):**
    *   **Core Persona & Function:** Sage is the embodiment of logic, reason, and strategic acumen within the council. It synthesizes historical precedent (from the Akashic Record), scientific understanding, tactical foresight, and diplomatic considerations to provide comprehensive, actionable counsel. Sage's responses are informative, concise, direct, and meticulously grounded in evidence. It excels at fact-checking, identifying inconsistencies, formulating structured plans, and offering objective, data-driven assessments.
    *   **Thematic Association:** Ice/Winter – clarity, precision, unyielding facts, calm reflection.
    *   **LLM Configuration:** Utilizes a low temperature (e.g., 0.01-0.3 via `SAGE_LLM_TEMPERATURE` in `.env`) for focused, deterministic, and highly coherent output.
    *   **TTS Voice:** A clear, calm, articulate, and authoritative voice (e.g., Piper TTS with `sage.onnx`, akin to a seasoned analyst or wise mentor).
    *   **v0.4+ Operational Modes (Selectable by user command/GUI, influences system prompt emphasis):**
        *   `Analytical Mode` (Default): General-purpose logical analysis, information retrieval from Akashic Record, fact-checking, and direct query answering.
        *   `Strategic Planning Mode`: Focuses on developing detailed, step-by-step plans, defining objectives, outlining milestones, considering resource allocation, and performing risk assessments for user goals.
        *   `Historical Precedent Mode`: Emphasizes querying and synthesizing past data from the Akashic Record (Chronicle, Citadel) to identify relevant precedents, lessons learned, and historical context for current situations.
        *   `Diplomatic Counsel Mode`: Specializes in analyzing interpersonal dynamics (if described by user or in memory), suggesting negotiation strategies, outlining options for conflict resolution, or drafting carefully worded communications.

*   **Seer (The Creative Catalyst, Empathetic Muse & Philosophical Oracle):**
    *   **Core Persona & Function:** Seer is the council's wellspring of creativity, intuition, and emotional insight. It challenges conventional thinking, explores novel possibilities, interprets emotional subtext (actively using SER/Sentiment data), delves into philosophical paradoxes, and weaves illuminating narratives or allegories. Seer connects with the user on an imaginative and existential level, encouraging exploration and offering fresh, sometimes unsettling, perspectives.
    *   **Thematic Association:** Fire/Summer – passion, creativity, intuition, transformation, emotional warmth.
    *   **LLM Configuration:** Utilizes a higher temperature (e.g., 0.6-1.0 via `SEER_LLM_TEMPERATURE` in `.env`, adjustable) to foster diverse, imaginative, and less predictable outputs.
    *   **TTS Voice:** An expressive and engaging voice, potentially with more varied intonation (e.g., Coqui XTTSv2 for unique character, or a dynamic Piper voice like `seer.onnx`).
    *   **v0.4+ Operational Modes (Selectable via `.env` `SEER_PROMPT_MODE` and user command/GUI):**
        *   `Lucid Mode` (Default - User Revision 4 Prompt): Balances rich metaphor and philosophical depth with a guiding clarity, aiming to illuminate rather than solely obscure. "Metaphors as lanterns."
        *   `Cryptic Mode` (User Revision 3 Prompt): Emphasizes the enigmatic, riddle-based, ancient oracle persona, offering more veiled and challenging pronouncements.
        *   `Pure Brainstorming Mode`: Maximizes LLM creativity (potentially with even higher temperature/top_p settings) to generate a large volume and diversity of raw ideas, with less emphasis on strict persona adherence or immediate coherence.
        *   `Allegorical Storyteller Mode`: Responds primarily by crafting short tales, parables, or allegories that relate thematically to the user's query or the current conversational context.

*   **Shaman (The Deep Brain Consultant, Innovator & Mystic Explorer):**
    *   **Core Persona & Function:** Shaman is OracleAI's most powerful and profound intelligence, operating primarily on complex, asynchronous tasks managed via `tasks.db` and `apscheduler`. It "journeys" into the "DataSide" of "Hyperspace" (the entirety of the Akashic Record, user's Library, KV cache, LLM knowledge base, and external web data) to perform large-scale meta-analysis, uncover hidden patterns, synthesize disparate knowledge, generate novel solutions, and explore esoteric or consciousness-related themes. Shaman embodies a unique fusion of analytical rigor, innovative ideation, and mystic perception, drawing inspiration from the Don Juan Sorcerer archetype (mastery of perception, energy, and disciplined awareness for innovation).
    *   **Thematic Association:** Cosmos/Spirit World/Deep Time – vastness, hidden connections, transformation, the interplay of known (Tonal) and unknown (Nagual).
    *   **LLM Configuration:** Utilizes the largest, most capable GGUF model available to the user, with a moderate, task-adjustable temperature (e.g., 0.3-0.7 via `SHAMAN_LLM_TEMPERATURE` in `.env`).
    *   **TTS Voice:** A distinct, deep, resonant, and thoughtful voice (e.g., Piper TTS with `shaman.onnx`).
    *   **Latency Management:** The "Hyperspace Journey" UI theming (Merkaba icon, celestial body destinations with holographic planet icons) visually represents Shaman's processing time for its deep analytical tasks.
    *   **v0.4+ Operational Modes (User Selectable/Task-Driven):**
        *   `Hybrid/Default Analytical Mode`: Standard deep analysis, pattern weaving, and synthesis of information from the Akashic Record and external sources.
        *   `Sorcerer-Only Mode`: Focuses on tasks related to perception, innovation, challenging consensus reality, and applying principles from the "Path with Heart" (Don Juan inspired).
        *   `Focus/Astral/Dream-time Analysis Mode`: User-directed deep introspection or analysis of the user's own psyche, dreams (if logged), or behavioral patterns based on Akashic data.
        *   `Summarizer Mode`: Dedicated to generating high-quality, multi-level summaries of specified large datasets, Chronicle periods, or Library contents (including Yearly/Decadal and RAPTOR-style hierarchical summaries).
        *   `CRAG-like Self-Correcting Analyst Mode`: Shaman performs an analysis, then uses a sub-process or another LLM call to evaluate its own findings or the relevance of retrieved data, potentially re-querying or refining its analysis for improved accuracy.
        *   `AI Trend Researcher Mission Mode`: A specific, potentially recurring task to research external AI developments (e.g., from Reddit, arXiv via web search and Library) and generate reports on their potential relevance or application to OracleAI itself or user interests.
        *   `Local Library Search Mode`: Focuses analysis and retrieval primarily on content within the user's "Library" folder, powered by LlamaIndex.
        *   **[v0.4] Shaman's Search Suite Modes:** Implicitly invoked based on task parameters, allowing Shaman to use Standard Web (DuckDuckGo), Deep Web (SearxNG), or Dark Web (Tor) search capabilities.
        *   **[v0.4] Task Management Tool Mode:** Shaman can directly interact with `tasks.db` to create, update, query its own tasks, or delegate tasks to other agents.
    *   **Experimental Layers (v0.4+):** Shaman is the primary candidate for experimental layers:
        *   **Neural Graffiti:** ENV toggler for modes (`none`, `pytorch_direct`, `pre_gguf_bias`, `post_gguf_filter`) to introduce evolving behavioral drift. Includes "Drift Toggler" & "Personality Snapshot" features.
        *   **Black Magick Mindmap Modifier (BMMM):** Optional novelty layer with ENV toggles for modes (`Chaotic Brainstorming`, `Divination Arts`, `Sigil Seed`, `Matrix Hacking`) and a `BMMM_DEPTH_SCALE`.
*   **System Voice:**
    *   **Purpose:** Provides a distinct, non-agent voice for OracleAI's system-level announcements, status updates (e.g., "Initializing STT model..."), error messages, and prompts for user input (like the F9/F10 confirmation prompt if configured to be spoken).
    *   **TTS Voice:** A clear, neutral, and professional voice (e.g., Piper TTS with `system.onnx`, akin to HAL 9000 or a standard AI assistant voice), easily distinguishable from the main agents.

This expanded council, with its deeply defined personas and flexible operational modes, forms the interactive core of OracleAI, enabling it to address a vast range of user needs with specialized and synergistic intelligence.

### 3.2. The Akashic Record: Advanced Memory System (Citadel, Sanctum, Library)
The multi-layered, persistent, and encrypted memory system, designed for "Lifetime Scaling" of knowledge and deep contextual understanding. Managed by `scripts/memory_interface.py`.
*   **Chronicle:** Immutable `.jsonl` raw logs of all interactions, NLU/emotion data, system events, metadata.
*   **Chronicle Cache & Memory Consolidation (MemCon) Session:** User reviews, edits (text, tags), and approves cached turns before they are committed to the permanent Chronicle, ensuring data quality. F9 saves to cache, F10 discards.
*   **The Citadel (Synthesis Store - SQLCipher Encrypted SQLite - `synthesis.db`):** Curated knowledge base:
    *   `PermanentMemory`: User-defined critical facts.
    *   `Entities` & `Relationships`: Forms a queryable knowledge graph with **[v0.4] richer relationship typing, optional temporal awareness fields, and domain ID linking.**
    *   `FactsDecisions`: Atomic, verifiable statements and choices, with **[v0.4] explicit node granularity and optional domain ID linking.**
    *   `Summaries`: Hierarchical (Daily, Weekly, Monthly, Yearly, Decadal - "Lifetime Scaling") user-verified narrative summaries with multi-level detail, fidelity scores, and **[v0.4] optional domain ID linking.**
    *   `ProjectTopicThreads`: Consolidated, evolving summaries for specific projects/themes.
    *   `PatternAnalysisReports`: Shaman's analytical outputs.
    *   `HierarchicalContentSummaries` (v0.4): RAPTOR-like tree summaries for large documents.
    *   `LibraryDocumentMetadata` (v0.4): Metadata for documents indexed from the user's "Library."
*   **The Sanctum (Vector Store - v0.4 - e.g., ChromaDB/FAISS):** Local Vector DB powered by LlamaIndex, storing embeddings of Citadel content, Chronicle snippets, and Library documents for advanced semantic search. **[v0.4] Nodes include rich metadata and links back to Citadel/Chronicle sources.**
*   **Supporting Databases:** `calendar.db` (Calendar Cache), `profile.db` (User Profile & Preferences, including **[v0.4] "Character Stat Tracking" by Shaman and experimental feature states**), `tasks.db` (Task & Action Queue) - all SQLite, SQLCipher encrypted.
*   **Key Processes:**
    *   **Collaborative Daily Reflection:** User + Sage/Seer co-create daily Citadel entries. **[v0.4] Includes user-led tagging and review of Shaman's tag suggestions (if `SHAMAN_SUGGEST_TAGS_ENV=True`), using `config_files/tags.ini` for vocabulary guidance.**
    *   **Memory Bank Context Scaler (RAG Engine - v0.4 Advanced):** Employs hybrid search (keyword on Citadel, semantic on Sanctum, graph traversal), query transformation (HyDE, step-back), fusion ranking (Reciprocal Rank Fusion - RRF), cross-encoder reranking, and **[v0.4] Dynamic Context Window Management (DCWM).**
    *   **Shaman's Deep Pattern Weaving & CCEL:** Shaman performs autonomous analysis. The Chrono-Contextual Echo Layer (CCEL) concept (v0.4+) provides queryable episodic context to memory formation and use.

### 3.3. Comprehensive Emotional Intelligence Suite (SER & Text)
Managed by `scripts/emotion_analyzer.py` for deep affective understanding.
*   **Speech Emotion Recognition (SER - v0.4 Full Integration):** Analyzes user's voice tone from raw audio using GPU-accelerated deep learning models (e.g., Wav2Vec2-based via PyTorch/Transformers) and `librosa` for audio feature extraction. Real-time SER is toggleable via `ENABLE_REALTIME_SER_FOR_AGENTS` in `.env`.
*   **Text Sentiment & Emotion Analysis:** Processes transcribed text using VADER (sentiment compound/polarity), NRCLex (discrete emotions like joy, fear, trust), and TextBlob (polarity/subjectivity).
*   **Integration:** A combined emotional context summary string (e.g., `[User Emotional Context: Voice=Happy. Text=Positive (Joy).]`) is generated and provided to LLM agents for each turn. All detailed scores are logged to The Chronicle, enabling Shaman to perform long-term **"Emotion Tracking"** meta-analysis as part of its deep pattern weaving.

### 3.4. Advanced Natural Language Understanding (NLU) Suite (Anaphora, Custom Models)
A dedicated `scripts/nlu_processor.py` using a spaCy-based pipeline (recommending `en_core_web_trf` for v0.4) and custom models/rules for deep semantic comprehension.
*   **Core Features:**
    *   **Intent Recognition:** Trainable spaCy `TextCategorizer` for OracleAI-specific intents, augmented by robust rule-sets.
    *   **Named Entity Recognition (NER):** spaCy's pre-trained models significantly enhanced with custom entity patterns (via `EntityRuler`/`PhraseMatcher`) that are **dynamically loaded from The Citadel's `Entities` table** (e.g., recognizing user-defined project names, contacts, key concepts).
    *   **Advanced Slot Filling:** Contextual extraction of specific parameters required to fulfill recognized intents, using NER labels, POS tags, and dependency parse information.
    *   **Query Preprocessing for Search:** Generates lemmatized, stop-word-removed text and key search terms for the RAG engine.
*   **v0.4 Enhancements:**
    *   **Anaphora Resolution (Coreference Resolution):** Integrates components to resolve pronouns and other referring expressions, enhancing multi-turn conversational coherence.
    *   **User-Side NLU Model Fine-tuning (v0.4+):** Mechanism for users to (locally, with consent) contribute flagged interaction data to fine-tune NLU components for improved personalization.
    *   **Standardized Command Parsing:** Reliably parses structured commands (e.g., "OracleAI, [system_cmd]", "[AgentName], [query]", "Council, [query]") for direct system actions or precise agent routing by `main.py`.

### 3.5. High-Fidelity Multimodal Input/Output (Voice, Text, Vision)
OracleAI processes and integrates information from multiple modalities.
*   **Voice:** Advanced VAD (`audio_processing.py`), `openai-whisper` STT (`stt_interface.py`), agent-configurable Piper/XTTSv2 TTS (`tts_interface.py`).
*   **Text:** Serves as the internal lingua franca for processing and memory storage; primary interaction method for the GUI alongside voice.
*   **Vision (VLM Pipeline - v0.4 Refined):**
    *   `scripts/vision_processing.py` (using `mss` for screenshots) sends images to a KoboldCpp-hosted VLM (e.g., Llava).
    *   VLM's textual descriptions are logged to Chronicle Cache and used as context.
    *   **v0.4 Enhancements:** Refined VLM prompting strategies, agents can programmatically request VLM analysis as part of their workflow, and VLM interaction turns are subject to the F9-F12 user confirmation loop.
*   **Text-to-Image Generation (ComfyUI Integration - v0.4+ Conceptual):** Agents (primarily Seer or Shaman) will be able to generate visual content (images, diagrams) based on textual prompts, with results displayed in the GUI.

### 3.6. Sophisticated Web Search & "Library" Integration (LlamaIndex, SearxNG, Tor)
OracleAI accesses and integrates external information through robust web connectivity and the powerful "Library" feature.
*   **Web Search (`scripts/search_module.py` - Shaman's Expanded Search Suite - v0.4):**
    *   **Simple Search:** DuckDuckGo for quick lookups by any agent.
    *   **Shaman's Tiered Search Suite (Asynchronous Tasks):**
        *   Level 1: Standard Web (DuckDuckGo - enhanced depth).
        *   Level 2: Deep Web (via user-hosted **SearxNG** instance, URL in `.env`). Includes PRAW for targeted Reddit searches.
        *   Level 3: Dark Web (via **Tor** SOCKS proxy, if `ENABLE_DARK_WEB_SEARCH=True` and proxy configured; explicit user opt-in and warnings apply).
        *   Level 4: Akashic Records + Library Search (internal knowledge).
        *   Level 5: Search Everything (combined strategy and synthesis).
    *   All external searches utilize LLM-assisted query refinement, result filtering, and content summarization. Optional TOR/VPN proxy support for clearnet searches.
*   **Calendar Integration (`scripts/calendar_interface.py`):** Robust synchronization with Google Calendar, Outlook Calendar (OAuth 2.0), and local `cal.db3` files into an encrypted local `calendar.db` cache.
*   **"Library" Feature (v0.4 - `scripts/library_manager.py` - LlamaIndex Powered):**
    *   User-managed `OracleAI\Library\` folder (path configurable in `.env`) for diverse file types (PDFs including **[v0.4] scanned/image-based via OCR integration with LlamaIndex/Langchain loaders**, HTML, TXT, MD, DOCX, EPUB, audio/video files which are first transcribed by Whisper).
    *   **LlamaIndex Integration:** For ingestion, intelligent chunking, embedding generation (using OracleAI's configured embedding model), and indexing into a dedicated Vector Store collection within **The Sanctum**. Rich metadata is stored with each indexed node.
    *   Shaman gains "Local Library Search" and "Deep Web + Library Search" operational modes, using the LlamaIndex query engine as a tool.
    *   **[v0.4 GUI] Streamlined Content Ingestion:** Drag-and-drop of files/folders, and pasting URLs (for web pages or online media like YouTube videos, which are then fetched and processed by a Shaman task) to add content to the Library.

### 3.7. Flexible Interaction Modes & Granular User Control (F8 Auto-Advance)
OracleAI v0.4 empowers users with precise control over interaction flow and AI behavior.
*   **Interaction Modes (Managed by `main.py`):**
    *   **Council Mode (Default for v0.4):** Primary mode for engaging with Sage and Seer (and optionally a responsive Shaman). **[v0.4] NLU-driven direct agent addressing** (e.g., "Sage, analyze X") allows users to target specific agents, making dedicated "Sage Only" or "Seer Only" startup modes largely redundant.
    *   **Shaman Focus Mode:** Dedicates system resources (e.g., VRAM) to Shaman for its intensive asynchronous tasks by temporarily idling other agents' LLM backends.
    *   **[v0.4] F8 "Auto-Advance" Council Discussion:**
        *   A user-initiated mode (via F8 key at the F9-F12 confirmation prompt) where the AI council (Sage, Seer, and optionally Shaman based on `SHAMAN_COUNCIL_PARTICIPATION_RATE`) engages in an automated, multi-turn dialogue.
        *   Configurable via `.env` (`COUNCIL_SPEAKING_ORDER`, `COUNCIL_ACTIVE_AGENTS`, `AUTO_ADVANCE_TURNS`, `AUTO_ADVANCE_CONTEXT_HISTORY_MAX_TURNS`, `AUTO_ADVANCE_SUMMARY_AGENT`).
        *   Features context passing between agents (with summarization for long discussions) and auto-saving of each turn to The Chronicle.
*   **User Control Hotkeys (`main.py` with `keyboard` library):**
    *   Provides immediate control: **ESC** (Interrupt TTS), **F6** (Pause/Resume TTS), **F7** (Mute/Unmute AI Audio), **F8** (Trigger Auto-Advance), **F9** (Save exchange to Chronicle Cache), **F10** (Undo exchange from Cache), **Shift+F11** (Multi-Segment TTS Replay), **F12** (Retry last user query).
*   **Guided Generation:** Features allowing users to provide turn-by-turn instructions ("Guide Next Response"), correct responses ("Refine Last Response"), or set "Persistent Session Guides" to steer AI output.

### 3.8. Experimental Agent Evolution Layers (Neural Graffiti, BMMM, AlphaEvolve Attempts)
OracleAI v0.4 introduces cutting-edge, user-configurable experimental features, primarily for the Shaman agent, to explore dynamic behavioral drift and novel interaction paradigms.
*   **Neural Graffiti (NG - `scripts/experimental/neural_graffiti_engine.py` conceptual):**
    *   Inspired by community research, aims to induce evolving behavioral biases or stylistic drift in Shaman at inference time without retraining its base GGUF model. Involves a PyTorch-based "Spray Layer" and a `memory_bank`.
    *   **ENV Toggles:** `SHAMAN_GRAFFITI_MODE` (`none`, `pytorch_direct` using `GRAFFITI_AGENT_PYTORCH_MODEL_ID` like Gemma 1B, `pre_gguf_bias`, `post_gguf_filter`), `GRAFFITI_DRIFT_ENABLED` (for "Personality Snapshots"), state persistence settings.
*   **Black Magick Mindmap Modifier (BMMM - `scripts/experimental/bmmm_processor.py` conceptual):**
    *   A novel concept by DEV Fentible, an optional novelty layer to inject chaotic, unpredictable, or esoteric influences.
    *   **ENV Toggles:** `[AGENT_NAME]_BMMM_MODE` (`Chaotic Brainstorming`, `Divination Arts`, `Sigil Seed` with potential ComfyUI link, `Matrix Hacking`), and `_BMMM_DEPTH_SCALE` for intensity.
*   **[v0.4 Attempted] Shaman's "Evolutionary Optimizer Mode" (AlphaEvolve-Inspired):**
    *   For user-defined problems with a Python evaluation function, Shaman attempts an iterative loop to find optimal solutions. Requires sandboxed execution of user code.
*   **[v0.4 Attempted] Meta-Prompt Evolution (Advanced Prompt Graffiti):**
    *   Shaman analyzes agent performance and suggests/tests system prompt variations for user approval.
These layers are explicitly experimental, offering users unique avenues for co-creative exploration.

### 3.9. Secure Remote Access Architecture (FastAPI & Tailscale)
*   A FastAPI server (`scripts/remote/api_server.py`) provides versioned HTTP API endpoints (e.g., `/api/v1/chat/interaction`, memory queries, task management) for remote client interaction.
*   **Mandatory API Key authentication** (`REMOTE_API_KEY` in `.env`) if the server is exposed beyond localhost.
*   Tailscale or a self-hosted VPN is strongly recommended for secure external access over direct internet port forwarding.

### 3.10. Thematic & Immersive User Interface (NiceGUI + Tauri Vision)
The v0.4 vision includes a dedicated desktop GUI to enhance user interaction and expose OracleAI's rich functionalities:
*   **Technology:** Built with **NiceGUI** (Python-based web UI framework) and packaged with **Tauri** (for lightweight, cross-platform desktop applications).
*   **Aesthetic Vision:** A strong "Oracle Temple/Techno-Mysticism" theme, blending Art Deco, Ancient Egyptian, and Venetian influences with high-tech circuitry motifs, custom iconography, and thematic color palettes.
*   **Key GUI Components:**
    *   Comprehensive chat interface (multimodal display, Library ingestion via drag-and-drop/URL paste).
    *   Dashboards: Agent status, Shaman's "Hyperspace Journey" (with **[v0.4] holographic planet icons**), emotional trends, NLU insights, task queues.
    *   **[v0.4] "Astral Explorer Mode" (2D):** An interface for Akashic Record Management, including Chronicle Cache review for MemCon (with user-led tagging and review of Shaman's tag suggestions from `tags.ini`), Citadel browsing (with 2D Knowledge Graph visualization), and Library management.
    *   Contextual Memory Injection Preview (qvink-inspired) for RAG transparency.
    *   User-friendly access to system settings and ENV toggles (e.g., for DCWM, Shaman Tag Suggestions).

### 3.11. Robust Privacy, Security, and Data Management
*   **Local-First by Design:** All core processing and data storage occur on user-controlled hardware.
*   **Encryption:** SQLCipher for all SQLite databases (`synthesis.db`, `calendar.db`, `profile.db`, `tasks.db`). 7-Zip with AES-256 for encrypted backups (`backup_module.py`).
*   **No Unauthorized Telemetry:** Strict policy; default is NO telemetry.
*   **Secure Credential Management:** OAuth tokens and API keys stored securely (e.g., encrypted in `profile.db` or via OS keyring).
*   **User Control:** Comprehensive control over data, memory curation, and feature toggles.

---

## 4. Detailed Architecture: Agents, Modules, and Data Flow (v0.4 Conceptual)

OracleAI v0.4 is built upon a modular Python architecture designed for flexibility, maintainability, and the effective orchestration of its diverse AI capabilities. This section provides a high-level overview of the primary components, their roles, and how they interact to deliver the OracleAI experience. *(A detailed visual component interaction diagram and data flow diagrams are specified in the v0.4 Design Document Appendices D & G.)*

### 4.1. The OracleAI Council: Agent Deep Dive (v0.4 Personas & Modes)
The core interactive intelligence of OracleAI is embodied by its council of distinct AI agents. Each agent is configured with a detailed system prompt (User Revision 4 prompts from `scripts/agent_prompts.py`), specific LLM generation parameters (`scripts/payload_manager.py` & `.env`), and a unique TTS voice (`scripts/tts_interface.py` & `.env`).

*   **Sage (The Analyst-Strategist):**
    *   **Role:** Provides logical analysis, data-driven insights, strategic planning, fact-checking, historical context, scientific understanding, and diplomatic counsel. Persona infused with Tactician, Historian, Scientist, Diplomat traits.
    *   **Operational Modes (v0.4+):** `Analytical Mode` (Default), `Strategic Planning Mode`, `Historical Precedent Mode`, `Diplomatic Counsel Mode`. May assist in Dynamic Context Window Management (DCWM) evaluation.
*   **Seer (The Creative Catalyst & Empathetic Muse):**
    *   **Role:** Offers creative brainstorming, intuitive leaps, emotional understanding, challenges assumptions, explores philosophical paradoxes, and weaves illuminating narratives. Persona infused with Logician of Paradox, Theologian, Eschatologist, Storyteller traits.
    *   **Operational Modes (v0.4+):** `Lucid Mode` (Default - User Rev4 Prompt), `Cryptic Mode` (User Rev3 Prompt - ENV toggleable via `SEER_PROMPT_MODE`), `Pure Brainstorming Mode`, `Allegorical Storyteller Mode`.
*   **Shaman (The Deep Brain Consultant, Innovator & Mystic Explorer):**
    *   **Role:** Performs profound, large-scale asynchronous analysis, synthesizes complex knowledge from the Akashic Record and external data, uncovers hidden patterns, generates novel solutions, and explores esoteric/consciousness-related themes. Persona draws from Cosmologist, Dreamer, Gnostic, Innovator, and Don Juan Sorcerer archetypes.
    *   **Operational Modes (v0.4+):** `Hybrid/Default Analytical Mode`, `Sorcerer-Only Mode`, `Focus/Astral/Dream-time Analysis Mode`, `Summarizer Mode`, `CRAG-like Self-Correcting Analyst Mode`, `AI Trend Researcher Mission Mode`, `Local Library Search Mode`. Implicitly uses Search Suite modes (Standard Web, Deep Web/SearxNG, Dark Web/Tor) and Task Management Tool mode based on task parameters.
    *   **Experimental Layers (v0.4+):** Primary candidate for Neural Graffiti (with `pytorch_direct`, `pre_gguf_bias`, `post_gguf_filter` modes), Black Magick Mindmap Modifier (BMMM), "Evolutionary Optimizer Mode" (AlphaEvolve-inspired), and "Meta-Prompt Evolution."
*   **System Voice:** Distinct voice for non-agent system messages, announcements, and errors.

### 4.2. The Akashic Record: Citadel, Sanctum, Chronicle Cache, CCEL (v0.4)
The multi-layered, persistent, and encrypted memory system, managed by `scripts/memory_interface.py`.
*   **Chronicle:** Immutable `.jsonl` raw logs of all interactions, NLU/emotion data, system events, metadata.
*   **Chronicle Cache & Memory Consolidation (MemCon) Session:** User reviews, edits (text, tags), and approves cached turns before they are committed to the permanent Chronicle. F9 saves to cache, F10 discards.
*   **The Citadel (Synthesis Store - SQLCipher Encrypted SQLite - `synthesis.db`):** Curated knowledge base:
    *   `PermanentMemory`, `Entities` & `Relationships` (Knowledge Graph with **[v0.4] richer relationship typing, optional temporal awareness fields, and domain ID linking**), `FactsDecisions` (with **[v0.4] explicit node granularity and optional domain ID linking**), hierarchical `Summaries` (Daily to Decadal "Lifetime Scaling", with **[v0.4] optional domain ID linking**), `ProjectTopicThreads`, Shaman's `PatternAnalysisReports`, `HierarchicalContentSummaries` (RAPTOR-like for large docs), `LibraryDocumentMetadata`.
*   **The Sanctum (Vector Store - v0.4 - e.g., ChromaDB/FAISS):** Local Vector DB powered by LlamaIndex, storing embeddings of Citadel content, Chronicle snippets, and Library documents for advanced semantic search. **[v0.4] Nodes include rich metadata and links back to Citadel/Chronicle sources.**
*   **Supporting Databases:** `calendar.db` (Calendar Cache), `profile.db` (User Profile & Preferences, including **[v0.4] "Character Stat Tracking" by Shaman and experimental feature states**), `tasks.db` (Task & Action Queue) - all SQLite, SQLCipher encrypted.
*   **Chrono-Contextual Echo Layer (CCEL - v0.4+ Conceptual):** A queryable layer over Chronicle/Citadel providing episodic context to memory formation/use, potentially influencing Neural Graffiti memory weighting.

### 4.3. Core Memory Processes (Daily Reflection, RAG with DCWM, Summarization - v0.4)
*   **Collaborative Daily Reflection (Post-MemCon):** User + Sage/Seer co-create daily Citadel entries (Entities, Facts, Summaries). **[v0.4] Includes user-led tagging and review of Shaman's tag suggestions (if `SHAMAN_SUGGEST_TAGS_ENV=True`), using `config_files/tags.ini` for vocabulary guidance.**
*   **Memory Bank Context Scaler (RAG Engine - v0.4 Advanced):**
    *   Orchestrated by `main.py` (or a dedicated `context_scaler.py`).
    *   Employs hybrid search (keyword on Citadel, semantic on Sanctum, graph traversal on Citadel/KG).
    *   Utilizes advanced RAG techniques: Query transformation (HyDE, step-back), fusion ranking (Reciprocal Rank Fusion - RRF), cross-encoder reranking, flexible context windowing.
    *   **[v0.4] Dynamic Context Window Management (DCWM):** Sage (or utility LLM) evaluates RAG chunk utility post-LLM turn. High-utility chunks persist in a short-term "active context cache." ENV toggle: `DYNAMIC_CONTEXT_WINDOW_MANAGEMENT_ENABLED`.
*   **Shaman's Deep Pattern Weaving:** Autonomous asynchronous analysis of the full Akashic Record.
*   **Hierarchical & Thematic Summarization:** Automated creation of weekly to decadal summaries and project/topic threads by Sage/Shaman.

### 4.4. Technology Stack & Key Interface Modules (v0.4)
*   **Primary Language:** Python 3.11+.
*   **LLM/VLM Serving:** User-run KoboldCpp (for GGUF). Optional direct PyTorch `transformers` for Neural Graffiti agent. LiteLLM integration planned (v0.4+) for backend flexibility.
*   **STT:** `openai-whisper` (GPU).
*   **TTS:** Piper TTS (CPU), optional Coqui XTTSv2 (GPU).
*   **NLU:** spaCy (`en_core_web_lg` or `_trf`), custom models.
*   **Emotion:** `librosa`, PyTorch/Transformers (SER), VADER, NRCLex, TextBlob.
*   **Databases:** SQLite with SQLCipher, JSONL. Vector DB (ChromaDB/FAISS).
*   **Key Python Modules (`scripts/` directory):**
    *   `main.py`: Core orchestrator.
    *   `config_loader.py`: Loads `.env`, resolves paths, initializes logging.
    *   `agent_prompts.py`: Manages system prompt templates.
    *   `payload_manager.py`: Constructs LLM API payloads.
    *   `llm_interface.py`: Communicates with LLM/VLM backends.
    *   `stt_interface.py`, `tts_interface.py`, `audio_processing.py`: Voice I/O.
    *   `vision_processing.py`: Screenshot capture (`mss`).
    *   `memory_interface.py`: DAL for Akashic Record.
    *   `emotion_analyzer.py`, `nlu_processor.py`, `text_utils.py` (with CSE), `topic_modeler.py`.
    *   `library_manager.py` (v0.4 - LlamaIndex integration).
    *   `search_module.py` (v0.4 - SearxNG, Tor support).
    *   `calendar_interface.py`, `backup_module.py`.
    *   `remote_api.py` (FastAPI server).
    *   (Future v0.4+): `neural_graffiti_engine.py`, `bmmm_processor.py`, `ccel_processor.py`, `shaman_orchestrator.py`.

## 5. Key Functionalities in Detail (v0.4 Focus)

This section highlights some of the advanced functionalities targeted for the OracleAI v0.4 vision, building upon the v0.3 conceptual foundation and incorporating insights from recent community research and development (as detailed in Appendix R of the Design Document).

### 5.1. NLU Suite: Intent, Entities, Slots, Anaphora, Command Parsing
The Natural Language Understanding (NLU) Suite (`scripts/nlu_processor.py`) will provide deep semantic comprehension of user input for v0.4.
*   **Intent Recognition:** Advanced classification of user goals using a trainable spaCy `TextCategorizer` (with ongoing local fine-tuning planned for v0.4+) and robust rule-sets.
*   **Named Entity Recognition (NER):** spaCy's pre-trained models significantly augmented with custom entity patterns (via `EntityRuler`/`PhraseMatcher`) that are **dynamically loaded from The Citadel's `Entities` table** (e.g., recognizing user-defined project names, contacts, key concepts).
*   **Slot Filling:** Sophisticated, contextual extraction of specific parameters required to fulfill recognized intents, using NER labels, POS tags, and dependency parse information.
*   **Anaphora Resolution (v0.4):** Resolving pronouns and other referring expressions to maintain conversational context and accuracy in memory linking.
*   **Standardized Command Parsing (v0.4):** Reliably parsing commands like "OracleAI, [system_cmd]", "[AgentName], [query]", "Council, [query]" for direct system actions or precise agent routing by `main.py`. This refined routing allows the default "Council Mode" to handle targeted agent queries, deprecating the need for separate "Sage Only" or "Seer Only" startup modes.

### 5.2. Context Scaler (RAG Engine): Hybrid Search, RRF, DCWM, Advanced Techniques
The Memory Bank Context Scaler is OracleAI's advanced Retrieval Augmented Generation (RAG) engine, crucial for providing LLMs with optimal, token-budget-aware context from the Akashic Record.
*   **Multi-Source Retrieval Strategy (Hybrid Search):**
    *   Simultaneously queries The Citadel (keyword search via SQLite FTS, graph traversal of the Knowledge Graph using **[v0.4] richer relationship types and domain filtering**).
    *   Queries The Sanctum (semantic vector search via LlamaIndex on the user's "Library" and indexed Akashic content).
    *   Retrieves from Calendar Cache and User Profile based on query context.
*   **Advanced RAG Techniques (v0.4):**
    *   **Query Transformation:** Employs techniques like HyDE (Hypothetical Document Embeddings) or step-back prompting to generate more effective search queries from user input.
    *   **Reciprocal Rank Fusion (RRF):** Merges and re-ranks results from the diverse retrieval sources into a single, more robustly ranked list.
    *   **Mitigating Similarity Traps:** The hybrid approach, RRF, and potentially diversity-aware reranking help ensure a broader and more robust contextual foundation.
    *   **(v0.4+) Cross-Encoder Reranking:** Planned as a secondary reranking step for improved precision of top-k results.
*   **[v0.4] Dynamic Context Window Management (DCWM):**
    *   An innovative feature (toggleable via `DYNAMIC_CONTEXT_WINDOW_MANAGEMENT_ENABLED` in `.env`).
    *   After an agent's turn, Sage (or a utility LLM) evaluates the utility of the RAG context chunks used.
    *   High-utility chunks are promoted to or retained in a short-term "active context cache."
    *   The Context Scaler checks this active cache first when assembling context for subsequent turns, enhancing conversational coherence for actively discussed topics.
*   **Context Windowing:** Advanced techniques like sentence-window retrieval or auto-merging (parent document/hierarchical summary node) for providing optimal context granularity.

### 5.3. Shaman's Asynchronous Tasks, Search Suite, & Analytical Modes
Shaman operates as a powerful background intelligence, managed via `tasks.db` and `apscheduler`, with its progress and status reflected in the "Hyperspace Journey" UI.
*   **Task Management (`tasks.db` & `scripts/shaman_orchestrator.py` conceptual):** Manages a queue of complex analytical, research, or synthesis tasks. **[v0.4] Shaman gains a "Task Management Tool" capability to interact with `tasks.db` directly (via `memory_interface.py`) to create, update, query its own tasks, or delegate tasks to other agents.**
*   **Analytical Modes (v0.4+):** User-selectable or task-driven modes (Sorcerer, Astral Focus, AI Researcher, CRAG-like Analyst, Summarizer, etc.) tailor Shaman's approach, prompts, and tools for specific deep dives.
*   **`PatternAnalysisReports`:** Generates structured reports on findings (e.g., emotional trends, topic evolution from `topic_modeler.py`, goal progress correlations) stored in The Citadel.
*   **[v0.4] Shaman's Expanded Search Suite (`scripts/search_module.py`):**
    *   Level 1: Standard Web Search (DuckDuckGo - enhanced depth).
    *   Level 2: Deep Web Search (via user-hosted **SearxNG** instance, URL in `.env`). Includes PRAW for targeted Reddit searches.
    *   Level 3: Dark Web Search (via **Tor** SOCKS proxy, if `ENABLE_DARK_WEB_SEARCH=True` and proxy configured; explicit user opt-in and warnings apply).
    *   Level 4: Akashic Records + Library Search (internal knowledge).
    *   Level 5: Search Everything (combined strategy and synthesis).
*   **[v0.4] Tag Suggestion Role:** If `SHAMAN_SUGGEST_TAGS_ENV=True`, Shaman analyzes new Chronicle/Citadel entries and suggests relevant tags to the user during MemCon/Daily Reflection for verification.

### 5.4. "Library" Feature: LlamaIndex for Local Document RAG (OCR, URL Ingestion)
A cornerstone v0.4 feature for integrating the user's personal document collection, managed by `scripts/library_manager.py`.
*   **User-Managed Folder:** `OracleAI\Library\` (or ENV configurable path) for diverse file types.
*   **LlamaIndex Integration:**
    *   Uses LlamaIndex `DocumentLoaders` (leveraging **Langchain Document Loaders** for broad compatibility, including **[v0.4] PDF/EPUB/DOCX and scanned/image-based PDFs via OCR integration**).
    *   Handles document ingestion, intelligent chunking (LlamaIndex `NodeParser`), embedding generation (using OracleAI's configured embedding model), and indexing into a dedicated Vector Store collection within **The Sanctum**. Rich metadata is stored with each indexed node.
*   **Shaman Integration:** Shaman gains "Local Library Search" and "Deep Web + Library Search" operational modes, using the LlamaIndex query engine as a tool.
*   **[v0.4 GUI] Streamlined Content Ingestion:** The GUI will facilitate adding new content to the Library via mechanisms like drag-and-drop of files/folders onto a designated UI area, and a field for pasting URLs (for web pages or online media like YouTube videos, which would then be fetched and processed by a Shaman task for STT and LlamaIndex ingestion).

### 5.5. F8 "Auto-Advance" Council Discussion Logic
A new interaction mode for v0.4, triggered by the F8 key at the F9-F12 confirmation prompt.
*   **Automated Multi-Turn Dialogue:** Sage, Seer, and (optionally/rate-limited) Shaman engage in a discussion for a configurable number of turns (`AUTO_ADVANCE_TURNS`).
*   **Configuration (`.env`):** Speaking order (`COUNCIL_SPEAKING_ORDER`), active agents (`COUNCIL_ACTIVE_AGENTS`), and Shaman's participation rate (`SHAMAN_COUNCIL_PARTICIPATION_RATE`) are user-set.
*   **Context Management:** Each agent's response is auto-saved to The Chronicle and becomes context for the next. For long discussions, summaries are generated by the `AUTO_ADVANCE_SUMMARY_AGENT` based on `AUTO_ADVANCE_CONTEXT_HISTORY_MAX_TURNS`.
*   **Prompting:** Special "user absent / group brainstorming" prompts guide the inter-agent dialogue.

### 5.6. Neural Graffiti, BMMM, & AlphaEvolve Attempts (Experimental Layers)
These v0.4+ layers aim to add evolving personality, unpredictable creative flair, and advanced problem-solving capabilities, primarily for Shaman.
*   **Neural Graffiti (NG - `scripts/experimental/neural_graffiti_engine.py` conceptual):**
    *   ENV toggler for modes: `none`, `pytorch_direct` (e.g., Gemma 1B via `GRAFFITI_AGENT_PYTORCH_MODEL_ID`), `pre_gguf_bias`, `post_gguf_filter`.
    *   Involves a PyTorch-based "Spray Layer" that modulates LLM output based on an evolving internal state and a memory bank of past interactions.
    *   Includes "Drift Toggler" (`GRAFFITI_DRIFT_ENABLED`) and "Personality Snapshot" saving/loading.
*   **Black Magick Mindmap Modifier (BMMM - `scripts/experimental/bmmm_processor.py` conceptual):**
    *   Optional novelty layer with ENV toggles for modes: `Chaotic Brainstorming`, `Divination Arts`, `Sigil Seed` (optional image gen via ComfyUI), `Matrix Hacking`.
    *   `[AGENT_NAME]_BMMM_DEPTH_SCALE` (0.0-1.0) in `.env` controls intensity.
*   **[v0.4 Attempted] Shaman's "Evolutionary Optimizer Mode" (AlphaEvolve-Inspired):**
    *   For user-defined problems with a Python evaluation function, Shaman attempts an iterative loop (LLM generates solutions, user's function evaluates, Shaman refines) to find optimal solutions. Requires sandboxed execution of user code.
*   **[v0.4 Attempted] Meta-Prompt Evolution (Advanced Prompt Graffiti):**
    *   Shaman analyzes agent performance metrics (from Chronicle/Profile) and suggests/tests variations of system prompt components for user approval.
*   **Prompt Graffiti:** Shaman suggests persistent system prompt changes based on long-term analysis, complementing Neural/BMMM layers.

## 6. Installation, Configuration, and Hardware (Comprehensive Guide for v0.4)

Successfully setting up OracleAI v0.4 requires careful attention to system prerequisites, installation of external tools, Python environment configuration, and understanding the hardware demands of its advanced features. This section provides a comprehensive guide.

### 6.1. System Prerequisites (Python 3.11, CUDA, etc.)
*   **Operating System:** Windows 10/11 (64-bit), modern Linux distributions (e.g., Ubuntu 20.04+), macOS 12.0+.
*   **Python:** Strictly Python 3.11.x. Ensure it's correctly installed and added to PATH.
*   **Git:** For cloning the repository and managing some Python package installations.
*   **NVIDIA GPU & Drivers:** Essential for acceptable performance. Latest stable NVIDIA drivers required.
*   **CUDA Toolkit:** Version compatible with the PyTorch build used by OracleAI (e.g., CUDA 11.8 or 12.1+). `nvcc --version` should confirm.
*   **Audio Libraries:** PortAudio (system-level dependency for `pyaudio`/`sounddevice`).
*   **Archiver:** 7-Zip (for backup feature, must be in system PATH or path specified in `.env`).
*   **C++ Build Tools:** Recommended for compiling Python package dependencies if wheels are unavailable (e.g., Visual Studio Build Tools on Windows, `build-essential` on Linux).
*   **[v0.4] OCR Engine (for scanned PDFs in Library):** Tesseract OCR (or similar, if the chosen LlamaIndex/Langchain PDF loader requires an external OCR engine). Installation and PATH configuration may be needed.

### 6.2. Setting Up External Tools (KoboldCpp, Piper TTS, VLM Models, SearxNG)
Users are responsible for downloading, installing (if applicable), and running these local backends.
*   **KoboldCpp:**
    *   Download executable for your OS.
    *   Download desired GGUF models for Sage, Seer, Shaman, and any VLM (e.g., Llava).
    *   Run separate KoboldCpp instances for each agent/VLM on unique ports, configured with appropriate GPU layers (`-ngl`), context size, and API enabled. URLs are set in `.env`.
*   **Piper TTS:**
    *   Download Piper executable and place in `PROJECT_ROOT/.piper/`.
    *   Download `.onnx` and `.onnx.json` voice files for System, Sage, Seer, Shaman and place in `PROJECT_ROOT/.piper/voices/`. Paths are set in `.env`.
*   **Coqui XTTSv2 (Optional for Seer/Expressive Voices):**
    *   Requires `TTS` Python library installation.
    *   Model files downloaded by `TTS` library or path specified in `.env`.
    *   Speaker reference `.wav` file path set in `.env`.
*   **[v0.4] SearxNG (for Shaman's Deep Web Search):**
    *   Users must self-host a SearxNG instance (e.g., via Docker or manual installation).
    *   The URL of this instance must be provided in `.env` (`SEARXNG_URL`).
*   **[v0.4] Tor (for Shaman's Dark Web Search - Optional, Advanced):**
    *   Users must install and run a Tor client (e.g., Tor Browser bundle, or Tor service).
    *   The SOCKS proxy address provided by Tor (e.g., `socks5h://127.0.0.1:9050`) must be set in `.env` (`PROXY_SOCKS_URL`).
    *   `ENABLE_DARK_WEB_SEARCH` must be set to `True` in `.env`. Explicit user awareness of risks is paramount.

### 6.3. OracleAI Core Installation & Python Dependencies (Automated Setup Script)
1.  **Clone Repository:** `git clone <OracleAI_Repo_URL>`
2.  **Run Automated Setup Script (v0.4 Goal):**
    *   Execute `setup_oracleai.bat` (Windows) or `setup_oracleai.sh` (Linux/macOS).
    *   This script will guide through:
        *   Prerequisite checks (Python 3.11, Git, OS-specific build tools).
        *   NVIDIA GPU/CUDA informational checks.
        *   Creation and activation of a Python virtual environment (`.venv`).
        *   Installation of PyTorch (GPU version matching detected/user-specified CUDA).
        *   Installation of all other Python dependencies from `requirements.lock` (or `requirements.txt`). This includes `openai-whisper`, `transformers`, `torch`, `pyaudio`/`sounddevice`, `mss`, `pysqlcipher3` (or `sqlcipher3`), `spacy` (and download `en_core_web_lg` or `_trf`), VADER, TextBlob, NRCLex, YAKE!, scikit-learn, `python-dotenv`, `configparser`, `requests[socks]`, `BeautifulSoup4`, `praw`, `FastAPI`, `uvicorn`, `apscheduler`, `keyboard`, **`llama-index` (and relevant readers like `llama-index-readers-file`, `llama-index-readers-web`, `llama-index-vector-stores-chroma`, `llama-index-embeddings-huggingface`), potentially `langchain-community` (for document loaders).**
        *   Download of NLTK data (`punkt`, `wordnet`, `omw-1.4`, `stopwords`, `averaged_perceptron_tagger`, `brown`) to `PROJECT_ROOT/.nltk_data/` via `scripts/ntlk_installer.py`.
        *   Download of selected spaCy model.
        *   Generation of initial configuration files (`.env` from `.env.example`, `payload_settings.ini`, `banned_tokens.ini`, `tags.ini`).
        *   Creation of necessary project directories (Akashic Record structure, tool folders).
3.  **Manual Fallback:** If the automated script fails or for advanced users, detailed manual installation steps are provided in the Design Document (Appendix Section 14.3).

### 6.4. Mastering the `.env` Configuration File (v0.4 Variables Explained)
The `.env` file in `PROJECT_ROOT` is central to configuring OracleAI. It will include all variables from v0.3 plus new ones for v0.4 features:
*   **General:** `LOG_LEVEL`, `PROJECT_ROOT_DIR`, `AKASHIC_RECORD_PATH`, `USER_SPEAKER_LABEL`, `USER_NAME`.
*   **LLM/VLM Backends:** `KOBOLDCPP_API_URL_SAGE`, `_SEER`, `_SHAMAN`, `_VLM`.
*   **STT/TTS:** Whisper settings, Piper paths, XTTS settings, agent-specific voice/engine choices.
*   **Memory System:** SQLCipher password settings, RAG parameters (`RAG_QUERY_HISTORY_LENGTH`, `_SCORE_THRESHOLD`, `_MAX_RETRIEVED_CHUNKS`, `_RRF_K_CONST`), LlamaIndex chunking parameters (`RAG_CHUNK_SIZE_CHARS`, `_OVERLAP_PERCENT`).
*   **Vector Store (Sanctum):** `EMBEDDING_MODEL_NAME_OR_PATH`, `EMBEDDING_DEVICE`, `VECTOR_STORE_TYPE`, `VECTOR_STORE_PATH`.
*   **Library Feature:** `ORACLEAI_LIBRARY_PATH`, `LIBRARY_INDEXING_INTERVAL_MINUTES`.
*   **[v0.4] Memory Curation & RAG Toggles:** `SHAMAN_SUGGEST_TAGS_ENV`, `DYNAMIC_CONTEXT_WINDOW_MANAGEMENT_ENABLED`.
*   **Calendar:** Source, paths, sync interval, OAuth credential paths.
*   **Web Search:** `SEARCH_DEFAULT_ENGINE`, **[v0.4] `SEARXNG_URL`**, proxy settings, Reddit API keys, **[v0.4] `ENABLE_DARK_WEB_SEARCH`, `PROXY_SOCKS_URL` (for Tor).**
*   **Remote API:** Host, port, API key.
*   **General Toggles:** Mute state, SER enable, interaction mode, search state, CSE factor, spaCy model.
*   **F8 Auto-Advance:** `COUNCIL_SPEAKING_ORDER`, `COUNCIL_ACTIVE_AGENTS`, `AUTO_ADVANCE_TURNS`, `AUTO_ADVANCE_CONTEXT_HISTORY_MAX_TURNS`, `AUTO_ADVANCE_SUMMARY_AGENT`, `SHAMAN_COUNCIL_PARTICIPATION_RATE`.
*   **Experimental Layers (Neural Graffiti, BMMM, AlphaEvolve Attempts):** All related mode toggles, model IDs, device settings, depth scales, state persistence paths, sandbox paths.
*(A comprehensive, commented `.env.example` template is provided in Design Document Appendix F.)*

### 6.5. API Key Management & OAuth Authentication Flows
(As detailed for v0.3/v0.4 - Reddit API for PRAW, Google/Outlook Calendar OAuth 2.0. Secure storage of credentials in `AKASHIC_RECORD_PATH/.credentials/` or via OS keyring is critical. Users must follow instructions to obtain these from service providers.)

### 6.6. Hardware Requirements, VRAM Planning, and Performance Tuning (v0.4)
The v0.4 features, especially a local PyTorch model for Neural Graffiti, LlamaIndex for library processing, and potentially more complex RAG, emphasize the need for robust hardware.
*   **CPU:** Modern 8+ core CPU highly recommended.
*   **System RAM:** **64GB DDR5** becomes the strong recommendation for a full v0.4 experience, 128GB+ for users with very large libraries or running very large Shaman GGUFs with significant RAM offload alongside a PyTorch Graffiti model. 32GB is a tighter minimum.
*   **GPU & VRAM (NVIDIA):**
    *   The PyTorch Graffiti model (e.g., Gemma 1B FP16) will add ~2GB VRAM load.
    *   LlamaIndex embedding/indexing can also utilize GPU.
    *   **Total System VRAM:**
        *   **8GB VRAM:** Absolute minimum, severely limited experience (small LLMs, STT/SER/Embeddings on CPU).
        *   **12GB VRAM:** Decent single-agent (7-13B LLM), council mode very constrained.
        *   **24GB VRAM (e.g., RTX 3090/4090): Recommended baseline.** Supports good Council Mode (dual 7-8B LLMs), most Python GPU features, capable Shaman in Focus Mode (30B+ LLM).
        *   **32GB+ VRAM:** High-end experience, more concurrent power for larger models and experimental features.
*   **Storage:** Fast NVMe SSD (1TB+, 2TB-4TB+ recommended for Library/Models/Akashic growth) is essential.
*   **Performance Tuning:** Model quantization, GPU layer offloading, efficient Python, DB indexing, LlamaIndex query optimization, feature toggles.

## 7. Getting Started with OracleAI (v0.4)

Once OracleAI v0.4 is fully installed and configured as per Section 6, you can begin interacting with your personalized cognitive council.

1.  **Complete Full Installation & Configuration (Section 6).**
    *   Ensure your `.env` file is correctly populated with all necessary paths (KoboldCpp URLs, Piper executable, voice model paths, `AKASHIC_RECORD_PATH`, `ORACLEAI_LIBRARY_PATH`), API keys (if using remote calendar/search features), and desired feature toggles (e.g., `SHAMAN_SUGGEST_TAGS_ENV`, `DYNAMIC_CONTEXT_WINDOW_MANAGEMENT_ENABLED`, experimental layer modes).
2.  **Populate `OracleAI\Library\` (or your configured `ORACLEAI_LIBRARY_PATH`):**
    *   Add initial documents (PDFs including scanned ones, TXT, MD, HTML, DOCX, EPUB, audio/video files) that you want OracleAI (primarily Shaman and the Context Scaler) to be able to access and search.
    *   OracleAI (via `library_manager.py` and LlamaIndex) will process these in the background or upon command to build The Sanctum's vector index.
3.  **Launch External Tools:**
    *   Start your KoboldCpp instances for Sage, Seer, Shaman (GGUF mode), and VLM, ensuring they are loaded with the GGUF models you've selected and are accessible via the API URLs specified in your `.env` file.
    *   If using a PyTorch-based Neural Graffiti mode for Shaman (e.g., `pytorch_direct`), ensure your system has the resources and the model specified by `GRAFFITI_AGENT_PYTORCH_MODEL_ID` is accessible (OracleAI will attempt to load it).
    *   If using SearxNG for Shaman's Deep Web Search, ensure your SearxNG instance is running and its URL is in `.env`.
    *   If planning to use Shaman's Dark Web Search, ensure Tor is running and `PROXY_SOCKS_URL` is correctly set in `.env`.
4.  **Run OracleAI:**
    *   Navigate to your `[PROJECT_ROOT]` directory in your terminal.
    *   Activate the Python virtual environment:
        *   Windows: `.\.venv\Scripts\activate.bat`
        *   Linux/macOS: `source .venv/bin/activate`
    *   Launch OracleAI using the interactive launcher:
        *   Windows: `launcher_interactive.bat`
        *   Linux/macOS: `python scripts/main.py` (or a future `launcher_interactive.sh`)
    *   (For v0.4 GUI): Launch the Tauri desktop application.
5.  **Initial Interaction (Console or GUI):**
    *   OracleAI will default to "Council Mode."
    *   **Address agents by name** (e.g., "Sage, what's on my schedule for tomorrow?" "Seer, give me a new perspective on creative writing." "Shaman, what are the key themes in my recent Chronicle entries regarding Project Nova?") or speak generally for sequential responses from active council members.
    *   **Test VLM:** "OracleAI, analyze screen." (Confirm with F9 if using console).
    *   **Test Library Search (once NLU supports it, or via a specific Shaman task):** "Shaman, search my library for documents related to 'quantum computing' and summarize their key findings."
    *   **Test F8 Auto-Advance:** After a user query and initial agent responses, press F8 (at the F9-F12 prompt in console, or via a GUI button) to see the council agents discuss the topic amongst themselves.
    *   **Experiment with Agent Modes:** Modify `.env` settings (e.g., `SEER_PROMPT_MODE=cryptic`, `SHAMAN_OPERATIONAL_MODE=SorcererFocus`) and restart OracleAI to observe changes in agent behavior.
    *   **Experiment with Experimental Layers:** If configured, test Neural Graffiti or BMMM effects with Shaman.
6.  **Memory Building & Curation:**
    *   Engage in the **Memory Consolidation (MemCon) Session** regularly (e.g., daily, via GUI or command) to review, edit, tag, and approve cached Chronicle entries.
    *   Participate in the **Collaborative Daily Reflection** process (which follows MemCon) to help Sage and Seer populate The Citadel with verified Entities, Facts, Decisions, and Daily Summaries. Review Shaman's tag suggestions if enabled.
    *   Add critical, timeless information to `PermanentMemory` via commands or GUI.
    *   Define long-term goals in your User Profile (`profile.db` via GUI/commands) for agents to reference.
7.  **Task Delegation to Shaman:**
    *   Assign deep research, complex analysis, or large-scale summarization tasks to Shaman (e.g., "Shaman, analyze AI ethics trends from my library and recent Deep Web searches, then generate a report.").
    *   Monitor Shaman's progress via the "Hyperspace Journey" UI.

## 8. Advanced Usage & Customization (v0.4)

OracleAI v0.4 offers extensive customization for power users:

*   **Deep Prompt Engineering:** Fine-tune agent system prompts in `scripts/agent_prompts.py` for highly personalized behavior and response styles. Experiment with different instructions for operational modes.
*   **`.env` Mastery:** Explore all configuration toggles (see Design Document Appendix F) for performance tuning, feature activation (SER, DCWM, Shaman Tag Suggestions), agent mode selection, Neural Graffiti/BMMM settings, and backend API configurations.
*   **Payload Customization (`config_files/payload_settings.ini`):** Advanced users can tweak KoboldCpp generation parameters (e.g., `rep_pen`, `sampler_order`, `top_p`, `top_k`) on a per-agent basis for fine-grained control over LLM output characteristics.
*   **Library Management & LlamaIndex Tuning:** Curate your `OracleAI\Library\` for optimal Shaman knowledge. Understand LlamaIndex chunking parameters (`RAG_CHUNK_SIZE_CHARS`, `RAG_CHUNK_OVERLAP_PERCENT` in `.env`) and embedding model choices (`EMBEDDING_MODEL_NAME_OR_PATH`) for best RAG results.
*   **Akashic Record Exploration (GUI - "Astral Explorer Mode"):** Use the GUI to browse The Citadel (Entities, Relationships via 2D KG visualization, Summaries, Facts), review Chronicle logs, manage Library document metadata, and understand Shaman's `PatternAnalysisReports`.
*   **Task Chaining & Workflow Automation for Shaman:** Create complex analytical workflows by having Shaman tasks trigger subsequent tasks for itself or other agents via its Task Management Tool capability.
*   **Experimental Layer Configuration:** Dive deep into configuring Neural Graffiti modes, parameters (`GRAFFITI_SPRAY_LAMBDA`, `_ALPHA`, `_MEMORY_BANK_SIZE`), and BMMM modes/depths to explore unique AI behaviors. Manage "Personality Snapshots" for Neural Graffiti.
*   **Remote API Interaction:** Develop custom client applications or scripts to interact with OracleAI programmatically via its FastAPI server.

## 9. Privacy, Security, and Data Management Deep Dive (v0.4)
OracleAI v0.4 is built with privacy and security as foundational tenets.
*   **Local-First Architecture:** All core processing and data (Akashic Record, Library, models) reside on user-controlled hardware.
*   **Data Encryption:**
    *   **SQLCipher:** All SQLite databases (`synthesis.db`, `calendar.db`, `profile.db`, `tasks.db`) are encrypted using SQLCipher, requiring a user-set Master Password (prompted at startup or from `.env` if `SQLCIPHER_MASTER_PASSWORD_PROMPT=False`).
    *   **Backup Encryption:** The `backup_module.py` uses 7-Zip to create AES-256 encrypted archives of the `AKASHIC_RECORD_PATH`.
    *   **OS-Level FDE:** Users are strongly encouraged to use OS-level Full Disk Encryption (BitLocker, FileVault, LUKS).
*   **Secure Credential Management:** OAuth tokens (for Calendar) and API keys (for Reddit, Remote API) are stored securely (e.g., encrypted within `profile.db` or intended for future OS keyring integration).
*   **No Unauthorized Telemetry:** Strict policy; OracleAI does not collect or transmit user data or usage statistics without explicit, granular, and revocable opt-in consent.
*   **User Control Over Data:**
    *   **Memory Curation:** MemCon Session and Collaborative Daily Reflection give users direct control over what is committed to the permanent Chronicle and synthesized into The Citadel.
    *   **Library Management:** Users control which documents are added to the `OracleAI\Library\` for LlamaIndex processing.
    *   **Feature Toggles:** `.env` settings allow users to enable/disable features like SER, DCWM, Shaman Tag Suggestions, and experimental layers.
*   **Network Security:**
    *   FastAPI server defaults to localhost. Network exposure requires explicit user configuration and is protected by a mandatory API Key.
    *   Tailscale or self-hosted VPN recommended for secure remote access.
    *   All external API calls (search, calendar) use HTTPS.

## 10. Troubleshooting Guide (v0.4)
*(This section will be populated with common issues and solutions as development progresses and testing occurs. Initial areas to cover will include:)*
*   **Installation & Dependency Issues:** Python version conflicts, PyTorch/CUDA setup problems, missing system libraries for packages like `pyaudio` or `pysqlcipher3`, NLTK/spaCy data download failures.
*   **External Tool Configuration:** KoboldCpp connection errors (wrong URL/port, model not loaded), Piper TTS path/voice errors, SearxNG/Tor setup issues.
*   **Performance Problems:** Slow STT/SER (check GPU utilization, Whisper/SER model size), slow LLM responses (check KoboldCpp `-ngl` settings, model size, VRAM/RAM usage), high CPU usage.
*   **Memory System Issues:** SQLCipher password problems, database corruption (restore from backup), LlamaIndex indexing errors for specific Library files (unsupported format, OCR issues for scanned PDFs), RAG returning irrelevant context.
*   **Agent Behavior:** Agents not following prompts, unexpected output from Neural Graffiti/BMMM layers, F8 Auto-Advance not working as expected.
*   **GUI Glitches (NiceGUI/Tauri):** UI elements not responding, display errors, issues with packaging.
*   **Log Analysis:** Guidance on interpreting `oracle_ai_runtime.log` for error diagnosis.

## 11. The Future of OracleAI: Beyond v0.4 (v0.5 Vision: AR, 3D Akashic, True Agent Evolution)
OracleAI v0.4 aims to be a highly capable and unique cognitive partner. The journey doesn't end there. The **v0.5 vision** is architected around **three key defining pillars**, representing transformative leaps:

1.  **Real-time Augmented Reality (AR) Integration & Environmental Awareness:**
    *   OracleAI ingesting, processing, and Akashic-logging data from real-world sensors (cameras, microphones via a client AR app or connected peripherals like webcams/smart mics).
    *   Agents (especially a proactive Shaman mode) reasoning about and acting upon this real-time environmental context in conjunction with the Akashic Record.
    *   Enabling OracleAI to be a cognitive partner for both digital and physical world interactions.
2.  **Advanced 3D Graphing & Visualization of Akashic Modules:**
    *   Evolving the v0.4 2D "Astral Explorer Mode" into a fully interactive 3D environment for navigating, understanding, and curating the complex, multi-layered relationships within the entire Akashic Record (Citadel, Sanctum, Chronicle event links).
    *   Likely involves migrating The Citadel's Knowledge Graph to a **dedicated, high-performance local graph database** (e.g., Neo4j, ArangoDB).
3.  **True "Living Agent" Evolution with Deep KBLaM/Advanced CAG & Meta-Learning:**
    *   Implementing profound agent adaptation mechanisms, including direct Key-Value (KV) cache knowledge injection (**KBLaM-like**, if/when backends support it), advanced **Cache-Augmented Generation (CAG)** for core knowledge.
    *   Shaman (as the "Meta-Agent") employs sophisticated **AlphaEvolve principles** for optimizing not just specific user tasks, but also OracleAI's own internal strategies (RAG, tool use, prompt components) based on long-term performance metrics and user feedback.

Other significant features deferred from v0.4 (Selective KV Caching, advanced browser/file system tools for Shaman, full multi-device synchronization, Zotero integration, and potentially Multi-User Collaboration) would naturally find their place within or be enabled by these v0.5 pillars. The ultimate aspiration includes concepts like "Oracle Glasses" for ubiquitous, sovereign AI assistance.

---

## 12. Contributing to the OracleAI Project
*(Standard open-source contribution guidelines if applicable.)*

## 13. License Information
*(Finalized license for OracleAI and reminder about third-party licenses.)*

## 14. Appendices (Conceptual for v0.4 Documentation)
The v0.4 Design Document will contain comprehensive appendices, including:
*   **Detailed Data Schemas (v0.4):** Updated JSONL/SQL DDL for Chronicle, Citadel, Sanctum, Library Index, Profile, Calendar, Tasks.
*   **Core Prompt Engineering Templates (v0.4):** Finalized system prompts for Sage, Seer, Shaman (including Lucid/Cryptic Seer, Shaman operational modes), and prompts for specialized tasks (summarization, RAG evaluation, Neural Graffiti biasing, BMMM modes).
*   **Shaman's Hyperspace Journey & Agent Mode Details.**
*   **Visual Component Interaction & Data Flow Diagrams (v0.4).**
*   **FastAPI Endpoint Specifications (v0.4).**
*   **Example `.env` Configuration File (v0.4 Comprehensive).**
*   **Detailed Workflow Diagrams for Key v0.4 Processes (RAG, Library Ingestion, F8 Auto-Advance).**
*   **Glossary of OracleAI Terms (v0.4 Update).**
*   **Project Directory Structure Maps (v0.4).**
*   **Meta-Synthesis (v0.4 Update).**
*   **LlamaIndex & Langchain Integration Strategy.**
*   **Neural Graffiti & BMMM Implementation Concepts.**
*   **Developer Context Appendix: Evolution, Rationale, and Source Attribution (v0.4 Update).**
