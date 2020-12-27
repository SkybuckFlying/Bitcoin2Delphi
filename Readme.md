# Bitcoin2Delphi

## Superproject for conversion of Bitcoin/C/C++ to Pascal/Delphi

This git repository is the super/maintenance repository to guide
the conversion from bitcoin/c/c++ to pascal/delphi programming language !

The original bitcoin is added as a submodule /bitcoin.

The to be converted source code will be stored in /delphicoin.

# Delphicoin

https://github.com/SkybuckFlying/Delphicoin/

# Bitcoin 

https://github.com/bitcoin/bitcoin

## Get started as follows:

1. Start git bash.

2. Clone Bitcoin2Delphi locally to for example C:\SourceCode as follows:

cd "C:/SourceCode"
    
git clone https://github.com/SkybuckFlying/Bitcoin2Delphi

3. Clone/pull in the submodules:

cd "C:/SourceCode/Bitcoin2Delphi"
 
git submodule init

git submodule update 

(Currently the heads of submodules will be in a detach head state)

4. To get head back under control for submodule bitcoin:

cd "C:/SourceCode/Bitcoin2Delphi/bitcoin"
git switch master

5. To get head back under control for submodule Delphicoin:

cd "C:/SourceCode/Bitcoin2Delphi/Delphicoin"
git switch main

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
