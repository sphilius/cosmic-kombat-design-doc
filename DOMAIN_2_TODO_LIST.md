### Domain 2: Technical Infrastructure To-Do List

---

#### 1. Define Data Schemas

**Overall Goal:** Create a clear, consistent, and enforceable structure for all game data to prevent errors and simplify tool creation.

*   **1.1: Design Character Data Schema**
    *   **Information Needed:** A comprehensive list of all data points for a character (e.g., `characterId`, `tier`, `baseHealth`, `walkSpeed`, `weight`).
    *   **Definition of Done:** A JSON Schema file (`schemas/character.schema.json`) is created that defines the structure, types, and validation rules for character data.

*   **1.2: Design Move Data Schema**
    *   **Information Needed:** A comprehensive list of all data points for a single move (e.g., `moveId`, `frameData` (object), `damage`, `hitstun`, `blockstun`, `meterGain`).
    *   **Definition of Done:** A JSON Schema file (`schemas/move.schema.json`) is created that defines the structure and validation rules for move data.

---

#### 2. Document Event System API

**Overall Goal:** Create a robust, decoupled communication system for all parts of the game engine.

*   **2.1: Define Event Naming and Structure Convention**
    *   **Information Needed:** A consistent naming convention (e.g., `Domain.Subject.Verb`, like `Gameplay.Player.Died`) and a standard structure for event payloads.
    *   **Definition of Done:** The convention is documented in a new GDD section titled "Event System API," with examples.

*   **2.2: Document Core Gameplay Events**
    *   **Information Needed:** A list of critical gameplay events (e.g., `MatchStarted`, `RoundOver`, `PlayerTookDamage`, `MoveLanded`). For each, define its payload (e.g., `PlayerTookDamage` includes `victim`, `attacker`, `damageAmount`).
    *   **Definition of Done:** A table of core gameplay events and their payloads is added to the "Event System API" section of the GDD.

---

#### 3. Establish Performance Budgets

**Overall Goal:** Ensure the game runs smoothly on all target platforms by defining strict performance limits.

*   **3.1: Define Frame Rate and CPU Budget**
    *   **Information Needed:** Target frame rate (60 FPS) and the maximum milliseconds allowed per frame for major systems (e.g., `Physics: 2ms`, `Animation: 3ms`, `AI: 2ms`).
    *   **Definition of Done:** A table of per-system CPU time budgets is documented in a new GDD section titled "Performance Budgets."

*   **3.2: Define Memory and Network Budget**
    *   **Information Needed:** Maximum memory (RAM and VRAM) allocation for a standard match and the maximum network bandwidth per player per second.
    *   **Definition of Done:** The memory and network budgets are documented in the "Performance Budgets" section of the GDD.

---

#### 4. Create Technical Design Documents (TDDs)

**Overall Goal:** Provide engineering teams with detailed specifications for implementing major game systems.

*   **4.1: Write Replay System TDD**
    *   **Information Needed:** A detailed plan covering how replays are recorded (input stream vs. state-based), the file format, storage, and playback UI.
    *   **Definition of Done:** A `REPLAY_SYSTEM_TDD.md` document is completed and added to the repository.

*   **4.2: Write Spectator Mode TDD**
    *   **Information Needed:** A detailed plan for the spectator system, covering how it connects to live matches, data transmission, and latency targets.
    *   **Definition of Done:** A `SPECTATOR_MODE_TDD.md` document is completed and added to the repository.

*   **4.3: Write Save/Cloud Sync TDD**
    *   **Information Needed:** A plan for the save game format, what data is saved (settings, story progress, unlocks), and how it will sync with cloud services (Steam Cloud, PS Plus).
    *   **Definition of Done:** A `SAVE_SYSTEM_TDD.md` document is completed and added to the repository.

---

#### 5. Design Replay File Format

**Overall Goal:** Create an efficient and future-proof file format for game replays.

*   **5.1: Specify Replay Data Structure**
    *   **Information Needed:** The exact data to be stored in a replay file (e.g., game version, character selections, stage, and a timestamped list of all player inputs).
    *   **Definition of Done:** The data structure is formally documented within the `REPLAY_SYSTEM_TDD.md`.

*   **5.2: Choose a File Encoding Format**
    *   **Information Needed:** A decision on the encoding format (e.g., binary, JSON, MessagePack) based on file size and parsing speed requirements.
    *   **Definition of Done:** The chosen format and the reasoning for the choice are documented in the `REPLAY_SYSTEM_TDD.md`.

---

#### 6. Develop Cross-Platform Play Strategy

**Overall Goal:** Create a unified online experience for all players, regardless of their platform.

*   **6.1: Plan Platform Abstraction Layer**
    *   **Information Needed:** A design for an abstraction layer that handles platform-specific services like friends lists, achievements, and user profiles.
    *   **Definition of Done:** A `CROSS_PLATFORM_TDD.md` is created, outlining the design of this abstraction layer.

*   **6.2: Define Matchmaking and Session Management Flow**
    *   **Information Needed:** A flow diagram and technical plan for how a player on one platform can invite and play with a player on another.
    *   **Definition of Done:** The cross-platform session management flow is documented in the `CROSS_PLATFORM_TDD.md`.

---

#### 7. Design Anti-Cheat Strategy

**Overall Goal:** Protect the integrity of the competitive online environment.

*   **7.1: Research and Select Anti-Cheat Middleware**
    *   **Information Needed:** A comparative analysis of leading anti-cheat solutions (e.g., Easy Anti-Cheat, BattlEye) based on cost, integration effort, and effectiveness.
    *   **Definition of Done:** A decision is made and documented in a new `ANTI_CHEAT_STRATEGY.md` file.

*   **7.2: Plan for Server-Side Validation**
    *   **Information Needed:** A design for server-side checks to validate critical game state information and detect common cheats (e.g., speed hacks, cooldown manipulation).
    *   **Definition of Done:** The server-side validation plan is documented in the `ANTI_CHEAT_STRATEGY.md` file.
