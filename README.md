#OS X Scripts
A collection of useful shell scripts for OS X. I found some and wrote some. All scripts are released under the GPLv2 unless it mentions otherwise in the comments.

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

##screensaver.sh
Fixes a screensaver timeout policy that is too short. Create a plist file with the following contents in your launchctl folder (~/Library/LaunchAgent/screensaver.plist) and it will run on a schedule:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN"
  "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>Label</key>
    <string>screensaver</string>
    <key>ProgramArguments</key>
    <array>
        <string>~/osx-scripts/screensaver.sh</string>
    </array>
    <key>StartInterval</key>
    <integer>240</integer>
</dict>
</plist>
```
