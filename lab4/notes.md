# Lab 4 Notes

### 1. Meaning of `--global` in `git config` and omitting it
The `--global` flag applies settings across all repositories for your current user account on this machine. If you omit `--global`, the configuration applies only to the current repository you are in. Without either setting, Git will not know what identity to attach to commits.

### 2. Contents of `.git` revealed by `ls -a`
Running `ls -a` reveals the hidden `.git/` directory, which is Git's internal tracking database. Inside are directories and files such as `objects/`, `refs/`, `HEAD`, and `config` that store all snapshots, branches, and version control metadata.

### 3. Approximate untracked file count and identifying untracked code
Git offers to track hundreds or thousands of files when virtual environments or cache files exist. The files inside `.venv/` represent third-party Python libraries that you did not write yourself and should not be tracked in version control.

### 4. Difference in `git status` after creating `.gitignore`
After creating `.gitignore`, all the files and folders specified inside it (`.venv/`, `__pycache__/`, `.DS_Store`) completely disappear from the untracked files list. Git stops tracking those temporary files.

### 5. Why `.gitignore` itself should be committed rather than ignored
The `.gitignore` file should be committed because it is a shared project configuration file. Committing it ensures that all collaborators and remote environments ignore the same non-project files automatically.

### 6. Movement of `README.md` across sections in `git status` (three-places model)
Running `git add README.md` moves the file from "Untracked files" to "Changes to be committed". In the three-places model, the file moved from the Working Directory into the Staging Area (index).

### 7. Output produced by `git commit` and count of changed files
Git outputs the branch name, the short commit hash, the commit message, and a change summary listing how many files changed along with insertions and deletions. The file count matches all initial project files staged.

### 8. Name and purpose of the first seven characters of a commit hash
The first seven characters are called the short SHA-1 hash (or short commit hash). They serve as a unique identifier for that specific commit snapshot, allowing you to view, reference, or roll back to that state later.
