# Godot Project Structure Guide

**Project Name:** Cosmic Kombat
**Engine:** Godot 4.3+
**Project Type:** 2D Fighting Game

---

## Complete Directory Structure

```
cosmic-kombat/                          # Root project folder
├── project.godot                       # Godot project file
├── .gitignore                          # Git ignore file
├── .gitattributes                      # Git LFS configuration
├── README.md                           # Project README
│
├── assets/                             # All game assets (not imported)
│   ├── characters/                     # Character sprites and animations
│   │   ├── ryn/
│   │   │   ├── sprites/               # PNG sprite sheets
│   │   │   │   ├── idle.png
│   │   │   │   ├── walk.png
│   │   │   │   ├── attacks.png
│   │   │   │   └── ...
│   │   │   ├── vfx/                   # Character-specific VFX
│   │   │   │   ├── hit_sparks.png
│   │   │   │   └── trails.png
│   │   │   └── audio/                 # Character-specific audio
│   │   │       ├── voice/
│   │   │       └── sfx/
│   │   │
│   │   ├── kira/
│   │   │   └── [same structure as ryn]
│   │   │
│   │   └── [other characters...]
│   │
│   ├── stages/                        # Stage backgrounds
│   │   ├── training_stage/
│   │   │   ├── background.png
│   │   │   ├── midground.png
│   │   │   ├── foreground.png
│   │   │   └── music.ogg
│   │   └── [other stages...]
│   │
│   ├── ui/                            # UI elements
│   │   ├── menus/
│   │   │   ├── main_menu_bg.png
│   │   │   ├── buttons/
│   │   │   └── frames/
│   │   ├── hud/
│   │   │   ├── health_bar.png
│   │   │   ├── percentage_display.png
│   │   │   └── timer.png
│   │   ├── fonts/
│   │   │   ├── main_font.ttf
│   │   │   └── damage_numbers.ttf
│   │   └── icons/
│   │       └── [various icons]
│   │
│   ├── vfx/                           # Global VFX assets
│   │   ├── hit_effects/
│   │   ├── particles/
│   │   └── screen_effects/
│   │
│   └── audio/                         # Global audio
│       ├── music/
│       │   ├── menu_theme.ogg
│       │   └── [stage music]
│       ├── sfx/
│       │   ├── ui/
│       │   └── impacts/
│       └── announcer/
│           └── [announcer voice lines]
│
├── scenes/                            # Godot scene files
│   ├── characters/                    # Character scenes
│   │   ├── base_character.tscn       # Base character template
│   │   ├── ryn/
│   │   │   ├── ryn.tscn              # Main character scene
│   │   │   ├── hitboxes/             # Hitbox scenes
│   │   │   └── states/               # State machine states
│   │   │
│   │   ├── kira/
│   │   │   ├── kira.tscn
│   │   │   ├── energy_trap.tscn      # Trap object
│   │   │   ├── energy_cannon.tscn    # Projectile
│   │   │   └── ...
│   │   │
│   │   └── [other characters...]
│   │
│   ├── stages/                        # Stage scenes
│   │   ├── base_stage.tscn           # Base stage template
│   │   ├── training_stage.tscn
│   │   └── [other stages...]
│   │
│   ├── ui/                            # UI scenes
│   │   ├── menus/
│   │   │   ├── main_menu.tscn
│   │   │   ├── character_select.tscn
│   │   │   ├── options_menu.tscn
│   │   │   └── pause_menu.tscn
│   │   ├── hud/
│   │   │   ├── battle_hud.tscn       # In-match UI
│   │   │   ├── health_bar.tscn
│   │   │   ├── timer.tscn
│   │   │   └── combo_counter.tscn
│   │   └── training_mode/
│   │       ├── frame_data_display.tscn
│   │       ├── input_display.tscn
│   │       └── dummy_controls.tscn
│   │
│   ├── game_modes/                    # Game mode scenes
│   │   ├── versus_mode.tscn
│   │   ├── training_mode.tscn
│   │   ├── arcade_mode.tscn
│   │   └── [other modes...]
│   │
│   ├── effects/                       # VFX scenes
│   │   ├── hit_spark.tscn
│   │   ├── screen_shake.tscn
│   │   └── particle_effects/
│   │
│   └── main.tscn                      # Main game scene
│
├── scripts/                           # GDScript files
│   ├── autoload/                      # Singleton scripts (autoload)
│   │   ├── game_manager.gd           # Global game state
│   │   ├── input_manager.gd          # Input buffering and processing
│   │   ├── audio_manager.gd          # Audio control
│   │   ├── save_manager.gd           # Save/load system
│   │   └── debug_manager.gd          # Debug tools
│   │
│   ├── characters/                    # Character scripts
│   │   ├── base_character.gd         # Base character class
│   │   ├── state_machine.gd          # State machine base
│   │   ├── hitbox_manager.gd         # Hitbox/hurtbox management
│   │   ├── health_system.gd          # Dual health system
│   │   ├── input_buffer.gd           # Per-character input buffer
│   │   │
│   │   ├── ryn/
│   │   │   ├── ryn_character.gd
│   │   │   ├── ryn_state_machine.gd
│   │   │   └── states/               # Individual state scripts
│   │   │       ├── idle.gd
│   │   │       ├── walk.gd
│   │   │       ├── attack_la1.gd
│   │   │       └── ...
│   │   │
│   │   └── [other characters...]
│   │
│   ├── combat/                        # Combat system scripts
│   │   ├── frame_data.gd             # Frame data tracker
│   │   ├── combo_system.gd           # Combo detection
│   │   ├── damage_calculator.gd      # Damage scaling
│   │   ├── knockback_system.gd       # Knockback physics
│   │   └── tier_modifiers.gd         # Tier-based modifications
│   │
│   ├── ui/                            # UI scripts
│   │   ├── main_menu.gd
│   │   ├── character_select.gd
│   │   ├── battle_hud.gd
│   │   └── [other UI scripts]
│   │
│   ├── game_modes/                    # Game mode scripts
│   │   ├── versus_mode.gd
│   │   ├── training_mode.gd
│   │   ├── arcade_mode.gd
│   │   └── match_manager.gd          # Round/match logic
│   │
│   ├── stages/                        # Stage scripts
│   │   ├── base_stage.gd
│   │   └── [stage-specific scripts]
│   │
│   ├── network/                       # Online/networking scripts
│   │   ├── rollback_manager.gd       # Rollback netcode integration
│   │   ├── network_manager.gd        # Network connection
│   │   └── sync_manager.gd           # State synchronization
│   │
│   └── utils/                         # Utility scripts
│       ├── constants.gd              # Global constants
│       ├── enums.gd                  # Enumerations
│       ├── math_utils.gd             # Math helpers
│       └── debug_draw.gd             # Debug visualization
│
├── data/                              # Game data (JSON, resources)
│   ├── characters/                    # Character data files
│   │   ├── ryn.json                  # Ryn's stats and properties
│   │   ├── kira.json
│   │   └── [other characters...]
│   │
│   ├── moves/                         # Move data files
│   │   ├── ryn_moves.json            # Ryn's complete moveset
│   │   ├── kira_moves.json
│   │   └── [other characters...]
│   │
│   ├── stages/                        # Stage data
│   │   └── stage_list.json
│   │
│   ├── game_balance/                  # Balance data
│   │   ├── tier_modifiers.json       # Tier scaling values
│   │   ├── damage_scaling.json       # Combo scaling
│   │   └── frame_advantage.json      # Global frame data rules
│   │
│   └── schemas/                       # JSON schema definitions
│       ├── character_schema.json
│       ├── move_schema.json
│       └── [other schemas...]
│
├── resources/                         # Godot Resource files (.tres)
│   ├── characters/
│   │   ├── ryn_data.tres             # Character resource (alternative to JSON)
│   │   └── [others...]
│   │
│   └── materials/                     # Shader materials
│       └── [various materials]
│
├── shaders/                           # Shader files (.gdshader)
│   ├── hit_flash.gdshader            # Hit flash effect
│   ├── outline.gdshader              # Character outline
│   └── screen_effects.gdshader       # Post-processing
│
├── addons/                            # Godot addons/plugins
│   ├── godot-rollback-netcode/       # Rollback netcode addon
│   │   └── [addon files]
│   │
│   └── [other addons...]
│
├── tests/                             # Unit tests (optional but recommended)
│   ├── test_combat_system.gd
│   ├── test_hitbox_detection.gd
│   └── [other tests...]
│
├── tools/                             # Development tools/utilities
│   ├── frame_data_editor/            # Custom editor for frame data
│   ├── hitbox_visualizer/            # Debug hitbox tool
│   └── character_validator/          # Validate character data
│
└── docs/                              # In-project documentation
    ├── setup_guide.md
    ├── scripting_conventions.md
    └── [other docs...]
```

---

## Key Directories Explained

### `/assets/`
**Purpose:** All source assets before Godot import
- Use `.import` files will be generated by Godot
- Keep organized by type (characters, stages, UI, etc.)
- Use Git LFS for large files (PNGs, audio)

**Best Practices:**
- High-resolution source files here
- Consistent naming: `character_name_animation_frame.png`
- Keep backup of .psd/.aseprite files elsewhere (not in project)

---

### `/scenes/`
**Purpose:** All Godot scene files (.tscn)
- Each scene is a reusable game object
- Organized by functionality

**Best Practices:**
- Create base/template scenes (e.g., `base_character.tscn`)
- Inherit from base scenes for specific characters
- Keep scenes small and focused (single responsibility)
- Name scenes clearly: `character_name.tscn`, not `scene1.tscn`

---

### `/scripts/`
**Purpose:** All GDScript files (.gd)
- Organized by system/domain
- `/autoload/` for singleton scripts (global access)

**Best Practices:**
- One class per file
- Match file name to class name: `HealthSystem` → `health_system.gd`
- Use PascalCase for class names, snake_case for file names
- Comment extensively, especially for complex systems

---

### `/data/`
**Purpose:** Game data in JSON (or Godot Resource format)
- Character stats, move properties, balance values
- Editable without recompiling scripts
- Version controlled (track balance changes)

**Best Practices:**
- Use JSON for data that designers might edit
- Define schemas for validation
- Keep data separate from logic (scripts)

---

### `/resources/`
**Purpose:** Godot Resource files (.tres, .res)
- Alternative to JSON for Godot-specific data
- Can be edited in Godot inspector
- Good for complex nested data

**When to use Resources vs JSON:**
- **JSON:** Simple data, external editing, readability
- **Resources:** Complex data, Godot inspector editing, references to other resources

---

## Autoload (Singleton) Setup

**Autoload scripts** are globally accessible singletons. Configure in Project Settings → Autoload.

### Recommended Autoloads:

1. **GameManager** (`scripts/autoload/game_manager.gd`)
   ```gdscript
   extends Node
   # Global game state, scene transitions, game flow
   ```

2. **InputManager** (`scripts/autoload/input_manager.gd`)
   ```gdscript
   extends Node
   # Input buffering, motion detection, remapping
   ```

3. **AudioManager** (`scripts/autoload/audio_manager.gd`)
   ```gdscript
   extends Node
   # Music and SFX control, volume management
   ```

4. **SaveManager** (`scripts/autoload/save_manager.gd`)
   ```gdscript
   extends Node
   # Save/load game data, settings, unlocks
   ```

5. **DebugManager** (`scripts/autoload/debug_manager.gd`)
   ```gdscript
   extends Node
   # Debug tools, hitbox visualization, frame data display
   ```

---

## Scene Organization Best Practices

### Character Scene Structure

**Example: `scenes/characters/ryn/ryn.tscn`**

```
Ryn (CharacterBody2D)                  # Root node
├── StateMachine (Node)                # State machine controller
│   ├── Idle (Node)                    # State: Idle
│   ├── Walk (Node)                    # State: Walk
│   ├── Attack_LA1 (Node)              # State: Light Attack 1
│   └── ...                            # Other states
│
├── Sprite2D                           # Character sprite
│   └── AnimationPlayer                # Sprite animations
│
├── HitboxManager (Node2D)             # Manages hitboxes
│   ├── Hurtbox (Area2D)               # Body collision (always active)
│   │   └── CollisionShape2D
│   └── HitboxContainer (Node2D)       # Spawned hitboxes go here
│
├── HealthSystem (Node)                # Dual health tracking
│
├── InputBuffer (Node)                 # Input buffering
│
├── AudioStreamPlayer2D                # SFX player
│
└── DebugLabel (Label)                 # Shows current state (debug only)
```

**Explanation:**
- **CharacterBody2D:** Root node for physics
- **StateMachine:** Controls character behavior (idle, attacking, etc.)
- **Sprite2D + AnimationPlayer:** Visuals and animations
- **HitboxManager:** Spawns hitboxes during attacks
- **HealthSystem:** Tracks percentage and health bar
- **InputBuffer:** Stores recent inputs for special moves

---

### Stage Scene Structure

**Example: `scenes/stages/training_stage.tscn`**

```
TrainingStage (Node2D)                 # Root node
├── Background (ParallaxBackground)    # Scrolling background
│   ├── BackLayer (ParallaxLayer)      # Far background
│   │   └── Sprite2D
│   ├── MidLayer (ParallaxLayer)       # Mid ground
│   │   └── Sprite2D
│   └── FrontLayer (ParallaxLayer)     # Near foreground
│       └── Sprite2D
│
├── StageFloor (StaticBody2D)          # Ground collision
│   └── CollisionShape2D
│
├── Boundaries (Node2D)                # Stage boundaries
│   ├── LeftWall (Area2D)              # Left boundary
│   │   └── CollisionShape2D
│   ├── RightWall (Area2D)             # Right boundary
│   │   └── CollisionShape2D
│   ├── Ceiling (Area2D)               # Top boundary
│   │   └── CollisionShape2D
│   └── DeathZone (Area2D)             # Ring-out zone
│       └── CollisionShape2D
│
├── SpawnPoints (Node2D)               # Player spawn positions
│   ├── Player1Spawn (Marker2D)
│   └── Player2Spawn (Marker2D)
│
├── Camera (Camera2D)                  # Stage camera
│
└── AudioStreamPlayer                  # Stage music
```

---

## Data File Structure

### Character Data JSON Example

**File: `data/characters/ryn.json`**

```json
{
  "name": "Ryn",
  "display_name": "Ryn \"The Striker\"",
  "tier": 11,
  "archetype": "All-Rounder",
  "difficulty": "Beginner",

  "stats": {
    "health": 100,
    "weight": 5,
    "walk_speed": 5.0,
    "dash_speed": 7.0,
    "jump_height": 6.0,
    "air_control": 6.0
  },

  "tier_modifiers": {
    "hitbox_size": 1.0,
    "knockback_modifier": 1.0,
    "damage_scaling": 1.0
  },

  "movement": {
    "dash_duration": 18,
    "dash_distance": 3.0,
    "backdash_invincibility": [1, 8],
    "air_jumps": 0,
    "air_dash_enabled": false
  },

  "visuals": {
    "sprite_scale": 1.0,
    "color_primary": "#2B2B2B",
    "color_secondary": "#B91C1C",
    "vfx_color": "#EF4444"
  }
}
```

### Move Data JSON Example

**File: `data/moves/ryn_moves.json`**

```json
{
  "character": "ryn",
  "moves": [
    {
      "id": "LA1",
      "name": "Quick Jab",
      "input": "L",
      "type": "light_attack",

      "frame_data": {
        "startup": 5,
        "active": 2,
        "recovery": 8,
        "on_hit": 5,
        "on_block": 1,
        "total": 15
      },

      "properties": {
        "damage_health": 3,
        "damage_percentage": 2,
        "knockback": 0.2,
        "knockback_angle": 60,
        "hitstun": 12,
        "blockstun": 10,
        "range": 1.5
      },

      "hitbox": {
        "shape": "circle",
        "radius": 0.4,
        "offset_x": 1.5,
        "offset_y": 0.0
      },

      "cancel_options": ["LA2", "LA3", "MA1", "SP1", "SP2"],
      "cancel_window": [6, 15],

      "animation": "attack_la1",
      "sfx": "whoosh_light"
    },

    // ... more moves
  ]
}
```

---

## Git Configuration

### `.gitignore`

```gitignore
# Godot-specific ignores
.import/
export.cfg
export_presets.cfg
*.translation

# Godot exported game builds
*.exe
*.pck
*.zip

# Mono-specific ignores (if using C#)
.mono/
data_*/

# System files
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/

# Temp files
*.tmp
*.log
```

### `.gitattributes` (for Git LFS)

```gitattributes
# Images
*.png filter=lfs diff=lfs merge=lfs -text
*.jpg filter=lfs diff=lfs merge=lfs -text
*.jpeg filter=lfs diff=lfs merge=lfs -text
*.psd filter=lfs diff=lfs merge=lfs -text

# Audio
*.wav filter=lfs diff=lfs merge=lfs -text
*.ogg filter=lfs diff=lfs merge=lfs -text
*.mp3 filter=lfs diff=lfs merge=lfs -text

# Other large files
*.zip filter=lfs diff=lfs merge=lfs -text
```

---

## Naming Conventions

### Files
- **Scenes:** `snake_case.tscn` (e.g., `main_menu.tscn`, `ryn_character.tscn`)
- **Scripts:** `snake_case.gd` (e.g., `health_system.gd`)
- **Assets:** `descriptive_name_variant.png` (e.g., `ryn_idle_001.png`)

### Code
- **Classes:** `PascalCase` (e.g., `HealthSystem`, `InputManager`)
- **Variables:** `snake_case` (e.g., `current_health`, `is_attacking`)
- **Constants:** `SCREAMING_SNAKE_CASE` (e.g., `MAX_HEALTH`, `GRAVITY`)
- **Functions:** `snake_case` (e.g., `calculate_damage()`, `spawn_hitbox()`)
- **Signals:** `snake_case` (e.g., `health_changed`, `attack_landed`)

### Nodes
- **Scene nodes:** `PascalCase` (e.g., `Sprite2D`, `CollisionShape2D`)
- **Custom node names:** `PascalCase` (e.g., `HealthBar`, `PlayerSpawn`)

---

## Development Workflow

### Initial Setup
1. Create project in Godot 4.3+
2. Set up directory structure (create folders)
3. Configure Git (init, .gitignore, Git LFS)
4. Set up autoload scripts in Project Settings
5. Create base scenes (base_character, base_stage)

### Character Development Workflow
1. Create character specification document (see templates)
2. Commission or create art assets
3. Create character scene from base_character template
4. Create character data JSON
5. Create move data JSON
6. Implement character script and state machine
7. Implement individual moves
8. Test frame data accuracy
9. Add VFX and audio
10. Balance and iterate

### Testing Workflow
1. Unit test individual systems (hitbox detection, frame data)
2. Playtest character in training mode
3. Playtest matchup vs other characters
4. Iterate based on feedback
5. Document balance changes

---

## Performance Optimization Tips

1. **Use object pooling** for frequently spawned objects (hitboxes, VFX)
2. **Limit particle effects** on screen simultaneously
3. **Optimize sprite sheets** (power-of-2 dimensions, compressed)
4. **Use Area2D** for hitboxes (lighter than RigidBody2D)
5. **Disable nodes** that aren't visible (don't just hide them)
6. **Profile regularly** using Godot's profiler
7. **Target 60 FPS minimum** on modest hardware

---

## Recommended Addons

1. **Godot Rollback Netcode** (essential for online play)
   - GitHub: https://github.com/FlutterTal/godot-rollback-netcode

2. **Gut** (testing framework - optional but recommended)
   - For unit testing game systems

3. **Dialogue Manager** (if adding story mode)

4. **Input Helper** (for motion input detection)

---

## Next Steps

1. **Set up project:** Create folders, configure Git
2. **Create base scenes:** `base_character.tscn`, `base_stage.tscn`
3. **Implement autoload scripts:** Start with GameManager and InputManager
4. **Build first character:** Ryn (using specification document)
5. **Create training stage:** Simple flat stage for testing
6. **Implement training mode:** Frame data display, dummy control

---

## Additional Resources

- **Godot Docs:** https://docs.godotengine.org
- **Fighting Game Tutorial:** Search YouTube for "godot fighting game"
- **Rollback Netcode Docs:** See addon GitHub repository

---

**Document Version:** 1.0
**Last Updated:** 2025-10-24
**For Project:** Cosmic Kombat (Godot 4.3+)
