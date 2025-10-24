# Godot 2D Solo Dev: Technical Pivot Analysis

**Document Version:** 1.0
**Date:** 2025-10-24
**Status:** Technical Architecture Revision

---

## Executive Summary

**Project Scope Changes:**
- **Developer:** 8-person team → **Solo developer**
- **Engine:** Unreal Engine 5 → **Godot 4.x**
- **Rendering:** 3D → **Stylized 2D**
- **Art Style:** Guilty Gear + Mortal Kombat blend
- **Demo Scope:** 6 characters (2 low-tier, 2 mid-tier, 2 unlockable high-tier)
- **Platform:** PC-only (Windows 11)
- **Goal:** Portfolio project

**Key Verdict:** ✅ **This pivot SIGNIFICANTLY IMPROVES feasibility for solo development**

---

## Part 1: Why This Pivot Makes Sense

### Advantages of Godot 2D for Solo Fighting Game

#### 1. **Engine Complexity**
**UE5:**
- ❌ Heavyweight (40GB+ install)
- ❌ Steep learning curve
- ❌ Overkill for 2D
- ❌ Slower iteration time
- ❌ Requires C++ for performance-critical code

**Godot 4:**
- ✅ Lightweight (150MB install)
- ✅ Gentle learning curve
- ✅ Built for 2D
- ✅ Fast iteration
- ✅ GDScript is simple and fast to write
- ✅ Excellent 2D physics out-of-the-box
- ✅ Deterministic by default (crucial for fighting games)

#### 2. **Art Production Workload**
**3D Pipeline (UE5):**
- ❌ Modeling: 2-3 weeks per character
- ❌ Rigging: 1 week per character
- ❌ Animation: 2-3 weeks per character
- ❌ Texturing/materials: 1 week per character
- ❌ **Total: 6-7 weeks per character (solo)**

**2D Pipeline (Godot):**
- ✅ Concept art: 3-5 days per character
- ✅ Sprite sheet creation: 1-2 weeks per character (or outsource)
- ✅ Animation assembly: 3-5 days per character
- ✅ VFX sprites: 1 week per character
- ✅ **Total: 3-4 weeks per character (solo)**
- ✅ Can use sprite commission services ($500-1500 per character)

**Time Savings: ~50% reduction in character production time**

#### 3. **Technical Complexity**
**UE5:**
- ❌ Custom GGPO integration (complex)
- ❌ Physics determinism requires custom work
- ❌ Blueprint vs C++ balance needed
- ❌ Packaging and build process complex

**Godot 4:**
- ✅ Rollback netcode addon available (open source)
- ✅ 2D physics deterministic by default
- ✅ Single language (GDScript)
- ✅ Export to Windows with one click

#### 4. **Performance**
**UE5:**
- 3D rendering overhead
- Needs optimization work
- 60 FPS target requires effort

**Godot 4:**
- 2D rendering is extremely fast
- 60 FPS easy to achieve
- Can target 120 FPS+ with minimal effort

#### 5. **Solo Developer Workflow**
**UE5:**
- ❌ Designed for team collaboration
- ❌ Heavy on system resources
- ❌ Longer compile times
- ❌ Complex asset management

**Godot 4:**
- ✅ Perfect for solo devs
- ✅ Runs on modest hardware
- ✅ Instant script changes (no compilation)
- ✅ Simple asset management

---

## Part 2: Visual Style Analysis

### Guilty Gear + Mortal Kombat Blend

#### Guilty Gear Characteristics:
- Hand-drawn anime aesthetic
- 3D models rendered to look 2D (Xrd, Strive)
- Cel-shaded with hand-drawn details
- Exaggerated animations with smear frames
- Vibrant colors and high contrast
- Dynamic camera angles during special moves
- Heavy emphasis on visual flair and style

#### Mortal Kombat Characteristics:
- Realistic/gritty aesthetic
- Detailed character designs
- Gore and impact emphasis
- Dark, moody color palette
- Cinematic presentation
- Heavy visual weight on attacks
- Brutality and visceral combat feel

#### Your Blend (Stylized 2D):
**Recommended Approach:**
- **Base:** Hand-drawn 2D sprites (Guilty Gear influence)
- **Detail Level:** Higher realism in anatomy and shading (MK influence)
- **Color:** Vibrant but with darker/grittier tones (blend)
- **Animation:** Exaggerated but weighty (blend)
- **VFX:** Flashy anime effects with impact emphasis (blend)

**Art Style Examples to Reference:**
- Guilty Gear Xrd/Strive (cel-shaded 3D-to-2D technique)
- Blazblue (high-detail 2D sprites)
- Skullgirls (hand-drawn animation)
- Injustice 2 (realistic but stylized)

**Technical Implementation Options:**

**Option A: Pure 2D Sprites (Recommended for Solo)**
- Hand-draw or commission sprite sheets
- Frame-by-frame animation
- Easier to outsource
- Lower technical barrier
- **Estimated cost:** $1,000-2,000 per character (outsourced)
- **Time investment (DIY):** 3-4 weeks per character

**Option B: 3D-to-2D Pipeline (Advanced)**
- Model characters in Blender
- Render to sprite sheets with cel-shading
- Guilty Gear Xrd technique
- More control over angles
- **Time investment:** 5-6 weeks per character
- Requires 3D modeling skills

**Recommendation:** Start with **Option A** for speed. Consider Option B for final version if you want more polish.

---

## Part 3: Technical Architecture Changes

### 3.1 Engine Architecture Comparison

| Component | UE5 (Original) | Godot 4 (New) | Change Impact |
|-----------|----------------|---------------|---------------|
| **Engine** | Unreal Engine 5 | Godot 4.3+ | 🔄 Complete rewrite |
| **Language** | C++ / Blueprints | GDScript / C# | 🔄 Code rewrite |
| **Rendering** | 3D (Chaos) | 2D (Custom) | 🔄 Complete change |
| **Physics** | UE5 Chaos (custom) | Godot Physics2D | ✅ Simpler, deterministic |
| **Networking** | Custom GGPO | Godot Rollback Netcode | ✅ Easier implementation |
| **Input** | UE Input System | Godot Input | 🔄 Reimplement |
| **Animation** | Control Rig | AnimationPlayer | 🔄 Reimplement |
| **VFX** | Niagara | Godot Particles2D / GPUParticles2D | 🔄 Reimplement |
| **UI** | UMG | Godot Control nodes | 🔄 Reimplement |
| **Audio** | MetaSounds | Godot AudioStreamPlayer | 🔄 Reimplement |
| **Data** | DataTables | JSON / Resources | ✅ Simpler |

---

### 3.2 New Technical Stack (Godot 4)

#### Core Engine
- **Godot 4.3+** (latest stable)
  - Built-in 2D physics (deterministic)
  - Scene system (perfect for character composition)
  - Node-based architecture
  - Hot-reload during development

#### Programming
- **GDScript** (primary)
  - Python-like syntax
  - Fast to write
  - Integrated with Godot
  - Perfect for gameplay logic
- **C#** (optional, for performance-critical)
  - Use only if GDScript becomes bottleneck (unlikely for 2D fighter)

#### Networking
- **Godot Rollback Netcode Addon**
  - Open source, community-maintained
  - Based on GGPO principles
  - Specifically designed for fighting games
  - GitHub: https://github.com/FlutterTal/godot-rollback-netcode
  - Active community support

#### Physics
- **Godot Physics2D**
  - Deterministic by default
  - Perfect for fighting games
  - Built-in collision shapes
  - Raycast support for projectiles

#### Animation
- **AnimationPlayer + AnimationTree**
  - Frame-by-frame sprite animation
  - State machine support
  - Blend animations
  - Animation callbacks for hitboxes

#### VFX
- **GPUParticles2D** (for effects)
- **Sprite2D** (for frame-by-frame VFX)
- **Shader materials** (for special effects)

#### Data Management
- **JSON files** for character data
  - Easy to edit
  - Version control friendly
  - No custom tools needed initially
- **Custom Resources** (later)
  - Godot's built-in data format
  - Inspector-editable
  - Can create custom editor plugins

---

### 3.3 System Architecture

```
Cosmic Kombat (Godot 4)
│
├── Core Systems
│   ├── GameManager (singleton)
│   │   ├── Round management
│   │   ├── Victory conditions
│   │   └── Pause/menu handling
│   │
│   ├── InputManager (singleton)
│   │   ├── Input buffering
│   │   ├── Motion detection
│   │   └── Player input mapping
│   │
│   └── MatchManager
│       ├── 2-player state sync
│       ├── Timer management
│       └── Round results
│
├── Character System
│   ├── Character (base scene)
│   │   ├── StateMachine
│   │   ├── HitboxManager
│   │   ├── HealthSystem (dual health)
│   │   ├── AnimationController
│   │   └── TierProperties
│   │
│   └── CharacterData (resource)
│       ├── Stats (health, speed, weight)
│       ├── Moves (array of MoveData)
│       └── Tier modifiers
│
├── Combat System
│   ├── HitboxManager
│   │   ├── Hitbox2D nodes
│   │   └── Collision detection
│   │
│   ├── DualHealthSystem
│   │   ├── Percentage tracker
│   │   ├── Health bar tracker
│   │   └── Victory condition checker
│   │
│   └── FrameDataTracker
│       ├── Startup frames
│       ├── Active frames
│       └── Recovery frames
│
├── Training Systems
│   ├── TrainingMode (scene)
│   ├── FrameDataDisplay (UI overlay)
│   ├── InputDisplay (UI overlay)
│   └── DummyController
│
├── UI System
│   ├── MainMenu
│   ├── CharacterSelect
│   ├── HUD (health bars, timer, percentage)
│   └── PauseMenu
│
└── Network System
    ├── RollbackSynchronizer (addon)
    ├── NetworkManager (singleton)
    └── OnlineMatchManager
```

---

## Part 4: What Changes, What's Removed, What's Added

### 4.1 REMOVED from Scope (UE5 → Godot 2D, Team → Solo)

#### ❌ Completely Removed:
1. **3D Asset Pipeline**
   - No 3D modeling, rigging, or animation
   - No texture/material work
   - No lighting setup

2. **Advanced Visual Features**
   - No real-time ray tracing
   - No complex particle systems (Niagara)
   - No dynamic camera angles during gameplay
   - No cinematic cutscenes (use static art + dialogue)

3. **Team Collaboration Tools**
   - No complex version control workflows
   - No asset management system
   - No build pipeline for multiple team members

4. **Advanced Networking Features (for demo)**
   - No matchmaking system
   - No lobby system
   - No ranked mode
   - **Keep for full launch:** Basic online versus with rollback

5. **Complex Game Modes (for demo)**
   - No story mode
   - No survival mode
   - No arcade mode endings
   - **Keep:** Training mode, local versus, basic arcade

6. **Live Operations (for demo)**
   - No battle pass
   - No in-game store
   - No seasonal content
   - **Keep for full launch:** DLC character support

#### ⚠️ Simplified (Reduced Scope):
1. **Training Mode**
   - Keep: Frame data display, input buffer visualization, dummy control
   - Simplify: Analytics dashboard (basic stats only)
   - Remove for demo: Remote coaching, community benchmarks

2. **Character Roster**
   - Original plan: 15-20 characters for launch
   - **Demo:** 6 characters (2+2+2 tiers)
   - **Full launch:** 12-15 characters

3. **Stage Count**
   - Original plan: 6+ stages
   - **Demo:** 2 stages
   - **Full launch:** 4-6 stages

4. **UI Complexity**
   - Keep: Essential menus (main, character select, options)
   - Simplify: No complex animations or transitions
   - Use clean, functional design

5. **Audio**
   - Simplify: 1 music track per stage (not dynamic)
   - Use royalty-free SFX initially
   - Voice acting: Text-only (no voice)

---

### 4.2 CHANGED (Technical Implementation)

#### 🔄 Major Changes:

1. **Character System**
   - **Old:** Component-based 3D with mesh + skeleton
   - **New:** Node-based 2D with sprite sheets + AnimationPlayer
   - **Implementation:** Simpler, faster to prototype

2. **Physics**
   - **Old:** Custom deterministic Chaos physics
   - **New:** Built-in Physics2D (already deterministic)
   - **Implementation:** Much easier, no custom work needed

3. **Hitbox System**
   - **Old:** 3D collision volumes
   - **New:** 2D Area2D / CollisionShape2D
   - **Implementation:** Simpler, easier to visualize and debug

4. **Frame Data**
   - **Old:** Complex 3D animation timeline
   - **New:** Simple frame numbers in sprite animation
   - **Implementation:** Easier to calculate and display

5. **VFX System**
   - **Old:** Niagara procedural particles
   - **New:** Sprite-based effects + simple particles
   - **Implementation:** Faster to create, more stylized

6. **Networking**
   - **Old:** Custom GGPO integration in UE5
   - **New:** Godot Rollback Netcode addon
   - **Implementation:** Plug-and-play, community-supported

7. **Data Pipeline**
   - **Old:** UE5 DataTables + custom tools
   - **New:** JSON files + text editor (initially)
   - **Implementation:** No tools needed to start

---

### 4.3 ADDED (New Opportunities)

#### ✅ New Advantages:

1. **Faster Iteration**
   - Hot-reload in Godot means instant testing
   - No compile times
   - Can test balance changes in seconds

2. **Modding Support**
   - Godot exports are mod-friendly
   - Easy to add custom character support later
   - Community can contribute content

3. **Cross-Platform Potential**
   - Godot exports to Linux/Mac easily
   - Could add Steam Deck support trivially
   - Low system requirements (runs on potato PCs)

4. **Pixel-Perfect Options**
   - Can do pixel art style if desired
   - Or high-res hand-drawn
   - More art style flexibility

5. **Open Source Tools**
   - Use Godot plugins from community
   - Contribute back if you make cool tools
   - No licensing fees ever

6. **Portfolio Value**
   - Godot is growing in indie community
   - Shows ability to work with modern indie tools
   - Demonstrates technical versatility

---

## Part 5: Solo Developer Roadmap

### 5.1 Realistic Timeline Assessment

**Key Constraint:** You're one person doing all:
- Game design
- Programming
- Art direction
- Asset creation (or outsourcing management)
- Testing
- Marketing

**Time Allocation Per Week (Realistic):**
- Full-time (40 hours/week): Aggressive but sustainable
- Part-time (20 hours/week): Slower but common for portfolio projects

**Skill Dependencies:**
- Programming: Critical path (you must do this)
- Art: Can outsource (recommended)
- Design: You're doing (documented already)

---

### 5.2 Phase 1: Pre-Production & Prototyping (Months 0-2)

**Objective:** Prove the core mechanics work in Godot

#### Month 1: Setup & Learning
**Focus:** Get comfortable with Godot and set up foundation

**Week 1-2: Godot Learning**
- [ ] Install Godot 4.3+
- [ ] Complete official Godot 2D tutorial
- [ ] Study fighting game examples in Godot
- [ ] Research Godot Rollback Netcode addon
- [ ] Set up project structure

**Resources:**
- Godot Docs: https://docs.godotengine.org
- Fighting game tutorials: Look for "godot fighting game" on YouTube
- Rollback addon: https://github.com/FlutterTal/godot-rollback-netcode

**Week 3-4: Core Systems Prototype**
- [ ] Build character controller (walk, dash, jump)
- [ ] Implement basic attack system
- [ ] Create simple hitbox/hurtbox system
- [ ] Test collision detection
- [ ] Build dual health system prototype

**Deliverables:**
- Project structure set up
- Two boxes fighting (programmer art)
- Dual health working (percentage + health bar)
- Movement feels responsive

**Time Investment:** 80-120 hours

---

#### Month 2: Mechanics Implementation
**Focus:** Complete core combat loop

**Week 1-2: Combat Mechanics**
- [ ] Implement frame data system
- [ ] Add hitstun and blockstun
- [ ] Create knockback system (tier-based)
- [ ] Implement blocking
- [ ] Add throw/grab mechanic
- [ ] Build combo system

**Week 3-4: First Character Spec**
- [ ] Define first character in detail (Tier 11 - low power)
- [ ] Implement 5 moves:
  - Light attack
  - Medium attack
  - Heavy attack
  - Special move
  - Ultimate attack
- [ ] Test moveset with placeholder sprites
- [ ] Balance frame data

**Deliverables:**
- Complete combat system with all mechanics
- First character playable with full moveset
- Frame data functional
- Combat feels good with placeholder art

**Time Investment:** 80-120 hours

**Total Pre-Production:** 160-240 hours (2 months full-time or 4 months part-time)

---

### 5.3 Phase 2: Vertical Slice (Months 3-8)

**Objective:** 2-character demo that's fun to play

#### Month 3-4: Art Production (Character 1 & 2)
**Focus:** Create or commission art for first 2 characters

**Option A: Commission Art ($2,000-4,000)**
- [ ] Write detailed character briefs (visual design)
- [ ] Commission concept art ($200-400 each)
- [ ] Commission sprite sheets ($1,000-2,000 each character)
  - Idle, walk, dash, jump
  - 5 attacks (light, medium, heavy, special, ultimate)
  - Hit reactions, block
  - Victory/defeat poses
- [ ] Commission VFX sprites ($300-500 per character)

**Option B: Create Art Yourself**
- [ ] Design characters (concept art)
- [ ] Draw sprite sheets (3-4 weeks per character)
- [ ] Create VFX sprites (1 week per character)

**Recommendation:** Commission art to focus on programming

**Week 1-2:**
- Write character briefs for Character 1 (Tier 11) and Character 2 (Tier 11)
- Commission concept art
- Begin integrating Character 1 sprites as they arrive

**Week 3-4:**
- Integrate Character 1 fully
- Commission Character 2 sprites
- Test Character 1 in combat

**Month 4:**
- Integrate Character 2 sprites
- Polish animations
- Balance matchup

**Deliverables:**
- 2 fully animated characters
- Both characters fun to play
- Distinct visual styles
- VFX for all attacks

**Time Investment:** 60-80 hours (if outsourcing) or 200-300 hours (if DIY)

---

#### Month 5-6: Core Game Modes
**Focus:** Training mode and versus mode

**Training Mode (Priority 1):**
- [ ] Frame data display overlay
- [ ] Hitbox/hurtbox visualization (color-coded)
- [ ] Input buffer display
- [ ] Dummy control (stance, recording)
- [ ] Training stage design
- [ ] Basic UI (clean and functional)

**Versus Mode:**
- [ ] Local 2-player functional
- [ ] Character select screen
- [ ] Stage select (2 stages)
- [ ] Round management
- [ ] Victory/defeat screens
- [ ] Basic menus

**Stage Creation:**
- [ ] Design 2 stages (concept art)
- [ ] Commission or create stage art ($300-600 per stage if outsourced)
- [ ] Implement parallax scrolling backgrounds
- [ ] Add ring-out boundaries

**UI/UX:**
- [ ] Design clean, functional UI (reference Guilty Gear Strive for inspiration)
- [ ] Health bars with percentage display
- [ ] Round timer
- [ ] Character portraits
- [ ] Menu system

**Deliverables:**
- Training mode with frame data (best-in-class)
- Local versus mode polished
- 2 stages
- Full UI flow (menus to gameplay)

**Time Investment:** 120-160 hours

---

#### Month 7-8: Polish & Vertical Slice Demo
**Focus:** Make it shippable quality

**Programming Polish:**
- [ ] Bug fixing
- [ ] Performance optimization (target 60 FPS minimum)
- [ ] Input buffering refinement
- [ ] Balance pass

**Audio:**
- [ ] Add music (2 stage tracks) - use royalty-free or commission
- [ ] SFX for all attacks - royalty-free libraries
- [ ] UI sound effects
- [ ] Hit impact sounds

**Visual Polish:**
- [ ] VFX timing and polish
- [ ] Screen shake and camera effects
- [ ] UI animations
- [ ] Particle effects

**Content:**
- [ ] Create demo-specific content:
  - Title screen
  - Options menu (rebindable controls, volume)
  - Credits
  - "Demo" watermark/notice

**Testing:**
- [ ] Self-testing (100+ hours of playtesting)
- [ ] Friends/playtesters (10+ people)
- [ ] Balance adjustments
- [ ] Bug fixes

**Build & Packaging:**
- [ ] Export to Windows
- [ ] Test on different PCs
- [ ] Create installer or ZIP
- [ ] Write README with controls

**Deliverables:**
- **2-Character Vertical Slice Demo**
  - 2 characters (both Tier 11 for demo simplicity)
  - Training mode (industry-leading)
  - Local versus mode
  - 2 stages
  - Polished UI
  - 60 FPS locked
  - Windows build

**Time Investment:** 120-160 hours

**Total Vertical Slice:** 300-400 hours (4-6 months full-time or 8-12 months part-time)

---

### 5.4 Phase 3: Expanding to 6-Character Demo (Months 9-14)

**Objective:** Add 4 more characters (2 mid-tier, 2 high-tier) and unlock system

#### Month 9-11: Mid-Tier Characters (Tier 8 x2)
**Focus:** Add 2 mid-tier characters with distinct playstyles

**Character 3 (Tier 8 - Rushdown):**
- [ ] Design character (concept art)
- [ ] Commission sprites ($1,000-2,000)
- [ ] Implement moveset (7 moves now - 2 specials)
- [ ] Balance against existing characters
- [ ] Create character-specific VFX

**Character 4 (Tier 8 - Zoner):**
- [ ] Design character (concept art)
- [ ] Commission sprites ($1,000-2,000)
- [ ] Implement moveset (7 moves with projectiles)
- [ ] Add projectile system
- [ ] Balance against existing characters

**Tier System Validation:**
- [ ] Implement tier-based frame data modifiers
- [ ] Test Tier 8 vs Tier 11 balance
- [ ] Adjust knockback and damage scaling

**New Stage:**
- [ ] Design and implement 1 new stage

**Deliverables:**
- 4 total characters (2 Tier 11, 2 Tier 8)
- Distinct archetypes (all-rounder, rushdown, zoner, grappler)
- Tier system functional and balanced
- 3 total stages

**Time Investment:** 200-250 hours

---

#### Month 12-14: High-Tier Unlockables (Tier 5 x2)
**Focus:** Boss-tier characters with unlock system

**Unlock System:**
- [ ] Track which characters used to beat arcade mode
- [ ] Implement unlock conditions (beat with all 4 characters)
- [ ] Save system for unlocks
- [ ] Unlock notification UI

**Character 5 (Tier 5 - High Power):**
- [ ] Design character (more elaborate)
- [ ] Commission sprites ($1,500-2,500)
- [ ] Implement expanded moveset (8-9 moves)
- [ ] Create flashy ultimate attack
- [ ] More elaborate VFX

**Character 6 (Tier 5 - High Power):**
- [ ] Design character (most elaborate)
- [ ] Commission sprites ($1,500-2,500)
- [ ] Implement expanded moveset (8-9 moves)
- [ ] Create flashy ultimate attack
- [ ] Most elaborate VFX

**Arcade Mode:**
- [ ] Create simple arcade ladder (5-6 fights)
- [ ] Difficulty progression
- [ ] Boss fight (Character 6 as final boss)
- [ ] Simple ending screen (text + character art)

**Polish:**
- [ ] Balance all 6 characters against each other
- [ ] Test unlock system
- [ ] Final bug fixing
- [ ] Demo polish pass

**Deliverables:**
- **6-Character Demo Complete**
  - 2 Tier 11 characters (starter)
  - 2 Tier 8 characters (mid-power)
  - 2 Tier 5 characters (unlockable high-power)
  - Unlock system functional
  - Arcade mode (basic)
  - Training mode (best-in-class)
  - Local versus mode
  - 3-4 stages
  - Full UI/menus
  - 60 FPS performance

**Time Investment:** 200-250 hours

**Total for 6-Character Demo:** 400-500 hours (5-7 months full-time or 10-14 months part-time)

---

### 5.5 Complete Timeline Summary (Demo)

| Phase | Duration (Full-Time) | Duration (Part-Time) | Hours | Cost (Outsourcing) |
|-------|---------------------|---------------------|-------|-------------------|
| Pre-Production (2 chars programmer art) | 2 months | 4 months | 160-240 | $0 |
| Vertical Slice (2 chars with art) | 4-6 months | 8-12 months | 300-400 | $2,000-4,000 |
| Mid-Tier Expansion (4 total chars) | 3 months | 6 months | 200-250 | $2,000-4,000 |
| High-Tier + Arcade (6 total chars) | 3 months | 6 months | 200-250 | $3,000-5,000 |
| **TOTAL FOR 6-CHAR DEMO** | **12-14 months** | **24-28 months** | **860-1,140 hours** | **$7,000-13,000** |

**Realistic Solo Timeline:**
- **Full-time (40 hrs/week):** 12-14 months
- **Part-time (20 hrs/week):** 24-28 months
- **Hobbyist (10 hrs/week):** 36-48 months

---

## Part 6: Full Launch Roadmap (12-15 Character Roster)

### 6.1 Post-Demo Development (Months 15-24+)

**Objective:** Expand to full roster and add online play

#### Characters 7-12: Expanding the Roster
**Timeline:** 2 months per character (solo pace)

**Tier Distribution (12-character full game):**
- Tier 11 (Low Power): 2 characters ✅ (in demo)
- Tier 10 (Low-Mid): 2 characters ⚠️ (add for full)
- Tier 9 (Mid-Low): 2 characters ⚠️ (add for full)
- Tier 8 (Mid): 2 characters ✅ (in demo)
- Tier 7 (Mid-High): 1 character ⚠️ (add for full)
- Tier 6 (High-Mid): 1 character ⚠️ (add for full)
- Tier 5 (High): 2 characters ✅ (in demo)

**Additional 6 Characters:**
- Month 15-16: Character 7 (Tier 10)
- Month 17-18: Character 8 (Tier 10)
- Month 19-20: Character 9 (Tier 9)
- Month 21-22: Character 10 (Tier 9)
- Month 23-24: Character 11 (Tier 7)
- Month 25-26: Character 12 (Tier 6)

**Per Character Work:**
- Design and concept art: 1 week
- Commission sprites: 3-4 weeks (external)
- Implementation: 2-3 weeks
- Testing and balance: 1 week

**Cost:** $6,000-12,000 (6 additional characters)

---

#### Online Multiplayer (Months 20-24)
**Timeline:** 4-5 months (parallel with character work)

**Implementation:**
- [ ] Integrate Godot Rollback Netcode addon
- [ ] Test with 2 characters first
- [ ] Expand to all characters
- [ ] Create online lobby system (simple)
- [ ] Implement netcode debugging tools
- [ ] Test with various network conditions

**Features:**
- Direct IP connection (minimum)
- Friend invite system (nice-to-have)
- Basic matchmaking (optional for v1.0)
- Replay save/load

**Testing:**
- Closed beta with friends (10-20 people)
- Open testing (itch.io or Steam playtest)

**Time Investment:** 150-200 hours

---

#### Additional Game Modes (Months 22-24)
**Timeline:** 2-3 months

**Survival Mode:**
- [ ] Continuous battles with health recovery
- [ ] Difficulty scaling
- [ ] Local leaderboard

**Time Attack Mode:**
- [ ] Speed-based challenges
- [ ] Leaderboard

**Story Mode (Optional):**
- [ ] Simple narrative (text-based)
- [ ] Character-specific endings (artwork + text)
- [ ] 5-7 battles per character
- **Cost:** $1,000-2,000 (ending artwork if commissioned)

**Time Investment:** 80-120 hours

---

#### Stages & Content (Ongoing)
**Timeline:** Spread throughout development

**Additional Stages:**
- 2 more stages (total 5-6)
- $600-1,200 if outsourced

**UI/UX Polish:**
- Main menu improvements
- Gallery mode (view character art)
- Sound test
- Options expansion

**Time Investment:** 60-80 hours

---

### 6.2 Launch Preparation (Months 24-26)

#### Final Polish
- [ ] Balance pass (all characters vs all characters)
- [ ] Bug fixing and QA
- [ ] Performance optimization
- [ ] Accessibility features (colorblind mode, rebinding)

**Time Investment:** 100-150 hours

---

#### Steam Preparation
- [ ] Create Steam store page
- [ ] Prepare marketing materials:
  - Screenshots
  - Trailer (1-2 minutes)
  - Key art
  - Capsule images
- [ ] Write store description
- [ ] Set up Steam achievements (optional)
- [ ] Build Steam depot

**Cost:**
- Steam Direct fee: $100
- Trailer creation: $500-2,000 (commission) or DIY
- Key art: $300-800 (commission)

**Time Investment:** 40-60 hours (plus trailer time if DIY)

---

#### Marketing & Community
- [ ] Create social media presence (Twitter, Discord)
- [ ] Post devlog updates
- [ ] Reach out to fighting game content creators
- [ ] Create press kit
- [ ] Submit to gaming sites/YouTubers

**Time Investment:** Ongoing, 5-10 hours/week

---

### 6.3 Full Launch Timeline

| Phase | Duration | Cost | Total Time from Start |
|-------|----------|------|-----------------------|
| 6-Character Demo | 12-14 months | $7,000-13,000 | Month 0-14 |
| Characters 7-12 | 12 months | $6,000-12,000 | Month 15-26 |
| Online Multiplayer | 4-5 months (parallel) | $0 | Month 20-24 |
| Additional Game Modes | 2-3 months (parallel) | $1,000-2,000 | Month 22-24 |
| Polish & Steam Prep | 2 months | $900-2,900 | Month 24-26 |
| **TOTAL FOR FULL LAUNCH** | **24-26 months** | **$14,900-29,900** | **~26 months** |

**Full-Time Solo Dev:** ~2 years from start to launch
**Part-Time Solo Dev:** ~4 years from start to launch

---

### 6.4 Post-Launch DLC Plan (Optional)

If the game is successful, consider:

**Season 1 (6 months post-launch):**
- 2 new characters (Tiers 3-4)
- 1 new stage
- Balance patches
- **Price:** $5.99 or free

**Season 2 (12 months post-launch):**
- 2 new characters (Tiers 1-2)
- 1 new stage
- New game mode
- **Price:** $5.99 or free

**Total DLC Characters:** Up to 16 total roster

---

## Part 7: Budget Breakdown

### 7.1 Demo Budget (6 Characters)

| Item | Cost |
|------|------|
| **Art Assets** | |
| Character concept art (6 characters @ $200-400) | $1,200-2,400 |
| Character sprite sheets (6 @ $1,000-2,000) | $6,000-12,000 |
| VFX sprites (6 characters @ $200-500) | $1,200-3,000 |
| Stage art (3-4 stages @ $300-600) | $900-2,400 |
| UI art/icons | $300-800 |
| **Audio** | |
| Music (3-4 tracks @ $100-300) | $300-1,200 |
| SFX pack (royalty-free) | $50-200 |
| **Tools & Software** | |
| Godot (free) | $0 |
| Art software (if needed) | $0-500 |
| **Marketing** | |
| Domain name (optional) | $12/year |
| **TOTAL DEMO** | **$9,962-22,500** |

**Budget Tiers:**
- **Minimum:** $7,000 (bare bones, mixed quality)
- **Recommended:** $12,000-15,000 (good quality)
- **Premium:** $20,000+ (high quality art)

---

### 7.2 Full Launch Budget (12 Characters)

| Item | Cost |
|------|------|
| Demo development | $10,000-15,000 |
| Additional 6 characters (art) | $6,000-12,000 |
| Additional 2-3 stages | $600-1,800 |
| Music (2-3 more tracks) | $200-900 |
| Steam launch | $100 |
| Marketing materials (trailer, key art) | $800-2,800 |
| **TOTAL FULL LAUNCH** | **$17,700-32,500** |

**Realistic Budget for Solo Dev:** $15,000-25,000

---

## Part 8: Risk Assessment & Mitigation

### 8.1 Solo Developer Risks

#### Risk 1: Scope Creep / Burnout
**Probability:** 🔴 Very High
**Impact:** Critical (project abandonment)

**Mitigation:**
- Set hard feature locks at each milestone
- Take breaks (1 week off every 3 months)
- Join gamedev community for support
- Track progress visibly (Trello, notion)
- Celebrate small wins
- Don't compare to AAA games

#### Risk 2: Art Quality / Consistency
**Probability:** 🟡 Medium
**Impact:** High (portfolio impression)

**Mitigation:**
- Commission from same artist(s) for consistency
- Create detailed style guide before commissioning
- Review work-in-progress before finalizing
- Budget for revisions (add 20% to art costs)
- Use royalty-free assets as backup

#### Risk 3: Technical Challenges (Netcode)
**Probability:** 🟡 Medium
**Impact:** Medium (online play quality)

**Mitigation:**
- Use proven addon (Godot Rollback Netcode)
- Join addon's Discord for support
- Test early and often
- Defer to post-demo if too difficult
- Make single-player solid first

#### Risk 4: Balance Issues
**Probability:** 🟡 Medium
**Impact:** Medium (competitive viability)

**Mitigation:**
- Extensive self-testing
- Recruit playtesters from fighting game community
- Iterate based on feedback
- Data-driven balance (track win rates)
- Post-launch patches allowed

#### Risk 5: Funding Shortfall
**Probability:** 🟡 Medium
**Impact:** High (can't complete art)

**Mitigation:**
- Start with 2-character demo (lower cost)
- Seek funding/crowdfunding after demo
- Consider Kickstarter with playable demo
- Freelance/contract work to fund development
- Release early access to fund completion

---

## Part 9: Key Decision Points

### Decision Point 1: Art Creation Strategy
**When:** Month 0 (now)
**Options:**

**Option A: Full Outsourcing (Recommended)**
- Pros: Faster, professional quality, focus on programming
- Cons: $15,000-25,000 cost
- Best if: You have budget or plan to crowdfund

**Option B: Hybrid (Learn + Outsource)**
- Pros: Lower cost ($8,000-12,000), learn art skills
- Cons: Slower development (add 6-12 months)
- Best if: Limited budget, want to learn art

**Option C: Full DIY**
- Pros: Lowest cost ($2,000-5,000 for tools/music)
- Cons: Requires art skills, adds 12-24 months
- Best if: You're already an artist or want to become one

**Recommendation:** Option A for faster completion, Option B if budget-constrained

---

### Decision Point 2: Demo Scope
**When:** Month 0 (now)
**Options:**

**Option A: 2-Character Minimal Demo**
- Scope: 2 characters, 1 stage, training + versus
- Timeline: 6-8 months
- Cost: $2,000-4,000
- Best if: Want to test concept quickly

**Option B: 4-Character Balanced Demo**
- Scope: 4 characters (2+2 tiers), 2 stages, training + versus + arcade
- Timeline: 10-12 months
- Cost: $5,000-9,000
- Best if: Want substantial demo for portfolio

**Option C: 6-Character Full Demo (Your Plan)**
- Scope: 6 characters (2+2+2 tiers), 3 stages, all modes
- Timeline: 12-14 months
- Cost: $7,000-13,000
- Best if: Want near-complete game experience

**Recommendation:** Start with Option A or B, expand to C if successful

---

### Decision Point 3: Release Strategy
**When:** Month 12-18
**Options:**

**Option A: Free Demo → Full Paid Release**
- Release 6-character demo for free
- Build community
- Full 12-character version as paid ($15-25)
- Best if: Want to build audience first

**Option B: Early Access**
- Release 6-character version as Early Access ($10-15)
- Fund remaining development
- Update to full version
- Best if: Need funding to continue

**Option C: Complete Then Launch**
- Finish 12-character version first
- Launch as complete product ($20-30)
- Best if: Have full funding upfront

**Recommendation:** Option A (free demo) or B (early access) for indie dev

---

## Part 10: Immediate Action Plan (Next 30 Days)

### Week 1: Setup & Design
- [ ] Install Godot 4.3+
- [ ] Complete Godot 2D tutorial (10 hours)
- [ ] Set up project structure
- [ ] Create character specification template
- [ ] Define first 2 characters in detail (Tier 11)
- [ ] Research sprite artists (ArtStation, Fiverr, Twitter)

### Week 2: Core Prototype
- [ ] Build character controller (movement)
- [ ] Implement basic attack system
- [ ] Create hitbox/hurtbox system
- [ ] Build dual health system
- [ ] Test with placeholder sprites (boxes)

### Week 3: Combat Depth
- [ ] Add frame data tracking
- [ ] Implement hitstun/blockstun
- [ ] Add knockback system
- [ ] Create blocking mechanic
- [ ] Test combat feel

### Week 4: First Character Spec
- [ ] Implement full moveset for Character 1 (5 moves)
- [ ] Balance frame data
- [ ] Playtest extensively
- [ ] Commission concept art for Character 1 & 2
- [ ] Start sprite artist search/commission

**Goal:** By end of Month 1, have playable prototype with 1 character (placeholder art) and art commissioning underway.

---

## Part 11: Godot Resources for Fighting Games

### Essential Learning Resources

**Official Godot:**
- Docs: https://docs.godotengine.org/en/stable/
- 2D Tutorial: https://docs.godotengine.org/en/stable/getting_started/first_2d_game/

**Fighting Game Specific:**
- Godot Rollback Netcode: https://github.com/FlutterTal/godot-rollback-netcode
- Fighting game tutorial (YouTube): Search "godot fighting game tutorial"
- GDQuest (excellent Godot tutorials): https://www.gdquest.com/

**Community:**
- Godot Discord: https://discord.gg/godotengine
- r/godot: https://reddit.com/r/godot
- Fighting Game Dev Discord: Search for "fighting game developers discord"

**Art Resources:**
- Sprite commission: Fiverr, ArtStation, Twitter (#commissions)
- Reference art: Guilty Gear Xrd/Strive, Blazblue, Skullgirls
- Royalty-free SFX: freesound.org, OpenGameArt.org
- Music: incompetech.com, Purple Planet Music

---

## Part 12: Summary & Recommendation

### The Switch to Godot 2D is HIGHLY RECOMMENDED

**Why:**
- ✅ 50% faster character production
- ✅ Much simpler technical implementation
- ✅ Better suited for solo development
- ✅ Free and open source
- ✅ Faster iteration and testing
- ✅ Built-in 2D physics (deterministic)
- ✅ Active community support
- ✅ Proven for fighting games

**Trade-offs:**
- ⚠️ Less visual spectacle than 3D (but stylized 2D can be stunning)
- ⚠️ Need to rewrite everything (but it'll be simpler)
- ⚠️ Learning new engine (but Godot is easier than UE5)

---

### Realistic Timeline for Your Goals

**6-Character Demo:**
- Full-time: 12-14 months
- Part-time: 24-28 months
- **Budget:** $10,000-15,000 (outsourcing art)

**12-Character Full Launch:**
- Full-time: 24-26 months from start
- Part-time: 48-52 months from start
- **Budget:** $18,000-30,000 total

---

### Your Next Steps (Priority Order)

1. **This Week: Learn Godot**
   - Install and complete 2D tutorial
   - Study fighting game examples

2. **Week 2-3: Build Core Prototype**
   - Character controller + combat system
   - Dual health system
   - Test with placeholder art

3. **Week 4: Commission Art**
   - Write character briefs
   - Find sprite artists
   - Commission concept art for first 2 characters

4. **Month 2: First Character**
   - Integrate sprites
   - Full moveset implementation
   - Polish and test

5. **Month 3-6: Vertical Slice**
   - 2-character demo
   - Training mode
   - Versus mode

6. **Month 7-14: Expand to 6 Characters**
   - Add remaining 4 characters
   - Unlock system
   - Arcade mode

---

### Budget Recommendations

**Minimum Viable Demo (2 characters):**
- Budget: $2,000-4,000
- Timeline: 6-8 months
- Use to test concept and seek funding

**Recommended Portfolio Demo (6 characters):**
- Budget: $10,000-15,000
- Timeline: 12-14 months
- Strong portfolio piece, potential for sales

**Funding Options:**
- Personal savings: Most sustainable
- Crowdfunding: After 2-character demo
- Early Access: After 4-6 character demo
- Part-time work: To fund development

---

## Conclusion

**The switch from UE5 3D to Godot 2D is STRONGLY RECOMMENDED for solo development.**

Your 6-character demo is achievable in 12-14 months (full-time) with a budget of $10,000-15,000. The stylized 2D approach (Guilty Gear + MK blend) is perfect for this scope.

Start learning Godot this week, build a prototype next month, and commission art once you've proven the concept. Focus on making the training mode exceptional - that's your unique selling point.

You can absolutely do this solo. Many successful indie fighting games were made by small teams or solo devs:
- Skullgirls (started with 3 people)
- Yomi Hustle (solo dev, using GGRS rollback)
- Tough Love Arena (small team)

**Next document to create:** Character specification template and first 2 character designs.

Good luck! You've got a solid plan now. 🎮⚔️
