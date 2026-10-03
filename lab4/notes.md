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

### 10. Special purpose and placement of README.md
A root-level `README.md` is a universally recognized standard across the software development community. Hosting services like GitHub automatically detect this specific file and render it as the home page documentation for anyone visiting the repository.

### 11. How `gh auth login` eliminates future password prompts
`gh auth login` runs an OAuth authentication process with GitHub and securely stores a personal access token in your operating system's credential helper. Future Git operations use this token automatically over HTTPS instead of asking for your account password.

### 12. File rendered on GitHub's front page and the reason why
The `README.md` file is rendered on the front page. By convention, GitHub detects a Markdown file named README at the root of a repository and automatically formats and displays it as the project homepage.

### 13. Effect of `git push` on local history
Running `git push` does not alter your local commit history or change any commit hashes. It copies your local commits to the remote GitHub server and updates the remote tracking branch pointer (`origin/main`).

### 14. Distinction between a private repository vs. no repository on GitHub
A private repository exists as an off-site backup on GitHub's cloud servers, accessible securely to you and invited collaborators like your TAs. If a repository does not exist on GitHub, all code and version history exist solely on your local machine with no cloud backup or collaboration access.
