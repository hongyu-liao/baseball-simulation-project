# Work Breakdown Structure (WBS) - Baseball Monte Carlo Simulation

1.  **Project Initialization & Planning**
    1.1. Define Project Scope and Objectives
    1.2. Create GitHub Repository & Initial Structure
    1.3. Develop Initial Project Management Artifacts
        1.3.1. Functional Specifications
        1.3.2. Work Breakdown Structure (this document)
        1.3.3. Product Backlog
        1.3.4. Status Log (initial setup)
        1.3.5. Activity List (initial setup)
        1.3.6. Roadmap

2.  **Data Acquisition and Preparation**
    2.1. Identify Required Player Statistics (Batting: BA, OBP, SLG; Pitching: ERA)
    2.2. Locate and Confirm Source Data (CSV files from `pitch-by-pitch-pro` repo's `data/clean/` directory)
    2.3. Develop Data Loading Module (Python)
        2.3.1. Implement CSV reading functionality (using Pandas)
        2.3.2. Implement parsing for Batter statistics
        2.3.3. Implement parsing for Pitcher statistics
        2.3.4. Implement error handling for missing/malformed data (use defaults)
    2.4. Place prepared data files into `/prepared_data/` directory (Manual copy for this assignment)

3.  **Simulation Core Logic Development (Python)**
    3.1. Define Player Class
        3.1.1. Attributes: name, avg, obp, slg, derived probabilities (hit_chance, etc.)
    3.2. Define Pitcher Class
        3.2.1. Attributes: name, era, derived factors (control_factor, etc.)
    3.3. Define GameState Class
        3.3.1. Attributes: inning, outs, bases, scores, current batter indices
        3.3.2. Methods: record_out, advance_runners, new_inning_half
    3.4. Implement At-Bat Simulation Logic
        3.4.1. Calculate outcome probabilities based on batter/pitcher stats
        3.4.2. Determine at-bat result (out, SO, walk, 1B, 2B, 3B, HR)
    3.5. Implement Half-Inning Simulation Logic
        3.5.1. Loop through batters until 3 outs
    3.6. Implement Full Game Simulation Logic
        3.6.1. Loop through 9 innings (or more for ties if implemented later)
        3.6.2. Alternate between top and bottom of innings
        3.6.3. Handle basic game-ending conditions

4.  **Monte Carlo Simulation Implementation**
    4.1. Develop Loop to Run Multiple Game Simulations (e.g., 1000 times)
    4.2. Aggregate Results
        4.2.1. Count wins for each team
    4.3. Calculate and Output Win Percentages

5.  **Code Refinement and Testing**
    5.1. Unit testing for individual functions/classes (Simplified for this scope)
    5.2. Integration testing for full game simulation (Simplified for this scope)
    5.3. Debugging and code cleanup

6.  **Documentation and Finalization**
    6.1. Update/Finalize all Project Management Artifacts
    6.2. Write README for the project in the root directory
    6.3. Ensure repository is correctly structured as per assignment prompt
    6.4. Prepare submission comment on AI collaboration and peer insights

7.  **Supplementary Code (If Applicable)**
    7.1. Document any scripts in `/supplementary_code/raw_data_processing/` (if any were created beyond using existing cleaned data)