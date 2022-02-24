> ### [Posted As An Answer In StackOverflow](https://stackoverflow.com/a/71192747/14427765)

# Configure VsCode as default editor for Commit Messages, Difftool, Mergetool
> ### [Full Guide Here](https://www.roboleary.net/vscode/2020/09/15/vscode-git.html)

## Add the following lines to your `.gitconfig` file:
> The default location of `.gitconfig` file is `C:\Users\USER_NAME\.gitconfig`
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
> NOTE:
> -  `-w` is mandatory, and tells `git` to wait for *vscode* to load.
> - `-n` is optional, and tells `git` to open *vscode* in a new-window.

### In case you want to configure a custom path to the editor in Windows:
You need to replace the word `code` with *Path to '.exe' of VsCode*.

For example:
```
[core]
  editor = "'C:/Users/Tal/AppData/Local/Programs/Microsoft VS Code/Code.exe'" -w -n
[diff]
  tool = vscode
[difftool "vscode"]
  cmd = "'C:/Users/Tal/AppData/Local/Programs/Microsoft VS Code/Code.exe'" -w -n --diff $LOCAL $REMOTE
[merge]
  tool = vscode
[mergetool "vscode"]
  cmd = "'C:/Users/Tal/AppData/Local/Programs/Microsoft VS Code/Code.exe'" -w -n $MERGED
```
> Note:
> - You need to surround the path with *single-quotes* `''`.
> - The slashes in the path should be *forward-slashes* `/`.

Or another example:

```
[core]
	editor = \"C:\\Users\\Tal\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" -w -n

[diff]
	tool = vscode
[difftool "vscode"]
	cmd = \"C:\\Users\\Tal\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" -w -n --diff $LOCAL $REMOTE

[merge]
	tool = vscode
[mergetool "vscode"]
	cmd = \"C:\\Users\\Tal\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" -w -n $MERGED
```


## Your `.gitconfig` may look like this after the edit (for example):

```
[user]
	name = YOUR-GITHUB-USERNAME
	email = YOUR-GITHUB-EMAIL
[http]
	postBuffer = 2097152000
[https]
	postBuffer = 2097152000
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
