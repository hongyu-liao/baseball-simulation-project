# Product Backlog: Baseball Monte Carlo Simulation

| ID    | Type    | Description                                                                                                 | Priority | Status      | Notes                                         |
| :---- | :------ | :---------------------------------------------------------------------------------------------------------- | :------- | :---------- | :-------------------------------------------- |
| PB-001 | Feature | Simulate a single 9-inning baseball game between two teams.                                                 | High     | Done        | Core game logic implemented.                  |
| PB-002 | Feature | Load batter statistics (AVG, OBP, SLG) from a CSV file for each team.                                       | High     | Done        | Pandas used for CSV reading.                  |
| PB-003 | Feature | Load pitcher statistics (ERA) from a CSV file for each team's starting pitcher.                               | High     | Done        | Pandas used for CSV reading.                  |
| PB-004 | Feature | At-bat outcomes (out, SO, walk, hit types) are determined probabilistically based on player/pitcher stats.    | High     | Done        | Simplified probability model.                 |
| PB-005 | Feature | Implement Monte Carlo simulation to run N (e.g., 1000) games.                                               | High     | Done        | Loop implemented.                             |
| PB-006 | Feature | Calculate and output win percentages for each team after Monte Carlo simulation.                            | High     | Done        | Basic win/loss tracking.                      |
| PB-007 | Task    | Handle missing or malformed data in CSVs by assigning default stats.                                      | Medium   | Done        | Implemented via try-except blocks.            |
| PB-008 | Feature | Implement more realistic baserunner advancement logic.                                                      | Medium   | To Do       | Current logic is very simplified.             |
| PB-009 | Feature | Incorporate more detailed player statistics (e.g., K%, BB%, ISO) for more accurate at-bat outcomes.          | Medium   | To Do       | Would improve simulation realism.             |
| PB-010 | Feature | Model pitcher fatigue and bullpen usage.                                                                    | Low      | To Do       | Currently uses one pitcher per team always.   |
| PB-011 | Feature | Implement more diverse out types (flyout, groundout based on player tendencies).                            | Low      | To Do       | Currently generic "out".                      |
| PB-012 | Task    | Add comments and clean up the Python code for better readability.                                           | Medium   | In Progress | Basic comments exist.                         |
| PB-013 | Task    | Create/Finalize all required project management artifacts.                                                  | High     | In Progress | This task.                                    |
| PB-014 | Bug     | (Hypothetical) Simulation occasionally results in an invalid game state (e.g. negative outs).                | High     | To Do       | If found during more extensive testing.       |
| PB-015 | Feature | Allow user to specify team data files as input instead of hardcoding.                                       | Medium   | To Do       |                                               |