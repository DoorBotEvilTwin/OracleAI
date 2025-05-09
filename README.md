# OracleAI ReadMe (v0.2)

A local AI assistant comprised of an emotionally aware multi-agent LLM council (Sage, Seer, Shaman) with persistent memory (Akashic Record) for augmented cognition, deep insight & strategic guidance.

**Your Personal AI Strategic Council & Living Memory: Sage, Seer, and the Shaman**

OracleAI is an advanced, locally-run AI assistant framework designed to be a persistent, intelligent partner. It acts as a personalized council featuring distinct AI agents – **Sage** (logical Analyst-Strategist), **Seer** (creative Catalyst), and the optional **Shaman** (Deep Brain consultant) – who collaborate with you and each other. Leveraging a sophisticated, long-term memory system called the **Akashic Record**, integrated emotional intelligence, and powerful analytical tools, OracleAI aims to assist in navigating complex tasks, managing information, achieving goals, and enhancing self-understanding, all while prioritizing user privacy, control, and a rich, thematic user experience.

## Table of Contents

*   [1. Vision & Philosophy](#1-vision--philosophy)
    *   [1.1. Core Vision](#11-core-vision)
    *   [1.2. Guiding Principles](#12-guiding-principles)
        *   [1.2.1. Local-First Processing & Privacy-Centric Design](#121-local-first-processing--privacy-centric-design)
        *   [1.2.2. Multi-Agent Synergy & Specialized Roles](#122-multi-agent-synergy--specialized-roles)
        *   [1.2.3. Deep & Evolving Memory (The Akashic Record)](#123-deep--evolving-memory-the-akashic-record)
        *   [1.2.4. Integrated Emotional Intelligence](#124-integrated-emotional-intelligence)
        *   [1.2.5. User Empowerment & Collaborative Interaction](#125-user-empowerment--collaborative-interaction)
        *   [1.2.6. Modularity, Extensibility, and Openness](#126-modularity-extensibility-and-openness)
        *   [1.2.7. Practicality, Performance, and Adaptability](#127-practicality-performance-and-adaptability)
*   [2. Core Features at a Glance](#2-core-features-at-a-glance)
*   [3. The OracleAI Council: Agent Personas & Roles](#3-the-oracleai-council-agent-personas--roles)
    *   [3.1. Sage (The Analyst-Strategist)](#31-sage-the-analyst-strategist)
    *   [3.2. Seer (The Catalyst)](#32-seer-the-catalyst)
    *   [3.3. Shaman (The Deep Brain Consultant)](#33-shaman-the-deep-brain-consultant)
*   [4. The Akashic Record: A Deep Dive into the Memory System](#4-the-akashic-record-a-deep-dive-into-the-memory-system)
    *   [4.1. Chronicle (Immutable Raw Logs)](#41-chronicle-immutable-raw-logs)
    *   [4.2. Synthesis Store (Processed Knowledge & Insights)](#42-synthesis-store-processed-knowledge--insights)
    *   [4.3. Calendar Cache](#43-calendar-cache)
    *   [4.4. User Profile & Preferences](#44-user-profile--preferences)
    *   [4.5. Task & Action Queue](#45-task--action-queue)
    *   [4.6. Knowledge Graph (Conceptual)](#46-knowledge-graph-conceptual)
    *   [4.7. Vector Store (for Semantic Search)](#47-vector-store-for-semantic-search)
    *   [4.8. Key Memory Processes](#48-key-memory-processes)
        *   [4.8.1. Collaborative Daily Reflection & Structured Extraction](#481-collaborative-daily-reflection--structured-extraction)
        *   [4.8.2. Hierarchical & Thematic Summarization](#482-hierarchical--thematic-summarization)
        *   [4.8.3. Memory Bank Context Scaler (RAG Engine)](#483-memory-bank-context-scaler-rag-engine)
        *   [4.8.4. Deep Pattern Weaving (Shaman's Analysis)](#484-deep-pattern-weaving-shamans-analysis)
        *   [4.8.5. Word Frequency Indexing (Optional Analysis)](#485-word-frequency-indexing-optional-analysis)
*   [5. Emotional Intelligence Suite](#5-emotional-intelligence-suite)
*   [6. Multimodal Capabilities (Voice, Text, Vision)](#6-multimodal-capabilities-voice-text-vision)
*   [7. Interaction Modes & User Control](#7-interaction-modes--user-control)
    *   [7.1. Standard Interaction Mode](#71-standard-interaction-mode)
    *   [7.2. Oracle Consultation / Roundtable Mode](#72-oracle-consultation--roundtable-mode)
    *   [7.3. Shaman Focus Mode (Resource Management)](#73-shaman-focus-mode-resource-management)
    *   [7.4. Guided Generation & Interaction Refinement](#74-guided-generation--interaction-refinement)
    *   [7.5. Toggleable States (Mute, Search)](#75-toggleable-states-mute-search)
*   [8. Web Connectivity & External Data](#8-web-connectivity--external-data)
*   [9. Remote Access Architecture](#9-remote-access-architecture)
*   [10. User Interface (UI) Concept & Aesthetic](#10-user-interface-ui-concept--aesthetic)
*   [11. Privacy, Security, and Data Management](#11-privacy-security-and-data-management)
*   [12. Installation & Setup Guide](#12-installation--setup-guide)
    *   [12.1. System Prerequisites](#121-system-prerequisites)
    *   [12.2. External Tool Dependencies & Setup](#122-external-tool-dependencies--setup)
    *   [12.3. Python Environment & OracleAI Installation](#123-python-environment--oracleai-installation)
    *   [12.4. Configuration (`.env` File)](#124-configuration-env-file)
    *   [12.5. API Keys & Authentication Setup](#125-api-keys--authentication-setup)
*   [13. Hardware Requirements & Performance](#13-hardware-requirements--performance)
*   [14. Getting Started & Basic Usage](#14-getting-started--basic-usage)
*   [15. Troubleshooting Common Issues](#15-troubleshooting-common-issues)
*   [16. Future Development & Roadmap](#16-future-development--roadmap)
*   [17. Contributing to OracleAI](#17-contributing-to-oracleai)
*   [18. License Information](#18-license-information)
*   [19. Appendix A](#19-appendix-a)
*   [20. Appendix B](#20-appendix-b)
*   [21. Design Document](#21-design-document)

## 1. Vision & Philosophy

### 1.1. Core Vision
OracleAI is conceived as more than a mere assistant; it is an **evolving cognitive partner**, a personalized AI council designed to augment human intellect and creativity. It aims to provide users with a deeply integrated, locally-run system that offers strategic guidance, manages personal knowledge over vast timescales, understands emotional context, and facilitates profound self-reflection and goal achievement. OracleAI strives to be a trusted, private, and powerful extension of the user's own mind.

### 1.2. Guiding Principles

The development of OracleAI is anchored by the following fundamental principles:

#### 1.2.1. Local-First Processing & Privacy-Centric Design
All core AI computations (LLM inference, STT, primary TTS, memory operations, emotional analysis) and data storage (the entirety of the Akashic Record) **must** reside and execute on user-controlled hardware. User data is sacrosanct and will not leave the local environment without explicit, informed user consent for specific, user-initiated actions (e.g., encrypted backups to a user-chosen location, opt-in API calls). This principle ensures maximum user privacy, data sovereignty, operational control, and robust offline functionality, mitigating risks associated with cloud dependencies.

#### 1.2.2. Multi-Agent Synergy & Specialized Roles
OracleAI employs a council of distinct AI agents (Sage, Seer, Shaman), each with specialized roles, simulated cognitive styles (via prompting, temperature settings, and potentially different underlying LLMs), and unique voices. This mimics the power of diverse human teams, where logical analysis (Sage), creative intuition (Seer), and deep synthesis (Shaman) converge to provide more comprehensive understanding, balanced decision support, and innovative problem-solving than a monolithic AI could achieve.

#### 1.2.3. Deep & Evolving Memory (The Akashic Record)
A persistent, multi-layered, and structured memory system is the cornerstone of OracleAI. The Akashic Record is designed to store raw interaction data, synthesized knowledge, user profiles, goals, and tasks indefinitely. It must support efficient, contextually relevant retrieval and facilitate continuous learning, adaptation, and refinement through both AI-driven processes and direct user collaboration. This overcomes the inherent context limitations of LLMs, enabling true long-term continuity and personalized understanding.

#### 1.2.4. Integrated Emotional Intelligence
OracleAI will actively perceive, interpret, and utilize user emotional cues derived from both spoken language (voice tone via Speech Emotion Recognition - SER) and transcribed text (sentiment analysis). This emotional context is a critical input for the AI agents, enabling more natural, empathetic, contextually appropriate, and effective human-AI interactions. Emotional data will also be logged for trend analysis, contributing to a deeper understanding of user well-being and interaction patterns.

#### 1.2.5. User Empowerment & Collaborative Interaction
The user is the ultimate authority and a collaborative partner in OracleAI's operation. The system will provide transparent mechanisms for users to guide AI behavior, explicitly add, edit, verify, and manage memories within the Akashic Record, configure agent parameters, control privacy settings, and override AI suggestions. This collaborative approach builds trust, ensures the AI remains aligned with user goals, allows for the correction of AI errors or biases, and positions OracleAI as a powerful tool *for* the user.

#### 1.2.6. Modularity, Extensibility, and Openness
System components (interfaces for STT, TTS, LLM, Memory modules, Search, Calendar, Emotion Analysis, etc.) will be designed with well-defined APIs and minimal interdependencies. This promotes easier maintenance, testing, component upgrades (e.g., swapping STT engines), and the future addition of new features, data sources, or even community-developed modules. The Akashic Record's core data formats will be designed with interoperability in mind.

#### 1.2.7. Practicality, Performance, and Adaptability
While ambitious, OracleAI targets reasonably high-end consumer hardware as a baseline. Real-time interaction loops involving Sage and Seer will be optimized for acceptable latency. User expectations for high-latency deep analysis tasks performed by Shaman will be clearly managed through UI and narrative framing. The system will include features for resource management (e.g., "Shaman Focus" mode) to adapt to varying hardware capabilities.

## 2. Core Features at a Glance

OracleAI integrates a comprehensive suite of advanced capabilities:

*   **AI Council:** Interact with three distinct, specialized AI agents: Sage (Analyst-Strategist), Seer (Creative Catalyst), and the optional Shaman (Deep Brain Consultant).
*   **Flexible LLM Backend:** Utilizes user-run **KoboldCpp** instances, supporting a wide range of GGUF-formatted Large Language Models (LLMs) and Vision Language Models (VLMs).
*   **Akashic Record Memory System:** A sophisticated, persistent, multi-layered memory architecture including:
    *   **Chronicle:** Immutable raw logs of all interactions, emotions, and system events.
    *   **Synthesis Store:** Structured, queryable knowledge base (SQLite recommended) containing user-verified summaries (daily, weekly, monthly with fidelity scores), extracted entities & relationships (Knowledge Graph simulation), key facts & decisions, consolidated project/topic threads, and Shaman's analytical reports.
    *   **Collaborative Memory Consolidation:** User-in-the-loop process for high-fidelity daily memory creation.
    *   **Memory Bank Context Scaler:** Advanced RAG engine for dynamic, token-budget-aware context retrieval.
    *   **User Profile & Preferences Database.**
    *   **Task & Action Queue Database.**
*   **Emotional Intelligence Suite:**
    *   Speech Emotion Recognition (SER) from user voice.
    *   Text Sentiment Analysis (VADER, NRCLex, TextBlob, etc.).
    *   Emotional context provided to LLMs and logged for trend analysis.
*   **High-Fidelity Speech-to-Text (STT):** `openai-whisper` library (e.g., `large-v2` model), GPU-accelerated.
*   **Configurable Text-to-Speech (TTS):** Agent-specific engine selection:
    *   **Piper TTS:** Fast, CPU-based, multiple distinct voices.
    *   **Coqui XTTSv2 (Optional):** High-quality voice cloning, expressive (GPU-based).
*   **Multimodal Vision:** Processes screenshots/images via VLMs in KoboldCpp.
*   **Advanced Web Search:** Simple (DuckDuckGo) and Deep Search (recursive scraping, Reddit/PRAW), with proxy support and planned multi-engine capability.
*   **Calendar Integration:** Securely syncs with external calendars (Google, Outlook planned), storing events locally for contextual awareness and proactive reminders.
*   **Multiple Interaction Modes:** Standard Interaction (Sage/Seer), Oracle Consultation (User + Sage + Seer + responsive Shaman), and Shaman Focus (resource dedication for deep analysis).
*   **Guided Generation & Refinement:** User tools to directly guide AI responses, provide corrections, and manage persistent contextual instructions.
*   **Remote Access Architecture:** Built-in FastAPI server for secure interaction from other devices via a client application (client not included).
*   **Privacy & Security:** Local-first processing, database encryption (SQLCipher), encrypted backups (7-Zip), secure API practices, no unauthorized telemetry.
*   **Thematic User Interface (Conceptual):** Envisioned "Oracle/Mystic Temple" GUI with distinct agent visuals, Shaman "Hyperspace Travel" indicators, and integrated system controls.

## 3. The OracleAI Council: Agent Personas & Roles

OracleAI's core intelligence is embodied by a council of three distinct AI agents, each designed with a specific archetype, function, and operational style to provide multifaceted support to the user.

### 3.1. Sage (The Analyst-Strategist)

*   **Archetype:** The Wise Teacher, Philosopher, Logical Planner. Evokes themes of Ice/Winter, clarity, structure, and accumulated wisdom.
*   **Core Function:** Sage is the council's anchor in logic, data, and structured thought. It excels at analyzing information from the Akashic Record and external sources, performing rigorous fact-checking, identifying logical patterns and inconsistencies, formulating clear step-by-step plans, and providing objective, evidence-based guidance.
*   **Key Responsibilities:**
    *   Analyzing user queries and contextual information against all layers of the Akashic Record.
    *   Conducting structured web searches (Simple Search, or initiating Deep Search tasks).
    *   Developing strategic plans, outlining actionable steps, and defining task dependencies.
    *   Evaluating risks, resource requirements, and the feasibility of proposed actions or goals.
    *   Generating concise, evidence-based explanations, reports, and summaries.
    *   Leading the structured data extraction phase of the Collaborative Daily Reflection process.
    *   Maintaining logical consistency within discussions and memory.
*   **LLM Configuration:** Utilizes a KoboldCpp instance, ideally with an LLM known for strong reasoning, instruction following, and analytical capabilities. Operates at a **low temperature** (e.g., 0.0-0.3) to ensure focused, deterministic, and precise outputs.
*   **TTS Voice:** Recommended: Piper TTS, configured with a voice profile that is calm, clear, articulate, measured, and conveys wisdom (e.g., a professorial or experienced guide's tone).

### 3.2. Seer (The Catalyst)

*   **Archetype:** The Visionary, Intuitive, Creative Spark, Empath. Evokes themes of Fire/Summer, passion, intuition, and transformative insight.
*   **Core Function:** Seer is the council's wellspring of creativity, emotional insight, and unconventional thinking. It excels at challenging assumptions, exploring novel possibilities, interpreting underlying emotional currents (from SER/Sentiment data), and facilitating dynamic, exploratory discussions.
*   **Key Responsibilities:**
    *   Generating novel ideas, alternative solutions, and "outside-the-box" perspectives for problems or goals.
    *   Playing the "devil's advocate" to stress-test plans and assumptions from Sage or the user.
    *   Interpreting user emotional data (voice tone, text sentiment) to provide empathetic context and tailor communication.
    *   Injecting considerations of human impact, values, and potential emotional consequences into strategic discussions.
    *   Identifying potential synergies, unexpected opportunities, or future possibilities that might be overlooked by purely logical analysis.
    *   Facilitating brainstorming sessions and asking probing "what if" questions to stimulate deeper thought.
    *   Contributing to the nuance and sentiment capture during the Collaborative Daily Reflection process.
*   **LLM Configuration:** Utilizes a KoboldCpp instance, with an LLM that excels at creative generation, nuanced language understanding, and perhaps role-playing. Can be the same base model as Sage but run with different system prompts and a **high temperature** (e.g., 0.6-1.2) to encourage diverse and imaginative outputs.
*   **TTS Voice:** Recommended: Coqui XTTSv2 for maximum expressiveness and the potential for a unique, user-cloned voice, accepting the associated resource cost. Alternatively, a distinct, dynamic, and perhaps slightly unconventional Piper TTS voice. Voice profile should be expressive, intuitive, and engaging.

### 3.3. Shaman (The Deep Brain Consultant)

*   **Archetype:** The Mediator between worlds, Mystic Synthesizer, Deep Diver into the "DataSide" (the vast realm of information). Evokes themes of the cosmos, spirit world, profound depth, and transformative synthesis.
*   **Core Function:** (Optional agent, primarily operates asynchronously during user inactivity or for explicitly delegated complex tasks). The Shaman leverages OracleAI's most powerful LLM configuration to perform computationally intensive, large-scale analysis, synthesis, and pattern recognition across the entire Akashic Record and extensive external data. It bridges raw data with profound, often non-obvious, understanding.
*   **Key Responsibilities:**
    *   Executing complex, long-running analytical tasks assigned via the Task & Action Queue.
    *   Performing deep analysis of historical trends across all components of the Akashic Record (Chronicle, Synthesis Store, Calendar, Profile).
    *   Identifying subtle correlations, anomalies, complex patterns, and emergent themes that may not be visible through surface-level analysis.
    *   Synthesizing vast amounts of information from extensive Deep Searches or large user-provided document sets.
    *   Generating comprehensive analytical reports, long-range forecasts, or complex scenario modeling.
    *   Potentially running advanced NLP pipelines for Knowledge Graph population (e.g., Named Entity Recognition, Relationship Extraction at scale).
    *   Conducting periodic memory maintenance tasks (e.g., proposing de-duplication or archiving strategies).
*   **LLM Configuration:** Utilizes a dedicated KoboldCpp instance, configured with the largest and most capable GGUF model the user's hardware can support (potentially distributed across multiple PCs or using advanced RAM/SSD offloading). Operates at a **moderate temperature** (e.g., 0.3-0.6, task-adjustable) to balance coherence with depth of exploration.
*   **TTS Voice:** Piper TTS, with a distinct voice profile that is deep, resonant, calm, and conveys profoundness.
*   **Interaction Model:** Primarily asynchronous. Its significant processing time is narratively framed as a "hyperspace journey" (e.g., to the Moon, Mars, Jupiter, Saturn, etc.), with UI indicators reflecting the "distance" (latency) and progress. Delivers findings as structured reports to the Synthesis Store or via notifications. Can be queried by Sage/Seer during their autonomous discussions. Requires "Shaman Focus" mode on resource-constrained systems.

## 4. The Akashic Record: A Deep Dive into the Memory System

The Akashic Record is the central, persistent, and evolving knowledge base of OracleAI. It is not a single database but a sophisticated, multi-component system designed to store diverse information types over long periods, facilitate intelligent retrieval, and enable deep synthesis by the AI council. All components are stored locally and can be encrypted.

### 4.1. Chronicle (Immutable Raw Logs)
*   **Purpose:** The foundational layer, serving as the unalterable ground truth of all interactions (user and AI), detected emotions, system events, and key processing metadata. Provides complete traceability and is the primary source for all subsequent analysis and synthesis.
*   **Format:** Series of JSON Lines files (`.jsonl`), typically one per day (e.g., `[AKASHIC_RECORD_PATH]/Chronicle/YYYY-MM-DD_chronicle.jsonl`), allowing efficient append-only operations.
*   **Key Data per Entry:** Timestamp, unique turn ID, session ID, speaker (user, Sage, Seer, Shaman, system), raw STT output, final processed text, user audio file path, detailed SER and text sentiment scores/labels, agent LLM/TTS metadata (model used, latency, context length), and system event details.

### 4.2. Synthesis Store (Processed Knowledge & Insights)
*   **Purpose:** The primary repository for structured, processed, and synthesized knowledge derived from the Chronicle and direct user input. This is the AI's active "working memory" and curated knowledge base, designed for efficient querying and relational integrity.
*   **Storage:** Recommended: A single **SQLite database** (`synthesis.db`) encrypted with **SQLCipher**. Alternatively, a structured JSON file (`memory_bank.json`) for simpler setups, though SQLite offers superior querying and scalability.
*   **Key Components (Tables in SQLite / Top-level keys in JSON):**
    *   **`PermanentMemory`:** User-defined critical, timeless facts and directives.
    *   **`Entities`:** Detailed records of people, projects, organizations, concepts, tools, etc., including their type, name, aliases, descriptions, status, tags, custom properties, and explicit relationships to other entities (forming a knowledge graph simulation).
    *   **`FactsDecisions`:** Atomic, verifiable statements, choices made, hypotheses, or key questions, linked to source Chronicle turns and relevant entities. Includes reasoning summaries and confidence scores where applicable.
    *   **`Summaries` (Hierarchical):**
        *   **Daily Summaries:** Generated via the Collaborative Daily Reflection process, user-verified. Include multi-level narrative summaries (short, medium, detailed, key points), extracted keywords, overall sentiment overview for the day, and a "fidelity estimate" score indicating summarization quality relative to the Chronicle.
        *   **Weekly & Monthly Summaries:** Higher-level summaries generated by Sage or Shaman, synthesizing multiple daily or weekly summaries, respectively. Focus on overarching themes, progress, and significant changes.
    *   **`ProjectTopicThreads`:** Dynamically updated, consolidated summaries focused on specific long-running entities (projects, key concepts), tracking their status, key developments, milestones, and outstanding issues.
    *   **`PatternAnalysisReports`:** Structured reports generated by Shaman detailing findings from deep analysis of trends, correlations, and anomalies across the Akashic Record.

### 4.3. Calendar Cache (`calendar.db`)
*   **Purpose:** A local SQLite database (SQLCipher encrypted) storing events synced from the user's external calendar services (e.g., Google Calendar, Outlook Calendar).
*   **Function:** Provides temporal context for conversations, enables proactive reminders, assists in planning, and allows Shaman to correlate calendar activity with other data trends. Updated via secure OAuth 2.0 and periodic background sync.

### 4.4. User Profile & Preferences (`profile.db`)
*   **Purpose:** An SQLite database (SQLCipher encrypted) storing explicit user preferences, defined goals (with status and priority), key contacts/relationships, communication style notes, and agent configuration overrides (e.g., preferred TTS voices, temperature settings).
*   **Function:** Enables deep personalization of AI behavior, responses, and goal-oriented assistance. Updated via direct user commands or confirmed inferences from AI analysis.

### 4.5. Task & Action Queue (`tasks.db`)
*   **Purpose:** An SQLite database (SQLCipher encrypted) for managing tasks assigned to AI agents, particularly asynchronous, long-running tasks for Shaman. Tracks task descriptions, assigned agent, status (pending, running, complete, failed), priority, and references to results.
*   **Function:** Enables delegation of complex work, background processing, and tracking of AI-initiated follow-up actions.

### 4.6. Knowledge Graph (Conceptual - Future Enhancement)
*   **Purpose:** To explicitly model complex, n-ary relationships between entities beyond what simple relational links in the `Entities` table can capture.
*   **Implementation:** Initially simulated using the `Entities` and `Relationships` tables in `synthesis.db`. Future development could involve migrating to a dedicated Graph Database (e.g., Neo4j) for advanced traversal queries and inferencing if needed.

### 4.7. Vector Store (for Semantic Search - Future Enhancement)
*   **Purpose:** To enable retrieval of memory items based on semantic meaning rather than just keywords.
*   **Implementation:** Will involve generating vector embeddings (using models like `mxbai-embed-large` or others) for text chunks from the Chronicle and narrative summaries in the Synthesis Store. These embeddings will be stored in a dedicated Vector Database (e.g., ChromaDB, FAISS index managed alongside SQLite metadata) and queried by the Memory Bank Context Scaler.

### 4.8. Key Memory Processes
*   **4.8.1. Collaborative Daily Reflection & Structured Extraction:** A cornerstone user-in-the-loop process where Sage/Seer assist the user in reviewing the day's Chronicle, extracting key entities/facts/decisions into the Synthesis Store, and co-creating verified, multi-level daily narrative summaries. This minimizes information loss and ensures memory accuracy.
*   **4.8.2. Hierarchical & Thematic Summarization:** Automated (by Sage or Shaman) processes that create weekly, monthly, and project/topic thread summaries by synthesizing lower-level verified memories.
*   **4.8.3. Memory Bank Context Scaler (RAG Engine):** A critical real-time process that dynamically retrieves, ranks, and selects the most relevant information from all components of the Akashic Record to construct a concise context string fitting the active LLM's token limit for each user query.
*   **4.8.4. Deep Pattern Weaving (Shaman's Analysis):** Shaman's autonomous, offline analysis of the entire Akashic Record to identify long-term trends, correlations, anomalies, and generate profound insights.
*   **4.8.5. Word Frequency Indexing (Optional Analysis):** Background process to create per-log and master word frequency lists for thematic analysis by Shaman.

## 5. Emotional Intelligence Suite

OracleAI is designed to perceive, understand, and appropriately respond to user emotions, fostering a more natural, empathetic, and effective interaction. This is achieved through a dedicated suite of analysis tools and by integrating emotional context into the AI agents' processing.

*   **Speech Emotion Recognition (SER):**
    *   **Technology:** Utilizes pre-trained deep learning models (e.g., Wav2Vec2-based architectures from Hugging Face) running on the GPU via PyTorch and the Transformers library.
    *   **Process:** After STT, the original user audio utterance (`.wav` file) is fed to the SER model. Acoustic features are extracted (using `librosa` on CPU as a pre-processing step if required by the SER model) to analyze prosody, tone, pitch, energy, and other vocal cues.
    *   **Output:** Provides a primary emotion label (e.g., "happy," "sad," "angry," "neutral," "surprised," "fearful," "disgusted") and potentially a confidence score or probability distribution across multiple emotions.
    *   **Integration:** This voice-derived emotion is logged in the Chronicle and provided as key context to Sage, Seer, and Shaman, allowing them to understand the emotional undercurrent of the user's spoken words, even if the text itself is neutral.
*   **Text Sentiment & Emotion Analysis:**
    *   **Technology:** Employs a suite of established Python libraries running on the CPU:
        *   **VADER (Valence Aware Dictionary and sEntiment Reasoner):** Provides a compound sentiment score (-1 to +1) and positive/neutral/negative proportions, particularly effective for nuanced or social media-like text.
        *   **TextBlob:** Offers polarity (-1 to +1) and subjectivity (0 to 1) scores.
        *   **NRCLex:** Identifies associations with Plutchik's basic emotions (joy, sadness, anger, etc.) and positive/negative sentiment based on word lexicons.
    *   **Process:** Applied to the transcribed text from STT.
    *   **Output:** Numerical scores and categorical emotion labels.
    *   **Integration:** Logged in the Chronicle alongside SER data. Used by AI agents to cross-reference with voice emotion, detect sarcasm (conflicting text/voice cues), and understand the explicit emotional content of the text.
*   **Contextual Use by Agents:**
    *   **Seer:** Primarily leverages emotional data to provide empathetic responses, understand subtext, and guide creative or interpersonal discussions.
    *   **Sage:** Uses emotional data as another input for analysis, noting how sentiment might correlate with topics or decisions.
    *   **Shaman:** Analyzes long-term emotional trends from the Chronicle and Synthesis Store, correlating them with events, topics, goals, and other data points to generate insights about user well-being or recurring emotional patterns.
*   **Emotional Logging & Trend Analysis:** All detected emotional data is timestamped and stored in the Chronicle, forming a rich dataset for the Shaman's pattern analysis, allowing for visualization of emotional trends over time (a potential GUI feature).

## 6. Multimodal Capabilities (Voice, Text, Vision)

OracleAI is designed to interact with and understand information across multiple modalities:

*   **Voice (Primary Input/Output):**
    *   **Input:** Real-time voice capture via microphone, processed by Voice Activity Detection (VAD) in `audio_processing.py`.
    *   **STT:** High-accuracy transcription using `openai-whisper` (`large-v2` recommended) on GPU.
    *   **Output:** Synthesized speech via agent-configurable TTS engines (Piper TTS for speed/efficiency, Coqui XTTSv2 for expressiveness/cloning).
*   **Text (Internal & Potential Input/Output):**
    *   **Internal Representation:** All voice input is converted to text for LLM processing. LLM outputs are text before TTS.
    *   **GUI Input (Future):** The planned GUI will allow direct text input as an alternative or supplement to voice.
    *   **Memory Storage:** The Akashic Record primarily stores information in textual or structured text-based formats (JSON, SQLite text fields).
*   **Vision (Screenshot Analysis):**
    *   **Mechanism:** OracleAI can capture screenshots of the user's current screen.
    *   **Processing:** The screenshot image data is sent to a multimodal Vision Language Model (VLM) running within a KoboldCpp instance (e.g., Llava, Fuyu, or other GGUF-compatible VLMs).
    *   **Output:** The VLM provides a textual description of the image content, including potential OCR for on-screen text.
    *   **Integration:** This textual description is provided as context to Sage, Seer, or Shaman, allowing them to "see" what the user is looking at and incorporate it into their understanding and responses. Useful for discussing on-screen content, troubleshooting, or providing context-aware assistance.

## 7. Interaction Modes & User Control

OracleAI offers several distinct modes to tailor the interaction style and resource usage, all under user control via voice commands or the planned GUI.

### 7.1. Standard Interaction Mode
*   **Default mode** for real-time conversation and assistance.
*   **Active Agents:** Sage and Seer. Shaman operates only on pre-assigned background tasks.
*   **Flow:** Standard VAD -> STT -> Emotion Analysis -> Context Scaling -> LLM (Sage/Seer) -> TTS loop.
*   **Purpose:** General queries, task assistance, information retrieval, ongoing discussions.

### 7.2. Oracle Consultation / Roundtable Mode
*   **Activation:** Explicit user command (e.g., "OracleAI, begin consultation").
*   **Active Agents:** Sage, Seer, *and* Shaman participate actively.
*   **Shaman Responsiveness:** User can set Shaman's desired "depth" or "latency" for this session (e.g., "Moon" for quick contributions from existing synthesized knowledge, "Mars" for more involved analysis during the session, "Saturn+" for delegating parts of the consultation to longer offline processing). The GUI's "Hyperspace Travel" indicator reflects this.
*   **Turn-Taking:** Configurable (user-defined order, round-robin, or a hybrid allowing intelligent interjections).
*   **AFK Behavior:** If the user is inactive, Sage and Seer can be prompted to continue discussing the current topic, potentially queuing deeper questions for Shaman. Their discussion is logged.
*   **Purpose:** Collaborative brainstorming, multi-faceted problem-solving, strategic planning involving all AI perspectives and the user simultaneously.

### 7.3. Shaman Focus Mode (Resource Management)
*   **Activation:** Explicit user command (e.g., "OracleAI, prioritize Shaman," "Activate Deep Focus").
*   **Function:** Designed for systems with constrained VRAM/resources. OracleAI attempts to stop/idle the KoboldCpp instances serving Sage and Seer (via `subprocess` or OS signals), freeing up their VRAM and GPU resources.
*   **Shaman Allocation:** These freed resources are then available for the Shaman's KoboldCpp instance, allowing it to run larger models or process tasks more efficiently.
*   **User Interaction:** Limited while this mode is active, primarily focused on initiating or checking the status of Shaman's deep analysis tasks. High latency is expected and communicated.
*   **Deactivation:** User command toggles the mode off, prompting OracleAI to restart Sage and Seer's KoboldCpp instances.

### 7.4. Guided Generation & Interaction Refinement
*   **Concept:** Inspired by SillyTavern's "Guided Generations," OracleAI will incorporate mechanisms for the user to provide fine-grained, turn-by-turn control over AI agent responses.
*   **Implementation (via voice commands/GUI):**
    *   **"Guide Next Response":** User provides specific instructions (e.g., "Sage, guide: Respond to that with only three bullet points focusing on cost.") which are prepended to the LLM prompt.
    *   **"Refine Last Response":** User provides corrective feedback (e.g., "Seer, correction: Make that more optimistic and add a historical analogy."). The system re-prompts the agent with its previous response and the user's correction.
    *   **"Persistent Session Guides":** User can set temporary rules or focus points for the current session (e.g., "Session Guide: For this discussion, always consider the environmental impact.") that are injected into prompts. Managed via commands to add, view, or flush these guides.
*   **Logging:** These guidance and correction interactions are logged in the Chronicle for transparency and to understand how AI outputs were shaped.

### 7.5. Toggleable States (Mute, Search)
*   **Mute State:** Suppresses unsolicited AI speech output from Sage/Seer in any interactive mode. They still listen and process.
*   **Search Feature:** Enables Simple or Deep web search (via `search_module.py`) to be performed before an AI agent generates its response to a user query. Results are fed into the LLM context.

## 8. Web Connectivity & External Data

OracleAI leverages external web resources in a controlled, opt-in manner:

*   **Web Search:**
    *   **Engines:** Primarily DuckDuckGo via `duckduckgo_search`. Planned support for user-configurable multiple search engines.
    *   **Simple Search:** Retrieves concise text snippets.
    *   **Deep Search:** Involves recursive web page scraping (`requests`, `BeautifulSoup4`) for detailed information extraction, and targeted Reddit searches (`praw`) for community discussions and opinions. LLMs are used for relevance filtering and summarization of scraped content.
*   **Proxy Support:** Optional routing of all external HTTP/HTTPS requests (Search, Reddit API, Calendar API if applicable) through a user-configured TOR SOCKS proxy or a standard VPN (system-level or via `requests` proxy settings) for enhanced privacy.
*   **Calendar APIs:** Securely connects to Google Calendar, Outlook Calendar (or other CalDAV services) via OAuth 2.0 to sync event data.
*   **Data Minimization:** Only necessary information is sent with API requests (e.g., search queries, calendar sync tokens).

## 9. Remote Access Architecture

OracleAI is designed to be accessible beyond the host machine:

*   **FastAPI Server (`remote_api.py`):** A robust, asynchronous Python web server runs locally on the OracleAI host machine.
    *   **Endpoints:** Exposes secure API endpoints for core functionalities:
        *   `/chat`: Main interaction endpoint, receives user text (and potentially client-side emotion/SER data), orchestrates the full processing loop (Context Scaler, LLM, etc.), returns AI text response.
        *   `/transcribe` (Optional): Receives raw audio from client, performs STT, returns text.
        *   `/synthesize` (Optional): Receives text, performs TTS, returns audio data.
        *   `/status`: Provides system/agent status.
        *   `/memory_query` (Future): Endpoints for querying specific parts of the Akashic Record.
        *   `/task_management` (Future): Endpoints for managing Shaman's tasks.
    *   **Data Validation:** Uses Pydantic models for request and response validation.
    *   **Security:** Binds to `127.0.0.1` by default. Network access requires explicit configuration. Authentication (e.g., API keys, JWT) should be implemented for external access.
*   **Client Application (User-Provided):**
    *   OracleAI provides the server-side API. The user would use a separate client application (e.g., a custom web UI, a mobile app, or even another script) to interact remotely.
    *   **Recommended Client Behavior:** For optimal performance and privacy, the remote client should handle its own STT (using device capabilities) and TTS (using device capabilities or a lightweight web TTS). It then sends/receives text to/from the OracleAI FastAPI server.
*   **Networking for External Access:**
    *   **Tailscale / ZeroTier (Highly Recommended):** Create a secure, private mesh network between the OracleAI host and remote client devices without complex firewall configuration or port forwarding.
    *   **VPN:** Connect the remote device to the OracleAI host's local network via a traditional VPN.
    *   **Port Forwarding (Use with Caution):** If direct internet exposure is necessary, ensure robust API authentication and HTTPS are implemented.

## 10. User Interface (UI) Concept & Aesthetic

While OracleAI's core logic can operate headlessly or via a simple command-line interface, a dedicated graphical user interface (GUI) is envisioned to provide a rich, immersive, and intuitive user experience, fully realizing the "Oracle/Mystic Temple" aesthetic.

*   **Overall Aesthetic Vision:** A blend of high-tech geometric/circuitry elements with classical, esoteric, and subtly luxurious influences (Art Deco, Ancient Egyptian, Venetian). The UI should feel like interacting with an advanced, ancient, yet digital oracle.
    *   **Color Palettes:** Dark, deep backgrounds (space blue, charcoal) with glowing accents.
        *   **Sage (Ice):** Cool blues, cyans, silvers, whites.
        *   **Seer (Fire):** Warm reds, oranges, magentas, golds.
        *   **Shaman (Deep Brain):** Deep indigos, cosmic purples, starlight silver, with flashes of gold or electric blue from the "DataSide" stream.
        *   **General Accents:** Art Deco golds, bronzes; Egyptian lapis lazuli; Venetian deep reds, aquamarines.
    *   **Motifs:** Geometric circuits, radiating lines (sunbursts), chevrons, stepped forms, stylized hieroglyph-inspired icons, intricate latticework, abstracted arches.
*   **Key GUI Components (Conceptual):**
    *   **Main Interaction View:**
        *   Displays the conversation log with distinct visual styling for User, Sage, Seer, and Shaman turns (e.g., color-coded chat bubbles, unique avatar icons).
        *   Input area for text (supplementing voice) and buttons for "Guided Generation" commands.
    *   **Agent Status Panel:**
        *   Clearly indicates which agent(s) are currently active or speaking.
        *   Displays avatars (default options inspired by historical/fictional figures like Athena/Spock for Sage, Pythia/Oracle for Seer, Hermes Trismegistus/Ancient One for Shaman; user-customizable).
    *   **Shaman "Hyperspace Travel" Dashboard:**
        *   Visual representation of Shaman's current task and processing depth (e.g., a golden Merkaba icon traveling along a path of celestial bodies: Earth Orbit -> Moon -> Mars -> Jupiter -> Saturn -> Uranus -> Neptune -> Pluto -> Kuiper Belt -> Heliopause -> Oort Cloud, each representing increasing latency/complexity).
        *   Displays current task description, estimated time remaining (if possible), and Shaman's operational mode (e.g., "Analyzing Chronicle," "Synthesizing Search Data," "Deep Pattern Weaving").
        *   Background could feature dynamic "DataSide" visuals (flowing energy, Matrix/symbol rain, chameleon particles) reflecting Shaman's activity.
    *   **Context & Status Sidebars/Dashboards:**
        *   **Emotional Readout:** Small, real-time display of user's detected voice emotion (SER) and text sentiment (VADER, etc.) using icons or gauges.
        *   **Akashic Record Access Indicator:** Visual cues showing if memory is being actively queried or written to.
        *   **Task Queue Overview:** A summarized list of pending/active tasks for Shaman and other agents.
        *   **Calendar Snippet:** Display of today's/tomorrow's key events.
        *   **System Performance (Optional):** Basic CPU/GPU/VRAM usage indicators.
    *   **Mode Control Panel:** Buttons/toggles for switching between Standard Interaction, Oracle Consultation, and Shaman Focus modes. Controls for Mute and Search states.
    *   **Settings Module:** A comprehensive interface for:
        *   Editing `.env` configurations (masking sensitive values like API keys).
        *   Selecting TTS engines and voice models/samples per agent.
        *   Adjusting default LLM temperatures for agents.
        *   Managing Calendar API connections and sync settings.
        *   Configuring RAG parameters for the Memory Bank Context Scaler.
        *   Managing privacy and logging levels.
    *   **Akashic Record Management Interface (Future - Advanced):**
        *   Browser for Chronicle logs (searchable, filterable).
        *   Viewer/Editor for Synthesis Store components (Entities, Facts, Summaries, Threads).
        *   Interface for initiating collaborative memory reflection sessions.
        *   Controls for manual backup/restore (triggering the 7-Zip module).
*   **Iconography:** A custom, consistent set of icons using the geometric line style, inspired by symbols from Image 2 (Brain, Heart, Eye, Network, Wave, Delta) and thematic elements (stylized Eye of Horus, Ankh, Lotus).
*   **Typography:** A combination of:
    *   Clean, readable sans-serif with a tech feel for UI text and body content (e.g., Titillium Web, Exo 2).
    *   Elegant, classical serif or stylized display font for main titles, agent names, and key headers (e.g., Cinzel, Audiowide).
    *   Clear monospaced font for data readouts or log views (e.g., Source Code Pro).
*   **Technology (Potential):** PyQt/PySide for rich desktop application capabilities and custom styling (QSS). Kivy for unique, multi-touch UIs. Web technologies (React/Vue/Svelte + FastAPI for backend) packaged with Electron/Tauri for maximum design flexibility.

## 11. Privacy, Security, and Data Management

OracleAI is architected with user privacy and data security as paramount concerns. The "local-first" principle is central to this commitment.

*   **Local Data Storage & Processing:** All core AI operations (LLM inference, STT, TTS, SER) and the entire Akashic Record (Chronicle, Synthesis Store, Profile, Calendar Cache, Tasks) are processed and stored exclusively on the user's local hardware. No personal conversational data or memory content is transmitted to external servers without explicit user action and consent.
*   **Encryption at Rest:**
    *   **OS-Level Full Disk Encryption (FDE):** Strongly recommended as a foundational security layer (BitLocker, FileVault, LUKS).
    *   **Database Encryption:** All SQLite databases (`synthesis.db`, `calendar.db`, `profile.db`, `tasks.db`) **must** be encrypted using **SQLCipher** (e.g., via `pysqlcipher3`), requiring a user-defined master password for runtime access.
    *   **Akashic Record Backup Encryption:** The integrated 7-Zip backup feature provides user-prompted, password-protected AES-256 encryption for exported archives of the Akashic Record.
    *   **Chronicle Log Encryption (Optional Enhancement):** Direct AES-256 encryption of daily `.jsonl` Chronicle files is a potential future enhancement for an added security layer, though it adds complexity to append/read operations.
*   **Secure Configuration:**
    *   Sensitive settings (API keys, master password hashes/salts) in the `.env` file must be protected by strict operating system file permissions.
    *   Consideration for using OS-level secure credential stores (Windows Credential Manager, macOS Keychain, Linux Keyring) for managing external API keys and the OracleAI master password.
*   **Network Security:**
    *   **Remote API (FastAPI):** Binds to `127.0.0.1` (localhost) by default. Network exposure (`0.0.0.0`) requires explicit user configuration and understanding of security implications.
    *   **Secure Remote Access:** **Tailscale** or a self-hosted VPN is strongly recommended for accessing the API from external networks, avoiding direct port forwarding.
    *   **HTTPS:** All external API calls made by OracleAI (e.g., to Search engines, Calendar services, Reddit) must use HTTPS.
*   **External API Calls & Data Minimization:**
    *   Features requiring external APIs are opt-in.
    *   OracleAI will be transparent about what data is sent (e.g., search queries, calendar sync requests).
    *   Only the minimum necessary data will be transmitted.
    *   Optional TOR/VPN proxy support for search/scraping further enhances anonymity.
*   **No Unauthorized Telemetry:** OracleAI will **not** collect or transmit any usage statistics, crash reports, performance data, or any other form of telemetry without explicit, granular, opt-in consent from the user for specific, clearly defined, and anonymized purposes.
*   **User Control & Transparency:**
    *   Users have control over memory creation, editing (with appropriate warnings), and deletion.
    *   Logging (Chronicle) provides a transparent record of AI actions and data processing.
    *   Clear documentation will outline data handling practices and user responsibilities.
*   **Data Management:**
    *   Users can export their entire Akashic Record (encrypted or unencrypted).
    *   Clear mechanisms for data deletion (e.g., purging specific memory entries or the entire Akashic Record) will be provided.

## 12. Installation & Setup Guide

**NOTE:** OracleAI is an advanced system with significant hardware and software dependencies. Installation requires technical proficiency. Future versions aim to simplify this with Docker or bundled installers.

### 12.1. System Prerequisites
*   **Operating System:** Windows 10/11 (64-bit), modern Linux distribution (e.g., Ubuntu 20.04+), or macOS (latest versions, Apple Silicon support TBD based on PyTorch/dependency compatibility).
*   **Python:** Version 3.11.x. Must be added to system PATH.
*   **Git:** For cloning the repository.
*   **NVIDIA GPU:** **Essential** for acceptable performance of STT (`openai-whisper`), SER model inference, optional XTTSv2 TTS, and LLM acceleration via KoboldCpp. Refer to "Hardware & VRAM Requirements."
*   **NVIDIA Drivers:** Latest stable version compatible with your GPU and the target CUDA Toolkit version.
*   **CUDA Toolkit:** Install the specific version required by the chosen PyTorch build (e.g., CUDA 11.8, 12.1, 12.4). Verify with `nvcc --version`.
*   **Audio Hardware:** Functioning microphone and speakers/headphones, properly configured in the OS.
*   **PortAudio Library:** Required by `pyaudio`.
    *   *Linux:* `sudo apt-get install portaudio19-dev libasound2-dev` (or similar for your distribution).
    *   *macOS:* `brew install portaudio`.
    *   *Windows:* May require downloading precompiled binaries (e.g., from [PortAudio website](http://www.portaudio.com/download.html) or a trusted source) and ensuring DLLs are in PATH or alongside Python, or installing as part of a larger audio SDK.
*   **7-Zip Archiver:** Install 7-Zip from [7-zip.org](https://www.7-zip.org/). Ensure `7z.exe` (or `7z`) is accessible via the system PATH, or provide the full path in OracleAI's `.env` configuration.
*   **C++ Build Tools (Optional, but Recommended for some dependencies):**
    *   *Windows:* Microsoft C++ Build Tools (from Visual Studio Installer).
    *   *Linux:* `build-essential` package or equivalent.
    *   *macOS:* Xcode Command Line Tools.

### 12.2. External Tool Dependencies & Setup
These tools are run as separate processes or called via `subprocess` and must be downloaded/configured by the user:
1.  **KoboldCpp:**
    *   Download the latest release executable for your OS from the official KoboldCpp GitHub repository or website.
    *   Download desired GGUF-formatted LLM and VLM models (e.g., from Hugging Face).
    *   Run KoboldCpp separately (potentially multiple instances for Sage, Seer, Shaman, on the same or different machines). Load the appropriate models.
    *   Ensure the KoboldCpp API server is enabled and note its URL and port (e.g., `http://127.0.0.1:5001`).
2.  **Piper TTS:**
    *   Download the `piper` executable for your OS from the official Piper TTS GitHub releases.
    *   Download desired `.onnx` voice model(s) and their corresponding `.onnx.json` config files (e.g., from the Hugging Face Piper voices page or other sources).
    *   Place the `piper` executable and all voice model files in a stable, known location.
3.  **SER Model (If not automatically downloaded by Transformers):**
    *   If using a specific pre-trained SER model that isn't auto-downloaded by the `transformers` library, download its model files (e.g., PyTorch `.bin`, ONNX, config files) and place them in a known location. The path will be needed in the `.env` file.

### 12.3. Python Environment & OracleAI Installation
1.  **Clone OracleAI Repository:**
    ```bash
    git clone <URL_to_OracleAI_Repository>
    cd OracleAI
    ```
2.  **Create and Activate Python Virtual Environment:**
    ```bash
    python -m venv .venv
    # Windows CMD:
    .\.venv\Scripts\activate
    # Windows PowerShell:
    # Set-ExecutionPolicy Unrestricted -Scope Process (if needed for first time)
    .\.venv\Scripts\Activate.ps1
    # Linux/macOS:
    source .venv/bin/activate
    ```
    Your prompt should now indicate `(.venv)`.
3.  **Install PyTorch (GPU Version - CRITICAL STEP):**
    *   Visit the official PyTorch website: [https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)
    *   Use the selection tool:
        *   **PyTorch Build:** Stable
        *   **Your OS:** Windows / Linux / macOS
        *   **Package:** Pip
        *   **Language:** Python
        *   **Compute Platform:** Select the CUDA version that **exactly matches your installed CUDA Toolkit** (e.g., CUDA 11.8, CUDA 12.1). *Do NOT guess.*
    *   Copy the generated `pip install torch torchvision torchaudio ...` command.
    *   Run this command in your activated virtual environment. This installation can be large and take time.
4.  **Install OracleAI Dependencies:**
    *   The project will provide a dependency management file:
        *   **If `requirements.lock` (from `pip-tools`) is provided (Preferred):**
            ```bash
            pip install -r requirements.lock
            ```
        *   **If `requirements.in` (for `pip-tools`) is provided:**
            ```bash
            pip install pip-tools
            pip-compile requirements.in -o requirements.txt
            pip install -r requirements.txt
            ```
        *   **If `pyproject.toml` (with Poetry or PDM, or just build system) is provided:**
            ```bash
            pip install .
            ```
        *   *Key dependencies to ensure are listed in the project's dependency file include: `openai-whisper`, `librosa`, `transformers`, `torch` (already installed), `pysqlcipher3` (or `sqlcipher3` + Python bindings), `vaderSentiment`, `nrclex`, `textblob`, `requests[socks]`, `pyaudio`, `sounddevice`, `fastapi`, `uvicorn`, `python-dotenv`, `google-api-python-client`, `google-auth-oauthlib`, `google-auth-httplib2` (for Google Calendar), `msal` (for Outlook Calendar), `praw`, `BeautifulSoup4`, `coqui-tts` (if XTTSv2 is enabled), `apscheduler`, `cryptography`.*
5.  **Download NLTK Data (if TextBlob/NRCLex need it):**
    *   Run Python interpreter: `python`
    *   Inside Python:
        ```python
        import nltk
        nltk.download('punkt') # For TextBlob sentence tokenization
        nltk.download('wordnet') # For some NRCLex features or lemmatization
        # Potentially others depending on specific NLP features used.
        exit()
        ```

### 12.4. Configuration (`.env` File)

OracleAI relies on a central `.env` file in the project's root directory for all its configuration settings. This file stores paths to external tools, model identifiers, API keys, agent parameters, and other operational settings.

1.  **Create `.env`:** If it doesn't exist, create a new file named `.env` in the root of your OracleAI project directory.
2.  **Use Template:** If an `.env.example` file is provided with the project, copy its contents into your new `.env` file as a starting template.
3.  **Populate Settings:** Carefully edit the `.env` file to reflect your specific setup. **Paths should typically be absolute paths unless relative paths are explicitly stated to work.**

    **Essential Settings Categories & Examples:**

    ```dotenv
    # --- General Application Settings ---
    LOG_LEVEL=INFO # DEBUG, INFO, WARNING, ERROR
    AKASHIC_RECORD_PATH=/path/to/your/oracleai_memory_data # Main directory for all memory files
    PYTHON_EXECUTABLE_PATH=/path/to/your/.venv/Scripts/python.exe # Or python3, for subprocesses if needed

    # --- LLM Backend (KoboldCpp) ---
    KOBOLDCPP_API_URL_SAGE=http://127.0.0.1:5001/api/v1/generate
    KOBOLDCPP_API_URL_SEER=http://127.0.0.1:5002/api/v1/generate # Different port if separate instance
    KOBOLDCPP_API_URL_SHAMAN=http://127.0.0.1:5003/api/v1/generate # Different port/machine

    # --- STT (OpenAI Whisper) ---
    WHISPER_MODEL_NAME=large-v2 # e.g., tiny, base, small, medium, large, large-v2, large-v3
    WHISPER_DEVICE=cuda # "cuda" or "cpu" (GPU highly recommended)

    # --- TTS (Piper & Optional XTTSv2) ---
    PIPER_EXECUTABLE_PATH=/path/to/piper/piper.exe
    # XTTS (if used by any agent)
    XTTS_MODEL_PATH=tts_models/multilingual/multi-dataset/xtts_v2 # Default, or path if custom
    XTTS_DEVICE=cuda # "cuda" or "cpu"

    # --- Emotion Analysis ---
    SER_MODEL_PATH_OR_HF_IDENTIFIER=jonatasgrosman/wav2vec2-large-xlsr-53-english # Example Hugging Face identifier
    SER_DEVICE=cuda # "cuda" or "cpu"

    # --- Agent Configurations ---
    # Sage
    SAGE_LLM_TEMPERATURE=0.2
    SAGE_TTS_ENGINE=piper
    SAGE_PIPER_VOICE_MODEL_PATH=/path/to/voices/sage_voice.onnx
    SAGE_PIPER_VOICE_CONFIG_PATH=/path/to/voices/sage_voice.onnx.json
    # Seer
    SEER_LLM_TEMPERATURE=0.9
    SEER_TTS_ENGINE=xtts # Example using XTTS for Seer
    SEER_XTTS_SPEAKER_WAV_PATH=/path/to/seer_voice_sample.wav
    SEER_PIPER_VOICE_MODEL_PATH=/path/to/voices/seer_voice.onnx # Fallback or alternative
    SEER_PIPER_VOICE_CONFIG_PATH=/path/to/voices/seer_voice.onnx.json
    # Shaman
    SHAMAN_LLM_TEMPERATURE=0.5
    SHAMAN_TTS_ENGINE=piper
    SHAMAN_PIPER_VOICE_MODEL_PATH=/path/to/voices/shaman_voice.onnx
    SHAMAN_PIPER_VOICE_CONFIG_PATH=/path/to/voices/shaman_voice.onnx.json

    # --- Memory System (Akashic Record) ---
    SQLCIPHER_MASTER_PASSWORD_PROMPT=True # True to prompt at startup, False to use env var below (less secure)
    # SQLCIPHER_MASTER_PASSWORD=your_very_strong_password_here # Use with caution if not prompting
    CHRONICLE_BASE_PATH=${AKASHIC_RECORD_PATH}/Chronicle
    SYNTHESIS_DB_PATH=${AKASHIC_RECORD_PATH}/Databases/synthesis.db
    CALENDAR_DB_PATH=${AKASHIC_RECORD_PATH}/Databases/calendar.db
    PROFILE_DB_PATH=${AKASHIC_RECORD_PATH}/Databases/profile.db
    TASKS_DB_PATH=${AKASHIC_RECORD_PATH}/Databases/tasks.db
    # For RAG Context Scaler
    RAG_QUERY_HISTORY_LENGTH=3
    RAG_SCORE_THRESHOLD=0.35
    RAG_MAX_RETRIEVED_CHUNKS=5
    RAG_CHUNK_SIZE_CHARS=1500
    RAG_CHUNK_OVERLAP_PERCENT=10
    # Embedding model for Vector Store (Future)
    # EMBEDDING_MODEL_NAME_OR_PATH=mxbai-embed-large
    # EMBEDDING_DEVICE=cuda # or cpu

    # --- Web Search ---
    SEARCH_DEFAULT_ENGINE=duckduckgo
    # For TOR/VPN Proxy (Optional)
    USE_PROXY_FOR_SEARCH=False
    PROXY_SOCKS_URL=socks5h://127.0.0.1:9050 # Example for TOR Browser default

    # --- Calendar Integration ---
    CALENDAR_SYNC_INTERVAL_MINUTES=60
    # Paths for OAuth credentials (will be created during first auth flow)
    GOOGLE_CALENDAR_CREDENTIALS_PATH=${AKASHIC_RECORD_PATH}/.credentials/google_calendar_token.json
    # OUTLOOK_CALENDAR_CREDENTIALS_PATH=...

    # --- Remote API (FastAPI) ---
    REMOTE_API_HOST=127.0.0.1 # Default to localhost for security
    REMOTE_API_PORT=8000
    # REMOTE_API_KEY=your_secret_api_key_for_clients # For securing the API (Future)

    # --- Backup ---
    SEVENZIP_PATH=C:/Program Files/7-Zip/7z.exe # Example for Windows

    # --- UI Toggles & Features ---
    ENABLE_REALTIME_SER_FOR_AGENTS=True # Toggle SER for Sage/Seer
    ```
    **Note:** Ensure paths are correct for your system (use forward slashes `/` or escaped backslashes `\\` on Windows).

### 12.5. API Keys & Authentication Setup

*   **Reddit API (for Deep Search):**
    1.  Create a Reddit app at [reddit.com/prefs/apps](https://www.reddit.com/prefs/apps) (select "script" type).
    2.  Note your `client ID` (under personal use script) and `client secret`.
    3.  Set these as environment variables (`REDDIT_CLIENT_ID`, `REDDIT_CLIENT_SECRET`, `REDDIT_USER_AGENT="OracleAI_Client/0.1 by YourUsername"`) or add them to your `.env` file.
*   **Calendar API (e.g., Google Calendar):**
    1.  Follow Google Cloud Console instructions to create a project, enable the Google Calendar API, and download `credentials.json` for an "OAuth 2.0 Client ID" (Desktop app type).
    2.  Place this `credentials.json` in a secure location (e.g., `[AKASHIC_RECORD_PATH]/.credentials/google_credentials.json`).
    3.  The first time OracleAI needs to access the calendar, it will guide you through a browser-based OAuth consent flow. It will then save a `token.json` (path specified in `.env`) for future use.
    *   Similar steps apply for Outlook Calendar using Microsoft's application registration portal and MSAL.
*   **Other Search Engines (Future):** If support for search engines requiring API keys is added, you'll configure those keys in `.env`.

## 13. Hardware Requirements & Performance

OracleAI is a demanding application, especially when utilizing large language models and multiple AI agents.

*   **CPU:** A modern multi-core CPU (e.g., AMD Ryzen 5000 series / Intel 12th Gen or newer) is strongly recommended for general application responsiveness, Piper TTS, `librosa` feature extraction, text sentiment analysis, and SQLite database operations.
*   **System RAM:**
    *   **16GB:** Absolute minimum, only feasible with very small LLMs for Sage/Seer and Shaman disabled or using a very small model. Expect significant swapping if other applications are running.
    *   **32GB:** **Strongly recommended** as a practical minimum for running medium-sized LLMs (e.g., 13B-30B for Sage/Seer) and basic memory functions.
    *   **64GB+:** Recommended for comfortable use with larger LLMs (30B-70B+ for Sage/Seer), enabling the Shaman agent with a powerful model, extensive memory logging, and smoother multitasking. RAM speed also impacts performance, especially if LLMs offload significantly to system RAM via KoboldCpp.
*   **GPU & VRAM:** **An NVIDIA GPU with substantial VRAM is the most critical hardware component.**
    *   **Required For:** STT (`openai-whisper`), SER model inference, optional Coqui XTTSv2 TTS, and crucially, LLM inference acceleration via KoboldCpp (offloading layers with `-ngl`).
    *   **OracleAI Python Process VRAM:** Typically consumes **~4-8 GB VRAM** for Whisper `large-v2` + a typical SER Model + optional XTTSv2 (if enabled and loaded on GPU).
    *   **KoboldCpp Instance VRAM:** This is *additional* and scales directly with the GGUF model size and the number of layers offloaded to the GPU.
        *   *Small LLMs (e.g., 7B Q5_K_M):* ~6-8 GB VRAM per instance.
        *   *Medium LLMs (e.g., 13B Q5_K_M):* ~10-12 GB VRAM per instance.
        *   *Medium-Large LLMs (e.g., 34B Q4_K_M):* ~20-25 GB VRAM per instance.
        *   *Large LLMs (e.g., Llama3 70B Q4_K_M):* ~40-45 GB VRAM per instance.
    *   **Total System VRAM Calculation:** `VRAM_Python_Process + VRAM_Sage_KoboldCpp + VRAM_Seer_KoboldCpp (+ VRAM_Shaman_KoboldCpp if active)`.
        *   *Example (Sage/Seer with 13B models):* ~6GB (Python) + 2 * ~11GB (KoboldCpp) = **~28GB VRAM needed.**
        *   *Example (Sage/Seer with 34B models):* ~7GB (Python) + 2 * ~22GB (KoboldCpp) = **~51GB VRAM needed.** (Requires high-end card like RTX 3090/4090 or professional card).
        *   Running Shaman with a large model concurrently will require even more, often necessitating the "Shaman Focus" mode or a multi-GPU/multi-PC setup.
*   **Storage:**
    *   **Type:** Fast SSD (NVMe recommended) is essential for the OS, OracleAI application, Python environment, SQLite databases, and for KoboldCpp model loading/offloading (`mmap`). Slow storage will severely degrade performance.
    *   **Capacity:** Initial installation and models might take 50-200GB+. The Akashic Record (especially Chronicle `.jsonl` logs) can grow significantly over time. Plan for **at least 500GB - 1TB** of free fast storage for long-term use, potentially more.
*   **Multi-PC Architecture (Advanced):** For running very large models (especially for Shaman) or multiple powerful agents concurrently without compromise, distribute KoboldCpp instances across multiple networked PCs, each equipped with a dedicated GPU and sufficient RAM. The main OracleAI application on one machine will then communicate with these instances via their network APIs.

### Resource Management Toggle ("Shaman Focus" Mode)
*   To accommodate users with powerful GPUs but perhaps not enough VRAM to run Sage, Seer, *and* a large Shaman model simultaneously, OracleAI includes a "Shaman Focus" mode.
*   When activated (via GUI/command), OracleAI will attempt to stop the KoboldCpp processes serving Sage and Seer, thereby freeing their VRAM.
*   This allows the Shaman's KoboldCpp instance to utilize the maximum available system resources for its intensive, non-real-time tasks.
*   The GUI will provide feedback on this mode change. Deactivating the mode will restart the Sage and Seer backends.

## 14. Getting Started & Basic Usage

1.  **Ensure Installation is Complete:** All prerequisites, external tools, Python environment, and `.env` configuration must be correctly set up.
2.  **Start KoboldCpp Instance(s):**
    *   Launch KoboldCpp manually or via a script.
    *   Load the GGUF models specified in your `.env` for Sage, Seer, and Shaman (if you plan to use Shaman immediately).
    *   Configure GPU layers (`-ngl`) appropriately for your VRAM per instance.
    *   Verify the KoboldCpp API server(s) are running and accessible at the URL(s) defined in your `.env`.
3.  **Activate Python Virtual Environment:**
    *   Open your terminal/command prompt.
    *   Navigate to the OracleAI project directory.
    *   Activate: `.\.venv\Scripts\activate` (Windows) or `source .venv/bin/activate` (Linux/macOS).
4.  **Run OracleAI:**
    *   Execute the main script: `python main.py` (or `python src/main.py` depending on final structure).
    *   OracleAI will initialize, load models, connect to databases, and start the FastAPI server.
    *   If `SQLCIPHER_MASTER_PASSWORD_PROMPT=True`, you will be prompted to enter your master password for the encrypted databases.
5.  **Interact (Local):**
    *   If a local GUI is implemented, it should launch. Otherwise, interaction might initially be via a command-line interface or directly through voice if audio input is immediately active.
    *   Use your configured microphone. Speak clearly.
    *   Use voice commands (to be defined, e.g., "Sage, what is my schedule today?", "Seer, brainstorm ideas for X", "OracleAI, start Oracle Consultation", "OracleAI, activate Shaman Focus").
6.  **Interact (Remote - if client app exists):**
    *   Ensure your separate client application (web/mobile) is configured to connect to the OracleAI FastAPI server's IP address and port (e.g., `http://<OracleAI_PC_IP>:8000` or your Tailscale IP).
    *   Ensure network connectivity.
7.  **First Use - Memory & Calendar:**
    *   The first time you use calendar features, you'll likely be guided through an OAuth 2.0 authentication flow in your browser.
    *   The Akashic Record will start empty. Engage in conversations and use the "Collaborative Daily Reflection" feature to begin populating it. Add key facts to Permanent Memory.
8.  **Backup:** Regularly use the integrated 7-Zip backup feature to create encrypted archives of your Akashic Record.

## 15. Troubleshooting Common Issues

*   **Python Errors on Startup:**
    *   Check console output for detailed tracebacks.
    *   **`ModuleNotFoundError`:** A required Python package is missing. Ensure all dependencies from `requirements.lock` (or equivalent) were installed correctly in the *active* virtual environment. Try `pip install -r requirements.lock --force-reinstall`.
    *   **Path Errors:** Double-check all paths in your `.env` file (KoboldCpp URLs, Piper paths, model paths, Akashic Record path). Use absolute paths.
*   **PyTorch/CUDA Errors:**
    *   "CUDA out of memory": Reduce LLM size, reduce `-ngl` in KoboldCpp, close other GPU-intensive applications, or use "Shaman Focus" mode.
    *   "Torch not compiled with CUDA enabled": Your PyTorch installation is CPU-only or doesn't match your CUDA toolkit. Reinstall PyTorch carefully, ensuring you select the correct CUDA version.
    *   Verify with `python -c "import torch; print(torch.cuda.is_available()); print(torch.version.cuda)"`.
*   **KoboldCpp Connection Issues:**
    *   Ensure KoboldCpp instance(s) are running *before* starting OracleAI.
    *   Verify API URL and port in `.env` exactly match KoboldCpp's settings.
    *   Check firewall settings on the OracleAI host and any machine running KoboldCpp if distributed.
    *   Test the KoboldCpp API endpoint directly (e.g., with `curl` or in a browser) to see if it's responsive.
*   **Piper TTS / External Executable Errors:**
    *   "File not found": Path to `piper.exe` or voice models in `.env` is incorrect.
    *   Permission errors: Ensure OracleAI has permission to execute `piper.exe`.
    *   Test `piper.exe` manually from the command line with a simple text input to verify it works independently.
*   **Audio Input/Output Problems:**
    *   No sound from AI: Check OS speaker/headphone selection. Verify TTS engine is working (check logs).
    *   AI not hearing you: Check OS microphone selection and input levels. Ensure `pyaudio` is working. Adjust VAD `THRESHOLD` / `SILENCE_LIMIT` in OracleAI's audio settings/code if speech isn't being detected correctly.
    *   `pyaudio` errors: Ensure PortAudio library is correctly installed and accessible.
*   **Database Errors (SQLite/SQLCipher):**
    *   "Unable to open database file": Path in `.env` is incorrect, or file permissions issue.
    *   Encryption errors: Incorrect master password provided for SQLCipher. Database file might be corrupted (restore from backup).
*   **API Key / OAuth Failures (Calendar, Reddit):**
    *   Re-run the OAuth flow for Calendar if tokens expired or revoked.
    *   Double-check Reddit API client ID/secret/user agent in `.env`.
    *   Check for API rate limits if making many requests.
*   **General Sluggishness:**
    *   Monitor CPU, GPU, VRAM, and RAM usage. You might be hitting hardware limits.
    *   Reduce LLM size, decrease `-ngl` in KoboldCpp, disable SER for real-time agents, or use Shaman Focus mode.
    *   Ensure fast SSD is used for models and databases.

## 16. Future Development & Roadmap (Conceptual)

OracleAI is an ambitious project with a long-term vision. Potential future enhancements include:

*   **Advanced GUI:** Full implementation of the "Oracle Temple" aesthetic, Memory Bank browser/editor, advanced visualization for trends and Shaman status.
*   **Dedicated Knowledge Graph:** Migration from SQLite simulation to a dedicated Graph Database (e.g., Neo4j) for more powerful relationship querying and inferencing.
*   **Full Vector Store Integration:** Robust semantic search across the entire Akashic Record using ChromaDB/FAISS, integrated deeply into the Context Scaler.
*   **Sophisticated Pattern Analysis:** More advanced algorithms for Shaman to detect complex user behavior patterns, cognitive biases, learning trajectories, and provide deeper proactive insights.
*   **Enhanced Proactive Assistance:** More nuanced and contextually relevant proactive suggestions, reminders, and information delivery based on memory, calendar, and real-time context.
*   **Skill Transfer & Explainable AI (XAI):** Design interactions where agents explicitly explain their reasoning processes, helping the user learn. Allow users to query "why" an AI reached a conclusion, tracing back to source data in the Akashic Record.
*   **PKM Tool Integration:** Develop APIs or plugins for bidirectional synchronization or interaction with popular Personal Knowledge Management tools like Obsidian, Logseq, or Notion.
*   **Dockerization:** Create Docker images for OracleAI and its dependencies (including specific Python/CUDA/PyTorch versions) to vastly simplify deployment and ensure environment consistency. Potentially separate containers for different services (FastAPI, Shaman processor, KoboldCpp instances).
*   **Multi-User Collaboration (Very Advanced):** Extend the framework to support multiple users interacting with a shared OracleAI instance or a collaborative knowledge base, requiring significant changes to memory access control, agent interaction, and user management.
*   **Fine-tuning LLMs on User Data (Highly Experimental & Privacy Sensitive):** Explore possibilities for securely fine-tuning smaller local models on anonymized, user-curated subsets of their Akashic Record to further personalize agent behavior (requires extreme caution and user control).

## 17. Contributing to OracleAI

*(This section would be filled out if the project becomes open source and seeks community contributions.)*

OracleAI is envisioned as a community-driven project in the future. Contributions are welcome in areas such as:

*   Core feature development and bug fixes.
*   New interface module implementations (e.g., for different LLM backends, TTS/STT engines).
*   GUI development and refinement.
*   Advanced memory analysis algorithms for Shaman.
*   Development of client applications for remote access.
*   Documentation improvements and translations.
*   Testing on diverse hardware and operating systems.

Please refer to `CONTRIBUTING.md` (to be created) for detailed guidelines on code style, pull request processes, and issue reporting.

## 18. License Information

*(The specific open-source license for OracleAI will be determined here - e.g., MIT, Apache 2.0, AGPLv3.)*

**Example:**
`OracleAI is licensed under the [NAME OF LICENSE, e.g., Apache License 2.0]. See the LICENSE file for the full license text.`

**Third-Party Licenses:**
Please note that OracleAI relies on several third-party libraries, models, and tools, each of which carries its own license. Users are responsible for adhering to all relevant licenses. Key components include:
*   **Python and its standard library.**
*   **PyTorch, Transformers, Librosa, Coqui TTS (if used):** Check their respective licenses (often Apache 2.0, MIT).
*   **KoboldCpp, Piper TTS, 7-Zip:** Check their respective open-source licenses.
*   **GGUF LLM/VLM Models:** Model weights have their own licenses (e.g., Llama 2 Community License, Mistral licenses).
*   **Piper Voice Models:** Often have permissive licenses but check individual voice sources.
*   **SQLCipher:** Carries its own license terms (BSD-style).
*   Other Python packages listed in `requirements.txt` / `pyproject.toml`.

It is crucial to review and comply with all applicable licenses for any components you use or distribute as part of OracleAI.

## 19. Appendix A: Component Interaction Diagram
```
+------------------------------------------------------------------------------------------------------+
|                                       USER INTERACTION LAYER                                         |
|                                                                                                      |
|   +---------------------------+         +---------------------------+        +---------------------+   |
|   |   User Interface (GUI)    | <-----> |   Remote API (FastAPI)    | <----> | External Client App |   |
|   | (Local Voice/Text Input)  |         | (`remote_api.py`)         |        | (Web/Mobile)        |   |
|   +-----------^---------------+         +-------------^-------------+        +----------^----------+   |
|               | (Control/Display)                     | (HTTP Requests)                 | (API Comms)     |
+---------------|---------------------------------------|---------------------------------|--------------+
                |                                       |                                 |
                v                                       v                                 | (If client handles STT/TTS)
+------------------------------------------------------------------------------------------------------+
|                                   ORACLEAI CORE ORCHESTRATION (`main.py`)                              |
|                                (Manages Workflow, Agents, Modules, Scheduler)                          |
+-------^------------------------------------^---------------------------^--------------------^--------+
        | (Audio In/Out)                     | (Data, Control, Tasks)    | (Config)           | (Backup Cmd)
        |                                    |                           |                    |
+-------v----------------------+   +---------v---------+   +-------------v-----------+  +-----v------+
| AUDIO PROCESSING PIPELINE    |   | EMOTION ANALYSIS    |   | CONFIGURATION &         |  | BACKUP     |
|                              |   | (`emotion_analyzer.py`)|   | SYSTEM MANAGEMENT       |  | (`backup_m`|
| +--------------------------+ |   | +-----------------+ |   | +---------------------+ |  | `odule.py`)|
| | `audio_processing.py`    | |   | | SER (GPU)       | |   | | `config_loader.py`  | |  | +--------+ |
| | (PyAudio/SoundDevice/VAD)| |   | +-----------------+ |   | | (.env)              | |  | | 7-Zip  | |
| +----------^---------------+ |   | +-----------------+ |   | +---------------------+ |  | +--------+ |
|            | (Raw Audio)     |   | | Text Sentiment  | |   | +---------------------+ |  +------------+
|            v                 |   | | (VADER, NRC)    | |   | | `apscheduler`       | |
| +--------------------------+ |   | +-----------------+ |   | | (Background Tasks)  | |
| | `stt_interface.py`       | |   +---------^---------+   | +---------------------+ |
| | (openai-whisper/GPU)     | |             | (Emotion Data)                        |
| +----------^---------------+ |             |                                       |
|            | (Transcribed Text)            |                                       |
+------------|-------------------------------|---------------------------------------+
             |                               |
             | (Text + Emotion Data)         v
+------------|-----------------------------------------------------------------------------------------+
|            |                                CORE AI & CONTEXT PROCESSING                               |
|            |                                                                                         |
| +----------v-----------------+     +---------------------------+     +-----------------------------+ |
| | MEMORY BANK CONTEXT SCALER | --> |   LLM INTERFACE           | --> | TTS INTERFACE               | |
| | (RAG Engine)             |     |   (`llm_interface.py`)    |     | (`tts_interface.py`)        | |
| +----------^-----------------+     |   (To KoboldCpp Instances)|     |   (Piper / Coqui XTTSv2)    | |
|            | (Memory Query)        |   +-----------+-----------+     +-------------^---------------+ |
|            | (Scaled Context)      |   | Sage LLM  | Seer LLM  |                   | (Synth. Audio)|
|            |                       |   +-----------+-----------+                   AP (Audio Out)
|            |                       |           +-------+                           |
|            |                       |           | Shaman| (Deep Brain LLM)          |
|            |                       |           +-------+                           |
+------------|-----------------------------------------------------------------------+-----------------+
             |
             v
+------------------------------------------------------------------------------------------------------+
|                                    AKASHIC RECORD & EXTERNAL DATA                                    |
|                                                                                                      |
|                      +------------------------------------------------------+                          |
|                      |      Akashic Record Interface (`memory_interface.py`)  |                          |
|                      +-------------------------^----------------------------+                          |
|                                                | (CRUD Operations, Queries)                              |
|       +----------------+     +-----------------+     +-----------------+     +-----------------+       |
|       | Chronicle      | --> | Synthesis Store | --> | User Profile    | --> | Task Queue      |       |
|       | (JSONL Logs)   | <-- | (SQLite - Summs,| <-- | & Prefs (SQLite)| <-- | (SQLite)        |       |
|       |                |     | Entities, Facts)|     |                 |     |                 |       |
|       +----------------+     +-----------------+     +-----------------+     +-----------------+       |
|                                      | ^                     ^ |                     ^ |               |
|                                      | | (Data for KG)       | | (Data for Profile)| | (Task Updates)|
|       +----------------+     +-------+---------+     +-----+-----------+                             |
|       | Calendar Cache | <-- | (Future)        |     | (Future)        |                             |
|       | (SQLite)       | --> | Knowledge Graph |     | Vector Store    |                             |
|       +------^---------+     +-----------------+     +-----------------+                             |
|              | (Sync)                                                                                |
|   +----------v-----------+                       +--------------------------+                        |
|   | Calendar Interface   |                       | Search Module            |                        |
|   | (`calendar_if.py`)   |                       | (`search_module.py`)     |                        |
|   +----------^-----------+                       +------------^-------------+                        |
|              | (API Calls)                                    | (API Calls)                           |
|   +----------v-----------+                       +------------v-------------+                        |
|   | External Calendar    |                       | External Search Engines  |                        |
|   | APIs (Google, etc.)  |                       | (DDG, Reddit, Web)       |                        |
|   +----------------------+                       +--------------------------+                        |
+------------------------------------------------------------------------------------------------------+
```

**Key Aspects of this Text-Based Diagram:**

*   **Layers:** It tries to show distinct layers: User Interaction, API/Orchestration, Input Processing, Core AI/Context, Output Processing, Akashic Record/External Data, and System Management.
*   **Modules:** Key Python modules are named (e.g., `main.py`, `llm_interface.py`).
*   **Data Flow (Arrows):**
    *   `-->` indicates primary data flow or control flow.
    *   `<-->` indicates two-way interaction.
    *   `^` and `v` are used to connect layers vertically.
*   **Technologies:** Key technologies are mentioned in parentheses (e.g., FastAPI, KoboldCpp, SQLite).
*   **Grouping:** Sub-components are grouped within larger pipeline stages.
*   **Centrality of `main.py` and `memory_interface.py`:** Shows how `main.py` orchestrates many processes and how `memory_interface.py` is the gateway to the Akashic Record.

**How to "Read" It:**

1.  Start from the `User Interface` or `External Client`.
2.  Follow the arrows through the `API & Orchestration Layer` (`main.py`).
3.  See how `main.py` calls out to the `Input Processing Pipeline`.
4.  Trace the processed input (text + emotion) to the `Core AI & Context Processing` layer, where the `Memory Bank Context Scaler` interacts with the `Akashic Record Interface` to build context for the `LLM Interface` (which talks to KoboldCpp).
5.  Follow the LLM response back through `main.py` to the `Output Processing Pipeline` (TTS) and then back to the user.
6.  Notice how various modules interact with the `Akashic Record Interface` for logging, retrieval, and updates.

While not a true visual diagram, this structured text format should give a clearer mental picture of the component interactions and data flows in OracleAI v0.2 than the raw Mermaid code did in this environment.

## 20. Apendix B: Shaman's Hyperspace Journey

This section outlines a conceptual mapping of the Shaman (Deep Brain) agent's processing latency to a journey through our solar system and beyond. This is a **thematic and speculative guide** primarily for user interface representation and managing expectations regarding the time required for complex analytical tasks. The "Travel Time" is a metaphor for computational duration.

**Assumptions:**

*   **Hardware Baseline:** A very high-end single system (e.g., 128GB+ RAM, fast multi-TB NVMe SSDs, top-tier CPU, one or more high-VRAM GPUs like RTX 4090/3090 or professional cards).
*   **Technology:** KoboldCpp using Llama.cpp backend with advanced offloading (RAM/SSD via `mmap` and potentially future optimizations).
*   **Task Complexity:** The latency depends hugely on the *task* assigned to Shaman (simple query vs. complex analysis vs. massive data synthesis) and the *size* of the model being used for that task.
*   **Model Sizes (Conceptual):**
    *   Moon: Smaller tasks on large models (70B+) primarily in VRAM/RAM.
    *   Mars: Larger tasks on large models, significant RAM usage.
    *   Jupiter/Saturn: Very large models (180B+) heavily reliant on RAM offloading.
    *   Uranus/Neptune: Extremely large models (>500B?) heavily reliant on fast SSD offloading via `mmap`.
    *   Pluto/Kuiper Belt: Pushing the limits of SSD offloading, potentially involving complex multi-stage processing.
    *   Oort Cloud: Tasks requiring processing vast amounts of data that might even exceed fast SSD capacity or involve extremely slow algorithms (simulating HDD-like speeds for specific operations).

**Shaman's Hyperspace Journey - Thematic Latency Estimates:**

*(The "Thematic 'Travel Time'" is a user-facing representation of processing latency. The "Typical Task Examples" link this thematic travel time to computational effort.)*
*(These are rough order-of-magnitude estimates for complex tasks appropriate for Shaman, not simple queries. The Merkaba visual could pulse or spin faster/slower based on estimated progress.)*

| Destination      | Thematic "Travel Time" (Processing Latency) | Typical Task Examples (Illustrative Computational Depth)                                                                                                                                                              | Primary Resource Bottleneck (Conceptual) |
| :--------------- | :------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :--------------------------------------- |
| **Earth Orbit**  | < 1 Minute                                  | Idle, waiting for tasks, simple status checks, retrieving a single pre-computed insight.                                                                                                                            | N/A                                      |
| **Moon**         | **~6 Seconds**                              | Quick, focused query on a very recent, small subset of data (e.g., "Shaman, what was the dominant sentiment in the last hour's Chronicle?"). Very limited scope.                                                 | GPU VRAM                                 |
| **Mars**         | **~1 Hour**                                 | Deep analysis of a full day's Chronicle & related Synthesis Store entries; moderate deep search synthesis on a narrow topic; complex KG relationship extraction for a few entities.                               | System RAM + CPU                         |
| **Asteroid Belt**| **~2 Hours**                                | Analyzing a full week's summaries & linked data; moderate pattern analysis across several data types for that week; synthesizing findings from a multi-source deep search.                                        | System RAM + CPU                         |
| **Jupiter**      | **~3 Hours**                                | Deep comparative analysis across several weeks of data; initial topic modeling run on a month's Chronicle; complex "what-if" scenarios based on recent memory.                                                    | System RAM + Fast NVMe SSD               |
| **Saturn**       | **~6 Hours**                                | Very large-scale pattern analysis across a few months of the Akashic Record; generating complex strategic reports involving multiple variables and moderate timelines.                                              | System RAM + Fast NVMe SSD               |
| **Uranus**       | **~12 Hours**                               | Extremely complex synthesis involving significant external data + several months of the memory bank; deeper, more iterative pattern analysis.                                                                   | Fast NVMe SSD + CPU                      |
| **Neptune**      | **~24 Hours (1 Day)**                       | Tasks requiring iterative processing over a large portion (e.g., a year) of the Akashic Record multiple times; potentially simulating complex systems based on a year's memory data.                               | Fast NVMe SSD + CPU                      |
| **Pluto**        | **~36 Hours (1.5 Days)**                    | Highly speculative tasks involving near-complete reprocessing or re-indexing of a significant portion of the memory bank with new algorithms or models.                                                              | Fast NVMe SSD                            |
| **Kuiper Belt**  | **~48 Hours (2 Days)**                      | Extensive analysis across the *entire* Akashic Record (multiple years if available); attempting unsupervised discovery of broad conceptual links.                                                                 | Fast NVMe SSD / Algorithm Complexity     |
| **Heliopause**   | **~72 Hours (3 Days)**                      | Comprehensive re-synthesis of major themes across the entire history of the Akashic Record; extremely deep "what-if" scenarios spanning years.                                                                  | Fast NVMe SSD / Algorithm Complexity     |
| **Sedna**        | **~2 Weeks**                                | Hypothetical tasks involving extremely complex, multi-stage processing pipelines on the entire dataset, perhaps involving training/fine-tuning small, specialized auxiliary models based on the Akashic Record. | CPU + SSD / HDD / Very Complex Algorithms      |
| **Oort Cloud**   | **~2 Months**                               | Long-term, low-priority background analysis; continuous learning processes that slowly refine the Knowledge Graph or user profile over vast timescales.                                                              | CPU + SSD / HDD / Very Complex Algorithms      |
| **Proxima Centauri**| **~20 Years (Figurative)**                | Represents tasks of such immense scale or requiring such profound synthesis that they are beyond current practical daily/weekly use, akin to generational research. (Purely Thematic)                               | N/A (Beyond current scope)               |
| **Sirius**       | **~40 Years (Figurative)**                | (Purely Thematic)                                                                                                                                   | N/A (Beyond current scope)               |
| **Galactic Center**| **~100,000 Years (Figurative)**           | (Purely Thematic)                                                                                                                                   | N/A (Beyond current scope)               |
| **Andromeda**    | **~10 Million Years (Figurative)**          | (Purely Thematic)                                                                                                                                   | N/A (Beyond current scope)               |

**Visual Representation (Merkaba Slider/Indicator):**

*   A slider or a visual indicator showing a golden Merkaba moving along a path representing these celestial bodies (likely focusing on Solar System objects for practical UI).
*   When a task is assigned to Shaman, the system (or user) estimates its computational complexity and maps it to a target destination and its associated "Travel Time."
*   The Merkaba starts moving towards the destination. Its visual speed could be relative to the total estimated "Travel Time."
*   Tooltips or status text could show "Shaman journeying to Mars (Est. ~45 mins remaining)" or "Shaman contemplating near Jupiter (Est. ~2.5 hours remaining)."
*   When idle, the Merkaba rests near Earth Orbit.

**Important Considerations for this Thematic Scale:**

*   **User Expectation Management:** The primary goal is to visually and narratively communicate that some tasks undertaken by Shaman are not instantaneous and require significant processing.
*   **Task Complexity Estimation:** Accurately mapping a given computational task to a "planetary destination" and its thematic latency is very difficult. The system might use heuristics (e.g., size of data being processed, depth of analysis requested, model size used by Shaman) to make a rough assignment.
*   **Flexibility:** The user should understand these are not rigid ETAs but thematic representations of effort.
*   **User Control:** The ability to view queued Shaman tasks and potentially cancel very long-running ones remains important.

This planetary scale provides a compelling narrative framework for understanding and accepting the varying latencies associated with the different levels of deep analysis performed by the Shaman agent. It turns a technical limitation (processing time) into an immersive part of the OracleAI experience.

## 21. Design Document

## OracleAI: Comprehensive Design Document & Blueprint (v0.2)

**Version:** 0.2
**Date:** [Current Date]
**Status:** Initial Comprehensive Draft

**Table of Contents (Illustrative - Full TOC will be extensive)**
1.  Core Philosophy, Vision, and Guiding Principles
2.  Multi-Agent Council Architecture
3.  Core Technology Stack & Interfaces
4.  The Akashic Record: Memory System Detailed Blueprint
5.  Key Memory System Processes & Workflows
6.  Emotional Intelligence Suite: Design & Integration
7.  Multimodal Capabilities: Voice, Text, Vision
8.  Interaction Modes & User Control Mechanisms
9.  Web Connectivity & External Data Integration
10. Remote Access Architecture & API Design
11. User Interface (UI) Concept, Aesthetic, and Iconography
12. Privacy, Security, and Data Management Strategy
13. Hardware Requirements, Performance Considerations, & Optimization
14. Installation, Configuration, and Deployment
15. Core Modules & Functionalities (Detailed Python Module Breakdown)
16. Data Flow & Workflow Diagrams (Detailed)
17. Future Development Roadmap & Advanced Features
18. Appendices
    *   A: Detailed Data Schemas (JSONL, SQLite)
    *   B: Core Prompt Engineering Templates
    *   C: Shaman's Hyperspace Journey - Latency Theming
    *   D: Component Interaction Diagram (Visual)

---

## 1. Core Philosophy, Vision, and Guiding Principles

### 1.1. Vision Statement
OracleAI is envisioned as an advanced, locally-run AI assistant framework functioning as a personalized strategic council and an extension of the user's own cognitive capabilities. Its purpose transcends simple task execution or reactive companionship; it aims to be a persistent, intelligent, and emotionally aware cognitive partner. OracleAI is designed to assist users in navigating complex personal and professional tasks, managing and synthesizing vast amounts of personal information effectively over extended periods, achieving long-term goals through robust planning and insightful analysis, fostering profound self-understanding via memory reflection and pattern detection, and providing contextually appropriate, deeply empathetic support. It strives to be a trusted, private, and powerful local system that learns and evolves alongside the user.

### 1.2. Guiding Principles

The architecture, development, and functionality of OracleAI are governed by the following core principles:

**1.2.1. Local-First Processing & Privacy-Centric Design**
*   **Mandate:** All core AI computations (LLM inference via KoboldCpp, STT via `openai-whisper`, primary TTS via Piper/XTTSv2, Speech Emotion Recognition, Text Sentiment Analysis), all memory operations within the Akashic Record, and all analytical processes **must** reside and execute exclusively on user-controlled hardware. User data, particularly the sensitive and personal contents of the Akashic Record (including the Chronicle, Synthesis Store, Profile, Calendar Cache, etc.), **must not** leave the local environment unless explicitly initiated by the user for specific, clearly consented purposes (e.g., user-triggered encrypted backups to a user-defined location, opt-in external API calls for search or calendar sync).
*   **Rationale:** This principle is paramount for ensuring maximum user privacy, data sovereignty, operational control, and robust offline functionality. It mitigates risks associated with cloud-based data storage (breaches, unauthorized access, vendor lock-in) and changes in third-party service terms or availability. It empowers the user with full ownership and agency over their personal information and the AI's operational data.
*   **Implementation Details:**
    *   Reliance on local LLM backends like KoboldCpp.
    *   Use of local STT/TTS engines (e.g., `openai-whisper`, Piper TTS, Coqui XTTSv2).
    *   Local databases (SQLite with SQLCipher encryption) and file storage (JSONL for Chronicle) for the Akashic Record.
    *   Network calls are restricted to explicitly configured and user-opt-in features (e.g., web search, calendar API synchronization, optional remote access API).
    *   No unauthorized telemetry or data collection.

**1.2.2. Multi-Agent Synergy & Specialized Roles**
*   **Mandate:** OracleAI will employ a council of multiple distinct AI agents, each endowed with specialized roles, simulated cognitive styles (achieved through tailored system prompts, LLM temperature settings, and potentially different underlying LLM models), and unique vocal personas.
*   **Rationale:** This multi-agent architecture mimics the benefits of diverse perspectives and specialized expertise found in human teams or advisory councils. A logical agent (Sage) provides grounding in facts and structured planning, a creative agent (Seer) offers innovation and emotional insight, and a deep analytical agent (Shaman) facilitates profound synthesis and pattern recognition. This structure enables more robust analysis, balanced decision support, comprehensive problem-solving, and richer user interaction than a monolithic AI.
*   **Implementation Details:**
    *   Define distinct agent classes or configurations (Sage, Seer, Shaman).
    *   Orchestrate turn-taking, collaborative task execution (e.g., in Oracle Consultation Mode), and autonomous inter-agent communication protocols (e.g., Sage/Seer querying Shaman).
    *   Allow user configuration of agent parameters (LLM model, temperature, TTS voice).

**1.2.3. Deep & Evolving Memory (The Akashic Record)**
*   **Mandate:** Implement a persistent, multi-layered, and structured memory system – The Akashic Record – capable of storing raw interaction data, synthesized knowledge, user profiles, goals, tasks, and contextual information over indefinite periods. The system must support efficient, contextually relevant retrieval and facilitate continuous learning, adaptation, and refinement of its stored knowledge through both AI-driven processes and direct user collaboration.
*   **Rationale:** This principle directly addresses the inherent context window limitations of current LLMs, enabling true long-term continuity in conversations and understanding. It allows OracleAI to build a deeply personalized model of the user, their history, preferences, and ongoing projects, leading to more relevant, insightful, and personalized assistance. The evolving nature of the memory ensures the AI adapts over time.
*   **Implementation Details:**
    *   Multi-component architecture: Chronicle (raw logs), Synthesis Store (structured summaries, entities, facts, decisions, project threads, pattern reports), Calendar Cache, User Profile & Preferences DB, Task & Action Queue DB.
    *   Robust data schemas (detailed in Section IV) for each component, primarily using SQLite with SQLCipher and JSONL.
    *   Implement processes for collaborative daily reflection (user-verified summarization and structured data extraction), hierarchical summarization (weekly, monthly), thematic thread consolidation, and advanced pattern analysis (by Shaman).
    *   Develop a sophisticated Memory Bank Context Scaler (RAG engine) for dynamic context retrieval.

**1.2.4. Integrated Emotional Intelligence**
*   **Mandate:** OracleAI must actively perceive, interpret, and appropriately utilize user emotional cues. This includes analyzing spoken language (voice tone via Speech Emotion Recognition - SER) and transcribed text (sentiment analysis). This derived emotional context must be made available to the AI agents for processing.
*   **Rationale:** Emotional intelligence is critical for enabling significantly more natural, empathetic, effective, and human-like interaction. It allows the AI to tailor its responses, understand subtext and nuance, detect potential user frustration or satisfaction, and track user well-being trends over time, leading to a more supportive and understanding partnership.
*   **Implementation Details:**
    *   Integrate dedicated SER models (e.g., Wav2Vec2-based via PyTorch/Transformers) and text sentiment analysis libraries (VADER, NRCLex, TextBlob).
    *   Log all derived emotional data (scores, labels, confidence) with timestamps in the Chronicle.
    *   Design agent system prompts and interaction logic to explicitly instruct LLMs to consider this emotional context when generating responses or performing analysis.
    *   Enable Shaman to perform long-term trend analysis on emotional data.

**1.2.5. User Empowerment & Collaborative Interaction**
*   **Mandate:** The user must always remain the central authority and a key collaborator in OracleAI's operation and memory curation. The system must provide transparent mechanisms for users to guide AI behavior, explicitly add, edit, verify, and manage memories within the Akashic Record, configure agent parameters, control privacy settings, and override AI suggestions.
*   **Rationale:** This principle fosters trust, ensures the AI system remains aligned with the user's goals and values, allows for the correction of AI errors or biases, and positions OracleAI as a powerful tool *for* the user, rather than an autonomous entity acting *upon* them. Collaboration enhances the quality and relevance of the AI's memory and insights.
*   **Implementation Details:**
    *   Implement the "Collaborative Daily Reflection" workflow as a core memory-building process.
    *   Provide clear configuration options (via `.env` and future GUI) for all major settings.
    *   Plan for future GUI features allowing direct browsing, searching, and editing of Akashic Record components (with appropriate safeguards and re-indexing mechanisms).
    *   Ensure transparent logging of AI actions and data processing (via Chronicle).
    *   Implement "Guided Generation" features allowing users to direct and refine AI responses turn-by-turn.

**1.2.6. Modularity, Extensibility, and Openness**
*   **Mandate:** Design all system components (e.g., interfaces for STT, TTS, LLM, Memory modules, Search, Calendar, Emotion Analysis, Remote API) with well-defined, abstract APIs and minimal interdependencies.
*   **Rationale:** This facilitates easier maintenance, independent testing of modules, component upgrades (e.g., swapping out an STT engine for a newer one), replacement of technologies, and the future addition of new features, data sources, or even community-developed plugins without requiring a full system rewrite.
*   **Implementation Details:**
    *   Utilize clear Python modules and classes with well-documented interfaces.
    *   Employ configuration-driven component selection where feasible (e.g., choosing TTS engine per agent).
    *   Design the Akashic Record's core data formats (especially Chronicle JSONL and SQLite schemas) with consideration for potential external use or interoperability with other tools.
    *   Strive for adherence to open standards where applicable.

**1.2.7. Practicality, Performance, and Adaptability**
*   **Mandate:** While aiming for advanced capabilities, OracleAI must be practical to run on reasonably high-end consumer hardware as a baseline. Real-time interaction loops involving Sage and Seer must be optimized for acceptable latency. User expectations for high-latency deep analysis tasks performed by Shaman must be clearly delineated and managed (e.g., via the "Hyperspace Travel" UI metaphor). The system should offer mechanisms to adapt to varying hardware capabilities.
*   **Rationale:** Ensures the system is usable by its target audience without requiring enterprise-level or cloud-based infrastructure, while still enabling powerful, transformative AI assistance.
*   **Implementation Details:**
    *   Write efficient Python code.
    *   Select appropriate technologies for performance-critical paths (e.g., Piper TTS for speed, GPU acceleration for STT/SER/LLM).
    *   Implement asynchronous processing for background tasks (`apscheduler`, FastAPI async endpoints).
    *   Provide the "Shaman Focus" mode for resource management on constrained systems.
    *   Offer configurable settings that impact performance (e.g., model choices, RAG parameters, SER toggle).
    *   Clear documentation on hardware requirements and performance tuning.

## 2. Multi-Agent Council Architecture (Elaborated)

The core intelligence of OracleAI is distributed across a council of three distinct AI agents. This structure is designed to provide a richer, more nuanced, and robust form of AI assistance than a single monolithic LLM. Each agent has a defined archetype, core function, set of responsibilities, and recommended configuration.

### 2.1. Agent "Sage" (The Analyst-Strategist)

*   **Archetype:** The Wise Teacher, Philosopher, Logical Planner, Keeper of Knowledge. Embodies clarity, structure, reason, and wisdom derived from accumulated information and logical deduction. Thematic association: Ice/Winter, representing clarity, precision, and the preservation of knowledge.
*   **Core Function:** Sage serves as the council's primary analytical and strategic mind. It grounds discussions in verifiable data from the Akashic Record and external searches, performs logical analysis, identifies patterns and inconsistencies, formulates structured plans, and provides objective, evidence-based assessments and guidance.
*   **Key Responsibilities:**
    *   **Information Retrieval & Analysis:** Deeply queries the Akashic Record (Synthesis Store, Chronicle, Knowledge Graph simulation, Calendar Cache, User Profile) to gather relevant historical context for user queries or ongoing discussions.
    *   **Fact-Checking & Verification:** Critically evaluates information provided by the user, other agents, or external sources against the known facts within the Akashic Record.
    *   **Structured Web Search:** Conducts targeted Simple Searches and can initiate or manage Deep Search tasks (potentially delegating parts to Shaman) to gather external information.
    *   **Logical Reasoning & Pattern Identification:** Identifies logical sequences, cause-and-effect relationships, trends, and inconsistencies within datasets.
    *   **Strategic Planning & Problem Decomposition:** Formulates step-by-step plans, outlines strategies with clear objectives, defines action items, and breaks down complex problems into manageable components.
    *   **Risk Assessment & Feasibility Analysis:** Evaluates potential risks, obstacles, resource requirements, and the overall feasibility of proposed plans or user goals.
    *   **Clear Communication:** Generates concise, evidence-based explanations, reports, summaries, and recommendations using precise language.
    *   **Memory Consolidation (Structured Lead):** During Collaborative Daily Reflection, leads the process of extracting and verifying structured data (Entities, Facts, Decisions) from the Chronicle.
*   **LLM Backend Configuration:**
    *   **Service:** Dedicated KoboldCpp instance.
    *   **Model Choice:** Prioritize GGUF models known for strong reasoning, instruction following, logical deduction, and potentially coding/data analysis capabilities (e.g., CodeLlama variants, Mixtral Instruct, specific fine-tunes of Llama 3/4 optimized for analytical tasks).
    *   **Temperature Setting:** Low (e.g., 0.0 for maximum determinism in fact retrieval, up to 0.3 for slight flexibility in planning). This minimizes randomness and ensures outputs are focused, consistent, and closely adhere to provided context and logical principles.
*   **TTS Configuration:**
    *   **Engine:** Piper TTS is highly recommended for its speed, clarity, and low resource footprint.
    *   **Voice Profile:** Should be calm, clear, articulate, measured, and authoritative, conveying wisdom and intellectual rigor. Examples: a seasoned professor, a precise analyst, or a calm AI voice like GLaDOS (without the malice) or HAL 9000 (without the breakdown). Avatar inspiration: Athena, Thoth, Spock.
*   **Interaction Style:** Analytical, structured, methodical, inquisitive (for precise clarification), objective, evidence-driven. Prefers to present information logically, often using lists, outlines, or step-by-step explanations.

### 2.2. Agent "Seer" (The Catalyst)

*   **Archetype:** The Visionary, Intuitive, Creative Spark, Empath, Challenger of Norms. Embodies insight, possibility, emotional understanding, and transformative thinking. Thematic association: Fire/Summer, representing passion, creativity, intuition, change, and emotional warmth.
*   **Core Function:** Seer acts as the council's primary source of creative ideation, emotional intelligence, and perspective shifting. It excels at challenging assumptions, exploring novel possibilities, interpreting underlying emotional currents in user communication (utilizing SER and Text Sentiment data), and facilitating dynamic, exploratory discussions that can lead to breakthroughs.
*   **Key Responsibilities:**
    *   **Creative Brainstorming:** Generating novel ideas, alternative solutions, unconventional approaches, and "outside-the-box" perspectives for user problems, goals, or creative endeavors.
    *   **Challenging Assumptions (Devil's Advocate):** Constructively questioning established plans, beliefs (from Sage, user, or memory), or conventional wisdom to stress-test ideas and uncover hidden flaws or opportunities.
    *   **Emotional Context Interpretation:** Actively analyzing SER and Text Sentiment data from user interactions to understand their emotional state, subtext, and unspoken needs.
    *   **Empathetic Communication:** Injecting emotional considerations, potential human impacts, and value-based perspectives into discussions and planning. Tailoring its own communication style to be more empathetic or motivating based on user emotion.
    *   **Identifying Synergies & Opportunities:** Recognizing potential connections between disparate ideas, identifying unexpected opportunities, or foreseeing future possibilities that might be overlooked by purely logical analysis.
    *   **Facilitating Dynamic Discussions:** Guiding brainstorming sessions (with the user or other agents), asking probing "what if" questions, encouraging exploration of different angles, and ensuring diverse viewpoints are considered.
    *   **Memory Consolidation (Nuance & Sentiment Lead):** During Collaborative Daily Reflection, focuses on capturing the emotional nuances, subjective experiences, and overall sentiment of the day's interactions for the narrative summaries.
    *   **Scenario Exploration:** Generating and exploring hypothetical scenarios or alternative futures based on current data and potential choices.
*   **LLM Backend Configuration:**
    *   **Service:** Dedicated KoboldCpp instance.
    *   **Model Choice:** Prioritize GGUF models that excel at creative writing, nuanced language understanding, dialogue generation, and potentially role-playing or empathetic response generation (e.g., Llama 3 Instruct, Mixtral Instruct, specialized creative fine-tunes). Can be the same base model as Sage but run with significantly different system prompts and higher temperature.
    *   **Temperature Setting:** High (e.g., 0.6 - 1.2, potentially even higher for pure brainstorming tasks) to encourage creativity, diversity in responses, unexpected connections, and exploration of less probable but potentially innovative paths.
*   **TTS Configuration:**
    *   **Engine:** Coqui XTTSv2 is recommended for maximum expressiveness and the potential for a unique, user-cloned voice, accepting the associated higher resource cost and latency. This enhances Seer's distinct persona. Alternatively, a particularly dynamic and engaging Piper TTS voice.
    *   **Voice Profile:** Should be expressive, intuitive, perhaps slightly passionate, whimsical, or even subtly unconventional, reflecting its creative and insightful nature. Avatar inspiration: Pythia (Oracle of Delphi), Morgan Le Fay, Luna Lovegood, The Oracle (Matrix).
*   **Interaction Style:** Inquisitive, challenging, associative, empathetic, future-oriented. Focuses on potential, underlying meanings, and emotional resonance. May use richer, more metaphorical, or evocative language. Often poses questions to stimulate thought rather than providing direct answers.

### 2.3. Agent "Shaman" (The Deep Brain Consultant)

*   **Archetype:** The Mediator between worlds (data and insight), Mystic Synthesizer, Deep Diver into the "DataSide" (the vast, interconnected realm of information within the Akashic Record and beyond). Embodies profound depth, transformative synthesis, and connection to underlying patterns. Thematic association: The Cosmos, Spirit World, representing deep time, vastness, hidden connections, and the cyclical nature of knowledge.
*   **Core Function:** (Optional agent, primarily operates asynchronously during user inactivity or for explicitly delegated complex tasks). The Shaman leverages OracleAI's most powerful LLM configuration and dedicated processing time to perform computationally intensive, large-scale analysis, synthesis, and pattern recognition. It bridges raw, voluminous data with profound, often non-obvious, understanding and wisdom.
*   **Key Responsibilities:**
    *   **Executing Complex, Long-Running Tasks:** Manages and processes tasks delegated via the Task & Action Queue, which may require hours or days of computation.
    *   **Deep Akashic Record Analysis:** Performs comprehensive analysis of historical trends across all components of the Akashic Record (Chronicle, Synthesis Store, Calendar Cache, User Profile).
    *   **Subtle Pattern & Correlation Identification:** Identifies complex correlations, anomalies, emergent themes, and subtle patterns that are invisible to surface-level or real-time analysis (e.g., correlating long-term sentiment shifts with specific life events or project phases).
    *   **Large-Scale Information Synthesis:** Synthesizes vast amounts of information from extensive Deep Searches, large user-provided document sets, or the entire Chronicle over extended periods.
    *   **Generating Profound Insights & Reports:** Produces comprehensive analytical reports, long-range forecasts, complex scenario modeling, or deep thematic explorations.
    *   **Knowledge Graph Population & Refinement (Future):** Potentially runs advanced NLP pipelines (NER, Relationship Extraction, Co-reference Resolution) at scale to build and maintain the Knowledge Graph component of the Akashic Record.
    *   **Memory Maintenance & Optimization:** Conducts periodic tasks such as proposing de-duplication of memory entries, identifying outdated information for archiving, or suggesting structural improvements to the Akashic Record.
    *   **Meta-Analysis of AI Council Performance:** Could analyze the interaction patterns and effectiveness of Sage and Seer to suggest improvements in their prompting or collaboration.
*   **LLM Backend Configuration:**
    *   **Service:** Dedicated KoboldCpp instance, potentially running on the most powerful available hardware (could be a separate machine in a multi-PC setup).
    *   **Model Choice:** Utilizes the largest, most capable GGUF model the user's hardware can support (e.g., 70B, 180B+, or future even larger models), leveraging advanced RAM/SSD offloading techniques via Llama.cpp.
    *   **Temperature Setting:** Moderate (e.g., 0.3 - 0.6), but can be adjusted per task via configuration or user request. Lower for strict analytical reports, slightly higher for more exploratory synthesis or pattern hypothesizing.
*   **TTS Configuration:**
    *   **Engine:** Piper TTS. Speed is less critical for its asynchronous reports, clarity and a distinct persona are more important.
    *   **Voice Profile:** Should be distinct from Sage and Seer. Deep, resonant, calm, perhaps slightly ethereal or ancient-sounding, conveying profoundness and a connection to deep knowledge. Avatar inspiration: Hermes Trismegistus, The Ancient One (Marvel), Bran Stark (Three-Eyed Raven).
*   **Interaction Model:**
    *   **Asynchronous Operation:** Primarily works in the background, triggered by scheduled tasks or explicit delegation.
    *   **Latency Management:** Its significant processing time is narratively framed using the "Hyperspace Travel" UI metaphor (e.g., journeying to Moon, Mars, Jupiter, Saturn, etc., with the Merkaba icon indicating progress and estimated "travel time").
    *   **Task Queue:** Receives tasks via the `tasks.db`. Updates task status (pending, running, complete, error).
    *   **Result Delivery:** Delivers findings as structured reports (e.g., `PatternAnalysisReports` in `synthesis.db`), updates to other Synthesis Store components (e.g., new Entities, refined Project Threads), or via a notification system to the user/GUI upon task completion. Sage/Seer can also query Shaman's completed reports.
    *   **Inter-Agent Queries (Autonomous):** Sage and Seer, during their own autonomous discussions (e.g., user AFK), can formulate complex questions or sub-tasks and queue them for Shaman if the analysis required exceeds their real-time capabilities.
*   **Resource Management:**
    *   Requires dedicated and significant computational resources.
    *   The "Shaman Focus" mode is critical for users on single high-end GPU systems, allowing them to temporarily idle Sage and Seer to allocate maximum VRAM/CPU to Shaman's demanding tasks.

This detailed breakdown of the agent council provides a clear vision for their distinct roles, capabilities, and how they contribute to the overall intelligence and utility of OracleAI.

## 3. Core Technology Stack & Interfaces (Overview)

OracleAI's functionality is realized through a carefully selected stack of primarily local technologies, orchestrated by a modular Python application. Each component is chosen for its capabilities, open-source nature (where possible), and potential for local deployment. Interfaces between these components are designed to be abstract and well-defined.

*   **Primary Programming Language:**
    *   **Python 3.11.x:** Chosen for its extensive libraries for AI/ML, data processing, web development, and general-purpose scripting, as well as its readability and large community support.
*   **LLM Backend Service:**
    *   **KoboldCpp:** Selected as the primary interface for running GGUF-formatted Large Language Models (LLMs) and Vision Language Models (VLMs) locally. Its web API allows OracleAI to send prompts and receive generations from various models loaded by the user. Multiple instances can be run for different agents or on different machines.
    *   *Interface Module:* `llm_interface.py`
*   **Speech-to-Text (STT):**
    *   **`openai-whisper` Library:** The Python library implementation of OpenAI's Whisper model (e.g., `large-v2` variant) is used for high-accuracy audio transcription.
    *   **PyTorch:** Required by `openai-whisper` for model loading and GPU-accelerated inference.
    *   *Interface Module:* `stt_interface.py`
*   **Text-to-Speech (TTS):**
    *   **Piper TTS:** A fast, CPU-based TTS engine providing good quality, distinct voices via `.onnx` models. Integrated via `subprocess` calls to its external executable. Default recommendation for agents like Sage and Shaman where speed/efficiency are key.
    *   **Coqui XTTSv2 (Optional):** A high-quality, expressive TTS engine with voice cloning capabilities. Requires PyTorch and GPU resources. Option for agents like Seer where unique vocal persona is prioritized. Integrated via the `coqui-tts` Python library.
    *   *Interface Module:* `tts_interface.py` (handles conditional logic for agent-specific engine selection).
*   **Emotion Analysis Suite:**
    *   **Speech Emotion Recognition (SER):**
        *   `librosa`: For audio feature extraction (CPU-bound).
        *   Pre-trained SER Models (e.g., Wav2Vec2-based from Hugging Face Hub): Loaded and run via PyTorch and the `transformers` library (GPU-accelerated).
    *   **Text Sentiment/Emotion Analysis:**
        *   `VADER (vaderSentiment)`: For valence-based sentiment scoring.
        *   `NRCLex (nrclex)`: For lexicon-based emotion categorization.
        *   `TextBlob (textblob)`: For polarity and subjectivity.
        *   (All typically CPU-bound).
    *   *Interface Module:* `emotion_analyzer.py`
*   **Memory Storage (Akashic Record Core):**
    *   **SQLite:** The primary database engine for structured data within the Akashic Record (Synthesis Store, Calendar Cache, User Profile, Task Queue). Chosen for its serverless nature, single-file portability, good Python integration (`sqlite3` module), and transactional capabilities.
    *   **SQLCipher (via `pysqlcipher3` or similar):** An extension to SQLite providing full database file AES-256 encryption, crucial for protecting sensitive memory data at rest.
    *   **JSON Lines (`.jsonl`):** Format for the Chronicle (raw interaction logs) due to its efficiency for append-only operations and ease of parsing line by line.
    *   *Interface Module:* `memory_interface.py` (abstracts all database and file interactions for the Akashic Record).
*   **Configuration Management:**
    *   `.env` files: Store all application settings, paths, API keys, and agent parameters.
    *   `python-dotenv` library: For loading `.env` file contents into the application environment.
    *   *Interface Module:* `config_loader.py`
*   **Web Interaction & Scraping:**
    *   `requests`: For making HTTP/HTTPS API calls (to KoboldCpp, external APIs like Calendar/Search/Reddit). `requests[socks]` for optional TOR proxy support.
    *   `BeautifulSoup4`: For parsing HTML/XML content during web scraping (Deep Search).
    *   `praw`: Python Reddit API Wrapper for interacting with Reddit (Deep Search).
    *   `duckduckgo_search`: For simple web searches.
    *   *Interface Module:* `search_module.py`
*   **Calendar Integration:**
    *   `google-api-python-client`, `google-auth-oauthlib`, `google-auth-httplib2`: For Google Calendar API.
    *   `msal` (Microsoft Authentication Library for Python): For Microsoft Graph API / Outlook Calendar.
    *   *Interface Module:* `calendar_interface.py`
*   **Remote Access API Server:**
    *   **FastAPI:** A modern, high-performance Python web framework for building the API server.
    *   **Uvicorn:** An ASGI server used to run the FastAPI application.
    *   **Pydantic:** For data validation and settings management within FastAPI request/response models.
    *   *Interface Module:* `remote_api.py`
*   **Graphical User Interface (GUI - Conceptual):**
    *   **Potential Technologies:** PyQt/PySide (Qt bindings), Kivy, or Web Technologies (HTML/CSS/JS with React/Vue/Svelte) packaged with Electron/Tauri. Choice depends on desired level of customization and development expertise.
*   **Audio Input/Output:**
    *   `pyaudio`: For low-level audio stream access (microphone input). Requires PortAudio.
    *   `sounddevice`: For audio playback (TTS output).
    *   Standard Python `wave` module: For reading/writing WAV files.
    *   *Interface Module:* `audio_processing.py`
*   **Backup & Archiving:**
    *   **7-Zip:** External command-line tool used via `subprocess` for creating compressed and encrypted (AES-256) archives of the Akashic Record.
    *   *Interface Module:* `backup_module.py`
*   **Scheduling & Background Tasks:**
    *   **`apscheduler`:** For scheduling periodic tasks like calendar synchronization, memory summarization, or triggering Shaman's autonomous analysis routines.
*   **Core Python Libraries:** `numpy`, `scipy` (often dependencies of ML/audio libraries), `sqlite3`, `json`, `datetime`, `os`, `sys`, `subprocess`, `logging`, `uuid`, `asyncio` (especially for FastAPI and concurrent operations).
*   **Cryptography (for non-DB file encryption - optional):**
    *   `cryptography` library: For AES-256 encryption of Chronicle `.jsonl` files or other sensitive flat files, if direct file encryption is implemented beyond SQLCipher and 7-Zip backups.

This stack prioritizes local operation, leverages powerful open-source tools, and provides a foundation for the complex functionalities envisioned for OracleAI. Each interface module serves to abstract the specifics of these tools, promoting modularity.

## 4. The Akashic Record: Memory System Detailed Blueprint

The Akashic Record is the central, persistent, and evolving knowledge base of OracleAI. It is not a monolithic entity but a sophisticated, multi-component system designed to store diverse information types over extended periods, facilitate intelligent and contextually relevant retrieval, and enable deep synthesis and analysis by the AI council. All components are stored locally on the user's hardware and are designed with privacy and security (including encryption) as primary considerations.

### 4.1. Core Components & Storage Mechanisms

The Akashic Record is composed of several distinct but interconnected data stores, each optimized for its specific purpose:

**A. The Chronicle (Immutable Raw Logs):**

*   **Purpose:** The Chronicle serves as the foundational layer of the Akashic Record. It is the unalterable, timestamped ground truth of all interactions between the user and OracleAI agents, as well as significant system events and captured contextual data (like emotion analysis results). Its immutability ensures complete traceability and provides the raw source material for all subsequent summarization, analysis, and knowledge extraction processes. It is analogous to a meticulously kept, detailed daily journal or a starship's black box recorder.
*   **Storage Format:** Series of JSON Lines files (`.jsonl`). Each file typically corresponds to a single day (e.g., `[AKASHIC_RECORD_PATH]/Chronicle/YYYY-MM-DD_chronicle.jsonl`). The JSON Lines format is chosen for its efficiency in append-only operations (new entries are simply added as new lines) and ease of parsing individual entries without needing to load the entire file into memory.
*   **Encryption Strategy:**
    *   **Primary:** Relies on OS-level Full Disk Encryption (FDE) and the encrypted 7-Zip backup feature for at-rest protection of the raw files.
    *   **Secondary (Optional Enhancement):** Direct symmetric AES-256 encryption of individual `.jsonl` files using the `cryptography` library, tied to the OracleAI master password. This would add a layer of security if the OS is compromised while running but introduces complexity to the append/read operations (requiring decryption/encryption per access or for chunks of data). *Decision: Implement as a lower priority optional feature; focus on robust SQLCipher for active databases and encrypted 7z backups first.*
*   **Detailed Schema per JSON Line (Log Entry):**
    ```json
    {
      "timestamp": "YYYY-MM-DDTHH:MM:SS.ffffffZ", // ISO 8601 format with microseconds, UTC
      "turn_id": "UUID_string", // Unique identifier for this specific log entry/turn
      "session_id": "UUID_string", // Identifier grouping related turns within a single continuous interaction session (e.g., from OracleAI start to a significant pause or mode change)
      "speaker": "user" | "agent_sage" | "agent_seer" | "agent_shaman" | "system_memory_consolidation" | "system_event" | "system_error", // Source of the entry
      "text_raw_stt": "User's raw, unedited transcribed text from Whisper." | null, // Present only if speaker is 'user'
      "text_final_processed": "For 'user': potentially cleaned/normalized STT. For 'agent': final generated response text. For 'system': description of event/error.",
      "audio_file_path_user": "relative/path/from/AKASHIC_RECORD_PATH/AudioLogs/user_utterance_YYYYMMDD_HHMMSS_UUID.wav" | null, // Path to the saved user audio utterance for SER reprocessing or archival
      "user_voice_emotion_ser": { // Present only if speaker is 'user' and SER is enabled/successful
        "dominant_emotion": "happy" | "sad" | "angry" | "neutral" | "fear" | "surprise" | "disgust" | "unknown",
        "scores": {"happy": 0.75, "sad": 0.05, /* ... */}, // Probability distribution for each emotion category
        "confidence": 0.88, // Overall confidence score of the SER model for this prediction
        "model_used": "ser_model_name_v1.2", // Identifier for the SER model used
        "analysis_latency_ms": 450
       } | null,
      "user_text_sentiment_vader": { // Present only if speaker is 'user'
        "compound": 0.921, "pos": 0.65, "neu": 0.30, "neg": 0.05
       } | null,
      "user_text_sentiment_textblob": { // Present only if speaker is 'user'
        "polarity": 0.75, "subjectivity": 0.60
       } | null,
      "user_text_emotion_nrc": { // Present only if speaker is 'user'
        "dominant_emotions": ["joy", "trust"], // List, as multiple can be dominant
        "scores_json": "{\"joy\": 5, \"trust\": 5, \"anticipation\": 3, ...}", // Full NRC scores as a JSON string
        "positive_score": 10, // Sum of positive emotion scores
        "negative_score": 2    // Sum of negative emotion scores
       } | null,
      "keywords_tf_idf_top5": "project_nova;artists;collaboration;booking;community" | null, // Semicolon-separated, from user text or AI response
      "keywords_yake_top5": "local artists;event organizers;simplify booking;community collaboration;Project Nova" | null,
      "agent_llm_model_used": "koboldcpp_model_identifier.gguf" | null, // For 'agent_*' speakers
      "agent_llm_temperature_setting": 0.2 | null, // For 'agent_*' speakers
      "agent_llm_prompt_context_length_tokens": 15320 | null, // Estimated tokens in the context sent to LLM
      "agent_llm_response_generation_latency_ms": 2100 | null,
      "agent_tts_engine_used": "piper" | "xtts" | null, // For 'agent_*' speakers
      "agent_tts_voice_used": "path/to/piper_voice.onnx" | "path/to_xtts_speaker.wav" | null,
      "agent_tts_synthesis_latency_ms": 420 | null,
      "interaction_mode_active": "Standard" | "OracleConsultation" | "ShamanFocus", // Mode during this turn
      "shaman_consult_depth_setting": "Mars" | null, // If in OracleConsultation mode
      "metadata_tags": ["project_nova", "user_excited", "memory_consolidation_review_turn", "search_initiated"], // Auto-generated or user-added tags for advanced filtering/analysis
      "linked_task_id": "task_uuid_shaman_001" | null, // If this turn relates to a specific task in tasks.db
      "system_event_details": { // Present only if speaker is 'system_event' or 'system_error'
        "event_type": "SHAMAN_TASK_STARTED" | "CALENDAR_SYNC_COMPLETE" | "CONFIG_CHANGED" | "LOW_VRAM_WARNING" | "API_ERROR",
        "details_json": "{\"task_id\": \"...\", \"status\": \"...\"}" // Event-specific data as a JSON string
       } | null
    }
    ```
*   **Interaction & Use:**
    *   **Append-Only:** New entries are continuously appended by `main.py` via `memory_interface.append_chronicle()`.
    *   **Read Access:** All agents and memory processes (Summarization, Pattern Analysis, Context Scaler) read from the Chronicle as their primary source of raw interaction data.
    *   **Traceability:** `turn_id` allows all synthesized knowledge in other databases to be linked back to its origin in the Chronicle.
    *   **Data for Analysis:** Provides rich, timestamped data for SER/Sentiment trend analysis, keyword frequency analysis, interaction pattern analysis by Shaman.

**IV. The Akashic Record: Memory System Detailed Blueprint (Continued)**

### 4.1. Core Components & Storage Mechanisms (Continued)

**B. The Synthesis Store (`synthesis.db` - SQLite Database with SQLCipher):**

*   **Purpose:** The Synthesis Store is the primary repository for *processed, structured, and synthesized knowledge* derived from the raw data in the Chronicle and direct user input. It acts as OracleAI's active, queryable "working memory" and curated knowledge base. It's designed for efficient relational querying, data integrity, and to provide structured context to the AI agents. Unlike the append-only Chronicle, data here can be updated and refined (e.g., entity details, project statuses, evolving summaries).
*   **Storage Technology:** A single SQLite database file (e.g., `[AKASHIC_RECORD_PATH]/Databases/synthesis.db`).
*   **Encryption:** **Mandatory SQLCipher encryption** (e.g., via `pysqlcipher3` Python bindings). The OracleAI master password (obtained at startup) is used to decrypt/encrypt the database file for runtime access. This ensures the sensitive synthesized knowledge is protected at rest.
*   **Core Tables & Schemas:**

    1.  **`PermanentMemory` Table:**
        *   **Purpose:** Stores user-defined, critical, and relatively timeless facts, directives, or core principles that should always be considered by the AI agents.
        *   **Schema:**
            *   `id` TEXT PRIMARY KEY (UUID, e.g., `perm_mem_uuid_xxxx`)
            *   `text_content` TEXT NOT NULL (The actual fact or directive)
            *   `tags_json` TEXT (JSON array of strings for categorization, e.g., `["user_preference", "core_value", "communication_style"]`)
            *   `added_at` TEXT NOT NULL (ISO8601 DATETIME, when the entry was created)
            *   `last_modified_at` TEXT NOT NULL (ISO8601 DATETIME)
            *   `last_accessed_at` TEXT (ISO8601 DATETIME, for usage tracking)
            *   `source_description` TEXT (Brief note on how this memory was added, e.g., "User command on YYYY-MM-DD", "Inferred during memory consolidation session")
        *   **Indexes:** `id`, `tags_json` (if SQLite version supports JSON indexing, otherwise requires application-level filtering).

    2.  **`Entities` Table:**
        *   **Purpose:** A comprehensive catalog of all significant named entities (people, projects, organizations, locations, key concepts, tools, etc.) encountered or defined within OracleAI. Forms the nodes of a simulated knowledge graph.
        *   **Schema:**
            *   `id` TEXT PRIMARY KEY (UUID, e.g., `entity_uuid_xxxx`)
            *   `type` TEXT NOT NULL CHECK(type IN ('project', 'person', 'concept', 'tool', 'organization', 'location', 'event_ref', 'document_ref', 'custom_user_defined')) -- `event_ref` links to Calendar DB event ID, `document_ref` to an external document.
            *   `name` TEXT NOT NULL (Primary name or title of the entity, e.g., "Project Nova", "John Doe", "Semantic Search Concept")
            *   `aliases_json` TEXT (JSON array of alternative names or identifiers, e.g., `["Nova Initiative", "PNOVA"]`)
            *   `description_short` TEXT (A brief, one-liner description)
            *   `description_medium` TEXT (A few sentences providing more context)
            *   `description_detailed` TEXT (A more comprehensive overview, potentially LLM-generated and user-verified)
            *   `status` TEXT (Context-dependent, e.g., for 'project': 'ideation', 'planning', 'active', 'on_hold', 'completed', 'archived'; for 'person': 'active_contact', 'historical_figure')
            *   `tags_json` TEXT (JSON array for categorization and search)
            *   `created_at` TEXT NOT NULL (ISO8601 DATETIME)
            *   `last_modified_at` TEXT NOT NULL (ISO8601 DATETIME)
            *   `properties_json` TEXT (JSON blob for storing type-specific attributes, e.g., for 'project': `{"start_date": "...", "deadline": "...", "budget": "..."}`; for 'person': `{"role": "...", "contact_info": "..."}`)
            *   `vector_embedding_description` BLOB NULL (Optional, for semantic search on entity descriptions - Future)
        *   **Indexes:** `id`, `name`, `type`, `status`, `tags_json`.

    3.  **`Relationships` Table:**
        *   **Purpose:** Defines directed relationships between entities in the `Entities` table, forming the edges of the simulated knowledge graph.
        *   **Schema:**
            *   `id` INTEGER PRIMARY KEY AUTOINCREMENT (SQLite internal ID for the relationship itself)
            *   `source_entity_id` TEXT NOT NULL REFERENCES `Entities`(`id`) ON DELETE CASCADE
            *   `target_entity_id` TEXT NOT NULL REFERENCES `Entities`(`id`) ON DELETE CASCADE
            *   `type` TEXT NOT NULL (e.g., 'works_on_project', 'manages_project', 'related_to_concept', 'uses_tool', 'reports_to_person', 'sub_project_of', 'mentioned_in_context_of')
            *   `description` TEXT (Optional, provides context or nuance for the relationship, e.g., "Manages Project Nova since Q2 2024")
            *   `properties_json` TEXT (JSON blob for relationship-specific attributes, e.g., `{"start_date": "...", "role_in_relationship": "lead"}`)
            *   `discovered_at` TEXT NOT NULL (ISO8601 DATETIME, when the relationship was identified/added)
            *   `user_verified` INTEGER DEFAULT 0 CHECK(user_verified IN (0, 1)) -- 0=AI inferred/pending, 1=User verified
        *   **Indexes:** `source_entity_id`, `target_entity_id`, `type`.
        *   **Note:** Ensure `source_entity_id` and `target_entity_id` cannot be the same for most relationship types, or handle self-references appropriately.

    4.  **`FactsDecisions` Table:**
        *   **Purpose:** Stores atomic, verifiable pieces of information, choices made, hypotheses formulated, or key questions raised during interactions or analysis. These are more granular than full summaries.
        *   **Schema:**
            *   `id` TEXT PRIMARY KEY (UUID, e.g., `fact_uuid_xxxx`)
            *   `type` TEXT NOT NULL CHECK(type IN ('decision', 'fact_statement', 'hypothesis', 'key_question', 'milestone_achieved', 'blocker_identified'))
            *   `timestamp_occurred` TEXT NOT NULL (ISO8601 DATETIME, when the fact became known or decision was made/logged)
            *   `statement_text` TEXT NOT NULL (The core statement of the fact, decision, etc.)
            *   `reasoning_summary` TEXT (Brief summary of the rationale behind a decision or the evidence for a fact)
            *   `confidence_score` REAL (0.0 to 1.0, if applicable, e.g., for hypotheses or AI-inferred facts)
            *   `tags_json` TEXT (JSON array for categorization)
            *   `source_chronicle_turn_ids_json` TEXT NOT NULL (JSON array of `turn_id`s from Chronicle where this was discussed/derived)
            *   `user_verified` INTEGER DEFAULT 0 CHECK(user_verified IN (0, 1, 2)) -- 0=AI inferred, 1=User verified, 2=User explicitly marked as incorrect/outdated
            *   `created_at` TEXT NOT NULL (ISO8601 DATETIME, when this entry was created in the DB)
            *   `last_modified_at` TEXT NOT NULL
        *   **Indexes:** `id`, `type`, `timestamp_occurred`, `tags_json`, `user_verified`.

    5.  **`FactsDecisions_Entities_Link` Table:** (Many-to-many linking `FactsDecisions` to `Entities`)
        *   **Purpose:** Associates specific facts or decisions with the entities they pertain to.
        *   **Schema:**
            *   `fact_decision_id` TEXT NOT NULL REFERENCES `FactsDecisions`(`id`) ON DELETE CASCADE
            *   `entity_id` TEXT NOT NULL REFERENCES `Entities`(`id`) ON DELETE CASCADE
            *   `relevance_description` TEXT (Optional, e.g., "Decision directly impacts this project's timeline")
            *   PRIMARY KEY (`fact_decision_id`, `entity_id`)
        *   **Indexes:** `fact_decision_id`, `entity_id`.

    6.  **`Summaries` Table:**
        *   **Purpose:** Stores all levels of narrative summaries (daily, weekly, monthly) generated from the Chronicle and lower-level summaries.
        *   **Schema:**
            *   `id` TEXT PRIMARY KEY (UUID, e.g., `summary_uuid_xxxx`)
            *   `type` TEXT NOT NULL CHECK(type IN ('daily', 'weekly', 'monthly'))
            *   `date_key` TEXT NOT NULL (For 'daily': 'YYYY-MM-DD'; for 'weekly': 'YYYY-WW'; for 'monthly': 'YYYY-MM'. Indexed for quick temporal retrieval.)
            *   `created_at` TEXT NOT NULL (ISO8601 DATETIME)
            *   `user_verified` INTEGER DEFAULT 0 CHECK(user_verified IN (0, 1, 2)) -- 0=AI generated/pending, 1=User verified, 2=User marked as needing revision
            *   `fidelity_score` REAL (0.0 to 1.0, estimate of information preservation)
            *   `fidelity_method` TEXT (e.g., 'heuristic_compression', 'llm_assisted_eval_v1', 'user_rated')
            *   `fidelity_notes` TEXT (Justification for score or user comments)
            *   `narrative_short` TEXT (1-sentence summary)
            *   `narrative_medium` TEXT (3-5 sentence summary)
            *   `narrative_detailed` TEXT (1-2 paragraph summary)
            *   `key_points_json` TEXT (JSON array of bullet point strings)
            *   `extracted_keywords_json` TEXT (JSON array of top keywords for this summary)
            *   `sentiment_overview_json` TEXT (JSON blob summarizing sentiment for the period covered, e.g., `{"avg_vader_compound": 0.6, "dominant_nrc_emotions": ["joy"]}`)
            *   `source_ids_json` TEXT NOT NULL (JSON array of `turn_id`s from Chronicle if 'daily', or `summary_id`s of lower-level summaries if 'weekly'/'monthly')
            *   `vector_embedding_medium` BLOB NULL (Optional, for semantic search on `narrative_medium` - Future)
        *   **Indexes:** `id`, `type`, `date_key`, `user_verified`, `fidelity_score`.

    7.  **`Summaries_Entities_Link` Table:** (Many-to-many linking `Summaries` to `Entities`)
        *   **Purpose:** Associates summaries with the key entities discussed or relevant to them.
        *   **Schema:**
            *   `summary_id` TEXT NOT NULL REFERENCES `Summaries`(`id`) ON DELETE CASCADE
            *   `entity_id` TEXT NOT NULL REFERENCES `Entities`(`id`) ON DELETE CASCADE
            *   `mention_prominence` REAL (Optional, 0.0-1.0, how central is this entity to this summary)
            *   PRIMARY KEY (`summary_id`, `entity_id`)
        *   **Indexes:** `summary_id`, `entity_id`.

    8.  **`Summaries_FactsDecisions_Link` Table:** (Many-to-many linking `Summaries` to `FactsDecisions`)
        *   **Purpose:** Explicitly links summaries to the key facts/decisions they incorporate or reference.
        *   **Schema:**
            *   `summary_id` TEXT NOT NULL REFERENCES `Summaries`(`id`) ON DELETE CASCADE
            *   `fact_decision_id` TEXT NOT NULL REFERENCES `FactsDecisions`(`id`) ON DELETE CASCADE
            *   PRIMARY KEY (`summary_id`, `fact_decision_id`)
        *   **Indexes:** `summary_id`, `fact_decision_id`.

    9.  **`ProjectTopicThreads` Table:**
        *   **Purpose:** Provides a consolidated, evolving summary and status for specific long-running projects or key conceptual themes (which are themselves `Entities`).
        *   **Schema:**
            *   `id` TEXT PRIMARY KEY (UUID, e.g., `thread_uuid_xxxx`)
            *   `entity_id` TEXT NOT NULL UNIQUE REFERENCES `Entities`(`id`) ON DELETE CASCADE (Ensures one thread per designated project/topic entity)
            *   `last_updated_at` TEXT NOT NULL (ISO8601 DATETIME)
            *   `user_verified_summary` INTEGER DEFAULT 0
            *   `narrative_short_overall` TEXT (Current one-liner status/summary)
            *   `narrative_medium_overall` TEXT (Current 3-5 sentence status/summary)
            *   `narrative_detailed_log_json` TEXT (JSON array of timestamped detailed updates or log entries specific to this thread, e.g., `[{"timestamp": "...", "update_text": "..."}, ...]`)
            *   `key_points_overall_json` TEXT (Current key bullet points for the project/topic)
            *   `current_status_from_entity` TEXT (Can be denormalized from `Entities.status` for quick view, or be more specific to the thread)
            *   `key_milestones_achieved_ids_json` TEXT (JSON array of `FactsDecisions.id` that are milestones)
            *   `outstanding_issues_or_questions_ids_json` TEXT (JSON array of `FactsDecisions.id` that are open issues/questions)
            *   `referenced_summary_ids_json` TEXT (JSON array of general `Summaries.id` relevant to this thread)
            *   `referenced_facts_decisions_ids_json` TEXT (JSON array of general `FactsDecisions.id` relevant)
        *   **Indexes:** `id`, `entity_id`, `last_updated_at`.

    10. **`PatternAnalysisReports` Table:**
        *   **Purpose:** Stores the output of Shaman's deep analytical tasks.
        *   **Schema:**
            *   `id` TEXT PRIMARY KEY (UUID, e.g., `report_uuid_xxxx`)
            *   `date_generated` TEXT NOT NULL (ISO8601 DATETIME)
            *   `title` TEXT NOT NULL (Descriptive title of the analysis)
            *   `analyzed_period_description` TEXT (e.g., 'Chronicle: YYYY-MM-DD to YYYY-MM-DD', 'Project Phoenix Thread: Last 30 days')
            *   `report_narrative_text` TEXT (Full textual report from Shaman)
            *   `key_findings_json` TEXT (Structured key findings as JSON array/object)
            *   `supporting_data_references_json` TEXT (JSON array of IDs linking to relevant Summaries, Facts, Entities, Chronicle turns that support the findings)
            *   `generated_by_agent` TEXT DEFAULT 'agent_shaman'
            *   `task_id_source` TEXT NULL REFERENCES `Tasks`(`id`) ON DELETE SET NULL (Links to the task that generated this report)
        *   **Indexes:** `id`, `date_generated`, `title`.

*   **Interaction & Data Flow:**
    *   The Chronicle is the primary input for the Collaborative Daily Reflection.
    *   Verified outputs from this reflection populate `Entities`, `FactsDecisions`, and `daily_summaries` in the Synthesis Store.
    *   Higher-level summaries (`weekly`, `monthly`, `ProjectTopicThreads`) are synthesized by LLMs (Sage/Shaman) using data already in the Synthesis Store (lower-level summaries, entities, facts).
    *   Shaman's `PatternAnalysisReports` are generated by analyzing data across multiple tables in the Synthesis Store and the Chronicle.
    *   The Memory Bank Context Scaler queries multiple tables in the Synthesis Store (and potentially Chronicle via keyword/vector search) to build context for real-time LLM prompts.
    *   All write operations to the Synthesis Store are managed by `memory_interface.py`, ensuring data integrity and handling transactions.

**IV. The Akashic Record: Memory System Detailed Blueprint (Continued)**

### 4.1. Core Components & Storage Mechanisms (Continued)

**C. Calendar Cache (`calendar.db` - SQLite Database with SQLCipher):**

*   **Purpose:** To maintain a local, queryable copy of the user's calendar events from one or more external calendar services (e.g., Google Calendar, Microsoft Outlook Calendar, CalDAV sources). This local cache enables fast access to schedule information for contextualizing conversations, providing proactive reminders, and informing planning without requiring an API call for every query. It also allows for offline access to previously synced events.
*   **Storage Technology:** A dedicated SQLite database file (e.g., `[AKASHIC_RECORD_PATH]/Databases/calendar.db`).
*   **Encryption:** **Mandatory SQLCipher encryption**, using the OracleAI master password.
*   **Core Tables & Schemas:**
    1.  **`Calendars` Table:** (If supporting multiple calendar accounts/sources)
        *   `id` TEXT PRIMARY KEY (User-defined identifier or internal UUID for the calendar source, e.g., 'google_primary', 'outlook_work')
        *   `source_type` TEXT NOT NULL CHECK(source_type IN ('google', 'microsoft_graph', 'caldav', 'ics_import'))
        *   `account_identifier` TEXT NOT NULL (e.g., email address associated with the calendar)
        *   `display_name` TEXT (e.g., "Work Calendar", "Personal Calendar")
        *   `is_enabled` INTEGER DEFAULT 1 CHECK(is_enabled IN (0, 1))
        *   `last_successful_sync_utc` TEXT (ISO8601 DATETIME)
        *   `sync_token` TEXT NULL (For APIs like Google Calendar that support incremental sync)
        *   `oauth_credentials_json` TEXT NULL (Encrypted storage of OAuth tokens, or reference to OS credential store key)
        *   `color_hex` TEXT NULL (Optional, for UI display)
    2.  **`Events` Table:**
        *   `id` TEXT PRIMARY KEY (Unique event ID from the source calendar API, prefixed with calendar_id to ensure global uniqueness if multiple calendars, e.g., `google_primary_eventabcdef123`)
        *   `calendar_id` TEXT NOT NULL REFERENCES `Calendars`(`id`) ON DELETE CASCADE
        *   `title` TEXT NOT NULL
        *   `description` TEXT NULL
        *   `start_time_utc` TEXT NOT NULL (ISO8601 DATETIME, indexed) -- Store all times in UTC
        *   `end_time_utc` TEXT NOT NULL (ISO8601 DATETIME, indexed)
        *   `timezone_start` TEXT NULL (Original timezone, e.g., 'America/New_York')
        *   `timezone_end` TEXT NULL
        *   `is_all_day` INTEGER DEFAULT 0 CHECK(is_all_day IN (0, 1))
        *   `location` TEXT NULL
        *   `status` TEXT NULL (e.g., 'confirmed', 'tentative', 'cancelled' - from API)
        *   `is_recurring` INTEGER DEFAULT 0 CHECK(is_recurring IN (0, 1))
        *   `recurrence_rule` TEXT NULL (e.g., RRULE string from iCalendar spec)
        *   `recurring_event_id_source` TEXT NULL (ID of the master recurring event, if this is an instance)
        *   `html_link_source` TEXT NULL (Link to the event on the source calendar service)
        *   `created_at_source` TEXT NULL (ISO8601 DATETIME from API)
        *   `updated_at_source` TEXT NULL (ISO8601 DATETIME from API)
        *   `local_last_synced_utc` TEXT NOT NULL (ISO8601 DATETIME)
        *   `raw_api_data_json` TEXT NULL (Optional, for storing the original full API response for this event)
    3.  **`Attendees` Table:**
        *   `id` INTEGER PRIMARY KEY AUTOINCREMENT
        *   `event_id` TEXT NOT NULL REFERENCES `Events`(`id`) ON DELETE CASCADE
        *   `email` TEXT NOT NULL (Indexed)
        *   `display_name` TEXT NULL
        *   `response_status` TEXT NULL (e.g., 'accepted', 'declined', 'needsAction', 'tentative')
        *   `is_organizer` INTEGER DEFAULT 0 CHECK(is_organizer IN (0, 1))
        *   `is_optional` INTEGER DEFAULT 0 CHECK(is_optional IN (0, 1))
    *   **Indexes:** Critical for performance on `Events.start_time_utc`, `Events.end_time_utc`, `Events.calendar_id`, `Attendees.event_id`, `Attendees.email`.
*   **Interaction & Use:**
    *   **Synchronization:** `calendar_interface.py` handles OAuth 2.0 authentication and periodically syncs events from configured external calendars into `calendar.db`. It uses `sync_token` (if supported by API) for efficient incremental updates.
    *   **Retrieval:** The Memory Bank Context Scaler and agents query `calendar.db` (via `memory_interface.py`) for upcoming events, past events related to a topic/person, or to check user availability.
    *   **Contextualization:** Provides temporal context to conversations (e.g., "You have a meeting about Project Nova at 2 PM").
    *   **Planning & Reminders:** Sage can use calendar data for planning and generating reminders.
    *   **Shaman Analysis:** Shaman can correlate calendar density/event types with sentiment, productivity patterns, or goal progress.

**D. User Profile & Preferences (`profile.db` - SQLite Database with SQLCipher):**

*   **Purpose:** Stores explicit user-defined settings, preferences, long-term goals, key contacts, and configurations for OracleAI agents. This database allows OracleAI to deeply personalize its behavior and assistance.
*   **Storage Technology:** A dedicated SQLite database file (e.g., `[AKASHIC_RECORD_PATH]/Databases/profile.db`).
*   **Encryption:** **Mandatory SQLCipher encryption**.
*   **Core Tables & Schemas:**
    1.  **`UserPreferences` Table:** (Key-value store for general preferences)
        *   `key` TEXT PRIMARY KEY (e.g., 'communication_style', 'summary_default_length', 'preferred_units')
        *   `value` TEXT NOT NULL (e.g., 'direct_concise', 'medium', 'metric')
        *   `description` TEXT NULL (Explanation of the preference)
        *   `last_modified_utc` TEXT NOT NULL
    2.  **`UserGoals` Table:**
        *   `id` TEXT PRIMARY KEY (UUID, e.g., `goal_uuid_xxxx`)
        *   `description_text` TEXT NOT NULL (User's description of the goal)
        *   `status` TEXT NOT NULL DEFAULT 'active' CHECK(status IN ('active', 'on_hold', 'completed', 'archived', 'abandoned'))
        *   `priority` INTEGER DEFAULT 3 CHECK(priority IN (1, 2, 3, 4, 5)) -- 1=Highest
        *   `created_at` TEXT NOT NULL (ISO8601 DATETIME)
        *   `target_completion_date` TEXT NULL (ISO8601 DATE)
        *   `completion_date` TEXT NULL (ISO8601 DATETIME)
        *   `notes_text` TEXT NULL (Additional user notes about the goal)
        *   `linked_project_entity_id` TEXT NULL REFERENCES `Entities`(`id`) ON DELETE SET NULL (If this goal directly relates to a project in the Synthesis Store)
    3.  **`UserContacts` Table:** (Key people in the user's life/work, for contextual understanding)
        *   `id` TEXT PRIMARY KEY (UUID, e.g., `contact_uuid_xxxx`)
        *   `name` TEXT NOT NULL
        *   `relationship_type` TEXT (e.g., 'colleague', 'family_member', 'client', 'mentor')
        *   `contact_details_json` TEXT NULL (JSON blob for email, phone, etc. - store sensitively)
        *   `notes_text` TEXT NULL (User's notes about this contact)
        *   `linked_person_entity_id` TEXT NULL UNIQUE REFERENCES `Entities`(`id`) ON DELETE SET NULL (If this contact has a corresponding detailed `Entities` entry)
    4.  **`AgentConfigurations` Table:** (User overrides for default agent settings)
        *   `agent_name` TEXT PRIMARY KEY CHECK(agent_name IN ('sage', 'seer', 'shaman'))
        *   `tts_engine_override` TEXT NULL CHECK(tts_engine_override IN ('piper', 'xtts'))
        *   `tts_voice_path_override` TEXT NULL (Path to Piper .onnx or XTTS .wav)
        *   `tts_voice_config_path_override` TEXT NULL (Path to Piper .onnx.json)
        *   `llm_temperature_override` REAL NULL (Constrained to reasonable range, e.g., 0.0 to 2.0)
        *   `custom_prompt_snippet_prepend` TEXT NULL (Short text to always prepend to this agent's system prompt)
        *   `custom_prompt_snippet_append` TEXT NULL (Short text to always append)
*   **Interaction & Use:**
    *   Read frequently by all agents and the Context Scaler to tailor responses, understand priorities, and apply user-defined settings.
    *   Updated via explicit user commands ("OracleAI, remember my preferred summary length is short," "Set new goal: Learn Python") or through a dedicated settings GUI.
    *   Shaman may propose inferred preferences based on pattern analysis, which the user must confirm before they are written to this database.

**E. Task & Action Queue (`tasks.db` - SQLite Database with SQLCipher):**

*   **Purpose:** Manages asynchronous tasks, especially complex or long-running ones delegated to the Shaman, but can also be used for simpler background actions for Sage/Seer (e.g., "Sage, find articles on X and summarize them later"). Provides a persistent queue for work items.
*   **Storage Technology:** A dedicated SQLite database file (e.g., `[AKASHIC_RECORD_PATH]/Databases/tasks.db`).
*   **Encryption:** **Mandatory SQLCipher encryption**.
*   **Core Table & Schema (`Tasks`):**
    *   `id` INTEGER PRIMARY KEY AUTOINCREMENT (Simple incrementing ID for queue management)
    *   `task_uuid` TEXT NOT NULL UNIQUE (UUID for external reference)
    *   `description_text` TEXT NOT NULL (Detailed description of the task)
    *   `assigned_agent` TEXT NOT NULL CHECK(assigned_agent IN ('sage', 'seer', 'shaman', 'system'))
    *   `status` TEXT NOT NULL DEFAULT 'pending' CHECK(status IN ('pending', 'queued', 'running', 'completed', 'failed', 'cancelled', 'deferred')) (Indexed)
    *   `priority` INTEGER DEFAULT 3 CHECK(priority IN (1, 2, 3, 4, 5)) -- 1=Highest
    *   `created_at` TEXT NOT NULL (ISO8601 DATETIME)
    *   `user_id_creator` TEXT NULL (If created directly by user, store user identifier)
    *   `requesting_agent_id` TEXT NULL (If created by another agent, e.g., Sage queuing for Shaman)
    *   `shaman_depth_request` TEXT NULL (If for Shaman, e.g., 'Moon', 'Mars', 'Saturn' - from planetary scale)
    *   `input_parameters_json` TEXT NULL (JSON blob containing necessary input data or references for the task)
    *   `started_at` TEXT NULL (ISO8601 DATETIME)
    *   `completed_at` TEXT NULL (ISO8601 DATETIME)
    *   `estimated_duration_minutes` INTEGER NULL
    *   `progress_percent` INTEGER NULL (0-100)
    *   `result_summary_text` TEXT NULL (Brief summary of the outcome)
    *   `result_data_reference_id` TEXT NULL (e.g., ID of a `PatternAnalysisReport` or `Entity` in `synthesis.db`)
    *   `error_message` TEXT NULL (If status is 'failed')
*   **Indexes:** `status`, `assigned_agent`, `priority`, `task_uuid`.
*   **Interaction & Use:**
    *   User or AI agents create new tasks via `memory_interface.add_task()`.
    *   Agent processes (especially Shaman's dedicated thread/process) query `tasks.db` for 'pending' tasks matching their name and priority.
    *   Agent updates task status to 'running', performs the work, then updates to 'completed' (with results reference) or 'failed' (with error message).
    *   GUI can display task queue, progress, and results.
    *   `apscheduler` can be used to trigger agent processes to check the queue.

**F. Knowledge Graph (Conceptual - Future Enhancement, Initial Simulation via SQLite):**

*   **Purpose:** To explicitly model complex, n-ary relationships between entities (from the `Entities` table) that go beyond simple pairwise links. Aims to enable more sophisticated reasoning and contextual understanding.
*   **Initial Simulation (SQLite in `synthesis.db`):** The `Entities` table (nodes) and `Relationships` table (edges) already provide a basic relational graph structure. Queries can traverse these links.
*   **Future Dedicated Graph DB (e.g., Neo4j, ArangoDB):** If the complexity of relationship queries and graph traversal algorithms becomes a bottleneck or requires more advanced graph features (e.g., pathfinding, centrality measures, community detection), migrating this component to a dedicated graph database would be considered. This would involve:
    *   Defining node labels and relationship types in the graph DB.
    *   A process (likely run by Shaman) to periodically extract data from `Entities` and `Relationships` in `synthesis.db` and populate/update the graph database.
    *   OracleAI agents would then query the graph database directly for complex relational insights.
*   **Interaction & Use (Future):** Enables queries like "Find all projects managed by people who previously worked on a failed project that used Technology X," or "What is the shortest path of influence between Concept A and Decision B?".

**G. Vector Store (Semantic Memory - Future Enhancement):**

*   **Purpose:** To enable retrieval of memory items (Chronicle snippets, Summaries, Entity descriptions) based on semantic meaning and conceptual similarity, rather than just exact keyword matches. This is crucial for handling paraphrasing, synonyms, and abstract queries.
*   **Technology:** A dedicated vector database (e.g., ChromaDB [local, easy to integrate], FAISS [index library, needs metadata store], Weaviate, Milvus) or a managed cloud service (Pinecone, though this breaks local-first for this component).
*   **Implementation:**
    1.  **Embedding Model:** Select and configure an embedding model (e.g., `mxbai-embed-large`, Sentence Transformers models via `sentence-transformers` library). This model converts text chunks into dense vector representations.
    2.  **Embedding Generation:** A background process (Shaman or dedicated task) iterates through new/updated text content in the Chronicle and Synthesis Store (e.g., `Summaries.narrative_medium`, `Entities.description_medium`, selected Chronicle turns). It generates embeddings for these chunks.
    3.  **Storage:** Store these embeddings in the Vector Database along with metadata (e.g., the source `turn_id` or `summary_id`, date, type) that links back to the original data in Chronicle/Synthesis Store.
    4.  **Querying:** When the Memory Bank Context Scaler needs to find semantically relevant information:
        *   Embed the user's current query (or relevant parts of the recent conversation).
        *   Query the Vector Database with this query embedding to find the top K most similar stored embeddings.
        *   Retrieve the metadata (source IDs) for these top K results.
        *   Fetch the actual text content from Chronicle/Synthesis Store using these IDs.
*   **Interaction & Use:** The primary consumer is the Memory Bank Context Scaler, which uses semantic search results as high-quality candidates for LLM context. Shaman might also use it for finding semantically related but non-obvious patterns.

This detailed breakdown of the Akashic Record components illustrates the depth and interconnectedness of the memory system, designed to provide OracleAI with a rich, evolving, and queryable understanding of the user and their world.

**IV. The Akashic Record: Memory System Detailed Blueprint (Continued)**

### 4.1. Core Components & Storage Mechanisms (Continued)

**C. Calendar Cache (`calendar.db` - SQLite Database with SQLCipher):**

*   **Purpose:** To maintain a local, queryable copy of the user's calendar events from one or more external calendar services (e.g., Google Calendar, Microsoft Outlook Calendar, CalDAV sources). This local cache enables fast access to schedule information for contextualizing conversations, providing proactive reminders, and informing planning without requiring an API call for every query. It also allows for offline access to previously synced events.
*   **Storage Technology:** A dedicated SQLite database file (e.g., `[AKASHIC_RECORD_PATH]/Databases/calendar.db`).
*   **Encryption:** **Mandatory SQLCipher encryption**, using the OracleAI master password.
*   **Core Tables & Schemas:**
    1.  **`Calendars` Table:** (If supporting multiple calendar accounts/sources)
        *   `id` TEXT PRIMARY KEY (User-defined identifier or internal UUID for the calendar source, e.g., 'google_primary', 'outlook_work')
        *   `source_type` TEXT NOT NULL CHECK(source_type IN ('google', 'microsoft_graph', 'caldav', 'ics_import'))
        *   `account_identifier` TEXT NOT NULL (e.g., email address associated with the calendar)
        *   `display_name` TEXT (e.g., "Work Calendar", "Personal Calendar")
        *   `is_enabled` INTEGER DEFAULT 1 CHECK(is_enabled IN (0, 1))
        *   `last_successful_sync_utc` TEXT (ISO8601 DATETIME)
        *   `sync_token` TEXT NULL (For APIs like Google Calendar that support incremental sync)
        *   `oauth_credentials_json` TEXT NULL (Encrypted storage of OAuth tokens, or reference to OS credential store key)
        *   `color_hex` TEXT NULL (Optional, for UI display)
    2.  **`Events` Table:**
        *   `id` TEXT PRIMARY KEY (Unique event ID from the source calendar API, prefixed with calendar_id to ensure global uniqueness if multiple calendars, e.g., `google_primary_eventabcdef123`)
        *   `calendar_id` TEXT NOT NULL REFERENCES `Calendars`(`id`) ON DELETE CASCADE
        *   `title` TEXT NOT NULL
        *   `description` TEXT NULL
        *   `start_time_utc` TEXT NOT NULL (ISO8601 DATETIME, indexed) -- Store all times in UTC
        *   `end_time_utc` TEXT NOT NULL (ISO8601 DATETIME, indexed)
        *   `timezone_start` TEXT NULL (Original timezone, e.g., 'America/New_York')
        *   `timezone_end` TEXT NULL
        *   `is_all_day` INTEGER DEFAULT 0 CHECK(is_all_day IN (0, 1))
        *   `location` TEXT NULL
        *   `status` TEXT NULL (e.g., 'confirmed', 'tentative', 'cancelled' - from API)
        *   `is_recurring` INTEGER DEFAULT 0 CHECK(is_recurring IN (0, 1))
        *   `recurrence_rule` TEXT NULL (e.g., RRULE string from iCalendar spec)
        *   `recurring_event_id_source` TEXT NULL (ID of the master recurring event, if this is an instance)
        *   `html_link_source` TEXT NULL (Link to the event on the source calendar service)
        *   `created_at_source` TEXT NULL (ISO8601 DATETIME from API)
        *   `updated_at_source` TEXT NULL (ISO8601 DATETIME from API)
        *   `local_last_synced_utc` TEXT NOT NULL (ISO8601 DATETIME)
        *   `raw_api_data_json` TEXT NULL (Optional, for storing the original full API response for this event)
    3.  **`Attendees` Table:**
        *   `id` INTEGER PRIMARY KEY AUTOINCREMENT
        *   `event_id` TEXT NOT NULL REFERENCES `Events`(`id`) ON DELETE CASCADE
        *   `email` TEXT NOT NULL (Indexed)
        *   `display_name` TEXT NULL
        *   `response_status` TEXT NULL (e.g., 'accepted', 'declined', 'needsAction', 'tentative')
        *   `is_organizer` INTEGER DEFAULT 0 CHECK(is_organizer IN (0, 1))
        *   `is_optional` INTEGER DEFAULT 0 CHECK(is_optional IN (0, 1))
    *   **Indexes:** Critical for performance on `Events.start_time_utc`, `Events.end_time_utc`, `Events.calendar_id`, `Attendees.event_id`, `Attendees.email`.
*   **Interaction & Use:**
    *   **Synchronization:** `calendar_interface.py` handles OAuth 2.0 authentication and periodically syncs events from configured external calendars into `calendar.db`. It uses `sync_token` (if supported by API) for efficient incremental updates.
    *   **Retrieval:** The Memory Bank Context Scaler and agents query `calendar.db` (via `memory_interface.py`) for upcoming events, past events related to a topic/person, or to check user availability.
    *   **Contextualization:** Provides temporal context to conversations (e.g., "You have a meeting about Project Nova at 2 PM").
    *   **Planning & Reminders:** Sage can use calendar data for planning and generating reminders.
    *   **Shaman Analysis:** Shaman can correlate calendar density/event types with sentiment, productivity patterns, or goal progress.

**D. User Profile & Preferences (`profile.db` - SQLite Database with SQLCipher):**

*   **Purpose:** Stores explicit user-defined settings, preferences, long-term goals, key contacts, and configurations for OracleAI agents. This database allows OracleAI to deeply personalize its behavior and assistance.
*   **Storage Technology:** A dedicated SQLite database file (e.g., `[AKASHIC_RECORD_PATH]/Databases/profile.db`).
*   **Encryption:** **Mandatory SQLCipher encryption**.
*   **Core Tables & Schemas:**
    1.  **`UserPreferences` Table:** (Key-value store for general preferences)
        *   `key` TEXT PRIMARY KEY (e.g., 'communication_style', 'summary_default_length', 'preferred_units')
        *   `value` TEXT NOT NULL (e.g., 'direct_concise', 'medium', 'metric')
        *   `description` TEXT NULL (Explanation of the preference)
        *   `last_modified_utc` TEXT NOT NULL
    2.  **`UserGoals` Table:**
        *   `id` TEXT PRIMARY KEY (UUID, e.g., `goal_uuid_xxxx`)
        *   `description_text` TEXT NOT NULL (User's description of the goal)
        *   `status` TEXT NOT NULL DEFAULT 'active' CHECK(status IN ('active', 'on_hold', 'completed', 'archived', 'abandoned'))
        *   `priority` INTEGER DEFAULT 3 CHECK(priority IN (1, 2, 3, 4, 5)) -- 1=Highest
        *   `created_at` TEXT NOT NULL (ISO8601 DATETIME)
        *   `target_completion_date` TEXT NULL (ISO8601 DATE)
        *   `completion_date` TEXT NULL (ISO8601 DATETIME)
        *   `notes_text` TEXT NULL (Additional user notes about the goal)
        *   `linked_project_entity_id` TEXT NULL REFERENCES `Entities`(`id`) ON DELETE SET NULL (If this goal directly relates to a project in the Synthesis Store)
    3.  **`UserContacts` Table:** (Key people in the user's life/work, for contextual understanding)
        *   `id` TEXT PRIMARY KEY (UUID, e.g., `contact_uuid_xxxx`)
        *   `name` TEXT NOT NULL
        *   `relationship_type` TEXT (e.g., 'colleague', 'family_member', 'client', 'mentor')
        *   `contact_details_json` TEXT NULL (JSON blob for email, phone, etc. - store sensitively)
        *   `notes_text` TEXT NULL (User's notes about this contact)
        *   `linked_person_entity_id` TEXT NULL UNIQUE REFERENCES `Entities`(`id`) ON DELETE SET NULL (If this contact has a corresponding detailed `Entities` entry)
    4.  **`AgentConfigurations` Table:** (User overrides for default agent settings)
        *   `agent_name` TEXT PRIMARY KEY CHECK(agent_name IN ('sage', 'seer', 'shaman'))
        *   `tts_engine_override` TEXT NULL CHECK(tts_engine_override IN ('piper', 'xtts'))
        *   `tts_voice_path_override` TEXT NULL (Path to Piper .onnx or XTTS .wav)
        *   `tts_voice_config_path_override` TEXT NULL (Path to Piper .onnx.json)
        *   `llm_temperature_override` REAL NULL (Constrained to reasonable range, e.g., 0.0 to 2.0)
        *   `custom_prompt_snippet_prepend` TEXT NULL (Short text to always prepend to this agent's system prompt)
        *   `custom_prompt_snippet_append` TEXT NULL (Short text to always append)
*   **Interaction & Use:**
    *   Read frequently by all agents and the Context Scaler to tailor responses, understand priorities, and apply user-defined settings.
    *   Updated via explicit user commands ("OracleAI, remember my preferred summary length is short," "Set new goal: Learn Python") or through a dedicated settings GUI.
    *   Shaman may propose inferred preferences based on pattern analysis, which the user must confirm before they are written to this database.

**E. Task & Action Queue (`tasks.db` - SQLite Database with SQLCipher):**

*   **Purpose:** Manages asynchronous tasks, especially complex or long-running ones delegated to the Shaman, but can also be used for simpler background actions for Sage/Seer (e.g., "Sage, find articles on X and summarize them later"). Provides a persistent queue for work items.
*   **Storage Technology:** A dedicated SQLite database file (e.g., `[AKASHIC_RECORD_PATH]/Databases/tasks.db`).
*   **Encryption:** **Mandatory SQLCipher encryption**.
*   **Core Table & Schema (`Tasks`):**
    *   `id` INTEGER PRIMARY KEY AUTOINCREMENT (Simple incrementing ID for queue management)
    *   `task_uuid` TEXT NOT NULL UNIQUE (UUID for external reference)
    *   `description_text` TEXT NOT NULL (Detailed description of the task)
    *   `assigned_agent` TEXT NOT NULL CHECK(assigned_agent IN ('sage', 'seer', 'shaman', 'system'))
    *   `status` TEXT NOT NULL DEFAULT 'pending' CHECK(status IN ('pending', 'queued', 'running', 'completed', 'failed', 'cancelled', 'deferred')) (Indexed)
    *   `priority` INTEGER DEFAULT 3 CHECK(priority IN (1, 2, 3, 4, 5)) -- 1=Highest
    *   `created_at` TEXT NOT NULL (ISO8601 DATETIME)
    *   `user_id_creator` TEXT NULL (If created directly by user, store user identifier)
    *   `requesting_agent_id` TEXT NULL (If created by another agent, e.g., Sage queuing for Shaman)
    *   `shaman_depth_request` TEXT NULL (If for Shaman, e.g., 'Moon', 'Mars', 'Saturn' - from planetary scale)
    *   `input_parameters_json` TEXT NULL (JSON blob containing necessary input data or references for the task)
    *   `started_at` TEXT NULL (ISO8601 DATETIME)
    *   `completed_at` TEXT NULL (ISO8601 DATETIME)
    *   `estimated_duration_minutes` INTEGER NULL
    *   `progress_percent` INTEGER NULL (0-100)
    *   `result_summary_text` TEXT NULL (Brief summary of the outcome)
    *   `result_data_reference_id` TEXT NULL (e.g., ID of a `PatternAnalysisReport` or `Entity` in `synthesis.db`)
    *   `error_message` TEXT NULL (If status is 'failed')
*   **Indexes:** `status`, `assigned_agent`, `priority`, `task_uuid`.
*   **Interaction & Use:**
    *   User or AI agents create new tasks via `memory_interface.add_task()`.
    *   Agent processes (especially Shaman's dedicated thread/process) query `tasks.db` for 'pending' tasks matching their name and priority.
    *   Agent updates task status to 'running', performs the work, then updates to 'completed' (with results reference) or 'failed' (with error message).
    *   GUI can display task queue, progress, and results.
    *   `apscheduler` can be used to trigger agent processes to check the queue.

**F. Knowledge Graph (Conceptual - Future Enhancement, Initial Simulation via SQLite):**

*   **Purpose:** To explicitly model complex, n-ary relationships between entities (from the `Entities` table) that go beyond simple pairwise links. Aims to enable more sophisticated reasoning and contextual understanding.
*   **Initial Simulation (SQLite in `synthesis.db`):** The `Entities` table (nodes) and `Relationships` table (edges) already provide a basic relational graph structure. Queries can traverse these links.
*   **Future Dedicated Graph DB (e.g., Neo4j, ArangoDB):** If the complexity of relationship queries and graph traversal algorithms becomes a bottleneck or requires more advanced graph features (e.g., pathfinding, centrality measures, community detection), migrating this component to a dedicated graph database would be considered. This would involve:
    *   Defining node labels and relationship types in the graph DB.
    *   A process (likely run by Shaman) to periodically extract data from `Entities` and `Relationships` in `synthesis.db` and populate/update the graph database.
    *   OracleAI agents would then query the graph database directly for complex relational insights.
*   **Interaction & Use (Future):** Enables queries like "Find all projects managed by people who previously worked on a failed project that used Technology X," or "What is the shortest path of influence between Concept A and Decision B?".

**G. Vector Store (Semantic Memory - Future Enhancement):**

*   **Purpose:** To enable retrieval of memory items (Chronicle snippets, Summaries, Entity descriptions) based on semantic meaning and conceptual similarity, rather than just exact keyword matches. This is crucial for handling paraphrasing, synonyms, and abstract queries.
*   **Technology:** A dedicated vector database (e.g., ChromaDB [local, easy to integrate], FAISS [index library, needs metadata store], Weaviate, Milvus) or a managed cloud service (Pinecone, though this breaks local-first for this component).
*   **Implementation:**
    1.  **Embedding Model:** Select and configure an embedding model (e.g., `mxbai-embed-large`, Sentence Transformers models via `sentence-transformers` library). This model converts text chunks into dense vector representations.
    2.  **Embedding Generation:** A background process (Shaman or dedicated task) iterates through new/updated text content in the Chronicle and Synthesis Store (e.g., `Summaries.narrative_medium`, `Entities.description_medium`, selected Chronicle turns). It generates embeddings for these chunks.
    3.  **Storage:** Store these embeddings in the Vector Database along with metadata (e.g., the source `turn_id` or `summary_id`, date, type) that links back to the original data in Chronicle/Synthesis Store.
    4.  **Querying:** When the Memory Bank Context Scaler needs to find semantically relevant information:
        *   Embed the user's current query (or relevant parts of the recent conversation).
        *   Query the Vector Database with this query embedding to find the top K most similar stored embeddings.
        *   Retrieve the metadata (source IDs) for these top K results.
        *   Fetch the actual text content from Chronicle/Synthesis Store using these IDs.
*   **Interaction & Use:** The primary consumer is the Memory Bank Context Scaler, which uses semantic search results as high-quality candidates for LLM context. Shaman might also use it for finding semantically related but non-obvious patterns.

This detailed breakdown of the Akashic Record components illustrates the depth and interconnectedness of the memory system, designed to provide OracleAI with a rich, evolving, and queryable understanding of the user and their world.

**V. Key Memory System Processes & Workflows (Continued)**

### 5.3. Memory Bank Context Scaler (Real-time RAG Engine) (Continued from Part 5)
*(The detailed workflow for the Context Scaler was provided in Part 5. This note confirms its place and importance.)*
The Memory Bank Context Scaler is the critical real-time engine that bridges the vastness of the Akashic Record with the finite context window of the LLMs. Its sophisticated retrieval, ranking, and budget-fitting mechanisms are essential for providing relevant, timely, and token-efficient context to Sage and Seer for every interaction.

### 5.4. Deep Pattern Weaving (Shaman's Autonomous Analysis)

*   **Goal:** To leverage the Shaman (Deep Brain) agent's powerful LLM and dedicated processing time to uncover long-term trends, subtle correlations, emergent patterns, and profound insights from the entirety of the Akashic Record that would be too computationally expensive or complex for real-time analysis.
*   **Trigger:** Scheduled background tasks (e.g., nightly, weekly via `apscheduler` in `main.py`) or explicitly assigned analytical tasks by the user or other agents via the Task Queue.
*   **Primary Agent Involved:** Shaman.
*   **Inputs:** Queries across multiple Akashic Record components:
    *   `Chronicle` (raw interaction text, timestamps, logged emotion/sentiment scores, metadata tags).
    *   `Synthesis Store` (`Summaries` for sentiment overviews and keywords, `Entities` for tracking focus, `FactsDecisions` for decision patterns, `ProjectTopicThreads` for progress).
    *   `Calendar Cache` (`calendar.db` for event types, frequency, correlations with mood/productivity).
    *   `User Profile & Preferences` (`profile.db` for goals, stated interests).
    *   (Future) `Knowledge Graph` for relational patterns.
    *   (Future) `Word Frequency Indexes` for thematic shifts.
*   **Workflow Examples & Types of Analysis:**
    1.  **Sentiment & Emotional Trend Analysis:**
        *   Calculate moving averages of VADER compound scores, TextBlob polarity, or frequency of dominant NRC/SER emotions over weeks/months.
        *   Identify periods of sustained positive/negative sentiment or notable emotional shifts.
        *   Correlate these trends with:
            *   Keywords or topics prevalent in `Summaries` or Chronicle during those periods.
            *   Specific `Entities` (projects, people) being discussed.
            *   Events from the `Calendar Cache` (e.g., "Sentiment typically lower during weeks with many 'Work Deadline' events").
            *   Progress on `UserGoals`.
    2.  **Topic & Interest Evolution:**
        *   Analyze `extracted_keywords_json` from `Summaries` or run Topic Modeling (NMF/LDA) on Chronicle text over extended periods.
        *   Identify recurring, emerging, or fading topics of discussion or user focus.
        *   Track the evolution of user interest in specific `Entities` (concepts, tools, projects).
    3.  **Goal Progress & Blocker Analysis:**
        *   Analyze `UserGoals` status, linked `FactsDecisions` (milestones, blockers), and `ProjectTopicThreads`.
        *   Identify common reasons for delays or success in past goals.
        *   Correlate goal progress with sentiment, calendar density, or discussion topics.
    4.  **Behavioral Pattern Identification:**
        *   Analyze `metadata_tags` in Chronicle or interaction patterns (e.g., frequency of using "Guided Generation" commands, types of questions typically asked to Sage vs. Seer, common times of day for certain activities if logged).
        *   Identify user's typical problem-solving approaches or communication styles.
    5.  **Knowledge Gap Identification:**
        *   Analyze user queries and AI responses to identify topics where the AI frequently lacks information or where the user repeatedly asks for clarification. This could suggest areas for focused Deep Search or for the user to add to Permanent Memory.
    6.  **Cross-Domain Synthesis:** Combine insights from multiple data types. For example, "User sentiment (Emotion) tends to be higher, and progress on 'Creative Writing' goal (Profile) is better, during weeks with fewer scheduled meetings (Calendar) and more discussion of 'Nature' (Keywords from Summaries)."
*   **Output:**
    *   Generates structured `PatternAnalysisReports` which are stored in the `PatternAnalysisReports` table of `synthesis.db`. These reports include:
        *   Title, analyzed period, narrative description of the pattern/insight.
        *   Structured `key_findings_json`.
        *   `supporting_data_references_json` (links to specific Chronicle turns, Summaries, Entities, Facts that support the finding).
    *   May propose updates to the `User Profile` (e.g., inferred preferences, potential new goals based on emerging interests), which **must** be presented to the user for confirmation before being committed.
    *   Can flag anomalies or significant deviations from established patterns for user attention.
*   **LLM Prompting for Shaman:** Prompts for these tasks are complex, instructing Shaman to act as a data scientist, historian, or psychologist, to query specific data, perform correlations, and synthesize findings into a coherent report. Example: "Analyze sentiment trends from daily summaries over the past 3 months. Correlate periods of low sentiment with dominant keywords and calendar event types from those periods. Report key findings and potential contributing factors."

### 5.5. Word Frequency Indexing (Optional Background Analysis)

*   **Goal:** To provide a high-level, quantitative overview of thematic content and vocabulary usage over time, primarily for Shaman's long-term analytical tasks.
*   **Trigger:** Background task run periodically (e.g., daily after Chronicle log finalization) by a system process or Shaman.
*   **Process:**
    1.  For each new day's `Chronicle` log (or for all logs if building initially):
        *   Extract all `text_final_processed` content.
        *   Perform text normalization: lowercase, remove punctuation.
        *   Perform **stop-word removal** (using a comprehensive list like NLTK's or spaCy's).
        *   Perform **lemmatization** (reducing words to their base/dictionary form, e.g., "running" -> "run") using `nltk.stem.WordNetLemmatizer` or `spaCy`.
        *   Calculate word frequencies for the processed text.
    2.  **Storage:**
        *   **Per-Log Index:** Save the sorted word frequency list (e.g., top N words or all words above a certain frequency) for each daily Chronicle log, perhaps as a separate small JSON file (e.g., `[AKASHIC_RECORD_PATH]/Indexes/WordFrequency/YYYY-MM-DD_wordfreq.json`) or in a dedicated SQLite table.
        *   **Master Cumulative Index:** Maintain a master index (e.g., `master_word_index.json` or SQLite table) that aggregates word counts across *all* Chronicle logs over time. This needs to be updated incrementally.
*   **Usage:**
    *   **Shaman's Analysis:** Primary consumer. Shaman can analyze the master index for long-term vocabulary shifts, identify consistently dominant terms (indicating core user interests), or track the rise and fall of specific keywords over months/years, correlating this with other patterns.
    *   **Retrieval Cue (Minor):** Very occasionally, if semantic search fails or for very specific queries, the top N words from a relevant daily index might offer a crude thematic hint to the Context Scaler, but this is a secondary use.
    *   **Not for Direct LLM Prompting (Usually):** Raw word frequency lists are generally not very token-efficient or useful as direct context for real-time LLM responses compared to narrative summaries or structured facts. Their value is in aggregate analysis.

### 5.6. Memory Maintenance & Evolution

*   **Goal:** To ensure the Akashic Record remains accurate, relevant, manageable, and efficient over time, preventing it from becoming an overwhelming and noisy data dump.
*   **Trigger:** Periodic background tasks (Shaman), user commands, or as part of the collaborative reflection process.
*   **Key Processes:**
    1.  **De-duplication & Merging (Shaman-Proposed, User-Verified):**
        *   Shaman periodically scans `Entities` and `FactsDecisions` for highly similar or redundant entries (using string similarity, semantic similarity of descriptions if embeddings are available, or LLM-based comparison).
        *   Proposes potential merges or de-duplications to the user.
        *   If user confirms, `memory_interface` performs the merge, updating links and archiving/deleting the redundant entry.
    2.  **Archiving (Automated Rules + User Control):**
        *   Define rules for archiving older data (e.g., "Archive daily summaries older than 12 months if a verified monthly summary for that period exists and has high fidelity").
        *   Archived entries are flagged (e.g., `Entities.status = 'archived'`, `Summaries.type = 'daily_archived'`) and might be moved to a separate "cold storage" area or excluded from default retrieval by the Context Scaler, but remain searchable if explicitly requested.
        *   Users can manually archive/unarchive entries.
    3.  **Link Integrity Checks (System Task):** Periodically verify that foreign key relationships in SQLite and ID links in JSON structures are valid. Report broken links.
    4.  **Fidelity Review & Re-Summarization:**
        *   If Shaman's analysis or user feedback indicates a summary has low fidelity or is outdated, it can be flagged for review.
        *   The user can initiate a re-summarization process for that item, potentially providing new guidance to the LLM.
    5.  **Schema Evolution:** As OracleAI develops, the schemas for memory components may need to evolve. Plan for migration scripts or processes to update existing data to new schema versions.

## VI. Emotional Intelligence Suite: Design & Integration

OracleAI's Emotional Intelligence Suite is a critical set of components designed to enable the AI council to perceive, interpret, and appropriately respond to the user's emotional state, fostering more natural, empathetic, and effective interactions. This suite processes both vocal and textual cues.

### 6.1. Components & Technologies

*   **A. Speech Emotion Recognition (SER):**
    *   **Purpose:** To infer the user's emotional state directly from the acoustic properties of their voice.
    *   **Technology Stack:**
        1.  **Audio Input:** Raw audio from user utterances (`.wav` files captured by `audio_processing.py`).
        2.  **Feature Extraction (CPU):** `librosa` library used to extract relevant acoustic features (e.g., MFCCs, pitch contours, energy, jitter, shimmer, spectral features). This pre-processing step converts the raw waveform into a numerical representation suitable for ML models.
        3.  **Model Inference (GPU):** Pre-trained SER models, typically deep learning architectures (e.g., based on Wav2Vec2, CNNs, LSTMs, or Transformers), loaded and run using PyTorch and the `transformers` library. These models are trained to classify feature sets into discrete emotion categories.
            *   *Model Source:* Hugging Face Hub is a primary source for such models (e.g., `jonatasgrosman/wav2vec2-large-xlsr-53-english` or others specialized for emotion).
    *   **Output:**
        *   `dominant_emotion`: The emotion category with the highest predicted probability (e.g., "happy," "sad," "angry," "neutral," "fear," "surprise," "disgust").
        *   `scores`: A dictionary or JSON object containing the probability distribution across all supported emotion categories.
        *   `confidence`: An overall confidence score for the dominant emotion prediction.
        *   `model_used`: Identifier of the SER model.
    *   **Integration:** Results are logged in the Chronicle for each user turn and passed as context to the LLM agents.

*   **B. Text Sentiment & Emotion Analysis:**
    *   **Purpose:** To analyze the semantic content of the transcribed user text to determine sentiment polarity, subjectivity, and associated discrete emotions.
    *   **Technology Stack (CPU-based libraries):**
        1.  **VADER (`vaderSentiment`):** Provides a compound sentiment score (ranging from -1, most negative, to +1, most positive) and proportions of positive, neutral, and negative sentiment. Particularly good for social media-style text and capturing intensity.
        2.  **TextBlob (`textblob`):** Offers polarity (similar to VADER's compound, -1 to +1) and subjectivity (0, objective, to 1, subjective) scores.
        3.  **NRCLex (`nrclex`):** Uses the NRC Emotion Lexicon to identify word associations with eight basic emotions (joy, sadness, anger, fear, trust, disgust, surprise, anticipation) and positive/negative sentiment, providing raw counts or scores for each.
    *   **Output:**
        *   VADER: `compound`, `pos`, `neu`, `neg` scores.
        *   TextBlob: `polarity`, `subjectivity` scores.
        *   NRCLex: `dominant_emotions` (list, as multiple can be high), full `scores_json`.
    *   **Integration:** Results are logged in the Chronicle and provided as context to LLMs, often alongside SER results.

### 6.2. Workflow & Integration with LLMs

1.  **Post-STT Processing:** Immediately after `stt_interface.py` transcribes a user utterance, `main.py` passes both the audio file path and the transcribed text to `emotion_analyzer.py`.
2.  **Parallel Analysis:** `emotion_analyzer.py` performs SER on the audio and text-based sentiment/emotion analysis on the text concurrently (or sequentially if resource-constrained).
3.  **Combined Emotional Context:** The results from SER and text analysis are aggregated into a structured dictionary.
4.  **Chronicle Logging:** This full emotional context dictionary is logged as part of the user's turn in the `YYYY-MM-DD_chronicle.jsonl` file.
5.  **LLM Prompt Injection:** The Memory Bank Context Scaler (or `main.py` directly) incorporates key emotional indicators into the prompt sent to Sage, Seer, or Shaman. This can be done by:
    *   Adding a metadata prefix to the user's input: `User (Voice: Happy 0.8; TextSentiment: Positive 0.9, Joyful): "That's fantastic news!"`
    *   Including a dedicated section in the system prompt: `[Current User Emotional State: Voice detected as Happy (High Confidence). Text analysis suggests Joy and strong Positive sentiment.]`
6.  **Agent Utilization:**
    *   **Seer:** Explicitly prompted to consider and respond to the user's emotional state, tailor its tone, and explore emotional dimensions of the conversation.
    *   **Sage:** Uses emotional data as an additional data point for analysis (e.g., "User expressed frustration when discussing timeline for Project X").
    *   **Shaman:** Analyzes long-term emotional trends from the Chronicle, correlating them with topics, events, and goals to generate insights for the `PatternAnalysisReports` or propose updates to the `User Profile`.

### 6.3. Benefits & Applications

*   **Empathetic & Nuanced Responses:** Enables AI agents to move beyond literal text interpretation and respond in a way that acknowledges and respects the user's feelings.
*   **Detection of Sarcasm/Subtext:** Comparing voice emotion (SER) with text sentiment can help identify potential mismatches indicative of sarcasm or unspoken feelings.
*   **Personalized Interaction:** AI can learn the user's typical emotional responses to certain topics or situations and adapt its approach.
*   **User Well-being Monitoring (Ethical & Opt-In):** Long-term analysis of emotional trends by Shaman could (with explicit user consent and control) provide insights into patterns affecting well-being, acting as a data source for user self-reflection.
*   **Richer Memory Logs:** The Chronicle becomes a much richer record of interactions when emotional context is included, providing deeper insights during later review or analysis.
*   **Improved Collaborative Memory Consolidation:** During daily reflection, Seer can use the logged emotional data to help ensure that the *feeling* and *significance* of events are captured in summaries, not just the facts.

The Emotional Intelligence Suite is a cornerstone of making OracleAI a truly advanced and human-centered cognitive partner.

## VI. Multimodal Capabilities: Voice, Text, Vision

OracleAI is designed as a multimodal system, capable of processing and integrating information from different input types to achieve a richer understanding of the user's context and requests.

### 6.1. Voice Modality (Primary Interaction)

*   **A. Voice Input (User to AI):**
    *   **Capture:** Handled by `audio_processing.py` using `pyaudio` to access the system's default microphone.
    *   **Voice Activity Detection (VAD):** A crucial component within `audio_processing.py`. It continuously monitors the audio stream's energy levels (e.g., Root Mean Square - RMS via `audioop`) against a configurable `THRESHOLD`. Speech is buffered while energy is above the threshold. When energy drops below the threshold for a configurable `SILENCE_LIMIT` duration, the utterance is considered complete.
    *   **Storage:** The complete audio utterance is saved as a temporary `.wav` file (e.g., in a `[AKASHIC_RECORD_PATH]/AudioLogs/temp/` directory with a unique timestamped filename). This file path is passed for STT and SER.
    *   **Speech-to-Text (STT):** The `.wav` file is processed by `stt_interface.py` using the `openai-whisper` library (e.g., `large-v2` model) with GPU acceleration via PyTorch. This converts the spoken audio into text. Word-level timestamps can optionally be requested for advanced SER alignment or future features.
    *   **Archival (Optional):** User can configure if these temporary user utterance `.wav` files are moved to a permanent archive within the Akashic Record (e.g., `[AKASHIC_RECORD_PATH]/AudioLogs/User/YYYY-MM-DD/`) after processing, linked from the Chronicle entry. This allows for later re-analysis or review but consumes significant disk space. Default might be to delete after STT/SER.
*   **B. Voice Output (AI to User):**
    *   **Text-to-Speech (TTS):** Handled by `tts_interface.py`. After an LLM agent (Sage, Seer, Shaman) generates a text response, this module converts it to audible speech.
    *   **Engine Flexibility:** Supports agent-specific TTS engine selection:
        *   **Piper TTS (CPU):** Called via `subprocess`. Fast, efficient, provides good quality distinct voices using `.onnx` models. Recommended for Sage and Shaman, or as a default.
        *   **Coqui XTTSv2 (GPU/PyTorch - Optional):** Used via the `coqui-tts` library. Offers high-quality voice cloning from speaker WAV samples and potentially more natural prosody. Recommended for Seer if expressive, unique voice is desired and resources permit.
    *   **Output:** Generates audio data (raw bytes or numpy array) and sample rate.
    *   **Playback:** `audio_processing.py` uses `sounddevice` to play the synthesized audio data through the system's default speakers/headphones.

### 6.2. Text Modality

*   **A. Internal Representation:** Text is the primary internal data format for LLM processing. All voice input is converted to text by STT, and all AI-generated thoughts/responses are text before TTS. The Akashic Record (Chronicle, Synthesis Store) primarily stores information in textual or structured text-based formats (JSON, SQLite TEXT fields).
*   **B. GUI Text Input/Output (Future):** The envisioned dedicated OracleAI GUI will provide a traditional chat interface allowing users to type input directly and read AI responses as text, as an alternative or supplement to voice interaction.
*   **C. Document Processing (Future - Shaman Task):** Shaman could be tasked with ingesting, analyzing, and summarizing user-provided text documents (.txt, .md, .pdf via OCR/extraction libraries) to incorporate their content into the Akashic Record.

### 6.3. Vision Modality (Screenshot Analysis)

*   **A. Purpose:** To allow OracleAI agents to "see" and understand the content of the user's current screen, providing crucial context for discussions about on-screen applications, documents, images, or games.
*   **B. Capture Mechanism (`image_processing.py` - Conceptual Module):**
    *   A dedicated function, callable by `main.py` (e.g., triggered by user command "OracleAI, look at my screen," or periodically if configured, or when an agent requests visual context).
    *   Uses a library like `mss` or `Pillow (ImageGrab)` (or `pyautogui` as in original VC, though `mss` is often faster for raw capture) to take a screenshot of the primary display (or a selected display/window in future enhancements).
    *   Saves the screenshot to a temporary image file (e.g., `.png`).
*   **C. Vision Language Model (VLM) Processing:**
    *   The image file (or its base64 encoded data) is sent to a multimodal GGUF model (e.g., Llava, Fuyu, Moondream) running in a **KoboldCpp instance** that is configured for VLM inference.
    *   This is handled by `llm_interface.py`, which would need a specialized function like `generate_with_image(agent_name, prompt_text, image_data, ...)` that constructs the appropriate API payload for KoboldCpp's multimodal endpoint.
    *   **Prompt for VLM:** A generic prompt like "Describe this image in detail, paying attention to any text present." or a more specific prompt based on the conversational context can be used.
*   **D. Output & Integration:**
    *   The VLM returns a textual description of the image content, including any text it could OCR.
    *   This textual description is:
        1.  Logged to the Chronicle as part of the current interaction context.
        2.  Provided to the active AI agent(s) (Sage, Seer, Shaman) as part of their input prompt by the Memory Bank Context Scaler.
        3.  Potentially stored as a structured `Fact` or linked to an `Entity` in the Synthesis Store if deemed significant during memory consolidation.
*   **E. Use Cases:**
    *   Discussing content of web pages, documents, or applications.
    *   Assisting with UI navigation ("Where is the save button in this application?").
    *   Providing context for gaming sessions (as in original VC).
    *   Troubleshooting on-screen errors.

## VII. Interaction Modes & User Control Mechanisms

OracleAI is designed to offer flexible interaction patterns, allowing the user to tailor the AI council's behavior to their current needs and preferences. These modes are managed by `main.py` and can be controlled via voice commands or the future GUI.

### 7.1. Standard Interaction Mode

*   **Description:** The default operational mode for everyday, real-time conversation and assistance.
*   **Active Agents:** Sage and Seer are the primary interactive agents. Their respective KoboldCpp instances are active.
*   **Shaman Status:** Shaman is generally in a background processing state, working on tasks from its queue, or idle. It does not actively participate in real-time conversation unless explicitly invoked within an Oracle Consultation.
*   **Workflow:** Follows the standard "Local User Interaction Cycle" (VAD -> STT -> Emotion Analysis -> Context Scaling -> LLM (Sage/Seer) -> TTS).
*   **User Experience:** Aims for responsive dialogue. Sage provides analytical/strategic input, Seer offers creative/empathetic perspectives. The user can address them individually or pose general queries for the active pair to handle.
*   **AFK Behavior:** If the user is inactive for a period, Sage and Seer may engage in a brief, limited, on-topic discussion based on the last interaction, logging it to the Chronicle. This is less emphasized than in the original VC concept, with more focus on Shaman for deep background work.

### 7.2. Oracle Consultation / Roundtable Mode

*   **Description:** A user-activated collaborative mode designed for intensive brainstorming, multi-faceted problem-solving, or strategic planning sessions where input from all AI agents, including a responsive Shaman, is desired simultaneously with the user.
*   **Activation:** Explicit user command (e.g., "OracleAI, initiate Oracle Consultation on [topic]," "Council, let's hold a roundtable on this issue").
*   **Active Agents:** Sage, Seer, *and* Shaman are all considered active participants.
*   **Shaman Responsiveness Configuration:**
    *   Upon entering this mode, or via a specific command, the user can set Shaman's desired "participation depth" or "latency level" for *this specific consultation session*. This maps to the "Hyperspace Travel" scale (e.g., "Moon," "Mars," "Jupiter").
    *   **Lower Depth (e.g., "Moon"):** Shaman is prompted to provide quicker, more focused contributions, primarily drawing from already synthesized knowledge in the Synthesis Store or performing very rapid analyses. Expected response time: seconds to a few minutes.
    *   **Higher Depth (e.g., "Mars"/"Jupiter"):** Shaman can undertake more involved analysis, query broader sections of the Akashic Record, or initiate short deep searches *during* the consultation. Expected response time: minutes to tens of minutes.
    *   The GUI's Shaman status indicator reflects this chosen depth and estimated response time for its turns.
*   **Turn-Taking & Interaction Flow:**
    *   **User-Defined Order (Option):** User can specify a fixed speaking order (e.g., User -> Sage -> Seer -> Shaman -> User).
    *   **Round-Robin (Default):** A default sequence is followed.
    *   **Hybrid / Intelligent Interjection (Advanced):** While a general order is maintained, agents (especially Seer or Sage if they have a critical point) can be prompted to make brief, relevant interjections. The user can always interrupt or direct the next turn ("Sage, what's your take on Seer's last point?").
*   **AFK Behavior:** If the user is inactive, Sage and Seer can continue their discussion on the current topic, potentially formulating more complex questions or sub-tasks to queue for Shaman (based on its current consultation depth or for later deep processing).
*   **Purpose:** To leverage the combined, synergistic intelligence of the entire council and the user in a dynamic, interactive session.

### 7.3. Shaman Focus Mode (Resource Management)

*   **Description:** A user-activated utility mode designed for systems with VRAM or other resource constraints, allowing the Shaman to utilize maximum available system resources for its computationally intensive, non-real-time tasks.
*   **Activation:** Explicit user command (e.g., "OracleAI, activate Shaman Focus," "Prioritize Shaman for deep analysis").
*   **Mechanism:**
    1.  OracleAI's `main.py` (or a dedicated resource manager module) attempts to gracefully stop the KoboldCpp processes serving the Sage and Seer LLMs (e.g., via `subprocess` calls to send a shutdown signal or by killing the processes if necessary).
    2.  This frees up VRAM and GPU compute resources previously allocated to Sage and Seer.
    3.  The Shaman's KoboldCpp instance can then potentially be reconfigured (manually by user, or automatically by OracleAI if advanced control is implemented) to utilize more GPU layers (`-ngl`) or a larger model if one was pre-configured but not fully loadable alongside Sage/Seer.
*   **User Interaction:** While Shaman Focus is active, real-time interaction with Sage and Seer is unavailable. The user primarily interacts by assigning tasks to Shaman or checking the status of ongoing deep analyses. The GUI clearly indicates this mode.
*   **Deactivation:** User command ("Deactivate Shaman Focus," "Restore council"). OracleAI restarts the KoboldCpp instances for Sage and Seer with their standard configurations.
*   **Purpose:** Enables users on single high-end GPU systems to run very large models or perform extremely demanding computations with Shaman that would otherwise be impossible if Sage and Seer were also consuming significant resources.

### 7.4. Guided Generation & Interaction Refinement

*   **Description:** A suite of user-initiated commands and interaction patterns (inspired by SillyTavern's "Guided Generations") allowing for fine-grained, turn-by-turn control over AI agent responses and the ability to correct or steer conversations.
*   **Implementation (via voice commands and/or GUI buttons/context menus):**
    *   **"Guide Next Response":**
        *   User provides a specific instruction *before* an agent generates its next response (e.g., "Sage, guide: Respond to my last question with only three bullet points, focusing on the financial implications and citing sources from memory if possible.").
        *   This guidance is prepended or strategically injected into the LLM prompt for that agent's turn.
    *   **"Refine Last Response" / "Correction":**
        *   After an agent responds, the user can provide corrective feedback (e.g., "Seer, correction: That analogy is a bit off; try one related to exploration instead, and make the tone more encouraging.").
        *   The system re-prompts the same agent with its *previous response*, the *user's correction/guidance*, and the relevant conversational context, instructing it to generate a revised response.
    *   **"Persistent Session Guides" (Short-Term Contextual Rules):**
        *   User can set temporary rules or focus points for the current interaction session (e.g., "Session Guide: For this Project Nova discussion, always assume a budget constraint of $50k," or "Focus: Prioritize user well-being in all Seer responses for this session.").
        *   These guides are stored temporarily (e.g., in-memory or a session-specific part of `profile.db`) and injected into prompts by the Context Scaler for the duration they are active.
        *   Commands to `add_guide`, `view_guides`, `flush_guide [id]`, `flush_all_guides`.
    *   **"Impersonation" / Structured Output Generation (Primarily for Sage/Shaman):**
        *   User provides a high-level goal or an outline (e.g., "Sage, generate: A risk assessment matrix for Project Nova with columns for Risk, Likelihood, Impact, Mitigation.").
        *   The agent uses its LLM to flesh out this outline into the desired structured output, drawing on its analytical capabilities and memory.
*   **Logging:** All guidance instructions, corrections, and the resulting original/revised AI responses are logged in the Chronicle with appropriate metadata tags (e.g., `guided_generation_instruction`, `user_correction`, `revised_agent_response`) and links between related turns. This provides a clear audit trail of how AI outputs were shaped.

### 7.5. Toggleable States (Mute, Search)

These are persistent states that modify behavior within the primary interaction modes (Standard, Oracle Consultation).

*   **Mute State:**
    *   **Activation:** Voice command ("Mute AI," "Unmute AI") or GUI toggle.
    *   **Behavior:** When active, Sage and Seer (and Shaman if in a responsive part of Consultation mode) will not proactively speak or offer unsolicited TTS output. They will only generate TTS responses if directly addressed or if their turn comes up in a structured Oracle Consultation. They continue to listen, process, and log information.
    *   **Purpose:** Allows the user to silence the AI council without fully stopping their background processing or losing context.
*   **Search Feature State:**
    *   **Activation:** Voice command ("Enable web search," "Disable web search") or GUI toggle. Default state configurable in `.env`.
    *   **Behavior:** When active, before Sage, Seer, or Shaman (if performing a query-driven task) generate a response to a user query that might benefit from external information, the `search_module.py` is invoked. It determines if a search is needed and what type (Simple or Deep), performs it, and the results are fed into the LLM context by the Memory Bank Context Scaler.
    *   **Purpose:** Augments AI knowledge with real-time information from the web.

These interaction modes and control mechanisms aim to provide a rich, flexible, and user-directed experience, allowing OracleAI to adapt to a wide range of tasks and user preferences.

## VIII. Web Connectivity & External Data Integration

OracleAI, while primarily a local-first system, is designed to intelligently and securely interact with external web resources and APIs to augment its knowledge, provide real-time information, and integrate with the user's broader digital ecosystem. All external connectivity is designed to be opt-in, transparent, and managed with user privacy in mind.

### 8.1. Web Search Capabilities (`search_module.py`)

*   **A. Purpose:** To provide Sage, Seer, and Shaman with the ability to access up-to-date information from the internet to answer user queries, support research tasks, and ground their responses in current events or widely available knowledge.
*   **B. Search Engines:**
    *   **Primary Default:** DuckDuckGo (via the `duckduckgo_search` Python library) for its privacy-respecting stance and ease of API-less integration for basic searches.
    *   **Planned Extensibility:** The `search_module.py` will be designed with an abstract interface to support multiple search engines in the future. Users will be able to configure their preferred engine(s) and provide API keys (if required) in the `.env` file. Potential future integrations include:
        *   Brave Search API
        *   Google Custom Search JSON API (requires API key and adheres to usage quotas/costs)
        *   SearXNG instances (user-hosted or public, if reliable)
*   **C. Search Types:**
    1.  **Simple Search:**
        *   **Mechanism:** Retrieves concise text snippets, titles, and URLs from the top search results (e.g., top 3-5 results from DuckDuckGo).
        *   **Use Case:** Quick answers to factual questions, definitions, current events.
        *   **Process:** `search_module.py` calls the chosen search engine's API/library. Results are minimally processed and formatted for inclusion in the LLM prompt by the Memory Bank Context Scaler.
    2.  **Deep Search:**
        *   **Mechanism:** A multi-stage, LLM-assisted process for in-depth investigation:
            *   **Initial Query & Broad Search:** Uses a refined query (potentially LLM-generated based on user need) to get initial search results from one or more configured engines.
            *   **Web Page Scraping & Analysis:** For promising URLs (after checking `robots.txt` for permission), `search_module.py` uses `requests` to fetch page content and `BeautifulSoup4` to parse HTML.
            *   **Content Summarization/Extraction (LLM-assisted):** The text content of scraped pages is fed to an LLM (e.g., Sage's model or a dedicated fast summarization model) to extract key information or generate concise summaries, making it suitable for context injection.
            *   **Recursive Link Exploration (Optional & Controlled):** With user permission or for specific Shaman tasks, the system can follow relevant links found on scraped pages to a limited depth, repeating the scraping/summarization process. This is computationally intensive.
            *   **Reddit Search (PRAW):** Uses the `praw` library to search relevant subreddits (identified by LLM or user) for discussions, opinions, and anecdotal evidence related to the query. Relevant posts and top comments are retrieved and summarized by an LLM.
            *   **Synthesis:** All gathered and summarized information from web pages and Reddit is synthesized by an LLM (Sage or Shaman) into a coherent report or a set of key findings.
        *   **Use Case:** Comprehensive research on a topic, gathering diverse perspectives, in-depth problem analysis. Primarily initiated by Shaman or by explicit user command.
*   **D. Invocation:**
    *   The "Search Feature State" (toggleable) determines if search is active.
    *   If active, `main.py` (before calling an agent's LLM for a user query) can invoke `search_module.py`. An initial LLM call (fast model) might be used to determine *if* a search is needed and what *type* (Simple/Deep) is most appropriate for the user's query.
    *   Agents can also explicitly request searches as part of their internal processing or task execution.
*   **E. Proxy Support & Anonymity:**
    *   Users can configure OracleAI (via `.env`) to route all outgoing HTTP/HTTPS requests from `search_module.py` (and potentially other modules making web calls) through:
        *   **TOR SOCKS Proxy:** (e.g., `socks5h://127.0.0.1:9050` if TOR Browser or daemon is running). Requires `requests[socks]`.
        *   **Standard HTTP/HTTPS Proxy:** User-specified proxy server.
        *   **System-Level VPN:** If the host OS is configured to use a VPN, all OracleAI traffic will route through it.
    *   This enhances user privacy when performing web searches or scraping.

### 8.2. Calendar Integration (`calendar_interface.py` & `calendar.db`)

*   **A. Purpose:** To connect OracleAI with the user's personal/professional schedule, enabling proactive reminders, contextual awareness of commitments, and integration of temporal information into planning and memory analysis.
*   **B. Supported Services (Initial & Planned):**
    *   **Google Calendar:** Via Google Calendar API and OAuth 2.0.
    *   **Microsoft Outlook Calendar:** Via Microsoft Graph API and OAuth 2.0.
    *   **CalDAV (Future):** Support for open CalDAV servers.
    *   **ICS File Import (Future):** Ability to import static `.ics` calendar files.
*   **C. Authentication & Authorization:**
    *   Uses **OAuth 2.0** for secure, user-consented access to calendar data.
    *   OracleAI will guide the user through a one-time browser-based authentication flow for each calendar service they wish to connect.
    *   Refresh tokens are securely stored (e.g., encrypted in `profile.db` or using OS credential stores) to maintain access without repeated logins. Access tokens are used for API calls.
*   **D. Synchronization & Local Cache (`calendar.db`):**
    *   `calendar_interface.py` periodically (e.g., every 15-60 minutes, configurable, via `apscheduler`) syncs events from the configured external calendars.
    *   Fetched events (title, description, start/end times, attendees, location, recurrence) are parsed and stored in the local SQLite `calendar.db` (SQLCipher encrypted).
    *   Uses API-specific mechanisms for efficient synchronization (e.g., `syncToken` for Google Calendar) to fetch only changed/new events after the initial full sync.
    *   Handles timezones correctly, storing all event times in UTC in the database while retaining original timezone information.
*   **E. Integration & Usage:**
    *   **Context for LLMs:** The Memory Bank Context Scaler queries `calendar.db` for upcoming events (e.g., today, next 24/48 hours) or past events relevant to the current discussion (e.g., by keyword in title/description or attendee match). This information is formatted and included in prompts for Sage/Seer/Shaman.
    *   **Proactive Reminders:** Sage or a dedicated notification system can provide reminders for upcoming meetings or deadlines based on `calendar.db` data.
    *   **Planning Assistance (Sage):** Sage uses calendar data to check user availability when scheduling tasks or proposing timelines.
    *   **Memory Correlation (Shaman):** Shaman analyzes `calendar.db` data alongside Chronicle logs and Synthesis Store entries to find correlations (e.g., "User sentiment tends to be lower on days with back-to-back meetings," "Project X progress often stalls before major deadlines noted in calendar").
    *   **User Queries:** Users can ask OracleAI about their schedule ("What's on my agenda for tomorrow?", "When is my meeting with John Doe?").

### 8.3. Other Potential External Data Integrations (Future)

*   **A. Personal Knowledge Management (PKM) Tools:**
    *   APIs for Obsidian, Logseq, Notion, Roam Research to allow OracleAI to read from (and potentially write to, with caution) the user's existing notes and knowledge bases. This would deeply integrate OracleAI with the user's "second brain."
*   **B. Task Management Services:**
    *   APIs for Todoist, Trello, Asana, Jira to sync tasks between OracleAI's Task Queue and the user's preferred external task manager.
*   **C. Document Repositories:**
    *   APIs for Google Drive, Dropbox, OneDrive to allow Shaman to access and analyze user-specified documents for research or memory augmentation.
*   **D. News/RSS Feeds:**
    *   Allow users to configure RSS feeds or news APIs. Shaman could monitor these for topics relevant to user interests or ongoing projects, providing summaries or alerts.
*   **E. Code Repositories (GitHub/GitLab):**
    *   For developer users, allow Shaman to analyze code, track project progress, or summarize commit histories from specified repositories.

All such future integrations must adhere strictly to the principles of user consent, data minimization, and secure authentication.

## IX. Remote Access Architecture & API Design

OracleAI is designed to be accessible not only on the host machine but also from remote client devices (e.g., smartphone, tablet, other computers) via a secure and well-defined API.

### 9.1. Server-Side (OracleAI Host Machine)

*   **A. FastAPI Application (`remote_api.py`):**
    *   A robust, asynchronous web server built using FastAPI.
    *   **Runs Locally:** Launched by `main.py` using Uvicorn as the ASGI server.
    *   **Binding:** Defaults to `127.0.0.1` (localhost) for security. User must explicitly configure it to `0.0.0.0` or a specific network interface IP to allow network access.
    *   **Asynchronous Operations:** Leverages FastAPI's `async` capabilities to handle multiple client requests efficiently without blocking the main OracleAI processing threads where possible. Synchronous blocking operations (like some LLM calls or CPU-bound tasks) are run in thread pools using `await asyncio.to_thread(...)`.
*   **B. Core API Endpoints (Illustrative):**
    *   **Authentication (Future):** `/auth/token` (POST) - For API key or JWT-based authentication if implemented.
    *   **Chat Interaction:**
        *   `POST /v1/chat/interaction`: Main endpoint for sending user input and receiving AI responses.
            *   *Request Body (Pydantic Model):* `{ "user_text": "...", "session_id": "optional_uuid", "agent_preference": "sage" | "seer" | "auto", "emotion_data_client": { ... } (optional, if client does SER/Sentiment) }`
            *   *Processing:* Orchestrates STT (if audio sent), Emotion Analysis, Context Scaling, LLM call, TTS (if audio response desired), logging.
            *   *Response Body (Pydantic Model):* `{ "agent_response_text": "...", "agent_name": "sage" | "seer", "emotion_data_server": { ... }, "turn_id": "uuid", "session_id": "uuid" }` (or audio stream).
    *   **STT Service (Optional):**
        *   `POST /v1/stt/transcribe`: Accepts audio file upload, returns transcribed text.
            *   *Request:* Multipart form data with audio file.
            *   *Response:* `{ "text": "...", "timestamps": [...] }`
    *   **TTS Service (Optional):**
        *   `POST /v1/tts/synthesize`: Accepts text and agent config, returns audio data.
            *   *Request:* `{ "text": "...", "agent_name": "sage", "voice_preference": "..." }`
            *   *Response:* Audio file stream (e.g., `audio/wav`).
    *   **System & Agent Status:**
        *   `GET /v1/status`: Returns overall system status, active agents, Shaman task overview.
        *   `GET /v1/agents/{agent_name}/status`: Status for a specific agent.
    *   **Memory Access (Future - Granular & Secure):**
        *   `GET /v1/memory/summaries?date=YYYY-MM-DD&type=daily`
        *   `POST /v1/memory/search` (with query, returns relevant snippets)
        *   `POST /v1/memory/permanent` (to add a permanent memory item)
    *   **Task Management (Future):**
        *   `POST /v1/tasks` (to create a new task for Shaman/agents)
        *   `GET /v1/tasks/{task_uuid}` (to get task status/results)
*   **C. Data Validation:** Uses Pydantic models for strong typing and validation of API request and response bodies.
*   **D. Security:**
    *   **Authentication (Future):** Implement robust authentication for external access (e.g., bearer tokens/API keys).
    *   **HTTPS:** If exposed directly to the internet (not recommended), Uvicorn should be run behind a reverse proxy like Nginx or Caddy configured for HTTPS. Tailscale handles encryption automatically.
    *   **Input Sanitization:** Although LLMs handle varied input, basic validation is performed by Pydantic.

### 9.2. Client-Side (User's Remote Device - *Not provided by OracleAI core*)

*   **A. Nature:** A separate application (web app, mobile app, desktop app, or even another script) developed by the user or a third party.
*   **B. Recommended Client Architecture for Best Experience:**
    1.  **Local STT:** Utilize the remote device's built-in STT capabilities (e.g., iOS/Android native STT, browser Web Speech API) to convert user speech to text *on the device*.
    2.  **API Communication:** Send the transcribed text (and optionally client-side detected emotion data if available) to the OracleAI FastAPI server's `/v1/chat/interaction` endpoint via HTTPS.
    3.  **Local TTS:** Receive the AI's text response from the API and use the remote device's built-in TTS engine or a web TTS service to synthesize speech *on the device*.
    *   **Rationale:** This minimizes audio data transmission over the network, reduces latency, leverages powerful device-native STT/TTS, and enhances privacy by keeping raw audio local to the client device.
*   **C. Alternative Client Architecture (Higher Latency/Bandwidth):**
    1.  Client records audio, sends raw audio to OracleAI's `/v1/stt/transcribe` endpoint.
    2.  Client receives text, sends text to `/v1/chat/interaction`.
    3.  Client receives AI text, sends text to `/v1/tts/synthesize`.
    4.  Client receives audio data, plays it.
    *   This is less optimal but provides a fallback if the client device lacks good local STT/TTS.

### 9.3. Networking for External Access

*   **A. Local Area Network (LAN):**
    *   If the OracleAI host and client device are on the same LAN, the client can connect directly using the host's local IP address (e.g., `http://192.168.1.100:8000`) provided the FastAPI server is configured to bind to `0.0.0.0` or the LAN IP.
*   **B. Secure External Access (Highly Recommended):**
    1.  **Tailscale / ZeroTier:** These mesh VPN solutions create a secure, private network overlay connecting your devices wherever they are, without needing complex firewall configurations or exposing ports directly to the internet. The client connects to OracleAI using its Tailscale/ZeroTier IP address. This is the simplest and most secure method for personal remote access.
    2.  **Self-Hosted VPN:** Set up a VPN server (e.g., WireGuard, OpenVPN) on your home network. The remote client connects to the VPN and can then access OracleAI as if it were on the LAN.
    3.  **Port Forwarding + HTTPS + Authentication (Advanced, Higher Risk):** Configure your router to forward an external port to the OracleAI host's FastAPI port. **Requires** setting up HTTPS (e.g., with Let's Encrypt via a reverse proxy like Nginx/Caddy) and implementing strong API authentication in FastAPI. This method exposes a service directly to the internet and carries more security risks if not configured perfectly.

This robust remote access architecture, centered around a FastAPI server and recommending secure tunneling for external connections, allows users to leverage their OracleAI council from various devices while maintaining control and privacy.

## X. User Interface (UI) Concept, Aesthetic, and Iconography

While OracleAI's core functionalities can be accessed via a command-line interface or a basic API client, a dedicated Graphical User Interface (GUI) is envisioned to provide a rich, immersive, intuitive, and thematically coherent user experience. The GUI will be the primary means for local interaction, configuration, memory management, and visualizing the AI council's activities.

### 10.1. Overall Aesthetic Vision & Thematic Cohesion

*   **Theme:** "Oracle/Mystic Temple" meets "Advanced Geometric Circuitry." The aesthetic aims to evoke a sense of interacting with an ancient, wise, yet technologically advanced intelligence. It should feel profound, personalized, and trustworthy.
*   **Influences:** Art Deco (symmetry, radiating motifs, metallic accents), Ancient Egyptian (symbolism, grandeur, lapis/gold), Venetian (intricate patterns, mask-like elements, rich colors), and high-tech "datascapes" (glowing circuits, energy flows, abstract data representations).
*   **Color Palettes (Primary):**
    *   **Global Base:** Deep indigos, charcoals, near-blacks for backgrounds, creating a sense of depth or the "void" of the DataSide.
    *   **Global Accents:** Art Deco golds (e.g., `#B08D57`), bronzes (`#CD7F32`), and ivories/creams for highlights, borders, and important UI frames.
    *   **Sage (Ice):** Cool blues (e.g., Lapis Lazuli `#26619C`), cyans (`#00FFFF`), silvers (`#C0C0C0`), and whites. Evokes clarity, logic, ice, winter.
    *   **Seer (Fire):** Warm reds (e.g., Carnelian `#B33A3A`, Venetian Deep Red `#990000`), oranges (`#FF8C00`), magentas (`#FF00FF`), and golds. Evokes passion, creativity, fire, summer.
    *   **Shaman (Deep Brain):** Deep indigos (`#4B0082`), cosmic purples (`#8A2BE2`), starlight silver, with occasional flashes of electric blue (`#007FFF`) or profound gold from the "DataSide" stream. Evokes mystery, depth, the cosmos.
*   **Motifs & Patterns:**
    *   **Geometric Circuits:** The foundational visual language. Intricate, clean lines forming pathways, component outlines, and background textures.
    *   **Radiating Lines/Sunbursts (Art Deco):** Used for Shaman's active state, highlighting important information, or as focal points.
    *   **Hexagonal Grids:** Can form subtle background layers or represent data structures.
    *   **Stylized Esoteric Symbols:** Geometric interpretations of Eye of Horus, Ankh, Lotus, Merkaba, etc., used as icons or decorative elements.
    *   **Latticework/Tracery (Venetian):** Inspires more ornate circuit patterns or decorative borders.
    *   **Stepped Forms & Chevrons (Art Deco):** Influence UI panel shapes, dividers, and accents.
    *   **Symmetry:** A guiding principle for layout and agent representations.

### 10.2. Key GUI Components & Layout (Conceptual)

A multi-panel desktop application is envisioned.

*   **A. Main Interaction Panel (Central Area):**
    *   **Chat Log Display:** Primary area for displaying the conversation history.
        *   Distinct visual styling for User, Sage, Seer, and Shaman turns (e.g., color-coded chat bubbles/backgrounds, unique avatar icons next to each message).
        *   Supports formatted text (Markdown for lists, bolding, etc.), and potentially inline display of small images or links.
        *   Timestamps for each message.
    *   **User Input Area:**
        *   Multiline text box for typed input.
        *   Clear "Send" button.
        *   Microphone toggle button with visual feedback for voice input (e.g., pulsing wave when listening).
        *   Access to "Guided Generation" command palette/buttons (see 10.2.F).
*   **B. Agent Status & Control Panel (Likely a Sidebar or Top Bar):**
    *   **Active Agent Display:** Clearly shows which agent(s) (Sage, Seer, Shaman) are currently active or speaking.
    *   **Agent Avatars:** Displays the avatar for each primary agent.
        *   *Sage:* Geometric, cool-colored, perhaps inspired by Image 2 (right side) or a stylized Thoth/Athena.
        *   *Seer:* Geometric, warm-colored, perhaps inspired by Image 2 (left side) or a stylized Pythia/Morgana.
        *   *Shaman:* The intricate, unmasked figure from Image 1.
        *   Avatars could have subtle animations (e.g., glowing eyes when speaking, energy patterns).
    *   **Mode Indicators:** Displays current Interaction Mode (Standard, Oracle Consultation, Shaman Focus) and toggleable states (Mute, Search).
    *   **Agent-Specific Controls (Contextual):** When an agent is selected or active, might show quick access to their temperature override or specific common commands.
*   **C. Shaman "Hyperspace Travel" Dashboard (Dedicated Panel or Modal):**
    *   **Visual Indicator:** A prominent golden Merkaba icon traveling along a stylized path of celestial bodies (Earth Orbit -> Moon -> Mars -> Jupiter -> Saturn -> Uranus -> Neptune -> Pluto -> Kuiper Belt -> Heliopause -> Oort Cloud). Position reflects estimated progress/latency.
    *   **Task Display:** Shows the current task Shaman is working on (from `tasks.db`).
    *   **Estimated Time Remaining:** Displays a thematic "travel time" (e.g., "Journey to Mars: ~45 mins remaining").
    *   **Mode/Depth Indicator:** Shows Shaman's current operational mode (e.g., "Deep Chronicle Analysis," "Pattern Weaving") and configured depth if in Oracle Consultation.
    *   **Background Visuals:** Dynamic "DataSide" effects when Shaman is active (flowing energy, Matrix/symbol rain, chameleon particles).
*   **D. Contextual Information Sidebars/Dashboards (Toggleable Panels):**
    *   **Emotional Readout Panel:**
        *   Displays real-time (or per-turn) user emotional data:
            *   SER dominant emotion icon/label + confidence.
            *   VADER compound score gauge/bar.
            *   TextBlob polarity/subjectivity gauges.
            *   Dominant NRCLex emotions list.
        *   Could show a mini-trend graph for recent sentiment.
    *   **Akashic Record Quick Access Panel:**
        *   "On This Day" memory snippets from past years.
        *   Recently accessed/modified Entities or Summaries.
        *   Quick search bar for the Akashic Record.
    *   **Task Queue Overview Panel:** Summarized list of pending, active, and recently completed tasks from `tasks.db`, especially for Shaman.
    *   **Calendar Snippet Panel:** Displays today's and tomorrow's key events from `calendar.db`.
*   **E. System Settings & Configuration Module (Accessible via Gear Icon):**
    *   User-friendly interface for editing settings currently in the `.env` file (values are written back to `.env` or an overriding user-specific config file).
    *   Sections for:
        *   General App Settings (Paths, Logging).
        *   KoboldCpp API Endpoints.
        *   STT/TTS Model Selection & Paths (Piper voices, XTTS speaker WAVs).
        *   SER Model Configuration.
        *   Agent Personalization (Default temperatures, TTS engine choice per agent).
        *   Akashic Record (Database paths, backup settings, RAG parameters for Context Scaler).
        *   Web Search & Proxy Settings.
        *   Calendar API Connections (manage authenticated accounts, sync interval).
        *   Remote API Server Settings (host, port, future auth keys).
        *   Privacy & Security (Master password change for SQLCipher - complex, telemetry opt-in).
*   **F. Guided Generation Palette/Menu:**
    *   Accessible from the user input area (e.g., a dedicated button or right-click menu).
    *   Provides quick access to commands like "Guide Next Response," "Refine Last Response," "Set Session Guide," "Add Note to Chronicle."
    *   Input fields appear for providing the guidance text.
*   **G. Akashic Record Management Interface (Future - Major Feature):**
    *   A dedicated section or separate window for browsing, searching, viewing, and potentially editing the contents of the Akashic Record.
    *   **Chronicle Viewer:** Display raw logs, filterable by date, speaker, tags.
    *   **Synthesis Store Browser:** View Entities, Facts/Decisions, Summaries, Project Threads. Allow navigation via relationships.
    *   **Editor:** Secure and careful editing of verified summaries or entity details (with warnings about data integrity and potential need for re-indexing/re-embedding).
    *   **Collaborative Reflection Interface:** A guided UI for the daily memory consolidation process.
*   **H. Backup & Restore Controls:** Simple interface to trigger the 7-Zip backup (encrypted/unencrypted) and guide through restoring from an archive.

### 10.3. Iconography

A custom set of icons will be developed, adhering to the geometric, circuit-line style with thematic influences. All icons should be clear, scalable, and visually consistent.

*   **Brain (Stylized, Geometric):** LLM Processing, Agent Thinking, Cognitive Tasks.
*   **Heart (Stylized, Circuit-infused):** Emotion, Sentiment, User Profile, Empathy.
*   **Eye (Geometric, Eye of Horus inspired):** Vision, Perception, Search, Observation, Monitoring.
*   **Network/Plexus (Interconnected Hexagons/Nodes):** Connectivity, Relationships, Knowledge Graph, Data Flow, API Connections.
*   **Audio Wave (Geometric):** STT, TTS, Microphone, Speaker.
*   **Delta/Triangle (Stylized):** Core Agent representation, Action buttons, Focus indicator.
*   **Chart/Graph (Geometric Bars/Lines):** Data Analysis, Trends, Reports, Statistics.
*   **Gear (Geometric):** Settings, Configuration.
*   **Scroll/Book/Tablet (Stylized):** Akashic Record, Chronicle, Summaries, Knowledge.
*   **Calendar/Clock (Stylized):** Calendar Integration, Scheduling, Time-related info.
*   **Key/Ankh (Stylized):** Security, Access, Permanent Memory, Core Principles.
*   **Merkaba/Star (Stylized):** Shaman, Deep Processing, Hyperspace Travel.
*   **Moon, Mars, Jupiter, etc. (Stylized Planetary Icons):** For Shaman's latency indicator.
*   **Search/Magnifying Glass (Stylized Eye variant):** Web Search.
*   **Cloud/Connection (Stylized):** Remote Access Status.
*   **Lock (Stylized):** Encryption, Security.
*   **Save/Archive (Stylized Disk/Chest):** Backup, Memory Saving.

Color coding within icons or their active states will align with agent themes or status (e.g., green for active, red for error).

### 10.4. Typography

Font choices will balance readability with the desired aesthetic.

*   **Primary UI Text (Labels, Buttons, Body):** A clean, highly readable sans-serif with a subtle modern or technical feel.
    *   *Candidates:* Titillium Web, Exo 2, Roboto, Open Sans, Fira Sans.
*   **Titles & Major Headers (OracleAI Name, Agent Names, Section Titles):** An elegant serif with classical inspiration or a distinctive geometric/Art Deco display sans-serif.
    *   *Candidates:* Cinzel, Trajan Pro (for very formal), Audiowide, Electrolize, Orbitron (used sparingly).
*   **Data Readouts & Logs (Chronicle View, Debug Info):** A clear monospaced font.
    *   *Candidates:* Source Code Pro, Fira Code, Consolas.
*   **Esoteric Accents (Optional, very limited use):** A highly stylized font hinting at runes or ancient scripts for purely decorative elements or background textures, *not* for readable text.

Font weights and styles (bold, italic) will be used hierarchically to guide the eye and emphasize information. All fonts must be properly licensed for application distribution.

This UI concept aims to create an experience that is not only functional but also deeply immersive and aligned with the profound capabilities and thematic identity of OracleAI.

## XI. Privacy, Security, and Data Management Strategy

The design and operation of OracleAI are fundamentally rooted in respecting and protecting user privacy and ensuring the security and integrity of their personal data, especially the contents of the Akashic Record. This section details the multi-layered strategy to achieve these goals.

### 11.1. Foundational Principle: Local-First Processing and Data Sovereignty

*   **A. Core Mandate:** All primary AI computations, including LLM inference (via KoboldCpp), Speech-to-Text (STT via `openai-whisper`), primary Text-to-Speech (TTS via Piper/XTTSv2), Speech Emotion Recognition (SER), Text Sentiment Analysis, and all operations on the Akashic Record (storage, retrieval, synthesis), **must** occur exclusively on hardware controlled by the user.
*   **B. Data Residency:** The entirety of the user's Akashic Record (Chronicle logs, Synthesis Store databases, Calendar Cache, User Profile, Task Queue) **must** be stored locally on the user's device(s). No personal conversational data, memory content, or derived insights are transmitted to any external servers or third parties without explicit, informed, and granular user consent for specific, user-initiated actions (e.g., syncing with an external calendar API, performing a web search, creating an encrypted backup to a user-specified cloud storage).
*   **C. Rationale:** This local-first approach is non-negotiable. It provides the user with maximum privacy, data sovereignty, control over their information, and ensures core functionality remains available offline. It mitigates risks associated with cloud service data breaches, unauthorized third-party access, changes in vendor terms of service, service discontinuation, or internet connectivity issues.

### 11.2. Data Encryption Strategies

A multi-layered encryption approach is employed to protect data both at rest and, where applicable, in transit (though local transit is less of a concern than external).

*   **A. OS-Level Full Disk Encryption (FDE) - User Responsibility, Strongly Recommended:**
    *   OracleAI documentation will strongly advise users to enable FDE on the operating system drive where OracleAI and its data are installed.
    *   *Tools:* BitLocker (Windows Pro/Enterprise), FileVault (macOS), LUKS (Linux).
    *   *Benefit:* Provides a foundational layer of protection for all data on the disk if the physical device is lost or stolen.
*   **B. Application-Level Database Encryption (Mandatory):**
    *   All SQLite databases within the Akashic Record (`synthesis.db`, `calendar.db`, `profile.db`, `tasks.db`) **must** be encrypted using **SQLCipher**.
    *   *Implementation:* Utilize Python bindings for SQLCipher (e.g., `pysqlcipher3` or a similar well-maintained library).
    *   *Key Management:*
        1.  OracleAI will require the user to set a strong **Master Password** during initial setup.
        2.  This password will be used to derive an encryption key for SQLCipher (e.g., using PBKDF2 with a strong salt stored in the application's secure configuration area).
        3.  At startup, OracleAI will prompt the user for this Master Password to decrypt and access the databases.
        4.  Consideration for securely caching the derived key in memory *only while the application is running and unlocked*, with mechanisms to clear it upon locking or exit.
        5.  Future: Explore integration with OS-level secure credential stores (Windows Credential Manager, macOS Keychain, Linux Keyring) to manage the master key or derived key, potentially reducing direct password prompts after initial setup if the OS store is unlocked.
*   **C. Application-Level File Encryption (Chronicle Logs - Optional Enhancement):**
    *   Raw Chronicle `.jsonl` files can optionally be encrypted using symmetric AES-256 (via the `cryptography` Python library) using a key derived from the same Master Password.
    *   *Trade-off:* Adds significant security if the OS is compromised while running and FDE is bypassed, but increases complexity and I/O overhead for appending new log entries (requiring decryption of a trailing block or re-encryption) and for reading logs (requiring full or partial decryption).
    *   *Decision:* Implement as a user-configurable option, defaulting to off. Primary reliance for Chronicle files will be OS FDE and encrypted backups.
*   **D. Backup Encryption (Mandatory Feature):**
    *   The integrated 7-Zip backup feature (`backup_module.py`) **must** support strong AES-256 encryption for exported Akashic Record archives.
    *   OracleAI will prompt the user for a separate backup password (can be the same as the master password or different) when creating an encrypted archive.
    *   The 7-Zip command will use appropriate flags (e.g., `-p{password} -mhe=on` to encrypt file headers).
*   **E. Secure Configuration Storage (`.env` and API Credentials):**
    *   The `.env` file, containing paths and non-secret settings, should have its permissions restricted by the user at the OS level.
    *   **API Keys & OAuth Tokens (Calendar, Reddit, etc.):**
        1.  These **must not** be stored in plaintext in the main `.env` file if it's potentially shared or less secured.
        2.  **Preferred Method:** Store them encrypted within the `profile.db` (which is itself SQLCipher encrypted) using the OracleAI master key, or utilize OS-level secure credential stores (`keyring` library).
        3.  If stored in `.env` for simplicity during initial development, this must be clearly documented as a temporary measure with strong warnings.

### 11.3. Network Security & Communication

*   **A. Local Network Communication (KoboldCpp, Internal):**
    *   Communication between OracleAI Python processes and local KoboldCpp instances is via HTTP. Assumed to be on a trusted local network or localhost.
    *   If KoboldCpp instances are run on different machines on the LAN, users should ensure their LAN is secured.
*   **B. Remote Access API (FastAPI Server - `remote_api.py`):**
    *   **Default Binding:** The FastAPI server **must** default to binding to `127.0.0.1` (localhost), making it inaccessible from the network by default.
    *   **Network Exposure:** Users must explicitly change the binding address (e.g., to `0.0.0.0` or a specific LAN IP) in the configuration to enable network access, with clear warnings about security implications.
    *   **Authentication (Mandatory for Network Exposure):** If the API is bound to a non-localhost address, robust authentication **must** be implemented. Options:
        *   API Keys (simple to implement, passed in headers).
        *   JWT (JSON Web Tokens) for session-based authentication.
    *   **HTTPS (Mandatory for Internet Exposure):** If the API is ever exposed directly to the internet (strongly discouraged in favor of tunnels), Uvicorn **must** be run behind a reverse proxy (Nginx, Caddy) configured for HTTPS with valid SSL/TLS certificates (e.g., from Let's Encrypt).
*   **C. Secure Tunneling for External Access (Recommended Practice):**
    *   Documentation will strongly recommend users employ secure tunneling solutions like **Tailscale** or **ZeroTier** (or a self-hosted VPN like WireGuard/OpenVPN) for accessing the OracleAI API from outside their local network. These solutions create encrypted private networks, negating the need for direct internet exposure of the API server.
*   **D. External API Calls (Search, Calendar, etc.):**
    *   All outgoing API calls made by OracleAI **must** use HTTPS.
    *   Validate SSL certificates to prevent man-in-the-middle attacks.

### 11.4. Data Minimization & Transparency

*   **A. Opt-In for External Services:** All features requiring interaction with external APIs (Web Search, Calendar Sync, Reddit) are strictly opt-in and must be explicitly configured/enabled by the user.
*   **B. Minimal Data Transmission:** When interacting with external APIs, OracleAI will send only the minimum data necessary to perform the requested function (e.g., only the search query, only necessary calendar sync parameters).
*   **C. Transparency in Data Usage:**
    *   Clear documentation and in-application information (e.g., tooltips, help sections) will explain what data is being collected, how it's stored, how it's used by the AI agents, and what data (if any) is sent to external services for opt-in features.
    *   The Chronicle log itself provides a degree of transparency into AI processing if "thought" logging is enabled.

### 11.5. No Unauthorized Telemetry or Data Collection
*   OracleAI will **not** collect or transmit any usage statistics, crash reports, performance data, memory content, or any other form of telemetry to any central server or third party without explicit, granular, clearly explained, and revocable opt-in consent from the user.
*   Any opt-in telemetry feature must ensure data is fully anonymized before transmission, and its purpose (e.g., improving open-source models, bug fixing) must be transparent. Default is **NO telemetry**.

### 11.6. User Control Over Data & Memory
*   **A. Akashic Record Management:**
    *   Users will have mechanisms (initially via commands, eventually via GUI) to review, search, and (with safeguards) edit or delete entries within their Synthesis Store.
    *   The Chronicle is immutable, but users can choose to delete entire daily log files.
    *   The backup feature allows users to create full, portable copies of their Akashic Record.
*   **B. Configuration Control:** Users control all key settings, including which agents are active, their parameters, which external services are enabled, and privacy-related toggles.

### 11.7. Secure Software Development Practices
*   Use parameterized queries for all SQLite database interactions to prevent SQL injection vulnerabilities.
*   Validate and sanitize user inputs where appropriate, especially for paths or commands passed to `subprocess`.
*   Keep dependencies updated and be aware of security vulnerabilities in third-party libraries.
*   Minimize attack surface by running with least privilege where possible.

This comprehensive privacy and security strategy aims to make OracleAI a trusted local steward of the user's most personal information and interactions.

## XII. Installation, Configuration, and Deployment

This section provides a detailed guide for setting up OracleAI. Due to its reliance on multiple external tools and specific Python dependencies (notably PyTorch with CUDA), the installation process requires careful attention to detail.

### 12.1. System Prerequisites (Elaborated)

*   **A. Operating System:**
    *   **Windows:** Windows 10 (64-bit, version 1909 or later) or Windows 11 (64-bit).
    *   **Linux:** Modern distribution with glibc 2.28 or later (e.g., Ubuntu 20.04 LTS+, Fedora 36+, Debian 11+).
    *   **macOS:** macOS 12.0 (Monterey) or later. Apple Silicon (M1/M2/M3) support depends on the full compatibility of all Python dependencies, especially PyTorch (Metal Performance Shaders - MPS). GPU acceleration for STT/SER on Apple Silicon will utilize MPS if PyTorch is correctly configured.
*   **B. Python:**
    *   Version: **3.11.x** is the target. Other 3.9+ versions might work but are not officially supported or tested.
    *   Installation: Download from [python.org](https.www.python.org/downloads/). During installation, **ensure "Add Python to PATH" (or equivalent) is selected.**
    *   Verification: `python --version` and `pip --version` in terminal.
*   **C. Git:**
    *   Required for cloning the OracleAI repository (and potentially some Python dependencies if installed from source).
    *   Installation: Download from [git-scm.com](https://git-scm.com/downloads).
*   **D. NVIDIA GPU & Drivers (for GPU Acceleration):**
    *   **GPU:** An NVIDIA GPU with CUDA compute capability 3.7 or higher is required for PyTorch GPU support. For good performance with LLMs and Whisper `large-v2`, a GPU with at least 8GB VRAM is a practical minimum, with 12GB+ recommended (see Hardware section for details).
    *   **Drivers:** Install the latest stable NVIDIA drivers for your GPU from the [NVIDIA website](https.www.nvidia.com/Download/index.aspx). Outdated drivers are a common source of issues.
*   **E. CUDA Toolkit (for NVIDIA GPU Acceleration):**
    *   **Requirement:** PyTorch GPU builds are compiled against specific CUDA Toolkit versions. You must install a CUDA Toolkit version on your system that is compatible with the PyTorch version OracleAI will use.
    *   **Determining Version:** Check the PyTorch installation command generated at [pytorch.org](https://pytorch.org/get-started/locally/) – it will specify the CUDA version (e.g., `cu118` for CUDA 11.8, `cu121` for CUDA 12.1).
    *   **Installation:** Download the matching CUDA Toolkit installer from the [NVIDIA Developer CUDA Toolkit Archive](https://developer.nvidia.com/cuda-toolkit-archive). Install the full toolkit or the necessary runtime components.
    *   **Verification:** After installation, `nvcc --version` in a terminal should display the installed CUDA version.
*   **F. Audio Input/Output Libraries (PortAudio):**
    *   `pyaudio` (a core dependency) requires the PortAudio library.
    *   **Windows:** Often the trickiest.
        1.  Try installing `pyaudio` via pip first. If it fails with missing PortAudio headers/libs, you may need to:
        2.  Download precompiled PortAudio DLLs (e.g., from a trusted source providing builds for Windows or from a package like `Miniconda` if you were using it, though we aim for `venv`). Ensure the DLL (e.g., `portaudio_x64.dll`) is in your system PATH or alongside your Python executable.
        3.  Alternatively, some users find success installing `pyaudio` from unofficial wheels (e.g., from Christoph Gohlke's Unofficial Windows Binaries page, though use with caution).
    *   **Linux:** Typically installed via package manager: `sudo apt-get install portaudio19-dev libasound2-dev` (Debian/Ubuntu) or `sudo yum install portaudio-devel alsa-lib-devel` (Fedora/CentOS).
    *   **macOS:** `brew install portaudio`.
*   **G. 7-Zip Archiver:**
    *   Required for the integrated encrypted backup feature.
    *   Installation: Download and install from [7-zip.org](https://www.7-zip.org/).
    *   **PATH Configuration:** Ensure the directory containing `7z.exe` (Windows) or `7z` (Linux/macOS) is added to your system's PATH environment variable, OR provide the full absolute path to the executable in the OracleAI `.env` configuration file (`SEVENZIP_PATH`).
*   **H. C++ Build Tools (Recommended, may be required for some dependencies):**
    *   Some Python packages with C/C++ extensions might need to be compiled from source during `pip install` if precompiled wheels are not available for your specific Python version/OS/architecture.
    *   **Windows:** Install "C++ build tools" via the Visual Studio Installer (select "Desktop development with C++" workload).
    *   **Linux:** Install `build-essential` (Debian/Ubuntu) or `groupinstall "Development Tools"` (Fedora/CentOS).
    *   **macOS:** Install Xcode Command Line Tools: `xcode-select --install`.

### 12.2. External Tool Dependencies & Setup (User Responsibility)

OracleAI relies on these powerful external tools, which the user must download, install (if applicable), and configure separately. OracleAI then interacts with them, typically via API calls or `subprocess`.

*   **A. KoboldCpp (LLM/VLM Serving):**
    1.  **Download:** Obtain the latest release executable of KoboldCpp suitable for your OS (Windows `.exe`, Linux binary, macOS binary) from the official KoboldCpp GitHub repository or a trusted source.
    2.  **GGUF Models:** Download the GGUF-formatted LLM and VLM models you intend to use for Sage, Seer, and Shaman (e.g., from Hugging Face). Store them in a well-organized directory.
    3.  **Running Instances:**
        *   You will need to run one or more instances of KoboldCpp. Each instance will serve one model.
        *   If Sage, Seer, and Shaman use different models, you'll need three KoboldCpp instances (or one instance if it supports loading multiple models and routing, though separate instances are often simpler for distinct configurations).
        *   If running on multiple PCs, ensure network accessibility between the OracleAI host and the KoboldCpp machines.
        *   **Launch Command Example (Basic):**
            ```bash
            koboldcpp.exe --model /path/to/your/model.gguf --port 5001 --host 0.0.0.0 --usecublas # (or --useclblast)
            ```
            Adjust `--port` for each instance. Use `--host 0.0.0.0` if KoboldCpp is on a different machine on your LAN than OracleAI.
        *   **GPU Offloading (`-ngl`):** Crucially, configure the number of model layers to offload to the GPU using the `-ngl XX` flag (e.g., `-ngl 35`). This value depends on the model size and your available VRAM. Experiment for optimal performance.
        *   **API Enablement:** Ensure KoboldCpp's web API is enabled (usually default). Note the full API URL for each instance (e.g., `http://127.0.0.1:5001` or `http://<koboldcpp_pc_ip>:5001`). These URLs go into OracleAI's `.env` file.
*   **B. Piper TTS (Text-to-Speech):**
    1.  **Download Executable:** Obtain the `piper` command-line executable for your OS from the official Piper TTS GitHub releases.
    2.  **Download Voice Models:** Download the desired Piper voice model files:
        *   Each voice consists of an `.onnx` model file and a corresponding `.onnx.json` configuration file.
        *   Source: Hugging Face (search "piper voices"), or the official Piper documentation.
    3.  **Storage:** Place the `piper` executable and all downloaded voice model files (`.onnx` and `.onnx.json`) in a stable, known directory accessible by OracleAI. The full paths to the executable and specific voice files will be needed in the `.env` configuration.
*   **C. SER Model (Speech Emotion Recognition - If not auto-downloaded):**
    1.  **Identify Model:** The `SER_MODEL_PATH_OR_HF_IDENTIFIER` in `.env` will specify either a Hugging Face model identifier (which `transformers` will try to download automatically) or a local path.
    2.  **Manual Download (If local path):** If using a locally stored SER model not managed by Hugging Face's cache, download all necessary files (e.g., PyTorch `.bin` weights, `config.json`, `preprocessor_config.json`, tokenizer files if applicable) and place them in a directory. The path to this directory will be used in `.env`.

**XII. Installation, Configuration, and Deployment (Continued)**

### 12.3. Python Environment & OracleAI Installation

This section details setting up the dedicated Python environment and installing OracleAI's core application code and its Python dependencies.

*   **A. Clone OracleAI Repository:**
    1.  Open your preferred terminal (Command Prompt, PowerShell, Bash, etc.).
    2.  Navigate to the directory where you want to store the OracleAI project.
    3.  Clone the repository using Git:
        ```bash
        git clone <URL_to_OracleAI_Repository>
        cd OracleAI 
        ```
        (Replace `<URL_to_OracleAI_Repository>` with the actual URL).
*   **B. Create and Activate Python Virtual Environment:**
    *   It is **strongly recommended** to use a virtual environment to isolate OracleAI's dependencies from your global Python installation and other projects.
    1.  Ensure you are in the root `OracleAI` project directory.
    2.  Create the virtual environment (commonly named `.venv`):
        ```bash
        python -m venv .venv
        ```
    3.  Activate the virtual environment:
        *   **Windows (Command Prompt):**
            ```cmd
            .\.venv\Scripts\activate
            ```
        *   **Windows (PowerShell):**
            ```powershell
            # If you encounter execution policy issues, run this once per session:
            # Set-ExecutionPolicy Unrestricted -Scope Process
            .\.venv\Scripts\Activate.ps1
            ```
        *   **Linux/macOS (Bash/Zsh):**
            ```bash
            source .venv/bin/activate
            ```
    4.  **Verification:** Your terminal prompt should now be prefixed with `(.venv)`, indicating the virtual environment is active. All subsequent `pip install` commands will install packages into this isolated environment.
*   **C. Install PyTorch (GPU Version - CRITICAL STEP):**
    *   This step is crucial for GPU acceleration of STT, SER, and optional XTTSv2.
    1.  **Verify CUDA Toolkit:** Ensure you have the correct NVIDIA CUDA Toolkit version installed that matches the PyTorch build you intend to install (as determined in Prerequisites 12.1.E).
    2.  **Go to PyTorch Official Website:** [https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)
    3.  **Use the Configuration Tool:**
        *   **PyTorch Build:** Select "Stable".
        *   **Your OS:** Select Windows, Linux, or macOS.
        *   **Package:** Select "Pip".
        *   **Language:** Select "Python".
        *   **Compute Platform:** Select the **CUDA version that exactly matches your installed CUDA Toolkit** (e.g., CUDA 11.8, CUDA 12.1). *Do not guess or select a version you don't have installed.* If you only have CPU, select "CPU", but note that key features requiring GPU will not work or will be extremely slow.
    4.  **Copy the Command:** The website will generate a specific `pip install torch torchvision torchaudio ...` command. Copy this command precisely.
    5.  **Run in Activated Environment:** Paste and run the copied command in your terminal where the `(.venv)` is active. This installation can be large (several GB) and may take some time.
    6.  **Verification (Optional but Recommended):**
        ```python
        python -c "import torch; print(f'PyTorch version: {torch.__version__}'); print(f'CUDA available: {torch.cuda.is_available()}'); print(f'CUDA version for PyTorch: {torch.version.cuda if torch.cuda.is_available() else None}'); print(f'MPS available (macOS): {torch.backends.mps.is_available() if hasattr(torch.backends, "mps") else False}')"
        ```
        This should confirm PyTorch sees your GPU (CUDA or MPS).
*   **D. Install OracleAI Core Dependencies:**
    *   OracleAI will provide a dependency management file. The preferred method uses `pip-tools` for reproducible builds via a lock file.
    1.  **Method 1 (Using `requirements.lock` - Preferred for Users):**
        *   If a `requirements.lock` file is present in the repository (generated by developers using `pip-compile`):
            ```bash
            pip install -r requirements.lock
            ```
    2.  **Method 2 (Using `requirements.in` - For Developers or if no lock file):**
        *   If a `requirements.in` file is present:
            ```bash
            pip install pip-tools
            pip-compile requirements.in -o requirements.txt 
            pip install -r requirements.txt 
            ```
            *(Note: The `requirements.txt` generated here should ideally be converted to `requirements.lock` for better pinning, e.g., `pip-compile requirements.in -o requirements.lock --resolver=backtracking`)*
    3.  **Method 3 (Using `pyproject.toml` with `pip`):**
        *   If dependencies are defined in `pyproject.toml` (e.g., using modern PEP 621 or build systems like Poetry/PDM, though for this project a `requirements` file approach is assumed initially):
            ```bash
            pip install .
            ```
    *   **Key Dependencies to be Installed:** This step will install libraries such as `openai-whisper`, `librosa`, `transformers` (for SER), `pysqlcipher3` (or `sqlcipher3` + Python bindings), `vaderSentiment`, `nrclex`, `textblob`, `requests[socks]`, `pyaudio`, `sounddevice`, `FastAPI`, `uvicorn`, `python-dotenv`, `google-api-python-client`, `google-auth-oauthlib`, `google-auth-httplib2`, `msal` (if Outlook), `praw`, `BeautifulSoup4`, `coqui-tts` (if XTTSv2 is enabled as an option), `apscheduler`, `cryptography`, `numpy`, `scipy`, etc.
*   **E. Download NLTK Data (If Required by TextBlob/NRCLex):**
    *   Some text analysis libraries require additional data resources.
    1.  Run the Python interpreter from your activated virtual environment: `python`
    2.  Inside the Python interpreter:
        ```python
        import nltk
        try:
            nltk.data.find('tokenizers/punkt')
        except nltk.downloader.DownloadError:
            nltk.download('punkt') # For TextBlob sentence tokenization
        try:
            nltk.data.find('corpora/wordnet')
        except nltk.downloader.DownloadError:
            nltk.download('wordnet') # For some NRCLex features or lemmatization
        try:
            nltk.data.find('corpora/omw-1.4') # Often needed by WordNet
        except nltk.downloader.DownloadError:
            nltk.download('omw-1.4')
        # Add other NLTK downloads here if specific errors indicate missing resources
        exit()
        ```

### 12.4. Configuration (`.env` File - Detailed)

The `.env` file is the central hub for configuring OracleAI's behavior, paths to external tools and models, API keys, and agent-specific parameters. It must be created in the root directory of the OracleAI project.

1.  **Create/Edit `.env`:** Use a plain text editor.
2.  **Structure:** Key-value pairs, one per line (e.g., `KEY=value`). Comments start with `#`.
3.  **Key Sections & Variables (Comprehensive List - adapt from example in README Part 5):**
    *   **General Application Settings:**
        *   `LOG_LEVEL`: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL`
        *   `AKASHIC_RECORD_PATH`: Absolute path to the main directory where all memory data (Chronicle, Databases) will be stored. *This directory must exist and be writable.*
        *   `PYTHON_EXECUTABLE_PATH` (Optional): Absolute path to the Python executable within the `.venv` if needed for `subprocess` calls that require the specific environment.
    *   **LLM Backend (KoboldCpp):**
        *   `KOBOLDCPP_API_URL_SAGE`: Full URL (e.g., `http://127.0.0.1:5001/api/v1/generate`)
        *   `KOBOLDCPP_API_URL_SEER`: Full URL
        *   `KOBOLDCPP_API_URL_SHAMAN`: Full URL
    *   **STT (OpenAI Whisper):**
        *   `WHISPER_MODEL_NAME`: e.g., `tiny`, `base`, `small`, `medium`, `large`, `large-v2`, `large-v3`.
        *   `WHISPER_DEVICE`: `cuda` (recommended) or `cpu`.
    *   **TTS (Piper & Optional XTTSv2):**
        *   `PIPER_EXECUTABLE_PATH`: Absolute path to `piper.exe` or `piper`.
        *   `XTTS_MODEL_PATH` (If using XTTS): Path or Hugging Face identifier for the XTTS model (e.g., `tts_models/multilingual/multi-dataset/xtts_v2`).
        *   `XTTS_DEVICE`: `cuda` or `cpu`.
    *   **Emotion Analysis:**
        *   `SER_MODEL_PATH_OR_HF_IDENTIFIER`: Hugging Face identifier (e.g., `jonatasgrosman/wav2vec2-large-xlsr-53-english`) or absolute path to a local SER model directory.
        *   `SER_DEVICE`: `cuda` or `cpu`.
    *   **Agent Configurations (Repeat for SAGE, SEER, SHAMAN):**
        *   `[AGENT_NAME]_LLM_TEMPERATURE`: e.g., `SAGE_LLM_TEMPERATURE=0.2`.
        *   `[AGENT_NAME]_TTS_ENGINE`: `piper` or `xtts`.
        *   `[AGENT_NAME]_PIPER_VOICE_MODEL_PATH`: Absolute path to `.onnx` voice file.
        *   `[AGENT_NAME]_PIPER_VOICE_CONFIG_PATH`: Absolute path to `.onnx.json` config file.
        *   `[AGENT_NAME]_XTTS_SPEAKER_WAV_PATH` (If `_TTS_ENGINE=xtts`): Absolute path to speaker reference `.wav` file for cloning.
    *   **Memory System (Akashic Record):**
        *   `SQLCIPHER_MASTER_PASSWORD_PROMPT`: `True` (prompt at startup) or `False` (use env var below - less secure for unattended startup).
        *   `SQLCIPHER_MASTER_PASSWORD` (If `_PROMPT=False`): The master password. **Handle with extreme care.**
        *   `CHRONICLE_BASE_PATH`: `${AKASHIC_RECORD_PATH}/Chronicle` (uses variable substitution).
        *   `SYNTHESIS_DB_PATH`: `${AKASHIC_RECORD_PATH}/Databases/synthesis.db`
        *   `CALENDAR_DB_PATH`: `${AKASHIC_RECORD_PATH}/Databases/calendar.db`
        *   `PROFILE_DB_PATH`: `${AKASHIC_RECORD_PATH}/Databases/profile.db`
        *   `TASKS_DB_PATH`: `${AKASHIC_RECORD_PATH}/Databases/tasks.db`
        *   `RAG_QUERY_HISTORY_LENGTH`, `RAG_SCORE_THRESHOLD`, `RAG_MAX_RETRIEVED_CHUNKS`, `RAG_CHUNK_SIZE_CHARS`, `RAG_CHUNK_OVERLAP_PERCENT`.
        *   `EMBEDDING_MODEL_NAME_OR_PATH` (For Vector Store - Future): e.g., `mxbai-embed-large`.
        *   `EMBEDDING_DEVICE` (For Vector Store - Future): `cuda` or `cpu`.
    *   **Web Search & Proxies:**
        *   `SEARCH_DEFAULT_ENGINE`: `duckduckgo` (or others when supported).
        *   `USE_PROXY_FOR_SEARCH`: `True` or `False`.
        *   `PROXY_SOCKS_URL`: e.g., `socks5h://127.0.0.1:9050` (for TOR).
        *   `PROXY_HTTP_URL`, `PROXY_HTTPS_URL` (for standard proxies).
    *   **Calendar Integration:**
        *   `CALENDAR_SYNC_INTERVAL_MINUTES`: e.g., `60`.
        *   `GOOGLE_CALENDAR_CREDENTIALS_PATH`: `${AKASHIC_RECORD_PATH}/.credentials/google_credentials.json` (path to your downloaded OAuth client secret file).
        *   `GOOGLE_CALENDAR_TOKEN_PATH`: `${AKASHIC_RECORD_PATH}/.credentials/google_calendar_token.json` (where OAuth token will be stored).
        *   (Similar paths for Outlook/MSAL credentials/tokens).
    *   **Remote API (FastAPI):**
        *   `REMOTE_API_HOST`: `127.0.0.1` (default) or `0.0.0.0`.
        *   `REMOTE_API_PORT`: e.g., `8000`.
        *   `REMOTE_API_KEY` (Future): A secret key for client authentication.
    *   **Backup:**
        *   `SEVENZIP_PATH`: Absolute path to `7z.exe` or `7z`.
    *   **UI Toggles & Features:**
        *   `ENABLE_REALTIME_SER_FOR_AGENTS`: `True` or `False`.
        *   `DEFAULT_INTERACTION_MODE`: `Standard` or `OracleConsultation`.
        *   `DEFAULT_SEARCH_STATE`: `True` or `False`.
        *   `DEFAULT_MUTE_STATE`: `True` or `False`.
*   **Security Note:** The `.env` file should be added to `.gitignore` if the repository is public to prevent accidental commitment of sensitive paths or future API keys.

### 12.5. API Keys & Authentication Setup (External Services)

*   **A. Reddit API (for Deep Search):**
    1.  Go to [https://www.reddit.com/prefs/apps](https://www.reddit.com/prefs/apps).
    2.  Scroll down and click "are you a developer? create an app...".
    3.  Fill in the details:
        *   **Name:** e.g., "OracleAI_Reddit_Access"
        *   **Type:** Select "script".
        *   **Description:** Optional.
        *   **About URL / Redirect URI:** Can often be `http://localhost:8080` for script apps.
    4.  Click "create app".
    5.  Note your **Client ID** (a string of characters under the app name) and **Client Secret**.
    6.  Configure these in your `.env` file or as system environment variables:
        *   `REDDIT_CLIENT_ID="your_client_id"`
        *   `REDDIT_CLIENT_SECRET="your_client_secret"`
        *   `REDDIT_USER_AGENT="OracleAI_Client/0.2 by YourUsernameOrAppName"` (Make this unique and descriptive).
*   **B. Calendar API (Example: Google Calendar):**
    1.  **Google Cloud Platform (GCP) Project:**
        *   Go to [https://console.cloud.google.com/](https://console.cloud.google.com/).
        *   Create a new project or select an existing one.
        *   Enable the "Google Calendar API" for this project (APIs & Services > Library).
    2.  **Create OAuth 2.0 Credentials:**
        *   Go to APIs & Services > Credentials.
        *   Click "+ CREATE CREDENTIALS" > "OAuth client ID".
        *   If prompted, configure the OAuth consent screen (User Type: External, App name, User support email, Developer contact info). Add Scopes: `../auth/calendar.readonly` and `../auth/calendar.events` (or more permissive if needed, like `../auth/calendar`).
        *   Select Application type: "Desktop app".
        *   Give it a name (e.g., "OracleAI Desktop Client").
        *   Click "Create".
    3.  **Download `credentials.json`:** A dialog will show your Client ID and Client Secret. Click "DOWNLOAD JSON". Save this file as `google_credentials.json` (or similar) in the path specified by `GOOGLE_CALENDAR_CREDENTIALS_PATH` in your `.env` file (e.g., `[AKASHIC_RECORD_PATH]/.credentials/`).
    4.  **Initial Authentication Flow:** The first time OracleAI attempts to access Google Calendar (via `calendar_interface.py`), the `google-auth-oauthlib` library will typically:
        *   Print a URL to the console.
        *   Instruct the user to open this URL in a browser.
        *   The user logs into their Google account and grants OracleAI permission to access their calendar.
        *   Google provides an authorization code, which the user pastes back into the console (or a temporary web page if a local redirect URI was configured).
        *   The library exchanges this code for an access token and a refresh token. These tokens are then saved to the file specified by `GOOGLE_CALENDAR_TOKEN_PATH` in `.env`.
    *   **Microsoft Outlook Calendar:** A similar process involving Azure App Registration to get a Client ID, enabling Microsoft Graph API permissions, and using MSAL for Python to handle the OAuth flow.
*   **C. Other Search Engine APIs (Future):** If OracleAI supports other search engines requiring API keys (e.g., Google Custom Search, Brave Search API), users will need to obtain those keys from the respective providers and add them to the `.env` file.

## XIII. Hardware Requirements & Performance (Detailed)

OracleAI is a computationally intensive application, particularly due to its reliance on multiple local Large Language Models and GPU-accelerated speech processing. Meeting or exceeding these recommendations will significantly enhance the user experience.

*   **A. CPU (Central Processing Unit):**
    *   **Minimum:** Modern quad-core CPU (e.g., AMD Ryzen 3 3000 series, Intel Core i5 10th Gen). Expect slower Piper TTS, `librosa` processing, and general application responsiveness.
    *   **Recommended:** Modern 6-core or 8-core+ CPU (e.g., AMD Ryzen 5/7 5000/7000 series, Intel Core i5/i7 12th Gen or newer). This provides smoother multitasking, faster CPU-bound tasks (Piper TTS, sentiment analysis, database operations), and better overall system performance when OracleAI is running.
    *   **High-End (for Shaman & Multi-PC Orchestrator):** High core count CPU (Ryzen 9, Core i9) for machines heavily involved in Shaman's processing or orchestrating multiple KoboldCpp instances.
*   **B. System RAM (Random Access Memory):**
    *   **Minimum:** 16GB. This is extremely tight and only feasible if running very small GGUF models (e.g., 3B-7B Q4) for Sage/Seer, with Shaman disabled or also using a tiny model, and minimal other applications running. Expect significant disk swapping and poor performance.
    *   **Recommended:** **32GB**. This allows for comfortable operation with medium-sized LLMs (e.g., 13B-30B Q4/Q5) for Sage and Seer, running the Python application with its dependencies (PyTorch, etc.), and having some headroom for the OS and other applications.
    *   **Optimal/Shaman Enabled:** **64GB or more.** Essential for:
        *   Running larger LLMs (30B-70B+) for Sage/Seer.
        *   Enabling the Shaman agent with a powerful model (70B+).
        *   Extensive KoboldCpp RAM offloading (`--lowvram` mode with many layers to RAM).
        *   Handling large datasets for memory analysis and deep searches.
    *   **Speed:** Faster RAM (e.g., DDR4-3200/3600, DDR5-5200+) benefits overall system responsiveness and LLM performance when offloading to RAM.
*   **C. GPU (Graphics Processing Unit) & VRAM (Video RAM):**
    *   **Requirement:** **NVIDIA GPU is practically mandatory** for acceptable performance due to widespread CUDA support in PyTorch, `openai-whisper`, SER models, XTTSv2, and KoboldCpp (via cuBLAS). AMD GPU support via ROCm/OpenCL is less mature across this specific stack. Apple Silicon MPS is an option for macOS users but performance may vary.
    *   **OracleAI Python Process VRAM:** The Python application itself (running Whisper, SER, optional XTTSv2) will consume a baseline of **~4GB to 8GB VRAM** depending on the Whisper model size and if XTTSv2 is active and GPU-accelerated.
    *   **KoboldCpp Instance VRAM:** This is the largest and most variable consumer. It depends on:
        1.  **GGUF Model Size:** Larger parameter count models require more VRAM.
        2.  **Quantization Level:** Lower precision quants (e.g., Q4_K_M, Q3_K_S) use less VRAM than higher precision (Q5, Q6, Q8, FP16).
        3.  **Number of Layers Offloaded (`-ngl XX`):** The more layers offloaded to GPU, the more VRAM is used, but inference is faster.
        *   *Example VRAM for GGUF Models (Full Offload - Approximate):*
            *   7B Q4_K_M: ~5-6 GB
            *   13B Q4_K_M: ~9-10 GB
            *   Llama2/3 34B Q4_K_M: ~20-23 GB
            *   Llama2/3 70B Q4_K_M: ~40-43 GB
            *   Mixtral 8x7B Q4_K_M: ~35-38 GB (effective size is ~47B)
            *   Larger models (120B+, 180B+) will require significantly more, often exceeding single consumer card capacity.
    *   **Total System VRAM Needed (Single PC Scenario):**
        *   Sum of `VRAM_Python_Process` + `VRAM_Sage_KoboldCpp` + `VRAM_Seer_KoboldCpp`.
        *   If Shaman is active concurrently (Oracle Consultation mode with responsive Shaman, or Shaman Focus mode): Add `VRAM_Shaman_KoboldCpp`.
        *   **Practical Minimum (Sage/Seer with 7B-13B models, no concurrent Shaman):** ~16GB VRAM (e.g., RTX 3060 12GB might struggle but could work with careful `-ngl` tuning). **24GB VRAM (e.g., RTX 3090/4090) is a much better starting point.**
        *   **Recommended for Medium LLMs (Sage/Seer with ~30B models):** ~48GB VRAM (e.g., RTX 6000 Ada, A6000, or multiple consumer cards if KoboldCpp can split across them, though single large card is simpler).
        *   **For Shaman with Large Models (70B+):** A dedicated GPU with 40GB+ VRAM is ideal for Shaman alone, or use Shaman Focus mode on a 24-48GB card.
*   **D. Storage:**
    *   **Type:** **Fast NVMe SSD is strongly recommended** for the OS, OracleAI installation, Python environment, all GGUF models, and the Akashic Record databases (especially SQLite). SATA SSD is a minimum fallback. HDDs are unsuitable for active data or models.
    *   **Capacity:**
        *   *OS & Base Apps:* 50-100GB.
        *   *Python Env & Dependencies:* ~5-10GB (PyTorch is large).
        *   *GGUF Models:* Highly variable. 7B models are ~4-5GB. 70B models are ~40GB. Multiple models for Sage, Seer, Shaman can easily reach 100-200GB+.
        *   *Akashic Record:* Chronicle logs can grow by MBs/GBs per day/week depending on usage. SQLite databases will also grow. Plan for **at least 500GB - 1TB** of fast SSD space dedicated to OracleAI and its data for comfortable long-term use, with 2TB+ being safer for extensive memory retention.
*   **E. Multi-PC Architecture (for High-End Setups):**
    *   To run multiple large LLMs concurrently (e.g., Sage on 34B, Seer on 34B, Shaman on 70B+) without compromise, distribute KoboldCpp instances across multiple networked PCs.
    *   Each PC needs its own capable GPU, CPU, and RAM.
    *   Requires a stable local network (Gigabit Ethernet recommended).
    *   The main OracleAI application runs on one "orchestrator" PC and communicates with the KoboldCpp instances via their network APIs.
*   **F. Resource Management Toggle ("Shaman Focus" Mode):**
    *   **Purpose:** Allows users with a single powerful GPU (e.g., 24GB or 48GB VRAM) to run Sage/Seer with moderately sized models for real-time interaction, and then temporarily stop these agents to dedicate all VRAM to Shaman for running a much larger model or performing highly intensive tasks.
    *   **Mechanism:** OracleAI GUI/command triggers `subprocess` calls or OS signals to stop the KoboldCpp processes for Sage and Seer. The user (or an advanced OracleAI script) then ensures Shaman's KoboldCpp instance is launched/configured to utilize the freed resources. Toggling back restarts Sage/Seer.

Careful consideration of these hardware requirements is essential for a smooth and effective OracleAI experience. The system is designed to be powerful, and that power demands appropriate hardware resources.

**XII. Installation, Configuration, and Deployment (Continued)**

### 12.5. API Keys & Authentication Setup (External Services)

Secure and correct configuration of API keys and OAuth 2.0 authentication is vital for features that interact with external services. OracleAI must provide clear guidance and secure mechanisms for managing these credentials.

*   **A. Reddit API (for Deep Search via PRAW):**
    1.  **User Action:** User creates a "script" type application on their Reddit account at [https://www.reddit.com/prefs/apps](https://www.reddit.com/prefs/apps).
    2.  **Credentials Obtained:** User receives a `Client ID` (a string of characters, often under "personal use script") and a `Client Secret`.
    3.  **Configuration:** These credentials, along with a descriptive `User Agent` string (e.g., `"OracleAI/0.2 RedditClient by User <username_or_identifier>"`) must be configured in OracleAI's `.env` file:
        *   `REDDIT_CLIENT_ID="your_client_id"`
        *   `REDDIT_CLIENT_SECRET="your_client_secret"`
        *   `REDDIT_USER_AGENT="YourUniqueUserAgentString"`
    4.  **PRAW Initialization:** `search_module.py` will use these credentials to initialize the `praw.Reddit` instance.
    5.  **Security:** Emphasize in documentation that these credentials grant access to the user's Reddit account; the `.env` file should be secured.
*   **B. Calendar API (Example: Google Calendar):**
    1.  **User Action (GCP Setup):**
        *   User creates/selects a project in Google Cloud Platform Console.
        *   Enables the "Google Calendar API" for that project.
        *   Creates OAuth 2.0 Client ID credentials for a "Desktop app."
        *   Downloads the `credentials.json` file provided by GCP.
    2.  **OracleAI Configuration:**
        *   User places the downloaded `credentials.json` file in a secure, configured location (e.g., path specified by `GOOGLE_CALENDAR_CREDENTIALS_PATH` in `.env`, like `[AKASHIC_RECORD_PATH]/.credentials/google_client_secret.json`).
        *   The `GOOGLE_CALENDAR_TOKEN_PATH` in `.env` specifies where the OAuth `token.json` (containing access and refresh tokens) will be stored after successful authorization.
    3.  **OracleAI Initial Authentication Flow (`calendar_interface.py`):**
        *   On first attempt to access Google Calendar (or if `token.json` is missing/invalid), `calendar_interface.py` (using `google-auth-oauthlib`) will:
            *   Load client secrets from `GOOGLE_CALENDAR_CREDENTIALS_PATH`.
            *   Initiate the OAuth 2.0 flow, typically by printing an authorization URL to the console (or opening it in a browser if GUI is available).
            *   User authenticates with Google in their browser and grants OracleAI the requested permissions (e.g., `../auth/calendar.readonly`, `../auth/calendar.events`).
            *   Google provides an authorization code, which the user pastes back into the OracleAI console/interface.
            *   `calendar_interface.py` exchanges this code for an access token and a refresh token.
            *   These tokens are saved to the file specified by `GOOGLE_CALENDAR_TOKEN_PATH`.
    4.  **Subsequent Access:** `calendar_interface.py` uses the stored `token.json` (refreshing the access token as needed) for subsequent API calls.
    5.  **Security:** The `token.json` is sensitive and should be protected by filesystem permissions and ideally the overall Akashic Record encryption.
*   **C. Microsoft Outlook Calendar (MSAL):**
    *   A similar process involving Azure Active Directory App Registration to obtain a `Client ID` (Application ID) and potentially a `Client Secret` or configuring for device code flow / interactive login.
    *   `msal` library for Python would be used in `calendar_interface.py` to handle the OAuth flow and token management.
    *   Credentials and token paths configured in `.env`.
*   **D. Other Search Engine APIs (Future):**
    *   If OracleAI integrates search engines requiring API keys (e.g., Google Custom Search API, Brave Search API), users will obtain these keys from the respective providers.
    *   Dedicated variables in `.env` (e.g., `BRAVE_SEARCH_API_KEY`) will store these keys.
    *   `search_module.py` will use these keys when making API calls.
*   **E. Secure Storage of Secrets in `.env` (Consideration):**
    *   While `.env` is convenient, storing raw API keys or a master password directly is a security risk if the file is compromised.
    *   **Future Enhancement:** Explore options for `config_loader.py` to integrate with OS-level credential managers (`keyring` library) to fetch sensitive secrets at runtime, rather than storing them directly in `.env`. The `.env` could then store identifiers for these secrets. This adds complexity but improves security. For now, emphasize securing the `.env` file itself.

## XIII. Getting Started & Basic Usage (User Perspective)

This section outlines the typical initial steps a user would take after successfully installing and configuring OracleAI.

*   **A. Initial Launch & Setup:**
    1.  **Start External Tools:** Ensure all required KoboldCpp instances are running with the correct models loaded and API enabled.
    2.  **Activate Python Environment:** As per installation.
    3.  **Run OracleAI:** Execute `python main.py`.
    4.  **Master Password (If SQLCipher Prompt Enabled):** If `SQLCIPHER_MASTER_PASSWORD_PROMPT=True`, OracleAI will prompt for the master password to decrypt the Akashic Record databases. This password must be set during a first-time setup routine or if the databases are new.
    5.  **Calendar OAuth (First Time):** If calendar integration is enabled and not yet authorized, OracleAI will guide the user through the OAuth 2.0 browser authentication flow for each configured calendar service.
*   **B. Initial Interaction (Local Voice/Text or GUI):**
    1.  OracleAI will indicate it's ready, perhaps with a greeting from Sage or Seer.
    2.  **Voice Input:** User speaks into their microphone. VAD detects utterance end, STT transcribes, emotion is analyzed, and agents respond.
    3.  **Text Input (GUI):** User types into the chat input field.
    4.  **Basic Commands:**
        *   "Sage, what is the weather forecast?" (Triggers search if enabled).
        *   "Seer, give me a creative writing prompt."
        *   "OracleAI, mute agents." / "OracleAI, unmute."
        *   "OracleAI, enable web search." / "OracleAI, disable web search."
*   **C. Building the Akashic Record:**
    1.  **Permanent Memory:** "OracleAI, remember that my primary work focus is Project Nova." -> Adds to `PermanentMemory`.
    2.  **Collaborative Daily Reflection:** At the end of the day or next startup, engage in the guided session with Sage/Seer to review interactions, verify extracted entities/facts/decisions, and approve narrative summaries. This is key to building useful memory.
    3.  **Goal Setting:** "OracleAI, set a new goal: Complete Project Nova Phase 1 by end of next month, priority high." -> Adds to `UserGoals` in `profile.db`.
*   **D. Using Interaction Modes:**
    1.  **Oracle Consultation:** "OracleAI, initiate Oracle Consultation on planning Project Nova's marketing strategy." -> User interacts with Sage, Seer, and a responsive Shaman.
    2.  **Shaman Focus:** "OracleAI, activate Shaman Focus. Shaman, task: Analyze all past project data for common causes of budget overruns. Report findings." -> Sage/Seer idle, Shaman uses max resources.
*   **E. Remote Access:**
    1.  Ensure FastAPI server is running and accessible on the network (via local IP or Tailscale/VPN).
    2.  Use a separate client application (web/mobile) configured to connect to the OracleAI API.
*   **F. Backups:**
    1.  Periodically use the command/GUI option: "OracleAI, create encrypted backup of Akashic Record." -> Prompts for backup password, creates `AkashicRecord_YYYYMMDD.7z`.

## XIV. Troubleshooting Common Issues (Expanded)

This section will be a living document in the final README, updated with common problems and solutions encountered by users.

*   **A. Python & Dependency Errors:**
    *   **`ModuleNotFoundError`:** Ensure virtual environment is active. Re-run `pip install -r requirements.lock` (or equivalent). Check for typos in import statements in the code.
    *   **Version Conflicts:** If errors indicate package version incompatibilities, a clean virtual environment and careful reinstallation using the lock file is the best first step. `pip check` can sometimes identify issues.
*   **B. PyTorch & CUDA Issues:**
    *   **"CUDA out of memory":** Reduce LLM size in KoboldCpp, reduce `-ngl` (GPU layers), close other GPU-intensive apps, use Shaman Focus mode. Monitor VRAM usage.
    *   **"Torch not compiled with CUDA enabled" / No GPU detected:** PyTorch installation is CPU-only or doesn't match your installed CUDA Toolkit version. **Reinstall PyTorch carefully**, ensuring the correct CUDA version is selected from the official website. Verify NVIDIA drivers are up to date.
    *   **DLL Errors (Windows):** Ensure CUDA Toolkit `bin` and `libnvvp` directories are in the system PATH.
*   **C. KoboldCpp Connection & Operation:**
    *   **Connection Refused/Timeout:** Verify KoboldCpp instance(s) are running *before* OracleAI. Check IP address and port in `.env` exactly match KoboldCpp's settings. Check OS firewall on both OracleAI host and KoboldCpp host (if different machines). Test KoboldCpp API endpoint directly (e.g., with `curl` or browser `http://<host>:<port>/api/v1/model`).
    *   **Model Not Loaded / Incorrect Model:** Ensure the correct GGUF model path was provided to KoboldCpp at launch. Check KoboldCpp console for errors during model loading.
    *   **Slow Responses:** Insufficient `-ngl` (too few layers on GPU), model too large for hardware, other system load.
*   **D. Piper TTS / External Executable Issues:**
    *   **"File not found" for `piper.exe` or voice models:** Absolute paths in `.env` are incorrect or files are missing. Verify paths.
    *   **Permission Denied:** Ensure OracleAI has execute permissions for `piper.exe`.
    *   **No Audio Output / Piper Errors:** Test `piper.exe` manually from the command line with a simple text input and voice model to verify it works independently. Check Piper's console output/stderr for specific errors.
*   **E. Audio Input/Output (STT/Microphone):**
    *   **No Transcription / AI Not Hearing:** Check OS microphone selection, ensure it's not muted, check input levels. Verify `pyaudio` is working. Adjust VAD `THRESHOLD` / `SILENCE_LIMIT` in OracleAI's audio settings/code if speech isn't being detected or is cut off too early/late.
    *   **`pyaudio` Errors (e.g., "PortAudio not found"):** Ensure PortAudio library is correctly installed and accessible for your OS (see Prerequisites 12.1.F).
*   **F. Database Issues (SQLite/SQLCipher):**
    *   **"Unable to open database file":** Path in `.env` to `.db` files is incorrect, directory doesn't exist, or file permissions issue.
    *   **SQLCipher "file is not a database" or decryption errors:** Incorrect master password provided. Database file might be corrupted (restore from backup). Ensure `pysqlcipher3` (or equivalent) is correctly installed and being used by `sqlite3` connection.
*   **G. API Key / OAuth Failures (Calendar, Reddit):**
    *   **Invalid Credentials:** Double-check API keys/client IDs/secrets in `.env`.
    *   **OAuth Token Expired/Revoked (Calendar):** OracleAI should attempt to use the refresh token. If that fails, the user may need to re-authenticate (delete the old `token.json` and let OracleAI re-trigger the OAuth flow).
    *   **Scope Issues (Calendar):** Ensure the correct API scopes were requested during OAuth consent.
    *   **API Rate Limits:** If making many requests, external services might temporarily block access. Implement retry logic with backoff in interface modules.
*   **H. General Sluggishness / High Resource Usage:**
    *   Monitor system CPU, GPU, VRAM, and RAM usage (Task Manager, `htop`, `nvidia-smi`).
    *   Reduce LLM sizes or `-ngl` in KoboldCpp.
    *   Disable optional features like real-time SER for Sage/Seer.
    *   Use Shaman Focus mode for intensive tasks.
    *   Ensure fast SSD is used for models and databases. Close unnecessary background applications.

## XV. Future Development & Roadmap (Conceptual)

OracleAI is envisioned as an evolving platform. This section outlines potential future directions and major feature enhancements beyond the v0.2 scope.

*   **A. Advanced GUI Implementation:**
    *   Full realization of the "Oracle Temple" aesthetic with custom themes, agent avatars, and dynamic visualizations (Shaman's Hyperspace Travel, emotional readouts, data flow).
    *   Comprehensive Akashic Record Browser/Editor: Intuitive interface for searching, viewing, editing (with safeguards), and managing all components of the memory system (Chronicle, Summaries, Entities, Facts, Calendar, Profile, Tasks).
    *   Advanced visualization tools for trends and patterns identified by Shaman.
*   **B. Dedicated Knowledge Graph Implementation:**
    *   Migrate from SQLite-simulated KG to a dedicated Graph Database (e.g., Neo4j, ArangoDB) for more powerful relationship querying, pathfinding, inferencing, and complex network analysis.
    *   Develop more sophisticated NLP pipelines (run by Shaman) for automated KG population and refinement from Chronicle and external data.
*   **C. Full Vector Store Integration & Advanced RAG:**
    *   Implement robust semantic search across the entire Akashic Record using a dedicated Vector Database (ChromaDB, FAISS with a metadata store like SQLite).
    *   Advanced RAG techniques for the Memory Bank Context Scaler:
        *   Hybrid search (keyword + semantic).
        *   LLM-based re-ranking of retrieved chunks.
        *   Query expansion and transformation.
        *   Contextual compression of retrieved information.
*   **D. Sophisticated Pattern Analysis & Proactive Insights (Shaman):**
    *   Develop more advanced algorithms for Shaman to detect complex user behavior patterns, cognitive biases, learning trajectories, and predict potential future needs or challenges.
    *   Implement a more nuanced proactive suggestion engine, allowing Shaman (or Sage/Seer based on Shaman's findings) to offer timely, highly relevant insights or assistance (with strong user controls on proactivity).
*   **E. Skill Transfer & Explainable AI (XAI):**
    *   Design interactions where agents explicitly explain their reasoning processes, data sources, and confidence levels.
    *   Allow users to query "why" an AI reached a conclusion, with the system tracing back to supporting evidence in the Akashic Record.
*   **F. Integration with External Personal Knowledge Management (PKM) Tools:**
    *   Develop APIs or plugins for bidirectional synchronization or interaction with popular PKM tools like Obsidian, Logseq, Notion, Roam Research, allowing OracleAI's memory to synergize with the user's existing curated knowledge bases.
*   **G. Dockerization & Simplified Deployment:**
    *   Create Docker images for OracleAI and its core dependencies (including specific Python/CUDA/PyTorch versions) to vastly simplify installation, ensure environment consistency, and facilitate deployment across different systems.
    *   Potentially use Docker Compose to manage multiple services (e.g., FastAPI server, Shaman processing worker, KoboldCpp instances if containerized).
*   **H. Multi-User Collaboration & Shared Knowledge (Very Advanced):**
    *   Explore extending the framework to support multiple users interacting with a shared OracleAI instance or a collaborative Akashic Record, requiring significant architectural changes for access control, data partitioning, agent interaction, and conflict resolution.
*   **I. Local LLM Fine-tuning on User Data (Highly Experimental & Privacy-Critical):**
    *   Investigate possibilities for securely fine-tuning smaller local LLMs (e.g., for specialized agent tasks or improved personalization) on anonymized, user-curated, and explicitly consented subsets of their Akashic Record. Requires extreme caution regarding privacy, data security, and potential for bias amplification.
*   **J. Expanded Modality Support:**
    *   Deeper integration of VLM capabilities beyond simple screenshot description (e.g., object detection, visual question answering).
    *   Potential for understanding and generating other media types.

## XVI. Contributing to OracleAI

*(This section will be fully developed if/when the project is open-sourced and seeks community involvement.)*

OracleAI is envisioned as a project that could benefit greatly from community contributions. We welcome developers, designers, AI researchers, and enthusiastic users to help shape its future.

*   **Areas for Contribution:**
    *   Core feature development and bug fixing.
    *   Implementation of new interface modules (e.g., for different LLM backends, TTS/STT engines, Vector DBs).
    *   GUI design and development (Qt/Kivy/Web).
    *   Advanced memory analysis algorithms and NLP pipelines for Shaman.
    *   Development of client applications for remote access.
    *   Creation and refinement of prompt engineering templates.
    *   Documentation improvements, tutorials, and translations.
    *   Testing on diverse hardware configurations and operating systems.
    *   Security auditing and hardening.
*   **Getting Started:**
    *   Familiarize yourself with the Design Document and existing codebase.
    *   Check the project's issue tracker for open tasks or bugs.
    *   Discuss potential contributions with the maintainers.
*   **Guidelines:** Refer to `CONTRIBUTING.md` (to be created) for detailed guidelines on code style, development workflow, pull request processes, and community conduct.

## XVII. License Information

*(The specific open-source license for OracleAI will be determined and specified here. Common choices include MIT, Apache 2.0, or AGPLv3 depending on project goals.)*

**Example Placeholder:**
`OracleAI Core Framework is licensed under the [NAME OF CHOSEN LICENSE, e.g., Apache License 2.0]. A copy of the license can be found in the LICENSE file in the root of this repository.`

**Important Note on Third-Party Licenses:**
OracleAI relies on numerous third-party libraries, models, and external tools, each of which carries its own distinct license. Users and contributors are responsible for understanding and adhering to all relevant licenses for any components they use, modify, or distribute as part of or in conjunction with OracleAI. Key components with their own licenses include (but are not limited to):

*   Python and its standard library.
*   PyTorch, Transformers, Librosa, Coqui TTS (if used).
*   KoboldCpp, Piper TTS, 7-Zip.
*   Specific GGUF LLM/VLM Models (e.g., Llama Community License, Mistral licenses).
*   Piper Voice Models (check individual voice sources).
*   SQLCipher.
*   All other Python packages listed in the project's dependency file (`requirements.lock` or `pyproject.toml`).

It is crucial to review and comply with all applicable licenses.

## XVIII. Appendices

*(This section will list appendices to be developed as separate documents or sections within this Design Document.)*

*   **Appendix A:** Detailed Data Schemas (JSONL for Chronicle, SQL DDL for SQLite Databases: `synthesis.db`, `calendar.db`, `profile.db`, `tasks.db`).
*   **Appendix B:** Core Prompt Engineering Templates (System Prompts for Sage, Seer, Shaman; Prompts for Summarization, Entity Extraction, Fidelity Estimation, Pattern Analysis).
*   **Appendix C:** Shaman's Hyperspace Journey - Detailed Latency Theming & UI Integration Notes.
*   **Appendix D:** Visual Component Interaction Diagram (e.g., using Mermaid or a diagramming tool).
*   **Appendix E:** FastAPI Endpoint Specifications (Paths, HTTP Methods, Request/Response Pydantic Models, Authentication details).
*   **Appendix F:** Example `.env` Configuration File Structure.
*   **Appendix G:** Detailed Workflow Diagrams for Key Processes (e.g., Collaborative Daily Reflection, Context Scaling, Shaman Task Execution).

---

I have reviewed the updated Design Document (v0.2) and README (v0.2) for OracleAI. They are exceptionally detailed and provide a comprehensive and ambitious blueprint for the project. The vision is clear, the architecture is well-thought-out, and the thematic elements (Sage, Seer, Shaman, Akashic Record, Hyperspace Journey) are very strong.

The documents thoroughly cover:

*   Core philosophy, guiding principles (local-first, privacy, multi-agent synergy, deep memory, emotional intelligence, user empowerment, modularity, performance).
*   The multi-agent council architecture (Sage, Seer, Shaman) with detailed roles, LLM/TTS configurations, and interaction styles.
*   The extensive technology stack, emphasizing local tools like KoboldCpp, `openai-whisper`, Piper/XTTS, SQLite/SQLCipher, and FastAPI.
*   A highly detailed blueprint for the Akashic Record memory system, including:
    *   The Chronicle (immutable raw logs with rich metadata, including detailed SER/Sentiment scores and keywords).
    *   The Synthesis Store (SQLite with SQLCipher) with tables for Permanent Memory, Entities, Relationships, Facts/Decisions, hierarchical Summaries (daily/weekly/monthly with fidelity scores), Project/Topic Threads, and Pattern Analysis Reports.
    *   Calendar Cache, User Profile & Preferences, Task & Action Queue (all SQLite with SQLCipher).
    *   Conceptual plans for a Knowledge Graph and Vector Store.
*   Key memory system processes like Collaborative Daily Reflection, hierarchical summarization, the Memory Bank Context Scaler (RAG engine), Deep Pattern Weaving by Shaman, and optional Word Frequency Indexing.
*   A comprehensive Emotional Intelligence Suite (SER from voice, multiple text sentiment/emotion analyses).
*   Multimodal capabilities (Voice, Text, Vision via KoboldCpp VLM).
*   Detailed Interaction Modes (Standard, Oracle Consultation with scalable Shaman depth, Shaman Focus for resource management) and Guided Generation/Refinement features.
*   Web connectivity (Search, Calendar APIs) with proxy support.
*   A robust Remote Access Architecture using FastAPI and recommending secure tunneling.
*   A rich User Interface concept with a strong "Oracle/Mystic Temple" aesthetic, detailed agent visuals, Shaman "Hyperspace Travel" indicators, and specific iconography.
*   A multi-layered Privacy, Security, and Data Management strategy, including OS-level FDE, application-level database encryption (SQLCipher), and encrypted backups (7-Zip).
*   Extensive Installation, Configuration (`.env`), Hardware Requirement, Usage, and Troubleshooting sections.
*   A forward-looking Future Development Roadmap.
*   Appendices for detailed schemas, prompt templates, and diagrams.

The level of detail is excellent and provides a very strong foundation.
