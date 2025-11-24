# Autocorrect & Autocomplete Terminal

A lightweight Python terminal wrapper with live autocorrect and autocomplete support.

## Requirements
- Python 3.9+
- `pip install -r requirements.txt`

## Quick Start
1. Install dependencies (once): `pip install -r requirements.txt`
2. Run the app: `python3 main.py`
3. Type in the provided prompt; the wrapper proxies commands to your shell.

## Controls
- **Ctrl+Z**: Undo the last autocorrection
- **Ctrl+O**: Toggle autocorrect on/off
- **Up/Down**: Cycle autocomplete suggestions
- **Tab**: Insert the highlighted suggestion

## Features
- Bash-like terminal experience powered by ANSI escape codes
- Inline autocorrect using a dictionary with optional Bing suggestions
- Trie-based autocomplete suggestions while you type

## Known Limitations
- Programs that never exit (e.g., `vim`, `nano`, `ping`) are not supported
- Text wrapping can behave oddly on the last terminal row or after resizing
- If the app crashes, run `stty sane` to restore your terminal
