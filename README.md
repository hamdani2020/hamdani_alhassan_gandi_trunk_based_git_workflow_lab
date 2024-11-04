# Trunk Based Development Git Strategy Lab

This repository demonstrates the implementation of Trunk Based Development (TBD) git workflow strategy, focusing on maintaining a single main branch for production-ready code with optional short-lived feature branches.

## Overview
Trunk Based Development is a source-control branching model where developers collobarates on code in a single branch called trunk (main), resist creating long-lived development branches, and strive to maintain produciton-ready code at all times.

## Prerequistes
- Git installed on your local machine
- GitHub account
- Basic understanding of Git commands
- Text editor

## Getting Started
1. Clone the repository
```
git clone https://github.com/<username>/<fullname>_trunk_based_git_workflow_lab.git
cd <fullname>_trunk_based_git_workflow_lab
```

2. Create initial code:
```
# Add initial production code
echo "THIS IS PRODUCTION READY CODE" > main.txt
git add main.txt
git commit -m "Add main.txt for production ready code"
git push -u origin main
```

## Lab Tasks
1. Main Branch Management
	- Create and maintain production-ready code in the main branch
	- implements direct commits for small changes
	- Ensure code quality through testing and reviews

2. Feature Branch Development
```
# Create feature branch
git checkout -b mfa_feature

# Make changes
echo "THIS IS PRODUCTION READY CODE secured with MFA" > main.txt
git add main.txt
git commit -m "Added mfa feature"
git push -u origin mfa_feature
```

3. Pull Request Process
	1. Create PR from feature branch to main
	2. Review code changes
	3. Merge feature into main
	4. Delete feature branch after successful merge

4. Hotfix Implementation
```
# Switch to main and revert changes
git checkout main
git revert -m 1 <merge-commit-hash>
git push origin main
```
## Branch Structure
- `main`- Production-ready code
- `freature/*`- Short-lived feature branches(optional)
