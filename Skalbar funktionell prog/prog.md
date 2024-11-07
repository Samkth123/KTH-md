### Key Functions

The code primarily revolves around functions for creating entities and managing game state.

#### Entity Creation Functions:

1. **`create-hero`**:
    
    - Creates a hero with a given name, and optionally overrides the default values (like `damage-taken`).
2. **`create-card`**:
    
    - Similar to `create-hero`, but for creating cards, with a name and optional override values.
3. **`create-minion`**:
    
    - Creates a minion with a given name and optional key-value overrides. This function also integrates with `get-definition` to retrieve specific minion definitions from elsewhere in the system.
4. **`create-empty-state`**:
    
    - Creates a default game state, potentially using provided hero definitions. If no heroes are provided, it defaults to two "Jaina Proudmoore" heroes.

#### State Manipulation:

1. **`add-minion-to-board`**:
    
    - Adds a minion to a player's board at a specified position. It also handles updating the positions of other minions if necessary.
2. **`add-card-to-deck`**, **`add-card-to-hand`**:
    
    - Adds a card (either by name or full card object) to a player's deck or hand.
3. **`create-game`**:
    
    - Initializes a game state with custom configurations like deck, hand, and minions, using the previously defined entities.

#### Entity Retrieval:

1. **`get-player`**:
    
    - Retrieves a player by their ID from the game state.
2. **`get-minions`**:
    
    - Retrieves the minions on the board for a given player or for both players.
3. **`get-heroes`**:
    
    - Retrieves all heroes in the game state.
4. **`get-minion`**:
    
    - Retrieves a specific minion by its ID.

#### Entity Updates and Removal:

1. **`replace-minion`**:
    
    - Replaces a minion with the same ID by a new minion.
2. **`update-minion`**:
    
    - Updates a minion's specific attributes (like `damage-taken`) using either a function or a direct value.
3. **`remove-minion`**:
    
    - Removes a minion from the game state by its ID.
4. **`remove-minions`**:
    
    - Removes multiple minions by their IDs from the game state.

### Testing and Assertions

Each of the functions is associated with a test function under the `:test` key. These tests ensure that the functions behave as expected:

- They check if the correct entities are created with the right attributes (e.g., creating heroes, cards, and minions).
- They verify that the game state can be manipulated correctly (e.g., adding cards to hands or decks, adding minions to boards, updating minions).
- They ensure that edge cases are handled, such as updating minions, removing minions, and checking player and game state consistency.

### Structure of Game State

The game state consists of several keys:

- **`:player-id-in-turn`**: Keeps track of whose turn it is.
- **`:players`**: A map of player IDs (`p1`, `p2`, etc.), with each player having their own deck, hand, minions, and hero.
- **`:counter`**: A counter for generating unique IDs.
- **`:minion-ids-summoned-this-turn`**: A list of minion IDs summoned during the current turn.


### Breakdown of Code

1. **`firestone.core`**:
    
    - **Business Logic**: This namespace contains most of the core gameplay mechanics:
        - `get-character`: Returns the character (hero or minion) by ID.
        - `get-health`: Calculates the health of a character based on the health definition and any damage taken.
        - `get-attack`: Retrieves the attack value for a given minion.
        - `sleepy?`: Checks if a minion is "sleepy" (presumably a state where the minion cannot attack).
        - `valid-attack?`: Checks whether an attack is valid, based on conditions such as whether the player is attacking an opponent, whether the minion is sleepy, whether it's the player's turn, etc.
2. **`firestone.core-api`**:
    
    - **Public API**: Provides a higher-level API for interacting with the game.
        - `end-turn`: Ends a player's turn and transitions the turn to the other player, with checks to ensure it's the correct player's turn.
3. **`firestone.definitions`**:
    
    - **Game Definitions**: Stores and retrieves game definitions (e.g., minion stats, hero stats, and abilities).
        - `add-definitions!`: Adds game definitions to an atom.
        - `get-definition`: Retrieves a game definition (minion, hero, card, etc.) by name.
4. **`firestone.definitions-loader`**:
    
    - **Loading Definitions**: This namespace is responsible for loading definitions, likely for heroes, minions, or cards, when they are needed.