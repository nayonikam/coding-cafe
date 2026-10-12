# Lab 4: Git & GitHub — Answers

## Question 1: What did `--global` mean here? What would happen if you left it out?

The `--global` option sets my name and email for all Git repositories belonging to my user account. If I leave it out, the setting is normally applied only to the current repository, provided I am inside one.

## Question 2: What appeared in `ls -a` but not in `ls`? What is inside it?

The `.git` directory appeared in `ls -a` but not in `ls` because it is a hidden directory. It contains Git's internal data, including information used to manage the repository's commits, branches and configuration.

## Question 3: Roughly how many files and folders is Git offering to track? Does anything in that list look like something you did not write?

Git lists the files and folders that are currently untracked in my repository. Some entries, such as files inside `.venv/` and `__pycache__/`, are generated or installed files rather than files I created myself.

## Question 4: Compare this `git status` with the one from Question 3. What disappeared?

After creating `.gitignore`, files and folders matching its rules, such as `.venv/`, `__pycache__/` and files ending in `.pyc`, no longer appear as untracked files. This keeps unnecessary files out of the repository.

## Question 5: Should `.gitignore` itself be committed, or ignored too? Why?

The `.gitignore` file itself should be committed because it contains rules specifying which files Git should ignore. Committing it allows other people working on the project to follow the same rules.

## Question 6: `README.md` moved from one heading to another in `git status`. Which two? What just happened to it?

`README.md` moved from the "Untracked files" section to the "Changes to be committed" section. Running `git add README.md` moved it into the staging area, where it was prepared for the next commit.

## Question 7: What did Git print after the commit? How many files did it say changed?

After the commit, Git displayed information about the new commit, including its identifier and a summary of the changes. The number of files changed is the number reported in my terminal after running `git commit`.

## Question 8: What are the first seven characters of your commit called, and what are they for?

The first seven characters of a commit's identifier are called the short commit hash. They provide a convenient way to identify a particular commit without writing its full hash.

## Question 9: You now have two commits. What are the four steps of the loop you just did twice?

The four steps are edit, stage, commit and check. I edit the files, stage the changes using `git add`, save them using `git commit`, and check the result using commands such as `git status` or `git log --oneline`.

## Question 10: Why does this file get a special name and a special place, rather than being called `notes.md`?

The `README.md` file has a special name because GitHub automatically displays it on the repository's main page. It provides an introduction to the project and helps visitors understand its purpose and contents.

## Question 11: What did `gh auth login` do that means you will not be asked for a password when you push?

The `gh auth login` command authenticated my GitHub account through the GitHub CLI and configured the credentials used for Git operations. This allows Git to authenticate future pushes without requiring me to enter my GitHub account password each time.

## Question 12: Refresh the repository page on GitHub. What is showing on the front page, and why that file?

The repository page displays my project files and shows the contents of `README.md` as formatted text. GitHub automatically renders README files on the repository's main page so visitors can understand the project.

## Question 13: Run `git log --oneline` again. Did pushing change your local history in any way?

No, pushing did not change my local commit history. The `git push` command uploaded my existing commits to GitHub, while my local history remained unchanged.

## Question 14: Your repository is private but your TAs can now read it. What is the difference between a private repository and no repository on GitHub at all?

A private repository exists on GitHub but can only be accessed by its owner and people who have been granted permission. If a repository does not exist on GitHub, there is no online repository for collaborators to access.
