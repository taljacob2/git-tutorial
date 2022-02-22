## Configure Settings For Git To Use Vscode As The Default Editor

- ### Configure `--global` settings
	Run the command:
	```
	git config --global --edit
	```
	and add the following lines:
	```
	[core]
	  editor = code -w -n
	[diff]
	  tool = vscode
	[difftool "vscode"]
	  cmd = code -w -n --diff $LOCAL $REMOTE
	[merge]
	  tool = vscode
	[mergetool "vscode"]
	  cmd = code -w -n $MERGED
	```

**If this doesn't work for you, please view the full guide to [Configure VsCode as default editor for Commit Messages, Difftool, Mergetool](Configure-VsCode-as-default-editor-for-Commit-Messages-Difftool-Mergetool.md).**
