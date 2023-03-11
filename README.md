## DmWithGameState
### Introduction

This prompt was designed as a starting point for running a Dungeons and Dragons campaign using Chat GPT as the Dungeon Master. Older iterations had a few key issues which is solved by this current version:

- PCs and NPCs were not consistently tracked or added into the world by the DM.
- - This was solved by introducing the **game_state** section of the prompt which stores the current values for entities within the game.
- - This was further advanced by introducing the **commands** section of the prompt which are essentially functions to teach the DM how to consistently handle storing and recalling the game state.

- While the model was keeping track of PCs & NPCs added into the game, it's description of those characters would get odd over time.
- - This was solved by modifying the **game_state** to include **tags** for each entity, which the DM is able to update as the game moves on as needed.
- - This provides enough scoped context for each entity that it dramatically improves the flavor text and dialogue accuracy for each entity.

- If a quest or objective was given by the DM, other NPCs would have knowledge of this new quest.
- - This was partially solved by adding the **objectives** property into the game state and associating a given npc to the objective.
- - Likely still adjustmenets needed to enforce this boundary, but it does drastically improve this issue.

- During combat, there was no clarity for the DM as far as initiative, health pools, which characters are involved in combat, etc.
- - This was solved by introducing the **encounters** section into the game state and associating a list of entities to each enounter, allowing for initiative rolls and an overall scope for the encounter.


