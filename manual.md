# User Manual

**Project:** Short Demo Application

**Author:** Siddhi Pathak

**Version:** 1.0

---

## Overview

This short user manual describes how to install, run, and test the Demo Application provided for Lab 1. The goal is to give a clear, minimal set of steps so a new user can get the app running and understand its basic features.

## Features

* Feature A — Demonstrates input processing
* Feature B — Shows output formatting
* Simple CLI to run demonstrations

## Prerequisites

* Git (>= 2.0)
* Python 3.8+ (or Node.js / Java depending on your project) — this manual assumes a Python demo
* A GitHub account (for pushing and PR workflow)

## Installation (local)

1. Clone the repository:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

2. Create and activate a virtual environment (Python example):

```bash
python3 -m venv venv
source venv/bin/activate   # Linux / macOS
# .\venv\Scripts\activate  # Windows PowerShell
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

## How to run (examples)

Run the demo CLI:

```bash
python -m demo main --input sample_input.txt
```

Expected output: a formatted result printed to stdout and saved to `output/result.txt`.

## Configuration

* `config.yaml` — small YAML file to change demo parameters (timeout, verbosity, output path)
* Example snippet:

```yaml
verbosity: info
output_dir: output
max_items: 10
```

## Running tests

1. Run unit tests:

```bash
pytest tests
```

2. Run linters:

```bash
flake8 src tests
mypy src
```

## Troubleshooting

* If dependencies fail to install, make sure your Python version matches the one required and try upgrading `pip`:

```bash
pip install --upgrade pip
```

* If `pytest` fails with import errors, verify `PYTHONPATH` or run tests from project root with the virtual environment activated.

## Contribution / PR workflow (for the lab)

1. Create a feature branch:

```bash
git checkout -b feature/add-demo
```

2. Make changes and commit often with meaningful messages:

```bash
git add demo.py
git commit -m "Add CLI entrypoint and docs"
```

3. Push the branch:

```bash
git push -u origin feature/add-demo
```

4. Open a Pull Request on GitHub from `feature/add-demo` into `main`. Request two reviewers.

5. Address review comments by pushing new commits to the same branch.

6. After approval, merge the PR and pull the `main` branch locally:

```bash
git checkout main
git pull
```

## Files included

* `README.md` — project overview
* `user_manual.md` (this file) — user manual
* `requirements.txt` — Python dependencies
* `src/` — application source
* `tests/` — unit tests

## Contact

If something’s unclear, contact: [your.email@example.com](mailto:your.email@example.com)

---

*End of manual*
