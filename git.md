---
marp: true
paginate: true
---


![bg right:30%](figures/linus.jpg)



# What is git

- Git is a “Control Version System” (CVS),
- To take track of modifications on text files (source code but non only),
- Can be used locally (as an archive) or with a remote server, like Gihub, Gitlab, Gitea for collaboration.
- Many development tools are now linked with git 

![alt text](figures/git.png)


---

# How does git works?

- Git stores the differences between to version of the same file (when it’s possible)
- The history is never deleted (beware when uploading big files)
- You can work on several version of the same file using branches

### Train with git

https://learngitbranching.js.org
 
![bg left:40%](figures/xkcd.png)

---

# Some git vocabulary

**repository**: a folder containing the files that are tracked by the git system

**commit**: the basic operation in git to validate modifications to the code.  A commit is a version of the content of the repository. In practice, it contains the difference with respect to the previous commit.

**work copy**: the status of the file in the repository. Some files may have uncommitted changes or not even be tracked by git.


--- 

# Some git vocabulary

**staged files**: the files and changes that will be included in the next commit. Files can be added to that list thanks to the command git add.

**branch**: git can track several version of the same repository, called branchs 

**local & remote repository**: change are usually done on a local version of the repository, and are then synchronised with a remote copy of it (on Github, Gitlab, Gitea, or other) to allow collaboration. 

---


# Let's try it now with a example!

1. Clone the test repository: ``git clone git@github.com:nbrucy/git_tuto.git``

2. Check the working copy ``ls -l``

3. Check the status  `git status` 
   ℹ️ Some tools like `gitg` allows to do it with a graphic interface.
   
4. Check previous commit `git log` 
   
5. Do a modification (see next slide)

---

# Basic git workflow

1. `git clone` or  `git init` → only once : create a repository
2. `git pull` → *fetch* new *commits* from the *remote repository* and *merge* them with the local version
3.  Modify file.example 
4. `git add file.example`
5. `git commit -m “Changed the example”` →  Validate the changes. Commit messages are important to keep track of what modifications where made
6. `git status` → Check if the repository status is as expected
7. `git push` → Upload the modifications to the remote repository

--- 


# Deal with conflicts

---

# Working with branches

![bg right:22%](figures/branch.png)

Branch are useful to develop feature or bugfix in parallel

### The basic commands:

- `git checkout -b bugfix` Create a new branch and switch to it
- `git checkout main` Switch to another branch
- `git merge bugfix` Merge the branch `bugfix` into the main branch

### Merging branches

In a colloborative environnement, merging is better done using the *Merge request* or *Pull request* feature of Gitlab/Github

---


# Some useful tricks

- `git commit --amend` Update the last commit. 
    :warning: Do it only if the last commit was not pushed on the remote


