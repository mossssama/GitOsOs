GitOsOs <a name="TOP"></a>
===================
# **Git Commands**
1. DataFlow
    - Forward
    - BackWard  
    - Branching
    - Merging
    - Stashing
    - Tagging
2. Information
3. Configuration
4. Security
- - - - 
## 1. Data Flow
### 1.1 Forward 
1.1.1 Initalize a repo in working directory (used when we create repo from scratch)

    git init
- - - - 
1.1.2 Add a file/fileUpdate from working directory to staging area<br/><br/>
Use **git add _fileName_** as the following three examples

    git add OsOs.txt
    git add ProjectDirectory
    git add *
- - - - 
1.1.3 Add all files at staging area to local repo<br/><br/>
Use **git commit -m _stringMessega_** 

    git commit -m "Adding BroadCast Receiver to Project"
- - - - 
1.1.4 Add all files at local repo to remote repo<br/><br/>
Use **git push _remoteRepoName_ _localRepoName/tagName_**    to push only<br><br/>
Use **git push -u _remoteRepoName_ _localRepoName/tagName_** to pull then push
    
    git push origin main
    git push origin master
        
    git push -u origin main
    git push -u origin master
- - - - 
1.1.5 Add project to remote repo with this name<br/><br/> 
Use **git remote add _remoteRepoName_ _https_** 
    
    git remote add main https://github.com/mossssama/GitOsOs.git
    
- - - -
- - - - 
### 1.2 BackWard
1.2.1 Return a file/folder from staging area to working directory<br/><br/>
Use **git reset hard _fileName/folderName_**

    git reset hard OsOs.txt
- - - - 
1.2.2 Deletes all pushed commits above this commit<br/><br/> 
Use **git reset --hard _hashCodeOfCommitYouWantItToBeLastCommit_**

    git reset --hard a4ec3db1ddd361433eea4c2fe70a382ad56b0b71
- - - - 
1.2.3 Return a file from staging area to working directory<br/><br/>
Use **git restore --staged _file/folderName_**

    git restore --staged OsOs.txt
- - - - 
1.2.4 List the working directory content that will be deleted<br/><br/>
Use **git clean -n**

    git clean -n
- - - -     
1.2.5 Delete the working directory content<br/><br/>
Use **git clean -f**

    git clean -f
- - - - 
1.2.6 Take copy from remote repo represented by https to our working directory on PC<br/><br/>
Use **git clone _https_**

    git clone https://github.com/mossssama/GitOsOs.git
- - - - 
1.2.7 Take update from remote repo(specific branch) to our working directory on PC<br/><br/>
Use **git pull _branchName_**

    git pull main
- - - - 
- - - -

### 1.3 Branching (local branches)
1.3.1 Create branch<br/><br/>		
Use **git branch _branchName_	**

    git branch blindFeature	
- - - - 
1.3.2 Rename current branch<br/><br/> 
Use **git branch -m _newName_**

    git branch -m blindMode
- - - - 
1.3.3 Delete branch<br/><br/>
Use **git branch -d _branchName_**

    git branch -d blindMode
- - - - 
1.3.4 Switch to specific branch<br/><br/>
Use **git checkout _branchName_**

    git checkout de7kMode
- - - -     
1.3.5 Create branch & switch to it<br/><br/>
Use **git checkout -b _branchName_**

    git checkout -b ososEngineer
- - - - 
- - - - 

### 1.4 Merging
1.4.1 Merge currentBranch with this specificBranch<br/><br/>
Use **git merge _branchName_**

    git merge blindMode
- - - - 
- - - - 

### 1.5 Stashing(in a directory)
1.5.1 Saves working directory contents in stash<br/><br/>		
Use **git stash**

   git stash
- - - - 
1.5.2 Saves working directory contents+message in stash<br/><br/> 
Use **git stash save _writtedMessage_**

    git stash save tempStash
- - - - 
1.5.3 Returns last stash<br/><br/>
Use **git stash pop**

    git stash pop	
- - - - 
1.5.4 Returns specific stash<br/><br/>
Use **git stash pop stash@{_number_}**

    git stash pop stash@{3}
- - - -     
1.5.5 Deletes last stash<br/><br/>
Use **git stash drop**

    git stash drop
- - - - 
1.5.6 Deletes specific stash<br/><br/>
Use **git stash drop stash@{_number_}**

    git stash drop stash@{3}
- - - -   
1.5.7 Shows last stash contents<br/><br/>
Use **git stash show**

    git stash show
- - - - 
1.5.8 Shows specific stash contents<br/><br/>
Use **git stash show stash@{_number_}**

    git stash show stash@{3}
- - - -     
1.5.9 Returns copy of last stash<br/><br/>
Use **git stash apply**

    git stash apply
- - - - 
1.5.10 Gives all stashes<br/><br/>
Use **git stash list**

    git stash list
- - - -   
1.5.11 delete all stashes<br/><br/>
Use **git stash clear**

    git stash clear
- - - -     
- - - -

### 1.6 Tagging/Realesing
1.6.1 Gives all created tags in local repo<br/><br/>		
Use **git tag**

   git tag
- - - - 
1.6.2 Create tag with this name<br/><br/> 
Use **git tag _version_**

    git tag v1.0
- - - - 
1.6.3 Create tag with this name & with commit inside it<br/><br/>
Use **git tag -a _version_ -m _tagCommit_**

    git tag -a __v1.0__ -m __StartingVersion__
- - - - 
1.6.4 List all tags starting from entered version<br/><br/>
Use **git tag -l _version_.***

    git tag -l __2.*__
- - - -     
1.6.5 Delete remote tag with this name<br/><br/>
Use **git tag -d _version_**

    git tag -d __1.0__
- - - - 
- - - -   
- - - - 

## 2. Information 
2.1 Gives information about unstaged/unadded files & uncommited files<br/><br/>
Use **git status**

    git status
- - - - 
2.2 Gives all the available branches in local repo<br/><br/> 
Use **git branch**

    git branch
- - - - 
2.3 Gives all the available branches in remote repo<br/><br/>
Use **git remote -v**

    git remote -v
- - - - 
2.4 Gives all the previous commits with the HEAD; HEAD is pointer to last commit;(use q to get out of log)<br/><br/>
Use **git log**

    git log
- - - -
- - - -
- - - -
    
## 3. Configuration   
3.1 Gives all the available configurations/gitProperties<br/><br/>
Use **git config -l**

    git config -l
- - - - 
3.2 Gives the configurations locations on our PC<br/><br/>
Use **git config -l --show origin**

    git config -l --show origin
- - - - 
3.3 Gives the value assigned to this property<br/><br/>
Use **git config --global _gitProperty_** 

    git config --global user.name
- - - - 
3.4 Assigns a value to this property<br/><br/>
Use **git config --global _gitProperty_ _value_** to push only<br><br/>
    
    git config --global user.name OsOs
- - - - 
3.5 Allows editing properties using textEditor not cmd<br/><br/> 
Use **git config --global --edit** 
    
    git config --global --edit	
- - - -
3.6 Gives speed dial to specific command<br/><br/>
Use **git config --global alias._speedDial_ _commandToBeReplaced_** 
    
    git config --global alias.cm "commit -m"
    git config --global alias.st status
- - - -
- - - -
- - - -

## 4. Information 
4.1 Asks to enter key passphrase to verify yourself to be able to push to gitHub without signing in<br/><br/>
Use **ssh -T git@github.com**

    ssh -T git@github.com
- - - - 
4.2 Asks to generate a key to allow pushing updates to gitHub from another device(without need to sign in to gitHub<br/><br/> 
Use **ssh-keygen -t rsa -b 4096 -C _emailAddress_**

    ssh-keygen -t rsa -b 4096 -C messi@gmail.com
- - - -
- - - -
- - - -
- - - -

Don't forget while dealing with git Commands in cmd
- origin is default remote repo branch
- master is default local repo branch
