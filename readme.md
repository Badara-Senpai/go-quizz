# Quiz App

This is a small quiz application built with Go to practice operating systems concepts, Go routines, and channels. The quiz reads problems from a CSV file and times the user as they answer the questions.

## Features

- Read quiz questions and answers from a CSV file
- Time-limited quiz using Go routines and channels
- Concurrent handling of user input and timer

## Technologies Used

- **Go**: Programming language
- **CSV**: For storing quiz questions and answers

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Badara-Senpai/quiz-app.git
    cd quiz-app
    ```

2. Build the application:
    ```bash
    go build -o quizapp
    ```

3. Run the application:
    ```bash
    ./quiz-app -csv=problems.csv -timer=30
    ```

## Usage

1. **CSV File Format**: The CSV file should be in the format of `question,answer`. Here is an example of `problems.csv`:
    ```csv
    5+5,10
    7+3,10
    1+1,2
    ```

2. **Run the Quiz**: By default, the application will look for a file named `problems.csv` in the current directory and will set a 30-second timer. You can customize these settings with the `-csv` and `-timer` flags:
    ```bash
    ./quiz-app -csv=yourfile.csv -timer=60
    ```

## Code Overview

- **main.go**: The main file containing the logic to read the CSV file, start the timer, handle user input, and calculate the score.
    - `parseLines(lines [][]string) []problem`: Parses the lines of the CSV file into a slice of `problem` structs.
    - `exit(msg string)`: Exits the program with a given message.


## Contact

If you have any questions or suggestions, feel free to reach out to me at [badara.samb@outlook.com].
