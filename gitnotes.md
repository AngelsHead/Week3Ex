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

