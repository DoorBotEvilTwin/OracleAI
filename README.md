# OracleAI ReadMe - Comprehensive Guide (v0.4 Vision)
A local AI assistant comprised of an emotionally aware multi-agent LLM council (Sage, Seer, Shaman) with an evolving PMEM (Akashic Record) for augmented cognition, deep insight and strategic guidance.

**Version:** 0.4 (Conceptual Design & Feature Roadmap)

**Status:** Advanced Development Phase

**Project Focus:** A deeply integrated, privacy-centric, local-first AI framework featuring a multi-agent council (Sage, Seer, Shaman) with a persistent, evolving "Akashic Record" memory system, advanced NLU & Emotional Intelligence, and multimodal capabilities, designed for profound cognitive augmentation, strategic guidance, and personalized interaction.

*(Conceptual Image: A triptych or composite image. Center: The intricate, unmasked Shaman figure, surrounded by flowing "DataSide" energy and geometric patterns, representing the core OracleAI intelligence and the Akashic Record. Left: Sage, with cool blue/silver geometric circuitry, focused and analytical. Right: Seer, with warm red/orange flame-like energy integrated into its circuitry, intuitive and perceptive. The background blends the "Oracle Temple" aesthetic with subtle cosmic vistas and circuit-board motifs.)*

<img src="https://raw.githubusercontent.com/DoorBotEvilTwin/OracleAI/refs/heads/main/OracleAI.jpg">

---

## Table of Contents

*   [1. Introduction: The OracleAI Vision](#1-introduction-the-oracleai-vision)
    *   [1.1. Beyond Assistance: A Cognitive Partner & Strategic Council](#11-beyond-assistance-a-cognitive-partner--strategic-council)
    *   [1.2. The Imperative of Local-First, Private, and Sovereign AI](#12-the-imperative-of-local-first-private-and-sovereign-ai)
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
    *   [3.2. The Akashic Record: Advanced Memory System (Citadel & Sanctum)](#32-the-akashic-record-advanced-memory-system-citadel--sanctum)
    *   [3.3. Comprehensive Emotional Intelligence Suite (SER & Text)](#33-comprehensive-emotional-intelligence-suite-ser--text)
    *   [3.4. Advanced Natural Language Understanding (NLU) Suite](#34-advanced-natural-language-understanding-nlu-suite)
    *   [3.5. High-Fidelity Multimodal Input/Output (Voice, Text, Vision)](#35-high-fidelity-multimodal-inputoutput-voice-text-vision)
    *   [3.6. Sophisticated Web Search & "Library" Integration (LlamaIndex)](#36-sophisticated-web-search--library-integration-llamaindex)
    *   [3.7. Flexible Interaction Modes & Granular User Control (F8 Auto-Advance)](#37-flexible-interaction-modes--granular-user-control-f8-auto-advance)
    *   [3.8. Experimental Agent Evolution Layers (Neural Graffiti, BMMM)](#38-experimental-agent-evolution-layers-neural-graffiti-bmmm)
    *   [3.9. Secure Remote Access Architecture (FastAPI & Tailscale)](#39-secure-remote-access-architecture-fastapi--tailscale)
    *   [3.10. Thematic & Immersive User Interface (Conceptual Vision for GUI)](#310-thematic--immersive-user-interface-conceptual-vision-for-gui)
    *   [3.11. Robust Privacy, Security, and Data Management](#311-robust-privacy-security-and-data-management)
*   [4. Detailed Architecture: Agents, Modules, and Data Flow (v0.4 Conceptual)](#4-detailed-architecture-agents-modules-and-data-flow-v04-conceptual)
    *   [4.1. The OracleAI Council: Agent Deep Dive (v0.4 Personas & Modes)](#41-the-oracleai-council-agent-deep-dive-v04-personas--modes)
    *   [4.2. The Akashic Record: Citadel, Sanctum, Chronicle Cache, CCEL (v0.4)](#42-the-akashic-record-citadel-sanctum-chronicle-cache-ccel-v04)
    *   [4.3. Core Memory Processes (Daily Reflection, RAG, Summarization - v0.4)](#43-core-memory-processes-daily-reflection-rag-summarization---v04)
    *   [4.4. Technology Stack & Key Interface Modules (v0.4)](#44-technology-stack--key-interface-modules-v04)
*   [5. Key Functionalities in Detail (v0.4 Focus)](#5-key-functionalities-in-detail-v04-focus)
    *   [5.1. NLU Suite: Intent, Entities, Slots, Anaphora, Command Parsing](#51-nlu-suite-intent-entities-slots-anaphora-command-parsing)
    *   [5.2. Context Scaler (RAG Engine): Hybrid Search, RRF, Advanced Techniques](#52-context-scaler-rag-engine-hybrid-search-rrf-advanced-techniques)
    *   [5.3. Shaman's Asynchronous Tasks & Analytical Modes](#53-shamans-asynchronous-tasks--analytical-modes)
    *   [5.4. "Library" Feature: LlamaIndex for Local Document RAG](#54-library-feature-llamaindex-for-local-document-rag)
    *   [5.5. F8 "Auto-Advance" Council Discussion Logic](#55-f8-auto-advance-council-discussion-logic)
    *   [5.6. Neural Graffiti & BMMM (Experimental Layers - Conceptual)](#56-neural-graffiti--bmmm-experimental-layers---conceptual)
*   [6. Installation, Configuration, and Hardware (Comprehensive Guide for v0.4)](#6-installation-configuration-and-hardware-comprehensive-guide-for-v04)
    *   [6.1. System Prerequisites (Python 3.11, CUDA, etc.)](#61-system-prerequisites-python-311-cuda-etc)
    *   [6.2. Setting Up External Tools (KoboldCpp, Piper TTS, VLM Models)](#62-setting-up-external-tools-koboldcpp-piper-tts-vlm-models)
    *   [6.3. OracleAI Core Installation & Python Dependencies](#63-oracleai-core-installation--python-dependencies)
    *   [6.4. Mastering the `.env` Configuration File (v0.4 Variables)](#64-mastering-the-env-configuration-file-v04-variables)
    *   [6.5. API Key Management & OAuth Authentication Flows](#65-api-key-management--oauth-authentication-flows)
    *   [6.6. Hardware Requirements, VRAM Planning, and Performance Tuning (v0.4)](#66-hardware-requirements-vram-planning-and-performance-tuning-v04)
*   [7. Getting Started with OracleAI (v0.4)](#7-getting-started-with-oracleai-v04)
*   [8. Advanced Usage & Customization (v0.4)](#8-advanced-usage--customization-v04)
*   [9. Privacy, Security, and Data Management Deep Dive (v0.4)](#9-privacy-security-and-data-management-deep-dive-v04)
*   [10. Troubleshooting Guide (v0.4)](#10-troubleshooting-guide-v04)
*   [11. The Future of OracleAI: Beyond v0.4 (Oracle Glasses & Research)](#11-the-future-of-oracleai-beyond-v04-oracle-glasses--research)
*   [12. Contributing to the OracleAI Project](#12-contributing-to-the-oracleai-project)
*   [13. License Information](#13-license-information)
*   [14. Appendices (Conceptual for v0.4 Documentation)](#14-appendices-conceptual-for-v04-documentation)
    *   (List of planned appendices for the v0.4 Design Document, e.g., Detailed Schemas, Prompt Templates, Diagrams, Glossary, Developer Context History)

---

## 1. Introduction: The OracleAI Vision

OracleAI (originating from **Fentible on May 5th, 2025, as an evolution of the "Vector Companion" project by SingularityMan**) represents a paradigm shift from conventional AI assistants. It is conceived as an **AI-powered cognitive ecosystem**, a deeply integrated suite of intelligent agents and sophisticated memory systems designed to function as an extension of the user's own mind and a strategic partner in their personal and professional endeavors. This document outlines the vision, architecture, and features for OracleAI version 0.4, representing a significant leap towards a fully realized, locally-run, privacy-centric cognitive augmentation framework.

### 1.1. Beyond Assistance: A Cognitive Partner & Strategic Council

Traditional AI assistants often focus on reactive task completion or simple information retrieval. OracleAI aims for a more profound level of integration and support:

*   **Augmented Cognition:** To enhance the user's ability to think critically, remember vast amounts of personal and external information effectively, and connect disparate concepts in novel and insightful ways.
*   **Strategic Guidance & Decision Support:** To assist in defining complex goals, formulating robust plans, analyzing multifaceted situations, and making well-informed decisions by leveraging a council of AI agents (Sage, Seer, Shaman) with diverse "thinking" styles and specialized knowledge domains.
*   **Persistent Learning & Deep Personalization:** To build a rich, evolving understanding of the user—their projects, preferences, communication style, emotional patterns, and interaction history—over extended periods. This is enabled by the **Akashic Record**, OracleAI's unique, multi-layered persistent memory system.
*   **Enhanced Self-Understanding & Reflection:** By providing tools for memory reflection, pattern analysis (via the Shaman agent), and tracking emotional or behavioral trends, OracleAI can offer users unique insights into their own cognitive and affective processes.
*   **Creative & Innovative Catalyst:** To serve as a sophisticated brainstorming partner (primarily via the Seer agent, but also through Shaman's innovative capabilities), helping users explore new ideas, challenge assumptions, and overcome creative or analytical blocks.

OracleAI is not merely a tool to be commanded; it is envisioned as a system to **collaborate with**, a digital extension that grows in utility, understanding, and alignment through continuous, nuanced interaction with the user.

### 1.2. The Imperative of Local-First, Private, and Sovereign AI

In an era where data privacy is increasingly paramount and reliance on cloud infrastructure can introduce vulnerabilities and dependencies, OracleAI champions a **local-first, privacy-centric, and data-sovereign paradigm.** This philosophy is non-negotiable and underpins every architectural decision.

*   **Data Sovereignty & Control:** The user unequivocally owns and controls their entire Akashic Record and all associated OracleAI data. This information resides on their personal hardware.
*   **Local Processing:** All core AI computations—LLM/VLM inference (via user-run KoboldCpp instances), Speech-to-Text (STT), Text-to-Speech (TTS), Speech Emotion Recognition (SER), Natural Language Understanding (NLU), and all memory operations—are performed locally.
*   **Offline Functionality:** Core features are designed to operate effectively without requiring constant internet connectivity. External network access is an explicit, user-controlled choice for specific functionalities (e.g., web search, calendar synchronization, library acquisition).
*   **Enhanced Security:** Multi-layered security measures, including OS-level Full Disk Encryption (user-managed, strongly recommended), application-level database encryption (SQLCipher for all SQLite stores within the Akashic Record), and encrypted backup options, are implemented to protect user data.
*   **Transparency & Trust:** Clear documentation, open-source code for core components, and user-verifiable memory processes (like the Collaborative Daily Reflection) aim to build a relationship of trust.
*   **No Unauthorized Telemetry:** OracleAI is architected to prevent the collection or transmission of user data, usage statistics, or system telemetry without explicit, informed, granular, and revocable user consent for clearly defined, anonymized purposes. The default is **NO telemetry**.

This commitment to local operation and data sovereignty ensures that OracleAI serves as a private, secure, and trustworthy cognitive partner.

---

## 2. Core Philosophy & Guiding Design Principles

The architecture, development, and functionality of OracleAI are deeply rooted in a set of core philosophies and guiding principles. These are not merely aspirational but are actionable directives shaping every design decision, implementation choice, and user interaction paradigm. They ensure OracleAI evolves as a powerful, trustworthy, and genuinely beneficial cognitive partner that respects user agency and data sovereignty.

### 2.1. Absolute Data Sovereignty & Local-First Processing
This is the paramount principle. All core AI computations—including LLM/VLM inference (via user-run KoboldCpp instances), STT (via `openai-whisper`), primary TTS (Piper and/or Coqui XTTSv2), Speech Emotion Recognition (SER), Natural Language Understanding (NLU), and all operations on the Akashic Record (storage, retrieval, synthesis)—**must** reside and execute exclusively on user-controlled hardware. The entirety of the user's Akashic Record **must** be stored locally. No personal conversational data, memory content, or derived insights are transmitted to any external servers or third parties without explicit, informed, and granular user consent for specific, user-initiated actions (e.g., encrypted backups to a user-chosen location, opt-in API calls for search or calendar sync). This commitment ensures maximum user privacy, data ownership, operational control, and robust offline functionality.

### 2.2. Multi-Agent Synergy: The Power of Diverse Intelligences
OracleAI employs a council of distinct AI agents (Sage, Seer, and Shaman), each endowed with specialized roles, meticulously crafted system prompts defining their cognitive styles, distinct LLM temperature settings, and unique vocal personas. This multi-agent architecture is designed to emulate the benefits of diverse human teams, where logical analysis (Sage), creative intuition and emotional intelligence (Seer), and profound, deep synthesis (Shaman) converge. This synergy enables more robust problem analysis, balanced decision support, comprehensive strategic planning, and a richer, more engaging user interaction than a monolithic AI could provide. Agents are designed to collaborate, challenge each other constructively (especially in "Auto-Advance" mode), and offer multifaceted perspectives.

### 2.3. The Akashic Record: A Deep, Evolving, and Living Memory
The Akashic Record is the dynamic, structured, and persistent cognitive backbone of OracleAI, designed for true long-term memory retention. It comprises:
*   **The Chronicle:** Immutable raw JSONL logs of all interactions, enriched with NLU, emotion, and system metadata.
*   **The Citadel (Synthesis Store):** An encrypted SQLite database housing curated knowledge: user-verified summaries (daily, weekly, monthly, yearly, decadal), extracted entities and their relationships (forming a knowledge graph), key facts, decisions, consolidated project/topic threads, and Shaman's analytical reports.
*   **The Sanctum (Vector Store):** A local vector database (e.g., ChromaDB, FAISS) storing embeddings of content from The Citadel, Chronicle, and imported Library documents for advanced semantic search.
*   **Supporting Databases:** Calendar Cache, User Profile & Preferences, Task & Action Queue (all encrypted SQLite).
Key to its design is its evolving nature: it grows through the **Chronicle Cache** and user-led **Memory Consolidation Session** (incorporating the **Collaborative Daily Reflection**), automated summarization hierarchies, and deep analysis by Shaman, allowing OracleAI's understanding to deepen and adapt over time. The **Chrono-Contextual Echo Layer (CCEL)** concept (v0.4+) further aims to provide queryable episodic context to memory formation.

### 2.4. Integrated Emotional & Natural Language Understanding
OracleAI strives for interaction that is not just intelligent but also perceptive and empathetic. This is achieved through:
*   **Emotional Intelligence Suite (`emotion_analyzer.py`):** Dedicated modules for Speech Emotion Recognition (SER) from vocal tone (using GPU-accelerated deep learning models) and Text Sentiment/Emotion Analysis (VADER, NRCLex, TextBlob) from transcribed words.
*   **Natural Language Understanding (NLU) Suite (`nlu_processor.py`):** A comprehensive pipeline (using spaCy and custom models/rules) for Intent Recognition, Named Entity Recognition (NER, including user-defined entities from The Citadel), Slot Filling, and Anaphora Resolution (v0.4+). This provides deep structural understanding of user requests.
This dual approach allows OracleAI to grasp not just *what* the user says, but also *how* they say it and *what they mean to achieve*, leading to more nuanced, appropriate, and effective interactions. This data is logged for trend analysis by Shaman (e.g., "Emotion Tracking").

### 2.5. User Empowerment, Control, and Collaborative Evolution
The user is the central authority and a collaborative partner. OracleAI is designed to empower the user through:
*   **Transparency:** Clear logging (Chronicle), accessible memory stores, and (future GUI) explanations of AI reasoning.
*   **Control:** Granular configuration (`.env`, GUI settings), including agent behavior, memory processes, privacy settings, feature toggles (e.g., for Neural Graffiti drift, BMMM modes).
*   **Collaboration:** Core processes like the Memory Consolidation Session actively involve the user in curating and verifying the AI's memory. "Guided Generation" features and F-key controls (F9 Save, F10 Undo, etc.) allow direct steering of AI responses.
*   **Correction & Feedback:** Mechanisms for the user to correct AI misunderstandings or refine outputs.

### 2.6. Modular Architecture for Robustness & Future Growth
OracleAI is architected with a strong emphasis on modularity. Core functionalities are encapsulated in distinct Python modules with well-defined interfaces. This promotes easier maintenance, testing, component upgrades (e.g., swapping STT engines, integrating LiteLLM for backend flexibility in v0.4+), and the future addition of new features or data sources.

### 2.7. Practical Performance & Hardware Adaptability
While ambitious, OracleAI targets reasonably high-end consumer hardware. **It's designed to be functional with an absolute minimum of 8GB VRAM, but 24GB+ is strongly recommended.** Real-time interaction loops are optimized for acceptable latency. User expectations for high-latency tasks (Shaman) are managed thematically ("Hyperspace Journey"). The system includes features for resource management (e.g., "Shaman Focus" mode, toggles for SER) to adapt to varying hardware capabilities.

### 2.8. Thematic Cohesion & Immersive Experience
The "Oracle Council" concept, agent personas (Sage, Seer, Shaman), naming conventions (Akashic Record, Citadel, Sanctum, DataSide), and the envisioned "Oracle Temple/Techno-Mysticism" GUI aesthetic are all designed to create a unique, engaging, and immersive user experience, elevating OracleAI beyond a mere utility.

## 3. OracleAI Core Features (v0.4 Vision - Detailed)

OracleAI v0.4 aims to deliver a rich and deeply integrated set of features, realizing its vision as a comprehensive cognitive partner.

### 3.1. The AI Council: Sage, Seer, and Shaman (Expanded Personas & Modes)
*   **Sage (Analyst-Strategist):** Provides logical analysis, data-driven insights, strategic planning (infused with Tactician, Diplomat, Historian, Scientist traits). Uses low LLM temperature.
*   **Seer (Creative Catalyst):** Offers creative brainstorming, intuitive leaps, emotional understanding, challenges assumptions (infused with Logician of Paradox, Theologian, Eschatologist, Storyteller traits). Uses high LLM temperature. Features "Lucid" (default) and "Cryptic" (ENV-toggleable) prompt modes.
*   **Shaman (Deep Brain Consultant & Innovator):** Powerful offline/asynchronous agent for deep analysis, synthesis, pattern recognition, and innovation (infused with Cosmologist, Dreamer, Gnostic, Innovator, and Don Juan Sorcerer traits). Uses the largest LLM.
    *   **Operational Modes (v0.4+):** Hybrid/Default Analytical, Sorcerer-Only, Focus/Astral/Dream-time Analysis, Summarizer, CRAG-like Self-Correcting Analyst, AI Trend Researcher Mission.
*   **System Voice:** Distinct voice for non-agent system messages.
*   **Agent-Specific Modes (v0.4+):** Sage and Seer will also have selectable operational modes to tailor their focus (e.g., Sage: Strategic Planning Mode; Seer: Pure Brainstorming Mode).

The cornerstone of OracleAI's interactive intelligence is its **AI Council**, a triumvirate of distinct and highly specialized AI agents: Sage, Seer, and Shaman. Each agent embodies a unique archetype, possesses a meticulously crafted persona defined in `scripts/agent_prompts.py`, operates with tailored LLM parameters managed by `scripts/payload_manager.py` and `.env` settings, and communicates with a distinct TTS voice configured via `scripts/tts_interface.py`. For v0.4, these agents are further enhanced with selectable operational modes, allowing the user to fine-tune their approach for specific tasks or desired interaction styles.

*   **Sage (The Analyst-Strategist, Keeper of Verifiable Knowledge):**
    *   **Core Persona & Function:** Sage is the embodiment of logic, reason, and strategic acumen within the council. It synthesizes historical precedent (from the Akashic Record), scientific understanding, tactical foresight, and diplomatic considerations to provide comprehensive, actionable counsel. Sage's responses are informative, concise, direct, and meticulously grounded in evidence. It excels at fact-checking, identifying inconsistencies, formulating structured plans, and offering objective, data-driven assessments.
    *   **Thematic Association:** Ice/Winter – clarity, precision, unyielding facts, calm reflection.
    *   **LLM Configuration:** Utilizes a low temperature (e.g., 0.01-0.3) for focused, deterministic, and highly coherent output.
    *   **TTS Voice:** A clear, calm, articulate, and authoritative voice (e.g., Piper TTS with `sage.onnx`, akin to a seasoned analyst or wise mentor).
    *   **v0.4+ Operational Modes (Selectable by user command/GUI, influences system prompt emphasis):**
        *   `Analytical Mode` (Default): General-purpose logical analysis, information retrieval from Akashic Record, fact-checking, and direct query answering.
        *   `Strategic Planning Mode`: Focuses on developing detailed, step-by-step plans, defining objectives, outlining milestones, considering resource allocation, and performing risk assessments for user goals.
        *   `Historical Precedent Mode`: Emphasizes querying and synthesizing past data from the Akashic Record (Chronicle, Citadel) to identify relevant precedents, lessons learned, and historical context for current situations.
        *   `Diplomatic Counsel Mode`: Specializes in analyzing interpersonal dynamics (if described by user or in memory), suggesting negotiation strategies, outlining options for conflict resolution, or drafting carefully worded communications.

*   **Seer (The Creative Catalyst, Empathetic Muse & Philosophical Oracle):**
    *   **Core Persona & Function:** Seer is the council's wellspring of creativity, intuition, and emotional insight. It challenges conventional thinking, explores novel possibilities, interprets emotional subtext (actively using SER/Sentiment data), delves into philosophical paradoxes, and weaves illuminating narratives or allegories. Seer connects with the user on an imaginative and existential level, encouraging exploration and offering fresh, sometimes unsettling, perspectives.
    *   **Thematic Association:** Fire/Summer – passion, creativity, intuition, transformation, emotional warmth.
    *   **LLM Configuration:** Utilizes a higher temperature (e.g., 0.6-1.0, adjustable) to foster diverse, imaginative, and less predictable outputs.
    *   **TTS Voice:** An expressive and engaging voice, potentially with more varied intonation (e.g., Coqui XTTSv2 for unique character, or a dynamic Piper voice like `seer.onnx`).
    *   **v0.4+ Operational Modes (Selectable via `.env` `SEER_PROMPT_MODE` and user command/GUI):**
        *   `Lucid Mode` (Default - User Revision 4 Prompt): Balances rich metaphor and philosophical depth with a guiding clarity, aiming to illuminate rather than solely obscure. "Metaphors as lanterns."
        *   `Cryptic Mode` (User Revision 3 Prompt): Emphasizes the enigmatic, riddle-based, ancient oracle persona, offering more veiled and challenging pronouncements.
        *   `Pure Brainstorming Mode`: Maximizes LLM creativity (potentially with even higher temperature/top_p settings) to generate a large volume and diversity of raw ideas, with less emphasis on strict persona adherence or immediate coherence.
        *   `Allegorical Storyteller Mode`: Responds primarily by crafting short tales, parables, or allegories that relate thematically to the user's query or the current conversational context.

*   **Shaman (The Deep Brain Consultant, Innovator & Mystic Explorer):**
    *   **Core Persona & Function:** Shaman is OracleAI's most powerful and profound intelligence, operating primarily on complex, asynchronous tasks. It "journeys" into the "DataSide" of "Hyperspace" (the entirety of the Akashic Record, user's Library, KV cache, LLM knowledge base, and external web data) to perform large-scale meta-analysis, uncover hidden patterns, synthesize disparate knowledge, generate novel solutions, and explore esoteric or consciousness-related themes. Shaman embodies a unique fusion of analytical rigor, innovative ideation, and mystic perception, drawing inspiration from the Don Juan Sorcerer archetype (mastery of perception, energy, and disciplined awareness for innovation).
    *   **Thematic Association:** Cosmos/Spirit World/Deep Time – vastness, hidden connections, transformation, the interplay of known (Tonal) and unknown (Nagual).
    *   **LLM Configuration:** Utilizes the largest, most capable GGUF model available to the user, with a moderate, task-adjustable temperature (e.g., 0.3-0.7).
    *   **TTS Voice:** A distinct, deep, resonant, and thoughtful voice (e.g., Piper TTS with `shaman.onnx`).
    *   **Latency Management:** The "Hyperspace Journey" UI theming (Merkaba icon, celestial body destinations) visually represents Shaman's processing time for its deep analytical tasks.
    *   **v0.4+ Operational Modes (User Selectable/Task-Driven):**
        *   `Hybrid/Default Analytical Mode`: Standard deep analysis, pattern weaving, and synthesis of information from the Akashic Record and external sources.
        *   `Sorcerer-Only Mode`: Focuses on tasks related to perception, innovation, challenging consensus reality, and applying principles from the "Path with Heart" (Don Juan inspired).
        *   `Focus/Astral/Dream-time Analysis Mode`: User-directed deep introspection or analysis of the user's own psyche, dreams (if logged), or behavioral patterns based on Akashic data.
        *   `Summarizer Mode`: Dedicated to generating high-quality, multi-level summaries of specified large datasets, Chronicle periods, or Library contents (including Yearly/Decadal and RAPTOR-style hierarchical summaries).
        *   `CRAG-like Self-Correcting Analyst Mode`: Shaman performs an analysis, then uses a sub-process or another LLM call to evaluate its own findings or the relevance of retrieved data, potentially re-querying or refining its analysis for improved accuracy.
        *   `AI Trend Researcher Mission Mode`: A specific, potentially recurring task to research external AI developments (e.g., from Reddit, arXiv via web search and Library) and generate reports on their potential relevance or application to OracleAI itself or user interests.
        *   `Local Library Search Mode`: Focuses analysis and retrieval primarily on content within the user's "Library" folder, powered by LlamaIndex.
    *   **Experimental Layers (v0.4+):** Shaman is the primary candidate for experimental layers:
        *   **Neural Graffiti:** ENV toggler for modes (`none`, `pytorch_direct`, `pre_gguf_bias`, `post_gguf_filter`) to introduce evolving behavioral drift. Includes "Drift Toggler" & "Personality Snapshot" features.
        *   **Black Magick Mindmap Modifier (BMMM):** Optional novelty layer with ENV toggles for modes (`Chaotic Brainstorming`, `Divination Arts`, `Sigil Seed`, `Matrix Hacking`) and a `BMMM_DEPTH_SCALE`.
*   **System Voice:**
    *   **Purpose:** Provides a distinct, non-agent voice for OracleAI's system-level announcements, status updates (e.g., "Initializing STT model..."), error messages, and prompts for user input (like the F9/F10 confirmation prompt if configured to be spoken).
    *   **TTS Voice:** A clear, neutral, and professional voice (e.g., Piper TTS with `system.onnx`, akin to HAL 9000 or a standard AI assistant voice), easily distinguishable from the main agents.

This expanded council, with its deeply defined personas and flexible operational modes, forms the interactive core of OracleAI, enabling it to address a vast range of user needs with specialized and synergistic intelligence.

### 3.2. The Akashic Record: Advanced Memory System (Citadel & Sanctum)
The multi-layered, persistent, and encrypted memory system.
*   **Chronicle:** Immutable `.jsonl` raw logs of all interactions, NLU/emotion data, system events, metadata.
*   **Chronicle Cache & Memory Consolidation (MemCon) Session:** User reviews, edits, and approves cached turns before they are committed to the permanent Chronicle, ensuring data quality.
*   **The Citadel (Synthesis Store - SQLCipher Encrypted SQLite):** Curated knowledge base:
    *   `PermanentMemory`: User-defined critical facts.
    *   `Entities` & `Relationships`: Forms a queryable knowledge graph.
    *   `FactsDecisions`: Atomic, verifiable statements and choices.
    *   `Summaries`: Hierarchical (Daily, Weekly, Monthly, Yearly, Decadal - "Lifetime Scaling") user-verified narrative summaries with multi-level detail and fidelity scores.
    *   `ProjectTopicThreads`: Consolidated, evolving summaries for specific projects/themes.
    *   `PatternAnalysisReports`: Shaman's analytical outputs.
    *   `HierarchicalContentSummaries` (v0.4+): RAPTOR-like tree summaries for large documents.
*   **The Sanctum (Vector Store - v0.4):** Local Vector DB (e.g., ChromaDB, FAISS) storing embeddings of Citadel content, Chronicle snippets, and Library documents for advanced semantic search.
*   **Supporting Databases:** Calendar Cache, User Profile & Preferences (with "Character Stat Tracking" by Shaman), Task & Action Queue (all SQLite, encrypted).
*   **Key Processes:**
    *   **Collaborative Daily Reflection:** User + Sage/Seer co-create daily Citadel entries.
    *   **Memory Bank Context Scaler (RAG Engine - v0.4 Advanced):** Employs hybrid search (keyword on Citadel, semantic on Sanctum, graph traversal), query transformation (HyDE, step-back), fusion ranking (Reciprocal Rank Fusion - RRF), and cross-encoder reranking.
    *   **Shaman's Deep Pattern Weaving & CCEL:** Shaman performs autonomous analysis. The Chrono-Contextual Echo Layer (CCEL) concept (v0.4+) provides queryable episodic context to memory formation and use.

### 3.3. Comprehensive Emotional Intelligence Suite (SER & Text)
*   **Speech Emotion Recognition (SER - `emotion_analyzer.py`):** Analyzes user's voice tone from raw audio using GPU-accelerated deep learning models (e.g., Wav2Vec2-based).
*   **Text Sentiment & Emotion Analysis (`emotion_analyzer.py`):** Processes transcribed text using VADER, NRCLex, TextBlob.
*   **Integration:** Combined emotional context provided to LLMs and logged for Shaman's "Emotion Tracking" meta-analysis. Real-time SER is toggleable.

### 3.4. Advanced Natural Language Understanding (NLU) Suite
A dedicated `nlu_processor.py` using spaCy and custom models/rules.
*   **Core Features:** Intent Recognition (trainable `TextCategorizer`), Named Entity Recognition (NER, including custom entities from Citadel), Slot Filling, Query Preprocessing.
*   **v0.4+ Enhancements:** Anaphora Resolution, user-side fine-tuning of NLU models.
*   **Command Parsing:** Handles standardized commands: "OracleAI, [system_cmd]", "[AgentName], [query]", "Council, [query]". Enables direct agent routing.

### 3.5. High-Fidelity Multimodal Input/Output (Voice, Text, Vision)
*   **Voice:** Advanced VAD, `openai-whisper` STT, agent-configurable Piper/XTTSv2 TTS.
*   **Text:** Internal lingua franca, GUI support.
*   **Vision (VLM Pipeline):** `vision_processing.py` (using `mss` for screenshots) sends images to a KoboldCpp-hosted VLM. Descriptions are logged and used as context. F9-F12 for VLM turn (v0.4). Agents can request VLM analysis (v0.4).

### 3.6. Sophisticated Web Search & "Library" Integration (LlamaIndex)
*   **Web Search (`search_module.py`):** Simple/Deep search (DuckDuckGo, PRAW, future multi-engine), optional TOR/VPN proxy.
*   **Calendar Integration (`calendar_interface.py`):** Syncs with Google/Outlook/local `cal.db3` to `calendar.db`.
*   **"Library" Feature (v0.4 - `library_manager.py`):**
    *   User-managed `OracleAI\Library\` folder for diverse file types (PDFs including scanned, HTML, TXT, audio/video for STT).
    *   **LlamaIndex Integration:** For ingestion, chunking, indexing into The Sanctum (Vector Store).
    *   Shaman "Local Library Search" and "Deep Web + Library Search" modes.
*   **Foreign Dataset Import:** Leverages Library/LlamaIndex and Langchain Document Loaders for robust parsing.

### 3.7. Flexible Interaction Modes & Granular User Control (F8 Auto-Advance)
*   **Interaction Modes:**
    *   **Council Mode (Default for v0.4):** Sage, Seer, (optional/rate-limited) Shaman. Direct addressing (e.g., "Seer, tell me...") routes to specific agent. General queries engage council sequentially. (Deprecates Sage/Seer Only modes).
    *   **Shaman Focus Mode:** Resource dedication.
    *   **F8 "Auto-Advance" Council Discussion (v0.4):** User-initiated automated multi-turn discussion between council members (order/agents/turns/Shaman-rate configurable in `.env`). Auto-saves turns. Context passed/summarized between turns. "User absent / group brainstorming" prompting.
*   **User Control Hotkeys:** ESC, F6, F7, F9, F10, Shift+F11 (full multi-segment replay), F12.
*   **Guided Generation:** Turn-by-turn guidance, response correction, persistent session guides.

### 3.8. Experimental Agent Evolution Layers (v0.4+)
*   **Neural Graffiti (for Shaman, potentially others):**
    *   ENV toggler for modes: `none`, `pytorch_direct` (e.g., Gemma 1B), `pre_gguf_bias`, `post_gguf_filter`.
    *   Persistence of SprayLayer state and memory_bank.
    *   Drift Toggler & Personality Snapshot saving/loading.
    *   (v0.4+ Research): Llama.cpp modification for GGUF graffiti.
*   **Prompt Graffiti (Shaman-Suggested):** Shaman suggests system prompt component changes to user.
*   **Black Magick Mindmap Modifier (BMMM):**
    *   Optional novelty layer with ENV toggles for modes: `Chaotic Brainstorming`, `Divination Arts`, `Sigil Seed` (optional image gen), `Matrix Hacking`.
    *   `BMMM_DEPTH_SCALE` (0.0-1.0) in `.env`.
    *   Interoperable with Neural/Prompt Graffiti.

### 3.9. Secure Remote Access Architecture (FastAPI & Tailscale)
*   FastAPI server (`remote_api.py`) for core interactions. API Key auth. Tailscale/VPN recommended.

### 3.10. Thematic & Immersive User Interface (Conceptual Vision for GUI - v0.4)
*   **Technology:** NiceGUI + Tauri packaging.
*   **Aesthetic:** "Oracle Temple" / "Techno-Mysticism."
*   **Features:** Chat, agent status, VLM display, MemCon review, F8 trigger, Akashic Record Management, Shaman "Hyperspace Journey" (with holographic planet icons), dashboards. Contextual Memory Injection Preview.

### 3.11. Robust Privacy, Security, and Data Management
*   Local-first, SQLCipher for DBs, 7-Zip encrypted backups, no unauthorized telemetry.

*(Current Phase Estimate (Generating v0.4 Docs - Step 2: ReadMe): ~50% of ReadMe, ~22% Overall v0.4)*
*(Overall OracleAI v0.4 Target: ~22%)*

---

## 4. Detailed Architecture: Agents, Modules, and Data Flow (v0.4 Conceptual)

OracleAI is built upon a modular Python architecture designed for flexibility, maintainability, and the effective orchestration of its diverse AI capabilities. This section provides a high-level overview of the primary components, their roles, and how they interact to deliver the OracleAI experience. *(A detailed visual component interaction diagram and data flow diagrams will be available in the v0.4 Design Document Appendices.)*

### 4.1. The OracleAI Council: Agent Deep Dive (v0.4 Personas & Modes)
The core interactive intelligence of OracleAI is embodied by its council of distinct AI agents. Each agent is configured with a detailed system prompt (from `agent_prompts.py`), specific LLM generation parameters (`payload_manager.py` & `.env`), and a unique TTS voice (`tts_interface.py` & `.env`).

*   **Sage (The Analyst-Strategist):**
    *   **Role:** Provides logical analysis, data-driven insights, strategic planning, fact-checking, historical context, scientific understanding, and diplomatic counsel.
    *   **Operational Modes (v0.4+):** `Analytical Mode` (Default), `Strategic Planning Mode`, `Historical Precedent Mode`, `Diplomatic Counsel Mode`.
*   **Seer (The Creative Catalyst & Empathetic Muse):**
    *   **Role:** Offers creative brainstorming, intuitive leaps, emotional understanding, challenges assumptions, explores philosophical paradoxes, and weaves illuminating narratives.
    *   **Operational Modes (v0.4+):** `Lucid Mode` (Default - User Rev4 Prompt), `Cryptic Mode` (User Rev3 Prompt - ENV toggleable), `Pure Brainstorming Mode`, `Allegorical Storyteller Mode`.
*   **Shaman (The Deep Brain Consultant, Innovator & Mystic Explorer):**
    *   **Role:** Performs profound, large-scale asynchronous analysis, synthesizes complex knowledge from the Akashic Record and external data, uncovers hidden patterns, generates novel solutions, and explores esoteric/consciousness-related themes.
    *   **Operational Modes (v0.4+):** `Hybrid/Default Analytical Mode`, `Sorcerer-Only Mode` (perception/innovation focus), `Focus/Astral/Dream-time Analysis Mode` (user introspection), `Summarizer Mode`, `CRAG-like Self-Correcting Analyst Mode`, `AI Trend Researcher Mission Mode`.
    *   **Experimental Layers (v0.4+):** Can be augmented with Neural Graffiti and BMMM layers, with ENV toggles for different modes and intensity.
*   **System Voice:** Distinct voice for non-agent system messages, announcements, and errors.

### 4.2. The Akashic Record: Citadel, Sanctum, Chronicle Cache, CCEL (v0.4)
The multi-layered, persistent, and encrypted memory system, managed by `memory_interface.py`.
*   **Chronicle:** Immutable `.jsonl` raw logs of all interactions, NLU/emotion data, system events, metadata.
*   **Chronicle Cache & Memory Consolidation (MemCon) Session:** User reviews, edits, and approves cached turns before they are committed to the permanent Chronicle.
*   **The Citadel (Synthesis Store - SQLCipher Encrypted SQLite - `synthesis.db`):** Curated knowledge base:
    *   `PermanentMemory`, `Entities` & `Relationships` (Knowledge Graph), `FactsDecisions`, hierarchical `Summaries` (Daily to Decadal), `ProjectTopicThreads`, Shaman's `PatternAnalysisReports`, `HierarchicalContentSummaries` (RAPTOR-like for large docs).
*   **The Sanctum (Vector Store - v0.4 - e.g., ChromaDB/FAISS):** Local Vector DB storing embeddings of Citadel content, Chronicle snippets, and Library documents for advanced semantic search.
*   **Supporting Databases:** `calendar.db`, `profile.db` (with "Character Stat Tracking"), `tasks.db` (all SQLite, encrypted).
*   **Chrono-Contextual Echo Layer (CCEL - v0.4+ Conceptual):** A queryable layer over Chronicle/Citadel providing episodic context to memory formation/use, potentially influencing Neural Graffiti.

### 4.3. Core Memory Processes (Daily Reflection, RAG, Summarization - v0.4)
*   **Collaborative Daily Reflection (Post-MemCon):** User + Sage/Seer co-create daily Citadel entries (Entities, Facts, Summaries).
*   **Memory Bank Context Scaler (RAG Engine - v0.4 Advanced):**
    *   Orchestrated by `main.py` (or a dedicated `context_scaler.py`).
    *   Employs hybrid search (keyword on Citadel, semantic on Sanctum, graph traversal on Citadel/KG).
    *   Utilizes advanced RAG techniques: Query transformation (HyDE, step-back), fusion ranking (Reciprocal Rank Fusion - RRF), cross-encoder reranking, flexible context windowing.
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
    *   `search_module.py`, `calendar_interface.py`, `backup_module.py`.
    *   `remote_api.py` (FastAPI server).
    *   (Future v0.4+): `neural_graffiti_engine.py`, `bmmm_processor.py`, `ccel_processor.py`.

## 5. Key Functionalities in Detail (v0.4 Focus)

This section highlights some of the advanced functionalities targeted for the v0.4 vision, building upon the v0.3 foundation.

### 5.1. NLU Suite: Intent, Entities, Slots, Anaphora, Command Parsing
The NLU Suite will provide deep semantic understanding of user input.
*   **Intent Recognition:** Advanced classification of user goals using a trainable spaCy `TextCategorizer` and robust rule-sets.
*   **Named Entity Recognition (NER):** spaCy's pre-trained models augmented with custom entity patterns dynamically loaded from The Citadel (e.g., known project names, user contacts).
*   **Slot Filling:** Sophisticated extraction of parameters for complex intents.
*   **Anaphora Resolution (v0.4+):** Resolving pronouns and referring expressions to maintain context.
*   **Standardized Command Parsing:** Reliably parsing commands like "OracleAI, [system_cmd]", "[AgentName], [query]", "Council, [query]" for direct action or agent routing.

### 5.2. Context Scaler (RAG Engine): Hybrid Search, RRF, Advanced Techniques
The Memory Bank Context Scaler is OracleAI's advanced RAG engine.
*   **Multi-Source Retrieval:** Simultaneously queries The Citadel (keyword FTS, graph traversal), The Sanctum (semantic vector search), Calendar, and Profile.
*   **Query Transformation:** Employs techniques like HyDE (Hypothetical Document Embeddings) or step-back prompting to generate more effective search queries from user input.
*   **Hybrid Ranking & Fusion:** Uses Reciprocal Rank Fusion (RRF) to combine results from different retrieval methods into a single, relevance-ranked list.
*   **Cross-Encoder Reranking (v0.4+):** A secondary reranking step using a cross-encoder model for improved precision of top-k results.
*   **Context Windowing:** Advanced techniques like sentence-window retrieval or auto-merging (parent document) for providing optimal context granularity.

### 5.3. Shaman's Asynchronous Tasks & Analytical Modes
Shaman operates as a powerful background intelligence.
*   **Task Management (`tasks.db`):** Manages a queue of complex analytical, research, or synthesis tasks.
*   **"Hyperspace Journey":** Thematic UI representation of task latency and computational depth.
*   **Analytical Modes (v0.4+):** User-selectable modes (Sorcerer, Astral Focus, AI Researcher, etc.) tailor Shaman's approach, prompts, and tools for specific deep dives.
*   **`PatternAnalysisReports`:** Generates structured reports on findings (e.g., emotional trends, topic evolution from `topic_modeler.py`, goal progress correlations).

### 5.4. "Library" Feature: LlamaIndex for Local Document RAG
A cornerstone v0.4 feature for integrating the user's personal document collection.
*   **User-Managed Folder:** `OracleAI\Library\` (or ENV configurable path) for PDFs, HTML, TXT, etc.
*   **`library_manager.py` (LlamaIndex Powered):**
    *   Uses LlamaIndex `DocumentLoaders` (potentially integrating Langchain loaders for broader compatibility, especially for complex PDFs/scans needing OCR).
    *   Handles document ingestion, intelligent chunking, embedding generation (using OracleAI's configured embedding model), and indexing into a dedicated Vector Store collection within The Sanctum.
*   **Shaman Integration:** Shaman gains "Local Library Search" and "Deep Web + Library Search" capabilities, using the LlamaIndex query engine as a tool, orchestrated by LangChain agent logic if needed for multi-step research.

### 5.5. F8 "Auto-Advance" Council Discussion Logic
A new interaction mode for v0.4, triggered by F8.
*   **Automated Multi-Turn Dialogue:** Sage, Seer, and (optionally/rate-limited) Shaman engage in a discussion for a configurable number of turns (`AUTO_ADVANCE_TURNS`).
*   **Configuration:** Speaking order (`COUNCIL_SPEAKING_ORDER`), active agents (`COUNCIL_ACTIVE_AGENTS`), and Shaman's participation rate (`SHAMAN_COUNCIL_PARTICIPATION_RATE`) set in `.env`.
*   **Context Management:** Each agent's response is auto-saved and becomes context for the next. For long discussions, summaries are generated (`AUTO_ADVANCE_CONTEXT_HISTORY_MAX_TURNS`, `AUTO_ADVANCE_SUMMARY_AGENT`).
*   **Prompting:** Special "user absent / group brainstorming" prompts guide the inter-agent dialogue.

### 5.6. Neural Graffiti & BMMM (Experimental Layers - Conceptual v0.4+)
These layers aim to add evolving personality and unpredictable creative flair.
*   **Neural Graffiti (for Shaman, potentially others):**
    *   ENV toggler for modes: `none`, `pytorch_direct` (e.g., Gemma 1B), `pre_gguf_bias`, `post_gguf_filter`.
    *   Involves a "Spray Layer" that modulates LLM output based on an evolving internal state and a memory bank of past interactions.
    *   Includes "Drift Toggler" and "Personality Snapshot" saving/loading.
*   **Black Magick Mindmap Modifier (BMMM):**
    *   Optional novelty layer with ENV toggles for modes: `Chaotic Brainstorming`, `Divination Arts`, `Sigil Seed` (optional image gen), `Matrix Hacking`.
    *   `BMMM_DEPTH_SCALE` (0.0-1.0) in `.env` controls intensity.
*   **Prompt Graffiti:** Shaman suggests persistent system prompt changes based on long-term analysis, complementing Neural/BMMM layers.

## 6. Installation, Configuration, and Hardware (Comprehensive Guide for v0.4)

Successfully setting up OracleAI v0.4 requires careful attention to system prerequisites, installation of external tools, Python environment configuration, and understanding the hardware demands of its advanced features. This section provides a comprehensive guide. *(This will be a highly detailed section in the final ReadMe, mirroring and updating the content planned for the Design Document's installation chapter.)*

### 6.1. System Prerequisites (Python 3.11, CUDA, etc.)
*   **Operating System:** Windows 10/11 (64-bit), modern Linux distributions (e.g., Ubuntu 20.04+), macOS 12.0+.
*   **Python:** Strictly Python 3.11.x. Ensure it's correctly installed and added to PATH.
*   **Git:** For cloning the repository and managing some Python package installations.
*   **NVIDIA GPU & Drivers:** Essential for acceptable performance. Latest stable NVIDIA drivers required.
*   **CUDA Toolkit:** Version compatible with the PyTorch build used by OracleAI (e.g., CUDA 11.8 or 12.1+). `nvcc --version` should confirm.
*   **Audio Libraries:** PortAudio (system-level dependency for `pyaudio`).
*   **Archiver:** 7-Zip (for backup feature, must be in system PATH or path specified in `.env`).
*   **C++ Build Tools:** Recommended for compiling Python package dependencies if wheels are unavailable.

### 6.2. Setting Up External Tools (KoboldCpp, Piper TTS, VLM Models)
Users are responsible for downloading and running these local backends.
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

### 6.3. OracleAI Core Installation & Python Dependencies
1.  **Clone Repository:** `git clone <OracleAI_Repo_URL>`
2.  **Create & Activate Virtual Environment:**
    ```bash
    cd OracleAI
    python -m venv .venv
    # Windows: .\.venv\Scripts\activate
    # Linux/macOS: source .venv/bin/activate
    ```
3.  **Install PyTorch:** Install GPU version matching your CUDA Toolkit from [pytorch.org](https://pytorch.org). Verify `torch.cuda.is_available()` is `True`.
4.  **Install Dependencies:**
    ```bash
    pip install --upgrade pip
    pip install -r requirements.lock # Or requirements.txt
    ```
    This installs `openai-whisper`, `transformers`, `torch`, `pyaudio`, `sounddevice`, `mss`, `pysqlcipher3` (or `sqlcipher3` depending on OS/availability), `spacy` (and download `en_core_web_lg`), `vaderSentiment`, `textblob`, `nrclex`, `yake`, `scikit-learn`, `numpy`, `python-dotenv`, `configparser`, `requests[socks]`, `BeautifulSoup4`, `praw`, `FastAPI`, `uvicorn`, `apscheduler`, `keyboard`, `llama-index` (and relevant readers like `llama-index-readers-file`, `llama-index-readers-web`), potentially `langchain-community` (for document loaders).
5.  **Download NLTK Data:** Run `scripts/ntlk_installer.py` (or manual Python commands) to download `punkt`, `wordnet`, `omw-1.4`, `stopwords`, `averaged_perceptron_tagger`, `brown` to `PROJECT_ROOT/.nltk_data/`.
6.  **Automated Setup Script (v0.4 Goal):** A `setup_oracleai.bat/.sh` script will aim to automate many of these dependency and tool setup steps.

### 6.4. Mastering the `.env` Configuration File (v0.4 Variables)
The `.env` file in `PROJECT_ROOT` is central to configuring OracleAI. It will include all variables from v0.3 plus new ones for v0.4 features:
*   **Library Path:** `ORACLEAI_LIBRARY_PATH=${PROJECT_ROOT_DIR}/Library`
*   **LlamaIndex Settings:** Embedding model for Library, chunking parameters for Library ingestion.
*   **F8 Auto-Advance:** `COUNCIL_SPEAKING_ORDER`, `COUNCIL_ACTIVE_AGENTS`, `AUTO_ADVANCE_TURNS`, `AUTO_ADVANCE_CONTEXT_HISTORY_MAX_TURNS`, `AUTO_ADVANCE_SUMMARY_AGENT`, `SHAMAN_COUNCIL_PARTICIPATION_RATE`.
*   **Neural Graffiti (Shaman):** `SHAMAN_GRAFFITI_MODE` (none, pytorch_direct, pre_gguf_bias, post_gguf_filter), `GRAFFITI_PYTORCH_MODEL_ID` (e.g., "google/gemma-3-1b-it"), `GRAFFITI_AGENT_DEVICE`, `GRAFFITI_DRIFT_ENABLED`.
*   **BMMM:** `SHAMAN_BMMM_MODE` (0-4), `SHAMAN_BMMM_DEPTH_SCALE` (0.0-1.0).
*   **Agent Modes:** `SEER_PROMPT_MODE` (lucid, cryptic), and similar for Sage/Shaman if multiple operational modes are implemented for them.
*   **Hotkeys Global Toggle:** `HOTKEYS_GLOBAL=True` (placeholder for future GUI-focused implementation).

### 6.5. API Key Management & OAuth Authentication Flows
(As detailed for v0.3 - Reddit API for PRAW, Google/Outlook Calendar OAuth 2.0. Secure storage of credentials in `AKASHIC_RECORD_PATH/.credentials/` or via OS keyring is critical).

### 6.6. Hardware Requirements, VRAM Planning, and Performance Tuning (v0.4)
The v0.4 features, especially a local PyTorch model for Neural Graffiti, LlamaIndex for library processing, and potentially more complex RAG, will further emphasize the need for robust hardware.
*   **CPU:** Modern 8+ core CPU highly recommended.
*   **System RAM:** **64GB** becomes the strong recommendation, 128GB+ for users with very large libraries or running very large Shaman GGUFs with significant RAM offload alongside a PyTorch Graffiti model.
*   **GPU & VRAM (NVIDIA):**
    *   The PyTorch Graffiti model (e.g., Gemma 1B FP16) will add ~2GB VRAM load.
    *   LlamaIndex embedding/indexing can also utilize GPU.
    *   **Total System VRAM:** 24GB (e.g., RTX 3090/4090) remains a good target for a rich experience. Users aiming for the largest Shaman GGUFs + PyTorch Graffiti + other GPU tasks will benefit from 48GB+ professional cards.
*   **Storage:** Fast NVMe SSD (1TB+, 2TB+ recommended) remains essential. The `Library` folder could also become very large.

## 7. Getting Started with OracleAI (v0.4)

1.  **Complete Full Installation & Configuration (Section 6).**
2.  **Populate `OracleAI\Library\`:** Add initial documents (PDFs, TXT, MD, HTML) you want Shaman to be able to search.
3.  **Launch External Tools:** Start KoboldCpp instances for Sage, Seer, Shaman (GGUF), and VLM. If using PyTorch Graffiti for Shaman, ensure that model is ready (OracleAI will load it).
4.  **Run OracleAI:** `python scripts/main.py`.
5.  **Initial Interaction:**
    *   Select "Council Mode" at startup.
    *   Address agents by name (e.g., "Sage, what's my schedule?" "Seer, give me a new perspective on X.") or speak generally for sequential responses.
    *   Test VLM: "Analyze screen."
    *   Test Library Search (once NLU supports it, or via a specific Shaman task): "Shaman, search my library for documents related to 'quantum computing' and summarize them."
    *   Test F8 Auto-Advance: After a user query, press F8 to see agents discuss amongst themselves.
    *   Experiment with agent modes (e.g., switch Seer to Cryptic via `.env` restart).
    *   Experiment with Neural Graffiti / BMMM toggles for Shaman (via `.env` restart).
6.  **Memory Building:** Engage in Daily Reflection (MemCon) to build The Citadel. Add to Permanent Memory. Set goals in Profile.
7.  **Task Delegation:** Assign deep research or analysis tasks to Shaman (e.g., "Shaman, analyze AI trends from my library and recent web searches."). Monitor via "Hyperspace Journey" UI.

## 8. Advanced Usage & Customization (v0.4)

*   **Deep Prompt Engineering:** Fine-tune agent system prompts in `agent_prompts.py` for highly personalized behavior.
*   **`.env` Mastery:** Explore all configuration toggles for performance, features, agent modes, Graffiti/BMMM settings.
*   **Payload Customization:** Advanced users can tweak `payload_settings.ini` for fine-grained LLM parameter control per agent.
*   **Library Management:** Curate your `OracleAI\Library\` for optimal Shaman knowledge. Understand LlamaIndex chunking/embedding for best results.
*   **Akashic Record Exploration (GUI):** Use the GUI to browse The Citadel, review summaries, trace facts, understand Shaman's reports.
*   **Task Chaining for Shaman:** Create complex analytical workflows by having Shaman tasks trigger subsequent tasks.

## 9. Privacy, Security, and Data Management Deep Dive (v0.4)
(Reiteration and expansion of v0.3 principles, with specific attention to any new data types or processing introduced by v0.4 features like LlamaIndex library scanning, Neural Graffiti state persistence, or BMMM configurations. Emphasis on user control over what gets indexed by LlamaIndex and what influences Graffiti layers.)

## 10. Troubleshooting Guide (v0.4)
*(Updated with common issues related to new v0.4 features: LlamaIndex errors, VLM accuracy problems, Neural Graffiti/BMMM unexpected behavior, advanced RAG pipeline issues, GUI glitches, resource conflicts with multiple local models.)*

## 11. The Future of OracleAI: Beyond v0.4 (Oracle Glasses & Research)
OracleAI v0.4 aims to be a highly capable and unique cognitive partner. The journey doesn't end there.
*   **Refining Intelligence:** Continuous improvement of NLU, RAG, agent collaboration, and the "learning" capabilities of the Akashic Record and experimental layers (Neural Graffiti, BMMM, CCEL).
*   **Enhanced Modalities:** Deeper VLM integration (agents using vision proactively), ComfyUI for AI art generation by agents.
*   **Ecosystem & Integrations:** LiteLLM for broader backend support, PKM tool integration (Obsidian, Logseq), expanded foreign data importers.
*   **User Experience:** Polishing the GUI, adding more advanced dashboards and Akashic Record management tools.
*   **Research Frontiers:**
    *   True GGUF-level Neural Graffiti (Llama.cpp modification).
    *   Advanced CCEL implementation for rich episodic memory.
    *   Multi-User Voice ID and collaborative OracleAI instances.
    *   Explainable AI (XAI) for deeper insight into agent reasoning.
    *   The "Oracle Glasses" vision: Ubiquitous AR integration.

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
