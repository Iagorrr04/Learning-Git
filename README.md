# Learning Git

## MD formatation.
- "#" for a main title.  
- " " double space to break line.  
- Add a line and a space above some text to create a "window".
- "- text" to create a little point.
- "---" to create a horizontal rule.
- Use the extensial "Markdown preview" in VS Code.
- "```" to create a code formatation.

---

## Basic Git commands
- "clone" to bring files to the local machine.  
- "add" to track the changes.  
- "commit" to save files in Git.  
- "push" to upload Git commits.  
- "pull" to download the changes in a local machine. -
```
    $ ls - la //To list EVERY file or folder in the folder.  
    $ git status //To show files that have to be commited or add.  
    $ git add  //To track all files in the respective folder.  
    $ git add <file name>  //To track an specific file.  
```
- Is necessary to "add" a file before commit it, because git needs to track the changes.
```
    $git commit -m "message" -m "descipition"  //To commit the files, and create the message and description about the changes, it only creates the commit and saves in the local machine.  
    $ clear //To clear the bash terminal.  
    $ cls //To clear the cmd terminal.  
    $ clr //Also clear the cmd terminal.
```
- [git -commit domumentation](https://git-scm.com/docs/git-commit)
  
---

## SSH keys
- ssh-keygen -t rsa -b 4096 -C "email", "-t" stands for the type of encryption, "-b" for the strengh, and after "-C" is necessary to enter the GitHUb email.  
- "keyname.pub", is the public key, can be shared on github, the other key is private.  
- In the respective folder type "cat sshkeyname.pub" to show the key "code".  
- Is also necessary to add a the ssh to the agent, and to the GitHub account.  
- After the SSSHkey is set, run "git push origin main".  

---

## Creating a repository locally.
```
    $ git init //To turn a normal folder in a repository for GitHub.  
    $ git remote add origin <link> //To give the reference about the repository.
    $ git remote -v //To show any remote repository that is connected.
```
- After that and run the "git add" and "git commit", then we can finally run "git push orign master".

---

## Git Branching  
- Master branch, is the main branch that contains the main version of the code.
- Feature branch, are useful to work with a group.  
- Hot fix branch, just like a feature branch but with a single commit.  
``` 
    $ git branch //To see the current branchs.
    $ git branch -M "main" //To change the master branch name to main.
```  
- The "*" indicates the current branch that you are working.  
``` 
    $ git checkout <branch name>//To switch between branchs.  
    $ git checkout -b <new branch name> //To create and switch to the new branch.
```
- A change made in a feature branch don't appear in the main/master branch, is just like copy a folder and.  
```
    $ git diff <name of the branch> //To check the differences betwenn the current branch and the spcified branch.  
    $ git merge <name of the branch> //To merge the branchs.
```
- Before switch the branch is necessary commit the changes, or the current branch changes will be overwritten by the next branch.    
- When stucked in the terminal just press "q".  
- In a feature branch just after "push" the branch, will get an "error" message, so copy the given command.  
- PR = Pull request, that means a request to have the code pulled into another branch.
```
    $ git pull //To donwload the file with branch.
```
- After merge a branch is likey that we don't use it so again, so delete it.
```
    $ git branch -D <name of the branch> //To delete a branch local.
    4 git push origin --delete <name of the branch> //To delete a brach remote.
    $ git commit -am "message" //To add the changes of a modified files, doesn't work for new files.
```

---

## Git merge conflict
- Happens when we try to merge two branchs that have changes in the same line...  r
- If we try to merge two files in conflit the VS code will show us the conflict it self, then just fix it and then commit.  

--- 

## Undoing git
- Used to when you commit or add something acidentally, or get back the decision.  
```
    $ git reset //To show the list of files that has been added but not commited.  
    $ git reset HEAD~1 //HEAD points to the last commit HEAD~1 points to the penultimate commit, this command line unstage and uncommit the changes.  
    $ git log //To show all commit that have been made.  
    $ git reset <hash of the commit> //To return to a specific commit.  
```

---

## Fork
- Used to make a copy of some repository, so we can have full acess and make it as our own.
- Then we can make or own commits, and make a pull request the "original" repository.

## Authorize another machine.
- To avoid enter the name and password all the time is easier to set a SSH key in the new machine.
- Run the following commands in the terminal to generate a new SSH key.

    $ ssh-keygen -t ed25519-sk -C "your_email@example.com"

- The following message will appears, so just press enter to save with the default name.
    
    Generating public/private ed25519 key pair.
    Enter file in which to save the key (/home/user_name/.ssh/id_ed25519): [enter]

- To avoid enter the passpharse every time just press enter to the following two lines.

    Enter passphrase (empty for no passphrase): [enter]
    Enter same passphrase again: [enter]

- A SSH key is now generated and stored in your machine, now just need to add the new ssh to your account, to run view the SSH key code run the following command.

        cat ~/.ssh/id_ed25519.pub

- The nex time you try to push some commit git you look for the SSH and authorize your machine.
