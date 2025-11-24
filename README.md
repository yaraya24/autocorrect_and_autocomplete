# Autocorrect and Autocomplete Terminal

A Python-based terminal emulator that adds live autocorrect and autocomplete support on top of a bash-like experience.

## Features
- **Custom terminal shell:** Runs commands through bash while keeping track of cursor position and user input in raw mode.
- **Autocorrect:** Checks typed words against a dictionary and falls back to the Bing Autocorrect API when needed. Corrections can be undone.
- **Autocomplete:** Provides cycling suggestions backed by a trie data structure; suggestions can be inserted with **Tab**.

## Requirements
Install dependencies with:
```bash
pip install -r requirements.txt
```

## Running the app
From the repository root, run:
```bash
python3 main.py
```

## Keyboard shortcuts
- **Ctrl-Z** – Undo the last autocorrection
- **Ctrl-O** – Toggle autocorrect on/off
- **Up/Down** – Cycle through autocomplete suggestions
- **Tab** – Insert the highlighted autocomplete suggestion

## Known limitations
- Programs that do not exit on their own (e.g., `vim`, `nano`, `ping`) are not supported.
- Resizing the terminal mid-command can cause display glitches for wrapped text.
- If the program crashes, the terminal may stay in raw mode; run `stty sane` to recover.

## Tests
Unit tests cover the autocomplete and spellcheck helpers:
```bash
python -m pytest
```
