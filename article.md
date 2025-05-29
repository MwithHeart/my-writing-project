# Here are some of my jottings from the sessions from week 3 so far
> I haven't proofread it so please permit typo errors when you find them.
---

## What We Did in Week 3 
### Git & VS Code
1. Installed git - I had it installed. SO I checked git version: git - -version  
2. Created a directory in my GitHub Folder (under document) with mkdir **“TechBootcamp”**  
3. TechBootcamp is the name of the new directory I made, the one I want to use to house my repos.  
4. Back to VS Code. I opened the new TechBootcamp folder in my VS Code  
5. I created *index.html* and *style.css* styles to mirror what the tutor did.  
6. Then I did git init to create a hidden .git folder that will house my staged files. Notice that html and css files have a U (called U flag) in front of them meaning Untracked  
7. Then use git add to add unsaved files to the temporary stage (staging area).  
8. So if I want to add one after the other, I’ll type *git add index.html*, otherwise use *git add .* to add everything to staging area.   
> Notice that the symbol in front of the index file changes to A (meaning it is in the staging area).  
10. Then make git commit, it’ll commit it to your local repository.  

When you edit a document and Ctrl + S, it gets the M flag meaning modified. Then you can commit it.   
Then check status with git status.
> **gitlog**:  Used to show commit history — so write detailed commit messages.

---
### Created a Remote origin (remote repo- GitHub)
1. Create new repo locally
2. Create repo in GitHub without Readme file or gitignore file with same name as local repo
3. Cloned GitHub repo with git clone  https://github.com/MwithHeart/my-writing-project.git
Or git remote add origin (if no readme file or gitignore file was added) https://github.com/MwithHeart/my-writing-project.git
4. Then in VS Code, git branch -M main
5. Then checked branch in VS Code with git branch.
6. Then git push -u (pronounced flag U) origin main. But after this time, you’ll only need to use git push.

> To initialize a git repository, 
* Run git in it, use git add and git commit
* Your GitHub repo is your remote repo
* Your repo on VS Code is your local repo 

## Branching & Merging
* Before resuming work on VS Code, do git pull first to avoid merge conflicts.
> Remote Repo is the one on GitHub

* *.gitignore* is useful when you do not want files to show online. Could be files that are susceptible to attack. 
* *.env* files are those that contain sensitive information like private API keys.  

* Create new files in your VS code and name them .gitignore and .env
* In the .gitignore file, type .env. Immediately you save that, you realize that the env file that was flagged untracked will no longer be flagged.

### To Create Branch
Branching allows you to create separate versions of your project so you can work on different tasks or features inependently without affecting the main feature.

#### Common Branching Strategies
* main- stable production code
* feature/new-button – new features
* bugfix/hot-scroll – fix specific issues
* release/ request payemnt – prepare for production
* hotfix/login – urgent fixes for live systems.