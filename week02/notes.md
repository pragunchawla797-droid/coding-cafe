# Lab 1 - Notes

1. `pwd` printed the absolute path of my current working directory (`/Users/yourusername`).
2. `ls -a` revealed hidden files and directories (those starting with a `.`, like `.zshrc` and `..`) which standard `ls` hides.
3. The first column shows file permissions and file type (e.g., `drwxr-xr-x` indicates a directory `d` with read, write, and execute permissions).
4. It works because `coding-cafe/week02` is a **relative path** relative to the current home directory, not an absolute path starting from root (`/`).
5. In the first instance, `mv` **moved/relocated** the file to a different folder (`week01/`). In the second instance, it **renamed** the file to `old-readme.md`.
6. There are 6 directories listed in my `PATH` variable, separated by colons.
7. My `python3` lives at `/opt/homebrew/bin/python3` (or `/usr/bin/python3`).
8. They may differ because different machines use different installation methods (e.g., Homebrew installs to `/opt/homebrew/bin/`, while macOS system Python lives in `/usr/bin/`).
9. The shell said `command not found: pyton3`. This means the shell searched through every folder listed in `$PATH` and could not find an executable matching that typo.
10. `.venv` starts with a dot (`.`), which marks it as a hidden directory; plain `ls` ignores hidden files.
11. The prompt was prefixed with `(.venv)`, showing that the virtual environment is currently active.
12. No, it is now `/Users/yourusername/coding-cafe/.venv/bin/python3`. Activating the virtual environment prepended `.venv/bin` to the front of `$PATH`.
13. `requests` and its dependencies (`urllib3`, `idna`, `certifi`, `charset-normalizer`) appeared in the second list.
14. It points back to the system/Homebrew Python (`/opt/homebrew/bin/python3`).
15. The `-h` flag makes file sizes human-readable (e.g., displaying sizes in K, M, or G instead of raw byte numbers).
16. `Ctrl + C` sends an interrupt signal (`SIGINT`) to cancel the current command line without quitting Python. `Ctrl + D` sends an End-Of-File (`EOF`) signal that closes the Python interpreter entirely.