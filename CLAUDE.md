
## Coding Principles
  - K.I.S.S.
  - "The best process is no process"
  - "Everything should be made as simple as possible, but not simpler."

## Build/Test/Lint Commands
- Shell scripts:
  - Syntax check: `bash -n scriptname`
  - Lint/static analysis: `shellcheck scriptname`
  - Version check: `cat .version`

## Code Style
- Python: 
  - 2-space indentation, shebang line `#!/usr/bin/env python3`
  - Import order: standard lib, third-party, local modules
  - Constants: Define at top of files, use UPPER_CASE
  - Use descriptive function and variable names
  - Docstrings for functions; comment complex logic sections
  - Always end scripts with '\n#fin\n' to indicate the end of script
  - In HTML tags always prefer use of single quotes over double quotes where possible

- Shell scripts:
  - Shebang: '#!/bin/bash'  
  - Always `set -euo pipefail` at start for error handling, unless there is a good reason not to do this
  - 2-space indentation
  - Always declare variables before use with `local` in functions
  - Use `local -i` for integer variables
  - Prefer `[[` over `[` for conditionals
  - Prefer `((...))` for arithmetic operations
  - Document functions with comments above definition
  - Always end scripts with '\n#fin\n' to indicate the end of script
  - Implement -h/--help options with usage examples
  - Store version in .version file in project root
  - Use ripgrep (rg) for enhanced file search

- PHP:
  - Always use 2-space indent
  - Prefer PHP short tags (<? ... ?>), except at the top of a file where you should always use <?php
  - Always use <?=...?> where possible for simple output; never <?php echo ...?>
  - Follow PSR-12 coding standards
  - Use prepared statements for all database queries
  - Always check array keys with isset() before accessing
  - Filter user inputs with filter_input() functions
  - Sanitize output with htmlspecialchars() or similar
  - Always check file operations for errors
  - Use proper HTTP status codes for errors

- JavaScript:
  - Use ES6+ syntax and features
  - Avoid jQuery where possible, use modern DOM APIs
  - Follow Bootstrap patterns for UI components
  - Always sanitize dynamic content before insertion
  - Use strict mode ('use strict')

- Error handling:
  - Python: Use try/except with logging
  - Shell: Use proper exit codes and targeted error messages
  - Validate all input parameters early
  - Provide helpful usage examples in help text

- Environment:
  - Python venvs: Activate with `source <dir>/.venv/bin/activate`
  - Use MySQL or Sqlite3 database for data storage, as appropriate

## Developer Tech Stack
- Ubuntu 24.04.2
- Bash 5.2.21
- Python 3.12.3
- Apache2 2.4.58
- PHP 8.3.6
- MySQL 8.0.41
- sqlite3 3.45.1
- Bootstrap 5.3
- FontAwesome

## Hardware
- Development Machine (hostname 'okusi'):
  - model: Lenovo Legion i9
  - gpu: GEForce RTX
  - system memory: 32GB

- Production Machine (hostname 'okusi3'):
  - model: Intel Xeon Silver 4410Y, 2 cpu
  - gpu: NVIDIA L4
  - system memory: 128GiB

## Backups and Code Checkpoints
- The '.../wah.id/.gudang/' directory contains complete codebase backups
- Backup format: .gudang/YYYYMMDD_hhmmss/
- .gudang directories should normally be ignored.

#fin
