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
Use **git reset hard _fileName/folderName_ **

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

## 2. Information 
    
# To Be Continued #

    Stay Tuned

