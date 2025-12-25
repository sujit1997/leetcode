# LeetCode Solutions

[![Repo Size](https://img.shields.io/badge/solutions-__PLACEHOLDER__-blue)]() [![Languages](https://img.shields.io/badge/languages-Python%2C%20C%2B%2B%2C%20Java-lightgrey)]() [![License](https://img.shields.io/badge/license-MIT-green)]()

A curated collection of LeetCode problem solutions organized for learning, reference, and interview preparation. This repository contains clean, well-documented solutions across multiple languages, with testing instructions, contribution guidelines, and conventions to keep everything consistent.

## Table of Contents

- [Repository Structure](#repository-structure)
- [Conventions](#conventions)
- [How to Run / Test](#how-to-runtest)
- [How to Add a Solution](#how-to-add-a-solution)
- [Progress Tracking](#progress-tracking)
- [Coding Style & Best Practices](#coding-style--best-practices)
- [CI / Automation](#ci--automation)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Repository Structure

Organize solutions by problem number and topic (optional). Example layout:

- problems/
  - 0001-two-sum/
    - solution.py
    - solution.cpp
    - solution.java
    - README.md         # problem statement summary, complexity, notes
    - tests/
      - test_0001.py
  - arrays/
    - 0027-remove-element/
      - solution.py
      - README.md
- utils/                # helper libs used across solutions (optional)
- scripts/              # helper scripts (run tests, format code, generate index)
- README.md
- CONTRIBUTING.md

Recommended path formats:
- problems/<problem-number>-<slug>/...
- optional topic folders: problems/arrays/, problems/dynamic-programming/

## Conventions

Use consistent filenames and metadata inside each problem folder.

Example solution header (Python):
```python
# LeetCode 1 - Two Sum
# https://leetcode.com/problems/two-sum/
# Difficulty: Easy
# Tags: Array, Hash Table
# Time Complexity: O(n)
# Space Complexity: O(n)
# Author: <your-name> (github: @username)
```

File naming:
- solution.py / solution.cpp / Solution.java (language-idiomatic)
- tests: test_<problem-number>.py for Python pytest

Include a short README.md inside each problem folder with:
- problem link
- brief description
- approach summary
- complexity analysis
- references (if any)

## How to Run / Test

General instructions — adapt per language.

Python (recommended):
- Use virtualenv / venv
- Install test dependencies (if any):
  - pip install -r requirements.txt
- Run pytest for all tests:
  - pytest -q

Example:
```bash
python -m venv .venv
source .venv/bin/activate        # macOS / Linux
.\.venv\Scripts\activate         # Windows
pip install -r requirements.txt
pytest tests/ -q
```

C++:
- Use your preferred build system (g++, CMake). Example:
```bash
g++ -std=c++17 solution.cpp -O2 -o solution
./solution
```

Java:
- Use Maven/Gradle or javac:
```bash
javac Solution.java
java Solution
```

Scripts folder can include helper commands like:
- scripts/run_all_python_tests.sh
- scripts/generate_index.py

## How to Add a Solution

1. Fork the repo and create a branch: `feat/leetcode-<num>-<slug>`
2. Create folder `problems/<num>-<slug>/`
3. Add:
   - solution.(py|cpp|java)
   - README.md with problem link, approach, complexity
   - tests/ (optional, preferred)
4. Run tests locally
5. Open a PR with a clear title: `Add LeetCode <num> - <Title> (<Language>)`
6. Fill PR description with approach and complexity

PR checklist:
- [ ] Solution compiles / runs
- [ ] Tests added (if applicable)
- [ ] README contains link and complexity
- [ ] Code follows style guide

## Progress Tracking

Maintain a table or JSON in the repo root (e.g., PROGRESS.md or progress.json). Example PROGRESS.md snippet:

| Problem | Title | Langs | Status | Notes |
|---------|-------|-------|--------|-------|
| 1 | Two Sum | py, cpp | done | Optimized hash map O(n) |

You can also add GitHub project boards or use issues to track "to-solve" / "in-progress" / "done".

## Coding Style & Best Practices

- Keep solutions idiomatic for each language.
- Prefer readability over golfed solutions — include explanatory comments.
- Explain non-obvious steps in the problem README.
- Limit global state; write pure functions where possible (easier to test).
- Document time and space complexity for each solution.

Linting & formatting:
- Python: black + flake8
- C++: clang-format
- Java: google-java-format

## CI / Automation

Suggested GitHub Actions workflow:
- Run on push/PR
- For Python: setup Python, install dependencies, run pytest
- For C++: compile and run basic tests
- Run linters (optional)

Example workflows can be placed in .github/workflows/ci.yml

## Contributing

Please see CONTRIBUTING.md for detailed instructions. Short summary:
- Follow repository conventions
- Add tests and README for the problem
- Make small, focused PRs
- Be respectful and provide helpful PR descriptions

If you want a personal practice plan (e.g., daily streak), open an issue and label it discussion.

## License

This repository is licensed under the MIT License. See LICENSE for details.

## Contact

Maintained by sujit1997 (GitHub: @sujit1997). Open issues or PRs for suggestions, corrections, or improvements.

---

Happy coding! Make sure to include the original LeetCode problem link in each problem folder README to respect problem statements and references.
