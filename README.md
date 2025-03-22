# printline

A simple bash utility to draw a line from the current cursor position to the end of the terminal line.

## Usage

```bash
printline [char] [prefix_text]
```

Where:
- `char` is any single character to repeat (default: `-`)
- `prefix_text` is optional text to print before the line

## Examples

```bash
# Basic usage with default character
printline

# Using a custom character
printline '='

# With prefix text
printline '*' '# Header '

# Combined with echo
echo -n "Title: "; printline
```

## Installation

Copy the `printline` script to a directory in your PATH.

```bash
cp printline /usr/local/bin/
chmod +x /usr/local/bin/printline
```

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.