2023-12-19 01:39

Status: #idea

Tags: [[programming]]

# git

**Git** is a [[DevOps]] tool used for source code management. It is a free and open-source version control system used to handle small to very large projects efficiently. 

Git is used to tracking changes in the source code, enabling multiple developers to work together on non-linear development. [[Linus Torvalds]] created Git in 2005 for the development of the [[linux]] [[kernel]].

Git [[SCM]] (Source Control Manager)


git commands:

```bash
git init
git commit
git diff //check difference in commit
git restore --staged index.html // remove from index.html from staging and move it to working environment
git commit -a -m "commit text" //skip staging and go straight to commit
git rm "secret file" //remove the file name "secret file"
git restore "file-name" //restore deleted file 
git log //show git commit history log
git log --oneline //git log but only the commit message
git commit --amend -m "message"  //change the most recent commit message
git log -p
git rebase //GMT!

//branches
git branch //see list of branches
git branch branch-name //create new branch
git checkout branc-name //switch branch
git merge -m "merge branch-name to master" branch-name //merge a branch to its parent(master)
git branch -d remove-name //delete a branch
git switch -c brahcn-name //-c(create) create and switch to the new branch
git checkout - //go to previous branch

git fetch //get changes from remote to local repo

git pull //same as fetch but without the git merge command
```

git command for pushing existing repo to github:
```bash
git init
git add -A
git commit -m 'Added my project'
git remote add origin "git.url"
git push -u -f origin main //-u --set-upstream
```


# References
Git and Github tutorial for beginners - Kevin Stratvert



