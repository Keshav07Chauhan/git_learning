## **IMP POINTS** : 

* Git(is a Software) is a version control system that allows you to track changes to your files & collaborate with others.
* GitHub is a web based hosting service for git repo.
* In Sci fi language, we can say: 
    * Repository(repo) -> folder
    * Branch -> alternative timeline
* Empty folders are not going to be tracked by git.
* If required to put empty folder, then, a file named `.gitkeep` is placed in that folder.
* For help: `git --help` | `git -h`
* To secure imp. info. from public, `.gitignore` file is used and in which name of all the private(not to show to public) files and folders are placed.
    * example files and folders are `node_modules` & `.env`
* WORKFLOW:
    * git init (once for each repository)
    * git add (to add files to the repository)
    * git commit (to save changes)
    * git push (to push changes to github or remote repo)

# Git commands
---

## 1. Setup & Configuration

```bash
git --version  | git -v
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global --list
```

---

## 2. Create & Clone Repositories

```bash
git init
git clone <repository_url>
```

---

## 3. Basic Workflow

```bash
git status
git add <file1> <file2> 
git add .
git commit -m "commit message"
```

---

## 4. Branching

```bash
git branch
git branch <branch_name>
git checkout <branch_name>
git checkout -b <branch_name>
git branch -m <old_branch_name> <new_branch_name>
git branch -d <branch_name>
```
**head** is a pointer to the current branch that you are woring on.

Modern alternative (clearer, less error‑prone):

```bash
git switch <branch_name>
git switch -c <branch_name>
```

---

## 5. Merging & Rebasing

```bash
git merge <branch_name>
git rebase <branch_name>
```

**NOTE**: 
* Merge keeps history explicit. Rebase rewrites it.
* *How to merge*: go to the branch where you want to merge code, then, write the name of branch in command from which you want to merge code😊.

---

## 6. Remote Repositories

```bash
git remote -v
git remote add origin <url>
git push origin <branch>
git push -u origin <branch>
git pull origin <branch>
```

---

## 7. Stashing (Temporary Saves)

```bash
git stash
git stash list
git stash apply
git stash pop
git stash drop
```

Stashing constantly will create problem. ( workflow is broken )

---

## 8. Undoing Mistakes (Critical Section)

### Unstage a file

```bash
git reset <file>
```

### Discard local changes

```bash
git checkout -- <file>
```

### Amend last commit

```bash
git commit --amend
```

### Reset commits

```bash
git reset --soft HEAD~1
git reset --hard HEAD~1
```

`--hard` deletes work. If run it blindly.

---

## 9. Viewing History

```bash
git log
git log --oneline --graph --all
git diff
git diff --staged
```

**NOTE**: *If you don’t read `git log`, you don’t understand your project.*

---

## 10. Tags & Releases

```bash
git tag
git tag v1.0.0
git push origin v1.0.0
git tag -d v1.0.0
```

---

## 11. Cleaning the Working Directory

```bash
git clean -n
git clean -f
git clean -fd
```

Always run `-n` first otherwise you can delete the wrong files.

---

## 12. Useful Shortcuts (Optional but Smart)

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm "commit -m"
```

---

