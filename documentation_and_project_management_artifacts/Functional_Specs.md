# Functional Specifications: Baseball Monte Carlo Simulation

## 1. Overview

This document outlines the functional specifications for the Baseball Monte Carlo Simulation project. The primary goal is to simulate a large number of baseball games between two teams using player statistics loaded from CSV files and to predict overall win probabilities.

## 2. User Stories

* **US-001:** As a user, I want to simulate a single baseball game between two predefined teams (e.g., Cubs vs. White Sox) so that I can see a possible outcome and score.
* **US-002:** As a user, I want the simulation to use player batting statistics (AVG, OBP, SLG) from CSV files to influence at-bat outcomes so that the simulation reflects player abilities.
* **US-003:** As a user, I want the simulation to use pitcher statistics (ERA) from CSV files to influence at-bat outcomes so that pitcher quality is a factor.
* **US-004:** As a user, I want the simulation to run for a specified number of innings (e.g., 9 innings) to represent a standard game.
* **US-005:** As a user, I want to run a Monte Carlo simulation (e.g., 1000 games) so that I can obtain statistically relevant win probability predictions for each team.
* **US-006:** As a user, I want to see the final win percentages for each team after the Monte Carlo simulation is complete.
* **US-007:** As a developer, I want the simulation to handle basic game state (innings, outs, score, runners on base) so that game progression is logical.

## 3. Requirements

| ID    | Requirement Description                                                                    | User Story | Priority |
| :---- | :----------------------------------------------------------------------------------------- | :--------- | :------- |
| REQ-001 | The system shall simulate a baseball game inning by inning.                                | US-001     | High     |
| REQ-002 | Each at-bat outcome (out, strikeout, walk, single, double, triple, home run) shall be determined probabilistically. | US-001     | High     |
| REQ-003 | The system shall load batter data (Player Name, BA, OBP, SLG) from specified CSV files.    | US-002     | High     |
| REQ-004 | The system shall load pitcher data (Player Name, ERA) from specified CSV files.             | US-003     | High     |
| REQ-005 | Batter hit/on-base chances shall be influenced by their loaded statistics and the opposing pitcher's ERA (via control_factor, strikeout_bonus). | US-002, US-003 | High     |
| REQ-006 | The simulation shall track outs, with 3 outs ending a half-inning.                         | US-007     | High     |
| REQ-007 | The simulation shall track runners on bases and advance them based on at-bat outcomes (simplified logic). | US-007     | Medium   |
| REQ-008 | The simulation shall track and update the score for both teams.                            | US-007     | High     |
| REQ-009 | A standard game simulation shall run for 9 innings.                                        | US-004     | High     |
| REQ-010 | The system shall be capable of running a specified number of game simulations (e.g., 1000) in a batch (Monte Carlo). | US-005     | High     |
| REQ-011 | After completing the Monte Carlo simulation, the system shall output the win count and win percentage for each team. | US-006     | High     |
| REQ-012 | The system shall handle cases where data might be missing or non-numeric in CSV files by using default player/pitcher statistics. | N/A        | Medium   |

## 4. Acceptance Criteria

| ID    | Requirement ID | Acceptance Criterion                                                                                                                               |
| :---- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| AC-001 | REQ-001, REQ-009 | A single game simulation completes after 9 full innings (unless specific game-ending conditions like home team leading in bottom of 9th are met). |
| AC-002 | REQ-002        | At-bat outcomes are varied and reflect a reasonable distribution (e.g., not all strikeouts, not all home runs).                                  |
| AC-003 | REQ-003, REQ-004 | Player and Pitcher objects are successfully created with statistics loaded from the CSV files without error (or use defaults if data is invalid). |
| AC-004 | REQ-005        | Different pitchers (based on ERA) should demonstrably affect batter outcomes over a large number of simulations.                                     |
| AC-005 | REQ-006, REQ-007, REQ-008 | Game state (outs, score, bases) is updated correctly after each at-bat and half-inning.                                                    |
| AC-006 | REQ-010        | The system can execute 1000 simulations without crashing.                                                                                          |
| AC-007 | REQ-011        | The final output correctly displays the total wins and win percentage for each team based on the completed simulations.                              |
| AC-008 | REQ-012        | If CSV data is malformed for a player/pitcher, the simulation runs using default placeholder stats for that entity without crashing.                 |