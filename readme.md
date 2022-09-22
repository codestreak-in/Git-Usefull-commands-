10 Git Commands Every Developer Should Know

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


 