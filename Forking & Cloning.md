# Forking & Cloning
## Clone a repository
You often clone a repo when you have access to the repo. 
To clone a repo:
* On the home page of the repo in GitHub, theres a green icon named "Code"
* Click the drop down arrow beside it and copy the link to the repo.
* Then go to your command line on your device and paste the link to the repo which you copied from GitHub.
* Then change directory into it by typing ```cd new repo```

## Fork a repository
Here you'll learn how to fork a repository:

* The tutor searched **Public-apis** on GitHub
* He forked it on GitHub (just the main branch), then cloned to local repo.
* Then branched (very important) with ```git checkout -b “feature/newapi”```
* Set original repo that was forked as remote. Very important since you're not the only one working on it. Do this with ```git remote add upstream “repo url copied from Google url bar”```
* Then do ```git remote```, you'll see origin and upstream
* To check for changes, do ```git fetch upstream``` (like a git pull so you can be up to date with the original repo)
* Then do ```git merge upstream/main``` (remember some repos may use master instead of main so it'd be upstream/master).
* Then push. But remember you'd need to **create a new branch in GitHub for your new local branch**. You can do that locally with ```git push  - - set -upstream origin feature/newapi```


## Some git commands
* Git innit
* Git log: Used to check the history of the GitHub, the changes and who made changes. 
A personal note: After using git log, it felt liek I couldn't type another command. If such happens, type **Q**
* ls: For listing the folders in a directory
* git status
* git restore: Used if you want to keep your work but undo a previous commit

