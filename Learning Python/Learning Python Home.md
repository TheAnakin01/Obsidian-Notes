---
type: home
project: Learning Python
status: active
started: 2026-09-29
repo: https://github.com/TheAnakin01/Learning_Python
local_path: ~/Documents/Python
tags: [learning-python, home, python, learning]
---
# 🐍 Learning Python — Home

Back to [[Projects]]

Small beginner exercises, one question per file. Each one practises **functions, `input()`, and the
`if __name__ == "__main__": main()` pattern**.

## 🔗 Links
- **Code:** https://github.com/TheAnakin01/Learning_Python
- **On this computer:** `~/Documents/Python`

## ✅ Exercises
| # | File | What it does | Concepts | Done |
|---|---|---|---|---|
| Q1 | `hello.py`, `age.py` | Prints Hello World; tells you your age in 5 years | `print`, f-strings, `int()` conversion | 2026-09-29 |
| Q2 | `celcius.py` | Celsius → Fahrenheit (`c × 1.8 + 32`), rounded to 1 decimal | `float()`, `round()`, return values | 2026-09-30 |
| Q3 | `grade.py` | Marks → grade A–F (rejects < 0 or > 100) | `if / elif / else` chains, input validation | 2026-10-01 |
| Q4 | `leap.py` | Is a year a leap year? | Nested conditions, `%` (modulo) | 2026-10-01 |
| Q5 | `triangle.py` | Prints a star triangle of height *n* | `for` loops, `range()`, string × number | 2026-10-01 |
| Q6 | `sentence.py` | *In progress*: `main()` and `get_times()` are still stubs (`...`) | n/a | ⏳ not committed yet |

## 💡 Lessons so far
- `input()` always returns **text**. Convert it with `int()` / `float()` before doing maths.
- Leap-year rule: divisible by 4, **except** centuries, **unless** divisible by 400 (2000 ✅, 1900 ❌).
  Could be shortened to `return year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)`.
- Keep logic in its own function (`get_grade`, `is_leap`…) so it can be tested without typing input.

## 🧹 Small clean-ups to consider
- `celcius.py` → the usual spelling is *celsius*.
- In `grade.py`, `return("A")` works but `return "A"` is the normal style (no brackets needed).
- 2026-09-30 commit `01a1991` moved files out of a nested `Python/` folder. The layout is flat now.

## 📜 History
`14d4d18` upload → `a0fe362` Q1 → `a62726d` merge with GitHub → `01a1991` tidy → `9e09776` Q2 → `555df10` Q3 → `4cf9eaa` Q4 → `e147e46` Q5
