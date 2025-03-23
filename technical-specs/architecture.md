# Technical Architecture

## Core Architecture

- Implement a modular, component-based architecture with clear separation of concerns
- Use event-driven communication between systems to minimize coupling
- Adopt data-driven design for all balancing parameters

## Key Technical Decisions

1. **Engine**: Unreal Engine 5 with custom modifications for fighting game needs
2. **Networking**: Custom implementation of GGPO rollback netcode
3. **Character System**: Component-based with inheritance for tier-based behaviors
4. **Physics**: Modified UE5 Chaos with deterministic calculations
5. **Input Handling**: Buffer-based system with configurable timing windows