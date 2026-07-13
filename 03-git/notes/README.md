# Git

What is Git ?
- Git isnt something that just stores code, in fact it is the foundation of how modern teams collaborate, build, test, ship and even recover from when an engineer breaks a production at lets say 2 am. 

## Version Control

- Something that seems simple however is essential for any DevOps/Engineering workflow.
  1. It tracks changes to code over time
  2. Lets you undo, inspect and collaborate
  3. Its like a time machine where you can review previous codes. 





## Centralised (SVN) vs Distributed (VCS)

- Centralised server is where everyone back then would work off, suppose if the server went down it was game over , you couldnt commit, update or work. It would lead to a merge of conflicts. 
- Then came 2005 where Linus Toravlds lost access to an important tool called bitkeeper, Linus being Linus came up with an idea why not write my own verison control, a few years later Git was born. 
- Git changed everything, instead of relying on one server, every developer like myself  has a fully copy of the repo. 

<img width="488" height="254" alt="image" src="https://github.com/user-attachments/assets/9a006295-b0e7-4c97-9332-19cd34c4c8d8" />


## Git Architecture and Internals 

Git is not a File Tracker !

- In fact what Git tracks is snapshots, eveytime you do a commit  or a change, Git takes a snapshot  not of the line you just changed but the whole file. For example, if you was to change one line it would save that verison of the file efficently. 
- Git uses a key value store called SHA-1 hash which are long files of string that uniquely represent the contents of your file. So no two different blobs or file contents would have the same hash.

- In simple words, its not just a tracker its a smart,compress hash-based snapshot engine.

<img width="480" height="241" alt="image" src="https://github.com/user-attachments/assets/e94d3839-9bde-4777-8ac3-2cbb15766b41" />


## Git Terminology and Key Concepts 

- Repository: A git project with all your files stored
- Commit: A snapshot of your files and metadata (author,timestamp,message etc)
- Branch: A movable pointer to a specific commit
- Remote: A reference to an external Git host (like GitHub, GitLab) usually named origion
- Staging Area: A buffer between your working directory and the repo what you plan to commit
- Blobs: Stores the actual contents of your file (just the data, no filename/path)
- Trees: Stores filenames, filepaths, and pointers to blobs (files) and other trees (directories)
- Refs (Reference): Pointer to a commit: branches(refs/heads), tags (refs/tags), and special ones like HEAD
- Index: the actual file .git/index, a binary file that holds the staging area info
- HEAD: pointer to the current branch or commit your working on
- Object Store: .git/objects/- where Git stores all blobs,trees,and commits by SHA hash
- Tag: a ref to a specific commit, often used for marking releases

## The .git directory 

- The .git directory is the brain of your project, it stores everything that Git needs for it to function (history, configurations, branches etc)

  <img width="479" height="250" alt="image" src="https://github.com/user-attachments/assets/35840181-49e4-4761-a6d5-4d7f6004ae45" />

## Git Common Commands 

- git innit: initalises a new Git repo with .git directory
- git add: stage changes
- git commit: snapshot changes
- git staged: shows staged/unstaged work
- git log: shows commit history
- git diff: shows what changed
- git config: set user/email
- git help <command>: built-in docs
- git clone: copy a remote repo
- git rm: remove files
- git mv: rename files
- git restore: undo file changes (modern)

## Areas of Git

1. Working directory: where your actively editing your files whether its a python script or a terraform module
2. Staging Area: This is where you put files that your planning to commit
3. Repository: Where all your files are stored

- Important Note ! Just running git add wont save your file , you need to commit it by using the git commit command. 


## Viewing History Commands

- git log: allows you to see commit history
- git log --online --graph: shows a visual branch layout, very useful when dealing with merge changes
- git show <commit>: Used to view a specific commit
- git diff: compares unstaged vs last commit, very useful to see what you broke before
- git diff --staged: compares staged vs last commit
- git blame <file>: shows who last change each line
- git reflog: view local HEAD history(even deleted branch)

## Git vs GitHub

- Many people get confused and think Git is Github, however this is a misconception and in fact Git is a CI/CD version control tool that you use to make changes on GitHub
- GitHub on the other hand is a cloud based platform service, it hosts your repo online so you can collaborate witb others, track issues, review codes etc.
- Git runs locally whereas Github runs on the cloud
- Git works offline whereas Github doesnt
- Git is open source whereas GitHub is owned by Microsoft.

## Branching

- Branching 101: Branching essentially allows you to work on multiple things at once without messing up your main project.


<img width="396" height="234" alt="image" src="https://github.com/user-attachments/assets/ac48a00f-6adf-4de8-84b8-9a7326d26f97" />

## Merging

- Merging in Git is when you combine changes from one branch into another
- git merge: merge target into current branch

## Visualise Branches and logo 
<img width="301" height="108" alt="image" src="https://github.com/user-attachments/assets/34ac765b-6c66-4025-adfb-b3bd46c365a2" />

## Rebase vs Merge

- Merge is safe and friendly, it brings two branches together and preserves the full history, it also add a merge commit so you can where the branches have joined.
- Rebase is a bit more advanced it rewrites your git history to make it seem like it was written by the latest commit.

## Git Stash & Pop

- Git Stash is essentially a temporary storage box for your changes
- git stash: it hides away all your uncommited changes
- git stash list: view all stashes
- git stash apply: reapplies the latest stash
- git stash pop: reapplies the latest stash and deletes it right after
- These commands are very useful when switching branches mid task

## Reset,Revert and Cherry-pick

- git revert: it creates a brand new commit and undoes the effect of the previous one, it doesnt mess with the history and is widely used in production.
- git reset: moves the pointer backwards and there is three types - 1. soft = keeps all changes, 2. Mixed= unstages your changes, 3. Hard= Nukes everything
- git cherry-pick: allows you to apply a single commit from another branch to your current one. Useful for hotfixes or target changes.

 <img width="464" height="191" alt="image" src="https://github.com/user-attachments/assets/db01380d-7839-4067-9a73-00177c6eabdb" />
 
## Fork and Pull Requests

- Fork  essentially is  your own copy of someone elses repo on GitHub, you can then clone the forked repo to your local machine and make changes to GitHub. In order to propose the changes you need  make a pull request, in simple terms its where the owner can review your code and merge changes.
- This is mainly used in open source projects and cross-team workflows.

## Collaborating Practices

- 
  
