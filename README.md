# ricochet-robots

### Functional Requirements

#### User Interface and Experience

1. **Lobby Creation and Management:**

   - Users can create and join game lobbies with invite links.
   - **Only the lobby creator can manage the lobby settings**.

2. **Game Board Initialization:**

   - **The game board arrangement remains the same for each game to maintain consistency and simplify initial development**.

3. **Chip Selection:**

   - Randomly select one of the 17 chips at the beginning of each round, ensuring **chips are not repeated until all have been used**.

4. **Robot Movement and Interaction:**

   - Players can click on robots to visualize potential moves.
   - Highlight potential destinations for the selected robot.
   - Update move counter with each robot move.
   - **Players can reset both the board to its initial state and their move counters**.

5. **Solution Submission and Timer:**

   - Players submit their solution upon matching the robot to the chip's position.
   - A countdown timer starts upon the first solution submission.
   - Subsequent solutions that have a lower move count can reset the timer.

6. **Optimal Solution Display and Ranking:**

   - Display the sequence of moves for the winning solution at the end of each round.
   - **At the end of the game, display a ranking of players, highlighting the winner**.

7. **Score Tracking:**
   - Track the number of chips won by each player throughout the game.

#### Game Logic and Data Management

1. **Board Arrangement Logic:**

   - **The board setup remains constant for initial versions; permutation and flipping will be introduced as future features**.

2. **Multiplayer Synchronization:**

   - **Synchronize game state only at the beginning and upon someone winning a round**. This ensures that players do not see each other's moves during a round.

3. **Timer and Round Management:**
   - **Only the lobby creator can pause the game**, adding control over game flow.

### Business Rules

1. **Chip Selection Mechanism:**

   - Ensure that each chip is selected only once per game cycle, until all chips have been used.

2. **Lobby Management:**

   - Restrict lobby management capabilities (such as starting a game, pausing, and inviting players) to the lobby creator.

3. **Gameplay Privacy:**

   - Players work on their solutions independently; their interim board states and moves are not visible to others until a solution is submitted.

4. **End-of-Game Ranking:**
   - Provide a summary of player rankings at the end of the game, with a special highlight for the overall winner based on the number of chips collected.
