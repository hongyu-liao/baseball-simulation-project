# Work Breakdown Structure (WBS) - Baseball Monte Carlo Simulation

1.  **Project Setup & Planning**
    1.1. Define Core Project Goal (Monte Carlo Baseball Simulation)
    1.2. Create GitHub Repository (`baseball-simulation-project`) and Basic Folder Structure
    1.3. Outline Key Project Management Artifacts (Functional Specs, WBS, Backlog, Status Log, Activity List, Roadmap)

2.  **Data Handling**
    2.1. Identify and Locate Prepared CSV Data (Player Batting & Pitching Stats)
        2.1.1. Batting Data: `cubs_standard_batting_clean.csv`, `whitesox_standard_batting_clean.csv`
        2.1.2. Pitching Data: `cubs_standard_pitching_clean.csv`, `whitesox_standard_pitching_clean.csv`
    2.2. Implement CSV Data Loading in Python (using Pandas)
        2.2.1. Function to load batter data (BA, OBP, SLG)
        2.2.2. Function to load pitcher data (ERA)
        2.2.3. Basic error handling for data loading (use default stats if issues)

3.  **Core Simulation Logic Development (Python)**
    3.1. Define Core Classes
        3.1.1. `Player` Class (name, stats, derived chances)
        3.1.2. `Pitcher` Class (name, stats, derived factors)
        3.1.3. `GameState` Class (inning, outs, score, bases, etc.)
    3.2. Implement Single At-Bat Simulation
        3.2.1. Probabilistic outcome determination (based on loaded stats)
    3.3. Implement Game Simulation Flow
        3.3.1. Half-inning simulation (until 3 outs)
        3.3.2. Full game simulation (9 innings, basic game end conditions)

4.  **Monte Carlo Simulation & Results**
    4.1. Implement Batch Simulation (e.g., 10,000 games)
    4.2. Aggregate Game Results (Win/Loss Counts)
    4.3. Calculate and Output Win Percentages

5.  **Documentation & Finalization**
    5.1. Develop Functional Specifications
    5.2. Develop Work Breakdown Structure (this document)
    5.3. Develop Product Backlog
    5.4. Maintain Status Log
    5.5. Maintain Activity List
    5.6. Develop Roadmap
    5.7. Ensure Python code is placed in `/functional_code/`
    5.8. Ensure prepared data is referenced/placed correctly for `/prepared_data/` (even if loading from a relative path to your original repo's data for now)
    5.9. Prepare submission (GitHub link and AI collaboration comments)