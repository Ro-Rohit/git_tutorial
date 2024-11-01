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


//to stay up-to-date with main 
git checkout feature-branch
git rebase main

//Interactive Rebase
git rebase -i <base-branch>
git rebase -i HEAD~3

    pick: Keep the commit as-is.
    reword: Change the commit message without modifying the commit itself.
    edit: Pause the rebase at this commit to allow you to make changes to the commit.
    squash (or s): Combine this commit with the previous one, merging them into a single commit and prompting for a new commit message.
    drop: Remove the commit from the history.

  1. (SQUASH  COMMIT)
    pick abc1234 First commit message
    squash def5678 Second commit message
    squash ghi9012 Third commit message

  2. (REWORD COMMIT)
    pick abc1234 First commit message
    reword def5678 Second commit message
    pick ghi9012 Third commit message

  3.(EDIT COMMIT)
    pick abc1234 First commit message
    edit def5678 Second commit message
    fixup ghi9012 Third commit message

    git commit --amend <message>
    git rebase --continue

  
  4.(DROP COMMIT)
    pick abc1234 First commit message
    drop def5678 Second commit message
    pick ghi9012 Third commit message


//move a range of commits onto another branch
A---B---C---D (main)
     \
      E---F---G (feature)
git checkout feature
git rebase --onto main B feature


//to fetch changes from the remote branch and reapply your local commits ontop
git pull --rebase origin main



```