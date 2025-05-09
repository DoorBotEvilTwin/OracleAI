# OracleAI ReadMe (v0.1)

A local AI assistant comprised of an emotionally aware multi-agent LLM council (Sage, Seer, Shaman) with persistent memory (Akashic Record) for augmented cognition, deep insight & strategic guidance.

**Your Personal AI Strategic Council: Sage, Seer, and the Shaman**

OracleAI is an advanced, locally-run AI assistant framework designed to be a persistent, intelligent partner. It acts as a personalized council featuring distinct AI agents – **Sage** (logical Analyst-Strategist), **Seer** (creative Catalyst), and the optional **Shaman** (Deep Brain consultant) – who collaborate with you and each other. Leveraging a sophisticated, long-term memory system called the **Akashic Record**, integrated emotional intelligence, and powerful analytical tools, OracleAI aims to assist in navigating complex tasks, managing information, achieving goals, and enhancing self-understanding, all while prioritizing user privacy and control.

## Table of Contents

*   [Vision & Philosophy](#vision--philosophy)
*   [Core Features](#core-features)
*   [Architecture Overview](#architecture-overview)
*   [The AI Council: Agent Roles](#the-ai-council-agent-roles)
    *   [Sage (Analyst-Strategist)](#sage-analyst-strategist)
    *   [Seer (Catalyst)](#seer-catalyst)
    *   [Shaman (Deep Brain Consultant)](#shaman-deep-brain-consultant)
*   [The Akashic Record: Memory System](#the-akashic-record-memory-system)
*   [Emotional Intelligence](#emotional-intelligence)
*   [Interaction Modes](#interaction-modes)
*   [Remote Access](#remote-access)
*   [User Interface Concept](#user-interface-concept)
*   [Privacy & Security](#privacy--security)
*   [Installation](#installation)
    *   [Prerequisites](#prerequisites)
    *   [External Tools Setup](#external-tools-setup)
    *   [Python Environment Setup](#python-environment-setup)
    *   [Configuration (`.env`)](#configuration-env)
    *   [API Keys & Authentication](#api-keys--authentication)
*   [Hardware & VRAM Requirements](#hardware--vram-requirements)
    *   [Resource Management Toggle](#resource-management-toggle)
*   [Usage](#usage)
*   [Troubleshooting](#troubleshooting)
*   [Contributing](#contributing)
*   [License](#license)
*   [Design Document](#design-document)

## Vision & Philosophy

OracleAI aims to be more than just a chatbot; it's envisioned as a **cognitive partner**. Key principles guiding its development include:

*   **Local-First Processing:** Your data stays on your hardware. Core AI processing (LLM, STT, TTS, Memory) runs locally, ensuring privacy and offline capability.
*   **Privacy-Centric Design:** User data sovereignty is paramount. The Akashic Record utilizes local storage with robust encryption options (OS-level and application-level). External API calls are minimized, opt-in, secured, and transparent.
*   **Multi-Agent Synergy:** The council of Sage, Seer, and Shaman provides diverse perspectives (logical, creative, deep synthesis) for more comprehensive analysis and robust problem-solving.
*   **Deep & Evolving Memory (Akashic Record):** A persistent, multi-layered knowledge base allows OracleAI to learn from interactions, recall past context accurately, and synthesize information over extended periods, overcoming typical LLM context limitations.
*   **Integrated Emotional Intelligence:** OracleAI actively perceives and utilizes user emotional cues from both voice tone (SER) and text sentiment, enabling more empathetic, nuanced, and effective interactions.
*   **User Empowerment & Collaboration:** You are the central authority. Guide the council, verify insights, manage your Akashic Record, control settings, and participate directly in memory consolidation.
*   **Modularity & Extensibility:** Built with distinct components and clear interfaces for easier maintenance, upgrades, and future feature integration.

## Core Features

OracleAI integrates a wide array of advanced capabilities:

*   **AI Council:** Interact with three distinct, specialized AI agents:
    *   **Sage:** Logical Analyst-Strategist (Low Temperature LLM).
    *   **Seer:** Creative Catalyst & Intuitive Challenger (High Temperature LLM).
    *   **Shaman (Optional):** Deep Brain Consultant for intensive offline analysis (Powerful LLM, Moderate Temperature).
*   **Flexible LLM Backend:** Utilizes **KoboldCpp** (run separately by the user) allowing use of various GGUF-formatted Large Language Models (LLMs) and Vision Language Models (VLMs).
*   **Akashic Record Memory System:** A sophisticated, persistent memory architecture:
    *   **Chronicle:** Immutable raw logs of all interactions, emotions, and system events (JSONL).
    *   **Synthesis Store:** Structured knowledge base (SQLite recommended) containing:
        *   User-verified daily/weekly/monthly summaries with multiple detail levels and fidelity scores.
        *   Extracted entities (people, projects, concepts) with relationships (Knowledge Graph simulation).
        *   Key facts and decisions derived from conversations.
        *   Consolidated project/topic threads.
        *   Reports from Shaman's deep analysis.
    *   **Collaborative Memory Consolidation:** Unique user-in-the-loop process to verify and refine daily memory entries, minimizing information loss.
    *   **Memory Bank Context Scaler:** Intelligent RAG system dynamically selects and formats the most relevant memories to fit within the LLM's context window for each query.
    *   **User Profile & Preferences:** Stores goals, communication style, agent settings (SQLite).
    *   **Task & Action Queue:** Manages tasks assigned to agents (SQLite).
*   **Emotional Intelligence Suite:**
    *   **Speech Emotion Recognition (SER):** Analyzes user's voice tone using dedicated models (requires PyTorch/GPU).
    *   **Text Sentiment Analysis:** Processes transcribed text using VADER, NRCLex, TextBlob, etc. (CPU).
    *   Provides rich emotional context to LLMs.
    *   Enables emotional trend logging and analysis within the Akashic Record.
*   **High-Fidelity Speech-to-Text (STT):**
    *   Uses the `openai-whisper` library.
    *   Recommended model: `large-v2` for high accuracy.
    *   GPU-accelerated via PyTorch.
*   **Configurable Text-to-Speech (TTS):** Supports different engines per agent:
    *   **Piper TTS:** Default recommendation. Fast, CPU-based, supports multiple distinct high-quality voices via `.onnx` models.
    *   **Coqui XTTSv2 (Optional):** Enables high-quality voice cloning from audio samples. Expressive but requires PyTorch/GPU and adds latency. Ideal for agents like Seer where unique persona is key.
*   **Multimodal Vision:**
    *   Can process user-provided screenshots via multimodal GGUF models loaded in KoboldCpp.
    *   Visual information is used as context for the AI council.
*   **Advanced Web Search:**
    *   **Simple Search:** Quick information retrieval using DuckDuckGo snippets.
    *   **Deep Search:** In-depth investigation involving recursive web scraping (`requests`, `BeautifulSoup4`), analysis of relevant Reddit discussions (`praw`), and LLM-powered summarization.
    *   **Proxy Support:** Optional routing of search/scraping traffic via TOR (SOCKS proxy) or user-configured VPN.
    *   **Planned:** Support for multiple configurable search engines.
*   **Calendar Integration:**
    *   Connects securely (OAuth 2.0) to external calendar services (Google Calendar, Outlook Calendar planned).
    *   Fetches events and stores them in a local SQLite cache (`calendar.db`).
    *   Provides proactive reminders and uses schedule information as context for conversations and planning.
*   **Multiple Interaction Modes:**
    *   **Standard Interaction:** Real-time conversation with Sage and Seer.
    *   **Oracle Consultation:** Collaborative real-time session involving User, Sage, Seer, and Shaman (with adjustable responsiveness).
    *   **Shaman Focus:** Dedicates system resources to the Shaman for deep, offline analysis by idling Sage/Seer.
*   **Remote Access Capability:**
    *   Built-in **FastAPI** server exposes secure API endpoints.
    *   Allows interaction via a separate client application (web/mobile - *not included*) over the local network or secure tunnels (Tailscale recommended).
*   **Secure Backup & Restore:**
    *   Integrated functionality using **7-Zip** (requires external installation) to create password-protected, AES-256 encrypted archives of the entire Akashic Record for backup or transfer.

## Architecture Overview

OracleAI utilizes a modular Python architecture designed for flexibility and local processing:

1.  **LLM Backend:** Interfaces via HTTP API calls (`llm_interface.py`) to one or more external **KoboldCpp** instances serving GGUF models.
2.  **STT Engine:** Uses the **`openai-whisper`** library (`stt_interface.py`) leveraging PyTorch/GPU.
3.  **TTS Engine(s):** Supports **Piper TTS** (via `subprocess` calls managed by `tts_interface.py`) and/or **Coqui XTTSv2** (via `coqui-tts` library managed by `tts_interface.py`). Selection is agent-specific.
4.  **Emotion Analysis:** A dedicated module (`emotion_analyzer.py`) uses `librosa` (CPU) for features and SER models (PyTorch/GPU) for voice emotion, plus text sentiment libraries (CPU).
5.  **Memory System (Akashic Record):** Interacted with via a dedicated interface (`memory_interface.py`). Utilizes **SQLite databases** (with SQLCipher encryption) for structured data and **JSONL files** for raw logs. Future integration points for Vector DBs and Graph DBs.
6.  **Core Logic/Orchestration (`main.py`):** Manages the overall application state, interaction modes, agent selection, workflow sequencing (VAD -> STT -> Emotion -> Scaler -> LLM -> TTS), calls to interface modules, background task scheduling (`apscheduler`), and initialization.
7.  **Remote API (`remote_api.py`):** A **FastAPI** application defining endpoints, handling request/response validation (Pydantic), and calling core logic functions asynchronously.
8.  **Supporting Interfaces:** Dedicated modules for Web Search (`search_module.py`), Calendar (`calendar_interface.py`), Configuration (`config_loader.py`), Audio I/O (`audio_processing.py`), and Backup (`backup_module.py`).

## Component Interaction Diagram (Conceptual):
```
+-----------------+      +-----------------+      +-----------------+
| User Interface  |<---->|   Remote API    |<---->| External Client |
| (GUI / Local)   |      |  (FastAPI)      |      | (Web/Mobile App)|
+-------^---------+      +-------^---------+      +-----------------+
        |                        |
        | (Control/Display)      | (HTTP Requests)
        v                        v
+-------------------------------------------------------------------+
|                     OracleAI Core Orchestrator (`main.py`)        |
+-------^----------------------^----------------------^-------------+
        |                      |                      |
(Audio In/Out)       (Control/Data)         (Control/Data)
        |                      |                      |
+-------v---------+  +---------v---------+  +---------v-------------+
| Audio Processing|  | Emotion Analyzer  |  | STT Interface         |
| (PyAudio/SD/VAD)|  | (SER/Sentiment)   |  | (openai-whisper)      |
+-----------------+  +---------^---------+  +---------^-------------+
                               | (Audio Path)         | (Audio Path)
                               |                      | (Text Out)
+-----------------+  +---------v---------+  +---------v-------------+
| TTS Interface   |<-| LLM Interface     |<-| Memory Bank Context   |
| (Piper/XTTS)    |  | (KoboldCpp API)   |  | Scaler (RAG)          |
+-------^---------+  +---------^---------+  +---------^-------------+
        | (Text In)            | (Prompt Out)         | (Context Out)
(Audio Out)                    | (Response In)        | (Memory Query)
        |                      |                      |
+-------v---------+  +---------v---------+  +---------v-------------+
| Search Module   |  | Calendar Interface|  | Akashic Record        |
| (DDG/PRAW/Web)  |  | (API/calendar.db) |  | Interface (SQLite/JSONL)|
+-----------------+  +-------------------+  +-----------------------+
```

## The AI Council: Agent Roles

OracleAI features a council of specialized AI agents:

### Sage (Analyst-Strategist)
*   **Archetype:** The Wise Teacher/Philosopher. Represents logic, structure, and knowledge derived from data.
*   **Function:** Analyzes information from the Akashic Record and web searches, performs rigorous fact-checking, identifies logical patterns and inconsistencies, formulates clear step-by-step plans, evaluates risks and feasibility, provides objective, evidence-based guidance.
*   **Configuration:** Low LLM temperature (e.g., 0.0-0.3) for precision. Recommended TTS: Piper TTS with a calm, clear, articulate voice.
*   **Theme:** Ice/Winter, clarity, structure, wisdom, logic.

### Seer (Catalyst)
*   **Archetype:** The Visionary/Intuitive. Represents creativity, emotional insight, and possibility thinking.
*   **Function:** Challenges conventional approaches (plays devil's advocate), brainstorms novel solutions and ideas, interprets user emotional state (using SER/Sentiment data) to provide empathetic context, identifies hidden opportunities or potential future scenarios, facilitates dynamic and exploratory discussions.
*   **Configuration:** High LLM temperature (e.g., 0.6-1.2) for creativity. Recommended TTS: Coqui XTTSv2 for unique/cloned voice expressiveness, or a dynamic Piper voice.
*   **Theme:** Fire/Summer, passion, intuition, creativity, change, emotion.

### Shaman (Deep Brain Consultant)
*   **Archetype:** The Mediator/Mystic Synthesizer. Connects the raw data spirit world ("DataSide") with synthesized understanding.
*   **Function:** (Optional, primarily asynchronous/offline) Executes computationally intensive tasks delegated by the user or other agents. Performs deep analysis across the entire Akashic Record, identifies complex correlations and long-term patterns, synthesizes vast amounts of information, conducts extensive research.
*   **Configuration:** Utilizes the most powerful LLM available. Moderate temperature (e.g., 0.3-0.6, task-adjustable). Distinct Piper TTS voice (deep, resonant).
*   **Interaction:** Operates with significant latency, narratively framed as "hyperspace travel" (Moon, Mars, Jupiter, etc., indicating computational depth/time). Receives tasks via a queue. Delivers results as structured reports or updates to the Synthesis Store. Requires "Shaman Focus" mode on resource-constrained systems.
*   **Theme:** Spirit World/DataSide, depth, synthesis, patterns, connection, transformation, time.

## The Akashic Record: Memory System

At the heart of OracleAI lies the Akashic Record, a sophisticated, multi-layered memory system designed for persistence, context, and intelligent recall. It allows OracleAI to learn and evolve alongside the user.

*   **Chronicle (Immutable Logs):** The foundation. Raw, timestamped `.jsonl` files storing every interaction turn (user/AI text, SER/Sentiment data, system events). Provides complete traceability and serves as the source for all synthesized memory.
*   **Synthesis Store (Processed Knowledge):** Typically managed via **SQLite** (`synthesis.db` with SQLCipher encryption) for efficient querying and structured storage. Contains:
    *   **Permanent Memory:** User-defined critical facts.
    *   **Entities:** Detailed records of people, projects, concepts, tools, etc., including their types, statuses, tags, properties, and relationships (forming a knowledge graph).
    *   **Facts & Decisions:** Atomic, verifiable statements or choices extracted from conversations, linked to sources and entities.
    *   **Hierarchical Summaries:** Daily, weekly, and monthly summaries generated via collaborative (user-verified daily) and automated processes. Include multi-level narratives (short, medium, detailed, key points), keywords, sentiment overviews, and fidelity estimates.
    *   **Project/Topic Threads:** Consolidated, evolving summaries focused on specific long-running entities or themes.
    *   **Pattern Analysis Reports:** Insights generated by the Shaman's deep analysis of memory trends.
*   **Calendar Cache (`calendar.db`):** Local SQLite database storing events synced from external calendars.
*   **User Profile & Preferences (`profile.db`):** SQLite database holding user goals, preferences, contact info, agent configurations.
*   **Task & Action Queue (`tasks.db`):** SQLite database managing tasks assigned to AI agents, especially asynchronous Shaman tasks.
*   **Key Processes:**
    *   **Collaborative Daily Reflection:** A user-in-the-loop process ensuring high-fidelity daily memory creation.
    *   **Memory Bank Context Scaler (RAG):** Intelligently selects and formats the most relevant memory snippets to fit the LLM's context window for each query, enabling long-term context awareness.
    *   **Deep Pattern Weaving:** Shaman's autonomous analysis identifies trends and insights across the entire Akashic Record during user inactivity.

## Emotional Intelligence

OracleAI integrates emotional understanding as a core capability:

*   **Perception:** Utilizes Speech Emotion Recognition (SER) on user voice audio (via PyTorch/GPU) and Text Sentiment Analysis (VADER, NRCLex, TextBlob, etc.) on transcribed text (CPU).
*   **Contextualization:** Provides detected emotion and sentiment data as context to the LLM agents (Sage, Seer, Shaman).
*   **Response Adaptation:** Enables agents (especially Seer) to generate more empathetic, nuanced, and appropriate responses based on the user's perceived emotional state.
*   **Trend Analysis:** Emotional data is logged in the Chronicle and analyzed by the Shaman to identify long-term well-being patterns, correlations with topics/events, and provide potential self-reflection insights (always handled with privacy and user control in mind).

## Interaction Modes

OracleAI offers distinct modes to tailor the interaction:

1.  **Standard Interaction:** The default mode for real-time conversation with Sage and Seer. Ideal for typical queries, task assistance, and information retrieval. Shaman operates only on background tasks.
2.  **Oracle Consultation / Roundtable:** A user-activated collaborative mode where Sage, Seer, *and* Shaman participate actively in the conversation. The user can set Shaman's desired responsiveness level ("depth" or "distance" like Moon/Mars), balancing insight depth with latency. Supports various turn-taking styles and allows agents to continue discussion if the user is AFK. Excellent for complex brainstorming or multi-faceted problem-solving.
3.  **Shaman Focus:** A user-activated mode that idles/stops the Sage and Seer LLM backends to dedicate maximum system resources (especially VRAM) to the Shaman for computationally intensive, non-real-time analysis or tasks. User interaction is limited while this mode is active.
4.  **Mute State (Toggleable):** Suppresses unsolicited AI speech output in any mode.
5.  **Search Feature (Toggleable):** Enables Simple or Deep web search before AI responses are generated.

## Remote Access

OracleAI is designed for secure remote interaction:

*   **FastAPI Server:** A built-in server (`remote_api.py`) runs locally, exposing secure endpoints for core functionalities (transcription request, chat interaction, synthesis request, status checks, etc.).
*   **Client Application:** Requires a separate client application (web interface or mobile app - *currently not provided*) to communicate with the FastAPI server. For the best experience, the client should handle STT and TTS locally on the remote device.
*   **Networking:**
    *   **Local Network:** Access the API using the host PC's local IP address and configured port.
    *   **External Network:** **Tailscale** (mesh VPN) is highly recommended for simple and secure access without opening firewall ports. Alternatively, configure a traditional VPN or secure port forwarding. The API binds to `127.0.0.1` by default for security.

## User Interface Concept

While initially operable via command-line or basic interaction, a dedicated GUI is envisioned:

*   **Aesthetic:** "Oracle/Mystic Temple" theme – blending high-tech geometric circuitry with classical or esoteric elements. Color palettes differentiate agents (Cool blues/silvers for Sage, warm reds/oranges for Seer, deep purples/golds/cosmic for Shaman).
*   **Key Components:**
    *   Main chat interface with distinct agent visuals.
    *   Status dashboards (emotion readouts, system metrics, task queue).
    *   **Shaman Status Indicator:** Visual representation of Shaman's activity and latency (e.g., Merkaba traveling Moon-Mars-Jupiter path in the "DataSide").
    *   Controls for managing backend processes (KoboldCpp status/launch helpers).
    *   Settings panel for `.env` configuration and agent tuning.
    *   Future: Integrated Memory Bank browser/editor.
    *   Integrated controls for Akashic Record backup/restore (7-Zip).
*   **Iconography:** Custom set based on geometric line style (Brain, Heart, Eye, Network, Wave, Delta, Chart, Gear).
*   **Fonts:** Combination of clean tech fonts (e.g., Titillium Web, Exo 2) and stylized title fonts (e.g., Cinzel, Audiowide).

## Privacy & Security

User privacy and data security are foundational:

*   **Local-First:** All core processing and data storage occur on the user's machine.
*   **Encryption:**
    *   **OS-Level:** Full Disk Encryption (BitLocker/FileVault/LUKS) is strongly recommended.
    *   **Database:** Active SQLite databases (`synthesis.db`, `calendar.db`, etc.) use **SQLCipher** for transparent AES-256 encryption at rest.
    *   **Backup:** User-initiated backups via integrated **7-Zip** feature allow for strong AES-256 password protection of the entire Akashic Record archive.
*   **Network Security:** Remote API binds locally by default. External access requires user configuration and secure methods (Tailscale/VPN). All external API calls (Search, Calendar) use HTTPS.
*   **Data Minimization:** Only necessary data is sent to external APIs (opt-in features only).
*   **No Telemetry:** OracleAI does not send usage statistics or data externally without explicit, granular, anonymized user consent.
*   **Secure Configuration:** API keys and sensitive settings in `.env` should be protected by filesystem permissions. Use of OS credential stores is a future consideration.

## Installation

**NOTE:** Installation involves multiple steps, external tools, and Python dependencies including PyTorch with CUDA. Carefully follow each step. Docker support is planned for easier deployment in the future.

### Prerequisites
*   **Python:** Version 3.11.x recommended. Added to system PATH.
*   **Git:** For cloning the repository.
*   **NVIDIA GPU:** Required for GPU-accelerated STT (`openai-whisper`), SER model inference, and optional XTTSv2 TTS. Check VRAM requirements below.
*   **NVIDIA Drivers:** Latest stable version compatible with your GPU and target CUDA version.
*   **CUDA Toolkit:** Install the specific version required by the chosen PyTorch build (e.g., 11.8, 12.1, 12.4). Verify installation with `nvcc --version`.
*   **Audio Input/Output:** Functioning microphone and speakers/headphones configured in the OS.
*   **PortAudio:** Required by the `pyaudio` library. Installation varies by OS:
    *   *Linux:* Usually available via package manager (e.g., `sudo apt-get install portaudio19-dev`).
    *   *macOS:* Often installed via Homebrew (`brew install portaudio`).
    *   *Windows:* May require downloading binaries or installing as part of other audio software suites. Check `pyaudio` documentation for Windows specifics.
*   **7-Zip:** Install 7-Zip for backup/restore functionality. Ensure `7z.exe` is in the system PATH or provide the full path in the `.env` configuration.

### External Tools Setup
These must be downloaded and placed manually:
1.  **KoboldCpp:** Download the latest release executable for your OS from the official KoboldCpp repository/website. Run it separately and load the desired GGUF LLM/VLM models for Sage, Seer, and Shaman. Note the API URL (e.g., `http://127.0.0.1:5001`). You may need multiple instances if running agents on different models or machines.
2.  **Piper TTS:**
    *   Download the `piper` executable for your OS from Piper TTS releases.
    *   Download the desired `.onnx` voice model(s) and corresponding `.onnx.json` config files (e.g., from Hugging Face Piper voices page).
    *   Place the executable and voice files in a stable location accessible by OracleAI.

### Python Environment Setup
1.  **Clone Repository:** `git clone <OracleAI_repository_url>`
2.  **Navigate:** `cd OracleAI`
3.  **Create Virtual Environment:**
    *   `python -m venv .venv`
    *   Activate: `.\.venv\Scripts\activate` (Windows) or `source .venv/bin/activate` (Linux/macOS)
4.  **Install PyTorch (GPU Version):**
    *   **CRITICAL:** Visit [https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/).
    *   Select: Stable, Your OS (Windows/Linux), Pip, Python, Your **exact installed CUDA Toolkit version**.
    *   Copy and run the generated `pip install` command precisely. It will look similar to `pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cuXXX` (where `cuXXX` matches your CUDA version).
5.  **Install OracleAI Dependencies:**
    *   *(Method A - Lock File Preferred):* If a `requirements.lock` file exists: `pip install -r requirements.lock`
    *   *(Method B - requirements.in):* If `requirements.in` exists: `pip install pip-tools` then `pip-compile requirements.in -o requirements.txt` then `pip install -r requirements.txt`
    *   *(Method C - pyproject.toml):* If using `pyproject.toml` for dependencies: `pip install .`
    *   *(Ensure necessary libraries like `openai-whisper`, `librosa`, `transformers`, `pysqlcipher3` (or equivalent), `vaderSentiment`, `nrclex`, `textblob`, `requests[socks]`, `pyaudio`, `sounddevice`, `fastapi`, `uvicorn`, `python-dotenv`, `google-api-python-client`, `praw`, `BeautifulSoup4`, `coqui-tts` [if using XTTSv2], `apscheduler` are included in the dependency definition file).*

### Configuration (`.env`)
1.  Locate or create the `.env` file in the project root. Use `.env.example` as a template if provided.
2.  **Essential Settings:**
    *   `KOBOLDCPP_API_URL_SAGE`, `KOBOLDCPP_API_URL_SEER`, `KOBOLDCPP_API_URL_SHAMAN` (can be the same URL if running all on one instance, or different if distributed).
    *   `WHISPER_MODEL_NAME` (e.g., `large-v2`).
    *   `PIPER_EXECUTABLE_PATH` (Full path).
    *   `SER_MODEL_PATH` (Path to downloaded SER model).
    *   `AKASHIC_RECORD_PATH` (Directory to store Chronicle, DBs, etc.).
    *   `SEVENZIP_PATH` (Full path to `7z.exe`).
    *   `REMOTE_API_HOST` (e.g., `127.0.0.1` for local only, `0.0.0.0` for network access).
    *   `REMOTE_API_PORT` (e.g., `8000`).
3.  **Agent Specific Settings:** Define sections or prefixes for agent configs:
    *   `SAGE_TTS_ENGINE` (`piper`), `SAGE_PIPER_VOICE_MODEL`, `SAGE_PIPER_VOICE_CONFIG`, `SAGE_LLM_TEMPERATURE`.
    *   `SEER_TTS_ENGINE` (`xtts` or `piper`), `SEER_XTTS_SPEAKER_WAV` (if xtts), `SEER_PIPER_VOICE_MODEL` (if piper), `SEER_LLM_TEMPERATURE`.
    *   `SHAMAN_TTS_ENGINE` (`piper`), `SHAMAN_PIPER_VOICE_MODEL`, `SHAMAN_LLM_TEMPERATURE`.
4.  **Optional Settings:** `TOR_SOCKS_PROXY`, `USE_TOR_PROXY`, `LOG_LEVEL`.

### API Keys & Authentication
*   **Reddit:** Set `REDDIT_CLIENT_ID`, `REDDIT_CLIENT_SECRET`, `REDDIT_USER_AGENT` as environment variables or in `.env`.
*   **Calendar:** Run an initial setup script/command (part of OracleAI) to guide through the OAuth 2.0 flow for Google/Outlook. This will store necessary tokens securely (e.g., encrypted in `profile.db` or using OS credential store).

## Hardware & VRAM Requirements

*   **CPU:** Modern multi-core CPU recommended.
*   **RAM:** 32GB+ strongly recommended, especially if running large LLMs or Shaman. 16GB absolute minimum (likely only for small LLMs).
*   **GPU:** **NVIDIA GPU with sufficient VRAM is essential.**
    *   **Python Process VRAM:** ~4-8 GB needed for Whisper `large-v2` + SER Model + optional XTTSv2.
    *   **KoboldCpp VRAM:** Determined by LLM size and `-ngl` (layers offloaded).
        *   *Small LLMs (7B-13B):* +5-10 GB VRAM per instance.
        *   *Medium LLMs (30-34B):* +18-25 GB VRAM per instance.
        *   *Large LLMs (70B+):* +40GB+ VRAM per instance.
    *   **Total System VRAM:** Sum of Python process + all active KoboldCpp instances.
        *   *Basic (Sage/Seer with small LLMs):* ~16-24 GB total VRAM needed.
        *   *Medium (Sage/Seer with medium LLMs):* ~32-48 GB total VRAM needed.
        *   *Advanced (Including Shaman with large LLM):* 48GB+ VRAM highly recommended (e.g., RTX 3090/4090, A6000, RTX 6000 Ada).
*   **Multi-PC:** Distribute KoboldCpp instances across multiple networked PCs with GPUs to run larger models or more agents simultaneously.

### Resource Management Toggle
*   Provides a "Shaman Focus" mode to temporarily stop Sage/Seer KoboldCpp instances, freeing VRAM for the Shaman agent on systems with limited total VRAM.

## Usage

1.  **Start KoboldCpp Instance(s):** Launch KoboldCpp manually or via script. Load the GGUF models intended for Sage, Seer, and Shaman (if used). Ensure the API server is running and accessible at the URL(s) specified in `.env`. Configure GPU layers (`-ngl`) appropriately for your VRAM.
2.  **Activate Python Environment:** Open your terminal, navigate to the OracleAI directory, and activate the virtual environment (`.\.venv\Scripts\activate` or `source .venv/bin/activate`).
3.  **Run OracleAI:** Execute the main script: `python main.py` (or `python src/main.py`).
4.  **Interact (Local):** Use your configured microphone. Speak clearly. Use voice commands for mode switching, task assignment, memory queries, etc. (Specific commands TBD).
5.  **Interact (Remote):** Launch your separate client application (web/mobile) and configure it to connect to the OracleAI FastAPI server's IP address and port (e.g., `http://<OracleAI_PC_IP>:8000`). Ensure network connectivity (LAN or Tailscale/VPN).
6.  **Backup:** Use the integrated 7-Zip backup feature periodically.

## Troubleshooting

*   **Python Errors:** Check console output for tracebacks. Ensure all dependencies installed correctly (`pip check`). Verify Python version.
*   **PyTorch/CUDA Errors:** Confirm CUDA toolkit/driver compatibility with PyTorch build (`nvcc --version`). Check `torch.cuda.is_available()`.
*   **KoboldCpp Connection:** Verify KoboldCpp is running, API enabled, URL/port in `.env` match. Check firewall. Test API endpoint directly (e.g., with `curl` or browser).
*   **Piper/Whisper.cpp (if used):** Check executable paths in `.env`. Test executable manually from command line. Ensure model files exist and are accessible.
*   **Audio Issues:** Verify mic/speaker selection in OS. Check PortAudio installation. Adjust VAD `THRESHOLD` / `SILENCE_LIMIT` in code if needed.
*   **API Key/OAuth Errors:** Re-run Calendar auth flow. Double-check Reddit API keys in `.env`.
*   **Memory Access Errors:** Check permissions for the Akashic Record directory. Ensure SQLite databases are not corrupted (backups are crucial). Verify SQLCipher setup if used.

## Contributing

*(Details on how to contribute, coding standards, pull request process - To Be Added)*

## License

*(Specify the chosen open-source license - e.g., MIT, Apache 2.0. Note that dependencies like Coqui TTS, specific models, or libraries like SQLCipher may carry their own distinct licenses that users must adhere to.)*

## Design Document

## OracleAI: Comprehensive Design Document & Blueprint (v0.1)

**I. Core Philosophy, Vision, and Guiding Principles**

**1.1. Vision Statement:**
OracleAI is envisioned as an advanced, locally-run AI assistant framework functioning as a personalized strategic council. Its purpose extends beyond simple task execution or companionship; it aims to be a persistent, intelligent, and emotionally aware cognitive partner. OracleAI assists users in navigating complex personal and professional tasks, managing vast amounts of personal information effectively over long periods, achieving long-term goals through planning and analysis, fostering self-understanding via memory reflection and pattern detection, and providing contextually appropriate, empathetic support.

**1.2. Core Philosophy & Principles:**

*   **A. Local-First Processing & Privacy:**
    *   **Mandate:** All core computations (LLM inference, STT, primary TTS, memory storage, analysis) MUST reside and execute on user-controlled hardware. User data, particularly the sensitive contents of the Akashic Record, must not leave the local environment unless explicitly initiated by the user for specific, consented purposes (e.g., encrypted backup).
    *   **Rationale:** Ensures maximum user privacy, data sovereignty, control, and offline functionality. Mitigates risks associated with cloud-based data breaches or changes in service terms.
    *   **Implementation:** Utilize local LLM backends (KoboldCpp), local STT/TTS engines, local databases (SQLite), and file storage. Network calls are restricted to opt-in features.
*   **B. Multi-Agent Synergy:**
    *   **Mandate:** Employ multiple distinct AI agents with specialized roles, cognitive styles (simulated via prompting and temperature), and potentially different underlying LLMs.
    *   **Rationale:** Mimics the benefit of diverse perspectives in human teams. A logical agent (Sage) provides grounding, a creative agent (Seer) provides innovation, and a deep analytical agent (Shaman) provides synthesis. This structure facilitates more robust analysis, balanced decision support, and creative problem-solving than a monolithic AI.
    *   **Implementation:** Define distinct agent classes/configurations. Orchestrate turn-taking, collaborative task execution, and autonomous inter-agent communication protocols.
*   **C. Deep & Evolving Memory (Akashic Record):**
    *   **Mandate:** Implement a persistent memory system capable of storing raw interaction data, structured knowledge, synthesized summaries, user profiles, and task information over indefinite periods. The system must support efficient retrieval and facilitate continuous learning and refinement.
    *   **Rationale:** Overcomes the inherent context limitations of LLMs, enabling true long-term continuity, personalized understanding, and the ability to draw insights from past experiences.
    *   **Implementation:** Utilize a multi-component architecture (Chronicle, Synthesis Store, Profile DB, etc.) with robust data schemas and interfaces. Implement processes for summarization, entity extraction, relationship mapping, and pattern analysis.
*   **D. Integrated Emotional Intelligence:**
    *   **Mandate:** Actively perceive and interpret user emotional cues from both spoken language (voice tone via SER) and transcribed text (sentiment analysis). This emotional context must be available to the AI agents.
    *   **Rationale:** Enables significantly more natural, empathetic, and effective human-AI interaction. Allows the AI to tailor its responses, understand subtext, and track user well-being trends.
    *   **Implementation:** Integrate dedicated SER models and text sentiment analysis libraries. Log emotional data. Design prompts that instruct LLMs to consider this emotional context.
*   **E. User Empowerment & Collaboration:**
    *   **Mandate:** The user must remain the central authority. Provide mechanisms for users to guide AI behavior, explicitly add/edit/verify memories, configure agent parameters, manage privacy settings, and override AI suggestions.
    *   **Rationale:** Builds trust, ensures the AI aligns with user goals, allows correction of AI errors or biases, and makes the system a tool *for* the user, not an autonomous entity *acting upon* them.
    *   **Implementation:** Implement collaborative memory consolidation workflows, clear configuration options, potential memory editing interfaces, and transparent logging.
*   **F. Modularity & Extensibility:**
    *   **Mandate:** Design system components (interfaces for STT, TTS, LLM, Memory, Search, Calendar, Emotion Analysis, etc.) with well-defined APIs and minimal interdependencies.
    *   **Rationale:** Facilitates easier maintenance, testing, upgrades (e.g., swapping out an STT engine), replacement of components, and addition of new features or data sources in the future.
    *   **Implementation:** Utilize clear Python modules/classes, abstract interfaces, configuration-driven component selection. Design the Akashic Record format for potential external use.
*   **G. Practicality & Performance:**
    *   **Mandate:** Target reasonably high-end consumer hardware as a baseline. Optimize real-time interaction loops (Sage/Seer) for acceptable latency. Clearly delineate and manage user expectations for high-latency deep analysis tasks (Shaman).
    *   **Rationale:** Ensures the system is usable without requiring enterprise-level infrastructure, while still enabling powerful capabilities.
    *   **Implementation:** Efficient code, appropriate technology choices (e.g., Piper TTS for speed), GPU acceleration where beneficial (STT, SER, LLM), asynchronous processing for background tasks, resource management features (Shaman Focus mode).

**II. Multi-Agent Council Architecture**

The core intelligence comprises three distinct agents, forming a council:

**2.1. Agent "Sage" (The Analyst-Strategist):**
*   **Archetype:** The Wise Teacher, Philosopher, Logical Planner.
*   **Core Function:** Provides reasoned analysis, strategic planning, and knowledge synthesis based on verifiable data. Grounds the council in logic, facts, and structured thought.
*   **Responsibilities:**
    *   Analyzing user queries and context against the Akashic Record (Synthesis Store, Chronicle, KG).
    *   Performing fact-checking on information provided by the user or other agents.
    *   Conducting structured web searches (Simple Search primarily, or initiating Deep Search).
    *   Identifying logical patterns, trends, and inconsistencies in data.
    *   Formulating step-by-step plans, outlining strategies, defining action items.
    *   Evaluating risks, resource requirements, and feasibility of proposed actions.
    *   Generating clear, concise, evidence-based explanations and reports.
    *   Participating in collaborative memory consolidation, focusing on structured data extraction.
*   **LLM Backend Configuration:** KoboldCpp instance. Model choice should prioritize strong reasoning, instruction following, and potentially coding capabilities (e.g., CodeLlama variants, Mixtral Instruct, fine-tuned Llama 3).
*   **Temperature Setting:** Low (e.g., 0.0 - 0.3) to minimize randomness and ensure outputs are focused, deterministic, and closely adhere to provided context and instructions.
*   **TTS Configuration:** Piper TTS recommended. Voice profile should be calm, clear, articulate, measured, conveying wisdom and authority (e.g., inspired by Athena, Thoth, Spock).
*   **Interaction Style:** Analytical, structured, inquisitive (for clarification), objective, evidence-driven. Uses precise language.

**2.2. Agent "Seer" (The Catalyst):**
*   **Archetype:** The Visionary, Intuitive, Creative Spark, Empath.
*   **Core Function:** Provides creative insights, challenges assumptions, explores possibilities, interprets emotional context, and facilitates dynamic interaction. Acts as the council's source of novelty and human-centric perspective.
*   **Responsibilities:**
    *   Generating novel ideas, alternative solutions, and "outside-the-box" perspectives.
    *   Playing "devil's advocate" to stress-test plans and assumptions from Sage or the user.
    *   Interpreting SER and Text Sentiment data to understand user emotional state and subtext.
    *   Injecting emotional considerations and potential human impacts into discussions.
    *   Identifying potential synergies, unexpected opportunities, or future possibilities.
    *   Facilitating brainstorming sessions (with user or other agents).
    *   Asking probing "what if" questions.
    *   Participating in collaborative memory consolidation, focusing on capturing nuance and sentiment.
*   **LLM Backend Configuration:** KoboldCpp instance. Model choice should prioritize creativity, strong natural language understanding, and potentially role-playing capabilities (e.g., Llama 3 Instruct, Mixtral Instruct, specialized creative models). Can be the same base model as Sage but run with different system prompts and higher temperature.
*   **Temperature Setting:** High (e.g., 0.6 - 1.2) to encourage creativity, diversity in responses, and exploration of less probable paths.
*   **TTS Configuration:** Coqui XTTSv2 recommended for maximum expressiveness and potential voice cloning, accepting the higher resource cost and latency. Alternatively, a distinct, dynamic, and perhaps slightly unconventional Piper TTS voice. Voice profile: Expressive, intuitive, perhaps slightly passionate or whimsical (e.g., inspired by Pythia, Morgan Le Fay, Luna Lovegood).
*   **Interaction Style:** Inquisitive, challenging, associative, empathetic, focuses on potential and underlying meanings, uses richer or more metaphorical language.

**2.3. Agent "Shaman" (The Deep Brain Consultant):**
*   **Archetype:** The Mediator, Mystic Synthesizer, Deep Diver into the "DataSide".
*   **Core Function:** (Optional agent, primarily asynchronous) Performs computationally intensive, large-scale analysis, synthesis, and pattern recognition across the entire Akashic Record and external data sources during periods of user inactivity or when explicitly tasked. Bridges raw data and profound understanding.
*   **Responsibilities:**
    *   Executing complex, long-running tasks delegated via the Task Queue.
    *   Performing deep analysis of historical trends across all memory components (Chronicle, Synthesis Store, Calendar, Profile).
    *   Identifying subtle correlations, anomalies, and complex patterns invisible to surface analysis.
    *   Synthesizing vast amounts of information from deep searches or large document sets.
    *   Generating comprehensive reports, long-range forecasts, or complex scenario analyses.
    *   Potentially running NLP pipelines for Knowledge Graph population (NER, Relationship Extraction).
    *   Running periodic memory maintenance tasks (de-duplication, archiving proposals).
*   **LLM Backend Configuration:** Dedicated KoboldCpp instance, ideally running the largest, most capable GGUF model the user's hardware (potentially distributed or using advanced offloading) can support (e.g., 70B, 180B+).
*   **Temperature Setting:** Moderate (e.g., 0.3 - 0.6), adjustable per task via configuration or user request, balancing coherence with depth of exploration.
*   **TTS Configuration:** Piper TTS. Voice profile: Distinct, perhaps deep, resonant, calm, conveying profoundness (e.g., inspired by Hermes Trismegistus, The Ancient One).
*   **Interaction Model:** Asynchronous. Receives tasks via queue. Processing time is significant and represented by the "Hyperspace Travel" UI metaphor (Moon, Mars, Jupiter, etc.). Delivers results via updates to the Synthesis Store (e.g., `PatternAnalysisReports`) or potentially via TTS notification upon task completion. Can be queried by Sage/Seer during their autonomous discussions.
*   **Resource Management:** Requires dedicated resources. "Shaman Focus" mode allows users on constrained systems to idle Sage/Seer to allocate maximum VRAM/CPU to Shaman.

**III. Core Technology Stack & Interfaces (Overview)**

*   **Primary Language:** Python 3.11
*   **LLM Backend:** KoboldCpp (GGUF Models via Web API)
*   **STT:** `openai-whisper` library (PyTorch/GPU)
*   **TTS:** Piper TTS (CPU via `subprocess`) AND/OR Coqui XTTSv2 (GPU via `coqui-tts`/PyTorch) - Agent Configurable
*   **Emotion Analysis:** `librosa` (CPU), SER Models (PyTorch/Transformers/GPU), Text Sentiment Libraries (VADER, NRCLex, TextBlob - CPU)
*   **Memory Storage:** SQLite (with SQLCipher) for structured data, JSON Lines for Chronicle logs. Optional Vector DB (ChromaDB/FAISS) & Graph DB (Neo4j/SQLite Simulation).
*   **Configuration:** `.env` files via `python-dotenv`.
*   **Web Interaction:** `requests`, `BeautifulSoup4`, `praw`, `duckduckgo_search`. Optional `requests[socks]`.
*   **Calendar:** Google/Microsoft API clients (`google-api-python-client`, `msal`).
*   **Remote API:** FastAPI, Uvicorn.
*   **GUI (Conceptual):** PyQt/PySide, Kivy, or Web Tech + Electron/Tauri.
*   **Core Libraries:** `pyaudio`, `sounddevice`, `numpy`, `scipy`, `sqlite3`, `cryptography`, `pysqlcipher3`, `apscheduler`.
*   **Backup:** 7-Zip (via `subprocess`).
*   **Interface Modules:** Dedicated Python modules (`llm_interface.py`, `stt_interface.py`, `tts_interface.py`, `emotion_analyzer.py`, `search_module.py`, `calendar_interface.py`, `memory_interface.py`, `config_loader.py`, `audio_processing.py`, `remote_api.py`, `backup_module.py`) will abstract the core functionalities and interactions with these technologies.

**IV. The Akashic Record: Memory System Detailed Blueprint**

The Akashic Record is the central, persistent, and evolving knowledge base of OracleAI. It's designed to store diverse information types over long periods, facilitate intelligent retrieval, and enable deep synthesis by the AI council. It utilizes a combination of immutable logs, structured databases (primarily SQLite with SQLCipher encryption), and potentially specialized stores (Vector, Graph) in the future.

**4.1. Core Components & Storage Mechanisms:**

*   **A. The Chronicle (Immutable Raw Logs):**
    *   **Purpose:** Serves as the unalterable ground truth of all interactions and key system events. Provides complete traceability and the raw data source for all subsequent analysis and synthesis. Analogous to a detailed, timestamped journal.
    *   **Storage:** Series of JSON Lines files (`.jsonl`), typically one per day, stored in a dedicated directory (e.g., `[AKASHIC_RECORD_PATH]/Chronicle/YYYY-MM-DD_chronicle.jsonl`). JSON Lines format allows efficient appending without loading the entire file.
    *   **Encryption:** Files can be encrypted at rest using AES-256 via the `cryptography` library (requiring a master key at runtime) or rely on OS-level full disk encryption and the encrypted 7z backup feature. Direct file encryption adds complexity to appending and reading. *Decision: Prioritize SQLCipher for active DBs and 7z for backups; direct Chronicle file encryption is a lower priority optional enhancement.*
    *   **Schema per Line (JSON Object):**
        ```json
        {
          "timestamp": "ISO8601_DATETIME_Z", // Precise timestamp of event/turn end
          "turn_id": "UUID", // Unique identifier for this specific log entry/turn
          "session_id": "UUID", // Identifier grouping related turns within a single interaction session
          "speaker": "user" | "agent_sage" | "agent_seer" | "agent_shaman" | "system_memory_consolidation" | "system_event", // Source of the entry
          "text_raw_stt": "User's raw transcribed text from Whisper." | null, // Only for 'user' speaker
          "text_final_processed": "AI's final response text, processed user text, or system event description." | null,
          "audio_file_path_user": "relative/path/to/user_utterance_YYYYMMDD_HHMMSS_UUID.wav" | null, // Path to the saved audio for potential SER reprocessing or review
          "user_voice_emotion_ser": { // Only for 'user' speaker, if SER enabled
            "dominant_emotion": "happy" | "sad" | "angry" | "neutral" | "fear" | "surprise" | "disgust",
            "scores": {"happy": 0.8, "sad": 0.1, ...}, // Probability distribution
            "confidence": 0.85, // Overall confidence of the SER model
            "model_used": "model_name_version"
           } | null,
          "user_text_sentiment_vader": { // Only for 'user' speaker
            "compound": 0.85, "pos": 0.6, "neu": 0.3, "neg": 0.1
           } | null,
          "user_text_sentiment_textblob": { // Only for 'user' speaker
            "polarity": 0.7, "subjectivity": 0.6
           } | null,
          "user_text_emotion_nrc": { // Only for 'user' speaker
            "dominant_emotion": ["joy", "trust"] | null, // Can have multiple dominant if scores are close
            "scores": {"joy": 5, "trust": 5, "anger": 1, ...} // Raw counts or normalized scores
           } | null,
          "agent_llm_model_used": "koboldcpp_model_name.gguf" | null, // For AI turns
          "agent_llm_prompt_context_length_tokens": 12500 | null, // Estimated tokens sent to LLM
          "agent_llm_response_latency_ms": 1850 | null, // Time taken for LLM generation
          "agent_tts_engine_used": "piper" | "xtts" | null, // For AI turns
          "agent_tts_voice_used": "path/to/voice.onnx" | "path/to/speaker.wav" | null,
          "agent_tts_latency_ms": 350 | null, // Time taken for TTS synthesis
          "metadata_tags": ["project_phoenix", "user_frustrated", "memory_consolidation_review"], // Auto-generated or user-added tags for filtering/analysis
          "system_event_details": { // Only for 'system_event' speaker
            "event_type": "SHAMAN_TASK_STARTED" | "CALENDAR_SYNC_COMPLETE" | "CONFIG_CHANGED",
            "details": { /* Event-specific data */ }
           } | null
        }
        ```

*   **B. Synthesis Store (`synthesis.db` - SQLite Database):**
    *   **Purpose:** The primary repository for processed, structured, and synthesized knowledge derived from the Chronicle and user input. Designed for efficient querying and relational integrity.
    *   **Encryption:** SQLCipher enabled via `pysqlcipher3` or similar library, requiring the master key at runtime to open the database connection.
    *   **Core Tables:**
        *   **`PermanentMemory`:**
            *   `id` TEXT PRIMARY KEY (UUID)
            *   `text` TEXT NOT NULL
            *   `tags` TEXT -- Store as JSON array string '["tag1", "tag2"]'
            *   `added_at` TEXT (ISO8601 DATETIME)
            *   `last_accessed` TEXT (ISO8601 DATETIME)
        *   **`Entities`:**
            *   `id` TEXT PRIMARY KEY (UUID)
            *   `type` TEXT NOT NULL CHECK(type IN ('project', 'person', 'concept', 'tool', 'organization', 'location', 'event_ref')) -- event_ref links to Calendar DB
            *   `name` TEXT NOT NULL -- Primary name/title
            *   `aliases` TEXT -- JSON array string '["alias1", "alias2"]'
            *   `description_short` TEXT
            *   `description_medium` TEXT
            *   `status` TEXT -- e.g., 'active', 'completed', 'idea', 'reference'
            *   `tags` TEXT -- JSON array string
            *   `created_at` TEXT (ISO8601 DATETIME)
            *   `last_modified_at` TEXT (ISO8601 DATETIME)
            *   `properties_json` TEXT -- Store type-specific attributes as JSON blob (e.g., start/end dates for projects, role for person)
            *   `vector_embedding` BLOB NULL -- Optional, for semantic search on entity descriptions (Future)
        *   **`Relationships`:** (Many-to-many linking table for Entities)
            *   `id` INTEGER PRIMARY KEY AUTOINCREMENT
            *   `source_entity_id` TEXT NOT NULL REFERENCES Entities(id) ON DELETE CASCADE
            *   `target_entity_id` TEXT NOT NULL REFERENCES Entities(id) ON DELETE CASCADE
            *   `type` TEXT NOT NULL -- e.g., 'works_on', 'related_to', 'uses_tool', 'manages', 'reports_to', 'subconcept_of'
            *   `description` TEXT -- Optional context for the relationship
            *   `discovered_at` TEXT (ISO8601 DATETIME)
        *   **`FactsDecisions`:**
            *   `id` TEXT PRIMARY KEY (UUID)
            *   `type` TEXT NOT NULL CHECK(type IN ('decision', 'fact', 'hypothesis', 'question', 'milestone'))
            *   `timestamp_occurred` TEXT (ISO8601 DATETIME)
            *   `statement_text` TEXT NOT NULL
            *   `reasoning_summary` TEXT
            *   `confidence` REAL -- 0.0 to 1.0
            *   `tags` TEXT -- JSON array string
            *   `source_chronicle_turn_ids` TEXT -- JSON array string '["turn_id1", "turn_id2"]'
            *   `user_verified` INTEGER DEFAULT 0 -- 0=No, 1=Yes
            *   `created_at` TEXT (ISO8601 DATETIME)
        *   **`FactsDecisions_Entities`:** (Many-to-many linking table)
            *   `fact_decision_id` TEXT NOT NULL REFERENCES FactsDecisions(id) ON DELETE CASCADE
            *   `entity_id` TEXT NOT NULL REFERENCES Entities(id) ON DELETE CASCADE
            *   PRIMARY KEY (fact_decision_id, entity_id)
        *   **`Summaries`:**
            *   `id` TEXT PRIMARY KEY (UUID)
            *   `type` TEXT NOT NULL CHECK(type IN ('daily', 'weekly', 'monthly'))
            *   `date_key` TEXT NOT NULL -- 'YYYY-MM-DD', 'YYYY-WW', 'YYYY-MM' (Indexed)
            *   `created_at` TEXT (ISO8601 DATETIME)
            *   `user_verified` INTEGER DEFAULT 0 -- 0=No, 1=Yes, 2=Pending Review
            *   `fidelity_score` REAL -- 0.0 to 1.0
            *   `fidelity_method` TEXT -- 'heuristic', 'llm_assisted', 'user_rated'
            *   `fidelity_notes` TEXT
            *   `narrative_short` TEXT
            *   `narrative_medium` TEXT
            *   `narrative_detailed` TEXT
            *   `key_points_json` TEXT -- JSON array string '["point1", "point2"]'
            *   `extracted_keywords` TEXT -- JSON array string
            *   `sentiment_overview_json` TEXT -- JSON blob '{"avg_vader": 0.5, ...}'
            *   `source_ids` TEXT -- JSON array string of Chronicle turn IDs or lower-level Summary IDs
            *   `vector_embedding` BLOB NULL -- Optional, for semantic search (Future)
        *   **`Summaries_Entities`:** (Many-to-many linking table)
            *   `summary_id` TEXT NOT NULL REFERENCES Summaries(id) ON DELETE CASCADE
            *   `entity_id` TEXT NOT NULL REFERENCES Entities(id) ON DELETE CASCADE
            *   PRIMARY KEY (summary_id, entity_id)
        *   **`Summaries_FactsDecisions`:** (Many-to-many linking table)
            *   `summary_id` TEXT NOT NULL REFERENCES Summaries(id) ON DELETE CASCADE
            *   `fact_decision_id` TEXT NOT NULL REFERENCES FactsDecisions(id) ON DELETE CASCADE
            *   PRIMARY KEY (summary_id, fact_decision_id)
        *   **`ProjectTopicThreads`:** (Essentially specialized summaries linked to Project/Concept entities)
            *   `id` TEXT PRIMARY KEY (UUID)
            *   `entity_id` TEXT NOT NULL UNIQUE REFERENCES Entities(id) ON DELETE CASCADE -- One thread per project/topic entity
            *   `last_updated` TEXT (ISO8601 DATETIME)
            *   `user_verified` INTEGER DEFAULT 0
            *   `narrative_short` TEXT
            *   `narrative_medium` TEXT
            *   `narrative_detailed` TEXT
            *   `key_points_json` TEXT
            *   `current_status` TEXT -- Can be derived or explicitly set
            *   `key_milestones_ids` TEXT -- JSON array string linking to FactsDecisions IDs
            *   `outstanding_issues_ids` TEXT -- JSON array string linking to FactsDecisions IDs
            *   `referenced_summary_ids` TEXT -- JSON array string linking to relevant Summaries IDs
            *   `referenced_facts_ids` TEXT -- JSON array string linking to relevant FactsDecisions IDs
        *   **`PatternAnalysisReports`:**
            *   `id` TEXT PRIMARY KEY (UUID)
            *   `date_generated` TEXT (ISO8601 DATETIME)
            *   `title` TEXT
            *   `analyzed_period` TEXT -- e.g., 'YYYY-MM', 'Last 90 Days'
            *   `report_text` TEXT -- Narrative report from Shaman
            *   `key_findings_json` TEXT -- Structured findings '["finding1", {"finding2": "details"}]'
            *   `supporting_data_refs` TEXT -- JSON array linking to relevant Summary/Fact/Entity IDs
            *   `generated_by` TEXT DEFAULT 'agent_shaman'
*   **C. Calendar Cache (`calendar.db` - SQLite):**
    *   *Purpose:* Local cache of external calendar data.
    *   *Encryption:* SQLCipher enabled.
    *   *Tables:* `Events` (event_id, calendar_source, title, description, start_time DATETIME, end_time DATETIME, location, is_recurring, recurrence_rule, status, last_synced, raw_api_data_json), `Attendees` (attendee_id, event_id, email, display_name, response_status), `SyncStatus` (calendar_source, last_successful_sync, sync_token). Indexes on `start_time`, `end_time`, `event_id`, `attendee_email`.
*   **D. User Profile & Preferences (`profile.db` - SQLite):**
    *   *Purpose:* Stores user-specific settings and learned preferences.
    *   *Encryption:* SQLCipher enabled.
    *   *Tables:* `UserPreferences` (key TEXT PRIMARY KEY, value TEXT, description TEXT), `UserGoals` (id TEXT PRIMARY KEY, description TEXT, status TEXT, priority INTEGER, created_at TEXT, due_date TEXT, linked_entity_id TEXT NULL), `UserContacts` (id TEXT PRIMARY KEY, name TEXT, relationship_type TEXT, notes TEXT, linked_entity_id TEXT NULL), `AgentConfigurations` (agent_name TEXT PRIMARY KEY, tts_engine TEXT, voice_path TEXT, temperature_override REAL NULL).
*   **E. Task & Action Queue (`tasks.db` - SQLite):**
    *   *Purpose:* Manages asynchronous tasks for AI agents.
    *   *Encryption:* SQLCipher enabled.
    *   *Table:* `Tasks` (id INTEGER PRIMARY KEY AUTOINCREMENT, description TEXT, assigned_agent TEXT, status TEXT, priority INTEGER, created_at TEXT, started_at TEXT NULL, completed_at TEXT NULL, due_date TEXT NULL, result_summary_ref TEXT NULL, error_message TEXT NULL). Indexes on `status`, `assigned_agent`, `priority`.
*   **F. Knowledge Graph (Future):** Initially simulated using `Entities` and `Relationships` tables in `synthesis.db`. Future migration to a dedicated Graph DB (Neo4j) possible if complex traversal queries become necessary.
*   **G. Vector Store (Future):** External library/DB (ChromaDB, FAISS). Stores embeddings generated from `Summaries.narrative_medium` or Chronicle `text_final_processed` chunks. Metadata links embeddings back to the source `Summaries.id` or `Chronicle.turn_id`.

**4.2. Data Integrity & Consistency:**
*   Use database transactions for multi-step updates (e.g., adding an entity and its relationships).
*   Implement foreign key constraints (where applicable in SQLite) to maintain relational integrity.
*   Carefully manage UUID generation and usage for linking across tables/stores.
*   The "User Verification" flags on summaries are crucial for tracking data quality.
*   Implement robust error handling in the `memory_interface.py` for all database/file operations.

**4.3. Key Memory System Processes & Workflows:**

These processes describe how information flows into, is synthesized within, and retrieved from the Akashic Record.

*   **A. Collaborative Daily Reflection & Structured Extraction:**
    *   **Goal:** To create a high-fidelity, user-verified summary and extract key structured information from the day's interactions, minimizing information loss inherent in pure summarization. This is the primary mechanism for populating the Synthesis Store accurately.
    *   **Trigger:** Configurable. Options:
        1.  Automatically at the end of the day (e.g., midnight local time via `apscheduler`).
        2.  Automatically upon the first user interaction of a new day.
        3.  Manually triggered by user command ("OracleAI, let's review yesterday").
    *   **Primary Agents Involved:** Sage (for structure/logic), Seer (for nuance/emotion), User (for verification/guidance).
    *   **Workflow Steps:**
        1.  **Load Chronicle:** The system retrieves all entries from the previous day's `YYYY-MM-DD_chronicle.jsonl` file via `memory_interface`.
        2.  **Initiate Session:** Announce the start of the reflection session to the user.
        3.  **LLM Task 1 (Structured Extraction - Sage):**
            *   *Input:* Full text content from the day's Chronicle entries.
            *   *Prompt (Sage):* "Analyze the following conversation log from [Date]. Identify and list concisely: 1. **New Entities** mentioned (people, projects, organizations, key concepts, tools) with their apparent type. 2. **Updates to Existing Entities** (e.g., project status changes, new relationships). 3. **Key Facts** stated or learned. 4. **Decisions Made** (including brief reasoning if stated). 5. **Action Items** assigned or implied. For each item, suggest relevant tags and cite the source Chronicle turn ID(s)."
            *   *Output:* Structured list of potential entities, facts, decisions, action items.
        4.  **User Review 1 (Verification of Structured Data):**
            *   The system presents the LLM's extracted items clearly to the user (via GUI or formatted text).
            *   User Interface allows user to: Confirm items, Correct details (names, types, statements), Delete irrelevant/incorrect items, Add missing items.
        5.  **Storage 1 (Update Synthesis Store):**
            *   Verified/edited items are processed by `memory_interface`.
            *   New entities added to `Entities` table (generating UUIDs). Existing entities updated. Relationships added/updated.
            *   New facts/decisions added to `FactsDecisions` table (generating UUIDs), linked to entities and Chronicle turns.
            *   Action items potentially added to `Tasks` queue or noted as facts.
        6.  **LLM Task 2 (Narrative Summary Generation - Seer/Sage Collab):**
            *   *Input:* Full text content from Chronicle AND the *verified* structured items from Step 5.
            *   *Prompt (Seer/Sage - potentially one drafts, the other refines, or a joint prompt):* "Based on the conversation log from [Date] and the verified key information below: [Verified Entities/Facts/Decisions list], generate narrative summaries capturing the day's essence:
                *   `short` (1 sentence max 25 words): The absolute core takeaway.
                *   `medium` (3-5 sentences max 75 words): Main activities, topics, and overall mood/sentiment shift.
                *   `detailed` (1-2 paragraphs max 200 words): Elaborate on main activities, incorporate key decisions/facts, mention significant emotional context (referencing sentiment overview), highlight unresolved questions or next steps.
                *   `key_points` (3-5 bullets): Most critical takeaways.
                *   Also suggest 3-5 relevant `extracted_keywords` for the day.
                *   Also provide a `sentiment_overview` JSON summarizing average VADER/TextBlob scores and dominant NRC emotions for the day's user turns."
            *   *Output:* JSON object containing the different summary levels, keywords, and sentiment overview.
        7.  **User Review 2 (Verification of Narrative Summaries):**
            *   System presents the generated summaries (perhaps starting with medium, allowing user to request detailed) and keywords.
            *   User confirms or suggests edits to the narrative content or keywords.
        8.  **LLM Task 3 (Fidelity Estimation - Sage/LLM):**
            *   *Input:* Final detailed summary, source Chronicle text, verified structured items.
            *   *Prompt:* "Evaluate the fidelity of the final detailed summary compared to its source material (log and structured items). Assign a score (0.0-1.0) reflecting critical information preservation and lack of misrepresentation. Provide brief justification."
            *   *Output:* Fidelity score, method ('llm_assisted'), justification notes.
        9.  **Storage 2 (Finalize Daily Summary):**
            *   The finalized `daily_summary` object (including all narrative levels, keywords, sentiment overview, user_verified=True, fidelity estimate, links to entities/facts, source Chronicle info) is saved to the `Summaries` table in `synthesis.db` via `memory_interface`.
        10. **Session End:** Inform user reflection is complete.

*   **B. Hierarchical & Thematic Summarization:**
    *   **Goal:** Create higher-level overviews (weekly, monthly) and consolidate topic-specific information (project/topic threads) to manage context scale and provide broader perspectives.
    *   **Trigger:** Periodic background tasks scheduled via `apscheduler` (e.g., weekly on Sunday night, monthly on the 1st) or triggered by significant activity related to a project/topic.
    *   **Primary Agent Involved:** Shaman (ideal due to potential data volume) or Sage.
    *   **Workflow (Weekly Example):**
        1.  Load all *verified* `daily_summaries` for the past week from `synthesis.db`.
        2.  Load associated `facts_decisions` and `entities` referenced in those summaries.
        3.  **LLM Task (Summarization):** Prompt: "Synthesize the following verified daily summaries and associated key information from week [Week Number], [Year]. Generate multi-level narrative summaries (short, medium, detailed, key points) focusing on overarching themes, significant progress on projects/goals, major decisions, overall sentiment trends, and unresolved items carrying forward. Suggest keywords for the week."
        4.  **LLM Task (Fidelity Estimation):** Evaluate the weekly summary against the input daily summaries.
        5.  **Storage:** Save the new `weekly_summary` entry to the `Summaries` table, including links (`source_daily_summary_ids`). User verification is optional for these higher levels but can be flagged (`user_verified=0`).
    *   **Workflow (Project/Topic Thread Update):**
        1.  Identify the target `entity_id` for the project/topic.
        2.  Retrieve the existing `project_or_topic_threads` entry (if any).
        3.  Retrieve all *new* `daily_summaries`, `facts_decisions` linked to this `entity_id` since the last update.
        4.  **LLM Task (Update):** Prompt: "Update the project thread summary for '[Entity Name]' based on the following new information from recent logs/summaries: [New Summaries/Facts/Decisions]. Incorporate new developments, update the overall status narrative, add links to new key milestones or issues. Retain essential previous context."
        5.  **Storage:** Update the relevant entry in the `ProjectTopicThreads` table, setting the `last_updated` timestamp.

*   **C. Memory Bank Context Scaler (Real-time RAG):**
    *   **Goal:** Dynamically construct the most relevant context from the vast Akashic Record to fit within the target LLM's token limit for each real-time query.
    *   **Trigger:** Executed by `main.py` immediately before calling `llm_interface.generate` for Sage or Seer.
    *   **Inputs:** Current user query text, recent conversation history (e.g., last 3-5 turns), target token budget (based on LLM context window minus space for prompt/query/response).
    *   **Workflow Steps:**
        1.  **Initial Candidate Retrieval:**
            *   **Mandatory:** Fetch all entries from `PermanentMemory`.
            *   **Temporal:** Fetch latest N `daily_summaries`, latest `weekly_summary`, latest `monthly_summary`.
            *   **Entity Linking:** Identify key entities mentioned in the query/recent history using simple keyword matching or NER (future). Fetch corresponding entries from `Entities` table and potentially their linked `FactsDecisions` or `ProjectTopicThreads` summary (`narrative_short` or `key_points`).
            *   **Keyword Search:** Perform keyword search (using query terms) across indexed fields in `Summaries`, `FactsDecisions`, `Entities` within `synthesis.db`.
            *   **Semantic Search (Future):** Embed query, search Vector Store, retrieve IDs of top K similar summaries/Chronicle snippets. Fetch corresponding text from `synthesis.db` or Chronicle files.
            *   **Calendar Context:** Query `calendar.db` for events happening today/tomorrow or related to keywords/entities mentioned.
        2.  **Relevance Ranking & Scoring:**
            *   Assign relevance scores to all retrieved candidates based on: Vector similarity score (if used), keyword match density, recency, explicit entity links, source type priority (e.g., Permanent Memory > Verified Daily Summary > Monthly Summary > Raw Chronicle Snippet), summary fidelity score.
            *   (Optional Advanced) Use a fast LLM for re-ranking the top M candidates based on direct relevance to the immediate query.
        3.  **Iterative Budget Fitting & Selection:**
            *   Initialize empty context string and remaining token budget.
            *   Add `PermanentMemory` entries first if budget allows. Update budget.
            *   Sort remaining candidates by relevance score (descending).
            *   Iterate through sorted candidates:
                *   Select representation level based on remaining budget and item type (e.g., try `narrative_medium`, if too large try `narrative_short`, then `key_points`, then skip). Estimate token count using `tiktoken` or heuristics.
                *   If selected representation fits budget: Append to context string (with clear header like `[Daily Summary YYYY-MM-DD]: ...`), subtract tokens from budget.
                *   If budget is full or candidates exhausted, stop.
        4.  **Formatting:** Ensure final context string is clean, well-structured, and clearly delineates different memory sources.
    *   **Output:** A single string containing the curated context, ready for injection into the LLM prompt.

*   **D. Deep Pattern Weaving (Shaman - Autonomous):**
    *   **Goal:** Uncover long-term trends, correlations, and insights not apparent from individual logs or summaries.
    *   **Trigger:** Scheduled background task (e.g., nightly, weekly via `apscheduler`).
    *   **Primary Agent Involved:** Shaman (Deep Brain).
    *   **Workflow Examples:**
        1.  **Sentiment Trend Analysis:** Query `Summaries` table for daily `sentiment_overview_json` over weeks/months. Calculate moving averages, identify significant dips/peaks. Correlate with `extracted_keywords` or linked `Entities` from the same periods using SQL queries or Pandas DataFrames (if data loaded).
        2.  **Topic Frequency Analysis:** Analyze `extracted_keywords` from `Summaries` or run Topic Modeling (NMF/LDA) on Chronicle text over time. Identify recurring, emerging, or fading topics.
        3.  **Goal Progress Correlation:** Query `UserGoals` from `profile.db` and related `FactsDecisions` (milestones) or `ProjectTopicThreads` status updates from `synthesis.db`. Correlate goal progress with sentiment trends or calendar density.
        4.  **Behavioral Pattern Identification:** Analyze `metadata_tags` in Chronicle or interaction patterns (e.g., frequency of using specific commands, types of questions asked).
    *   **Output:** Generates `PatternAnalysisReports` stored in `synthesis.db`, potentially proposes updates to `User Profile` (e.g., inferred preferences - requires user confirmation step).

*   **E. Word Frequency Indexing (Optional Analysis):**
    *   **Goal:** Provide high-level thematic indicators based on vocabulary usage.
    *   **Trigger:** Background task run after Chronicle log finalization or periodically.
    *   **Process:** Reads Chronicle text, performs stop-word removal and lemmatization (using `nltk` or `spaCy`), calculates word frequencies. Stores per-log index (e.g., `YYYY-MM-DD_index.json`) and updates a master cumulative index (e.g., `master_word_index.json` or SQLite table).
    *   **Usage:** Primarily by Shaman for analyzing thematic shifts over long periods. Limited use as a minor retrieval cue or highly truncated context hint for real-time agents.

*   **F. Memory Maintenance:**
    *   **Goal:** Keep the Akashic Record relevant and manageable over time.
    *   **Trigger:** Periodic background tasks (Shaman) or user command.
    *   **Processes:**
        *   **De-duplication/Merging:** Use semantic search or LLM analysis to identify highly similar `Entities` or `FactsDecisions`. Propose merges to the user.
        *   **Archiving:** Define rules (e.g., archive daily summaries older than X months if a monthly summary exists and is verified) or allow user to manually archive entries (set a status flag). Archived data might be excluded from default retrieval but still searchable.
        *   **Integrity Checks:** Periodically verify links between tables/files.

**V. Core Modules & Functionalities (Elaborated)**

This section details the responsibilities and interactions of the key Python modules comprising OracleAI.

*   **`llm_interface.py`:**
    *   **Purpose:** Centralized communication gateway to all configured KoboldCpp LLM instances.
    *   **Responsibilities:**
        *   Load KoboldCpp API endpoint URLs (for Sage, Seer, Shaman) from configuration.
        *   Implement function `generate(agent_name, prompt, temperature=None, max_tokens=None, ...)` to send generation requests.
        *   Select correct endpoint based on `agent_name`.
        *   Retrieve default temperature for the agent from config, allow override via function parameter.
        *   Construct the JSON payload compatible with KoboldCpp's `/api/v1/generate` endpoint (or relevant multimodal endpoint if processing images).
        *   Use the `requests` library to execute POST requests. Handle timeouts and connection errors robustly.
        *   Parse JSON responses, extracting generated text (e.g., `response['results'][0]['text']`).
        *   Handle potential API errors returned by KoboldCpp (e.g., model not loaded, context overflow).
        *   Log request parameters (agent, temp, prompt length) and response details (latency, output length).
    *   **Key Interactions:** Called by `main.py` (for agent responses), `memory_interface.py` (for summarization/extraction tasks), `search_module.py` (for deep search summarization).

*   **`stt_interface.py`:**
    *   **Purpose:** Provide a consistent interface for Speech-to-Text functionality using `openai-whisper`.
    *   **Responsibilities:**
        *   Initialize the Whisper model at startup (`whisper.load_model(config.WHISPER_MODEL_NAME)`), loading to GPU via PyTorch.
        *   Implement function `transcribe_audio(audio_file_path)`:
            *   Takes the path to a saved `.wav` file (from `audio_processing`).
            *   Calls `model.transcribe(audio_file_path, language='en', fp16=True, ...)` potentially requesting word timestamps (`word_timestamps=True`) if needed for advanced SER alignment.
            *   Handles exceptions during transcription (e.g., file not found, model errors).
            *   Logs transcription time.
        *   Implement function `get_transcription_result(result_dict)` to extract text and potentially format timestamps if needed.
    *   **Key Interactions:** Called by `main.py` after `audio_processing` saves an utterance. Output text passed to `main.py` and `emotion_analyzer.py`. Audio path also passed to `emotion_analyzer.py`.

*   **`tts_interface.py`:**
    *   **Purpose:** Provide a unified interface for text synthesis using either Piper TTS or Coqui XTTSv2, based on agent configuration.
    *   **Responsibilities:**
        *   Initialize Coqui TTS engine (`TTS(...)`) at startup if XTTSv2 is configured for *any* agent. Store the object.
        *   Implement function `synthesize(text, agent_config)`:
            *   Reads `agent_config['tts_engine']`.
            *   If 'piper': Calls internal `_synthesize_piper(text, agent_config)`.
            *   If 'xtts': Calls internal `_synthesize_xtts(text, agent_config)`.
            *   Returns standardized output tuple `(audio_data, sample_rate)` or `(None, None)`.
        *   Internal `_synthesize_piper`:
            *   Gets paths (`piper_exe`, `onnx_model`, `json_config`) from config/`agent_config`.
            *   Constructs `subprocess` command.
            *   Manages temporary output WAV file.
            *   Executes Piper, pipes text via stdin, captures stderr.
            *   Reads audio data (bytes) and sample rate from output WAV using `wave`.
            *   Cleans up temp file. Returns `(audio_bytes, sample_rate)`.
        *   Internal `_synthesize_xtts`:
            *   Gets `speaker_wav` path from `agent_config`.
            *   Calls `tts_engine_object.tts(...)` using the pre-initialized Coqui TTS object.
            *   Handles potential exceptions.
            *   Returns `(audio_data_list_or_numpy, sample_rate)`.
        *   Includes robust error handling and logging for both engines.
    *   **Key Interactions:** Called by `main.py` after receiving an LLM response. Output passed to `audio_processing.py` for playback.

*   **`emotion_analyzer.py`:**
    *   **Purpose:** Analyze audio and text to provide emotional context.
    *   **Responsibilities:**
        *   Initialize SER model (PyTorch/Transformers, GPU) and Text Sentiment analyzers (VADER, NRCLex, TextBlob) at startup.
        *   Implement function `analyze_emotion(audio_file_path, text)`:
            *   Calls internal `_run_ser(audio_file_path)`.
            *   Calls internal `_run_text_sentiment(text)`.
            *   Combines results into a structured dictionary.
        *   Internal `_run_ser`: Loads audio with `librosa`, extracts features (MFCCs etc.), performs inference with SER model, returns emotion labels/scores/confidence.
        *   Internal `_run_text_sentiment`: Runs text through VADER, NRCLex, TextBlob, returns dictionary of scores/labels.
        *   Handles errors in analysis gracefully (e.g., returning null if SER fails).
    *   **Key Interactions:** Called by `main.py` after STT. Output dictionary passed to `main.py` for logging (Chronicle) and inclusion in LLM prompts.

*   **`search_module.py`:**
    *   **Purpose:** Execute web searches (Simple and Deep).
    *   **Responsibilities:**
        *   Implement `perform_search(query, search_type='simple', use_proxy=False)`:
            *   Checks `search_type`.
            *   If 'simple': Calls `duckduckgo_search.text()`. Formats results.
            *   If 'deep': Orchestrates the multi-step deep search process:
                1.  Initial DDG search.
                2.  Iterate results: Check `robots.txt`, scrape allowed pages (`requests`/`BeautifulSoup4`), potentially use LLM (`llm_interface`) for relevance filtering/summarization of scraped pages. Handle scraping errors/blocks.
                3.  Identify relevant subreddits (potentially LLM-assisted).
                4.  Search Reddit using `praw`.
                5.  Filter relevant posts (potentially LLM-assisted).
                6.  Summarize relevant Reddit content (`llm_interface`).
                7.  Combine and synthesize web + Reddit findings (`llm_interface`).
            *   Handles proxy configuration for `requests` if `use_proxy` is True (reads proxy URL from config).
        *   Includes error handling for network issues, API limits (PRAW), scraping blocks.
    *   **Key Interactions:** Called by `main.py` when search is triggered before an LLM response. Output string fed back into LLM prompt context.

*   **`calendar_interface.py`:**
    *   **Purpose:** Manage interaction with external calendar APIs and the local cache.
    *   **Responsibilities:**
        *   Handle OAuth 2.0 authentication flow (initial setup, token refresh). Securely store/retrieve tokens (using OS credential store or encrypted file).
        *   Implement `sync_calendar(calendar_source)`: Fetches events from API (using sync tokens if possible), parses data, calls `memory_interface` to update `calendar.db`.
        *   Implement `get_events(start_date, end_date, query=None)`: Queries the local `calendar.db` via `memory_interface` for events within a range, optionally filtering by query terms.
    *   **Key Interactions:** Called by background scheduler (`apscheduler` in `main.py`) for periodic sync. Called by `main.py` or `Context Scaler` to retrieve event data for LLM context or user queries.

*   **`memory_interface.py`:**
    *   **Purpose:** Provide a unified, abstracted API for all interactions with the Akashic Record storage components (Chronicle JSONL, SQLite DBs). Hides the underlying storage details.
    *   **Responsibilities:**
        *   Manage SQLite database connections (using `sqlite3` with `pysqlcipher3` hooks for encryption, requiring master key). Handle connection pooling if needed.
        *   Implement functions for CRUD operations on each SQLite table (e.g., `add_entity`, `get_entity`, `update_summary`, `find_summaries_by_date`, `get_tasks_by_status`, `add_calendar_event`, `get_calendar_events`). Use parameterized queries to prevent SQL injection. Handle transactions for multi-step updates.
        *   Implement `append_chronicle(turn_data)`: Opens the correct daily `.jsonl` file in append mode, writes the JSON entry, handles file locking if necessary (though less critical for append-only).
        *   Implement `read_chronicle(date_or_path)`: Reads entries from a specific Chronicle file.
        *   (Future) Interface functions for Vector Store (add embeddings, search similar).
        *   (Future) Interface functions for Knowledge Graph (add nodes/edges, query relationships).
        *   Includes robust error handling for file I/O and database operations.
    *   **Key Interactions:** Used extensively by almost all other modules (`main`, `Context Scaler`, `Shaman Process`, `calendar_interface`, `backup_module`) to read or write persistent data.

*   **`config_loader.py`:**
    *   **Purpose:** Load application settings from `.env` file.
    *   **Responsibilities:** Uses `python-dotenv`'s `load_dotenv()`. Provides functions or a config object to access settings (e.g., `config.get('KOBOLDCPP_API_URL_SAGE')`). Performs basic validation (e.g., check if required paths exist).
    *   **Key Interactions:** Called once at startup by `main.py`. Config object/values used by most other modules.

*   **`audio_processing.py`:**
    *   **Purpose:** Handle low-level audio input and output.
    *   **Responsibilities:**
        *   Initialize `pyaudio`. Find input/output devices.
        *   Implement `start_recording(callback_on_utterance)`: Opens microphone stream, performs VAD (checks RMS energy against `THRESHOLD`, detects silence > `SILENCE_LIMIT`), buffers audio during speech, saves complete utterance to a unique temporary WAV file upon silence detection, calls the provided callback function with the WAV file path.
        *   Implement `play_audio(audio_data, sample_rate)`: Uses `sounddevice.play(audio_data, samplerate=sample_rate)` and `sounddevice.wait()` for synchronous playback. Handles potential format differences between Piper/XTTSv2 outputs.
    *   **Key Interactions:** `main.py` calls `start_recording`. The callback triggers STT in `main.py`. `main.py` calls `play_audio` after TTS.

*   **`remote_api.py`:**
    *   **Purpose:** Expose OracleAI functionality via a web API for remote clients.
    *   **Responsibilities:**
        *   Defines FastAPI application (`app = FastAPI()`).
        *   Defines Pydantic models for request bodies and response structures (data validation).
        *   Implements API endpoints (e.g., `@app.post("/chat")`, `@app.post("/transcribe")`, `@app.get("/status")`) using `async def`.
        *   Endpoints call the relevant functions in other core modules (`llm_interface`, `stt_interface`, `memory_interface`, etc.) asynchronously where appropriate (`await asyncio.to_thread(...)` for synchronous functions).
        *   Handles API authentication/authorization (if implemented, e.g., API keys, JWT).
        *   Returns standard HTTP responses with JSON bodies or potentially audio files.
    *   **Key Interactions:** Run by `main.py` (using `uvicorn`). Receives requests from external clients. Calls other OracleAI modules to fulfill requests.

*   **`backup_module.py`:**
    *   **Purpose:** Handle creation of encrypted/unencrypted backups of the Akashic Record.
    *   **Responsibilities:**
        *   Implement `create_backup(output_path, encrypt=True, password=None)`:
            *   Gets the path to the main Akashic Record directory from config.
            *   Gets the path to `7z.exe` from config.
            *   Constructs the `7z a ...` command line arguments. Includes `-p{password}` and `-mhe=on` if `encrypt` is True (requires password).
            *   Uses `subprocess.run` to execute 7-Zip.
            *   Checks return code and handles errors.
    *   **Key Interactions:** Called by `main.py` based on user command or potentially a scheduled task.

*   **`main.py`:**
    *   **Purpose:** Main application entry point, orchestrator, local interaction loop manager.
    *   **Responsibilities:**
        *   Parse command-line arguments.
        *   Initialize logging.
        *   Load configuration via `config_loader`.
        *   Initialize all interface modules (LLM, STT, TTS, Emotion, Memory, Calendar, Search, Backup). Load necessary models (Whisper, SER, XTTS). Connect to databases.
        *   Start background scheduler (`apscheduler`) for tasks like calendar sync, periodic summarization, Shaman analysis triggers.
        *   Start FastAPI server (`remote_api.py`) using `uvicorn` (likely in a separate thread or using `asyncio` management).
        *   Initialize agent states and interaction mode.
        *   Enter main local interaction loop (if local interaction enabled):
            *   Call `audio_processing.start_recording` with a callback.
            *   Callback function orchestrates the STT -> Emotion -> Log -> Scaler -> LLM -> Log -> TTS -> Playback sequence as detailed in Workflow VII.A.
            *   Handle user commands parsed from STT output (mode changes, memory queries, task assignments).
            *   Manage agent turn-taking based on current interaction mode.
        *   Handle graceful shutdown (close DB connections, stop threads/scheduler, save state).

**VI. Interaction Modes**

*   **Standard Interaction:** Default real-time mode. Sage & Seer active. Shaman background only. Standard request-response loop. Limited inter-agent chat during user AFK.
*   **Oracle Consultation / Roundtable:** User-activated mode for collaboration. Sage, Seer, & Shaman active. User sets Shaman's responsiveness ('Moon', 'Mars', etc.). Supports structured or dynamic turn-taking. Allows continued Sage/Seer discussion during user AFK, potentially queuing deeper Shaman tasks.
*   **Shaman Focus:** User-activated mode. Stops/idles Sage & Seer KoboldCpp instances via `subprocess` or OS signals. Reallocates resources to Shaman's KoboldCpp instance. User interaction limited to tasking Shaman. High latency expected and communicated via UI. Mode is toggled back to restart Sage/Seer.

**VII. Data Flow & Workflows (Detailed Descriptions)**

*   **A. Local User Interaction Cycle:**
    1.  **Input:** `audio_processing` detects end of speech via VAD -> saves `utterance.wav`.
    2.  **STT:** `main` calls `stt_interface.transcribe_audio(wav_path)` -> returns `text`, `timestamps`.
    3.  **Emotion:** `main` calls `emotion_analyzer.analyze_emotion(wav_path, text)` -> returns `emotion_data`.
    4.  **Logging:** `main` calls `memory_interface.append_chronicle` with turn details (user, text, emotion, audio path).
    5.  **Context Scaling:** `main` calls `Context Scaler` with query context & token limit -> returns `memory_context_string` by querying `memory_interface`.
    6.  **LLM:** `main` assembles prompt (memory context + query + emotion), calls `llm_interface.generate(agent='sage'|'seer', ...)` -> returns `ai_response_text`.
    7.  **Logging:** `main` calls `memory_interface.append_chronicle` with AI turn details.
    8.  **TTS:** `main` calls `tts_interface.synthesize(ai_response_text, agent_config)` -> returns `audio_data`, `sample_rate`.
    9.  **Output:** `main` calls `audio_processing.play_audio(audio_data, sample_rate)`.
*   **B. Remote User Interaction Cycle:**
    1.  **Client:** Performs STT -> sends text via POST to FastAPI `/chat`.
    2.  **FastAPI (`/chat`):** Receives text -> Performs Text Sentiment analysis -> Calls Context Scaler -> Assembles prompt -> Calls `llm_interface` -> Receives AI text -> Returns AI text (JSON).
    3.  **Client:** Receives text -> Performs device-side TTS.
    *(Alternative: Client sends audio to `/transcribe` -> API returns text. Client sends text to `/chat` -> API returns AI text. Client sends AI text to `/synthesize` -> API returns audio data.)*
*   **C. Collaborative Daily Reflection Workflow:**
    1.  **Trigger:** `main` scheduler/command.
    2.  **Loop:** `main` orchestrates multiple turns:
        *   Call `llm_interface` (Sage) for structured extraction from Chronicle (via `memory_interface`).
        *   Present results to user (via TTS/GUI).
        *   Receive user verification/edits (via STT).
        *   Update Synthesis Store (`entities`, `facts_decisions`) via `memory_interface`.
        *   Call `llm_interface` (Seer/Sage) for narrative summaries using verified items.
        *   Present summaries to user.
        *   Receive user verification/edits.
        *   Call `llm_interface` for fidelity score.
        *   Update Synthesis Store (`daily_summaries`) via `memory_interface`.
*   **D. Shaman Task Delegation & Retrieval Workflow:**
    1.  **Delegation:** `main` (from user command or agent decision) adds task to `tasks.db` via `memory_interface`.
    2.  **Execution:** Separate Shaman process/thread queries `tasks.db` for 'pending'. Updates status to 'running'. Performs task using `llm_interface`, `memory_interface`, `search_module`. Updates status to 'complete'/'failed'. Stores results reference/error.
    3.  **Retrieval:** `main`/GUI queries `tasks.db` for status. Retrieves results from Synthesis Store using reference ID.

**VIII. Privacy & Security Strategy**

Ensuring user privacy and data security is a non-negotiable cornerstone of OracleAI's design.

*   **A. Local-First Mandate:** All core processing (LLM, STT, TTS, SER, Memory operations) and data storage (Akashic Record) MUST occur on user-controlled hardware. No conversational data, personal information, or memory content is sent to external servers unless explicitly configured and initiated by the user for specific opt-in services (e.g., cloud backup - not currently planned, external API calls).
*   **B. Data Encryption at Rest:**
    *   **OS Level (Baseline Recommendation):** Users should enable Full Disk Encryption provided by their OS (BitLocker for Windows Pro/Enterprise, FileVault for macOS, LUKS for Linux) to protect all data if the physical device is compromised.
    *   **Application Level (Mandatory for Databases):** All SQLite databases (`synthesis.db`, `calendar.db`, `profile.db`, `tasks.db`) MUST be encrypted using **SQLCipher** (via `pysqlcipher3` or equivalent bindings). OracleAI will require a user-set master password at startup (or retrieve it from a secure OS store) to decrypt and access these databases.
    *   **Application Level (Optional for Logs):** Raw Chronicle `.jsonl` files can optionally be encrypted using symmetric AES-256 (via `cryptography` library) with the same master password. This adds overhead to appending/reading logs but provides an extra layer if OS encryption is bypassed while the system is running. *Default: Rely on OS FDE + SQLCipher + Encrypted Backups.*
    *   **Backup Encryption:** The integrated 7-Zip backup feature MUST support user-provided password-protected AES-256 encryption (`-p{password} -mhe=on`) for exported Akashic Record archives.
*   **C. Secure Configuration & Credentials:**
    *   Sensitive information in `.env` (API keys, master password hash/salt if stored) must be protected by strict filesystem permissions. `.env` should NOT be committed to version control if containing secrets.
    *   **API Keys/OAuth Tokens:** Store securely. Options:
        1.  Directly in `.env` (requires user to secure the file).
        2.  Use OS credential stores (Windows Credential Manager, macOS Keychain, Linux Keyring) via libraries like `keyring`. (More secure, adds complexity).
        3.  Encrypt tokens within `profile.db` using the master key.
*   **D. Network Security:**
    *   **FastAPI Binding:** Default binding MUST be `127.0.0.1` (localhost) to prevent accidental network exposure. Binding to `0.0.0.0` requires explicit user configuration change.
    *   **External Access:** Strongly recommend using secure tunneling solutions like **Tailscale** or a self-hosted VPN instead of direct port forwarding for remote access.
    *   **HTTPS:** All external API calls (Search, Calendar, Reddit) MUST use HTTPS.
*   **E. External API Calls & Data Minimization:**
    *   Features requiring external APIs (Search, Calendar) are opt-in.
    *   Clearly document what data is sent (e.g., search queries, calendar sync requests).
    *   Implement optional TOR/VPN proxy for search/scraping requests to enhance anonymity.
*   **F. No Telemetry:** OracleAI will NOT collect or transmit any usage statistics, crash reports, performance data, or any other form of telemetry without explicit, granular, opt-in consent from the user for specific, clearly defined purposes. Any opt-in telemetry must be fully anonymized.
*   **G. User Education & Responsibility:** Documentation must clearly outline the security measures, the data being stored, the importance of a strong OS password, the implications of losing the OracleAI master password (if application-level file encryption is used), and secure practices for remote access.

**IX. Hardware & Performance Considerations**

OracleAI is designed for high-end consumer or prosumer hardware, but includes mechanisms for adaptability.

*   **A. CPU:** Modern multi-core CPU (e.g., Ryzen 5000 / Intel 12th Gen or newer recommended). Required for Piper TTS, `librosa` feature extraction, text sentiment analysis, database operations, and general application logic.
*   **B. RAM:** Minimum 16GB (only feasible with very small LLMs for Sage/Seer and no Shaman). **32GB strongly recommended** for running medium-sized LLMs and basic memory functions. **64GB+ recommended** for comfortable use with larger LLMs (30B+), extensive memory logging, and enabling the Shaman agent. RAM speed impacts performance, especially if LLMs offload significantly to system RAM.
*   **C. GPU & VRAM:** **NVIDIA GPU with sufficient VRAM is the primary requirement and bottleneck.**
    *   **Required For:** STT (`openai-whisper`), SER model inference, optional XTTSv2 TTS, and crucially, LLM inference acceleration via KoboldCpp (`-ngl` layers).
    *   **VRAM Breakdown:**
        *   *OracleAI Python Process:* ~4-8 GB VRAM (for Whisper `large-v2` + SER Model + optional XTTSv2). This is relatively constant.
        *   *KoboldCpp Instances:* VRAM usage scales directly with the size of the GGUF model loaded and the number of layers offloaded (`-ngl`).
            *   Small LLMs (7B-13B): ~5-10 GB VRAM per instance.
            *   Medium LLMs (30-34B): ~18-25 GB VRAM per instance.
            *   Large LLMs (70B+): ~40GB+ VRAM per instance.
    *   **Total System VRAM Needed:** `VRAM (Python Process) + VRAM (Sage KoboldCpp) + VRAM (Seer KoboldCpp) + VRAM (Shaman KoboldCpp, if active)`.
        *   *Minimum Practical (Small LLMs, No Shaman):* ~16GB (e.g., 6GB Python + 2x 5GB KoboldCpp). Performance might be limited.
        *   *Recommended Mid-Range (Medium LLMs, No Shaman):* ~32-48GB (e.g., 8GB Python + 2x 18GB KoboldCpp).
        *   *Recommended High-End (Large LLMs + Shaman):* 48GB+ (e.g., 8GB Python + 2x 18GB KoboldCpp + 40GB Shaman KoboldCpp = ~82GB total needed concurrently, OR use Shaman Focus Mode on a 48GB+ card). Professional cards (A6000, RTX 6000 Ada) or multiple consumer cards (e.g., 2x 3090/4090) are ideal.
*   **D. Storage:**
    *   **Fast SSD (NVMe Recommended):** Essential for OS, application, Python environment, and especially for SQLite databases and potentially KoboldCpp model offloading (`mmap`). Slow storage will severely bottleneck memory access and Shaman performance.
    *   **Capacity:** Depends on memory retention duration. Chronicle logs (`.jsonl`) can grow large over time. Summaries and databases are more compact. Plan for 100s of GBs to multiple TBs for long-term use.
*   **E. Multi-PC Architecture:** For optimal performance with large models or running all three agents concurrently at high load, distribute KoboldCpp instances across multiple networked PCs, each with a dedicated GPU and sufficient RAM. The main OracleAI application runs on one machine and communicates with KoboldCpp instances via network API calls.
*   **F. Resource Management Toggle ("Shaman Focus"):** Critical feature for single-GPU systems with high VRAM but not enough to run everything simultaneously. Allows users to stop Sage/Seer KoboldCpp processes (via `subprocess` or OS signals managed by OracleAI) to free VRAM for Shaman's intensive tasks. GUI provides feedback on status and potentially VRAM usage.
*   **G. Latency Expectations:** Real-time interaction with Sage/Seer aims for sub-5-second latency on high-end hardware (STT+SER+LLM+TTS). Shaman latency is variable (minutes to days) based on task complexity and hardware, managed via the "Hyperspace Travel" UI metaphor.

**X. Installation & Configuration Overview**

*   **A. Prerequisites:** Python 3.11, Git, NVIDIA GPU, compatible NVIDIA Drivers, matching CUDA Toolkit version, PortAudio library, 7-Zip executable accessible via PATH or config.
*   **B. External Tools Setup:** User must manually download/install:
    *   KoboldCpp executable.
    *   Desired GGUF LLM/VLM models for KoboldCpp.
    *   Piper TTS executable.
    *   Desired Piper TTS `.onnx` voice models and `.onnx.json` configs.
    *   (Potentially) Pre-trained SER model files if not bundled or downloaded automatically by `transformers`.
*   **C. Python Environment Setup:**
    1.  Clone repository.
    2.  Create/activate Python virtual environment (`venv`).
    3.  Install correct PyTorch version matching installed CUDA (using official command generator).
    4.  Install all other Python dependencies using the provided lock file (`requirements.lock`) or `pyproject.toml` via `pip`.
*   **D. Configuration (`.env`):** Crucial step. User creates `.env` file and populates it with:
    *   Full paths to external executables (Piper, 7z).
    *   Full paths to models (Whisper model name, Piper voices, SER model).
    *   KoboldCpp API URLs for each agent.
    *   Akashic Record base directory path.
    *   Agent configurations (TTS engine choice, voice paths, default temperatures).
    *   API keys (Reddit, Search Engines - optional).
    *   Calendar API credential path/info.
    *   FastAPI server host/port.
    *   TOR proxy settings (optional).
    *   Logging level.
*   **E. API Keys & Authentication:**
    *   Run initial OAuth flow for Calendar integration (guided by a script/command).
    *   Obtain and configure Reddit API keys if using Deep Search.

**XI. User Interface Concept**

*   **A. Vision:** Dedicated desktop GUI application providing an immersive "Oracle/Mystic Temple" aesthetic, blending high-tech geometric/circuit elements with classical/esoteric themes.
*   **B. Technology:** PyQt/PySide (recommended for customization), Kivy, or Web Tech (React/Vue/Svelte) + Electron/Tauri.
*   **C. Key Components:**
    *   **Main Interaction View:** Displays chat log, clearly differentiating user, Sage, Seer, Shaman turns with distinct visual styles/colors (Ice/Fire/Cosmic themes).
    *   **Status Dashboards:** Side panels showing:
        *   Current User Emotion/Sentiment readout (icons/gauges).
        *   Akashic Record access indicators.
        *   System Performance Metrics (optional).
        *   Task Queue summary.
        *   Upcoming Calendar Events snippet.
    *   **Shaman Status Panel:** Dedicated area featuring the "Hyperspace Travel" indicator (e.g., Merkaba moving Moon-Mars-Jupiter...), current task description, estimated time/progress, current "depth"/latency level.
    *   **Agent Control Panel:** Buttons/indicators to see active agents, potentially toggle Mute/Search states, activate Oracle Consultation or Shaman Focus modes.
    *   **Settings Module:** User-friendly interface for editing `.env` configurations (masking secrets), selecting TTS voices, adjusting agent parameters.
    *   **Memory Browser (Future):** Interface to search, view, and potentially edit Akashic Record components (Chronicle, Summaries, Entities).
    *   **Backup/Restore Controls:** Buttons to trigger encrypted/unencrypted 7-Zip backups.
*   **D. Iconography:** Consistent set using geometric line style for Brain (Cognition), Heart (Emotion), Eye (Vision/Search), Network (Connectivity), Wave (Audio), Delta (Agents/Action), Chart (Analysis), Gear (Settings).
*   **E. Fonts:** Combination of readable tech sans-serif (Titillium Web/Exo 2) for UI text and stylized display fonts (Cinzel/Audiowide) for titles/accents.

**XII. Future Considerations & Extensibility**

*   **Knowledge Graph:** Migrate from SQLite simulation to a dedicated Graph Database (Neo4j) for advanced relationship querying.
*   **Vector Store:** Fully integrate ChromaDB/FAISS for robust semantic search across the Akashic Record.
*   **Advanced Pattern Analysis:** Develop more sophisticated algorithms for Shaman to detect complex user behavior patterns, cognitive biases, or learning trajectories.
*   **Proactive Assistance:** Implement more nuanced proactive suggestions and nudges based on memory analysis and calendar context (with user controls).
*   **Skill Transfer:** Explicitly design prompts/interactions where agents explain their reasoning processes to teach the user.
*   **PKM Integration:** Develop APIs or plugins to sync/interact with tools like Obsidian, Logseq, Notion.
*   **Refined GUI:** Implement the full Memory Browser/Editor, advanced visualizations for trends.
*   **Dockerization:** Create Docker images for easier deployment and dependency management, potentially separating components into different containers (e.g., FastAPI server, Shaman processor).
*   **Multi-User Collaboration:** Extend the framework to support multiple users interacting with the same OracleAI instance or a shared knowledge base (requires significant changes to memory access control and agent interaction).

**XIII. Appendices (To Be Developed)**

*   Detailed JSON Schema Definitions for Chronicle entries and Synthesis Store JSON fields.
*   Detailed SQLite Schemas (SQL DDL) for all databases (`synthesis.db`, `calendar.db`, `profile.db`, `tasks.db`).
*   FastAPI Endpoint Specifications (Paths, Methods, Request/Response Pydantic Models).
*   Example `.env` File Structure.
*   Core Prompt Templates for Agents (System Prompts, Summarization Prompts, Analysis Prompts).
*   Detailed Workflow Diagrams.

**Appendix A: Shaman's Hyperspace Journey**

Okay, let's draft a conceptual mapping of Shaman's "hyperspace travel" distance (latency) to planetary bodies, representing increasing computational depth and time. This is highly speculative and serves primarily as a thematic UI element to manage user expectations.

**Assumptions:**

*   **Hardware Baseline:** A very high-end single system (e.g., 128GB+ RAM, fast multi-TB NVMe SSDs, top-tier CPU, one or more high-VRAM GPUs like RTX 4090/3090 or professional cards).
*   **Technology:** KoboldCpp using Llama.cpp backend with advanced offloading (RAM/SSD via `mmap` and potentially future optimizations).
*   **Task Complexity:** The latency depends hugely on the *task* assigned to Shaman (simple query vs. complex analysis vs. massive data synthesis) and the *size* of the model being used for that task.
*   **Model Sizes (Conceptual):**
    *   Moon: Smaller tasks on large models (70B+) primarily in VRAM/RAM.
    *   Mars: Larger tasks on large models, significant RAM usage.
    *   Jupiter/Saturn: Very large models (180B+) heavily reliant on RAM offloading.
    *   Uranus/Neptune: Extremely large models (>500B?) heavily reliant on fast SSD offloading via `mmap`.
    *   Pluto: Pushing the limits of SSD offloading, potentially involving complex multi-stage processing.
    *   Kuiper Belt: Tasks requiring processing vast amounts of data that might even exceed fast SSD capacity or involve extremely slow algorithms (simulating HDD-like speeds for specific operations).

**Shaman's Hyperspace Journey - Latency Estimates:**

*(These are rough order-of-magnitude estimates for complex tasks appropriate for Shaman, not simple queries. The Merkaba visual could pulse or spin faster/slower based on estimated progress.)*

| Destination    | Symbolic Representation                                  | Estimated Latency Range | Typical Task Examples                                                                                                                               | Primary Resource Bottleneck |
| :------------- | :------------------------------------------------------- | :---------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------- |
| **Earth Orbit**| (Starting Point / Idle)                                  | < 1 minute              | Idle, waiting for tasks, simple status checks.                                                                                                      | N/A                   |
| **Moon**       | Quick trip, familiar territory                           | **1 - 10 Minutes**      | Deep analysis of a single day's Chronicle + Summaries, complex query involving recent memory, moderate deep search synthesis, basic pattern check. | GPU VRAM + System RAM       |
| **Mars**       | Significant journey, requires planning                   | **10 - 60 Minutes**     | Analyzing a full week/month of summaries + Chronicle data, complex KG relationship extraction, moderate pattern analysis across multiple data types. | System RAM + CPU            |
| **Jupiter**    | Major expedition, vast scale                             | **1 - 4 Hours**         | Deep comparative analysis across several months of data, training/fine-tuning a small auxiliary model (e.g., sentiment), complex "what-if" scenarios. | System RAM + Fast NVMe SSD  |
| **Saturn**     | Long haul, intricate navigation required                 | **4 - 12 Hours**        | Very large-scale pattern analysis across entire memory bank, generating complex strategic reports involving multiple variables and long timelines.     | System RAM + Fast NVMe SSD  |
| **Uranus**     | Outer reaches, exploring the unknown                     | **12 - 48 Hours**       | Extremely complex synthesis involving massive external data + full memory bank, potentially initial stages of large model fine-tuning (if ever implemented). | Fast NVMe SSD + CPU         |
| **Neptune**    | Deep space, limits of current exploration                | **2 - 5 Days**          | Tasks requiring iterative processing over the entire Akashic Record multiple times, potentially simulating complex systems based on memory data.       | Fast NVMe SSD + CPU         |
| **Pluto**      | Edge of the system, profound but slow discovery          | **5 - 14 Days**         | Highly speculative tasks involving near-complete reprocessing or re-indexing of the entire memory bank with new algorithms or models.             | Fast NVMe SSD               |
| **Kuiper Belt**| Beyond known limits, potentially indefinite processing   | **Weeks - Months+**     | Hypothetical tasks like attempting unsupervised discovery of entirely new concepts across terabytes of data, or processes bottlenecked by extremely slow storage/algorithms. | Slow Storage (Simulated HDD) / Algorithm Complexity |

**Visual Representation (Merkaba Slider/Indicator):**

*   A slider or a visual indicator showing a golden Merkaba moving along a path representing these celestial bodies.
*   When a task is assigned, estimate its complexity (based on input data size, task type, model used) and map it to a target destination.
*   The Merkaba starts moving towards the destination. Its speed could be relative to the total estimated time.
*   Tooltips or status text could show "Traveling to Mars (Est. 35 mins remaining)" or "Processing Deep Patterns (Jupiter - Est. 2.5 hours)".
*   When idle, the Merkaba rests near Earth.

**Important Considerations:**

*   **Estimation is Hard:** Accurately predicting the runtime for complex LLM tasks, especially those involving RAM/SSD offloading, is extremely difficult. These are thematic guides, not precise ETAs. The system might provide a very rough estimate initially and refine it as the task progresses (if possible).
*   **Task Granularity:** A "task" could be broken down. Maybe reaching the "Moon" involves analyzing daily logs, but reaching "Mars" involves synthesizing those findings into a weekly report.
*   **User Control:** The user should ideally be able to see queued tasks for Shaman and potentially cancel long-running ones.
*   **Hardware Variation:** These times are highly dependent on the specific hardware configuration. A system with slower SSDs or less RAM would experience much longer times for the outer "planets."

This planetary scale provides a compelling narrative framework for understanding and accepting the varying latencies associated with the different levels of deep analysis performed by the Shaman agent. It turns a technical limitation (processing time) into an immersive part of the OracleAI experience.

---
This concludes the complete, detailed design blueprint for OracleAI. It incorporates all the current features, architectural decisions, and nuances.
