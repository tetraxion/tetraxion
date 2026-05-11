# 🔧 Git Commands Cheat Sheet

Quick reference untuk Git commands yang sering digunakan.

## 🚀 Push Pertama Kali

```bash
# Add semua file
git add .

# Commit dengan message
git commit -m "✨ Add advanced GitHub profile README with workflows"

# Push ke GitHub
git push origin main
```

---

## 📝 Update README

```bash
# Setelah edit README.md
git add README.md
git commit -m "📝 Update README content"
git push origin main
```

---

## 🔄 Update Workflows

```bash
# Setelah edit workflows
git add .github/workflows/
git commit -m "⚙️ Update GitHub Actions workflows"
git push origin main
```

---

## 🎨 Update Customization

```bash
# Setelah customization
git add .
git commit -m "🎨 Customize profile README"
git push origin main
```

---

## 📊 Check Status

```bash
# Lihat file yang berubah
git status

# Lihat perubahan detail
git diff

# Lihat commit history
git log --oneline
```

---

## 🔍 Useful Commands

```bash
# Undo changes (sebelum commit)
git checkout -- README.md

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Undo last commit (discard changes)
git reset --hard HEAD~1

# Pull latest changes
git pull origin main

# Create new branch
git checkout -b feature/new-feature

# Switch branch
git checkout main

# Merge branch
git merge feature/new-feature
```

---

## 🌿 Branch Management

```bash
# List all branches
git branch -a

# Delete local branch
git branch -d branch-name

# Delete remote branch
git push origin --delete branch-name

# Rename current branch
git branch -m new-name
```

---

## 🔧 Configuration

```bash
# Set username
git config --global user.name "Your Name"

# Set email
git config --global user.email "your.email@gmail.com"

# Check config
git config --list
```

---

## 🚨 Emergency Commands

```bash
# Discard all local changes
git reset --hard HEAD

# Clean untracked files
git clean -fd

# Stash changes
git stash

# Apply stashed changes
git stash pop

# List stashes
git stash list
```

---

## 📦 Commit Message Conventions

```bash
✨ feat: New feature
🐛 fix: Bug fix
📝 docs: Documentation
🎨 style: Formatting, styling
♻️ refactor: Code refactoring
⚡ perf: Performance improvement
✅ test: Adding tests
🔧 chore: Maintenance
🚀 deploy: Deployment
🔒 security: Security fix
```

**Examples**:
```bash
git commit -m "✨ feat: Add snake animation workflow"
git commit -m "🐛 fix: Fix broken portfolio link"
git commit -m "📝 docs: Update setup guide"
git commit -m "🎨 style: Improve README formatting"
```

---

## 🎯 Quick Workflow

### Daily Updates
```bash
git pull origin main          # Get latest changes
# ... make your changes ...
git add .                     # Stage changes
git commit -m "📝 Update"     # Commit
git push origin main          # Push
```

### Feature Development
```bash
git checkout -b feature/new-feature    # Create branch
# ... develop feature ...
git add .
git commit -m "✨ feat: Add new feature"
git push origin feature/new-feature
# Create Pull Request on GitHub
```

---

## 💡 Pro Tips

1. **Commit Often**: Small, frequent commits are better
2. **Write Clear Messages**: Describe what and why
3. **Pull Before Push**: Always pull latest changes first
4. **Use Branches**: Don't work directly on main
5. **Review Before Commit**: Check `git diff` first

---

## 🔗 Useful Links

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

---

**Happy Git-ing! 🚀**
