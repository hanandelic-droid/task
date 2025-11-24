# Go to home directory
cd ~

# Check current path
pwd

# Check git status (not in a repo yet)
git status

# Navigate to your project folder
cd ~/git-assignment

# Switch to main branch (already there) and try creating development branch
git checkout main
git checkout -b development

# Check git status (merge conflicts)
git status

# Open file to resolve conflict
nano feature_d.txt

# Stage resolved file
git add feature_d.txt

# Commit conflict resolution
git commit -m "Resolved merge conflict in feature_d.txt"

# Push development branch (403 error initially)
git push -u origin development

# Check branches
git branch

# Checkout development branch
git checkout development

# Remove remote origin
git remote remove origin

# Try push again (no remote)
git push -u origin development

# Add remote origin with token (for authentication)
git remote add origin https://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@github.com/hanandelic-droid/git-assignment.git

# Verify remote
git remote -v

# Push development branch (still denied)
git push -u origin development

# Clean up and start over
rm -rf ~/git-assignment

# Clear cached credentials
git credential-cache exit
git config --global --unset credential.helper

# Recreate project folder
mkdir ~/git-assignment
cd ~/git-assignment
git init

# Create README
echo "# Git Assignment" > README.md
git add README.md
git commit -m "Initial commit: Added README file."
git log --oneline

# Add remote repo
git remote add origin https://github.com/hanandelic-droid/task.git
git remote -v

# Push main branch
git push -u origin main

# Create feature-A branch
git checkout -b feature-A
git add .
git commit -m "FEAT: Added content for feature A"

# Switch back to main and try HOTFIX commit
git checkout main
git commit -am "HOTFIX: Quick update directly on main"

# Switch to feature-A and rebase
git checkout feature-A
git rebase main

# Stage README.md (after resolving conflicts)
git add README.md
git rebase --continue

# Push feature-A branch
git push origin feature-A

# Create development branch
git checkout main
git checkout -b development

# Create feature-C branch
git checkout -b feature-C
echo "Feature C complete" > feature_c.txt
git add feature_c.txt
git commit -m "FEAT: Completed feature C"

# Create feature-D branch
git checkout development
git checkout -b feature-D
echo "Feature D complete" > feature_d.txt
git add feature_d.txt
git commit -m "FEAT: Completed feature D"

# Merge feature-C and feature-D into development
git checkout development
git merge feature-C
git merge feature-D


![Screenshot 1](screenshots/1.png)
![Screenshot 2](screenshots/2.png)
![Screenshot 3](screenshots/3.png)
![Screenshot 4](screenshots/4.png)
![Screenshot 5](screenshots/5.png)
