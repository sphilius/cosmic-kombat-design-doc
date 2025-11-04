# Character Specification: Ryn

**Character Name:** Ryn "The Striker"
**Tier:** 11 (Human-level)
**Archetype:** All-Rounder
**Difficulty:** Beginner

---

## Character Overview

### Visual Design
**Appearance:** Athletic human male in his mid-20s with a lean, muscular build. Wears a sleeveless martial arts gi (top half tied around waist), showing toned arms and torso. Black combat pants with red accents. Short dark hair with red highlights. Wrapped hands/forearms with fighting tape. Height: 5'10" (178cm).

**Personality/Theme:** Disciplined street fighter who trained in mixed martial arts. Confident but not cocky. Represents the "everyman" fighter - no superpowers, just pure skill and determination. The Charlie/Ryu archetype of this game.

**Power Level Justification:** Tier 11 represents peak human capability without supernatural enhancement. Ryn is an exceptional martial artist but operates entirely within human physical limits. Fast, technical, and well-rounded but lacks the raw power or abilities of higher tiers.

**Color Palette:**
- Primary: Charcoal gray (pants, gi)
- Secondary: Deep red (accents, highlights)
- Accent: White (hand wraps, belt)
- VFX: Bright red energy trails with white sparks

---

## Base Statistics

### Core Stats
- **Health:** 100 (standard)
- **Weight:** Medium (standard weight, balanced knockback received)
- **Walk Speed:** 5 (average mobility)
- **Dash Speed:** 7 (above average - his strength is mobility)
- **Jump Height:** 6 (slightly above average)
- **Air Control:** 6 (good aerial movement)

### Tier Modifiers (Tier 11)
- **Hitbox Size Multiplier:** 1.0 (human-sized, smallest in game)
- **Knockback Modifier:** 1.0 (deals standard knockback)
- **Damage Scaling:** 1.0 (standard damage output)
- **Frame Data Modifier:** Fastest in game - quick startup, short recovery, smaller hitboxes, less active frames. Embodies "fast but weak" Tier 11 philosophy.

---

## Movement Abilities

### Ground Movement
- **Walk:** Forward/backward ground movement
  - Speed: 5.0 units/second
  - Can be canceled into: Any attack, dash, jump, block

- **Dash:** Fast forward movement with slight slide
  - Duration: 18 frames
  - Distance: 3.0 units
  - Recovery: 8 frames
  - Can be canceled into: Any attack (frame 10+), jump (frame 5+)

- **Backdash:** Evasive backward movement
  - Duration: 22 frames
  - Invincibility frames: 1-8 (upper body only)
  - Recovery: 10 frames
  - Distance: 2.5 units backward

### Aerial Movement
- **Jump:** Quick vertical leap
  - Startup: 4 frames (fast jump)
  - Peak height: 4.5 units
  - Total air time: 48 frames
  - Fall speed: Standard gravity
  - Air jumps: 0 (grounded fighter)

- **Air Dash:** No
  - Ryn is a grounded fighter, no air dash capability

---

## Universal Mechanics

### Blocking
- **Stand Block:** Blocks mid and high attacks
- **Crouch Block:** Blocks mid and low attacks
- **Air Block:** Not Allowed (Tier 11 limitation)
- **Pushback:** 0.3 units per blocked hit

### Throws
- **Forward Throw:**
  - Startup: 5 frames (fast throw)
  - Range: 1.2 units
  - Damage: 8% health, 12% percentage
  - Knockback: Soft knockdown, opponent 2.5 units away

- **Back Throw:**
  - Startup: 5 frames
  - Range: 1.2 units
  - Damage: 8% health, 12% percentage
  - Knockback: Hard knockdown, opponent 3.0 units away, Ryn switches sides

---

## Move List

### Light Attacks

#### Light Attack 1 (LA1) - Quick Jab
**Input:** Light button (standing)
**Move Type:** Standing normal
**Archetype Role:** Poke / Pressure / Combo starter

**Frame Data:**
- Startup: 5 frames (extremely fast)
- Active: 2 frames
- Recovery: 8 frames
- On Hit: +5 frames (can continue pressure)
- On Block: +1 frames (slightly plus, safe)
- **Total Duration:** 15 frames

**Properties:**
- Damage (Health): 3
- Damage (Percentage): 2%
- Knockback: Minimal (0.2 units at 0%, +0.01 per 10%)
- Knockback Angle: 60° (slight upward launch)
- Hitstun: 12 frames
- Blockstun: 10 frames
- Range: 1.5 units (short but reliable)
- Hitbox: Small circle (0.4 unit radius) at fist position

**Cancel Options:**
- Can cancel into: LA2, LA3, MA1, throws, specials
- Cancel window: Frames 6-15 (on hit or block)

**Special Properties:**
- Fastest normal in the game
- Can be chained into itself on hit (frame trap)
- Primary neutral tool and pressure starter

**Animation Notes:**
- Quick straight punch with lead hand (left)
- Minimal body movement, punch extends from guard position
- 2-3 frame smear on extension
- Returns to neutral stance quickly

**Audio:**
- SFX: Sharp, crisp "whoosh" sound (light impact)

---

#### Light Attack 2 (LA2) - Follow-up Strike
**Input:** Light button after LA1
**Move Type:** Chain normal
**Archetype Role:** Pressure / Combo connector

**Frame Data:**
- Startup: 6 frames
- Active: 3 frames
- Recovery: 10 frames
- On Hit: +4 frames
- On Block: 0 frames (neutral)
- **Total Duration:** 19 frames

**Properties:**
- Damage (Health): 4
- Damage (Percentage): 3%
- Knockback: Light (0.5 units at 0%, +0.02 per 10%)
- Knockback Angle: 70°
- Hitstun: 14 frames
- Blockstun: 11 frames
- Range: 1.8 units
- Hitbox: Medium circle (0.6 unit radius)

**Cancel Options:**
- Can cancel into: LA3, MA1, HA1, specials
- Cancel window: Frames 8-19

**Special Properties:**
- Natural chain from LA1
- Slightly more range than jab
- Good for confirming into bigger combos

**Animation Notes:**
- Cross punch with rear hand (right)
- Slight hip rotation for power
- Body weight shifts forward

**Audio:**
- SFX: Deeper "whoosh" than LA1, slightly louder impact

---

#### Light Attack 3 (LA3) - Low Sweep
**Input:** Down + Light button
**Move Type:** Crouching normal
**Archetype Role:** Low mixup / Trip

**Frame Data:**
- Startup: 8 frames
- Active: 4 frames
- Recovery: 14 frames
- On Hit: Knockdown (+20 frames advantage)
- On Block: -5 frames (unsafe, punishable by fast moves)
- **Total Duration:** 26 frames

**Properties:**
- Damage (Health): 5
- Damage (Percentage): 4%
- Knockback: Sweep knockdown (opponent falls, 1.0 units back)
- Knockback Angle: 20° (low sweep angle)
- Hitstun: N/A (knockdown)
- Blockstun: 12 frames
- Range: 2.0 units
- Hitbox: Wide, low rectangle (2.0 x 0.5 units)

**Cancel Options:**
- Cannot cancel on block (committed)
- Can cancel into specials on hit (frames 10-26)

**Special Properties:**
- Hits LOW - must be blocked crouching
- Causes hard knockdown on hit
- Unsafe on block but good reward
- Good for mixup after establishing stand block pressure

**Animation Notes:**
- Crouches low, extends leg in sweeping motion
- Body rotates with sweep
- Returns to crouch after recovery

**Audio:**
- SFX: "Swoosh" with foot scraping ground sound

---

### Medium Attacks

#### Medium Attack 1 (MA1) - Body Blow
**Input:** Medium button (standing)
**Move Type:** Standing normal
**Archetype Role:** Combo tool / Launcher / Anti-air

**Frame Data:**
- Startup: 8 frames
- Active: 4 frames
- Recovery: 16 frames
- On Hit: +8 frames (good for follow-ups)
- On Block: -3 frames (relatively safe)
- **Total Duration:** 28 frames

**Properties:**
- Damage (Health): 8
- Damage (Percentage): 6%
- Knockback: Medium (1.5 units at 0%, +0.05 per 10%)
- Knockback Angle: 75° (launches upward)
- Hitstun: 20 frames
- Blockstun: 15 frames
- Range: 1.6 units
- Hitbox: Large circle (0.8 unit radius), slightly elevated

**Cancel Options:**
- Can cancel into: HA1, specials, ultimate
- Cancel window: Frames 10-28

**Special Properties:**
- Primary launcher - puts opponent in air on hit
- Can be used as anti-air (hits above character)
- Good combo starter from light confirms
- Upper body invincibility frames 6-10 (anti-air property)

**Animation Notes:**
- Rising uppercut-style body blow
- Body coils then explodes upward
- Fist travels from low to high
- Full body extension at peak

**Audio:**
- SFX: Deep "THUD" impact sound

---

#### Medium Attack 2 (MA2) - Spinning Backfist
**Input:** Back + Medium button
**Move Type:** Command normal
**Archetype Role:** Spacing / Whiff punish

**Frame Data:**
- Startup: 11 frames
- Active: 5 frames
- Recovery: 18 frames
- On Hit: +6 frames
- On Block: -6 frames (unsafe)
- **Total Duration:** 34 frames

**Properties:**
- Damage (Health): 10
- Damage (Percentage): 7%
- Knockback: Medium-high (2.0 units at 0%, +0.06 per 10%)
- Knockback Angle: 45° (good for stage positioning)
- Hitstun: 22 frames
- Blockstun: 16 frames
- Range: 2.5 units (longest normal)
- Hitbox: Wide arc (sweeping hitbox)

**Cancel Options:**
- Can cancel into: Specials, ultimate (on hit only)
- Cancel window: Frames 14-34

**Special Properties:**
- Longest range normal attack
- Slightly slower but great for catching backdashes
- Spins Ryn 180°, hits behind him briefly (anti-crossup frames 12-14)
- Unsafe on block, reward for spacing

**Animation Notes:**
- Full body spin, arm extended
- Creates whirlwind effect visually
- Ends facing opponent

**Audio:**
- SFX: "WHOOSH" with wind effect

---

### Heavy Attacks

#### Heavy Attack 1 (HA1) - Power Strike
**Input:** Heavy button (standing)
**Move Type:** Standing heavy
**Archetype Role:** Punish / Combo ender / Wall bounce

**Frame Data:**
- Startup: 14 frames
- Active: 6 frames
- Recovery: 24 frames
- On Hit: Knockdown (+30 frames)
- On Block: -12 frames (very unsafe, fully punishable)
- **Total Duration:** 44 frames

**Properties:**
- Damage (Health): 15
- Damage (Percentage): 12%
- Knockback: High (3.5 units at 0%, +0.1 per 10%)
- Knockback Angle: 30° (low angle, good for ring-outs)
- Hitstun: N/A (knockdown)
- Blockstun: 18 frames
- Range: 2.0 units
- Hitbox: Large (1.0 unit radius)

**Cancel Options:**
- Can cancel into: Ultimate only (frames 18-44, on hit)
- No special cancels (committed move)

**Special Properties:**
- Causes wall bounce if opponent hits stage boundary
- Slow but very high damage
- Great combo ender
- Causes spinning knockdown animation
- Only use when guaranteed (combo ender or hard punish)

**Animation Notes:**
- Wind-up overhead punch
- Full body weight behind strike
- Character grunts with effort
- Exaggerated follow-through animation

**Audio:**
- SFX: Heavy "CRACK" impact, deep bass frequency

---

### Special Moves

#### Special Move 1 (SP1) - Rushing Charge
**Input:** Quarter-circle forward + Special (236+S)
**Move Type:** Movement special / Strike
**Archetype Role:** Mobility / Pressure / Mixup

**Frame Data:**
- Startup: 12 frames
- Active: 8 frames (hits multiple times during dash)
- Recovery: 16 frames
- On Hit: +15 frames (knockdown)
- On Block: -8 frames (unsafe)
- **Total Duration:** 36 frames

**Properties:**
- Damage (Health): 12 (multi-hit: 3+3+3+3)
- Damage (Percentage): 10% (2.5% per hit)
- Knockback: Medium (2.0 units, launches on final hit)
- Knockback Angle: 60°
- Range: 3.5 units (moves Ryn forward)
- Hitbox: Body hitbox during dash
- Hits: 4 rapid hits

**Special Properties:**
- Fast forward movement (covers 3.5 units)
- Can pass through projectiles (frames 8-16)
- Multi-hit: can be interrupted between hits
- Good for closing distance quickly
- Punishable on block
- Has EX version (if meter system added later)

**Animation Notes:**
- Ryn dashes forward in blur motion
- Red energy trail follows
- Multiple strike poses during dash
- Ends in strong stance

**Audio:**
- SFX: Rushing wind + rapid "pa-pa-pa-pa" hits

---

#### Special Move 2 (SP2) - Rising Fist
**Input:** Dragon punch motion + Special (623+S)
**Move Type:** Invincible reversal / Anti-air
**Archetype Role:** Defensive tool / Combo ender

**Frame Data:**
- Startup: 6 frames
- Active: 12 frames (hits three times during ascent)
- Recovery: 28 frames (20 landing, +8 landing recovery)
- On Hit: Knockdown (+40 frames, opponent high in air)
- On Block: -20 frames (extremely unsafe)
- **Total Duration:** 46 frames total (ascent + landing)

**Properties:**
- Damage (Health): 18 (6+6+6 three hits)
- Damage (Percentage): 15% (5% per hit)
- Knockback: Very high (4.0 units, straight up 90°)
- Knockback Angle: 90° (launches vertically)
- Invincibility: Frames 1-8 (full invincibility)
- Range: Ascends 5.0 units vertically
- Hitbox: Around fist, travels upward

**Special Properties:**
- **Fully invincible on startup** (classic DP property)
- Best anti-air in Ryn's kit
- Can be used as reversal to escape pressure
- Extremely punishable on block or whiff
- Risk/reward tool
- Final hit causes spinning knockdown

**Animation Notes:**
- Explosive upward jump with uppercut
- Spins during ascent
- Red spiral energy trails
- Vulnerable on landing (big recovery animation)

**Audio:**
- SFX: "RISING!" voice clip + powerful "WOOSH-CRACK" impact

---

### Ultimate Attack (ULTRA) - Striker's Fury

**Input:** Ultimate button (when available)
**Activation Condition:** Opponent must be in hit state or very close range (command grab properties)
**Move Type:** Cinematic Ultimate / Rush Super
**Archetype Role:** High damage finisher / Comeback tool

**Frame Data:**
- Startup: 8 frames (fast for ultimate)
- Active: 4 frames (grab window)
- Total Duration: 180 frames (3 seconds full cinematic)
- Invincibility: Frames 1-12 (fully invincible startup)

**Properties:**
- Damage (Health): 35
- Damage (Percentage): 40%
- Knockback: Ring-out level (7.0+ units, 45° angle)
- Range: 2.0 units (must be close)
- Grab range: 2.0 units (slightly better range than normal throw)

**Cinematic Elements:**
1. **Grab (frames 1-20):** Ryn grabs opponent, screen flashes red
2. **Rush sequence (frames 21-140):** Cinematic camera, Ryn delivers 20-hit combo sequence at high speed
   - Multiple camera angles
   - Speed lines and impact frames
   - Red energy aura intensifies
3. **Finisher (frames 141-180):** Final uppercut launches opponent with massive red explosion
   - Slow motion final impact
   - Screen shake
   - Camera follows opponent flying away

**Special Properties:**
- **Unblockable** if it connects (command grab)
- Can be jumped or avoided on reaction
- Deals full damage regardless of combo scaling
- Can only be used once per round
- Cinematic can be skipped after first viewing (hold button)
- Grants full invincibility during cinematic

**Animation Notes:**
- Explosive animation sequence
- 20 unique attack poses during rush
- Final uppercut is most dramatic
- Red energy emanates from Ryn's entire body
- Opponent has specific reaction animations for each hit

**Audio:**
- Voice: "THIS ENDS NOW!" (startup)
- SFX: Rapid fire punches (whoosh-thud-whoosh-thud)
- Voice: "STRIKER'S FURY!" (finisher)
- SFX: Massive explosion sound
- Music: Track intensifies during cinematic

---

## Combo Routes

### Basic Combo (BnB - Bread and Butter)
**Input Sequence:** LA1 → LA2 → MA1 → HA1
**Total Damage:** 30% health, 23% percentage
**Difficulty:** Beginner
**Hits:** 4
**Notes:**
- Works from max range jab
- MA1 launches, HA1 catches on descent
- Works at all percentages
- Confirms from safe poke

### Intermediate Combo #1
**Input Sequence:** LA1 → LA2 → MA1 → SP2 (Rising Fist)
**Total Damage:** 34% health, 26% percentage
**Difficulty:** Intermediate
**Hits:** 7 (2 lights + 1 medium + 3 SP2)
**Notes:**
- Better damage than basic combo
- Rising Fist must be timed as opponent reaches peak
- More style, ends with knockdown
- Good for building percentage quickly

### Intermediate Combo #2 (Corner)
**Input Sequence:** LA1 → LA2 → MA1 → HA1 (wall bounce) → Dash → MA1 → HA1
**Total Damage:** 50% health, 40% percentage
**Difficulty:** Intermediate
**Hits:** 6
**Notes:**
- Requires corner/wall position
- Wall bounce extends combo
- Highest damage without ultimate
- Requires dash timing after wall bounce

### Advanced Combo
**Input Sequence:** MA2 (whiff punish) → Dash cancel → LA1 → LA2 → MA1 → SP2 → Ultimate (as they fall)
**Total Damage:** 87% health, 85% percentage (likely KO)
**Difficulty:** Advanced
**Hits:** 12+
**Notes:**
- Requires perfect spacing for MA2 whiff punish
- Dash cancel timing is strict (2 frame window)
- Ultimate must connect during Rising Fist knockdown
- Maximum damage combo, will KO most characters above 50%
- Requires full ultimate meter

### Tier-Specific Combo (vs Tier 8+)
**Description:** Against heavier, slower opponents
**Input Sequence:** LA3 (sweep) → Dash → LA1 → LA2 → MA1 → SP1 (Rushing Charge) → HA1
**Total Damage:** 58% health, 47% percentage
**Notes:**
- Starts with risky low sweep
- Works better on heavier tiers (longer hitstun)
- Rushing Charge keeps them grounded for HA1 finisher
- Doesn't work on same-tier opponents (too fast recovery)

---

## Playstyle Guide

### Strengths
- **Fast normals:** Fastest jab in game (5f), wins scrambles
- **Good mobility:** Above-average dash and walk speed
- **Solid anti-air:** Rising Fist with full invincibility
- **Well-rounded:** No major weak points, all situations covered
- **Easy execution:** Clean, simple combos that work reliably
- **Strong pressure:** Plus frames on lights allow frame traps
- **Versatile:** Can play aggressive or defensive as needed

### Weaknesses
- **Low damage:** Tier 11 means each hit does less than higher tiers
- **Small hitboxes:** Shorter range than larger tier characters
- **No zoning:** No projectiles, must get in close
- **No air options:** Grounded fighter, weak to aerial approaches
- **Health disadvantage:** Takes more percentage damage from higher tiers
- **Lack of gimmicks:** Honest character, no tricks or setplay

### Gameplan

**Neutral Game:**
- **Primary tool:** LA1 (jab) - Use to control space and start pressure
- **Spacing:** Stay at jab range (1.5 units), just outside opponent's fastest attack
- **Movement:** Utilize dash speed to weave in and out of range
- **Anti-air:** React to jumps with MA1 or SP2 (Rising Fist)
- **Whiff punish:** Use MA2 (spinning backfist) to catch backdashes
- **Philosophy:** Patient but aggressive - wait for opening, then rush in with speed

**Offense:**
- **Pressure:** LA1 → LA1 (frame trap) or LA1 → throw mixup
- **Mixup:** Alternate between LA1 LA2 (mid) and LA3 (low)
- **Frame traps:** LA1 on block (+1) → LA1 again catches mash attempts
- **Throw game:** Use frequent throws to condition blocking
- **Combo confirms:** LA1 LA2 → confirm hit → MA1 for launch
- **Corner carry:** Use SP1 (Rushing Charge) to push toward corner
- **Oki (knockdown pressure):** After knockdown, time LA1 as they wake up

**Defense:**
- **Reversal:** SP2 (Rising Fist) for full invincibility - use sparingly (very punishable)
- **Backdash:** Quick 8f invincible backdash to escape pressure
- **Blocking:** Solid defense, look for gaps to punish
- **Anti-pressure:** Wait for opponent's minus frames, then LA1 to reclaim turn
- **Don't panic:** Ryn has tools but requires patient reads

**Tier Matchup Strategy:**

- **vs Tier 11 (Same Tier):**
  - Even matchup, pure skill-based
  - Speed is equal, focus on reads and spacing
  - Jab speed advantage can win neutral
  - Frame data knowledge crucial

- **vs Tier 10-9 (Slightly Higher):**
  - They hit harder but similar speed
  - Play patient, don't trade hits (you lose trades)
  - Use mobility advantage to avoid getting hit
  - Must outplay opponent with better fundamentals
  - Win through superior neutral and confirms

- **vs Tier 8-7 (Mid Tiers):**
  - Significant power difference, avoid trades at all costs
  - They're slower - use speed advantage
  - Bait whiffs, then punish with full combos
  - Run away and make them chase you
  - Use movement to frustrate them
  - Need 2-3 combos to equal one of their combos

- **vs Tier 6-5 (High Tiers):**
  - Massive disadvantage, requires perfect play
  - They have bigger hitboxes, better frame data, more damage
  - Must play very honest and patient
  - Look for mistakes, capitalize with ultimate
  - Use speed to hit-and-run
  - This is an uphill battle - embrace underdog status

- **vs Tier 4-0 (God Tiers):**
  - Nearly impossible matchup
  - They can probably kill in 1-2 touches
  - Speed advantage is only chance
  - Play to learn, not to win
  - Ultimate is your best tool (invincibility can steal rounds)
  - Moral victories count here

---

## Tier-Specific Properties

### Tier 11 Characteristics
- **Visual Scale:** Normal human proportions, 1.0x scale
- **VFX Intensity:** Light to moderate - red energy trails, white sparks on impact
- **Frame Data Philosophy:**
  - Fastest startup frames (5f jab vs 6-8f for higher tiers)
  - Shortest active frames (less linger on hitboxes)
  - Quickest recovery (can act sooner after attacks)
  - Smallest hitbox reach
  - Least damage per hit
  - Lowest knockback values
- **Power Fantasy:** "Speed and skill over raw power" - the technical fighter who must outplay opponents, not overpower them

### Balance Considerations
- Designed as the "baseline" character - all balance compares to Ryn
- Against other Tier 11s: Intended to be dead even, pure skill matchup
- Against higher tiers: Intentionally disadvantaged but not impossible
- Fast enough to rushdown, safe enough to play defensively
- Easy to learn, moderate skill ceiling
- Rewards fundamental fighting game skills: spacing, footsies, confirms, frame traps

---

## Art Asset Requirements

### Sprite Sheets Needed
1. **Idle Animation:** 6 frames at 12 FPS (breathing cycle)
2. **Walk Cycle:** 8 frames at 12 FPS
3. **Dash:** 6 frames (startup, movement, recovery)
4. **Backdash:** 6 frames (startup, invincible, recovery)
5. **Jump:** 8 frames (startup 2f, ascent 3f, peak 1f, fall 2f)
6. **LA1 (Jab):** 4 frames (startup, active, recovery, return)
7. **LA2 (Cross):** 5 frames
8. **LA3 (Sweep):** 7 frames (startup, active, recovery)
9. **MA1 (Body Blow):** 8 frames (windup, launch, peak, recovery)
10. **MA2 (Backfist):** 10 frames (windup, spin, impact, recovery)
11. **HA1 (Power Strike):** 12 frames (big windup, impact, follow-through)
12. **SP1 (Rushing Charge):** 10 frames (startup, dash sequence with smears, recovery)
13. **SP2 (Rising Fist):** 14 frames (startup, ascent with spins, peak, fall, landing)
14. **Ultimate:** 40 frames minimum (grab, rush sequence key frames, finisher)
    - Note: Many frames will be motion blur/smears
15. **Hit Reactions:**
    - Light hit: 3 frames
    - Heavy hit: 5 frames
    - Launched: 4 frames
    - Spinning knockdown: 8 frames
16. **Block:** 2 frames (stand, crouch)
17. **Throws:** 8 frames (throw startup, opponent grab, throw animation)
18. **Being Thrown:** 6 frames
19. **Victory:** 10 frames (victorious pose, maybe flex)
20. **Defeat:** 8 frames (collapse/kneel)

**Total Estimated Frames:** ~180-200 frames
**Art Style Notes:**
- Athletic, dynamic poses
- Red and white color scheme with gray/black base
- Anime-influenced but grounded (no wild hair or exaggerated proportions)
- Clear silhouette for gameplay readability
- Hand-drawn style similar to Guilty Gear but more realistic anatomy (MK influence)

---

### VFX Assets Needed
1. **Hit Sparks:** Red and white spark burst (3 variations: light, medium, heavy)
2. **Attack Trails:**
   - Light attacks: Thin red lines
   - Medium attacks: Thicker red trails with white outline
   - Heavy attacks: Wide red trails with white energy sparks
3. **Special Move Effects:**
   - Rushing Charge: Red speed lines, body blur effect
   - Rising Fist: Red spiral trailing upward, white sparks
4. **Ultimate Effect:**
   - Massive red explosion on grab
   - Speed lines during rush
   - White and red energy aura around Ryn
   - Final explosion with screen flash
5. **Movement Effects:**
   - Dash: Red trails behind feet
   - Jump: Small dust clouds on takeoff and landing

---

## Audio Asset Requirements

### Voice Clips
1. **Attack Grunts:** "Hah!" "Yah!" "Tah!" (3 variations)
2. **Special Moves:**
   - Rushing Charge: "Go!"
   - Rising Fist: "Rising!"
3. **Ultimate:**
   - Startup: "This ends now!"
   - Finisher: "Striker's Fury!"
4. **Victory:** "That's how it's done."
5. **Defeat:** Grunt/exhale sound

### Sound Effects
1. **Light Attacks:** Quick "whoosh" sounds (3 variations)
2. **Medium Attacks:** Deeper "whoosh" with impact "thud"
3. **Heavy Attack:** Very deep "whoosh" + heavy "CRACK" impact
4. **Rushing Charge:** Wind rushing sound + rapid impacts
5. **Rising Fist:** Explosive upward "WOOSH" + powerful impact
6. **Ultimate:**
   - Grab: Energy burst sound
   - Rush: Rapid fire punches with impacts
   - Finisher: Massive explosion
7. **Movement:**
   - Footsteps (subtle)
   - Dash "whoosh"
   - Jump takeoff/landing
8. **Hit Reactions:** Various impact sounds based on attack strength

---

## Implementation Notes

### Godot Scene Structure
```
Ryn.tscn (root: CharacterBody2D)
├── AnimationPlayer (controls all animations)
├── AnimationTree (state machine for animation blending)
├── Sprite2D (character sprite)
├── StateMachine (GDScript - gameplay states)
│   ├── Idle
│   ├── Walk
│   ├── Dash
│   ├── Jump
│   ├── Attack_LA1
│   ├── Attack_LA2
│   ├── Attack_LA3
│   ├── Attack_MA1
│   ├── Attack_MA2
│   ├── Attack_HA1
│   ├── Special_RushingCharge
│   ├── Special_RisingFist
│   ├── Ultimate
│   ├── Hitstun
│   ├── Blockstun
│   └── Knockdown
├── HitboxManager (GDScript)
│   ├── Hitbox (Area2D - dynamically created per attack)
│   └── Hurtbox (Area2D - always active, body collision)
├── HealthSystem (GDScript)
│   ├── percentage_damage: float
│   └── health_bar: float
├── InputBuffer (GDScript - stores inputs for motion commands)
└── AudioStreamPlayer2D (for SFX)
```

### JSON Data File Location
- Character stats: `res://data/characters/ryn.json`
- Move data: `res://data/moves/ryn_moves.json`

### Key Scripts
1. `ryn_character.gd` - Main character controller
2. `ryn_state_machine.gd` - State machine logic
3. `ryn_moves.gd` - Move definitions and frame data

### Testing Checklist
- [ ] All animations play at correct speed
- [ ] Frame data matches specification exactly
- [ ] Hitboxes appear on correct frames
- [ ] LA1 → LA2 → MA1 → HA1 combo connects consistently
- [ ] Rising Fist has invincibility frames 1-8
- [ ] Ultimate can be jumped/avoided on reaction
- [ ] Maintains 60 FPS with all VFX active
- [ ] Balanced against second Tier 11 character (once created)
- [ ] Sound effects synchronized with animations
- [ ] Tier modifiers apply correctly (1.0x across the board)

---

## Balance Version History

### v1.0 (Initial Design)
- Created as baseline Tier 11 character
- Designed to be beginner-friendly but competitive
- All frame data based on Guilty Gear/Street Fighter standards
- 5f jab to compete with other fast characters
- Rising Fist invincibility as "get off me" tool
- Ultimate designed to be reactable but threatening

**Design Philosophy:**
- Simple to understand, hard to master
- Rewards fundamental fighting game skills
- No gimmicks or unusual mechanics
- "Ryu/Ky" archetype - the all-rounder everyone should learn first

---

## Notes & Ideas

**Character Background (Optional Lore):**
- Street fighter from unknown city
- Trained in multiple martial arts (MMA style)
- Enters tournament to test skills against supernatural beings
- Doesn't care about power scaling - just wants good fights
- Respects strength regardless of tier
- Secretly admires higher-tier fighters
- "Even humans can stand with gods if they fight smart"

**Potential Alternate Costumes:**
- Training gear (tank top, sweatpants)
- Formal gi (traditional karate outfit)
- Street clothes (hoodie, jeans)
- Battle-damaged (torn gi, bruises)

**Easter Eggs:**
- If both players pick Ryn: Special mirror match intro ("Let's see who's the real striker!")
- Ultimate finish quote changes based on opponent tier
- Victory animation against Tier 0: "I actually won?!" (shock expression)

**Future Balance Considerations:**
- If too weak: Reduce recovery on LA1 from 8f to 7f
- If too strong: Reduce invincibility on Rising Fist from frames 1-8 to frames 3-8
- Ultimate can be tuned by adjusting grab range

---

**Character Status:** ✅ READY FOR IMPLEMENTATION
**Recommended as:** First character to prototype (simple, well-rounded, beginner-friendly)
**Artist Brief Prepared:** Yes (see Visual Design section)
**Estimated Development Time:** 3-4 weeks (with outsourced art)

---

**Template Version:** 1.0
**Character Version:** 1.0
**Last Updated:** 2025-10-24
**Designer:** [Your Name]
