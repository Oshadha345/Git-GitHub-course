# 🛠️ Comprehensive Git Workflow Guide


```
Oshdha Samarakoon 
```


---

## **1. Setting Up Git**

### 🚀 Install Git
- **🐧 Linux:**
  ```bash
  sudo apt-get update
  sudo apt-get install git
  ```
- **🪟 Windows:** Download from [git-scm.com](https://git-scm.com/).
- **🍎 macOS:**
  ```bash
  brew install git
  ```

### ⚙️ Configure Git
```bash
git config --global user.name "👤 Your Name"
git config --global user.email "📧 your.email@example.com"
```

✔️ Verify configuration:
```bash
git config --list
```

---

## **2. 🗂️ Initialize a Repository**

### 🆕 Create a Local Repository
```bash
mkdir my-repo
cd my-repo
git init
```

---

## **3. 📁 Basic Operations**

### ➕ Add a File
```bash
echo "👋 Hello, Git!" > file1.txt
git add file1.txt
```

### 📝 Commit Changes
```bash
git commit -m "🎉 Initial commit"
```

### 🧐 View Status
```bash
git status
```

### 🕰️ View Commit History
```bash
git log
```

---

## **4. 🌐 Working with Remote Repositories**

### 🔗 Add a Remote Repository
```bash
git remote add origin https://github.com/username/repository-name.git
```

### 📤 Push Changes to Remote
```bash
git push -u origin main
```

#### ⚠️ Issue: **Push Rejected**
**💡 Error:**
```bash
! [rejected]        main -> main (fetch first)
```
**🛠️ Solution:**
1. ⬇️ Pull changes from the remote:
   ```bash
   git pull origin main --allow-unrelated-histories
   ```
2. 🧹 Resolve merge conflicts (if any).
3. 📤 Push changes:
   ```bash
   git push origin main
   ```

### ⬇️ Pull Changes from Remote
```bash
git pull origin main
```

---

## **5. 🌳 Branching and Merging**

### 🌿 Create a Branch
```bash
git branch feature-branch
```

### 🔄 Switch to a Branch
```bash
git checkout feature-branch
```

### 🔀 Merge a Branch
1. Switch to the branch you want to merge into (e.g., `main`):
   ```bash
   git checkout main
   ```
2. Merge the feature branch:
   ```bash
   git merge feature-branch
   ```

#### ⚠️ Issue: **Merge Conflicts**
**💡 Error:**
```bash
CONFLICT (content): Merge conflict in file.txt
```
**🛠️ Solution:**
1. 📝 Open the conflicting files and resolve conflicts.
2. ➕ Stage resolved files:
   ```bash
   git add file.txt
   ```
3. 📝 Commit the merge:
   ```bash
   git commit -m "✅ Resolved merge conflicts"
   ```

---

## **6. 🔄 Reverting and Resetting**

### ⏪ Revert a Commit
```bash
git revert <commit-hash>
```

### 🔃 Reset to a Previous Commit
- **🛑 Soft Reset:** Keep changes in staging area:
  ```bash
  git reset --soft <commit-hash>
  ```
- **❌ Hard Reset:** Discard changes:
  ```bash
  git reset --hard <commit-hash>
  ```

---

## **7. 🏪 Stashing Changes**

### 💾 Save Changes Without Committing
```bash
git stash
```

### 🛠️ Apply Stashed Changes
```bash
git stash apply
```

### 🗑️ Drop Stash
```bash
git stash drop
```

---

## **8. ❌ Deleting Branches**

### 🗑️ Delete a Local Branch
```bash
git branch -d feature-branch
```

### 🌐 Delete a Remote Branch
```bash
git push origin --delete feature-branch
```

---

## **9. 🏷️ Tagging**

### 🏷️ Create a Tag
```bash
git tag -a v1.0 -m "Version 1.0"
```

### 📤 Push Tags
```bash
git push origin v1.0
```

---

## **10. ⚠️ Common Issues and Solutions**

### 🗂️ Problem: Untracked Files
**💡 Error:**
```bash
error: pathspec 'file.txt' did not match any file(s) known to git
```
**🛠️ Solution:**
Ensure the file is added:
```bash
git add file.txt
```

### 🌀 Problem: Detached HEAD
**💡 Error:**
```bash
You are in 'detached HEAD' state.
```
**🛠️ Solution:**
1. Create a branch from the current state:
   ```bash
   git checkout -b temp-branch
   ```
2. Switch back to the main branch and merge:
   ```bash
   git checkout main
   git merge temp-branch
   ```

### 🚧 Problem: Refusing to Merge Unrelated Histories
**💡 Error:**
```bash
fatal: refusing to merge unrelated histories
```
**🛠️ Solution:**
Use the following command:
```bash
git pull origin main --allow-unrelated-histories
```

---

## **11. 🚀 Advanced Operations**

### ⚙️ Interactive Rebase
```bash
git rebase -i HEAD~n
```

### 🧱 Squash Commits
During rebase, change `pick` to `squash` for the commits to combine.

---

## **12. 🌟 Best Practices**

1. **✔️ Commit Often:** Make small, logical commits.
2. **📝 Write Clear Messages:** Use descriptive commit messages.
3. **⬇️ Pull Before Push:** Always pull changes from the remote before pushing.
4. **🌳 Use Branches:** Isolate features and fixes in separate branches.
5. **⚠️ Avoid Force Push:** Only use `git push -f` when absolutely necessary.

---

## **13. 📚 Resources**
- [📖 Git Official Documentation](https://git-scm.com/doc)
- [📘 GitHub Guides](https://guides.github.com/)

---

This guide provides a 🏁 complete workflow for using Git, covering basic to advanced operations and addressing common issues. Follow these steps to master Git effectively.

