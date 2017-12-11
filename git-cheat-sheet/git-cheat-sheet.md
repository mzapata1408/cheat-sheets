# Git Cheat Sheet

## Commit procedure

First add changes to stage area, then commit, then push

```bash
git add .
git commit -m "My message"
git push
```

## Reset procedure

First add changes to stage area, then commit, then push

```bash
git add .
git commit -m "My message"
git push
```

## Git pretty stats

```bash
# Check for git prompt
if [[ `type -t __git_ps1` != 'function' ]]
then
   # Enable git prompt if available
   [[ -f /etc/bash_completion.d/git ]] && . /etc/bash_completion.d/git
fi
# Set shell prompt
if [[ `type -t __git_ps1` = 'function' ]]
then
   # Set git enabled prompt
   export GIT_PS1_SHOWDIRTYSTATE=1
   export GIT_PS1_SHOWSTASHSTATE=1
   export GIT_PS1_SHOWUPSTREAM='auto'
   export GIT_PS1_SHOWUNTRACKEDFILES=1
   # PS1='\n\033[32m${USER}@${HOSTNAME} \033[33m${PWD/${HOME}/~}\033[0m\[\033[31m\]$(__git_ps1)\[\033[0m\] $ '
   PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[31m\]$(__git_ps1)\[\033[00m\] \$ '

fi
```


