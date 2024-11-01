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


```