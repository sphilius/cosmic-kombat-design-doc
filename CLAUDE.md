# CLAUDE.md - AI Assistant Guide for Cosmic Kombat Design Documentation

**Repository:** Cosmic Kombat Design Documentation
**Project Status:** Pre-production Phase
**Last Updated:** 2025-11-14
**Purpose:** Design documentation for a revolutionary fighting game implementing VSBattles Wiki power scaling

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Repository Structure](#repository-structure)
3. [Key Concepts & Terminology](#key-concepts--terminology)
4. [Documentation Navigation](#documentation-navigation)
5. [Development Workflow](#development-workflow)
6. [Working with This Repository](#working-with-this-repository)
7. [Documentation Standards](#documentation-standards)
8. [Architecture & Technical Decisions](#architecture--technical-decisions)
9. [Current Priorities](#current-priorities)
10. [Common Tasks & How to Execute Them](#common-tasks--how-to-execute-them)

---

## Project Overview

### What is Cosmic Kombat?

Cosmic Kombat: Battle of the Tiers is a revolutionary fighting game that implements the VSBattles Wiki power scaling system (12 tiers from 11-C to Low 1-A). The game features a unique **dual health system** combining Super Smash Bros-style percentage damage with Mortal Kombat-style health bars.

### Project Status

- **Phase:** Pre-production / Design Documentation
- **Completeness:** ~40-50% design documentation complete
- **Next Milestone:** Vertical Slice Prototype (Target: 9 months from foundation sprint)
- **Target Platforms:** Unreal Engine 5 (PC, PlayStation, Xbox)

### Core Differentiators

1. **Dual Health System:** Combines percentage damage (knockback) with traditional health bars
2. **Tier-Based Power Scaling:** 12 tiers of character power (11-C through Low 1-A)
3. **Best-in-Class Training Mode:** Comprehensive frame data, analytics, and learning tools
4. **GGPO Rollback Netcode:** Industry-leading online play with cross-platform support
5. **Player-Friendly Monetization:** Transparent battle pass system, no pay-to-win

---

## Repository Structure

```
cosmic-kombat-design-doc/
│
├── README.md                              # Project overview and navigation
├── CLAUDE.md                              # This file - AI assistant guide
│
├── ARCHITECTURE_FEATURE_ANALYSIS.md       # MECE analysis, roadmap, and strategic plan
│
├── DOMAIN_*_TODO_LIST.md                  # Domain-specific action items
│   ├── DOMAIN_1_TODO_LIST.md              # Gameplay Systems tasks
│   ├── DOMAIN_2_TODO_LIST.md              # Technical Infrastructure tasks
│   ├── DOMAIN_3_TODO_LIST.md              # Content Systems tasks
│   ├── DOMAIN_4_TODO_LIST.md              # Player Experience tasks
│   └── DOMAIN_5_TODO_LIST.md              # Live Operations tasks
│
├── core-mechanics/                        # Core gameplay design docs
│   ├── combat-system.md                   # Dual health system specification
│   └── tier-system.md                     # VSBattles tier implementation
│
├── content/                               # Training and learning systems
│   ├── training-index.md                  # Overview of training suite
│   ├── training-mode.md                   # Training mode overview
│   ├── frame-data.md                      # Frame data system design
│   ├── input-buffer.md                    # Input buffer specification
│   └── analytics-dashboard.md             # Player analytics features
│
├── technical-specs/                       # Engineering architecture
│   └── architecture.md                    # Core technical decisions
│
├── business/                              # Business model documentation
│   └── monetization.md                    # Revenue and monetization strategy
│
└── post-launch/                           # Long-term planning
    └── roadmap.md                         # Post-launch content roadmap
```

### File Naming Conventions

- **ALL_CAPS.md**: High-level strategic documents (ARCHITECTURE_FEATURE_ANALYSIS.md, DOMAIN_*_TODO_LIST.md)
- **kebab-case.md**: Specific design documentation (combat-system.md, training-mode.md)
- **Category folders**: Lowercase with hyphens (core-mechanics/, technical-specs/)

---

## Key Concepts & Terminology

### Gameplay Mechanics

- **Dual Health System**: Two simultaneous health metrics - percentage damage (affects knockback) and health bar (traditional damage)
- **Tier System**: 12-tier power scaling from VSBattles Wiki (11-C weakest → Low 1-A strongest)
- **Ring-Out**: Victory condition when opponent is knocked out of arena boundaries
- **Knockback Scaling**: Higher percentage damage = greater knockback distance
- **Frame Data**: Timing specifications for moves (startup, active, recovery frames)

### Technical Terms

- **GGPO**: Rollback netcode technology for near-lagless online play
- **Component-Based Architecture**: Modular character system with tier-based behaviors
- **Deterministic Physics**: Ensures identical results across all platforms for competitive integrity
- **Input Buffer**: System that stores and processes player inputs with configurable timing windows
- **MECE Analysis**: Mutually Exclusive, Collectively Exhaustive (strategic planning framework)

### Development Phases

1. **Vertical Slice** (Months 0-9): 2 characters, core mechanics, training mode demo
2. **Alpha** (Months 10-18): 8 characters, all game modes, online infrastructure
3. **Beta** (Months 19-27): 15 characters, competitive features, polish
4. **Launch** (Month 30): Full release with 20+ characters

### Domain Structure

The project uses a **5-domain MECE framework** (see ARCHITECTURE_FEATURE_ANALYSIS.md):

1. **Domain 1 - Gameplay Systems**: Combat mechanics, character systems, movement
2. **Domain 2 - Technical Infrastructure**: Engine, networking, data management
3. **Domain 3 - Content Systems**: Art, animation, audio, UI/UX
4. **Domain 4 - Player Experience**: Tutorial, training, game modes, accessibility
5. **Domain 5 - Live Operations**: Matchmaking, monetization, community features

---

## Documentation Navigation

### For Understanding the Game Vision

**Start Here:**
1. `/README.md` - Project introduction
2. `/ARCHITECTURE_FEATURE_ANALYSIS.md` - Comprehensive strategic plan (parts 1-8)
3. `/core-mechanics/combat-system.md` - Core gameplay loop
4. `/core-mechanics/tier-system.md` - Power scaling implementation

### For Technical Implementation

**Engineering Focus:**
1. `/technical-specs/architecture.md` - Core technical decisions
2. `/ARCHITECTURE_FEATURE_ANALYSIS.md` → Part 2 (5 High-Impact Features)
3. `/content/frame-data.md` - Frame data system
4. `/content/input-buffer.md` - Input handling architecture

### For Content Creation

**Art/Design Focus:**
1. `/ARCHITECTURE_FEATURE_ANALYSIS.md` → Domain 3 Analysis (Content Systems)
2. `/DOMAIN_3_TODO_LIST.md` - Content system tasks
3. `/content/training-mode.md` - Visual design requirements

### For Current Tasks

**Action Items:**
1. `/DOMAIN_1_TODO_LIST.md` - Gameplay tasks (CRITICAL PRIORITY)
2. `/DOMAIN_2_TODO_LIST.md` - Infrastructure tasks
3. `/DOMAIN_3_TODO_LIST.md` - Content tasks (CRITICAL PRIORITY)
4. `/DOMAIN_4_TODO_LIST.md` - Player experience tasks
5. `/DOMAIN_5_TODO_LIST.md` - Live ops tasks

### For Business Understanding

**Stakeholder Focus:**
1. `/business/monetization.md` - Revenue model
2. `/post-launch/roadmap.md` - Long-term content plan
3. `/ARCHITECTURE_FEATURE_ANALYSIS.md` → Part 5 (Resource Planning & Budget)

---

## Development Workflow

### Git Branching Strategy

- **Main Branch**: `main` (or default branch name - check with `git branch`)
- **Feature Branches**: Use `claude/` prefix for AI-assisted development
  - Example: `claude/character-spec-template`
  - Example: `claude/combat-system-update`
- **Branch Naming**: `claude/<descriptive-name>-<session-id>`

### Commit Message Conventions

Based on git history analysis:

```
# Good Examples (from recent commits):
✓ "Add Domain 5 to-do list"
✓ "Add comprehensive MECE architecture analysis and development roadmap"
✓ "Create training suite index"

# Format Guidelines:
- Use imperative mood ("Add", "Create", "Update", "Fix", "Document")
- Be specific about what was changed
- Reference domain/feature areas when applicable
```

### Development Process

1. **Check current branch**: Verify you're on the correct development branch
2. **Read relevant docs**: Always review existing documentation before making changes
3. **Make changes**: Edit or create documentation files
4. **Commit with clear messages**: Follow commit conventions above
5. **Push to feature branch**: Use `git push -u origin <branch-name>`

### Pull Request Requirements

When creating PRs:
- Summarize changes with context from the documentation
- Reference related domain todo lists
- Highlight which gaps from ARCHITECTURE_FEATURE_ANALYSIS.md are addressed

---

## Working with This Repository

### Before Making Changes

**Always Read First:**
1. Check if documentation already exists for the topic
2. Review `ARCHITECTURE_FEATURE_ANALYSIS.md` for context and gaps
3. Check relevant `DOMAIN_*_TODO_LIST.md` for current priorities
4. Understand the MECE framework to avoid overlap

### When Creating New Documentation

**Follow These Patterns:**

1. **Gameplay Mechanics** → `/core-mechanics/[feature].md`
2. **Training/Learning Features** → `/content/[feature].md`
3. **Technical Architecture** → `/technical-specs/[system].md`
4. **Business/Monetization** → `/business/[topic].md`
5. **Post-Launch Planning** → `/post-launch/[topic].md`

### When Updating Existing Documentation

**Required Steps:**
1. Read the entire existing file first
2. Preserve existing structure and formatting
3. Add new sections logically (usually at the end or in relevant subsections)
4. Update any cross-references if content is moved
5. Maintain consistency with terminology from other docs

### Documentation Quality Standards

**Required Elements:**
- Clear headings with hierarchy (##, ###, ####)
- Use bullet points for lists
- Tables for comparative data or specifications
- Code blocks for technical specifications
- Cross-references to related documents

**Example Format:**
```markdown
# Feature Name

## Overview
Brief description of the feature and its purpose in Cosmic Kombat.

## Design Rationale
Why this feature exists and how it supports core differentiators.

## Technical Requirements
Specific implementation details (if applicable).

## Dependencies
What other systems/features this relies on.

## References
- [Related Doc 1](path/to/doc.md)
- [Related Doc 2](path/to/doc.md)
```

---

## Documentation Standards

### Markdown Style Guide

**Headers:**
- `#` = Document Title (one per file)
- `##` = Major Sections
- `###` = Subsections
- `####` = Minor Subsections (use sparingly)

**Lists:**
- Use `-` for unordered lists (not `*`)
- Use `1.`, `2.`, etc. for ordered lists
- Indent sub-items with 4 spaces

**Emphasis:**
- **Bold** (`**text**`) for important terms, feature names, critical priorities
- *Italic* (`*text*`) for emphasis (use sparingly)
- `Code` (`` `text` ``) for technical terms, file names, commands

**Links:**
- Use relative paths: `[Training Mode](../content/training-mode.md)`
- Use descriptive link text: `[See the combat system specification](../core-mechanics/combat-system.md)`

### Content Organization Principles

1. **Top-Down Structure**: Start with overview, then details
2. **Progressive Disclosure**: Basic info first, advanced info later
3. **Cross-Reference Liberally**: Link to related documents frequently
4. **Avoid Duplication**: Reference other docs instead of repeating content
5. **Update Related Docs**: If you change one doc, check if related docs need updates

### Domain Alignment

**Every piece of documentation should clearly belong to one of the 5 domains:**

| Domain | Focus Area | Key Files |
|--------|-----------|-----------|
| 1 - Gameplay | Mechanics, balance, combat | `core-mechanics/`, `DOMAIN_1_TODO_LIST.md` |
| 2 - Technical | Architecture, networking, tools | `technical-specs/`, `DOMAIN_2_TODO_LIST.md` |
| 3 - Content | Art, animation, audio, UI | `DOMAIN_3_TODO_LIST.md` (no folder yet - gap!) |
| 4 - Player Experience | Training, tutorials, modes | `content/`, `DOMAIN_4_TODO_LIST.md` |
| 5 - Live Ops | Monetization, matchmaking, community | `business/`, `post-launch/`, `DOMAIN_5_TODO_LIST.md` |

**If creating new documentation:**
- Determine which domain it belongs to
- Place it in the appropriate folder (create folder if needed)
- Update the domain's TODO list if it addresses a gap

---

## Architecture & Technical Decisions

### Core Technical Stack

From `/technical-specs/architecture.md`:

1. **Engine**: Unreal Engine 5 (custom modifications for fighting game mechanics)
2. **Networking**: GGPO rollback netcode (industry standard for competitive fighting games)
3. **Character System**: Component-based with inheritance for tier behaviors
4. **Physics**: Modified UE5 Chaos engine with deterministic calculations
5. **Input Handling**: Buffer-based system with configurable timing windows

### Architectural Principles

From `ARCHITECTURE_FEATURE_ANALYSIS.md`:

1. **Modular, Component-Based Architecture**: Clear separation of concerns
2. **Event-Driven Communication**: Minimize coupling between systems
3. **Data-Driven Design**: All balancing parameters externalized (JSON/YAML)
4. **Deterministic Gameplay**: Identical results across platforms (critical for competitive play)
5. **Performance First**: Locked 60 FPS, <8ms rollback, <4 frame input latency

### Design Philosophy

1. **Player-Friendly**: Transparent monetization, no pay-to-win, accessibility features
2. **Competitive Integrity**: Perfect balance across tiers despite power differences
3. **Learning-Focused**: Best-in-class training mode to reduce learning curve
4. **Spectacle & Identity**: Visual differentiation of tiers through procedural VFX
5. **Community-Driven**: Replay sharing, spectator mode, tournament support

---

## Current Priorities

### Critical Gaps (from ARCHITECTURE_FEATURE_ANALYSIS.md)

**🔴 HIGH RISK - Must Address Immediately:**

1. **Character-Specific Content** (Domain 1)
   - **Issue**: No character specifications exist
   - **Impact**: Cannot prototype or implement characters
   - **Action**: Create character specification template (see `DOMAIN_1_TODO_LIST.md` → Action 1)

2. **Visual Identity** (Domain 3)
   - **Issue**: No art style guide or visual direction defined
   - **Impact**: Blocking all art production
   - **Action**: Create comprehensive art style guide with tier visual differentiation

**🟡 MEDIUM RISK - Address in Vertical Slice:**

3. **Game Modes Documentation** (Domain 4)
   - **Issue**: Single-player content underspecified
   - **Impact**: Cannot plan progression or arcade mode
   - **Action**: Document all game modes with flow diagrams

4. **Networking Details** (Domain 2)
   - **Issue**: GGPO integration details missing
   - **Impact**: Cannot prototype online features
   - **Action**: Create technical design doc for rollback netcode

5. **Matchmaking & Ranking** (Domain 5)
   - **Issue**: Algorithm and systems not designed
   - **Impact**: Online retention will suffer
   - **Action**: Design MMR system and matchmaking parameters

### 5 Immediate Next Actions

From `ARCHITECTURE_FEATURE_ANALYSIS.md` → Part 3:

| Priority | Action | Owner | Timeline | Status |
|----------|--------|-------|----------|--------|
| 1 | Define Core Character Specification Template | Game Design Lead | Week 1 | 🔴 Not Started |
| 2 | Establish Visual Identity & Create Style Guide | Art Director | Weeks 1-2 | 🔴 Not Started |
| 3 | Implement Vertical Slice Prototype | Technical Lead | Weeks 2-8 | 🔴 Not Started |
| 4 | Design and Document Core Game Modes | Game Designer | Weeks 3-4 | 🔴 Not Started |
| 5 | Set Up Development Infrastructure & Pipelines | Tools Engineer | Weeks 1-3 | 🔴 Not Started |

### Domain-Specific Priorities

**Domain 1 (Gameplay):** Define universal mechanics, tier modifiers, damage scaling
**Domain 2 (Technical):** Data schemas, event system API, performance budgets
**Domain 3 (Content):** Art style guide, animation system, VFX categories
**Domain 4 (Player Experience):** Tutorial flow, learning curve mapping, FTUE design
**Domain 5 (Live Ops):** Matchmaking algorithm, battle pass pipeline, community tools

---

## Common Tasks & How to Execute Them

### Task 1: Adding a New Character Specification

**When:** Domain 1 work, character roster expansion

**Steps:**
1. Check if character spec template exists (it doesn't yet - see Priority 1)
2. Wait for template creation OR create template using guidance from `DOMAIN_1_TODO_LIST.md`
3. Create new file: `/characters/[character-name].md`
4. Include required sections:
   - Character overview (name, tier, archetype)
   - Base statistics (health, weight, speed)
   - Universal moves (light, medium, heavy attacks)
   - Special moves (inputs, frame data, properties)
   - Ultimate attack
   - Tier-specific modifiers
   - Playstyle description
   - Lore/backstory
5. Update character roster documentation (if it exists)

### Task 2: Documenting a New Game System

**When:** New mechanic, feature, or system is designed

**Steps:**
1. Determine which domain the system belongs to (1-5)
2. Check if similar documentation exists
3. Choose appropriate folder based on domain:
   - Domain 1 → `/core-mechanics/`
   - Domain 2 → `/technical-specs/`
   - Domain 3 → Create `/art-pipeline/` or similar
   - Domain 4 → `/content/` (training-related) or create `/game-modes/`
   - Domain 5 → `/business/` or `/post-launch/`
4. Create file: `/folder/[system-name].md`
5. Use standard documentation format (see [Documentation Quality Standards](#documentation-quality-standards))
6. Cross-reference from relevant TODO list
7. Update README.md if it's a major system

### Task 3: Updating the Architecture Analysis

**When:** Major strategic decisions, roadmap changes, new features identified

**Steps:**
1. Read entire `ARCHITECTURE_FEATURE_ANALYSIS.md` first
2. Identify which section needs updating:
   - Part 1: Domain analysis (1.1-1.4)
   - Part 2: High-impact features
   - Part 3: Immediate next actions
   - Part 4: Development roadmap
   - Part 5-8: Resources, risks, success criteria
3. Make changes while preserving structure
4. Update version number and date at top of document
5. Update relevant domain TODO lists if new gaps are identified

### Task 4: Creating a New Domain TODO List Item

**When:** New task identified for a specific domain

**Steps:**
1. Identify which domain (1-5)
2. Open corresponding `DOMAIN_*_TODO_LIST.md`
3. Review existing structure and numbering
4. Add new item in appropriate category
5. Include:
   - **Information Needed:** What specs/data are required
   - **Definition of Done:** Clear completion criteria
   - Optional: Dependencies, priority level, assignee
6. Update priority matrix if it's critical path

### Task 5: Expanding Training Mode Documentation

**When:** Adding new training features or specifications

**Steps:**
1. Review existing training docs:
   - `/content/training-index.md` (overview)
   - `/content/training-mode.md` (general features)
   - `/content/frame-data.md` (frame data system)
   - `/content/input-buffer.md` (input system)
   - `/content/analytics-dashboard.md` (analytics)
2. Determine if you're:
   - **Expanding existing feature** → Edit relevant file
   - **Adding new feature** → Create new file in `/content/`
3. Update `/content/training-index.md` with new feature link
4. Cross-reference from `ARCHITECTURE_FEATURE_ANALYSIS.md` → Feature 2 (Frame Perfect Training Laboratory)
5. Update `DOMAIN_4_TODO_LIST.md` if implementation tasks are needed

### Task 6: Documenting Technical Implementation Details

**When:** Converting design specs into technical requirements

**Steps:**
1. Read design specification first (e.g., from `/core-mechanics/`)
2. Create corresponding technical doc in `/technical-specs/`
3. Include:
   - System architecture diagram (ASCII or reference to external diagram)
   - Data structures and schemas (JSON/YAML examples)
   - API specifications (function signatures, events)
   - Performance requirements (frame budgets, memory limits)
   - Dependencies on other systems
   - Testing and validation criteria
4. Cross-reference design doc
5. Update `DOMAIN_2_TODO_LIST.md` with implementation tasks

### Task 7: Addressing a Gap from Architecture Analysis

**When:** Working on critical gaps identified in ARCHITECTURE_FEATURE_ANALYSIS.md

**Steps:**
1. Locate the gap in `ARCHITECTURE_FEATURE_ANALYSIS.md` (Part 1, sections 1.2)
2. Find corresponding TODO in `DOMAIN_*_TODO_LIST.md`
3. Create documentation to address the gap
4. Update the relevant domain analysis in ARCHITECTURE_FEATURE_ANALYSIS.md:
   - Change ❌ **Missing** → ✅ **Complete** or ⚠️ **Partial**
   - Update risk assessment if applicable
5. Mark TODO item as complete or in-progress
6. Commit with message referencing the gap addressed

### Task 8: Preparing for a Milestone

**When:** Approaching Vertical Slice, Alpha, Beta, or Launch milestones

**Steps:**
1. Review milestone requirements in `ARCHITECTURE_FEATURE_ANALYSIS.md` → Part 4
2. Check success criteria in Part 7
3. Review all DOMAIN TODO lists for milestone-critical items
4. Create milestone tracking document (e.g., `MILESTONE_VERTICAL_SLICE.md`)
5. Include:
   - Checklist of required deliverables
   - Status of each deliverable
   - Blockers and risks
   - Timeline and owners
6. Update weekly based on progress

---

## Best Practices for AI Assistants

### When Asked to Analyze the Codebase

**Remember:**
- This is a **design documentation repository**, not a code repository
- There is no actual game implementation yet (pre-production phase)
- Focus on design specs, architecture plans, and strategic documents

### When Asked to Implement Features

**Clarify:**
- Are they asking for **design documentation** of the feature?
- Or are they asking for **implementation planning** (technical specs)?
- This repo contains NO CODE - do not attempt to write game code

### When Asked to Update Documentation

**Always:**
1. Read existing documentation first (use Read tool)
2. Check ARCHITECTURE_FEATURE_ANALYSIS.md for strategic context
3. Review domain TODO lists for priorities
4. Maintain consistency with existing style and terminology
5. Cross-reference related documents

### When Asked About Project Status

**Reference:**
- Overall: 40-50% design documentation complete (pre-production)
- Domain 1 (Gameplay): ~30% complete, HIGH RISK
- Domain 2 (Technical): ~50% complete, MEDIUM RISK
- Domain 3 (Content): ~5% complete, HIGH RISK (critical blocker)
- Domain 4 (Player Experience): ~35% complete, MEDIUM RISK
- Domain 5 (Live Ops): ~25% complete, MEDIUM RISK

### When Asked for Recommendations

**Prioritize:**
1. Critical gaps (Domain 1 & 3) that block vertical slice
2. Immediate next actions from ARCHITECTURE_FEATURE_ANALYSIS.md Part 3
3. High-impact features from Part 2
4. Domain-specific todos in priority order

### When Uncertain

**Ask:**
- "Are you asking about design documentation or implementation?"
- "Which domain does this relate to? (Gameplay/Technical/Content/Player Experience/Live Ops)"
- "Is this for the vertical slice, alpha, or full release?"
- "Should I check ARCHITECTURE_FEATURE_ANALYSIS.md for strategic alignment first?"

---

## Quick Reference

### Most Important Files

| File | Purpose | Update Frequency |
|------|---------|------------------|
| `ARCHITECTURE_FEATURE_ANALYSIS.md` | Strategic plan, roadmap, gap analysis | Monthly or on major decisions |
| `DOMAIN_*_TODO_LIST.md` | Actionable task lists by domain | Weekly as tasks progress |
| `README.md` | Project intro and navigation | When major sections added |
| `core-mechanics/combat-system.md` | Core gameplay specification | When mechanics finalized |
| `technical-specs/architecture.md` | Technical foundation | When tech decisions made |

### Key Contacts (Roles, not names)

- **Game Director / Design Lead**: Owns gameplay vision, character specs, balance
- **Technical Lead**: Owns architecture, engine integration, performance
- **Art Director**: Owns visual identity, style guide, tier differentiation
- **Producer**: Owns timeline, resources, milestone tracking

### External References

- **VSBattles Wiki**: https://vsbattles.fandom.com/wiki/Tiering_System (source for tier system)
- **GGPO**: https://www.ggpo.net/ (rollback netcode technology)
- **Unreal Engine 5**: https://www.unrealengine.com/ (game engine)

---

## Document Maintenance

### When to Update This File

- Major changes to repository structure
- New domain folders created
- Workflow or conventions change
- New critical documentation added
- Milestone transitions (Vertical Slice → Alpha → Beta → Launch)

### Version History

- **v1.0** (2025-11-14): Initial creation, comprehensive analysis of existing docs

---

## Appendix: Domain Health Dashboard

Quick visual reference for domain completeness and risk:

```
DOMAIN 1: GAMEPLAY SYSTEMS
├─ Completeness: ███░░░░░░░ 30%
├─ Risk Level:   🔴 HIGH RISK
├─ Priority:     🔥 CRITICAL for Vertical Slice
└─ Next Action:  Define character specification template

DOMAIN 2: TECHNICAL INFRASTRUCTURE
├─ Completeness: █████░░░░░ 50%
├─ Risk Level:   🟡 MEDIUM RISK
├─ Priority:     🔥 CRITICAL for Vertical Slice
└─ Next Action:  Define data schemas and event system API

DOMAIN 3: CONTENT SYSTEMS
├─ Completeness: █░░░░░░░░░ 5%
├─ Risk Level:   🔴 HIGH RISK
├─ Priority:     🔥 CRITICAL for Vertical Slice (BLOCKER)
└─ Next Action:  Create comprehensive art style guide

DOMAIN 4: PLAYER EXPERIENCE
├─ Completeness: ███░░░░░░░ 35%
├─ Risk Level:   🟡 MEDIUM RISK
├─ Priority:     ⚠️  Important for Vertical Slice
└─ Next Action:  Design tutorial and onboarding flow

DOMAIN 5: LIVE OPERATIONS
├─ Completeness: ██░░░░░░░░ 25%
├─ Risk Level:   🟡 MEDIUM RISK
├─ Priority:     ✓ Nice-to-Have for Vertical Slice
└─ Next Action:  Design matchmaking algorithm
```

---

**END OF CLAUDE.md**

*This document is a living guide. Update it as the project evolves. When in doubt, read ARCHITECTURE_FEATURE_ANALYSIS.md for strategic context.*
