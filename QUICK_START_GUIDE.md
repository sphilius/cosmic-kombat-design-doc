# Cosmic Kombat: Quick Start Guide (Solo Dev)

**Last Updated:** 2025-10-24
**Project Type:** Portfolio Project - Fighting Game
**Developer:** Solo
**Engine:** Godot 4.3+
**Style:** Stylized 2D (Guilty Gear + Mortal Kombat blend)

---

## 🎯 Project Overview

**Demo Scope:** 6 characters (2 low-tier, 2 mid-tier, 2 unlockable high-tier)
**Timeline:** 12-14 months (full-time) or 24-28 months (part-time)
**Budget:** $10,000-15,000 (art outsourcing)
**Platform:** PC-only (Windows 11)
**End Goal:** Portfolio piece + potential Steam release

---

## 📊 Key Documents

1. **GODOT_2D_SOLO_DEV_PIVOT.md** ⭐ READ THIS FIRST
   - Complete technical analysis of Godot vs UE5
   - Detailed solo dev roadmap
   - Budget breakdown
   - Art pipeline guidance

2. **STATUS_AND_NEXT_ACTIONS.md**
   - Current repository state
   - Critical decisions needed
   - Prioritized action items

3. **ARCHITECTURE_FEATURE_ANALYSIS.md**
   - Original team-based analysis
   - High-impact features
   - Full game vision (reference for scope)

4. **Core Game Design Documents:**
   - `core-mechanics/combat-system.md` - Dual health system
   - `core-mechanics/tier-system.md` - VSBattles tier scaling
   - `content/training-mode.md` - Training mode vision
   - `content/frame-data.md` - Frame visualization system

---

## 🚀 Next 30 Days Action Plan

### Week 1: Learn Godot & Setup
- [ ] Install Godot 4.3+ (https://godotengine.org)
- [ ] Complete official Godot 2D tutorial (10 hours)
- [ ] Set up project structure in Godot
- [ ] Join Godot Discord and fighting game dev communities
- [ ] Research sprite artists on ArtStation, Fiverr, Twitter

### Week 2: Core Prototype
- [ ] Build character controller (walk, dash, jump)
- [ ] Implement basic attack system
- [ ] Create hitbox/hurtbox collision system
- [ ] Build dual health system (percentage + health bar)
- [ ] Test with placeholder sprites (colored boxes)

### Week 3: Combat Mechanics
- [ ] Add frame data tracking system
- [ ] Implement hitstun and blockstun
- [ ] Add knockback physics (tier-based)
- [ ] Create blocking mechanic
- [ ] Test combat feel with 2 "box" characters

### Week 4: Character Spec & Art
- [ ] Define first 2 characters in complete detail
- [ ] Write character design briefs (visual descriptions)
- [ ] Commission concept art for Character 1 & 2 ($400-800)
- [ ] Find sprite artists and get quotes
- [ ] Implement full 5-move moveset for Character 1 (placeholder art)

**End of Month 1 Goal:** Playable prototype with 1 character fighting (placeholder art) + art production started

---

## 💰 Budget Breakdown

### Minimum Viable (2-Character Demo)
**Total: $2,000-4,000**
- 2 character sprite sheets: $2,000-4,000
- Music/SFX (royalty-free): $50-200
- Timeline: 6-8 months

### Recommended (6-Character Demo)
**Total: $10,000-15,000**
- 6 character concept art: $1,200-2,400
- 6 character sprite sheets: $6,000-12,000
- VFX sprites: $1,200-3,000
- 3-4 stage backgrounds: $900-2,400
- Music/SFX: $300-1,200
- Timeline: 12-14 months

### Full Launch (12 Characters)
**Total: $18,000-30,000**
- Demo costs + 6 more characters + marketing
- Timeline: 24-26 months

---

## 🎨 Art Style Guidelines

### Visual Direction: Guilty Gear + Mortal Kombat Blend

**From Guilty Gear:**
- Hand-drawn anime aesthetic
- Cel-shaded look
- Exaggerated animations with smear frames
- Vibrant colors
- High contrast
- Dynamic poses
- Stylized proportions

**From Mortal Kombat:**
- Realistic anatomy and detail
- Gritty textures
- Dark/moody atmosphere
- Weighty, impactful hits
- Detailed muscle definition
- Visceral combat feel

**Your Blend:**
- Base: Hand-drawn 2D sprites (anime style)
- Detail: Higher realism in anatomy/shading
- Colors: Vibrant but with darker tones
- Animation: Exaggerated but weighty
- VFX: Flashy anime effects with heavy impact

**Reference Games:**
- Guilty Gear Strive (animation and style)
- Blazblue (high-detail sprites)
- Skullgirls (hand-drawn animation quality)
- Mortal Kombat 11 (impact and weight)

---

## 🛠️ Technical Stack

### Engine & Tools
- **Godot 4.3+** (free, open source)
- **GDScript** (primary programming language)
- **Godot Rollback Netcode Addon** (for online play)
- **JSON** (for character data)

### Art Tools (If Making Art)
- **Krita** (free) or **Aseprite** ($20) for sprites
- **Blender** (free) if using 3D-to-2D pipeline
- **Audacity** (free) for audio editing

### External Services
- **Sprite Commission:** Fiverr, ArtStation, Twitter artists
- **Music:** Incompetech.com, Purple Planet (royalty-free)
- **SFX:** Freesound.org, OpenGameArt.org

---

## 📋 Phase Breakdown

### Phase 1: Pre-Production (Months 1-2)
**Goal:** Core mechanics prototype with placeholder art
- Learn Godot
- Build combat system
- Dual health system
- 1 character with full moveset

### Phase 2: Vertical Slice (Months 3-8)
**Goal:** 2-character polished demo
- Commission art for 2 characters
- Training mode implementation
- Local versus mode
- 2 stages
- Full UI

**Deliverable:** Playable 2-character demo for portfolio

### Phase 3: Mid-Tier Expansion (Months 9-11)
**Goal:** Add 2 mid-tier characters
- Characters 3 & 4 (Tier 8)
- Tier system validation
- 1 additional stage

**Deliverable:** 4-character demo

### Phase 4: High-Tier & Arcade (Months 12-14)
**Goal:** Complete 6-character demo
- Characters 5 & 6 (Tier 5, unlockable)
- Unlock system
- Arcade mode
- Final polish

**Deliverable:** 6-character demo ready for portfolio/Steam

### Phase 5: Full Roster (Months 15-26)
**Goal:** 12-character full game
- 6 additional characters
- Online multiplayer
- Additional game modes
- Steam launch

---

## ✅ Success Criteria

### 2-Character Vertical Slice (Month 8)
- [ ] 2 characters fun to play for 30+ minutes
- [ ] Dual health system feels unique
- [ ] Training mode has frame data display
- [ ] 60 FPS performance locked
- [ ] Playtesters say "I want more characters"

### 6-Character Demo (Month 14)
- [ ] 6 characters, distinct playstyles
- [ ] Tier system feels meaningful
- [ ] Unlock system functional
- [ ] Arcade mode playable
- [ ] Polished enough for portfolio/itch.io release

### Full Launch (Month 26)
- [ ] 12 balanced characters
- [ ] Online multiplayer with rollback netcode
- [ ] Multiple game modes
- [ ] Steam release
- [ ] 100+ wishlists before launch

---

## 🚨 Common Pitfalls to Avoid

1. **Scope Creep**
   - Stick to 6 characters for demo
   - Don't add features until core is solid
   - Hard feature lock at each milestone

2. **Art Perfectionism**
   - Get playable mechanics first (placeholder art is fine)
   - Commission art once mechanics are proven
   - Don't remake art multiple times

3. **Trying to Do Everything**
   - Outsource art if budget allows
   - Focus on programming and design
   - Don't try to master 3D modeling, animation, music, etc.

4. **Burnout**
   - Take regular breaks (1 week off every 3 months)
   - Set realistic weekly hour goals
   - Join communities for support

5. **Comparing to AAA**
   - You're one person, not a 50-person team
   - Focus on your unique strengths (training mode!)
   - Embrace indie aesthetic

---

## 📚 Essential Resources

### Learning Godot
- Official Docs: https://docs.godotengine.org
- GDQuest Tutorials: https://www.gdquest.com/
- YouTube: "Godot 4 tutorial" + "godot fighting game"

### Fighting Game Development
- Godot Rollback Netcode: https://github.com/FlutterTal/godot-rollback-netcode
- Fighting Game Glossary: infil.net
- Frame data concepts: YouTube "frame data explained"

### Communities
- Godot Discord: discord.gg/godotengine
- r/godot: reddit.com/r/godot
- r/fightinggames: reddit.com/r/fightinggames
- Fighting Game Developers Discord (search on Discord)

### Art & Assets
- Commission art: Fiverr, ArtStation, Twitter #commissions
- Royalty-free music: incompetech.com, purple-planet.com
- SFX: freesound.org, opengameart.org

---

## 💡 Key Insights

### Why Godot 2D > UE5 3D for Solo
- 50% faster character production
- Simpler technical implementation
- Free and lightweight
- Faster iteration
- Better for 2D fighting games
- Proven by indie successes

### Why This Project is Feasible
- 2D fighting game is manageable scope for solo
- Can outsource art for $10-15k
- Training mode is your differentiator
- Dual health system is unique hook
- 6 characters is enough for solid demo
- Godot makes it technically achievable

### Critical Success Factors
1. **Focus on feel first** - Combat must feel good with boxes
2. **Outsource art** - Don't try to be artist + programmer
3. **Training mode is your strength** - Make it best-in-class
4. **Start small** - 2 characters first, then expand
5. **Community feedback** - Get playtesters from FGC early

---

## 🎯 Your First Week Checklist

- [ ] Read GODOT_2D_SOLO_DEV_PIVOT.md (full technical analysis)
- [ ] Install Godot 4.3+
- [ ] Complete official Godot 2D tutorial
- [ ] Set up Git repository for project
- [ ] Join Godot and fighting game dev communities
- [ ] Create character specification template
- [ ] Define first 2 characters (Tier 11) in detail
- [ ] Research sprite artists and get quotes
- [ ] Start building character controller prototype

---

## 📞 Questions? Next Steps?

1. **Read the full technical analysis:** GODOT_2D_SOLO_DEV_PIVOT.md
2. **Start learning Godot today:** https://godotengine.org
3. **Join communities for support**
4. **Build your first prototype this week**

You've got a solid plan. Time to start building! 🎮⚔️

---

**Remember:** Many successful indie fighting games were made by solo devs or tiny teams. You can do this. Focus on making one thing exceptional (your training mode), keep scope tight, and iterate based on feedback.

Good luck!
