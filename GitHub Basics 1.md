# Git, GitHub & VS Code
Here are my jottings from the WTH Technical Writing free Bottcamp session. 

---

## Key Terminologies
* **Directory:** This is your current workspace on your laptop (basically, yourlocal machine). Or your project folder.  

Git has 3 main states that your file can be in: 
1. **Modified**: You made changes to a file but you haven’t committed it to your database yet (you haven't informed your database). So your file is modified

2.  **Staged**: You have saved the modified file so it will go into your next commit snapshot. You've *saved* or done *git add newfile.md*

3. **Committed**: Committed means that the data is safely stored in your local database. You've done *git commit*  

*Repository vs staging area vs directory:*
* **Working Directory**: Where you work on your files locally on your device. 
**Staging Area (Index)**: A temporary holding area where you choose changes to include in the next commit. 
* **Repository**: Where all committed changes and project history are stored, on GitHub.

## Git & VS Code
1. Install git - I had it installed. So I checked git version: ```git --version```
2. Created a directory (on my device) in a folder callled GitHub using ```mkdir “TechBootcamp”  ```
3. TechBootcamp is the name of the new directory I made, the one I want to use to house my repos.  
4. Went to VS Code. I opened the new TechBootcamp folder in my VS Code  
5. I created *index.html* and *style.css* files to mirror what the tutor did.  
6. Then I did ```git init``` to create a hidden *.git folder* that will house my staged files. Notice that html and css files now have a U (called flag U) in front of them meaning Untracked.  
7. Then use git add to add unsaved files to the temporary stage (staging area).  
 * So if I want to add one after the other, I’ll type ```git add index.html```, otherwise use ```git add .``` to add everything to staging area.   
> Notice that the symbol in front of the index file changes to A (meaning it is in the staging area).  
10. Then make git commit, it’ll commit it to your local repository.  

When you edit a document and Ctrl + S, it gets the M flag meaning modified. Then you can commit it.   
Then check status with git status.
> **gitlog**:  Used to show commit history — so write detailed commit messages.

---
### Creating a Remote origin
**Note:** 
* Remote repo is GitHub repo.
* Local repo is repo on VS Code.  

Here's how to create a remote repo: 
1. Create new repo locally
2. Create repo in GitHub without Readme file or gitignore file with same name as local repo
3. Clone GitHub repo with ```git clone  https://github.com/MwithHeart/my-writing-project.git```  
Or ```git remote add origin https://github.com/MwithHeart/my-writing-project.git``` (if no readme file or gitignore file was added) 
4. Then in VS Code, ```git branch -M main```
5. Then check the branch with ```git branch```.
6. Then ```git push -u  origin main.```  
 After this time, you’ll only need to use ```git push```.


> *To initialize a git repository:*
* **Run git init, use git add and git commit.**

## Branching & Merging
Branching allows you to create separate versions of your project so you can work on different tasks or features inependently without affecting the main feature.

* Before resuming work on VS Code, do git pull first to avoid merge conflicts.
> Remote Repo is the one on GitHub

* *.gitignore* is useful when you do not want files to show online. Could be files that are susceptible to attack. 
* *.env* files are those that contain sensitive information like private API keys.  

* Create new files in your VS code and name them ```.gitignore``` and ```.env```
* In the .gitignore file, type *.env*. Immediately you save that, you realize that the env file that was flagged untracked will no longer be flagged.


### Common Branching Strategies/Names
* main- stable production code
* feature/new-button – new features
* bugfix/hot-scroll – fix specific issues
* release/ request payemnt – prepare for production
* hotfix/login – urgent fixes for live systems.

### How to create a branch locally
* Create a new branch with ```git checkout -b "feature/new-menu"``` (You may or may not put the quotation marks). The b flag (-b) is very important.
* Then type ```git branch``` in your terminal and you’ll see that you have two branches.
* Note that you can’t push the new branch to your remote repo on GitHub like that. 
* So go to GitHub and create **new branch** over there, then push from VS Code with ```git push - -set-upstream origin feature/new-menu```
* Create pull request and there you go
* When you’re done with the branch, you can delete the branch.


### How to maerge a branch locally
To merge locally, ensure you are in the branch you want to update (eg main) this means you're in the branch you want to merge another branch with. Then use:  
	```git checkout main```  
    ```git merge feature/new-menu```  

## Deleting
### How to delete a branch
Deleting branch on GitHub is easy.  

But when you delete on GitHub, the branch will still show up on VS Code when you use ```git branch```. So here's how to delete branch locally:
* Switch to another branch or the main branch with ```git checkout main```.
* Then ```git pull```.  

**OR**  
* Use ```git branch -d delete feature/new-menu```  
To delete two branches, just put space in between both branch names

### How to delete a local repo
Use ```rm -rf bootcamp_repo```

## Some Best Practices
* Always pull before working on your local repo. Merge conflicts are not always easy to resolve.
* Always check the branch you’re working on before starting work
* Commit small changes for each pull request. Changes should address something tangible but should be easy to review.
    * Which means you can do ```git add mariam.md``` and commit. Then write the commit message for that. Then do git add for another file, commit it and write its commit message


