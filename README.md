# GIT CHEAT SHEET

Git is open source distributed version control system.

### Git Installation

> *In Ubuntu*

    $ sudo apt-get install git

### Git Configuration

> *Configure user information for all local repositories*

Sets the name to the commit transactions
```sh
$ git config --global user.name [name]
```
Sets the email  to the commit transactions
```sh
$ git config --global user.email [email-address]
```


### CREATE REPOSITORIES

> *Start a new repository or obtain one from an existing URL*

Create a new local repository
```sh
$ git init [project-name]
```
Clone an existing repository
```sh
$ git clone [url]
```


### MAKE CHANGES
Lists all new or modified files in working directory
```sh
$ git status
```
Shows file differences not yet staged
```sh
$ git diff
```
Add all current changes to next commit
```sh
$ git add .
```

Add changes in [file] to next commit

```sh
$ git add [file]
```
Shows file differences between staging and the last file version
```sh
$ git diff --staged
```
Unstages the file, but preserve its contents
```sh
$ git reset [file]
```
Records file snapshots permanently in version history
```sh
$ git commit -m "[descriptive message]"
```

### GROUP CHANGES

> *Name a series of commits and combine completed efforts*

Lists all local branches in the current repository
```sh
$ git branch
```
Creates a new branch
```sh
$ git branch [branch-name]
```
Switch to the specified branch and update the working directory
```sh
$ git checkout [branch-name]
```
Combine the specified branch’s history into the current branch
```sh
$ git merge [branch]
```
Delete the specified branch
```sh
$ git branch -d [branch-name]
```


### REFACTOR FILENAMES
Delete the file from the working directory and stage the deletion
```sh
$ git rm [file]
```
Remove the file from version control but preserve the file locally
```sh
$ git rm --cached [file]
```
Change the file name and prepare it for commit
```sh
$ git mv [file-original] [file-renamed]
```

### SUPPRESS TRACKING

> *Exclude temporary files and paths*

```sh
*.log 
build/ 
temp-*
```

> *A text file named ***.gitignore*** suppresses accidental versioning of files*
> *and paths matching the specified patterns.*

Lists all ignored files in this project
```sh
$ git ls-files --other --ignored --exclude-standard
```


### REVIEW HISTORY

> *Browse and inspect the evolution of project files*

Lists version history for the current branch
```sh
$ git log
```
Lists version history for a file, including renames
```sh
$ git log --follow [file]
```
Shows content differences between two branches
```sh
$ git diff [first-branch]...[second-branch]
```
Outputs metadata and content changes of the specified commit
```sh
$ git show [commit]
```

### REDO COMMITS 

> *Erase mistakes and replacement history*

Undoes all commits after [commit], preserving changes locally
```sh
$ git reset [commit]
```
Discards all history and changes back to the specified commit
```sh
$ git reset --hard [commit]
```

### UPDATE AND PUBLISH
List all currently configured remote

    $ git remote -v

Show information about remote

    $ git remote show [remote]


Add new remote repository, named [remote]

    $ git remote add [shortname] [url]


Download changes and directly merge/integrate into HEAD

    $ git pull [remote] [branch]

Publish local changes to remote

     $ git push [remote] [branch]

Delete a branch on remote

    $ git branch -dr [remote/branch]
