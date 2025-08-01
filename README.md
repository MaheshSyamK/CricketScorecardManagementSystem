# Cricket Scorecard Management System

## Overview
The Cricket Scorecard Management System is a C++ program designed to manage and display detailed cricket match data using Object-Oriented Programming (OOP) principles and file handling. This project eliminates the need for a graphical interface, focusing on efficient storage and output through text files, specifically `scorecard.txt`. It provides a robust solution for tracking ball-by-ball updates, generating comprehensive scorecards, and storing match results.

## Features
- **Ball-by-Ball Updates**: Tracks every ball of the match for both innings, including runs, wickets, extras, and more.
- **File Handling**: Stores match details, scorecards, and final results in a structured text file (`scorecard.txt`).
- **Comprehensive Output**: Generates detailed scorecards, match summaries, and bar graphs for statistical analysis.
- **User-Friendly**: Provides an easy-to-read text-based scorecard and supports input validation for seamless operation.
- **OOP Design**: Utilizes classes and inheritance to model cricket entities like players, teams, and balls (e.g., `NormalBall`, `WideBall`, `WicketBall`).
- **Match Result Analysis**: Determines the winning team or declares a tie based on runs scored and batting choices.

## How It Works
1. Users input cricket match details such as team names, player names, venue, and the number of overs.
2. The system processes each ball, updating the scorecard with details like runs, wickets, fours, sixes, and extras.
3. All data, including ball-by-ball scores, team statistics, and match results, is stored in `scorecard.txt`.
4. The program generates a tabular scoreboard and bar graphs for visual comparison of team performance.
5. Sample input and output files, along with screenshots, are provided in the `samplerun/` folder for reference.

## File Structure
- **src.cpp**: The main C++ source code file containing the entire program logic.
- **scorecard.txt**: The output file where match details, scorecards, and results are stored.
- **samplerun/**: A folder containing example input/output files and screenshots of sample match scorecards.
- **README.md**: This file, providing an overview and instructions for the project.

## Prerequisites
- A C++ compiler (e.g., GCC, Visual Studio, or any IDE supporting C++11 or later).
- Basic knowledge of cricket scoring and terminology.

## How to Run
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/MaheshSyamK/CricketScorecardManagementSystem.git
   cd CricketScorecardManagementSystem
   ```
2. **Compile the Code**:
   Use your preferred C++ compiler to compile `src.cpp`. For example, with GCC:
   ```bash
   g++ src.cpp -o cricket_scorecard
   ```
3. **Run the Program**:
   Execute the compiled program and follow the prompts to input match details:
   ```bash
   ./cricket_scorecard
   ```
4. **Input Match Details**:
   - Enter team names, player names, venue, and number of overs.
   - Specify the toss winner and their choice (bat or bowl).
   - For each ball, input the ball type (e.g., `N` for normal, `w` for wide, `W` for wicket) as prompted.
5. **View Output**:
   - The program generates `scorecard.txt` with detailed match data, including scorecards, statistics, and results.
   - Check the `samplerun/` folder for sample outputs and screenshots.

## Code Structure
The program is built with an OOP approach, utilizing the following key components:
- **Classes**:
  - `CricketPlayer`: Represents a player with attributes like name and playing status.
  - `CricketTeam`: Manages team details and player lists.
  - `CricketMatch`: Handles match details, toss, and file output.
  - `Ball` (Abstract) and Derived Classes (`NormalBall`, `WideBall`, `NoBall`, etc.): Models different types of balls and their scoring logic.
- **Key Functions**:
  - `score_value()`: Displays valid ball input options.
  - `checkBatsmen()` and `checkbowler()`: Validate batsman and bowler names.
  - `displayScoreboard()`: Shows ball-by-ball and innings summaries.
  - `saveMatchDetail()`: Writes match data to `scorecard.txt`.
  - `writeBarGraphToFiles()`: Generates bar graphs for statistical visualization.

## Sample Input/Output
- **Input Example** (via console):
  - Team 1: `India`
  - Team 2: `Australia`
  - Venue: `Eden Gardens`
  - Overs: `5`
  - Toss Winner: `India`, Choice: `Bat`
  - Ball Inputs: `N 2`, `4`, `W`, `w 1`, `.`, etc.
- **Output** (`scorecard.txt`):
  - Team and player details.
  - Ball-by-ball scorecard for each over.
  - Tabular scoreboard with runs, wickets, fours, sixes, etc.
  - Bar graphs comparing team statistics.
  - Match result (e.g., "India won by 10 runs").
- **Samplerun Folder**:
  - Contains sample `scorecard.txt` files and screenshots of console outputs for reference.

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with a clear description of your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For questions or feedback, reach out via the [GitHub Issues](https://github.com/MaheshSyamK/CricketScorecardManagementSystem/issues) page.