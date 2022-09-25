10 Git Commands Every Software Developer Should Know

1. Git Clone

      Git clone is a command for downloading existing source code from a remote repository

            git clone <https://name-of-the-repository-link>




2. Git Branch

      Branches are highly important in the git world. By using branches, several developers are able to work in parallel on the same project simultaneously. We can use the git branch command for creating, listing and deleting branches.

      Creating New Branch 

            git branch <branch-name>

      To push the new branch into the remote repository
          
           git push -u <remote> <branch-name>

      Viewing branches

           git branch  or  git branch --list

      Deleting a branch in git 

          git branch -d <branch-name>




3. Git checkout
   
      To work in a branch, first you need to switch to it

      We use git checkout mostly for switching from one branch to another

      We can also use it for checking out files and commits.


      To switch to other branch 

            git checkout <name-of-your-branch>

    
      There are some steps you need to follow for successfully switching between branches:

        :- The changes in your current branch must be committed or stashed before you switch

        :- The branch you want to check out should exist in your local
    
      There is also a shortcut command that allows you to create and switch to a branch at the same time:

           git checkout -b <name-of-your-branch>

           :- This command creates a new branch in your local (-b stands for branch) and 
               checks the branch out to new right after it has been created.




4. Git Status

      The Git status command gives us all the necessary information about the current branch.

            git status


        :- We can gather information like:

            Whether the current branch is up to date

            Whether there is anything to commit, push or pull

            Whether there are files staged, unstaged or untracked

            Whether there are files created, modified or deleted



5. Git Add

    When we create, modify or delete a file, these changes will happen in our local 
    and won't be included in the next commit 

    We need to use the git add command to include the changes of a file(s) into our next commit. 


            To add a single file:       git add <file>

            To add everything at once:   git add -A


      Important: The git add command doesn't change the repository and the changes are not saved until we use git commit.



6. Git commit
    
     Once we reached a certain point in development, we want to save our changes
     
     Git commit is like setting a checkpoint in the development process which you can go back to later if needed.

     We also need to write a short message to explain what we have developed or changed in the source code.

            git commit -m "your commit message"
        
     Important: Git commit saves your changes only locally.




7. Git Push

    After committing your changes, the next thing you want to do is send your changes to the remote server. 
    
    Git push uploads your commits to the remote repository.

            git push     

            git push <remote> <branch-name>

    However, if your branch is newly created, then you also need to upload the branch with the following command:

            git push -u origin <branch_name>

    Important: Git push only uploads changes that are committed.


8. Git Pull

    The git pull command is used to get updates from the remote repo

    This command is a combination of git fetch and git merge 

    Which means, when we use git pull, it gets the updates from remote 
    
    repository (git fetch) and immediately applies the latest changes in your local (git merge).


            git pull 


    This operation may cause conflicts that you need to solve manually.


9. Git revert

    Sometimes we need to undo the changes that we've made. There are various ways to undo our 

    changes locally or remotely (depends on what we need), but we must carefully use these 

    commands to avoid unwanted deletions.

    A safer way that we can undo our commits is by using git revert. 

    To see our commit history, first we need to use 
    
            git log -- oneline:

    Then we just need to specify the hash code next to our commit that we would like to undo:  

           eg:    git revert 232323


10. Git Merge

    When you've completed development in your branch and everything works fine, 
    
    the final step is merging the branch with the parent branch (dev or master).


     when you want to merge your feature branch into the dev branch:

        First you should switch to the dev branch:

            git checkout dev

        Before merging, you should update your local dev branch:

            git fetch

        Finally, you can merge your feature branch into dev:

            git merge <branch-name>


 
