# git Tutorial

```
//from working dir --> Staged dir
git add .

// to commit
git commit -m "message" -d "description"

//add origin
git remote add origin "origin url"

//change origin url
git remote set-url origin "url"

//display origin 
git remote -v

//push
git push -u origin main

//pull
git pull origin main

//show branch
git branch

//create branch
git branch "branch-name"


//create and move into branch
git checkout -b "branch-name"


//move into branch
git checkout branch


//delete branch
git branch -d "branch-name"

// set-upstream to push changes on new branch
git push --set-upstream origin branch-name

//check status of an staged directory
git status

//check logs of commit
git logs --oneline 


//undo from staged dir --> working dir
git restore .
git restore <filename>

//Restore a specific file from a previous commit:
git checkout <commit-hash> -- <file-name>

//Revert a specific commit:
git revert <commit-hash>


//Revert multiple commits:
git revert <commit-hash1> <commit-hash2> ...

//Revert and squash into a single commit:
git revert -n <commit-hash>
git commit

//Reset cmd:
git reset --soft <commit-hash>
git reset --mixed <commit-hash>
git reset --hard <commit-hash>


// staged --> working dir
git restore --staged <file>
git restore .
git rm --cached <file>

```