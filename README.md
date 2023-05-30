# learning git

## config

```shell
# global user name
git config --global user.name "$NAME"
git config --global user.email "$EMAIL"
```

## create a git repository

```shell
# create a project folder
mkdir learngit

# using git for version control
# change to project folder
cd learngit
# init git
git init .

# init project
touch README.md
touch README_en.md
# check status of current git project
git status

# track project files and save to cache
git add README.md
git add README_en.md

# edit README.md
vi README.md

# save to cache
git add README.md

# edit README_en.md and save to cache
vi README_en.md
git add README_en.md

# edit README_en.md again
vi README_en.md

# discard changes and restore from cache
git restore README_en.md

# commit
git add *
git commit -m "project init"
git tag "v0.0.1"


# workflow with personal branch
git checkout basebranch
touch addFileToMyPrivateBranch.txt
git add addFileToMyPrivateBranch.txt
git checkout -b dev_pri_user1
git commit -m 'add a new file to my personal branch'
# git push <remote> <local>
git push origin dev_pri_user1
# rename branch
git branch -m dev_pri_user1 dev_pri_user2
# push to remote 
git push origin dev_pri_user2
# delete old branch
git push origin -d dev_pri_user1

```