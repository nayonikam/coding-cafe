# Lab 4: Git & GitHub - Notes & Answers

### Question 1
The `--global` flag saves your configuration settings in your global user profile (`~/.gitconfig`), applying them to all Git repositories on your computer. If you left it out, the setting would only apply to the current repository, and Git would require you to configure your identity separately for every new project.

### Question 2
The hidden `.git` directory appeared in `ls -a` but not in standard `ls`. It contains Git’s internal database, object store, configuration files, and reference logs that power the repository's version control history.

### Question 3
Git offered to track dozens of files and folders across the directory, including virtual environment files like `.venv/`. Files inside `.venv/` and `__pycache__/` are generated automatically by Python and package managers rather than code written by you.

### Question 4
After creating and populating `.gitignore`, all the files and folders specified inside it (such as `.venv/` and `__pycache__/`) completely disappeared from the untracked files list in `git status`.

### Question 5
`.gitignore` should be committed because it contains project-wide configuration rules that your collaborators and TAs also need in their local environments. If it were ignored, Git would not track the rules telling it what to ignore, preventing others from sharing those exclusions.

### Question 6
`README.md` moved from "Changes not staged for commit" (untracked) to "Changes to be committed" (staged). In the three-places model, the file moved from your working directory into the staging area (index).

### Question 7
Git printed the branch name, the abbreviated commit hash, your commit message, and a summary line indicating how many files changed along with the total number of insertions and deletions.

### Question 8
The first seven characters are the short commit hash (derived from a SHA-1 checksum). They serve as a compact, unique identifier to reference that specific commit within the repository's history.

### Question 9
The four steps of the iterative Git loop are: (1) edit your files, (2) check status using `git status`, (3) stage your changes using `git add`, and (4) commit your changes using `git commit`.

### Question 10
`README.md` gets a special name and root placement because platforms like GitHub automatically look for and render it as the front-page overview of the repository. This gives visitors and TAs an immediate, readable summary of what the project contains.

### Question 11
`gh auth login` authenticates your GitHub CLI tool and securely stores an OAuth token on your machine. This token authorizes your local Git client to communicate with GitHub without prompting you for a password on every push.

### Question 12
The rendered contents of `README.md` are displayed on the repository's front page because GitHub automatically detects and renders standard markdown README files at the root level.

### Question 13
No, pushing your commits to GitHub does not alter your local commit history in any way; it merely uploads and synchronizes your local history with the remote repository.

### Question 14
A private repository exists on GitHub with restricted permissions so that only you and explicitly invited collaborators (such as your TAs) can view or clone it. A repository that does not exist at all has no remote presence on GitHub, offering no cloud backup or remote collaboration capability.
