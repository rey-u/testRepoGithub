# testRepoGithub

## getting started
| Command                               | Action 
| :--                                   | :--
|**git** config --global user.name "*name*"   |set user name
|**git** config --global user.email "*email*" |set user email
|**git** init                           |initialize a git directory
|**git** remote add origin *URL*        |create a new remote called origin


## informational
| Command                               | Action
| :--                                   | :-- 
|**git** config --global --list         |list config settings
|**git** remote - v                     |display remote URL 
|**git** branch -a                      |list branches
|**git** status                         |View changes and staging


## common tasks
| Command                               | Action
| :--                                   | :-- 
|**git** branch *branch-name*           | Create branch with *branch-name*
|**git** checkout *branch-name*         |Work in *branch-name*
|**git** add -A                         |add all modified files to the staging area
**git** commit -m "*message*"           |commits the files in the staging area
|**git** push -u origin *branch-Name*   |
|**git** checkout master                |
|**git** pull origin master             |
|**git** merge *branch-to-be-merged*    |
|**git** branch -d *branch-to-be-deleted*  |
|**git** push origin --delete *branch-to-be-deleted*  |
|**git** push origin master             |
|**git** push --set-upstream origin master            |

## What is a commit?
   commit  
   (n) A single point in the Git history; the entire history of a project is represented as a set of interrelated commits. The word "commit" is often used by Git in the same places other revision control systems use the words "revision" or "version". Also used as a short hand for commit object.  
   (v) Storing a new snapshot of the project’s state in the Git history by creating a new commit representing the current state of the index and advancing HEAD to point at the new commit.  
Source: [gitglossary][1]

[1]: https://git-scm.com/docs/gitglossary


![git commands conceptualization](git-commands.png)


`git pull` ~= `git fetch` + `git merge FETCH_HEAD`  
`git pull` merges into the _current_ branch  
`git push` does not automatically merges
