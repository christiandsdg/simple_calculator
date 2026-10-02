# Simple Calculator

A command-line calculator written in Python. It adds, subtracts, multiplies and divides two numbers through a text menu.

Built for *Programming with Python*, Term 1, MSc Computer Science & Digital Innovation at IE University.

## Requirements

- Python 3.9 or newer
- No third-party packages are needed to run the calculator

## Running it

From the project folder:

```bash
python main.py
```

Or, with [uv](https://docs.astral.sh/uv/):

```bash
uv run main.py
```

## Usage

The program shows a menu and waits for a command. Type the operation's **name** (case-sensitive), not its number:

| Command | Operation      |
|---------|----------------|
| `Sum`   | a + b          |
| `Sub`   | a − b          |
| `Mul`   | a × b          |
| `Div`   | a ÷ b          |
| `Exit`  | Quit           |

Example session:

```
1.Sum
2.Sub
3.Mul
4.Div
5.Exit

What would you like to do? > Mul
Enter first number > 4
Enter second number > 2.5
10.0
```

Results are printed as floats. Any unrecognised command prints `Please enter a valid selection.` and shows the menu again.

## How it works

- `add`, `sub`, `mul` and `div` are small functions that take two floats and return a float.
- `div` raises `ZeroDivisionError` when the second number is `0`.
- A few `assert` checks run at startup to confirm each function returns the expected result.
- A `while True` loop shows the menu, reads the user's choice and calls the matching function until the user types `Exit`.

## Project structure

```
Calculator/
├── main.py         # Calculator functions, startup tests and menu loop
├── pyproject.toml  # Project metadata
└── uv.lock         # Locked dependencies (uv)
```
