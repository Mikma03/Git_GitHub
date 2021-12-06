# Table of content

1. [Usefull link and materials](#Usefull-link-and-materials)

2. [Introduction](#Introduction)

3. [Git interface (Git Bash) commands and work flow](<#Git-interface-(Git-Bash)-commands-and-work-flow>)

4. [Branches](#Branches)

5. [Git-Stash](#Git-Stash)

6. [Merge conflict](#Merge-conflict)

7. [Git Revert and Git reset](#Git-Revert-and-Git-reset)

8. [How to change names of commits](#How-to-change-names-of-commits)

9. [Fork and Pull Request](#Fork-and-Pull-Request)

10. [Git history](#Git-history)

11. [Pull request](#Pull-request)

# Usefull link and materials

[Add Image to GitHub Readme.md from Google Drive](https://stackoverflow.com/questions/52063556/add-image-to-github-readme-md-from-google-drive/70200170#70200170)

[When local branch and remotely branch are differen and you want work on one branch](https://stackoverflow.com/questions/69863948/git-creates-a-new-branch-despite-commit-how-to-fix-this)

[Git Ignore files - templates](https://github.com/github/gitignore)

# Introduction

Introduction to GIT flow using GIT Bash and GitHub.

This reposytary consist of usefull knowladge about GIT flow. Mainly this reposytary was created based on:

- Course created by Bogdan Stashchuk and available here: [Link](https://subscription.packtpub.com/video/web_development/9781800209855/p1/video1_1/introduction)

Moreover there is complete book which cover most information about GIT [Link](https://git-scm.com/book/en/v2)

Additionally documentation for GIT is avaliable here [Link](https://docs.github.com/en/get-started)

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=15RSv1aY_71BH8cekrD8fihYPDXeS0OFT" />
</p>

# Git interface (Git Bash) commands and work flow

1. When we want to check status of our repositary we can use:

> `git status`

2. Settings for user and user e-mail

> `git config --global.username "YOUR NAME"`

> `git config --global user.email "YOUR EMAIL"`

3. When we want clear our console

> `clear`

4. When we changed somthing on local repositary (e.g. local PC) the GIT flow could look like that:

> `git add FILE NAME`

> `git commit -m "your commnet for changes you've done"`

> `git push`

5. When we add all changes whuch we've done perfect solution for that seems to be:

> `add *`

6. When we want add changes for two or more fles and we want skip step `git add`

> `git commit -a -m "your comment and explanation"`

7. History of commits

> `git log`

8. .gitignore

In case of this file we tell git which files will be untracked.

There is posbibility to create this file manually or when repositary is created.

[Commends for .gitignoge](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)

Also on GitHub there is a project which cosnsist of templates for gitignore in case of every language. [Link](https://github.com/github/gitignore)

If we wany to ignore any file inside of folder in gitignore file we can use `*/`

9. When we want to see particular file in catologe we can use:

> `git status -uall`

10. Flow how to add .gitignore file

    10.1. Create the text file `gitignore.txt`.

    10.2. Open it in a text editor and add your rules, then save and close.

    10.3. Hold SHIFT, right click the folder you're in, then select Open `command` window here.

    10.4. Then rename the file in the command line, with ren `gitignore.txt` `.gitignore`.

# Branches

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1H8TGpxkK1N1v9yD9_VSNCi0-1iiyW2pr" />
</p>

1. How can we check where we are in case of branch:

> `git branch`

2. When we want to create new branch we can use:

> `git branch NAME_OF_NEW_BRANCH`

3. When we want change branch means that we want change branch where we will be working atlassian

`git checkout NAME_OF_BRANCH`

4. When we want to make changes on our remotely repository and add new branch which is already exist on our local workspace we can use commend:

> `git push -u origin NAME_OF_NEW_BRANCH`

5. When we want to create new brach and autamatillcy checkout branch we can use:

> `git checkout -b NAME_OF_NEW_BRANCH`

6. When we want to see graph of our changes in console:

> `git log -oneline -graph -all`

7. When we wantto open GIU for Git to see our previous changes

> `gitk -all`

8. When we want merge commits from our branches we can use:

> `git merge <name of branch which will be merge to actuall branch>`

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HE29F10Rqktdg8GPQniRB4134YxZ8Kvo" />
</p>

# Git Stash

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HEmqiOj50tK2vWmeZWyzBGGMRUWQJgPq" />
</p>

1. When we want add something to storage we can use command:

> `git stash`

2. If we want check what is in our storage we should use:

> ` git stash list`

3. Changes in our storage are indexed and we can acess to then by

> `stash@{X}`

4. We can add multipletimes changes and updates and everytime our list will be reindexed moreover the latest index is our last change and this is index{0}.
   If we want identify difference between stash commit we can use:

> `git stash show stash@{X}`

    where ```{X}``` is number of stash commit

5. When our changes in storage are simillar or commend `git stash show` doesn't show the changes we are interested in then we can use:

> `git stash show stash@{X} -p`

6. In case when we change two or more files we can use

> `git stash save "Descriotion for our changes"`

7. When we want apply changes from storage to our file we can use below command, but in this case only the latest commit will be applied. Also in this case
   changes are still in storage.

> `git stash apply`

8. When we want delete changes from storage after adding those to file we can use:

> `git stash pop`

9. In case when we want apply changes from choosen commit we can use:

> `git stash pop stash@{X}`

10. When we want delete stash commits form storage we can use

> `git stash drop stash@{X}`

or when we want everything what is inside of storage

> `git stash clear`

11. When we want to add new file but that file is untracked by git but we need to add changes in this file to storage then

> `git stash -u`

or

> `git stash -a`

12. If we want create new branch for stash commit we should use

> `git stash branch NAME_OF_NEW_BRANCH stash{0}`

13. Changes made by git stash can be moved to another branch

> `git stash pop`

# Merge conflict

If cinflict appear in out git flow we need to select which part of code we want in our file.
When conflict appera and after taht we select code we need to one again to throught git flow:

1. `git add`

2. `git commit`

3. `git push`

# Git Revert and Git reset

1.  When we want to go back to a selected point in the past on our time line we can do this with:

> `git checkout COMMIT_ID`

2.  In case when we want restore changes form selected commit

> `git revert COMMIT_ID`

3.  History of commits

> `git log --oneline`

4.  To reset old commits we can use

> `git reset COMMIT_ID`

5.  There are two possible reset posibillity

> `git reset COMMIT_ID --soft`

or

> `git reset COMMIT_ID --hard`

# How to change names of commits

1. When we want change commit we can use

> `git commit --amend -m "message update"`

2. To display information about one commit we should use

> `git show COMMIT_ID`

3. In case when we want change more than one commit we can use

> `git rebase -i HEAD~X`
> p = pick
> r = reward

# Fork and Pull Request

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HIXjvh_VCgKVCCZg_EJFMaxNrVP_l-Cz" />
</p>

1. To Fork another repositary from someone GitHub we need go there and choose "fork" then probably we want to clone that repositary to
   our local workspace.

> `git clone PASTE_URL_HERE`

2.  How to go into the project

> `cd PROJECTNAME/`

# Git history

1. To check Git history we should use:

> `git log`

or for example three last commits

> `git log --onelone -3`

or when we want to see selected authon

> `git log --author=AUTHOR_ID`

or we can select specyfic dates parameters:

> `git log --before "rrrr-mm-dd"`

2. Titles of commits

> `git log --oneline`

> `git log --graph`

> `git log --oneline --graph`

> `git log --pretty="%H - %aN - %aD"`

3. Reflog - local history

> `git reflog -NUMBER OD COMMITS`

# Pull request

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HOsDEJZfeoI8qL2W4rtkm9tzkOmr-7Fu" />
</p>

1. New branch

> ` git checkout -b BRANCH_NAME`

to send new branch to remotely repo we can use:

> `git commit -a -m "message"`

Next

> `git push --set-upstream origin BRANCH_NAME`

# Git rebase & git merge

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HU-NUqEDPrYcM33C1gzkCkwCsZPe3DEE" />
</p>

# Git squash

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HZMV3QHsj4j3xj7Iy36ZKW8yIjY_NhOu" />
</p>

> `git rebase -i COMMIT_ID`

and next we need to select -s squash

# Git cherry-pick

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HcP93RCj6LJTqTrghnnn4mbtnI8lU8ev" />
</p>

> `git cherry-pick COMMIT_ID`

# Tagging

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HhV0dsa_QjLCASLjh62dBtcim4g5eToT " />
</p>

1. Example

> `git tag TAG_NAME COMMIT_ID`

2. release all tags

> `git push --tags`

3. Delete tags

3.1. Local

> `git tag -d TAG_NAME`

3.2. Remote

> `git push -d origin TAG_NAME`

testowa zmiana na vsc
