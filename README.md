
# TOC
1. [Usefull link and materials](#Usefull-link-and-materials)

2. [Introduction](#Introduction)

3. [Git interface (Git Bash) commands and work flow](#Git-interface-(Git-Bash)-commands-and-work-flow)

4. [Branches](#Branches)



# Usefull link and materials

[Add Image to GitHub Readme.md from Google Drive](https://stackoverflow.com/questions/52063556/add-image-to-github-readme-md-from-google-drive/70200170#70200170)

[When local branch and remotely branch are differen and you want work on one branch](https://stackoverflow.com/questions/69863948/git-creates-a-new-branch-despite-commit-how-to-fix-this)

[Git Ignore files - templates](https://github.com/github/gitignore)

# Introduction

Introduction to GIT flow using GIT Bash and GitHub. 

This reposytary consist of usefull knowladge about GIT flow. Mainly this reposytary was created based on:

* Course created by Bogdan Stashchuk and available here: [Link](https://subscription.packtpub.com/video/web_development/9781800209855/p1/video1_1/introduction)

Moreover there is complete book which cover most information about GIT [Link](https://git-scm.com/book/en/v2)

Additionally documentation for GIT is avaliable here [Link](https://docs.github.com/en/get-started)

![image](https://drive.google.com/uc?export=view&id=15RSv1aY_71BH8cekrD8fihYPDXeS0OFT)


# Git interface (Git Bash) commands and work flow

1. When we want to check status of our repositary we can use:

> ```git status```


2. Settings for user and user e-mail

>```git config --global.username "YOUR NAME"```

>```git config --global user.email "YOUR EMAIL"```

3. When we want clear our console

>```clear```

4. When we changed somthing on local repositary (e.g. local PC) the GIT flow could look like that:

>```git add FILE NAME```

>```git commit -m "your commnet for changes you've done"```

>```git push```

5. When we add all changes whuch we've done perfect solution for that seems to be:

> ```add *```

6. When we want add changes for two or more fles and we want skip step ```git add```

>```git commit -a -m "your comment and explanation"```

7. History of commits

>```git log```

8. .gitignore

In case of this file we tell git which files will be untracked.

There is posbibility to create this file manually or when repositary is created.

[Commends for .gitignoge](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)

Also on GitHub there is a project which cosnsist of templates for gitignore in case of every language. [Link](https://github.com/github/gitignore)

If we wany to ignore any file inside of folder in gitignore file we can use ```*/```

9. When we want to see particular file in catologe we can use:

```git status -uall```


10. Flow how to add .gitignore file

10.1. Create the text file gitignore.txt.

10.2. Open it in a text editor and add your rules, then save and close.

10.3. Hold SHIFT, right click the folder you're in, then select Open command window here.

10.4. Then rename the file in the command line, with ren gitignore.txt .gitignore.


# Branches
