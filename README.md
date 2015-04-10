#OS X Scripts
A collection of useful shell scripts for OS X. I wrote some and found some. All scripts are released under the GPLv2.

##git-completion.bash
Adds tab completion to git. Reference in your .profile:
```sh
source ~/osx-scripts/git-completion.bash
```

##git-prompt.sh
Adds git status to the command line in git repo directories. Add a reference and configuration to your .profile: (see comments in scripts to change prompt)
```sh
source ~/osx-scripts/git-prompt.sh
PROMPT_COMMAND='__git_ps1 "\u@\h:\w" "\\\$ "'
GIT_PS1_SHOWCOLORHINTS=true
```
