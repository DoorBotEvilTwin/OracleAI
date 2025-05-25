# OracleAI Comprehensive Feature List Outline (for v0.4 Documentation)

**Version 0.1: Foundational Core & Basic Interaction (Conceptual "Alpha")**
*(Represents the initial stable baseline after diverging from Vector Companion, focusing on a single agent (Sage) with core local I/O and basic memory logging.)*

*   **F0100: Core Infrastructure & Setup:**
    *   [F0101] Python 3.11 Virtual Environment setup and dependency management (`requirements.lock`).
    *   [F0102] `.env` file for primary configuration, loaded by `config_loader.py`.
    *   [F0103] Centralized logging system (to console and timestamped file `oracle_ai_runtime.log` within `AKASHIC_RECORD_PATH/Logs/`), configured by `config_loader.py`.
    *   [F0104] Standardized project directory structure (`scripts/` for Python, dot-prefixed folders for tools/models, `akashic_record/` for data).
    *   [F0105] Dynamic path resolution in `config_loader.py` based on `PROJECT_ROOT`.
    *   [F0106] Basic error handling and graceful exit mechanisms in `main.py`.
*   **F0110: LLM Integration (Single Agent - Sage):**
    *   [F0111] `llm_interface.py`: Interface to **KoboldCpp** for GGUF model serving via HTTP API.
    *   [F0112] `payload_manager.py`: Manages KoboldCpp API payload construction.
        *   [F0112a] `BASE_DEFAULT_GENERATION_SETTINGS` defined in script.
        *   [F0112b] Auto-generates and loads `config_files/payload_settings.ini` for default and Sage-specific LLM parameters (e.g., `max_length`, `rep_pen`).
        *   [F0112c] Sage's LLM temperature override from `.env` via `config_loader.py`.
    *   [F0113] Initial System Prompt for Sage (analytical persona, low temperature) defined in `main.py`.
*   **F0120: Speech-to-Text (STT):**
    *   [F0121] `stt_interface.py`: Integration of `openai-whisper` Python library.
    *   [F0122] GPU acceleration for Whisper (PyTorch/CUDA).
    *   [F0123] Local Whisper model caching (e.g., in `PROJECT_ROOT/.whisper_models/`).
    *   [F0124] Configurable Whisper model name (e.g., `medium`) via `.env`.
*   **F0130: Text-to-Speech (TTS):**
    *   [F0131] `tts_interface.py`: Integration of Piper TTS via `subprocess`.
    *   [F0132] Configurable Piper executable path and voice model/config paths for Sage via `.env`.
    *   [F0133] `clean_text_for_tts()`: Removes Markdown for cleaner Piper output.
*   **F0140: Audio Processing (`audio_processing.py`):**
    *   [F0141] Microphone input using `pyaudio`.
    *   [F0142] Voice Activity Detection (VAD) with RMS threshold and silence limit to segment utterances.
        *   [F0142a] VAD Pre-buffering to capture leading soft sounds.
    *   [F0143] Saving user utterance to temporary `.wav` file.
    *   [F0144] Audio playback of TTS output using `pyaudio` (later `sounddevice`).
    *   [F0145] Threaded TTS playback (`play_tts_in_thread_wrapper` in `main.py`) to prevent blocking main loop.
    *   [F0146] Optional audio normalization for user input.
    *   [F0147] Global `threading.Event` objects for playback control (`playback_interrupt_event`, `playback_is_paused_event`, `tts_playback_started_event`).
*   **F0150: Memory System (Akashic Record - Initial Chronicle Logging):**
    *   [F0151] `memory_interface.py`: Basic functions for Chronicle interaction.
    *   [F0152] Daily Chronicle files (`[AKASHIC_RECORD_PATH]/Chronicle/YYYY-MM-DD_chronicle.jsonl`) storing:
        *   Timestamp, turn_id (UUID), session_id (UUID), speaker (user/sage).
        *   User's raw STT and final processed text.
        *   Sage's final response text.
        *   Basic LLM/TTS metadata placeholders.
*   **F0160: Main Interaction Loop (`main.py`):**
    *   [F0161] Orchestration of STT -> LLM (Sage) -> TTS -> Playback cycle.
    *   [F0162] Basic in-memory list for `conversation_history` (short-term context for LLM).
    *   [F0163] Keyboard listener thread (`keyboard` library).
    *   [F0164] **ESC key:** Interrupts current TTS playback.
    *   [F0165] Handling of user exit commands (e.g., "quit", "exit").
    *   [F0166] Basic `if __name__ == '__main__':` block for application startup.
*   **F0170: User Interface (Console - Basic):**
    *   [F0171] Text-based console interaction.
    *   [F0172] Clear prompts for user input (e.g., "User (Listening...):").
    *   [F0173] Display of AI agent responses.

---

**Version 0.2: Enhanced Interaction, Multi-Agent Council, Deeper Memory & Modalities (Conceptual "Stable Beta" / Our Current v0.2q)**
*(Represents the significant feature additions, refinements, and bug fixes leading to a robust multi-agent system with foundational advanced features.)*

*   **F0200: Multi-Agent Council & Personas:**
    *   [F0201] Introduction of **Seer** agent (creative catalyst, high temperature) alongside Sage.
    *   [F0202] Conceptual definition of **Shaman** agent (deep brain consultant).
    *   [F0203] Introduction of **System Voice** (distinct Piper TTS voice for system messages, e.g., "HAL-like").
    *   [F0204] Agent-specific configurations in `.env` and `payload_settings.ini` for LLM URLs, temperatures, TTS engines/voices.
    *   [F0205] `agent_prompts.py`: Centralized management of detailed system prompts (User Revision 4 "Lucid" for Seer).
        *   [F0205a] Standardized `SYSTEM INFORMATION (DO NOT REPEAT...):` block.
        *   [F0205b] Instructions on handling NLU/Emotion context strings.
        *   [F0205c] Explicit "Do not impersonate User, {USER_NAME}, other agents" instructions.
        *   [F0205d] Standardized Python format placeholders (`{ACTUAL_USER_NAME_KEY}`, `{SAGE_ACTUAL_LABEL}`, etc.).
    *   [F0206] `load_and_format_system_prompts()` in `main.py` uses `config_loader.USER_NAME` and agent labels for prompt formatting.
    *   [F0207] `USER_NAME` variable in `.env` (via `config_loader.py`) for AI to address user by name.
*   **F0210: Enhanced Interaction & Control (`main.py`):**
    *   [F0211] Startup mode selector (Console input: Sage Only, Seer Only, Sage & Seer Council).
    *   [F0212] **Council Mode (Sage & Seer):**
        *   [F0212a] Sequential turn-taking: User -> Sage -> Seer -> Confirmation.
        *   [F0212b] Robust TTS thread management to ensure smooth, automatic transition between agent TTS playback without hangs (primary reliance on `ai_is_speaking` flag).
    *   [F0213] **"Pass Turn" Command:** Basic inter-agent discussion in council mode (Agent A responds to Agent B based on last turn).
    *   [F0214] **F9-F12 User Confirmation Loop:**
        *   [F0214a] F9: Save exchange to Chronicle and `conversation_history`.
        *   [F0214b] F10: Undo/Discard exchange (no Chronicle log, no history update, clears `last_user_input_for_retry`).
        *   [F0214c] Shift+F11: Repeat TTS.
            *   [F0214c1] **Multi-Segment Replay:** In council mode, replays all agent audio segments from that turn sequentially.
            *   [F0214c2] **ESC during Multi-Replay:** Skips only the *current segment* being replayed, then continues to the next segment in the sequence.
        *   [F0214d] F12: Retry last user query (uses `last_user_input_for_retry`).
        *   [F0214e] Configurable timeout (`CONFIRMATION_TIMEOUT_SEC` in `.env`, default 1800s), defaults to "Undo" on timeout.
    *   [F0215] **F6 Pause/Resume TTS:** Pauses/resumes the *current* TTS utterance.
    *   [F0216] **F7 Simple Mute/Unmute AI Output:** Toggles all AI audio output (stops current, prevents new).
    *   [F0217] `play_system_message()` function for system audio output, integrated with TTS thread management.
*   **F0220: Emotional Intelligence Suite (Text-Based - `emotion_analyzer.py`):**
    *   [F0221] Integration of VADER, TextBlob, NRCLex for text sentiment/emotion analysis.
    *   [F0222] `get_emotional_context_summary_for_llm()` creates `[User Emotional Context: ...]` string.
    *   [F0223] Emotional context string prepended to LLM prompts.
    *   [F0224] Detailed emotion/sentiment scores logged to Chronicle (e.g., `user_text_sentiment_vader`, `user_text_emotion_nrclex`).
    *   [F0225] Robust NLTK data path management (`.nltk_data` in project root) and local download attempts for dependencies (`punkt`, `wordnet`, `omw-1.4`, `averaged_perceptron_tagger`, `brown`).
*   **F0230: Text Utilities (`text_utils.py` - TAS Inspired):**
    *   [F0231] **Keyword Extraction (YAKE!):** For user input and agent responses, logged to Chronicle (`keywords_yake_user`, `keywords_yake_agent`).
    *   [F0232] **Basic Text Stats (Total Words, Chars, Avg. Sentence Length):** For user/agent text, logged to Chronicle.
    *   [F0233] **Context Size Estimator (CSE):**
        *   [F0233a] `estimate_token_count()` function using `CHARS_PER_TOKEN_ESTIMATE` from `.env` (via `config_loader.py`).
        *   [F0233b] Estimated prompt token count logged to Chronicle (replacing old word count, new key `agent_llm_prompt_estimated_tokens`).
        *   [F0233c] DEBUG log of estimated prompt size in `main.py`.
    *   [F0234] **TF-IDF Keyword Extraction (Corpus-based):** `extract_tfidf_keywords()` function available for future batch use by Shaman.
    *   [F0235] NLTK data path management for `text_utils.py` (stopwords, punkt).
    *   [F0236] `initialize_text_utils()` called at `main.py` startup.
*   **F0240: Vision Modality (Basic VLM Integration):**
    *   [F0241] `vision_processing.py`: `capture_screenshot()` using `mss` library.
    *   [F0242] `KOBOLDCPP_API_URL_VLM` in `.env` and `config_loader.py`.
    *   [F0243] `llm_interface.py`: `encode_image_to_base64()` and `get_vlm_description(image_path, prompt_text)` using Llama.cpp `/completion` style payload (prompt with `[img-1]`, `image_data` field).
    *   [F0244] Basic "analyze screen" keyword command handling in `main.py` (`VLM_COMMAND_KEYWORDS`).
    *   [F0245] VLM description spoken by System Voice and logged to Chronicle (speaker `system_vlm`).
    *   [F0246] VLM command keywords printed to console during user listening prompt (but not to log file).
*   **F0250: STT Enhancements (`main.py`):**
    *   [F0251] Expanded `STT_JUNK_TRANSCRIPTIONS` list (e.g., "thanks for watching", "cough", "coughs").
*   **F0260: Output Filtering & Prompt Refinements (`main.py`, `agent_prompts.py`, `payload_manager.py`):**
    *   [F0261] Regex-based filtering in `process_agent_turn` to strip echoed `[User NLU Analysis: ...]` and `[User Emotional Context: ...]` strings from LLM output.
    *   [F0262] Filtering in `process_agent_turn` to remove hallucinated `User:` or `{USER_NAME}:` turns at the end of agent responses.
    *   [F0263] `payload_manager.py`: Enhanced stop sequence logic to include other active agent labels and user labels to prevent impersonation.
    *   [F0264] `agent_prompts.py`: System prompts include explicit "Do not impersonate" and "Do not repeat system information" directives.
*   **F0270: Logging & Debugging Enhancements:**
    *   [F0271] More detailed DEBUG and INFO level logging across modules for state tracking and error diagnosis.
    *   [F0272] Thread names included in TTS and audio processing logs.
    *   [F0273] `config_loader.py` creates necessary subdirectories (Logs, Chronicle, Databases, AudioLogs/temp, .piper/voices, .whisper_models, etc.) if they don't exist.
*   **F0280: Documentation (Initial Drafts):**
    *   [F0281] READMEs (Brief, Short, Long, Summarized for v0.1, v0.2, v0.3).
    *   [F0282] Design Documents (v0.1, v0.2, v0.3).
    *   [F0283] `rules_memory.md` and `rules_tts.md` for LLM guidance during development.
    *   [F0284] `VC_INSTRUCTION_MANUAL.md` and `VC_README.md` archived.

---

**OracleAI Comprehensive Feature List Outline (Continued)**

**Version 0.3: Advanced Capabilities & System Maturity (Conceptual "Full Beta")**
*(This version aims to implement the full suite of planned analytical tools, memory processes, and core functionalities, making OracleAI a deeply capable cognitive partner.)*

*   **F0300: Natural Language Understanding (NLU) Suite (`nlu_processor.py`):**
    *   [F0301] **spaCy Integration:** Load configurable spaCy model (e.g., `en_core_web_lg` via `SPACY_MODEL_NAME` in `.env`).
    *   [F0302] **Core Linguistic Processing:** Tokenization, Lemmatization, Part-of-Speech (POS) tagging, Dependency Parsing.
    *   [F0303] **Named Entity Recognition (NER):**
        *   [F0303a] Utilize spaCy's pre-trained NER (PERSON, ORG, LOC, DATE, etc.).
        *   [F0303b] Custom EntityRuler/PhraseMatcher for OracleAI-specific entities (AI_AGENT_NAME, MEMORY_COMPONENT_TYPE, ORACLEAI_COMMAND_KEYWORD, SHAMAN_DEPTH_LEVEL) and dynamically loaded user-defined entities (PROJECT_NAME, USER_CONTACT_NAME, KEY_CONCEPT from Citadel's `Entities` table).
    *   [F0304] **Intent Recognition:**
        *   [F0304a] Rule-based pre-screening for fixed system commands (e.g., `/textmode`, "oracleai mute").
        *   [F0304b] Custom spaCy `TextCategorizer` trained on OracleAI-specific intents (e.g., `ask_general_question`, `delegate_task_shaman_research`, `set_user_goal`, `query_calendar_schedule`, `provide_memory_fact`, `guided_generation_command`, `system_command_oracleai_mode_switch`).
        *   [F0304c] Mechanism for ongoing local training/fine-tuning of intent model with user-flagged examples (future GUI).
    *   [F0305] **Slot Filling:** Rule-based (using NER, POS, dependencies) extraction of parameters for recognized intents.
    *   [F0306] **Query Preprocessing for Search:** Generate lemmatized, stop-word-removed text and key search terms.
    *   [F0307] **NLU Output Integration:**
        *   [F0307a] Full NLU analysis JSON (intent, entities, slots, confidence, etc.) logged to Chronicle's `nlu_analysis` field.
        *   [F0307b] Concise NLU summary string (e.g., `[User NLU Analysis: Intent=X. Entities=Y,Z.]`) passed to LLM prompt via Context Scaler.
        *   [F0307c] Agent system prompts in `agent_prompts.py` updated to include instructions on utilizing NLU data.
    *   [F0308] **Command Routing in `main.py`:**
        *   [F0308a] Direct execution of simple system commands based on NLU intent without LLM call.
        *   [F0308b] Routing to specific agents based on NLU intent or explicit addressing (e.g., "Sage, analyze X").
    *   [F0309] **Standardized User Command List Parsing:** NLU handles commands like "OracleAI, [system_cmd]", "[AgentName], [query]", "Council, [query]".
*   **F0310: Akashic Record - Advanced Memory Foundation & Processes:**
    *   [F0311] **Chronicle Cache:**
        *   Interaction turns (user and agent pending log entries) written to a temporary cache directory (`[AKASHIC_RECORD_PATH]/ChronicleCache/session_id/turn_id.json`).
        *   F9 saves to this cache, F10 discards from this cache (for the current unconfirmed exchange).
    *   [F0312] **Memory Consolidation (MemCon) Session:**
        *   User-initiated session (e.g., daily, or on demand).
        *   Interface (initially CLI, future GUI) for user to review cached Chronicle entries from `ChronicleCache`.
        *   User can Approve, Edit (text content), or Discard cached turns.
        *   Approved (and edited) entries are committed to the permanent daily Chronicle `.jsonl` file.
    *   [F0313] **Full Collaborative Daily Reflection (Post-MemCon):**
        *   Workflow using Sage (structured data extraction) and Seer (narrative/emotion summarization) based on *committed* Chronicle entries for the day.
        *   Populates all core tables in **The Citadel (`synthesis.db`)**: `Entities`, `Relationships`, `FactsDecisions`, `Summaries` (Daily type). User verification steps integrated.
    *   [F0314] **Hierarchical Summaries (Weekly, Monthly):** Automated background task (Sage/Shaman via `apscheduler`) to create these in The Citadel from verified daily summaries.
    *   [F0315] **Project/Topic Threads:** Automated updates to `ProjectTopicThreads` in The Citadel based on new relevant data from daily reflections.
    *   [F0316] **Memory Bank Context Scaler (RAG Engine) - Citadel Integration:**
        *   Context Scaler now primarily retrieves from The Citadel (Entities, Facts, Summaries, Profile, Calendar).
        *   Implements keyword search (SQLite FTS) on Citadel content.
        *   (Semantic search via Vector Store is a v0.4 feature).
    *   [F0317] **SQLCipher Encryption:** All SQLite databases (`synthesis.db`, `calendar.db`, `profile.db`, `tasks.db`) are encrypted. Master password prompt at startup.
*   **F0320: Shaman Integration (Asynchronous Tasking & Foundational Analysis):**
    *   [F0321] Full implementation of `tasks.db` via `memory_interface.py` for queuing and managing Shaman's tasks.
    *   [F0322] Shaman's main processing loop (background thread/process via `apscheduler`) polls `tasks.db` for assigned tasks.
    *   [F0323] **Initial `PatternAnalysisReports`:** Shaman can generate reports for a few key analytical tasks (e.g., basic sentiment trends over a week from Chronicle emotion data, topic keyword frequency from daily summaries using `topic_modeler.py`).
    *   [F0324] **"Hyperspace Journey" Feedback (Console):** Basic console messages indicating Shaman task start, estimated "depth" (Moon/Mars from planetary scale), and completion.
    *   [F0325] **Oracle Consultation Mode:** Shaman participates responsively based on user-set depth.
*   **F0330: Emotional Intelligence Suite (SER Completion):**
    *   [F0331] **Speech Emotion Recognition (SER):**
        *   Load pre-trained SER model (e.g., Wav2Vec2-based) via PyTorch/Transformers in `emotion_analyzer.py`.
        *   `librosa` for audio feature extraction.
    *   [F0332] SER output (dominant emotion, scores, confidence) logged to Chronicle's `user_voice_emotion_ser` field and included in LLM emotional context string.
    *   [F0333] `ENABLE_REALTIME_SER_FOR_AGENTS` toggle in `.env`.
*   **F0340: Web Connectivity & External Data (Robust Implementation):**
    *   [F0341] **Robust `search_module.py`:** Simple and Deep Search fully functional with DuckDuckGo and PRAW.
    *   [F0342] **Full `calendar_interface.py`:** Support for Google Calendar, Outlook Calendar (via OAuth 2.0), and local `cal.db3`. Robust synchronization to `calendar.db`.
    *   [F0343] **Foreign Dataset Import (Initial):** Shaman can process user-provided `.txt` and `.md` files from `import_data/`, extract summaries/keywords, and store/link in The Citadel.
*   **F0350: Backup & Restore Module (`backup_module.py`):**
    *   [F0351] Implement 7-Zip encrypted (AES-256, password-prompted) and unencrypted backups of the entire `AKASHIC_RECORD_PATH`.
    *   [F0352] Basic restore functionality (user-guided, with warnings about overwriting).
*   **F0360: Remote Access API (`remote_api.py`):**
    *   [F0361] Functional FastAPI server for core chat interaction (`/api/v1/chat/interaction`).
    *   [F0362] Basic API Key authentication (`REMOTE_API_KEY` in `.env`) if network exposed.
*   **F0370: Initial GUI (Basic Functionality - NiceGUI + Tauri):**
    *   [F0371] **Technology Stack:** NiceGUI for UI definition in Python, Tauri for packaging as a cross-platform desktop application.
    *   [F0372] **Core Features:**
        *   Chat interface for text input/output with agents (Sage, Seer).
        *   Display of agent status and current interaction mode.
        *   Basic MemCon Chronicle Cache review/approval interface (list entries, approve/discard buttons).
        *   Button to trigger VLM screen analysis.
        *   (Placeholder for F8 Auto-Advance trigger).
*   **F0380: Documentation (v0.3 Release):**
    *   [F0381] Finalized v0.3 ReadMe (Brief, Short, Long, Summarized versions).
    *   [F0382] Finalized v0.3 Design Document (including all Appendices A-G, I-K, and updated Developer Context Appendix H).

---

**Version 0.4: Polished Experience, Deep Intelligence & Advanced Features (Conceptual "Full Vision")**
*(This version aims for a highly polished, deeply intelligent, and feature-complete OracleAI, incorporating advanced concepts, user experience refinements, and the full realization of the "cognitive partner" vision.)*

*   **F0400: Advanced NLU & Interaction:**
    *   [F0401] **Anaphora Resolution (Coreference Resolution):** Implemented in `nlu_processor.py` (e.g., using spaCy experimental components or dedicated libraries).
    *   [F0402] **Trainable Intent/NER Models (User-Side):** Mechanism for users to (locally, with consent) contribute flagged interaction data to fine-tune NLU components for improved personalization.
    *   [F0403] **Sophisticated Command Parsing & Execution:** Robust handling of complex, multi-part user commands identified by NLU, including chained actions or conditional logic.
    *   [F0404] **Agent-Specific Query Routing (NLU-driven):** `main.py` uses NLU output (intent, target agent entity) to route queries directly to the specified agent even in Council Mode, with summaries passed to other agents if needed. (Deprecates "Sage Only" / "Seer Only" modes in favor of targeted addressing within Council Mode).
*   **F0410: Akashic Record - Peak Functionality & Intelligence (Incorporating Appendix R Insights):**
    *   [F0411] **Full Vector Store ("The Sanctum" - LlamaIndex Powered):**
        *   [F0411a] Integration of a local Vector DB (e.g., ChromaDB, FAISS via `config_loader.VECTOR_STORE_TYPE`).
        *   [F0411b] Automated embedding generation (Sentence Transformers via `EMBEDDING_MODEL_NAME_OR_PATH`) for Library documents, Citadel content, and Chronicle snippets.
        *   [F0411c] Semantic search fully integrated into Context Scaler.
        *   [F0411d] **Rich Metadata for LlamaIndex Nodes:** `source_type`, `source_pk_id`, `tags_json`, `timestamp_content_created`, `embedding_model_used`, etc., for precise filtering.
        *   [F0411e] **Connecting Sanctum Nodes to Citadel Entities:** Bidirectional linking for hybrid RAG (e.g., `Entity.id` in Sanctum node metadata, `Sanctum_node_ids_json` in `Entities` table).
    *   [F0412] **Knowledge Graph ("The Citadel" Refined & Enhanced):**
        *   [F0412a] More advanced relationship extraction capabilities (by Shaman/NLU).
        *   [F0412b] Graph traversal queries integrated into Context Scaler.
        *   [F0412c] **Explicit Node Granularity:** For `FactsDecisions`, `Summaries` to improve retrieval precision (breaking down long texts into more atomic, linkable units).
        *   [F0412d] **Richer Relationship Typing:** Expanded `Relationships.type` vocabulary (inspired by Memory Graph MCP: `follows`, `supports`, `contradicts`, `refines`, `synthesizes`, `caused_by`, `part_of`).
        *   [F0412e] **Temporal Awareness (Enhanced):** More effective use of existing timestamps (`timestamp_occurred` in `FactsDecisions`, `date_key` in `Summaries`). Optional `valid_from_timestamp` and `valid_to_timestamp` fields for `Entities` (Graphiti-inspired).
        *   [F0412f] **Domain-Based Organization (Conceptual):** Optional `domain_id` in key Citadel tables (e.g., `FactsDecisions`, `Summaries`), linking to an `Entity` of type "Domain" (inspired by Memory Graph MCP).
    *   [F0413] **Memory Bank Context Scaler (RAG Engine) - Advanced Techniques:**
        *   [F0413a] Full hybrid search (keyword on Citadel FTS, semantic on Sanctum via LlamaIndex, graph traversal on Citadel KG).
        *   [F0413b] Query transformation (HyDE, step-back).
        *   [F0413c] Reciprocal Rank Fusion (RRF - `RAG_RRF_K_CONST` in `.env`).
        *   [F0413d] **Mitigating Similarity Traps** through diverse retrieval strategies (hybrid search, RRF, graph traversal) and potentially diversity-aware reranking.
        *   [F0413e] **Dynamic Context Window Management (DCWM):** Sage (or utility LLM) evaluates RAG chunk utility post-LLM turn. High-utility chunks persist in a short-term "active context cache" (in-memory or `profile.db`). ENV toggle: `DYNAMIC_CONTEXT_WINDOW_MANAGEMENT_ENABLED`.
    *   [F0414] **Hierarchical Summaries (Lifetime Scaling):** Shaman generates Yearly, and conceptually Decadal summaries, stored in `Summaries` table.
    *   [F0415] **Tagging Strategy (User-Led & AI-Assisted):**
        *   [F0415a] User-led tagging during MemCon/Daily Reflection GUI.
        *   [F0415b] **Shaman Tag Suggestions:** Based on NLU/Topic Modeling, user-verified. ENV toggle: `SHAMAN_SUGGEST_TAGS_ENV`.
        *   [F0415c] **`config_files/tags.ini`:** For controlled system tags (non-editable by user, with warning) and user-defined tag vocabulary (editable section for GUI autocomplete).
    *   [F0416] **RAPTOR-like Hierarchical Indexing:** For very large imported documents/datasets, Shaman builds a tree of summaries at different abstraction levels, stored in The Citadel (`HierarchicalContentSummaries` table). Context Scaler can traverse this tree.
    *   [F0417] **Chrono-Contextual Echo Layer (CCEL - v0.4+):**
        *   Conceptual layer for querying episodic memory.
        *   Implemented via specialized functions in `memory_interface.py` / `shaman_analytics.py` operating on Chronicle and Citadel to reconstruct context around memory creation/use.
        *   Can influence Neural Graffiti memory weighting.
*   **F0420: Agent Evolution & Advanced Modes:**
    *   [F0421] **F8 "Auto-Advance" Council Discussion:**
        *   Full implementation in `main.py`: ENV defined speaking order (`COUNCIL_SPEAKING_ORDER`), active agents (`COUNCIL_ACTIVE_AGENTS`), turn limit (`AUTO_ADVANCE_TURNS`).
        *   Auto-save of each turn to Chronicle and `auto_advance_history`.
        *   Context passing between agents, with summarization for long discussions (using `AUTO_ADVANCE_CONTEXT_HISTORY_MAX_TURNS` and `AUTO_ADVANCE_SUMMARY_AGENT`).
        *   Shaman variable participation rate (`SHAMAN_COUNCIL_PARTICIPATION_RATE`) with context catch-up.
        *   Special "user absent / group brainstorming" prompting.
    *   [F0422] **Agent-Specific Operational Modes:**
        *   ENV toggles for different system prompt variations per agent (e.g., Seer: Lucid/Cryptic; Shaman: Analytical/Sorcerer/Researcher/CRAG-like/Astral-Focus/Summarizer; Sage: Analytical/Strategic-Planner/Historical-Analyst/Diplomatic-Counsel).
        *   Managed by `agent_prompts.py` and selected/prompted by `main.py`.
    *   [F0423] **Shaman's Search Suite & Task Management:**
        *   [F0423a] **Search Suite:**
            *   Level 1: Standard Web Search (DuckDuckGo).
            *   Level 2: Deep Web Search (SearxNG integration - user provides SearxNG URL in `.env`).
            *   Level 3: Dark Web Search (Tor backend - user configures Tor SOCKS proxy in `.env`, explicit user opt-in and warnings).
            *   Level 4: Akashic Records + Library Search.
            *   Level 5: Search Everything (Combined Strategy).
        *   [F0423b] **Task Management Tool:** Shaman interacts with `tasks.db` (via `memory_interface.py`) to create, update, query its own tasks, or delegate tasks to other agents.
    *   [F0424] **Experimental Agent Evolution Layers (Attempt for v0.4, else v0.5+):**
        *   [F0424a] **Neural Graffiti (Shaman):** ENV toggles for modes (`pytorch_direct`, `pre_gguf_bias`, `post_gguf_filter`), drift control (`GRAFFITI_DRIFT_ENABLED`), state persistence (`GRAFFITI_STATE_PATH`, `_SAVE_INTERVAL_TURNS`), PyTorch model config (`GRAFFITI_AGENT_PYTORCH_MODEL_ID`, `_DEVICE`), layer params (`GRAFFITI_MEMORY_BANK_SIZE`, `_SPRAY_LAMBDA`, `_SPRAY_ALPHA`). "Personality Snapshot" saving/loading.
        *   [F0424b] **Black Magick Mindmap Modifier (BMMM):** ENV toggles for modes (`Chaotic Brainstorming`, `Divination Arts`, `Sigil Seed`, `Matrix Hacking`), depth scaling (`[AGENT_NAME]_BMMM_MODE`, `_BMMM_DEPTH_SCALE`).
        *   [F0424c] **Shaman's "Evolutionary Optimizer Mode" (AlphaEvolve-inspired):** For user-defined problems with Python evaluation functions (sandboxed execution).
        *   [F0424d] **Meta-Prompt Evolution (Advanced Prompt Graffiti):** Shaman suggests/tests prompt variations based on performance metrics/user feedback.
    *   [F0425] **Prompt Graffiti (Shaman-Suggested Prompt Evolution):** Shaman analyzes agent performance/drift and suggests system prompt component changes to the user for approval.
    *   [F0426] **Character Stat Tracking (Shaman + Profile DB):** Shaman proposes updates to user "stats" (inferred personality traits, preferences) based on interaction analysis; user verifies.
*   **F0430: Enhanced Modalities & Integrations:**
    *   [F0431] **VLM Refinement:** Improved VLM prompting, support for different VLM models. Agents can request VLM analysis. F9-F12 confirmation loop for VLM analysis turns.
    *   [F0432] **"Library" Feature (LlamaIndex Powered - Full Integration):**
        *   User-managed `OracleAI\Library\` folder (path configurable in `.env`).
        *   `scripts/library_manager.py`: Uses LlamaIndex `DocumentLoaders` (including PDF/EPUB via Langchain loaders, with OCR for scanned PDFs) to ingest, chunk, and create a dedicated vector index (part of The Sanctum) for Library content.
        *   Shaman "Local Library Search" mode and "Deep Web + Library Search" mode using this LlamaIndex query engine as a tool.
        *   **[GUI] Streamlined Content Ingestion:** Drag-and-drop, URL pasting for Library.
    *   [F0433] **[v0.4+] ComfyUI Integration (Text-to-Image):** Agents can generate images based on prompts/descriptions. Displayed in GUI. Configurable timing (real-time vs. pre-loading).
    *   [F0434] **[v0.4+] LiteLLM Integration:** Refactor `llm_interface.py` for flexible backend support (Ollama, LM Studio, cloud APIs if user opts-in).
*   **F0440: Polished GUI & User Experience (NiceGUI + Tauri):**
    *   [F0441] Full "Oracle Temple" / "Techno-Mysticism" aesthetic realized.
    *   [F0442] Comprehensive Akashic Record Management Interface:
        *   [F0442a] **"Astral Explorer Mode" (2D):** For Citadel KG visualization (Entities/Relationships), MemCon cache review, Library document browsing/status.
    *   [F0443] Advanced dashboards for Shaman tasks ("Hyperspace Journey" with holographic planet icons), agent status, emotional trends, NLU insights.
    *   [F0444] Contextual Memory Injection Preview toggler (qvink-inspired).
    *   [F0445] GUI elements for key ENV Toggles (e.g., Shaman Tag Suggestions, DCWM).
*   **F0450: System Robustness & Documentation:**
    *   [F0451] **Automated Setup Script (`setup_oracleai.bat/.sh`).**
    *   [F0452] Comprehensive end-user and developer documentation (v0.4 ReadMe, v0.4 Design Document including Appendix R and fully updated Appendix Z).
    *   [F0453] Rigorous testing, performance profiling, and optimization across all features.
*   **F0460: Advanced Concepts (v0.4+ Research & Stretch Goals - Original List):**
    *   [F0461] **Multi-User Voice ID (Speaker Diarization/Identification):** For potential future multi-user scenarios.
    *   [F0462] **Explainable AI (XAI):** Enhanced capabilities for agents to trace and explain their reasoning and the sources of their information from the Akashic Record.
    *   [F0463] **PKM Tool Integration (Obsidian, Logseq, etc.):** Bidirectional sync or interaction.
    *   [F0464] **"Oracle Glasses" Vision:** Conceptual groundwork for future AR integration.
*   **F0470: Advanced Concepts (v0.5+ Vision - To be detailed in Section 18 of DD, incorporating deferred items from Appendix R discussion):**
    *   [F0471] **Real-Time AR Integration & Environmental Awareness.**
    *   [F0472] **3D Graphing/Visualization of Akashic Modules.**
    *   [F0473] **True "Living Agent" Evolution with Deep KBLaM/Advanced CAG & Meta-Learning.**
    *   [F0474] Selective KV Caching (dependent on backend support).
    *   [F0475] Dedicated High-Performance Graph Database for The Citadel.
    *   [F0476] Advanced Browser/File System tools for Shaman (re-evaluate scope/security for v0.5).
    *   [F0477] Full multi-device sync with a "home server" model (Tailscale/FastAPI based, master machine R/W).
    *   [F0478] Zotero Integration.
    *   [F0479] Multi-User Collaboration & Federated Akashic Records (potential scope shift, re-evaluate against single-user focus).