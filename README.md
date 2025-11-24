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
git commit

![Screenshot 1](screenshots/1.png)
![Screenshot 2](screenshots/2.png)
![Screenshot 3](screenshots/3.png)
![Screenshot 4](screenshots/4.png)
![Screenshot 5](screenshots/5.png)
