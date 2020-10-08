# testRepoGithub

## getting started
| Command                               | Action 
| :--                                   | :--
|`git` config --global user.name "*name*"   |set user name
|`git` config --global user.email "*email*" |set user email
|`git` init                           |initialize a git directory
|`git` remote add origin *URL*        |create a new remote called origin


## informational
| Command                               | Action
| :--                                   | :-- 
|`git` config --global --list         |list config settings
|`git` remote - v                     |display remote URL 
|`git` branch -a                      |list branches
|`git` status                         |View changes and staging


## common tasks
| Command                               | Action
| :--                                   | :-- 
|`git` branch *branch-name*           |create branch with *branch-name*
|`git` checkout *branch-name*         |perform changes in *branch-name*
|`git` checkout -b *branch-name*      |create and checkout a new branch
|`git` add -A                         |add all modified files to staging
|`git` commit -m "*message*"          |commits the files in staging
|`git` push -u origin *branch-Name*   |
|`git` push --set-upstream origin master |
|`git` checkout master                |
|`git` pull origin master             |
|`git` merge *branch-name*            |
|`git` branch -d *branch-name*        | 
|`git` push origin --delete *branch-name* |
|`git` push origin master             |

## typical workflow
| Task                               | Command
| :--                                | :-- 
|create new branch to make edits     |`git` checkout -b *new-branch*
|add edits to staging and commit     |`git` add .
|                                    |`git` commit -m "*commit message*"
|move to master and update           |`git` checkout master
|                                    |`git` pull
|merge branch with updated master    |`git` merge *branch-name*
|delete working branch               |`git` branch -d *branch-name*
|push updated master to remote repo  |`git` push origin master



## What is a commit?
   commit  
   (n) A single point in the Git history; the entire history of a project is represented as a set of interrelated commits. The word "commit" is often used by Git in the same places other revision control systems use the words "revision" or "version". Also used as a short hand for commit object.  
   (v) Storing a new snapshot of the project’s state in the Git history by creating a new commit representing the current state of the index and advancing HEAD to point at the new commit.  
Source: [gitglossary][1]

[1]: https://git-scm.com/docs/gitglossary


![git commands conceptualization](git-commands.png)


`git pull` ~= `git fetch` + `git merge FETCH_HEAD`  
`git pull` merges into the _current_ branch  
`git push` does not automatically merge
