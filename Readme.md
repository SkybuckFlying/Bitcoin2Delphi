# Bitcoin2Delphi  
  
"Git Superproject" for conversion of Bitcoin/C/C++ to Delphicoin/Pascal/Delphi  

This superproject contains two submodules:

1. bitcoin  
2. Delphicoin  

These two submodules can be seen on the code page/tab of Bitcoin2Delphi like so/example:  
  
Delphicoin @ 3a966d7  
bitcoin @ 02cf20b  

The numbers behind the @ are git commits/hashes

Together they are git modules/pointers towards two other repositories at a certain commit hash/point of those repositories.

The bitcoin submodule links to bitcoin (core) repository at https://github.com/bitcoin/bitcoin at a certain commit of that repository.  
The delphicoin submodule links to Delphicoin repository at https://github.com/SkybuckFlying/Delphicoin at a certain commit of that repository.  

The local folders are:  
/bitcoin  
/Delphicoin  

The bitcoin c/c++ source code is to be converted to Pascal/Delphi programming language.  

There are certain rules to follow to do so. Please visit the Delphicoin repository for further details.  

The goal of Delphicoin is to stay compatible with Bitcoin (and use the same blockchain) but perhaps with improvements over time.  
  
# Delphicoin  
  
https://github.com/SkybuckFlying/Delphicoin/  
  
# Bitcoin   
  
https://github.com/bitcoin/bitcoin  
  
## Get started as follows:  
  
Step 1. Start git bash.  
  
Step 2. Clone Bitcoin2Delphi locally to for example C:\SourceCode as follows:  
  
    cd "C:/SourceCode"  
    git clone https://github.com/SkybuckFlying/Bitcoin2Delphi  
  
Step 3. Clone/pull in the submodules:  
  
    cd "C:/SourceCode/Bitcoin2Delphi"  
    git submodule init  
    git submodule update   
  
The head of the bitcoin submodule will be in a detach head state. This is normal since the delphi port will be based on an older commit point.  
To bring back the head in an attached state use git switch master in the bitcoin folder. However this will update the bitcoin master branch head pointer to the latest bitcoin commits which is not something you should do. To undo this go backto bitcoin2delphi folder and run git submodule update again to revert back to the commit as indicated in the super project/contained repository.   
To perform experiments on bitcoin code itself simply created a new branch on the detached head state for example git branch BitcoinExperiment  
  
Step 4. To get head back under control for submodule bitcoin, this should not be done because this updates bitcoin beyond the commit that we are porting from, see above how to fix.  
  
    cd "C:/SourceCode/Bitcoin2Delphi/bitcoin"  
    git switch master  
  
Step 5. To get head back under control for submodule Delphicoin, this switches to latest Delphicoin version, assuming a git fetch was done.  
  
    cd "C:/SourceCode/Bitcoin2Delphi/Delphicoin"  
    git switch main  

Step 6. To get head back to super project pointers go back to super project folder, this will cause heads to go back in detached state possiby:  

    cd "C:/SourceCode/Bitcoin2Delphi"
    git submodule update 
      
Example (using E: drive):  
  
    $ cd "E:/SourceCode"
  
    $ git clone https://github.com/SkybuckFlying/Bitcoin2Delphi
    Cloning into 'Bitcoin2Delphi'...
    remote: Enumerating objects: 21, done.
    remote: Counting objects: 100% (21/21), done.
    remote: Compressing objects: 100% (19/19), done.
    remote: Total 21 (delta 7), reused 10 (delta 2), pack-reused 0
    Receiving objects: 100% (21/21), done.
    Resolving deltas: 100% (7/7), done.
  
    $ cd "E:/SourceCode/Bitcoin2Delphi"
  
    $ git submodule init
    Submodule 'Delphicoin' (https://github.com/SkybuckFlying/Delphicoin) registered for path 'Delphicoin'
    Submodule 'bitcoin' (https://github.com/bitcoin/bitcoin) registered for path 'bitcoin'
  
    $ git submodule update
    Cloning into 'E:/SourceCode/Bitcoin2Delphi/Delphicoin'...
    Cloning into 'E:/SourceCode/Bitcoin2Delphi/bitcoin'...
    Submodule path 'Delphicoin': checked out 'daa78b42797dc18afe03024213059460f2762e84'
    Submodule path 'bitcoin': checked out 'f656165e9c0d09e654efabd56e6581638e35c26c'
    
    $ cd "E:/SourceCode/Bitcoin2Delphi/bitcoin"
   
    $ git switch master
    Previous HEAD position was f656165e9 Merge #18772: rpc: calculate fees in getblock using BlockUndo data
    Switched to branch 'master'
    Your branch is up to date with 'origin/master'.
    
    $ cd "E:/SourceCode/Bitcoin2Delphi/Delphicoin"
    
    $ git switch main
    Previous HEAD position was daa78b4 src/Coins added
    Switched to branch 'main'
    Your branch is up to date with 'origin/main'.
    
    to fix bitcoin so it reverts back to the commit we are porting from, execute submodule update again from bitcoin2delphi folder:
    $ cd "E:/SourceCode/Bitcoin2Delphi"
    $ git submodule update
    Submodule path 'bitcoin': checked out 'f656165e9c0d09e654efabd56e6581638e35c26c'
    
## Recommended workflow:

The recommended workflow after initially getting things working as described above:

1. Update Bitcoin2Delphi master branch

    cd "E:/SourceCode/Bitcoin2Delpi"  
    git pull origin master  

2. Update submodules

    git submodule update
    
3. Change folder to submodule Delphicoin

    cd "E:/SourceCode/Bitcoin2Delphi/Delphicoin"
    
4. Switch to main branch of Delphicoin
    
    git switch main
    
5. Merge changes of remote submodule Delphicoin into local submodule Delphicoin working copy
 
    git pull origin main
 
 
