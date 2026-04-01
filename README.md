# Using Git with Ansible 101 Demo Project 

ORIGINAL FILE: Standardized Red Hat AAP project structure.  
BEST PRACTICE: Provide a README.md (markdown) file with instructions.  ftw you can preview it in vscode.

ONE change - going to conflict.

## Simple CLI Test for Ansible

```bash

ansible-playbook -i inventory/hosts.yml playbooks/system_info.yml

```

##  Reference: Very First Steps Completed

### Create the Repo on GitHub (Manual Step)

Git needs a destination:

* Go to GitHub.com and log iPn.
* Click the + icon (top right) and select New repository.
* Name it B-git-primer 
* Crucial: Do not check "Initialize this repository with a README" (since you already have one).
* Click Create repository.

### Get the local files to the Repo

```

git init
git status
git add .
git commit -m "Initialize repo with basic files"
git branch -M main
git remote add origin git@github.com:ppremru/B-git-primer.git
git push -u origin main

```

## Git Workflow: "demo-1" Exercise

With an existing GitHub repo, practice branching strategy, follow these steps to update a playbook.

```
# Prep:
#   From GitHub, copy the [repository-url] to clone
#   git clone [repository-url]
#   cd ./B-git-primer

# Hints in VsCode:
#   Select Auto Save
#   README.md is a markdown file, use preview
#   after edits, notice the "M" flags Modified state of a file

# admire your environment
git status
git branch
git checkout -b demo-1
git branch

# edit hello_world.yml and README.md
git status
git add playbooks/hello_world.yml README.md
git status
git commit -m "Modifications for demo-1"
git status
git push -u origin demo-1

# Via GitHub UI, 
#   Create Pull Request 
#   Merge Pull Request, squash comments and delete branch
#   Assumption is no merge conflicts

git checkout main
git pull
git branch -d demo-1
```
