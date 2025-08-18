# Git Commands Guide

1. Setup & Configuration

# Set username
git config --global user.name "Your Name"
# Set email
git config --global user.email "your_email@example.com"
# Check settings
git config --list

#2. Create or Clone a Repository
# Initialize a new Git repository
git init
# Clone an existing repository
git clone https://github.com/username/repository.git

#3. Basic Workflow
# Check status of changes
git status
# Add files to staging area
git add filename.txt
# Add all files
git add .
# Commit changes with message
git commit -m "Your commit message"
# Push changes to remote repo
git push origin main

#4. Branching & Merging
# Create a new branch
git branch feature-branch
# Switch to a branch
git checkout feature-branch
# Create & switch in one command
git checkout -b feature-branch
# Merge branch into main
git checkout main
git merge feature-branch
# Delete branch (local)
git branch -d feature-branch

#5. Viewing History
# View commit history
git log
# One-line history
git log --oneline
# See branches and commits visually
git log --oneline --graph --all

#6. Undoing Changes
# Unstage a file (but keep changes)
git reset filename.txt
# Discard local changes (careful!)
git checkout -- filename.txt
# Undo last commit (keep changes staged)
git reset --soft HEAD~1
# Undo last commit (remove changes)
git reset --hard HEAD~1
# Revert a specific commit (safe way)
git revert <commit-hash>

#7. Remote Repositories
# Add remote repo
git remote add origin https://github.com/username/repository.git
# Verify remote
git remote -v
# Push to remote
git push -u origin main

#8. Stashing Changes
# Save current changes temporarily
git stash
# List stashed changes
git stash list
# Apply last stashed change
git stash apply
# Apply and drop last stash
git stash pop

#9. Tags
# Create a new tag
git tag v1.0
# Push tags to remote
git push origin --tags

#10. Helpful Shortcuts
# Show differences in files
git diff
# Show current branch
git branch --show-current
# Delete untracked files
git clean -f

#Tip:
git help <command>

# Pull latest changes from remote repo
git pull origin main
