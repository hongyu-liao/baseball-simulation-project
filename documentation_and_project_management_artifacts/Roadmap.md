# Product Roadmap: Baseball Monte Carlo Simulation

## Phase 1: Core Simulation Engine (Completed: ~May 20, 2025)

* **M1.1: Basic Game Logic:**
    * Define Player, Pitcher, and GameState classes.
    * Implement logic for a single at-bat with probabilistic outcomes.
    * Implement logic for simulating a half-inning (3 outs).
    * Implement logic for simulating a full 9-inning game.
    * Track basic game state (score, outs, inning).
* **M1.2: Initial Data Integration (CSV):**
    * Functionality to load player batting stats (BA, OBP, SLG) from CSV.
    * Functionality to load pitcher stats (ERA) from CSV.
    * Basic error handling for data loading (use defaults).

## Phase 2: Monte Carlo Simulation & Output (Completed: ~May 21, 2025)

* **M2.1: Batch Simulation:**
    * Implement functionality to run N (e.g., 1000) game simulations.
    * Aggregate win/loss results across all simulations.
* **M2.2: Results Output:**
    * Calculate and display win percentages for each team.
    * (Optional) Display average scores.

## Phase 3: Documentation & Repository Finalization (Target: By Assignment Deadline)

* **M3.1: Project Management Artifacts:**
    * Complete Functional Specifications.
    * Complete Work Breakdown Structure.
    * Complete Product Backlog (initial set of features).
    * Maintain Status Log and Activity List.
    * Finalize Roadmap (this document).
* **M3.2: Code Documentation:**
    * Add comments to Python code for clarity.
* **M3.3: Repository Structure:**
    * Ensure all files are in the correct directories as per assignment guidelines.
    * Create/update README.md for the root directory.
* **M3.4: Submission Preparation:**
    * Prepare comments on AI collaboration and peer review insights.

## Future Enhancements (Beyond Current Scope/Assignment)

* **FEAT-001:** More detailed probabilistic models for at-bat outcomes (using K%, BB%, ISO, etc.).
* **FEAT-002:** Realistic baserunning logic.
* **FEAT-003:** Pitcher fatigue and bullpen management.
* **FEAT-004:** Specific out types (flyout, groundout, etc.) based on player tendencies.
* **FEAT-005:** User interface for easier input and visualization of results.
* **FEAT-006:** Incorporation of fielding statistics and defensive plays.
* **FEAT-007:** Dynamic schedule loading for season simulation.