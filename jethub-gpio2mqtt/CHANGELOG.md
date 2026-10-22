# Changelog since v1.0.1
- chore: drop redundant apparmor key (true is the default) 
- fix(apparmor): scripts need rix, not ix - the interpreter must read the file

ix grants the execute transition but no read permission; a shebang
script is read by its interpreter (/bin/bash -> Permission denied).
Broke the 1.0.1 entrypoint on live systems. 
