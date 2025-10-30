```markdown
# Git Learnings

## 1. What Is Git?

A Version Control System (VCS) is a tool used to track, manage, and store changes to code in a special database called a *repository*. Git is one of the most widely used distributed version control systems. It simplifies collaboration, especially when multiple contributors work on a project or when multiple versions need to be maintained and tracked efficiently.

---

## 2. Types of Version Control Systems (VCS)

### Distributed Version Control System (DVCS)
In a Distributed VCS, every developer has a full copy of the repository, including the entire commit history. Work can be done offline, and changes are later synchronized with others.

**Advantages:** Faster, reliable, supports offline work, improved collaboration  
**Examples:** Git, Mercurial, Bazaar

### Centralized Version Control System (CVCS)
In a Centralized VCS, a single central server stores the repository. Developers must connect to the server to commit or retrieve changes.

**Advantages:** Simple and easy to manage  
**Disadvantages:** If the central server fails, the system becomes unusable  
**Examples:** Subversion (SVN), CVS, Perforce

---

## 3. Tools for Working with Git

### Git Bash
A command-line interface providing a Unix-like environment on Windows to execute Git commands. It enables access to advanced Git operations such as branching, merging, and configuration.

### Git GUI
A graphical interface for users who prefer visual interaction over command-line input. Suitable for simple commit and staging operations but lacks advanced features compared to Git Bash.

---

## 4. Creating Snapshots in Git

Snapshots represent the state of files in a repository at a particular point in time. They are created and managed using the following Git commands.

---

### 4.1 Configuring Git
```


Here is the corrected section with your new configuration content added under **4.1 Configuring Git** and written professionally:

---

````markdown
### 4.1 Configuring Git

When using Git for the first time, it is necessary to configure your user identity and some default settings. These configurations are stored globally and apply to all repositories on your machine.

#### 1. Set Your Username
This name will appear in your commit history.

```bash
git config --global user.name "Your Full Name"
````

###### 2. Set Your Email Address

Ensure this is the same email linked to your GitHub account so commits are properly associated.

```bash
git config --global user.email "your-email@example.com"
```

###### 3. Set Visual Studio Code as the Default Editor

This ensures that whenever Git opens an editor (for example, during commit messages), Visual Studio Code is used.

```bash
git config --global core.editor "code --wait"
```

`--wait` ensures Git pauses until you close the editor window.

###### 4. Handle Line Endings (Windows Users)

To avoid formatting issues when working across different systems:

```bash
git config --global core.autocrlf true
```

This ensures consistent file formatting and prevents accidental line-ending changes in commits.

###### 5. Verify Configuration Settings

To review all global configurations:

```bash
git config --global --list
```

Example output:

```
user.name=Your Full Name
user.email=your-email@example.com
core.editor=code --wait
core.autocrlf=true
```

#### 6. Editing the Configuration File Directly

To open the global configuration file for manual editing:

```bash
git config --global -e
```

This opens the configuration file in your default editor.

```

---

Opens the global Git configuration file to define user information and preferences.

---

### 4.2 Initializing a Repository
```

git init

```
Creates a new Git repository in the current directory.

---

### 4.3 Staging Files
```

git add file1.js
git add file1.js file2.js
git add *.js
git add .

```
Moves changes from the working directory to the staging area, preparing them for commit.

---

### 4.4 Viewing Current Status
```

git status
git status -s

```
Displays which files are staged, unstaged, or untracked.

---

### 4.5 Committing Staged Files
```

git commit -m "Message"
git commit

```
Records a snapshot of staged changes along with a descriptive message.

---

### 4.6 Skipping the Staging Area
```

git commit -am "Message"

```
Automatically stages and commits modified tracked files.

---

### 4.7 Removing Files
```

git rm file1.js
git rm --cached file1.js

```
Deletes files from the working directory or untracks them while keeping the file.

---

### 4.8 Renaming or Moving Files
```

git mv file1.js file1.txt

```
Renames or moves a file while tracking history.

---

### 4.9 Viewing Changes
```

git diff
git diff --staged
git diff --cached

```
Displays line-by-line differences between file states.

---

### 4.10 Viewing Commit History
```

git log
git log --oneline
git log --reverse

```
Shows commit history and metadata.

---

### 4.11 Viewing Specific Commits
```

git show 921a2ff
git show HEAD
git show HEAD~2
git show HEAD:file.js

```
Displays detailed commit information or previous file versions.

---

### 4.12 Unstaging Files
```

git restore --staged file.js

```
Removes a file from the staging area without changing the working directory file.

---

### 4.13 Discarding Local Changes
```

git restore file.js
git restore file1.js file2.js
git restore .
git clean -fd

```
Reverts or removes modifications and untracked files.

---

### 4.14 Restoring Earlier Versions
```

git restore --source=HEAD~2 file.js

```
Retrieves an earlier version of a file from a previous commit.

---

## 5. Complete Workflow Example

```

git init
git add .
git commit -m "Initial commit"

git status
git diff
git add file1.js
git commit -m "Added module"

git log --oneline
git restore --staged file1.js
git restore file1.js
git show HEAD~1:file1.js

```

---

## 6. Summary of Key Git Commands

| Task | Command | Description |
|------|---------|-------------|
| Configure Git | `git config --global -e` | Edit global configuration |
| Initialize Repo | `git init` | Create new repository |
| Stage Files | `git add file` | Add to staging area |
| View Status | `git status` | Show tracking state |
| Commit Changes | `git commit -m "msg"` | Save snapshot |
| Quick Commit | `git commit -am "msg"` | Stage and commit modified tracked files |
| Remove File | `git rm file` | Delete and untrack file |
| Rename File | `git mv old new` | Rename or move file |
| Compare Changes | `git diff` | View differences |
| View History | `git log --oneline` | Display commit history summary |
| Inspect Commit | `git show HEAD` | Show commit details |
| Unstage File | `git restore --staged file` | Undo staging |
| Discard Changes | `git restore file` | Revert working changes |
| Clean Untracked | `git clean -fd` | Remove untracked files |
| Restore Old Version | `git restore --source=HEAD~2 file` | Retrieve older file version |

---

## 7. Important Command Line (CMD / Shell) Commands

| Command | Meaning |
|--------|---------|
| `dir` | Lists non-hidden contents of current directory |
| `dir /a` | Lists all contents including hidden files |
| `start .` | Opens the current directory in file explorer |
| `start <filepath>` | Opens specified folder or file |
| `echo <content> > <filename>` | Writes content into a file |

---

End of Document.
```


