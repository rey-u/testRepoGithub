# testRepoGithub

## getting started
| Command                               | Details 
| :--                                   | :-: 
|**git** init                           |initializes a git directory
|**git** config --global user.name "*name*"   |sets user name
|**git** config --global user.email "*email*" |sets user email
|**git** config --global --list         |lists config settings
|**git** remote add origin *URL*        |creates a new remote called origin
|**git** remote - v                     |displays remote URL 

## common tasks
| Command                               | Details 
| :--                                   | :-: 
|**git** branch -a                      | List branches
|**git** branch *branch-name*           | Create branch with *branch-name*
|**git** checkout *branch-name*         |Work in *branch-name*
|**git** status                         |View changes and staging
|**git** add -A                         |add all modified files to the staging area
**git** commit -m "*message*"           |commits the files in the staging area
|**git** push -u origin *branch-Name*   |
|**git** checkout master                |
|**git** pull origin master             |
|**git** merge *branch-to-be-merged*    |
|**git** branch -d *branch-to-be-deleted*  |
|**git** push origin --delete *branch-to-be-deleted*  |
|**git** push origin master             |

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
