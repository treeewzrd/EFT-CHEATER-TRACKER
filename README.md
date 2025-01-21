# (EFT Cheater Tracker)

## Description

EFT Cheater Tracker helps players track cheaters in Escape from Tarkov based on server, time of day, and day of the week. By logging encounters over time, the app helps identify patterns to avoid certain servers at specific times

- What did I learn?
1. Data Tracking and Analysis: I’ve learned how to collect data (such as cheater encounters on specific servers, times, and days) and use that data to make informed decisions.

2. Web Development: I’ve worked with HTML, CSS, JavaScript, and Bulma. Which has helped me create an intuitive and visually appealing user interface for interacting with the data

3. Design with User Experience in Mind: By designing with Bulma and ensuring my app is easy to use, I’ve learned how important it is to make the experience seamless and visually engaging for users. I've also learned how to balance functionality and aesthetics.

4. Problem-Solving: Building an app like this requires a lot of creative problem-solving, from managing data to ensuring everything works together. I've learned how to break down problems and approach them methodically to build the app's functionality.

5. Patience and Iteration: I’ve realized how important it is to iterate and test frequently. Developing an app like this can take time, and I’ve learned the value of experimenting, tweaking, and refining code based on user feedback and my own observations.

6. Version Control and Organization: I’ve used version control (e.g., Git), I’ve learned how to manage and organize my codebase, keeping track of changes and ensuring I can safely experiment with new features without breaking existing functionality.

## Table of Contents (Optional)

If your README is long, add a table of contents to make it easy for users to find what they need.

- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)
- [Badges](#badges)
- [Features](#features)
- [How to Contribute](#how-to-contribute)
- [Tests](#tests)

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/treeewzrd/team-project.git

2. Navigate to the project folder in git
    ```bash
    cd team-project

3. Install dependencies (if any):
    ```bash
    npm install

4. Open the index.html file in your browser to start using the app.

## Usage
1. Open the app in your browser.
2. Input the server, time of day, and day of the week after each encounter.
3. View the generated reports to see patterns of when cheaters are most frequent.

## Credits
- [Bulma](https://bulma.io/) for the CSS framework
- [Escape from Tarkov community](https://forum.escapefromtarkov.com/) for helping identify common cheater behavior patterns


## License
This project is licensed under the MIT License - see the LICENSE file for details

## Badges
[![Build Status](https://img.shields.io/github/workflow/status/treeewzrd/eft-cheater-tracker/CI)](https://github.com/treeewzrd/eft-cheater-tracker/actions)
[![License](https://img.shields.io/github/license/treeewzrd/eft-cheater-tracker)](https://opensource.org/licenses/MIT)
[![Contributors](https://img.shields.io/github/contributors/treeewzrd/eft-cheater-tracker.svg)](https://github.com/treeewzrd/eft-cheater-tracker/graphs/contributors)
[![Version](https://img.shields.io/github/release/treeewzrd/eft-cheater-tracker.svg)](https://github.com/treeewzrd/eft-cheater-tracker/releases)
[![Last Commit](https://img.shields.io/github/last-commit/treeewzrd/eft-cheater-tracker.svg)](https://github.com/treeewzrd/eft-cheater-tracker/commits)
[![Issues](https://img.shields.io/github/issues/treeewzrd/eft-cheater-tracker.svg)](https://github.com/treeewzrd/eft-cheater-tracker/issues)
[![Downloads](https://img.shields.io/github/downloads/treeewzrd/eft-cheater-tracker/total.svg)](https://github.com/treeewzrd/eft-cheater-tracker/releases)
[![Language](https://img.shields.io/github/languages/top/treeewzrd/eft-cheater-tracker.svg)](https://github.com/treeewzrd/eft-cheater-tracker)


## Features
Features of EFT Cheater Tracker:

1. Track Cheaters by Server
Allows users to track the number of cheaters encountered on different Escape from Tarkov servers.

2. Time of Day Tracking
Users can log the time of day they encounter cheaters, allowing the app to identify patterns and trends in cheating activity during specific times.

3. Day of Week Tracking
Enables users to track which days of the week are more prone to encounters with cheaters, helping players avoid specific times and days.

4. Cheater Encounter Log
A system to log details about cheater encounters, including server name, time of day, and day of week, which can be referenced later.

5. Server Avoidance Recommendations
Based on the logged data, the app can suggest which servers are more likely to have cheaters at certain times, allowing users to make informed decisions about where to play.

6. Simple and User-Friendly Interface
A clean, intuitive UI built with HTML, CSS, and JavaScript, providing an easy way to log and view cheater encounter data.

7. Customizable Filters
Allows users to filter the data based on server, time of day, or day of week to see detailed reports.

8. Responsive Design
The app is responsive, ensuring it looks and works well on both desktop and mobile devices.

9. Data Visualization (Planned Feature)
I might add more graphs or charts to visualize trends over time, helping users quickly spot patterns.

10. Persistent Data Storage
The app will remember past logs, even after the user closes the app or reloads the page.

11. Cheater Encounter Statistics
Provides statistics, such as the total number of cheaters encountered, most problematic servers, and peak times for cheating activity.

12. Real-Time Updates
If integrated with a backend or API, it could allow real-time data logging and updates, showing the latest cheater encounters immediately.

13. User Feedback Option (Planned Feature)
Allows users to submit feedback or report new servers or times where they’ve encountered cheaters.

14. Dark Mode
A dark mode option to reduce eye strain for users during long gaming sessions.

15. Data Export (Planned Feature)
Users may be able to export their encounter data to a CSV or Excel file for further analysis.


## How to Contribute
Thank you for considering contributing to the EFT Cheater Tracker project! Your contributions are highly appreciated. 
Here’s how you can get involved:

1. Reporting Bugs:
If you encounter a bug or issue with the app, feel free to open an issue on the GitHub repository. Provide as much information as possible, including:

A clear description of the issue
Steps to reproduce the bug
Expected vs. actual behavior
Screenshots (if applicable)

2. Feature Requests:
If you have a feature idea that you think would improve EFT Cheater Tracker, open an issue with the "Feature Request" label. Provide a detailed description of the feature and why it would benefit the app.


## Tests
Writing Tests

Testing Framework:
This project uses Jest for JavaScript testing. If you're writing tests, make sure to follow the structure and guidelines used in this framework.

Test Location:
All tests are located in the tests/ directory. This is where you should add new tests.

Creating a New Test:
Create a new .test.js file in the tests/ folder for each new feature or function you're testing.
Test Structure:

Arrange: Set up any necessary data or mock functions.
Act: Call the function or execute the action you're testing.
Assert: Use assertions (expect()) to verify that the result matches your expectations.

Running Tests
To run the tests, follow these steps:

Install Dependencies:
Make sure you have all the dependencies installed by running:

```bash
npm install
Run the Tests:
To run all tests, use the following command:

```bash
npm test
This will execute Jest and display the results of all tests.

Watch Mode:
To run tests in "watch mode" (which automatically re-runs tests when you make changes to your code), use:

```bash
npm run test:watch
Test Coverage
Test coverage helps us measure how much of the code is covered by tests. To check the coverage, run:

```bash
npm run test:coverage
This will generate a report showing how much of the code is tested and which parts need more coverage.

Example Tests
If you'd like to see examples of tests in action, refer to the files in the tests/ directory. These include basic tests for various app features such as tracking cheaters, managing data, and generating reports.


