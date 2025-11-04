# Character Specification: Kira

**Character Name:** Kira "The Spellblade"
**Tier:** 11 (Peak Human + Minor Magical Enhancement)
**Archetype:** Zoner / Keepaway
**Difficulty:** Intermediate

---

## Character Overview

### Visual Design
**Appearance:** Athletic human female in her early 20s with a lean, agile build. Wears light tactical armor (chest piece, arm guards, leg guards) in dark purple and silver. Long silver-white hair tied in high ponytail. Carries ornate energy-channeling gauntlets on both arms. Height: 5'7" (170cm). Lithe dancer-like physique.

**Personality/Theme:** Tactical fighter who uses magical energy channeling through technology. Calm, calculated, prefers to control space rather than brawl. Former military who discovered minor magical affinity. Represents the "zoner/keepaway" archetype - keeps opponents at bay with projectiles and traps.

**Power Level Justification:** Tier 11 because her magical abilities are technologically augmented and limited to energy projection. Without her gauntlets, she's peak human with combat training. The magic is minimal - energy blasts, not reality warping. Smart tactical fighter who fights at range.

**Color Palette:**
- Primary: Dark purple (armor, clothing)
- Secondary: Silver (armor accents, gauntlets)
- Accent: White (hair, trim)
- VFX: Purple/violet energy with white electricity

---

## Base Statistics

### Core Stats
- **Health:** 95 (slightly lower - keepaway glass cannon)
- **Weight:** Light (easier to knock back, but less hitstun)
- **Walk Speed:** 4 (slower than Ryn - intentional weakness)
- **Dash Speed:** 6 (decent mobility)
- **Jump Height:** 7 (high jumper - aerial game)
- **Air Control:** 8 (excellent air control - stays away)

### Tier Modifiers (Tier 11)
- **Hitbox Size Multiplier:** 1.0 (human-sized, same as all Tier 11)
- **Knockback Modifier:** 1.0 (deals standard knockback)
- **Damage Scaling:** 1.0 (standard damage)
- **Frame Data Modifier:** Tier 11 standard - fast startup, but projectiles add unique frame data considerations (recovery+travel time)

---

## Movement Abilities

### Ground Movement
- **Walk:** Forward/backward movement
  - Speed: 4.0 units/second (intentionally slower)
  - Can be canceled into: Any attack, dash, jump, block

- **Dash:** Quick forward dash with purple after-image
  - Duration: 20 frames (slightly longer than Ryn)
  - Distance: 2.8 units
  - Recovery: 10 frames
  - Can be canceled into: Attacks (frame 12+), jump (frame 6+)

- **Backdash:** Long-range evasive retreat
  - Duration: 26 frames (slower but farther)
  - Invincibility frames: 1-10 (longer invincibility)
  - Recovery: 12 frames
  - Distance: 3.5 units (longest backdash in Tier 11)

### Aerial Movement
- **Jump:** High, floaty jump
  - Startup: 5 frames
  - Peak height: 6.0 units (higher than Ryn)
  - Total air time: 60 frames (floatier)
  - Fall speed: Slower (keepaway air game)
  - Air jumps: 1 (double jump capable)

- **Air Dash:** Yes (horizontal)
  - Duration: 16 frames
  - Distance: 3.0 units
  - Uses per jump: 1
  - Can attack during air dash

---

## Universal Mechanics

### Blocking
- **Stand Block:** Blocks mid and high attacks
- **Crouch Block:** Blocks mid and low attacks
- **Air Block:** Allowed (defensive option in air)
- **Pushback:** 0.4 units (pushed back more - keepaway design)

### Throws
- **Forward Throw:**
  - Startup: 6 frames (1f slower than Ryn)
  - Range: 1.1 units (slightly shorter)
  - Damage: 7% health, 10% percentage (less damage)
  - Knockback: Pushes opponent away 3.0 units (creates space)

- **Back Throw:**
  - Startup: 6 frames
  - Range: 1.1 units
  - Damage: 7% health, 10% percentage
  - Knockback: Sends opponent 3.5 units away (maximum spacing)

**Note:** Kira's throws are designed to create distance, not damage

---

## Move List

### Light Attacks

#### Light Attack 1 (LA1) - Quick Palm
**Input:** Light button (standing)
**Move Type:** Standing normal
**Archetype Role:** Defensive poke / Create space

**Frame Data:**
- Startup: 6 frames (1f slower than Ryn's jab)
- Active: 3 frames
- Recovery: 10 frames
- On Hit: +3 frames
- On Block: -1 frame (slightly minus, unsafe to continue)
- **Total Duration:** 19 frames

**Properties:**
- Damage (Health): 3
- Damage (Percentage): 2%
- Knockback: Medium (1.0 unit - pushes away)
- Knockback Angle: 45° (pushes back and slightly up)
- Hitstun: 14 frames
- Blockstun: 11 frames
- Range: 1.4 units (shorter than Ryn's jab)
- Hitbox: Small (0.4 unit radius)

**Cancel Options:**
- Can cancel into: Specials only (not other normals)
- Cancel window: Frames 8-19

**Special Properties:**
- Pushes opponent away on hit (creates zoning space)
- Main defensive tool in close range
- Cannot chain into other lights (keepaway design)

**Animation Notes:**
- Quick palm strike with energy flicker
- Small purple spark on contact
- Minimal commitment

**Audio:**
- SFX: Soft "whoosh" + electric "zap"

---

#### Light Attack 2 (LA2) - Energy Swipe (Crouching)
**Input:** Down + Light button
**Move Type:** Crouching normal
**Archetype Role:** Low poke / Spacing tool

**Frame Data:**
- Startup: 7 frames
- Active: 4 frames
- Recovery: 12 frames
- On Hit: +2 frames
- On Block: -3 frames
- **Total Duration:** 23 frames

**Properties:**
- Damage (Health): 4
- Damage (Percentage): 3%
- Knockback: Minimal (0.5 units)
- Knockback Angle: 30° (low)
- Hitstun: 15 frames
- Blockstun: 12 frames
- Range: 2.0 units (good range for low)
- Hitbox: Wide, low (1.8 x 0.4 units)

**Cancel Options:**
- Can cancel into: Specials
- Cancel window: Frames 10-23

**Special Properties:**
- Hits LOW - must block crouching
- Good range for Tier 11
- Safe-ish spacing tool

**Animation Notes:**
- Crouches and sweeps arm with purple energy trail
- Energy extends reach

**Audio:**
- SFX: "Swish" with energy hum

---

#### Light Attack 3 (LA3) - Aerial Energy Jab
**Input:** Light button (airborne)
**Move Type:** Jumping normal
**Archetype Role:** Air-to-air / Aerial approach

**Frame Data:**
- Startup: 7 frames
- Active: 5 frames
- Recovery: 10 frames (until landing)
- On Hit: Varies (depends on air hit)
- On Block: -4 frames (if blocked in air)
- **Total Duration:** 22 frames

**Properties:**
- Damage (Health): 4
- Damage (Percentage): 3%
- Knockback: Light (1.5 units)
- Knockback Angle: 60°
- Hitstun: 18 frames
- Range: 1.6 units
- Hitbox: Medium (0.6 radius), extends forward and down

**Cancel Options:**
- Can cancel into: Air specials
- Cancel window: Frames 10-22

**Special Properties:**
- Decent air-to-air tool
- Can combo into itself with air dash
- Stays out briefly (good for air control)

**Animation Notes:**
- Extends hand forward with energy pulse
- Purple flash

**Audio:**
- SFX: "Zap" sound

---

### Medium Attacks

#### Medium Attack 1 (MA1) - Energy Burst
**Input:** Medium button (standing)
**Move Type:** Standing normal
**Archetype Role:** Mid-range poke / Knockback

**Frame Data:**
- Startup: 10 frames
- Active: 5 frames
- Recovery: 18 frames
- On Hit: +5 frames
- On Block: -5 frames
- **Total Duration:** 33 frames

**Properties:**
- Damage (Health): 7
- Damage (Percentage): 5%
- Knockback: High (2.5 units - strong pushback)
- Knockback Angle: 40°
- Hitstun: 22 frames
- Blockstun: 16 frames
- Range: 2.5 units (excellent range)
- Hitbox: Large (1.0 radius), energy projectile-like

**Cancel Options:**
- Can cancel into: Specials, ultimate
- Cancel window: Frames 14-33

**Special Properties:**
- Excellent spacing tool
- Strong pushback on hit creates space
- Good range for Tier 11
- Can hit at tip for maximum safety

**Animation Notes:**
- Extends both hands, releases energy burst
- Purple explosion effect
- Recoil animation

**Audio:**
- SFX: "WHOMP" energy explosion

---

### Heavy Attacks

#### Heavy Attack 1 (HA1) - Charged Cannon
**Input:** Heavy button (standing, can be charged)
**Move Type:** Chargeable projectile
**Archetype Role:** Zoning tool / Space control

**Frame Data (Uncharged):**
- Startup: 16 frames
- Active: N/A (projectile)
- Recovery: 30 frames (long recovery)
- Projectile Travel Time: 45 frames to cross screen
- Total commitment: 46 frames until can act again

**Frame Data (Fully Charged - hold 60 frames):**
- Startup: 16 frames (after charge)
- Recovery: 35 frames
- Projectile Travel Time: 35 frames (faster)

**Properties (Uncharged):**
- Damage (Health): 8
- Damage (Percentage): 6%
- Knockback: Light (allows follow-up)
- Projectile Speed: Slow-Medium
- Projectile Durability: 1 hit (can be destroyed by attacks)
- Range: Fullscreen

**Properties (Fully Charged):**
- Damage (Health): 15
- Damage (Percentage): 12%
- Knockback: High (3.0 units)
- Projectile Speed: Fast
- Projectile Durability: 2 hits (stronger)
- Range: Fullscreen

**Cancel Options:**
- Can cancel charge into: Block, backdash (but loses charge)
- Cannot cancel recovery

**Special Properties:**
- **Core zoning tool**
- Charge by holding button (visible charging animation)
- Can release early for uncharged version
- Charged version has purple electricity effect
- Forces opponent to approach or jump

**Animation Notes:**
- Gauntlets glow with increasing intensity while charging
- Releases large purple energy sphere
- Heavy recoil on release

**Audio:**
- Charge: Humming sound increasing in pitch
- Release: "BOOM" energy cannon

---

### Special Moves

#### Special Move 1 (SP1) - Energy Trap
**Input:** Quarter-circle forward + Special (236+S)
**Move Type:** Trap / Setup projectile
**Archetype Role:** Space control / Zoning setup

**Frame Data:**
- Startup: 18 frames
- Active: N/A (trap placement)
- Recovery: 24 frames
- Trap Duration: 300 frames (5 seconds) if not triggered
- Trap Hit: 8 frame startup when triggered

**Properties:**
- Damage (Health): 6
- Damage (Percentage): 5%
- Knockback: Medium (1.8 units upward)
- Knockback Angle: 80° (launches up)
- Placement Range: 2.5 units in front of Kira
- Trigger Range: 1.5 unit radius around trap
- Max Traps: 1 at a time (placing new one destroys old)

**Special Properties:**
- **Places energy mine on ground**
- Trap is visible (purple glowing orb on ground)
- Explodes when opponent walks/dashes near it
- Can be destroyed by attacks (1 hit)
- Forces opponent to navigate around it
- Kira can move immediately after recovery
- **Does not trigger on Kira** (only opponent)

**Animation Notes:**
- Kira channels energy into ground
- Purple orb appears and hovers slightly
- Pulsing animation while active
- Explodes in purple burst when triggered

**Audio:**
- Placement: "Whirr" charging sound
- Active: Subtle pulsing hum
- Trigger: "BOOM" explosion

---

#### Special Move 2 (SP2) - Warp Step
**Input:** Dragon punch motion + Special (623+S)
**Move Type:** Teleport / Defensive escape
**Archetype Role:** Escape tool / Reset to neutral

**Frame Data:**
- Startup: 8 frames (fast escape)
- Teleport Duration: 12 frames (invincible)
- Recovery: 20 frames (at destination)
- Total: 40 frames

**Properties:**
- Damage: 0 (movement only)
- Invincibility: Frames 8-20 (during vanish and reappear)
- Teleport Distance: 5.0 units backward OR 4.0 units forward (direction dependent on input)
  - Backward: Hold back during input
  - Forward: Hold forward during input
  - Neutral: Goes backward by default

**Special Properties:**
- **Full invincibility during teleport**
- Cannot be thrown or hit during frames 8-20
- Creates distance vs pressure
- Vulnerable during recovery at destination (20 frames)
- Cannot attack immediately after
- Has startup, so not instant (can be hit before frame 8)

**Animation Notes:**
- Kira dissolves into purple particles
- Particles stream to destination
- Rematerializes with purple flash
- Slight crouch on arrival (recovery animation)

**Audio:**
- Vanish: "Fwoosh" warp-out sound
- Reappear: "Pop" warp-in sound

---

#### Special Move 3 (SP3) - Rising Launcher (Anti-air)
**Input:** Down, down + Special (22+S)
**Move Type:** Anti-air / Launcher
**Archetype Role:** Defensive anti-air

**Frame Data:**
- Startup: 9 frames
- Active: 6 frames
- Recovery: 26 frames
- On Hit: Launch state
- On Block: -18 frames (very unsafe)

**Properties:**
- Damage (Health): 10
- Damage (Percentage): 8%
- Knockback: Very high vertical (5.0 units, 85° angle)
- Invincibility: None (not a reversal)
- Range: 1.8 units (good anti-air range)
- Hitbox: Above and in front of character

**Special Properties:**
- Strong anti-air tool
- Launches opponent very high
- Can follow up with air dash → aerial
- Good reward on hit
- Very punishable on block (keepaway design - shouldn't be in pressure)

**Animation Notes:**
- Kira thrusts both hands upward
- Large purple energy pillar erupts
- Lifts opponent into air

**Audio:**
- SFX: "RISING!" with energy surge sound

---

### Ultimate Attack (ULTRA) - Orbital Strike

**Input:** Ultimate button (when available)
**Activation Condition:** Can be used at any time
**Move Type:** Fullscreen projectile super / Cinematic
**Archetype Role:** Ultimate zoning tool / Punish

**Frame Data:**
- Startup: 12 frames (fairly fast)
- Active: N/A (projectile super)
- Recovery: 60 frames (very long - committed)
- Beam Duration: 120 frames (2 seconds)
- Total Duration: 192 frames

**Properties:**
- Damage (Health): 40 (if all hits connect)
- Damage (Percentage): 45%
- Hits: Multi-hit (15+ hits during beam)
- Knockback: Final hit launches (6.0 units, 70° angle)
- Range: Fullscreen vertical beam
- Width: 3.0 units (wide beam)
- Invincibility: Frames 1-12 (startup only)

**Cinematic Elements:**
1. **Startup (frames 1-30):** Kira channels energy upward, camera zooms slightly, screen darkens
2. **Targeting (frames 31-60):** Reticle appears on opponent, tracks for 30 frames
3. **Strike (frames 61-180):** Massive purple energy beam descends from sky onto target location
   - Beam persists for 2 seconds
   - Multi-hit during beam
   - Particles and screen shake
4. **Recovery (frames 181-192):** Kira lowers arms, catches breath

**Special Properties:**
- **Tracks opponent position** during targeting phase (frames 31-60)
- Beam descends at locked position after tracking ends
- Can be dodged by dashing out of beam width during tracking
- If opponent is hit, they're trapped for full duration
- Blockable (must block entire duration or get chipped)
- **Very punishable on whiff** (60 frame recovery)

**Animation Notes:**
- Kira raises both arms to sky
- Gauntlets glow intensely
- Purple beam descends from above
- Massive explosion on final hit
- Kira exhausted after (heavy breathing)

**Audio:**
- Voice: "Rain down!" (startup)
- SFX: Energy charging (crescendo)
- Voice: "Orbital Strike!" (beam descent)
- SFX: Massive beam sound + explosions
- Music: Track peaks during beam

---

## Combo Routes

### Basic Combo (BnB)
**Input Sequence:** MA1 → HA1 (uncharged projectile)
**Total Damage:** 15% health, 11% percentage
**Difficulty:** Beginner
**Hits:** 2
**Notes:**
- Simple hit-confirm into projectile
- Creates space on hit
- Safe sequence
- Forces opponent to approach again

### Intermediate Combo (Space Control)
**Input Sequence:** SP1 (place trap) → HA1 (charge cannon) → Trap triggers → Dash forward → MA1
**Total Damage:** 21% health, 16% percentage
**Difficulty:** Intermediate
**Hits:** 3
**Notes:**
- Setup combo utilizing trap
- Requires opponent to trigger trap
- Forces movement into cannon
- Rewards reads

### Advanced Combo (Maximum Damage)
**Input Sequence:** SP3 (anti-air launch) → Air Dash → LA3 → LA3 → Ultimate (during fall)
**Total Damage:** 58% health, 58% percentage
**Difficulty:** Advanced
**Hits:** 18+ (including ultimate multi-hits)
**Notes:**
- Requires successful anti-air
- Air dash must be timed perfectly
- Ultimate must connect as they fall
- High execution but massive damage

### Tier-Specific Combo (vs Rushdown)
**Description:** Anti-pressure sequence
**Input Sequence:** SP2 (warp back) → HA1 (charged) → SP1 (trap) → Backdash → HA1 (uncharged)
**Total Damage:** 23% health, 18% percentage
**Notes:**
- Escapes pressure with warp
- Immediately reestablishes zone
- Multiple layers of defense
- Keeps opponent at bay

---

## Playstyle Guide

### Strengths
- **Excellent zoning:** Best projectile game in Tier 11
- **Space control:** Traps force opponent movement
- **High mobility:** Double jump + air dash = aerial control
- **Safe spacing:** Long-range normals keep distance
- **Defensive options:** Warp escape and long backdash
- **Air game:** Strong aerial tools with air block
- **Fullscreen threat:** Ultimate can punish anywhere

### Weaknesses
- **Low health:** 95 HP (5 less than average)
- **Slow walk speed:** Worst ground mobility
- **Weak up-close:** 6f jab loses to 5f jabs
- **Long recoveries:** Committed to actions
- **Light weight:** Takes more knockback
- **No invincible reversal:** SP2 has startup
- **Execution dependent:** Requires good spacing

### Gameplan

**Neutral Game:**
- **Primary tool:** HA1 (projectile) - Forces approach
- **Spacing:** Stay at max range (3+ units away)
- **Movement:** Use backdash and air mobility to maintain distance
- **Trap placement:** Use SP1 to control ground
- **Anti-air:** SP3 or MA1 depending on angle
- **Philosophy:** "You can't hit what you can't catch" - control space, never brawl

**Offense:**
- **Pressure:** Kira doesn't pressure - she zones
- **Mix up:** Fake projectile → dash throw is rare aggressive option
- **Conditioning:** Make them block projectiles, then throw
- **Corner carry:** Push opponent to corner with projectiles
- **Trap setups:** Place trap, force movement into it
- **Air approach:** Air dash → LA3 if opponent overcommits to ground

**Defense:**
- **Primary defense:** Stay away (backdash, air dash back)
- **Reversal:** SP2 (warp) to escape - requires read (has startup)
- **Anti-air:** SP3 is dedicated anti-air tool
- **Under pressure:** Block and look for gap to warp out
- **Don't panic:** Patient blocking, then escape when safe

**Tier Matchup Strategy:**

- **vs Tier 11 (Same Tier):**
  - Even matchup but playstyle-dependent
  - vs Ryn: Zoner vs rushdown (classic matchup)
  - Keep distance, make them chase
  - Punish approaches with anti-airs
  - Win through zoning and patience

- **vs Tier 10-9 (Slightly Higher):**
  - They hit harder, still manageable
  - Use mobility advantage (air dash, warp)
  - Zone harder - don't let them touch you
  - One mistake can lose round (they hit harder)
  - Play even more patient

- **vs Tier 8-7 (Mid Tiers):**
  - Significant power gap
  - Must play perfect keepaway
  - Use every tool to maintain distance
  - One combo from them = three combos from you
  - Traps and projectiles are lifeline
  - Ultimate is best damage equalizer

- **vs Tier 6-5 (High Tiers):**
  - Extremely difficult
  - They likely have tools to counter zoning
  - Play to not get hit (easier said than done)
  - Mobility is only advantage
  - Warp and air dash to survive
  - Win through chip and patience

- **vs Tier 4-0 (God Tiers):**
  - Nearly unwinnable
  - They probably have fullscreen tools too
  - Stay alive as long as possible
  - Ultimate might steal a round if lucky
  - Consider it training mode

---

## Tier-Specific Properties

### Tier 11 Characteristics
- **Visual Scale:** Normal human proportions, 1.0x scale
- **VFX Intensity:** Moderate - purple energy effects, electrical sparks
- **Frame Data Philosophy:**
  - Standard Tier 11 startup speeds
  - Longer recoveries due to projectile/trap mechanics
  - Good active frames on projectiles
  - Compensates with range and space control
- **Power Fantasy:** "Control the battlefield" - strategic zoner who dictates pace through intelligent placement

### Balance Considerations
- Designed as counter-archetype to Ryn (rushdown vs zoning)
- Against Ryn: Skill matchup (5-5) but playstyle clash makes it dynamic
- Against other rushdown: Slight advantage (6-4) if played well
- Against other zoners: Even (5-5), spacing battle
- Lower health (95) compensates for strong keepaway tools
- Higher execution required than Ryn (intermediate difficulty)

---

## Art Asset Requirements

### Sprite Sheets Needed
1. **Idle Animation:** 8 frames at 12 FPS (gauntlets pulse with energy)
2. **Walk Cycle:** 8 frames at 12 FPS (cautious, measured steps)
3. **Dash:** 6 frames (purple after-image trail)
4. **Backdash:** 8 frames (longer animation, invincible frames clear)
5. **Jump:** 10 frames (high arc, floaty)
6. **Air Dash:** 6 frames (horizontal dash with purple trail)
7. **LA1 (Palm):** 5 frames
8. **LA2 (Swipe):** 6 frames
9. **LA3 (Air Jab):** 5 frames
10. **MA1 (Energy Burst):** 9 frames
11. **HA1 (Cannon):** 16 frames (charge poses + release)
12. **SP1 (Trap):** 10 frames (placement animation + trap sprite)
13. **SP2 (Warp):** 12 frames (dissolve + rematerialize)
14. **SP3 (Rising Launcher):** 10 frames
15. **Ultimate:** 50 frames (startup, targeting, casting, recovery)
    - Separate beam sprite asset
16. **Hit Reactions:** 12 frames (light, heavy, launched, air hit)
17. **Block:** 2 frames (stand, crouch)
18. **Air Block:** 2 frames
19. **Throws:** 8 frames
20. **Victory:** 12 frames (poses triumphantly with gauntlets glowing)
21. **Defeat:** 8 frames (kneels, exhausted)

**Additional Assets:**
- Energy Trap sprite (pulsing orb, explosion)
- Energy Cannon projectile sprite
- Orbital Strike beam (large vertical beam)

**Total Estimated Frames:** ~220-240 frames
**Art Style Notes:**
- Sleek, tactical aesthetic
- Purple and silver color scheme
- Energy effects should look technological (not purely magical)
- Gauntlets are key visual focus
- Lithe, agile poses (dancer-like)
- Guilty Gear influence: stylized anime with detailed shading
- MK influence: Tactical gear, realistic anatomy

---

### VFX Assets Needed
1. **Hit Sparks:** Purple electric sparks (3 variations)
2. **Attack Trails:**
   - Light: Thin purple lines with white sparks
   - Medium: Thicker purple energy burst
   - Heavy: Large purple explosion with electricity
3. **Special Move Effects:**
   - Energy Trap: Pulsing purple orb, explosion on trigger
   - Warp Step: Particle dissolve/rematerialize effect
   - Rising Launcher: Vertical purple energy pillar
   - Charged Cannon: Growing energy sphere, projectile trail
4. **Ultimate Effect:**
   - Targeting reticle (purple, high-tech)
   - Massive purple beam from sky
   - Ground explosion effects
   - Screen flash on impact
5. **Movement Effects:**
   - Air dash: Purple speed trail
   - Double jump: Purple burst
   - Gauntlets: Constant subtle purple glow

---

## Audio Asset Requirements

### Voice Clips
1. **Attack Grunts:** "Hah!" "Hmph!" (2 variations, calm tone)
2. **Special Moves:**
   - Energy Trap: "Set!"
   - Warp Step: (No voice, just sound)
   - Rising Launcher: "Rise!"
   - Charged Cannon: "Charging..." (whisper during charge)
3. **Ultimate:**
   - Startup: "Rain down!"
   - Beam: "Orbital Strike!"
4. **Victory:** "Calculated."
5. **Defeat:** Exhale/gasp sound

### Sound Effects
1. **Light Attacks:** Soft "whoosh" + "zap" (electric)
2. **Medium Attacks:** Energy burst "WHOMP"
3. **Heavy Attack (Cannon):**
   - Charge: Humming escalation
   - Release: "BOOM" energy cannon
4. **Energy Trap:**
   - Placement: "Whirr" charge
   - Active: Pulsing hum
   - Trigger: "BOOM" explosion
5. **Warp Step:**
   - Vanish: "Fwoosh" warp-out
   - Reappear: "Pop" warp-in
6. **Rising Launcher:** Energy surge "WHOOSH"
7. **Ultimate:**
   - Charge: Crescendo build-up
   - Beam: Massive sustained energy sound
   - Impacts: Multiple explosions
8. **Movement:**
   - Footsteps (light, tactical)
   - Air dash whoosh
   - Jump/land (soft)

---

## Implementation Notes

### Godot Scene Structure
```
Kira.tscn (root: CharacterBody2D)
├── AnimationPlayer
├── AnimationTree
├── Sprite2D (character sprite)
├── StateMachine
│   ├── [Standard states like Ryn]
│   ├── Special_EnergyTrap
│   ├── Special_WarpStep
│   ├── Special_RisingLauncher
│   └── Ultimate_OrbitalStrike
├── HitboxManager
│   ├── Hitbox (Area2D)
│   └── Hurtbox (Area2D)
├── ProjectileManager (GDScript - handles projectiles)
│   ├── Cannon projectile scene instance
│   └── Trap scene instance
├── HealthSystem (95 max HP)
├── InputBuffer
└── AudioStreamPlayer2D
```

**Additional Scenes:**
- `energy_trap.tscn` (separate scene for trap object)
- `energy_cannon_projectile.tscn` (projectile scene)
- `orbital_strike_beam.tscn` (ultimate beam effect)

### JSON Data File Location
- Character stats: `res://data/characters/kira.json`
- Move data: `res://data/moves/kira_moves.json`
- Projectile data: `res://data/projectiles/kira_projectiles.json`

### Testing Checklist
- [ ] Projectile travels fullscreen correctly
- [ ] Energy trap places at correct distance
- [ ] Trap triggers only on opponent, not Kira
- [ ] Warp Step has invincibility frames 8-20
- [ ] Air dash → LA3 combos consistently
- [ ] Ultimate tracks opponent during targeting phase
- [ ] Ultimate can be dodged by dashing out
- [ ] Charged cannon charges and releases properly
- [ ] All VFX sync with animations
- [ ] Maintains 60 FPS with projectiles + traps active
- [ ] Balanced against Ryn (should be ~50/50 skill matchup)

---

## Balance Version History

### v1.0 (Initial Design)
- Created as zoner archetype counterpoint to Ryn
- Lower health (95) to compensate for strong keepaway
- Slower walk speed but better air mobility
- Projectile + trap design for space control
- Warp escape vs invincible reversal (different defensive tools)

**Design Philosophy:**
- Intermediate difficulty (requires spacing and reads)
- Rewards patient, tactical play
- Punishes aggressive, reckless opponents
- Makes Ryn players learn to approach (matchup teaching tool)
- "Keepaway" doesn't mean "cowardly" - requires skill and reads

---

## Notes & Ideas

**Character Background (Optional Lore):**
- Former special forces operative
- Discovered minor magical affinity during combat
- Developed tech to amplify and channel it (gauntlets)
- Believes technology + magic = future of combat
- Tactical mindset: "Every battle is won before it starts"
- Respects opponents who adapt and overcome zoning

**Potential Matchup Dynamics:**
- vs Ryn: Classic rushdown vs zoner (training matchup)
- vs Aerial characters: Good (strong anti-airs)
- vs Other zoners: Trap gives her unique advantage
- vs Grapplers: Excellent (they can't catch her)

**Alternate Costumes:**
- Military fatigues (tactical gear)
- Civilian clothes (casual, gauntlets remain)
- High-tech armor (full body suit)
- Damaged/battle-worn (cracked gauntlets, torn gear)

**Easter Eggs:**
- vs Ryn: Special intro ("Let's see you get past my defenses.")
- Ultimate vs airborne opponent: Beam tracks upward
- Low health: Gauntlets flicker (visual indicator)

**Future Balance Notes:**
- If too weak: Reduce projectile recovery from 30f to 25f
- If too strong: Increase warp startup from 8f to 12f (more reactable)
- Trap duration could be tuned (currently 5 seconds)
- Ultimate tracking duration could be reduced if too strong

---

**Character Status:** ✅ READY FOR IMPLEMENTATION
**Recommended as:** Second character (contrasts with Ryn, teaches spacing)
**Artist Brief Prepared:** Yes (see Visual Design section)
**Estimated Development Time:** 4-5 weeks (additional projectile systems needed)
**Implementation Note:** Should be developed after Ryn to contrast archetypes

---

**Template Version:** 1.0
**Character Version:** 1.0
**Last Updated:** 2025-10-24
**Designer:** [Your Name]
