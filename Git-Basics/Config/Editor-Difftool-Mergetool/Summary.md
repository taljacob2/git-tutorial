# Summary of all the configuring the Editor, Difftool and Mergetool

## In the `.gitconfig` file:

For Visual-Studio difference and merge, use:
```
[diff]
	tool = vsdiffmerge
[difftool]
	prompt = true
[difftool "vsdiffmerge"]
	cmd = "'C:/Program Files (x86)/Microsoft Visual Studio/2019/Community/Common7/IDE/CommonExtensions/Microsoft/TeamFoundation/Team Explorer/vsDiffMerge.exe'" $LOCAL $REMOTE //t
	keepBackup = false
	trustExitCode = true

[merge]
	tool = vsdiffmerge
[mergetool]
	prompt = true
[mergetool "vsdiffmerge"]
	cmd = "'C:/Program Files (x86)/Microsoft Visual Studio/2019/Community/Common7/IDE/CommonExtensions/Microsoft/TeamFoundation/Team Explorer/vsDiffMerge.exe'" $REMOTE $LOCAL $BASE $MERGED //m
	keepBackup = false
	trustExitCode = true
```


For VsCode difference and merge, use:
```
[diff]
tool = vscode
[difftool "vscode"]
cmd = \"C:\\Users\\Tal\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" -w -n --diff $LOCAL $REMOTE

[merge]
tool = vscode
[mergetool "vscode"]
cmd = \"C:\\Users\\Tal\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" -w -n $MERGED
```

To Use the commit message editor as VsCode, use:

```
[core]
editor = \"C:\\Users\\Tal\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" -w -n
```

To use the commit message editor as Notepad, use:

```
[core]
editor = notepad
```
