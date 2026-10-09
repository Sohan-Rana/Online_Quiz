# Online Quiz System

A simple quiz application written in Python. It runs in the terminal, stores questions and scores in SQLite, and needs **no external libraries**.

## Features

- Choose a category (Python, Computer Basics, Bangladesh) or play all of them
- Pick how many questions you want; questions come in random order
- Instant feedback, final score, percentage and grade
- Leaderboard of the best results
- Add your own questions from the menu
- Unit tests for the quiz logic and the database

## Requirements

Python 3.8 or newer. Nothing else to install.

## Run

```bash
python main.py
```

## Run tests

```bash
python -m unittest discover tests
```

## Project structure

```
Online-quiz-system/
├── main.py              # entry point
├── quiz/
│   ├── cli.py           # menus and user input/output
│   ├── engine.py        # quiz logic (scoring, grading)
│   └── database.py      # SQLite storage
├── data/questions.json  # starter questions
└── tests/test_quiz.py   # unit tests
```

## Adding questions in bulk

Edit `data/questions.json` and add an entry like this (`answer` is the 0-based index of the correct option):

```json
{"category": "Python", "text": "Your question?", "options": ["A", "B", "C", "D"], "answer": 2}
```

New questions are loaded automatically the next time you run the program.

## Ideas for the future

- Web version with Flask or FastAPI
- Timer for each question
- User accounts and an admin password
