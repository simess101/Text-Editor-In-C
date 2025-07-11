---

# Text-Editor-in-C (Kilo Clone)

## Overview

This project is a simple text editor written in C, inspired by the `kilo` text editor created by Salvatore Sanfilippo. It runs in the terminal and provides basic text editing capabilities such as file reading, saving, and navigating. The editor supports keyboard shortcuts for easier file manipulation.

## Features

- Basic text editing functionality (insert, delete, and navigation).
- Read and write text files.
- Supports search functionality within files.
- Terminal-based interface with raw mode for smoother input handling.
- Handles tabs, multi-line text, and window resizing.

## Compilation

To compile the text editor, you'll need a C compiler like `gcc`. Use the provided `Makefile` to compile the project.

### Makefile:

```make
kilo: kilo.c
    $(CC) kilo.c -o kilo -Wall -Wextra -pedantic -std=c99
```

### Steps:
1. Clone the repository or copy the `kilo.c` file to your machine.
2. Run the following command to compile the program:
   ```bash
   make
   ```

3. After successful compilation, an executable named `kilo` will be created.

## Running the Editor

To start the editor:

```bash
./kilo <filename>
```

- If the `<filename>` exists, it will open the file for editing.
- If the file does not exist, a new file will be created once you save it.

## Key Bindings

- `Ctrl-Q` – Quit the editor. If there are unsaved changes, you will be asked to confirm by pressing `Ctrl-Q` multiple times.
- `Ctrl-S` – Save the current file to disk.
- `Ctrl-F` – Search within the file. Use `Esc` to exit the search, and arrow keys to navigate through matches.
- `Arrow Keys` – Navigate the text (up, down, left, right).
- `Ctrl-H` or `Backspace` – Delete the character before the cursor.
- `Ctrl-L` – Refresh the screen.

## File Management

- You can create, edit, and save files using the `kilo` editor.
- If you attempt to quit with unsaved changes, you’ll be prompted to confirm the exit without saving.

## Dependencies

- The project uses standard C libraries like `unistd.h`, `termios.h`, and other system libraries for terminal handling.
- No external dependencies are required beyond a C compiler and a POSIX-compatible terminal.

## License

This project is open-source and free to use. Please give credit to Salvatore Sanfilippo, the creator of the original `kilo` text editor.

---
