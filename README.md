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
3. Information
4. Configuration
5. Security

- - - - 
## **1. Data Flow **
### 1.1 Forward
### 1.2 BackWard
### 1.3 Branching
### 1.4 Merging
### 1.5 Stashing
### 1.6 Tagging/Releasing

<br/><br/>
### 1.1 Forward 
1.1.1 Initalize a repo in working directory (used when we create repo from scratch)
    
    git init

<br/><br/>
1.1.2 Add a file/fileUpdate from working directory to staging area
Use git add <fileName> as the following three examples

    git add OsOs.txt
    
    git add ProjectDirectory
    
    git add *
    
<br/><br/>
1.1.3 Add all files at staging area to local repo
Use git commit -m <"str"> 

    git commit -m "Adding BroadCast Receiver to Project"
    
<br/><br/>
1.1.4 Add all files at local repo to remote repo;push only
Use git push <remoteRepoName> <localRepoName/tagName>   
    
    git push origin main
    
    git push origin master
    
<br/><br/>
1.1.5 Add all files at local repo to remote repo;pull then push
Use git push -u <remoteRepoName> <localRepoName/tagName>
    
    git push -u origin main
    
    git push -u origin master
    
<br/><br/>
1.1.6 Add project to remote repo with this name 
Use git remote add <remoteRepoName> <https> 
    
    git remote add main https://github.com/mossssama/GitOsOs.git
    
<br/><br/>

### 1.2 BackWard
1.2.1 Return a file/folder from staging area to working directory
Use git reset hard <fileName/folderName>

    git reset hard OsOs.txt
   
<br/><br/>
1.2.2 Deletes all pushed commits above this commit 
Use git reset --hard <hashCodeOfCommitYouWantItToBeLastCommit>

    git reset --hard a4ec3db1ddd361433eea4c2fe70a382ad56b0b71

<br/><br/>
1.2.3 Return a file from staging area to working directory
Use git restore --staged <file/folderName>

    git restore --staged OsOs.txt

<br/><br/>
1.2.4 List the working directory content that will be deleted
Use git clean -n

    git clean -n
    
<br/><br/>    
1.2.5 Delete the working directory content
Use git clean -f

    git clean -f
    
<br/><br/> 
1.2.6 Take copy from remote repo represented by https to our working directory on PC
Use git clone <https>

    git clone https://github.com/mossssama/GitOsOs.git

<br><br/>
1.2.7 Take update from remote repo(specific branch) to our working directory on PC
Use git pull <branchName>

    git pull main

<br><br/>

## 2. Information 
    
# To Be Continued #

    Stay Tuned

