#Usefull Git commands

@author: Nicholas Waytowich


## Feature Branch Workflow
When working on a new feature, it's usefull to create a new branch for the feature,
make commits as usual and push the new branch up to the remote repository. 
When finished with changes, you can merge feature branch into master branch. Ideally,
before this is done, on the GUI, you open a pull request so that others can see/help/review
the changes. Then, after merging, pull request will be closed, and you can delete the 
local and remote feature branches


### check your current remote repositories
    git remote -v
    
## Add remote repositories
    git remote add <quick-reference-name> <remote-url>
    (ie git remote add origin https://github.com/uname/myrepo.git)

## Switch the tracking of local/branch and remote/branch
    git branch <branch> -u <remote>/<branch>

# After tracking is set, 
    git push
    git pull

# List current branches
    git branch

# Create new branch:
    git branch <branch>
    
# Switch to a branch (make it ur current working branch):
    git checkout <branch>

# Create new branch and switch to it:
    git checkout -b <branch>
    
# Standard working commands
    git status
    git add <file>
    git commit -m "commit message"
    
# Push branch to remote (for the first time):
    git push -u <remote> <branch>  (ie. git push -u remote newbranch)
    
# All subsequent pushes to remote branch:
    git push
    
# To merge a branch (ie, merge feature branch back into master):
    git checkout master
    git pull
    git pull <remote> <branch>
    git push

# Alternative way to merge a branch
    git checkout <branch1>  #make some branch ur current working branch
    git merge <branch2>     #merge <branch2> into whatever ur current working branch is (branch1 in this case)
    git push                #I assume we need to push to remote after merging local?
    
# Delete local branch
    git -d <branch>  (safe delete - only deleted after merge)
    git -D <branch>  (hard delete)
    
# Delete remote branch
    git -push <remote> --delete <branch>



