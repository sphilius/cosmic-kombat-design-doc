### Domain 1: Gameplay Systems To-Do List

---

#### 1. Document Universal Mechanics

**Overall Goal:** Create a foundational document that specifies the core mechanics available to every character in the game.

*   **1.1: Define Standard Movement**
    *   **Information Needed:**
        *   Forward walk speed (units per second)
        *   Backward walk speed (units per second)
        *   Forward dash distance, startup frames, and total duration
        *   Backward dash distance, startup frames, and total duration
    *   **Definition of Done:** A section in the Game Design Document (GDD) titled "Universal Movement" contains a table with finalized values for these properties.

*   **1.2: Define Jump and Air Movement**
    *   **Information Needed:**
        *   Jump startup frames (pre-launch)
        *   Time to jump apex (in seconds/frames)
        *   Jump height (in units)
        *   Number of air jumps allowed (e.g., 1)
        *   Number of air dashes allowed (e.g., 1)
        *   Air control acceleration (how quickly the player can influence momentum in the air)
    *   **Definition of Done:** A subsection in the GDD under "Universal Movement" contains a table with finalized values for these jump and air movement properties.

*   **1.3: Define Universal Basic Attacks**
    *   **Information Needed:** For a standing, crouching, and jumping version of a Light, Medium, and Heavy attack (9 attacks total):
        *   Input command (e.g., "5L" for standing light)
        *   Frame Data: Startup, Active, Recovery frames
        *   Damage on hit
        *   Percentage on hit (for the dual health system)
        *   Hitstun duration (in frames)
        *   Blockstun duration (in frames)
        *   Special properties (e.g., "launches on hit")
    *   **Definition of Done:** A section in the GDD titled "Universal Attacks" contains a table with finalized data for these 9 baseline attacks.

---

#### 2. Define Tier-Specific Modifiers

**Overall Goal:** Document the exact gameplay impact of the 12-tier system.

*   **2.1: Create Tier Modifier Table**
    *   **Information Needed:** A list of all stats that will be affected by the tier system (e.g., Health, Damage Output, Movement Speed, Percentage Resistance).
    *   **Definition of Done:** A spreadsheet is created with Tiers 1-12 as rows and the stat categories as columns.

*   **2.2: Populate Tier Modifier Values**
    *   **Information Needed:** For each tier and each stat, a specific multiplier value (e.g., Tier 11 has 1.0x damage, Tier 10 has 1.1x damage).
    *   **Definition of Done:** The spreadsheet created in 2.1 is completely filled in with balanced and approved multiplier values. The spreadsheet is embedded or linked in the GDD.

---

#### 3. Create Damage Scaling Formulas

**Overall Goal:** Prevent infinite combos and ensure combat remains interactive.

*   **3.1: Design Combo Damage Scaling Formula**
    *   **Information Needed:** The mathematical formula that will be used to reduce the damage of each subsequent hit in a combo. This should include variables for the number of hits, the type of moves used, and any other relevant factors.
    *   **Definition of Done:** The formula is written out and explained in a new section of the GDD titled "Damage Scaling."

*   **3.2: Provide Scaling Examples**
    *   **Information Needed:** Using the formula from 3.1, provide at least three examples of a combo (e.g., a 3-hit, 5-hit, and 10-hit combo) and show the damage calculation for each hit.
    *   **Definition of Done:** The examples are documented in the "Damage Scaling" section of the GDD, demonstrating how the formula works in practice.

---

#### 4. Establish Frame Advantage Rules

**Overall Goal:** Create a clear and consistent system for determining who can act first after an interaction.

*   **4.1: Document Frame Advantage on Hit**
    *   **Information Needed:** The formula for calculating frame advantage on hit (`Frame Advantage = Blockstun - (Recovery + Active)`).
    *   **Definition of Done:** The formula is documented in a new GDD section titled "Frame Data and Advantage," with a clear explanation of each component.

*   **4.2: Document Frame Advantage on Block**
    *   **Information Needed:** The formula for calculating frame advantage on block (`Frame Advantage = Blockstun - (Recovery + Active)`).
    *   **Definition of Done:** The formula is documented in the "Frame Data and Advantage" section, with a clear explanation. It should be noted that blockstun values are typically different from hitstun values.

---

#### 5. Design Special Meter System

**Overall Goal:** Define the resource system that governs the use of special and ultimate moves.

*   **5.1: Define Meter Gain Conditions**
    *   **Information Needed:** A list of all actions that will build meter and the amount of meter gained for each (e.g., "Dealing Damage: 1 meter per 10 damage," "Blocking an attack: 2 meter").
    *   **Definition of Done:** A table of meter gain conditions and values is documented in a new GDD section titled "Special Meter System."

*   **5.2: Define Meter Spend Conditions**
    *   **Information Needed:** A list of all actions that will cost meter and their respective costs (e.g., "Special Move: 25 meter," "Ultimate Attack: 100 meter").
    *   **Definition of Done:** A table of meter spend conditions and costs is documented in the "Special Meter System" section of the GDD.

---
#### 6. Design and Document Character Movesets

**Overall Goal:** Create a standardized and complete moveset for the first two playable characters.

*   **6.1: Create a Moveset Template**
    *   **Information Needed:** A standardized format for documenting a character's moveset, including sections for an overview, normal attacks, special moves, and ultimate attacks.
    *   **Definition of Done:** A markdown template file named `CHARACTER_MOVESET_TEMPLATE.md` is created and committed to the repository, ready for use.

*   **6.2: Document Moveset for Two Initial Characters**
    *   **Information Needed:** Using the created template, a complete moveset for the first two characters (e.g., a Tier 11 and a Tier 8 character) must be filled out with all frame data, damage, and properties.
    *   **Definition of Done:** Two new markdown files, `CHARACTER_01_MOVESET.md` and `CHARACTER_02_MOVESET.md`, are created and completed in the repository.

---

#### 7. Design and Document Combo System

**Overall Goal:** Define the core rules that govern how players can chain attacks together.

*   **7.1: Define Combo Chaining Rules**
    *   **Information Needed:** The specific rules for which normal attacks can be canceled into other normal attacks (e.g., a "light -> medium -> heavy" gatling system).
    *   **Definition of Done:** A section in the GDD titled "Combo System" clearly documents the allowed normal-to-normal attack chains.

*   **7.2: Define Combo Linking Rules**
    *   **Information Needed:** An explanation of how to perform "links" (timing an attack to hit as soon as the character recovers from the previous one) based on frame advantage.
    *   **Definition of Done:** The "Combo System" section of the GDD explains the concept of linking with at least two practical examples using the universal basic attacks.

*   **7.3: Define Special and Ultimate Cancels**
    *   **Information Needed:** The rules for which moves can be canceled into special moves or ultimate attacks, and during which frames (startup, active, or recovery).
    *   **Definition of Done:** The "Combo System" section of the GDD documents the cancellation rules for all universal normal attacks.

---

#### 8. Design and Document Environmental Interactions

**Overall Goal:** Specify how characters interact with the boundaries of the stage.

*   **8.1: Define Wall Interactions**
    *   **Information Needed:** The behavior of characters when they are knocked into the walls of a stage. This includes defining "Wall Splat" (sticking to the wall, vulnerable to a combo) and "Wall Bounce" (bouncing off the wall for a juggle).
    *   **Definition of Done:** A section in the GDD titled "Environmental Interactions" documents the specific mechanics, including hitstun duration for a wall splat and the trajectory for a wall bounce.

*   **8.2: Define Stage-Specific Interactions**
    *   **Information Needed:** A list of any unique interactions available on specific stages (e.g., breakable floors or walls). For the initial design, this may just be a statement that there are none.
    *   **Definition of Done:** The "Environmental Interactions" section of the GDD documents any stage-specific mechanics or confirms their absence for the initial release.

---

#### 9. Design and Document Air Combat

**Overall Goal:** Define the rules for combat that takes place in the air.

*   **9.1: Define Air Combo Rules**
    *   **Information Needed:** The rules for how combos work in the air, including how many air attacks can be used in a single jump before landing.
    *   **Definition of Done:** A section in the GDD titled "Air Combat" documents the air combo rules, including any limits on air dashes or special moves within a combo.

*   **9.2: Define Juggle System**
    *   **Information Needed:** The mechanics of hitting an opponent who is in a helpless, airborne state. This must include formulas for how gravity and hitstun are affected with each successive juggle hit to prevent infinites.
    *   **Definition of Done:** The "Air Combat" section of the GDD documents the juggle system mechanics and provides formulas for juggle scaling.

---

#### 10. Design and Document Defensive Systems

**Overall Goal:** Provide players with a clear and robust set of defensive options.

*   **10.1: Define Blocking**
    *   **Information Needed:** The properties of blocking, including high/low blocking rules, chip damage percentage from special moves, and the mechanics of a "Guard Crush" state.
    *   **Definition of Done:** A section in the GDD titled "Defensive Systems" documents the complete mechanics of blocking.

*   **10.2: Define Parrying**
    *   **Information Needed:** The mechanics of the parry system, including the input, the timing window in frames, and the specific frame advantage or combo opportunity granted on a successful parry.
    *   **Definition of Done:** The "Defensive Systems" section of the GDD documents the parry mechanic in detail.

*   **10.3: Define Counter-Attacks**
    *   **Information Needed:** The mechanics of any dedicated counter-attack moves that may exist for certain characters, including their input and properties.
    *   **Definition of Done:** The "Defensive Systems" section of the GDD documents the universal design for counter-attack moves, if any.

---

#### 11. Design and Document Throws/Grabs

**Overall Goal:** Define the close-range, unblockable attack system.

*   **11.1: Define Throw Mechanics**
    *   **Information Needed:** The input for throws, their effective range, startup frames, damage, and whether they can hit an opponent who is in hitstun or blockstun.
    *   **Definition of Done:** A section in the GDD titled "Throws and Grabs" documents the complete throw mechanics.

*   **11.2: Define Throw Teching**
    *   **Information Needed:** The input and timing window (in frames) for a player to escape a throw, and the resulting state for both players (e.g., pushed apart, neutral situation).
    *   **Definition of Done:** The "Throws and Grabs" section of the GDD documents the throw tech mechanic in detail.
