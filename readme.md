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


 