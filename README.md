# UE4 Multiplayer Prototype

A technical prototype focused on **Server-Client communication** and **Gameplay Framework** basics in Unreal Engine 4.

Technical Implementation
This project was built to explore the fundamentals of networking in UE4. I focused on understanding how the server validates actions and how data is synchronized across clients.

Key Features:
- **Server-Authoritative Logic:** Implemented validation for weapon pickups and player actions to ensure game integrity.
- **Variable Replication:** Used `Replicated` variables to synchronize health, ammunition, and player states.
- **Remote Procedure Calls (RPCs):** Used `Server` and `Multicast` events for networked gameplay triggers (e.g., firing effects, spawning items).
- **UMG UI Logic:** Created a responsive HUD that updates based on replicated player data.

Gameplay Mechanics
- **Weapon System:** Players can interact with and equip weapons that are synced via the server.
- **Multiplayer Testing:** Successfully tested with multiple client instances to verify synchronization and authority.

Visuals & Blueprints
### 1. Server-Authoritative Spawning
This logic ensures that only the server has the authority to spawn loot from a predefined list. It prevents item duplication and ensures all clients see the same spawned actor.
<img width="1051" height="534" alt="image" src="https://github.com/user-attachments/assets/75bc4771-bc68-4f6e-9b66-f66ac6d09b02" />
)

### 2. Interaction & Casting
Using Overlap Events to detect players and verify their class via Casting before triggering the pickup logic.
(<img width="1301" height="645" alt="image" src="https://github.com/user-attachments/assets/63e39b77-7ccd-44ca-920d-8612bf52dc61" />
)
