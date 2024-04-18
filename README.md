# Git Commands

Unlock the power of Git  with this cheat sheet! Git, the free and open-source version control system behind GitHub, lets you manage your projects locally. This guide features essential Git commands for smooth sailing, from starting your project to collaborating with ease.

# * This cheat sheet covers all of the Git commands

  * ✓ Creating snapshots
  * ✓ Browsing history
  * ✓ Branching & merging
  * ✓ Collaboration using Git & GitHub

# * Creating Snapshots

 * Initializing a repository
 
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git init             | Initializing a repository                 |

 * Staging files

| Command             | Description                                |
|---------------------|----------------------------------------------|
| git add .             | Stages the current directory and all its content    |
| git add file1.txt    |  Stages a single file                     |
| git add *.txt            | Stages with a pattern                 |

  * Viewing the status
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git status             |  Full status    |
| git status -s    |  Short status                   |


 * Committing the staged files
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git commit -m “Message”             |  Commits with a one-line message    |
| git commit    |  Opens the default editor to type a long message                  |


* Committing the staged files
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git commit -m “Message”             |  Commits with a one-line message    |
| git commit    |  Opens the default editor such as VSCode to type a long message                  |


* Committing the staged files
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git commit -m “Message”             |  Commits with a one-line message    |
| git commit    |  Opens the default editor to type a long message                  |


* Skipping the staging area
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git commit -am “Message”            |  Skipping the staging area    |


* Removing files
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git rm file1.txt            |  Removes from working directory and staging area    |
| git rm --cached file1.txt            |  Removes from staging area only    |


* Viewing the staged/unstaged changes
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git diff            |  Shows unstaged changes    |
| git diff --staged           | Shows staged changes   |


* Viewing the history
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git log            |  Full history    |
| git log --oneline           | Shows staged changes   |
| git log --all           |  provides a complete history of all commits in your local Git repository   |
| git log --graph           |  visualizes your commit history, making it easier to understand how your codebase has evolved.   |

* Viewing a commit
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git show [SHA]            |  Shows the given commit    |
| git show HEAD           | Shows the last commit   |
| git show HEAD~1           |  One steps before the last commit   |
| git show HEAD:file.txt           |  Shows the version of file.txt stored in the last commit   |

* Unstaging files (undoing git add)
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git restore --staged file.txt            |  Copies the last version of file.txt from repo to staging    |


* Discarding local changes
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git restore file.txt           |  Copies file.txt from staging area to working directory    |
| git restore .           |  Discards all local changes (except untracked files)    |
| git clean -fd           |  Removes all untracked files from staging area  |


# * Browsing History

* Viewing the history
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git log --stat           |  Shows the list of modified files    |
| git log --patch           |  Shows the actual changes (patches)   |

* Filtering the history
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git log -2           |  Shows the last 2 entries   |
| git log --author=“name”           |  Shows commits by author )   |
| git log --before=“2024-04-17”           |  Shows commits by date   |
| git log --grep=“word"           |  Commits with “word” in their message   |
| git log hash1..hash2          |  Range of commits   |
| git log file.txt           |  Commits that touched file.txt   |

* Creating an alias
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git config --global alias.lg “log --oneline"         |  Creating an alias for the "log --oneline" command   |


* Viewing a commit
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git show HEAD~2:file.txt         |  Shows the version of file stored in this commit   |

* Comparing commits
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git diff HEAD~2 HEAD         |  Shows the changes between two commits  |
| git diff HEAD~2 HEAD file.txt         |  Changes to file.txt only  |

* Finding contributors
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git shortlog         |  Finding contributors |


* Finding the author of lines
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git blame file.txt         |  Shows the author of each line in file.txt |

* Tagging
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git tag v1.0         |  Tags the last commit as v1.0 |
| git tag v1.0 [SHA]         |  Tags an earlier commit |
| git tag         |  Lists all the tags |


# * Branching & Merging

* Managing branches
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git branch "name"           |  Creates a new branch called "name"    |
| git switch "name"           |  Switches to the "name" branch   |
| git switch -C "name"           |  Creates and switches   |
| git branch -d "name"           |  Deletes the bugfix branch   |

* Comparing branches
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git log master.."name"           |  Lists the commits in the "name" branch not in master   |
| git diff master.."name"           |  Shows the summary of changes   |


* Stashing
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git stash push -m “name”          |  Creates a new stash   |
| git stash list           |  Lists all the stashes   |
| git stash show 1           |  shortcut for stash@{1}  |
| git stash apply 1           |  Applies the given stash to the working dir  |
| git stash drop 1           |  Deletes the given stash  |
| git stash clear           |  Deletes all the stashes  |

* Merging
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git merge "branch-name"          |  Merges the "branch-name" branch into the current branch   |
| git merge --no-ff "branch-name"            |  Creates a merge commit even if FF is possible   |
| git merge --squash "branch-name"            |  Performs a squash merge |
| git merge --abort           |  Aborts the merge  |


* Viewing the merged branches
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git branch --merged         |  Shows the merged branches   |
| git branch --no-merged            | Shows the unmerged branches  |

* Rebasing
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git rebase master         |  Changes the base of the current branch   |



# * Collaboration

* Cloning a repository
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git clone url           |  Cloning a repository   |


* Syncing with remotes
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git fetch origin master           |  Fetches master from origin   |
| git pull         |  Fetch + merge   |
| git push         |  Pushes master to origin   |


* Sharing tags
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git push origin v1.0           |  Pushes tag v1.0 to origin   |


* Sharing branches
    
| Command             | Description                                |
|---------------------|----------------------------------------------|
| git branch -r           | Shows remote tracking branches   |
| git push -u origin "name"          | Pushes "name" to origin   |
| git push -d origin "name"          | Removes "name" from origin   |

    














