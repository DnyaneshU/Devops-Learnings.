
# Git Learnings

## 1. What Is Git?

Git is a **Distributed Version Control System (DVCS)** used to track and manage changes in code. It allows multiple developers to collaborate efficiently by maintaining a complete history of modifications in a repository. Git ensures reliability, version tracking, and parallel development across teams.

---

## 2. Types of Version Control Systems (VCS)

### **2.1 Distributed Version Control System (DVCS)**
Every developer has a complete copy of the repository, including the full version history. Work can be done offline and synced later.

**Advantages:** Faster, offline support, seamless collaboration  
**Examples:** Git, Mercurial, Bazaar

### **2.2 Centralized Version Control System (CVCS)**
A single central server holds the main repository. Developers must connect to the server for changes.

**Advantages:** Simple to set up  
**Disadvantages:** Server failure can disrupt development  
**Examples:** SVN, CVS, Perforce

---

## 3. Tools for Working with Git

### **Git Bash**
A command-line interface that provides a Unix-like terminal on Windows, enabling full Git functionality.

### **Git GUI**
A graphical interface useful for basic Git operations like staging and committing, though less powerful than Git Bash.

---

## 4. Creating Snapshots in Git

Git records the state of files using snapshots. These are created using commit commands after staging changes.

---

### **4.1 Configuring Git**

Set your identity and preferences before using Git:

#### 1. Set Your Name
```bash
git config --global user.name "Your Full Name"
````

#### 2. Set Your Email (Use your GitHub email)

```bash
git config --global user.email "your-email@example.com"
```

#### 3. Set VS Code as the Default Editor

```bash
git config --global core.editor "code --wait"
```

#### 4. Normalize Line Endings (Recommended for Windows Users)

```bash
git config --global core.autocrlf true
```

#### 5. Verify Configuration

```bash
git config --global --list
```

#### 6. Edit Config File Manually (Optional)

```bash
git config --global -e
```

---

### **4.2 Initializing a Repository**

```bash
git init
```

### **4.3 Staging Files**

```bash
git add file1.js
git add file1.js file2.js
git add *.js
git add .
```

### **4.4 Viewing Current Status**

```bash
git status
git status -s
```

### **4.5 Committing Staged Files**

```bash
git commit -m "Commit message"
git commit      # Opens editor
```

### **4.6 Skipping Staging (Direct Commit for Tracked Files)**

```bash
git commit -am "Commit message"
```

### **4.7 Removing Files**

```bash
git rm file1.js
git rm --cached file1.js   # Keep file locally, remove from tracking
```

### **4.8 Renaming or Moving Files**

```bash
git mv old.js new.js
```

### **4.9 Viewing Changes**

```bash
git diff
git diff --staged
git diff --cached
```

### **4.10 Viewing Commit History**

```bash
git log
git log --oneline
git log --reverse
```

### **4.11 Viewing Specific Commits**

```bash
git show <commit-id>
git show HEAD
git show HEAD~2
git show HEAD:file.js
```

### **4.12 Unstaging Files**

```bash
git restore --staged file.js
```

### **4.13 Discarding Local Changes**

```bash
git restore file.js
git restore .
git clean -fd   # Remove untracked files
```

### **4.14 Restoring Previous Versions**

```bash
git restore --source=HEAD~2 file.js
```

---

## 5. Complete Workflow Example

```bash
git init
git add .
git commit -m "Initial commit"

git status
git diff
git add file1.js
git commit -m "Added new module"

git log --oneline
git restore --staged file1.js
git restore file1.js
git show HEAD~1:file1.js
```

---

## 6. Summary of Key Git Commands

| Task                | Command                            | Description                    |
| ------------------- | ---------------------------------- | ------------------------------ |
| Configure Git       | `git config --global -e`           | Edit global configuration      |
| Initialize Repo     | `git init`                         | Create new repository          |
| Stage Files         | `git add file`                     | Move to staging area           |
| View Status         | `git status`                       | View tracked/untracked changes |
| Commit Changes      | `git commit -m "msg"`              | Save snapshot                  |
| Quick Commit        | `git commit -am "msg"`             | Stage & commit tracked files   |
| Remove File         | `git rm file`                      | Delete and untrack             |
| Rename File         | `git mv old new`                   | Move/rename file               |
| Compare Changes     | `git diff`                         | View modifications             |
| View History        | `git log --oneline`                | Compact commit history         |
| Inspect Commit      | `git show HEAD`                    | Show details of last commit    |
| Unstage File        | `git restore --staged file`        | Undo staging                   |
| Discard Changes     | `git restore file`                 | Revert file changes            |
| Clean Untracked     | `git clean -fd`                    | Remove untracked files         |
| Restore Old Version | `git restore --source=HEAD~2 file` | Restore older version          |

---

## 7. Useful Command Line (CMD / Terminal) Commands

| Command                | Description                     |
| ---------------------- | ------------------------------- |
| `dir`                  | List contents of directory      |
| `dir /a`               | List all files including hidden |
| `start .`              | Open current folder in Explorer |
| `start <file/folder>`  | Open file or directory          |
| `echo <text> > <file>` | Write text to file              |

---

*End of Document.*

```


