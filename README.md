# Learning Git
-Text.  
-"#" for a main title.  
-"  " double space to break line.  
-"clone" to bring files to the local machine.  
-"add" to track the changes.  
-"commit" to save files in Git.  
-"push" to upload Git commits.  
-"pull" to download the changes in a local machine.  
-"ls - la" to list every file or folder in the folder.  
-"git status" to show files that have to be commited.  
-"git add ." to track all files in the respective folder.  
-"git add <file name>"  to track an specific file.  
-Is necessary to "add" a file before commit it, because git has track the changes  
-"git commit -m "message" -m "descipition" " to commit the files, and create the message and description about the changes, it only creates the commit and saves in the local machine.  
-ssh-keygen -t rsa -b 4096 -C "email", "-t" stands for the type of encryption, "-b" for the strengh, and after "-C" is necessary to enter the GitHUb email.  
-"keyname.pub", is the public key, can be shared on github, the other key is private.  
-In the respective folder type "cat sshkeyname.pub" to show the key "code".  
-Is also necessary to add a the ssh to the agent, and to the GitHub account.  
-After the SSSHkey is set, run "git push origin main"  
    ~ git init //To turn a normal folder in a repository for GitHub  
    ~ clear //To clear the bash terminal  
    ~ cls //To clear the cmd terminal  
    ~ clr //Also clear the cmd terminal  
    ~ git remote add origin <link> //To give the reference about the repository.
    ~ git remote -v //To show any remote repository that is connected.
-After that and run the "git add" and "git commit" we can finally run "git push orign master".  
## Git Branching  
-Master branch.
-Feature branch are useful to work with a group.
-Hot fix branch are usually used to fix bugs  
    ~ git branch //To see the current branchs
-The "*" indicates the current branch that u are working.
    ~ git checkout //To switch between branchs.
    ~ git checkout -b branchname //To create and switch to the new branch.
-A change made in a feature branch don't appear in the main/master branch.
    ~ git diff <name of the branch> //To check the differences betwenn the current branch and the spcified branch
    ~ git merge <name of the branch> //To merge the branchs
-Before switch the branch is necessary commit the changes.
-When stucked in the terminal just press "q".  
-In a feature branch just after "push" the branch, will get a error message, so copy the given command.  
-PR = Pull request, that means a request to have the code pulled into another branch.  
    ~git pull //To donwload the file with branch  
    