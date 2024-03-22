## Week 03: Git over here..
The first thing you **always** need to do is to **load the git module to the current version.**
```bash
module load git/2.39.0
```
To make commits, first you must stage them but just using `git add`. 

If you want to all files in a specific dir (here: 'scripts') in the project:
```bash
git add scripts/*
```

To then make a commit, you just use:
```bash 
git commit -m "text"
```

use `>>` to add things to your text file. 
```bash
#EX:
echo "June 20, 1858: Send first draft to Huxley" >> todo.txt
```

To see if/what you've commited, check your git history. To do this:
```bash
git log --oneline
```

If you need to undo a change or accidently delete something, you can use git to restore:
```bash
git restore todo.txt
```

### General advice
- Use `git status` often.
- Make many, small commits regularly. Like quick saves. 
- Make the commit notes descriptive. 
- Try to just change one thing per commit. Makes it easier to track changes.

### Linking Repository to Github
Start by initating the repository.
```bash
git init
```
MOVE TO GITHUB. From there, create a new repository by clicking on the plus in the top right. 

**Make sure you have ssh selected.** The copy the link and come back to VS code.. 
```bash
git remote add -text- -link- 
```
- Replace text above with a name for the repo, and link with the link from github
- Then, you use `git push -u -text- main` to sync your local repo to the online version.
- `-u` flag only necessary for first time.
- Once you set it up, you just need `git push` to upload any and all commits to online.
- Additionally, once set up ypu dont need to "git add" anymore. Just `git push`. 

### Ignoring certian files
- Create `gitignore` files. (that then must be commited.. lol)
- This will create a **list** of all files for git to ignore. 
```bash
echo "data/" > .gitignore
echo "*~" >> .gitignore
```