Collection of commands
======================

This is a collection of commands I
try to remember.



Misc commands
-------------

    # show package info
    apt-cache showpkg ssh
  
    gitk --all &
    
    # Find in cmd history
    CTRL+R


Fix network

    sudo modprobe -r e1000
    sudo modprobe e1000
    sudo /etc/init.d/networking restart

Files
    
    md5sum filename
    base64 filename
    base64 -d filename

    sed s/find/replace/ filename
    # sort lines of text files
    sort

    # diff between files
    diff a b

    # to empty a file
    cat /dev/null >filename

    # add to file and append to file
    echo "hello" >filename
    echo "hello" >>filename 

    # Output is updated on the fly
    tail -f filename


Remotes - ssh
-------------

Create keys and copy public key to host

    ssh-keygen -t rsa
    ssh-copy-id username@host

Show fingerprint of host key

    ssh-keygen -lf /etc/ssh/ssh_host_rsa_key.pub 

Connect to host or run cmd on host

    ssh username@host
    ssh username@host pwd;ls

Copy file from host to local

    scp username@host:file ~/files/file.txt

Aliases
-------

Save aliases in ~/.bashrc or ~/.bash_aliases?

    alias ll='ls -alF'
    alias la='ls -A'
    alias l='ls -CF'

    alias s='git status'
    alias d='git diff'
    alias c='clear'

Git
---

Saves project based config in .git/config
and global config in ~/.gitconfig

    git config alias.st status 
    git config --global alias.st status

    git config --global user.name "Your Name"
    git config --global user.email your@name.com

    git init
    git remote add origin git@host:project/name.git

Using 

    git checkout -b
    git merge --no-ff branch_name
    git pull --rebase
    git status -u
    git diff --word-diff
    git diff --word-diff=color
    git log --oneline --decorate
    git checkout -t origin/feature

    git commit -v
    git commit -m 'commit message'

Stashing
 
    git stash
    git stash save 'Description'
    git stash apply
    git stash pop
  
