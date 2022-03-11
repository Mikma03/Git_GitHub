# Control version - Git

<p>&nbsp;</p>

# Table of content

<p>&nbsp;</p>

1. [Usefull link and materials](#Usefull-link-and-materials)

2. [Introduction](#Introduction)

3. [Git interface (Git Bash/Git GIU) commands and work flow](<#Git-interface-(Git-Bash-/-Git-GUI)-commands-and-work-flow>)

4. [Branches](#Branches)

5. [Git-Stash](#Git-Stash)

6. [Merge conflict](#Merge-conflict)

7. [Git Revert and Git reset](#Git-Revert-and-Git-reset)

8. [How to change names of commits](#How-to-change-names-of-commits)

9. [Fork and Pull Request](#Fork-and-Pull-Request)

10. [Git history](#Git-history)

11. [Pull request](#Pull-request)

12. [Git rebase & git merge](#Git-rebase-&-git-merge)

13. [Git squash](#Git-squash)

14. [Git cherry-pick](#Git-cherry-pick)

15. [Tagging](#Tagging)

16. [Git with VSC](#Git-with-VSC)


<p>&nbsp;</p>

# Usefull link and materials

- Add Image to GitHub Readme.md from Google Drive
  - https://stackoverflow.com/questions/52063556/add-image-to-github-readme-md-from-google-drive/70200170#70200170


  - Example how to connect to image from Google Drive:

    ```
    <p align="center">
    <img src="https://drive.google.com/uc?export=view&id=15RSv1aY_71BH8cekrD8fihYPDXeS0OFT" />
    </p>
    ```

<p>&nbsp;</p>

- When local branch and remote branch are differen and you want work on one branch
  - https://stackoverflow.com/questions/69863948/git-creates-a-new-branch-despite-commit-how-to-fix-this

<p>&nbsp;</p>

- Git Ignore (.gitignore) files - templates
  - https://github.com/github/gitignore

<p>&nbsp;</p>

# Introduction

<p>&nbsp;</p>

This repository consist of usefull materials and shows workflow in version control using Git. Some materials also show how to use GitHub.

<p>&nbsp;</p>

## GIT flow using GIT Bash and GitHub.

<p>&nbsp;</p>

**Mainly this reposytary was created based on:**

<p>&nbsp;</p>

- Book which cover most information about GIT
  - https://git-scm.com/book/en/v2

<p>&nbsp;</p>

- Documentation for GIT
  - https://docs.github.com/en/get-started

<p>&nbsp;</p>

- Git course (for native Polish speaker or those who like subtitles)
  - https://www.youtube.com/watch?v=tvHVafvw16Y&list=PLj-pbEqbjo6AKsJ8oE2pvIqsb15mxdrxs&ab_channel=Zaprogramuj%C5%BBycie


# Git interface (Git Bash / Git GUI) commands and work flow

<p>&nbsp;</p>

1. When we want to check status of files in our repositary we can use:

<p>&nbsp;</p>

The GIT interface must be enabled in the place where we have the repository on our local computer.


> `git status`

<p>&nbsp;</p>

2. Settings for new user and add user e-mail:

<p>&nbsp;</p>

> `git config --global user.name "Your Name"`

> `git config --global user.email "YOUR EMAIL"`

<p>&nbsp;</p>

3. When we want clear our console

<p>&nbsp;</p>

> `clear`

<p>&nbsp;</p>

4. When we changed somthing on our local repositary the GIT flow could look like that:

<p>&nbsp;</p>

> `git add FILE_NAME`

> `git commit -m "your commnet for changes you've done"`

> `git push`

<p>&nbsp;</p>

5. When we add all changes which we've done perfect solution for that seems to be:

<p>&nbsp;</p>

- Git Add - documentation
  - https://github.com/git-guides/git-add

The `git add` command adds new or changed files in your working directory to the Git staging area.

`git add` is an important command - without it, no `git commit` would ever do anything. Sometimes, `git add` can have a reputation for being an unnecessary step in development. But in reality, `git add` is an important and powerful tool. `git add` allows you to shape history without changing how you work.


> `git add *`

<p>&nbsp;</p>

6. When we want add changes for two or more fles and we want skip step `git add`

<p>&nbsp;</p>

> `git commit -a -m "your comment and explanation"`

<p>&nbsp;</p>

7. History of commits. Shows the commit logs.

<p>&nbsp;</p>

- Description
  - https://git-scm.com/docs/git-log


List commits that are reachable by following the `parent` links from the given commit(s), but exclude commits that are reachable from the one(s) given with a ^ in front of them. The output is given in reverse chronological order by default.

You can think of this as a set operation. Commits reachable from any of the commits given on the command line form a set, and then commits reachable from any of the ones given with ^ in front are subtracted from that set. The remaining commits are what comes out in the command’s output. Various other options and paths parameters can be used to further limit the result.


> `git log`

<p>&nbsp;</p>

8. .gitignore

In case of this file we tell git which files will be untracked.

There is posbibility to create this file manually or when repositary is created.

<p>&nbsp;</p>

- Commends for .gitignoge
  - https://www.atlassian.com/git/tutorials/saving-changes/gitignore)

<p>&nbsp;</p>

Also on GitHub there is a project which cosnsist of templates for gitignore in case of every language. 
<p>&nbsp;</p>

- Link
  - https://github.com/github/gitignore)

<p>&nbsp;</p>

If we wany to ignore any file inside of folder in gitignore file we can use `*/`

9. When we want to see particular file in catologe we can use:

<p>&nbsp;</p>

> `git status -uall`

<p>&nbsp;</p>

10. Flow how to add .gitignore file

<p>&nbsp;</p>

    10.1. Create the text file `gitignore.txt`.

    10.2. Open it in a text editor and add your rules, then save and close.

    10.3. Hold SHIFT, right click the folder you're in, then select Open `command` window here.

    10.4. Then rename the file in the command line, with ren `gitignore.txt` `.gitignore`.

<p>&nbsp;</p>

# Branches

<p>&nbsp;</p>

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1H8TGpxkK1N1v9yD9_VSNCi0-1iiyW2pr" />
</p>

<p>&nbsp;</p>

1. How can we check where we are in case of branch:

<p>&nbsp;</p>

> `git branch`

<p>&nbsp;</p>

2. When we want to create new branch we can use:

<p>&nbsp;</p>

> `git branch NAME_OF_NEW_BRANCH`

<p>&nbsp;</p>

3. When we want change branch means that we want change branch where we will be working atlassian

<p>&nbsp;</p>

`git checkout NAME_OF_BRANCH`

<p>&nbsp;</p>

4. When we want to make changes on our remotely repository and add new branch which is already exist on our local workspace we can use commend:

<p>&nbsp;</p>

> `git push -u origin NAME_OF_NEW_BRANCH`

<p>&nbsp;</p>

5. When we want to create new brach and autamatillcy checkout branch we can use:

<p>&nbsp;</p>

> `git checkout -b NAME_OF_NEW_BRANCH`

<p>&nbsp;</p>

6. When we want to see graph of our changes in console:

<p>&nbsp;</p>

> `git log -oneline -graph -all`

<p>&nbsp;</p>

7. When we wantto open GIU for Git to see our previous changes

<p>&nbsp;</p>

> `gitk -all`

<p>&nbsp;</p>

8. When we want merge commits from our branches we can use:

<p>&nbsp;</p>

> `git merge <name of branch which will be merge to actuall branch>`

<p>&nbsp;</p>

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HE29F10Rqktdg8GPQniRB4134YxZ8Kvo" />
</p>

<p>&nbsp;</p>

# Git Stash

<p>&nbsp;</p>

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HEmqiOj50tK2vWmeZWyzBGGMRUWQJgPq" />
</p>

<p>&nbsp;</p>

1. When we want add something to storage we can use command:

<p>&nbsp;</p>

> `git stash`

<p>&nbsp;</p>

2. If we want check what is in our storage we should use:

<p>&nbsp;</p>

> ` git stash list`

<p>&nbsp;</p>

3. Changes in our storage are indexed and we can acess to then by

<p>&nbsp;</p>

> `stash@{X}`

<p>&nbsp;</p>

4. We can add multipletimes changes and updates and everytime our list will be reindexed moreover the latest index is our last change and this is index{0}.
   If we want identify difference between stash commit we can use:

<p>&nbsp;</p>

> `git stash show stash@{X}`

    where ```{X}``` is number of stash commit

<p>&nbsp;</p>

5. When our changes in storage are simillar or commend `git stash show` doesn't show the changes we are interested in then we can use:

<p>&nbsp;</p>

> `git stash show stash@{X} -p`

<p>&nbsp;</p>

6. In case when we change two or more files we can use

<p>&nbsp;</p>

> `git stash save "Descriotion for our changes"`

<p>&nbsp;</p>

7. When we want apply changes from storage to our file we can use below command, but in this case only the latest commit will be applied. Also in this case
   changes are still in storage.

<p>&nbsp;</p>

> `git stash apply`

<p>&nbsp;</p>

8. When we want delete changes from storage after adding those to file we can use:

<p>&nbsp;</p>

> `git stash pop`

<p>&nbsp;</p>

9. In case when we want apply changes from choosen commit we can use:

<p>&nbsp;</p>

> `git stash pop stash@{X}`

<p>&nbsp;</p>

10. When we want delete stash commits form storage we can use

<p>&nbsp;</p>

> `git stash drop stash@{X}`

<p>&nbsp;</p>

or when we want everything what is inside of storage

<p>&nbsp;</p>

> `git stash clear`

<p>&nbsp;</p>

11. When we want to add new file but that file is untracked by git but we need to add changes in this file to storage then

<p>&nbsp;</p>

> `git stash -u`

<p>&nbsp;</p>

or

<p>&nbsp;</p>

> `git stash -a`

<p>&nbsp;</p>

12. If we want create new branch for stash commit we should use

<p>&nbsp;</p>

> `git stash branch NAME_OF_NEW_BRANCH stash{0}`

<p>&nbsp;</p>

13. Changes made by git stash can be moved to another branch

<p>&nbsp;</p>

> `git stash pop`

<p>&nbsp;</p>

# Merge conflict

<p>&nbsp;</p>

If cinflict appear in out git flow we need to select which part of code we want in our file.
When conflict appera and after taht we select code we need to one again to throught git flow:

<p>&nbsp;</p>

1. `git add`

<p>&nbsp;</p>

2. `git commit`

<p>&nbsp;</p>

3. `git push`

<p>&nbsp;</p>

# Git Revert and Git reset

<p>&nbsp;</p>

1.  When we want to go back to a selected point in the past on our time line we can do this with:

<p>&nbsp;</p>

> `git checkout COMMIT_ID`

<p>&nbsp;</p>

2.  In case when we want restore changes form selected commit

<p>&nbsp;</p>

> `git revert COMMIT_ID`

<p>&nbsp;</p>

3.  History of commits

<p>&nbsp;</p>

> `git log --oneline`

<p>&nbsp;</p>

4.  To reset old commits we can use

<p>&nbsp;</p>

> `git reset COMMIT_ID`

<p>&nbsp;</p>

5.  There are two possible reset posibillity

<p>&nbsp;</p>

> `git reset COMMIT_ID --soft`

<p>&nbsp;</p>

or

<p>&nbsp;</p>

> `git reset COMMIT_ID --hard`


<p>&nbsp;</p>

# How to change names of commits

<p>&nbsp;</p>

1. When we want change commit we can use

<p>&nbsp;</p>

> `git commit --amend -m "message update"`

<p>&nbsp;</p>

2. To display information about one commit we should use

<p>&nbsp;</p>

> `git show COMMIT_ID`

<p>&nbsp;</p>

3. In case when we want change more than one commit we can use

<p>&nbsp;</p>

> `git rebase -i HEAD~X`
> p = pick
> r = reward


<p>&nbsp;</p>

# Fork and Pull Request

<p>&nbsp;</p>

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HIXjvh_VCgKVCCZg_EJFMaxNrVP_l-Cz" />
</p>

<p>&nbsp;</p>

1. To Fork another repositary from someone GitHub we need go there and choose "fork" then probably we want to clone that repositary to
   our local workspace.

<p>&nbsp;</p>

> `git clone PASTE_URL_HERE`

<p>&nbsp;</p>

2.  How to go into the project

<p>&nbsp;</p>

> `cd PROJECTNAME/`

<p>&nbsp;</p>

# Git history

<p>&nbsp;</p>

1. To check Git history we should use:

<p>&nbsp;</p>

> `git log`

<p>&nbsp;</p>

or for example three last commits

<p>&nbsp;</p>

> `git log --onelone -3`

<p>&nbsp;</p>

or when we want to see selected authon

<p>&nbsp;</p>

> `git log --author=AUTHOR_ID`

<p>&nbsp;</p>

or we can select specyfic dates parameters:

<p>&nbsp;</p>

> `git log --before "rrrr-mm-dd"`

<p>&nbsp;</p>

2. Titles of commits

<p>&nbsp;</p>

> `git log --oneline`

<p>&nbsp;</p>

> `git log --graph`

<p>&nbsp;</p>

> `git log --oneline --graph`

<p>&nbsp;</p>

> `git log --pretty="%H - %aN - %aD"`

<p>&nbsp;</p>

3. Reflog - local history

<p>&nbsp;</p>

> `git reflog -NUMBER OD COMMITS`


<p>&nbsp;</p>

# Pull request

<p>&nbsp;</p>

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HOsDEJZfeoI8qL2W4rtkm9tzkOmr-7Fu" />
</p>

<p>&nbsp;</p>

1. New branch

<p>&nbsp;</p>

> ` git checkout -b BRANCH_NAME`


<p>&nbsp;</p>

to send new branch to remotely repo we can use:

<p>&nbsp;</p>

> `git commit -a -m "message"`

<p>&nbsp;</p>

Next

<p>&nbsp;</p>

> `git push --set-upstream origin BRANCH_NAME`

<p>&nbsp;</p>

# Git rebase & git merge

<p>&nbsp;</p>

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HU-NUqEDPrYcM33C1gzkCkwCsZPe3DEE" />
</p>

<p>&nbsp;</p>

# Git squash

<p>&nbsp;</p>

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HZMV3QHsj4j3xj7Iy36ZKW8yIjY_NhOu" />
</p>

<p>&nbsp;</p>

> `git rebase -i COMMIT_ID`

<p>&nbsp;</p>

and next we need to select -s squash

<p>&nbsp;</p>

# Git cherry-pick

<p>&nbsp;</p>

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HcP93RCj6LJTqTrghnnn4mbtnI8lU8ev" />
</p>

<p>&nbsp;</p>

> `git cherry-pick COMMIT_ID`

<p>&nbsp;</p>

# Tagging

<p>&nbsp;</p>

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HhV0dsa_QjLCASLjh62dBtcim4g5eToT " />
</p>

<p>&nbsp;</p>

1. Example

<p>&nbsp;</p>

> `git tag TAG_NAME COMMIT_ID`

<p>&nbsp;</p>

2. release all tags

<p>&nbsp;</p>

> `git push --tags`


<p>&nbsp;</p>

3. Delete tags

<p>&nbsp;</p>

3.1. Local


<p>&nbsp;</p>

> `git tag -d TAG_NAME`

<p>&nbsp;</p>

3.2. Remote

<p>&nbsp;</p>

> `git push -d origin TAG_NAME`


<p>&nbsp;</p>

# Git with VSC

<p>&nbsp;</p>

Best methon as always is learning by doing. I've found couple of tutorial on YT which very good describe what going on when we are using git working with VSC.

This is a list of tutorial:

<p>&nbsp;</p>

- Intro to VSC and GIT
  - https://www.youtube.com/watch?v=Fk12ELJ9Bww&t=8s&ab_channel=AutomationStepbyStep

<p>&nbsp;</p>

- Branches in VSC
  - https://www.youtube.com/watch?v=F2DBSH2VoHQ&ab_channel=Ihatetomatoes

<p>&nbsp;</p>

- TOP 6 Git extensions
  - https://www.youtube.com/watch?v=Guva-oab1pg&ab_channel=BryanJenks

<p>&nbsp;</p>

- Branches, merge, clone, fork
  - https://www.youtube.com/watch?v=3Tn58KQvWtU&list=PLpPVLI0A0OkLBWbcctmGxxF6VHWSQw1hi&ab_channel=DevWorld
