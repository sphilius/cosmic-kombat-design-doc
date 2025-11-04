# Character Specification Template

**Character Name:** [Character Name]
**Tier:** [0-11]
**Archetype:** [Rushdown / Zoner / Grappler / All-Rounder / Aerial / Technical]
**Difficulty:** [Beginner / Intermediate / Advanced / Expert]

---

## Character Overview

### Visual Design
**Appearance:** [Detailed description of character appearance - body type, clothing, colors, defining features]

**Personality/Theme:** [What is this character's personality? What theme do they represent?]

**Power Level Justification:** [Why are they in this tier? What makes them this strong/weak?]

**Color Palette:**
- Primary: [Color]
- Secondary: [Color]
- Accent: [Color]
- VFX: [Color scheme for effects]

---

## Base Statistics

### Core Stats
- **Health:** [0-100, default 100]
- **Weight:** [Light / Medium-Light / Medium / Medium-Heavy / Heavy]
- **Walk Speed:** [1-10, default 5]
- **Dash Speed:** [1-10, default 5]
- **Jump Height:** [1-10, default 5]
- **Air Control:** [1-10, default 5]

### Tier Modifiers (Tier [X])
- **Hitbox Size Multiplier:** [e.g., 1.0 for Tier 11, scales up to 1.5 for Tier 0]
- **Knockback Modifier:** [0.8-1.5, affects how much this character knocks opponents back]
- **Damage Scaling:** [0.8-1.5, affects raw damage output]
- **Frame Data Modifier:** [Description of how tier affects frame data]

---

## Movement Abilities

### Ground Movement
- **Walk:** Forward/backward ground movement
  - Speed: [value]
  - Can be canceled into: [attacks, dash, jump]

- **Dash:** Fast forward movement
  - Duration: [frames]
  - Distance: [pixels or units]
  - Recovery: [frames]
  - Can be canceled into: [attacks, jump]

- **Backdash:** Evasive backward movement
  - Duration: [frames]
  - Invincibility frames: [frames] (if any)
  - Recovery: [frames]

### Aerial Movement
- **Jump:** Vertical leap
  - Startup: [frames]
  - Peak height: [pixels/units]
  - Fall speed: [value]
  - Air jumps: [0-2]

- **Air Dash:** [Yes/No]
  - Duration: [frames]
  - Distance: [pixels/units]
  - Uses per jump: [1-2]

---

## Universal Mechanics

### Blocking
- **Stand Block:** Blocks mid and high attacks
- **Crouch Block:** Blocks mid and low attacks
- **Air Block:** [Allowed/Not Allowed]
- **Pushback:** [Distance pushed back when blocking]

### Throws
- **Forward Throw:**
  - Startup: [frames]
  - Range: [distance]
  - Damage: [percentage / health]
  - Uncharged knockback: [distance]

- **Back Throw:** [Same format as forward throw]

---

## Move List

### Light Attacks

#### Light Attack 1 (LA1) - [Move Name]
**Input:** [e.g., Light button / L]
**Move Type:** [Standing / Crouching / Aerial / Special]
**Archetype Role:** [Poke / Anti-air / Pressure / Combo starter]

**Frame Data:**
- Startup: [frames] (frames before hitbox becomes active)
- Active: [frames] (frames hitbox is active)
- Recovery: [frames] (frames after active before character can act)
- On Hit: [+/- frames] (frame advantage when move hits)
- On Block: [+/- frames] (frame advantage when move is blocked)
- **Total Duration:** [frames]

**Properties:**
- Damage (Health): [amount]
- Damage (Percentage): [amount]
- Knockback: [distance at 0%, scales with percentage]
- Knockback Angle: [degrees, 0° = horizontal right, 90° = straight up]
- Hitstun: [frames]
- Blockstun: [frames]
- Range: [distance]
- Hitbox: [Description, e.g., "small circle in front of character"]

**Cancel Options:**
- Can cancel into: [Other attacks, specials, jump, dash]
- Cancel window: [frames X-Y]

**Special Properties:**
- [e.g., "Hits low, must be blocked crouching"]
- [e.g., "Can be chained into LA2 or LA3"]
- [Any unique mechanics]

**Animation Notes:**
- [Brief description of what the character does visually]
- [Key poses or smear frames needed]

**Audio:**
- SFX: [Description of sound effect needed]

---

#### Light Attack 2 (LA2) - [Move Name]
[Same format as LA1]

---

#### Light Attack 3 (LA3) - [Move Name]
[Same format as LA1]

---

### Medium Attacks

#### Medium Attack 1 (MA1) - [Move Name]
**Input:** [e.g., Medium button / M]
**Move Type:** [Standing / Crouching / Aerial / Special]
**Archetype Role:** [Poke / Anti-air / Launcher / Combo tool]

[Same detailed format as Light Attacks, but with higher damage/longer startup/more recovery]

---

### Heavy Attacks

#### Heavy Attack 1 (HA1) - [Move Name]
**Input:** [e.g., Heavy button / H]
**Move Type:** [Standing / Crouching / Aerial / Special]
**Archetype Role:** [Punish / Launcher / Wall break / Combo ender]

[Same detailed format, highest damage and longest recovery]

---

### Special Moves

#### Special Move 1 (SP1) - [Move Name]
**Input:** [e.g., Quarter-circle forward + Special / Down, Down-Forward, Forward + S]
**Move Type:** [Projectile / Command grab / Movement / Buff]
**Archetype Role:** [Zoning / Mixup / Mobility / Pressure]

**Frame Data:**
[Same as above, but may have additional properties]

**Properties:**
- Damage (Health): [amount]
- Damage (Percentage): [amount]
- Knockback: [distance]
- Projectile Speed: [if applicable]
- Projectile Durability: [if applicable, can it be destroyed?]
- Special Meter Cost: [if meter system exists]

**Special Properties:**
- [e.g., "Projectile can be reflected"]
- [e.g., "Overhead, must be blocked standing"]
- [e.g., "Armored on frames 5-10"]

---

#### Special Move 2 (SP2) - [Move Name]
[Same format as SP1]

---

### Ultimate Attack (ULTRA) - [Move Name]

**Input:** [Complex input or simple button when conditions met]
**Activation Condition:** [e.g., "Press Ultimate button when opponent is below 30% health"]
**Move Type:** Cinematic Ultimate / Super Move
**Archetype Role:** High damage finisher

**Frame Data:**
- Startup: [frames]
- Active: [frames] (invincibility often granted)
- Recovery: [frames]
- Total Duration: [frames]

**Properties:**
- Damage (Health): [high amount, often 25-40]
- Damage (Percentage): [high amount, often 30-50%]
- Knockback: [Very high, often kills above certain percentage]
- Invincibility: [frames, usually entire startup]
- Range: [Often larger than normal moves]

**Cinematic Elements:**
- [Description of cinematic camera work]
- [Key visual moments]
- [Duration of cinematic]

**Special Properties:**
- [e.g., "Unblockable"]
- [e.g., "Can only be used once per round"]
- [e.g., "Costs full meter"]

---

## Combo Routes

### Basic Combo (BnB - Bread and Butter)
**Input Sequence:** [e.g., LA1 → LA2 → MA1 → HA1]
**Total Damage:** [Health + Percentage]
**Difficulty:** Beginner
**Notes:** [When to use, confirms, etc.]

### Intermediate Combo
**Input Sequence:** [More complex sequence]
**Total Damage:** [Higher than basic]
**Difficulty:** Intermediate
**Notes:** [Requires spacing, timing, etc.]

### Advanced Combo
**Input Sequence:** [Most complex, requires precise execution]
**Total Damage:** [Highest]
**Difficulty:** Advanced
**Notes:** [Situational, requires specific setup]

### Tier-Specific Combo
**Description:** [Combo that leverages this tier's unique properties]
**Input Sequence:**
**Notes:**

---

## Playstyle Guide

### Strengths
- [List of character's strong points]
- [What they do better than most]
- [Optimal range or situation]

### Weaknesses
- [List of character's weak points]
- [What they struggle with]
- [Bad matchups or situations]

### Gameplan
**Neutral Game:**
[How to approach neutral, what buttons to use, spacing goals]

**Offense:**
[How to pressure, mixup options, confirm options]

**Defense:**
[How to escape pressure, reversal options, defensive tools]

**Tier Matchup Strategy:**
- **vs Lower Tiers:** [How to leverage power advantage]
- **vs Same Tier:** [Even matchup strategy]
- **vs Higher Tiers:** [How to compensate for disadvantage]

---

## Tier-Specific Properties

### Tier [X] Characteristics
- **Visual Scale:** [e.g., Tier 11 characters are normal human-sized]
- **VFX Intensity:** [e.g., Light to moderate particle effects]
- **Frame Data Philosophy:** [e.g., Faster startup, shorter recovery, smaller hitboxes]
- **Power Fantasy:** [What does it feel like to play this tier?]

### Balance Considerations
- [How does this character balance against other Tier X characters?]
- [How does tier system affect this character specifically?]
- [Any special tier-based mechanics unique to this character?]

---

## Art Asset Requirements

### Sprite Sheets Needed
1. **Idle Animation:** [X frames at Y FPS]
2. **Walk Cycle:** [X frames at Y FPS]
3. **Dash:** [X frames]
4. **Jump:** [Startup, peak, fall - X frames total]
5. **LA1:** [X frames]
6. **LA2:** [X frames]
7. **LA3:** [X frames]
8. **MA1:** [X frames]
9. **HA1:** [X frames]
10. **SP1:** [X frames]
11. **SP2:** [X frames]
12. **Ultimate:** [X frames + cinematic poses]
13. **Hit Reactions:** [Light hit, heavy hit, launched]
14. **Block:** [Stand block, crouch block]
15. **Throws:** [Throwing, being thrown]
16. **Victory:** [X frames]
17. **Defeat:** [X frames]

**Total Estimated Frames:** [Calculate total]
**Art Style Notes:** [Any specific requirements for this character]

---

### VFX Assets Needed
1. **Hit Sparks:** [Style and color]
2. **Attack Trails:** [For each attack type]
3. **Special Move Effects:** [Unique per special]
4. **Ultimate Effect:** [Most elaborate, cinematic quality]
5. **Movement Effects:** [Dash trails, jump dust, etc.]

---

## Audio Asset Requirements

### Sound Effects
1. **Voice Clips:** [If any - attack grunts, victory, defeat]
2. **Attack SFX:** [Whoosh, impact, heavy impact]
3. **Special Move SFX:** [Unique sound per special]
4. **Ultimate SFX:** [Epic sound effect]
5. **Movement SFX:** [Footsteps, dash, jump land]

---

## Implementation Notes

### Godot Scene Structure
```
CharacterName.tscn (root)
├── AnimationPlayer
├── Sprite2D
├── StateMachine
│   ├── Idle
│   ├── Walk
│   ├── Dash
│   ├── Jump
│   ├── [Attack states]
│   └── Hitstun/Blockstun
├── HitboxManager
│   ├── Hitbox (Area2D - attack hitboxes)
│   └── Hurtbox (Area2D - collision box)
├── HealthSystem
│   ├── PercentageTracker
│   └── HealthBarTracker
└── InputBuffer
```

### JSON Data File
- Character stats stored in `data/characters/character_name.json`
- Move data stored in `data/moves/character_name_moves.json`
- Can be edited without recompiling

### Testing Checklist
- [ ] All moves animate correctly
- [ ] Frame data matches specification
- [ ] Hitboxes match visual expectation
- [ ] Combos connect reliably
- [ ] No unintended infinites or exploits
- [ ] Balanced against other characters
- [ ] Tier modifiers apply correctly
- [ ] Performance: maintains 60 FPS

---

## Balance Version History

### v1.0 (Initial)
- [Initial balance decisions]

### v1.1 (After testing)
- [Changes made based on playtesting]
- [Buffs/nerfs with reasoning]

---

## Notes & Ideas

[Any additional thoughts, potential alternate moves, Easter eggs, lore connections, etc.]

---

**Template Version:** 1.0
**Last Updated:** 2025-10-24
